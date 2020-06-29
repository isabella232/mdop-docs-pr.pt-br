---
title: Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores
description: Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796078"
---
# Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores


Este tópico descreve o processo de atualização do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) e do cliente MBAM de versões anteriores do MBAM.

**Observação**  Você pode atualizar diretamente para o MBAM 2,5 ou o MBAM 2,5 SP1 a partir de qualquer versão anterior do MBAM.

 

## Antes de iniciar a atualização


Revise as informações a seguir antes de iniciar a atualização.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que saber antes de começar</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se você estiver instalando os sites do MBAM em um servidor e os serviços Web em outro servidor, será necessário usar cmdlets do Windows PowerShell para configurá-los.</p></td>
<td align="left"><p>O assistente de configuração do servidor do MBAM não dá suporte à configuração dos sites em um servidor e nos serviços Web em um servidor diferente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Se você estiver atualizando para o MBAM 2.5 ou o 2,5 SP1 do MBAM 2.0 ou do 2,0 SP1 no Windows Server2008 R2:</p>
<p>O site de administração e monitoramento e o portal de autoatendimento não funcionarão se você instalar o software .NET Framework 4.5 necessário após a instalação dos serviços de informações da Internet (IIS).</p>
<p>Esse problema ocorre porque o ASP.NET não pode ser registrado corretamente com o IIS se o .NET Framework estiver instalado depois que o IIS já estiver instalado.</p></td>
<td align="left"><p><strong>Para resolver este problema:</strong></p>
<p>Execute <strong> aspnet_regiis – i </strong> do seguinte local:</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>Para obter mais informações, consulte: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.net a ferramenta de registro do IIS </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre um SPN na conta do pool de aplicativos se todas as seguintes opções forem verdadeiras:</p>
<ul>
<li><p>Você estiver atualizando de uma versão anterior do MBAM.</p></li>
<li><p>Atualmente, você não está executando os sites do MBAM em uma configuração de carga balanceada ou distribuída, mas quer fazer isso quando atualizar para o MBAM 2.5 ou 2,5 SP1.</p></li>
</ul></td>
<td align="left"><p>Para obter instruções, consulte <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planejando como proteger os sites do MBAM </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>O que recomendamos</strong></p></td>
<td align="left"><p>Registre um SPN (nome da entidade de serviço) para a conta do pool de aplicativos, mesmo que você já tenha registrado SPNs para a conta do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Por que recomendamos</strong></p></td>
<td align="left"><p>O registro de um SPN na conta do pool de aplicativos é necessário para configurar os sites em uma configuração balanceada ou de balanceamento de carga.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>O que acontece se os SPNs já estiverem configurados em uma conta de máquina?</strong></p></td>
<td align="left"><p>O MBAM usará os SPNs que você já registrou e não precisará configurar SPNs adicionais, mas não é possível configurar os websites em uma configuração balanceada ou distribuída.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## Etapas para atualizar a infraestrutura do MBAM Server


Use as etapas das seções a seguir para atualizar o MBAM para a topologia autônoma ou a topologia de integração do System Center Configuration Manager.

**Para atualizar a infraestrutura do MBAM Server para topologia autônoma**

