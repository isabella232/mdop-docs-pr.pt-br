---
title: Planejamento de formas para proteger os sites do MBAM
description: Planejamento de formas para proteger os sites do MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799589"
---
# Planejamento de formas para proteger os sites do MBAM


Este tópico descreve os métodos a seguir para proteger o site de administração e monitoramento do Microsoft BitLocker (MBAM) 2,5 para o site de administração e o portal de autoatendimento:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Obrigatório ou opcional?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usar certificados para proteger sites do MBAM</p></td>
<td align="left"><p>Opcional, mas altamente recomendado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrando o SPN (nomes de entidade de serviço) para a conta do pool de aplicativos</p></td>
<td align="left"><p>Obrigatório</p></td>
</tr>
</tbody>
</table>



Para obter mais informações sobre como proteger sua implantação do MBAM, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md).

## Usar certificados para proteger sites do MBAM


Recomendamos que você use um certificado para proteger a comunicação entre:

-   Cliente MBAM e os serviços Web

-   Navegador e o site de administração e monitoramento e sites de portal de autoatendimento

Para saber mais sobre como solicitar e instalar um certificado, consulte [Configurando certificados do servidor de Internet](https://technet.microsoft.com/library/cc731977.aspx).

**Observação**  
Você pode configurar os sites e serviços Web em servidores diferentes somente se você estiver usando o Windows PowerShell. Se você usar o assistente de configuração do servidor do MBAM para configurar os sites, você deve configurar os sites e os serviços Web no mesmo servidor.



Para proteger a comunicação entre os serviços Web e os bancos de dados, também recomendamos que você force a criptografia no SQL Server. Para obter informações sobre como proteger todas as conexões com o SQL Server, incluindo a comunicação entre os serviços Web e o SQL Server, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).

## Registrando SPNs para a conta do pool de aplicativos


Para habilitar os servidores MBAM para autenticar a comunicação a partir do site de administração e monitoramento e do portal de autoatendimento, você deve registrar um SPN (nome da entidade de serviço) para o nome do host na conta de domínio que você está usando para o pool de aplicativos Web.

Este tópico contém instruções sobre como registrar SPNs para os seguintes tipos de nomes de host:

-   Nome de domínio totalmente qualificado

-   Nome NetBIOS

-   Nome virtual

### Antes de criar SPNs para uma instalação inicial do MBAM

Revise as informações na tabela a seguir antes de começar a criar SPNs.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa ou item</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crie uma conta de serviço nos serviços de domínio Active Directory (AD DS).</p></td>
<td align="left"><p>A conta de serviço é uma conta de usuário que você cria no AD DS para fornecer segurança para os sites do MBAM. Os sites do MBAM são executados em um pool de aplicativos cuja identidade é o nome da conta de serviço. Em seguida, os SPNs são registrados na conta do pool de aplicativos.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você deve usar a mesma conta de pool de aplicativos para todos os servidores Web.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Verifique se a conta de grupo IIS-IUSRS ou a conta de pool de aplicativos recebeu os direitos necessários.</p></td>
<td align="left"><p>Para verificar isso, siga estas etapas:</p>
<ol>
<li><p>Abra o <strong> Editor de política de segurança local </strong> e expanda o <strong> nó Diretivas locais </strong> .</p></li>
<li><p>Selecione o <strong> nó atribuição de direitos de usuário </strong> e, em seguida, clique duas vezes no painel direito, clique em <strong> representar um cliente após autenticação </strong> e <strong> logon como um trabalho em lotes </strong> .</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Se você configurar os sites do MBAM usando uma conta de administrador de domínio, o MBAM criará os SPNs para você.</p></td>
<td align="left"><p>Se você configurar os sites do MBAM usando uma conta de administrador de domínio, siga as etapas neste tópico para registrar os SPNs manualmente para o tipo de nome de host que você está usando.</p></td>
</tr>
</tbody>
</table>



### Registrando SPNs quando você usa um nome de host de domínio totalmente qualificado

Se você usar um nome de host de domínio totalmente qualificado ao configurar o MBAM, será necessário registrar apenas um SPN, conforme mostrado no exemplo a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que você precisa fazer</th>
<th align="left">Exemplos e mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registre um SPN para o nome de domínio totalmente qualificado.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>O nome totalmente qualificado do host é <strong> mybitlockerrecovery.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure a delegação restrita para o SPN que você está registrando para a conta do pool de aplicativos.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuração da delegação restrita</a></p>
<p>Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### Registrando SPNs quando você usa um nome de host NetBIOS