1.  Desinstale as versões anteriores do MBAM em **programas e recursos** e em servidores Web para garantir que as informações não sejam gravadas de clientes do MBAM na infraestrutura MBAM. Para obter instruções, consulte [removendo recursos ou software do MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Faça backup de seus bancos de dados.

3.  Desinstale as versões anteriores do MBAM a partir do SQL Server usando **programas e recursos**, incluindo SQL Servers que hospedam os relatórios do MBAM por meio do SQL Server Reporting Services. Remova todas as pastas ou arquivos temporários restantes do servidor do MBAM do servidor de banco de dados e do Reporting Services.

    **Observação**  Os bancos de dados não serão removidos, e todos os dados de conformidade e recuperação serão mantidos no banco de dados.

     

4.  Instale e configure os bancos de dados, relatórios e aplicativos Web do MBAM 2.5 ou do 2,5 SP1, nessa ordem. Os bancos de dados estão atualizados no local.

5.  Atualize os objetos de política de grupo (GPOs) usando os modelos do MBAM 2,5 para aproveitar os novos recursos do MBAM, como a criptografia imposta. Se você não atualizar os GPOs e o cliente do MBAM para o MBAM 2,5, as versões anteriores dos clientes MBAM continuarão a se comunicar com seus GPOs atuais com funcionalidade reduzida. Veja [como obter modelos de política de grupo do MDOP (. admx)](https://www.microsoft.com/download/details.aspx?id=41183) para baixar os modelos ADMX mais recentes.

    Depois de atualizar a infraestrutura do MBAM Server, os computadores cliente existentes continuam a ser reportados com êxito para o servidor MBAM 2.5 ou 2,5 SP1, e os dados de recuperação continuam a ser armazenados.

6.  Instale o cliente mais recente do MBAM 2.5 ou do 2,5 SP1. Os computadores cliente não precisam ser reiniciados após a implantação.

**Para atualizar a infraestrutura do MBAM para a topologia de integração do System Center Configuration Manager**

1.  Desinstale as versões anteriores do MBAM em **programas e recursos** e em servidores Web para garantir que as informações não sejam gravadas de clientes do MBAM na infraestrutura MBAM. Para obter instruções, consulte [removendo recursos ou software do MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Faça backup de seus bancos de dados.

3.  Desinstale as versões anteriores do MBAM a partir do SQL Server usando **programas e recursos**, incluindo SQL Servers que hospedam os relatórios do MBAM por meio do SQL Server Reporting Services. Remova todas as pastas ou arquivos temporários restantes do servidor do MBAM do servidor de banco de dados e do Reporting Services.

4.  Desinstale o MBAM do servidor do Configuration Manager.

    **Observação**  Os bancos de dados e os objetos do Configuration Manager (linha de base, coleção de computadores com suporte MBAM e relatórios) não serão removidos, e todos os dados de conformidade e recuperação serão mantidos no banco de dados.

     

5.  Atualize os arquivos. mof.

6.  Instale e configure os bancos de dados do MBAM 2.5 ou do 2,5 SP1, relatórios, aplicativos Web e a integração do Configuration Manager nesta ordem. Os objetos de bancos de dados e do Configuration Manager são atualizados em vigor.

7.  Opcionalmente, atualize os objetos de política de grupo (GPOs) e edite as configurações se desejar implementar novos recursos no MBAM, como a criptografia imposta. Se você não atualizar os GPOs, o MBAM continuará a se comunicar com seus GPOs atuais. Veja [como obter modelos de política de grupo do MDOP (. admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) para baixar os modelos ADMX mais recentes.

    Depois de atualizar a infraestrutura do MBAM Server, os computadores cliente existentes continuam a ser reportados com êxito para o servidor MBAM 2.5 ou 2,5 SP1, e os dados de recuperação continuam a ser armazenados.

8.  Instale o cliente mais recente do MBAM 2.5 ou do 2,5 SP1. Os computadores cliente não precisam ser reiniciados após a implantação.

## Suporte de atualização para o cliente MBAM


O MBAM dá suporte a atualizações para o cliente do MBAM 2.5 de qualquer versão anterior do cliente MBAM.

**Maneiras de instalar o cliente MBAM:**

-   Atualize os computadores que executam o cliente do MBAM de uma vez ou gradualmente após a instalação da infraestrutura de servidor do MBAM 2.5.

-   Instale o cliente do MBAM por meio de um sistema de distribuição de software eletrônico ou de ferramentas, como os serviços de domínio do Active Directory ou o System Center Configuration Manager.



## Tópicos relacionados


[Implantando o MBAM 2.5](deploying-mbam-25.md)

[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