Se você usar um nome de host NetBIOS ao configurar o MBAM, registre um SPN para o nome NetBIOS e outro SPN para o nome de domínio totalmente qualificado, conforme mostrado nos exemplos a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que você precisa fazer</th>
<th align="left">Exemplos e mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registre um SPN para o nome do host NetBIOS.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>O nome do host NetBIOS é <strong> nbname01 </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre um SPN para o nome de domínio totalmente qualificado.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>O nome de domínio totalmente qualificado é <strong> nbname01.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure a delegação restrita para os SPNs que você está registrando para a conta do pool de aplicativos.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuração da delegação restrita</a></p>
<p>Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Registrando SPNs quando você usa um nome de host virtual

Se você configurar o MBAM com um nome de host virtual que é um nome de domínio totalmente qualificado, registre apenas um SPN para o nome do host virtual. Se o nome do host virtual que você configurar não for um nome de domínio totalmente qualificado, você deve criar um segundo SPN que especifica o nome de domínio totalmente qualificado, conforme descrito nos exemplos a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que você precisa fazer</th>
<th align="left">Exemplos e mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se o seu nome de host virtual for um nome de domínio totalmente qualificado, como neste exemplo, registre apenas um SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>No exemplo, o nome do host virtual é <strong> mbamvirtual.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre esse SPN adicional se seu nome de host virtual não for um nome de domínio totalmente qualificado.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>No exemplo, o nome do host virtual é <strong> mbamvirtual </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre esse SPN adicional se seu nome de host virtual não for um nome de domínio totalmente qualificado.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>No exemplo, o nome do host virtual é <strong> mbamvirtual.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>No servidor DNS (servidor de nomes de domínio), crie um "registro A" para o nome de host personalizado e o aponte para um servidor Web ou um balanceador de carga.</p></td>
<td align="left"><p>Consulte a seção "Configurar registros de um host DNS" em <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> Configurar registros de host DNS </a> .</p>
<p>Recomendamos que você use registros em vez de CNAMEs. Se você usar CNAMEs para apontar para o endereço de domínio, também deverá registrar os SPNs para o nome do servidor Web na conta do pool de aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure a delegação restrita para os SPNs que você está registrando para a conta do pool de aplicativos.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuração da delegação restrita</a></p>
<p>Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Registrando um SPN durante a atualização de versões anteriores do MBAM

Conclua as etapas nesta seção apenas se desejar:

-   Atualize a partir de uma versão anterior do MBAM.

-   Execute os sites no MBAM 2,5 em uma configuração de carga balanceada ou distribuída e, no momento, você está executando em uma configuração que não está equilibrada para a carga.

Se você já registrou SPNs na conta do computador, em vez de em uma conta de pool de aplicativos, o MBAM usa os SPNs existentes, e você não pode configurar os websites em uma configuração de carga balanceada ou distribuída.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que você precisa fazer</th>
<th align="left">Exemplos e mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Criar uma conta de pool de aplicativos nos serviços de domínio Active Directory (AD DS).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Remova os sites e serviços Web instalados no momento.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Removendo os recursos de servidor ou o software do MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remova os SPNs da conta do computador.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre os SPNs na conta do pool de aplicativos.</p></td>
<td align="left"><p>Siga as etapas para <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrar os SPNs quando você usar um nome de host virtual </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reconfigure os aplicativos Web e serviços Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Como configurar os aplicativos Web do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Siga um destes procedimentos, dependendo do método usado para a configuração:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Assistente de configuração do servidor do MBAM</strong></p></td>
<td align="left"><p>Digite a conta do pool de aplicativos no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Cmdlet do Windows PowerShell</p></td>
<td align="left"><p>Digite a conta no <code>WebServiceApplicationPoolCredential</code> parâmetro.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>O nome do host inserido deve ser o mesmo nome que o nome do host virtual para o qual você está criando os SPNs. Além disso, no seu farm da Web, os nomes de host e as credenciais do pool de aplicativos devem ser iguais em todos os servidores que você está configurando.</p>
</div>
<div>

</div>
<p>Quando o MBAM configura os aplicativos da Web, ele tenta registrar os SPNs para você, mas ele só pode fazer isso se você tiver direitos de administrador de domínio no servidor no qual você está instalando o MBAM. Se você não tiver esses direitos, você pode concluir a configuração, mas será necessário definir os SPNs antes ou depois de configurar o MBAM.</p></td>
</tr>
</tbody>
</table>

## Configurações de filtragem de solicitações necessárias

 ' Permitir extensões de nome de arquivo não listadas ' é necessário para que o aplicativo opere conforme o esperado.  Isso pode ser encontrado ao navegar para o ' Microsoft BitLocker Administration and Monitoring '-> solicitação de filtragem-> editar configurações de recursos.


## Tópicos relacionados


[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Pré-requisitos para implantação do MBAM 2.5](mbam-25-deployment-prerequisites.md)





## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



