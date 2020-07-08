---
title: Notas de versão do MBAM 2.5
description: Notas de versão do MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799581"
---
# Notas de versão do MBAM 2.5


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM e podem conter informações que não estão disponíveis na documentação do produto. Se estas notas de versão forem diferentes de outras documentações do MBAM 2,5, considere as alterações mais recentes a serem autoritativas. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## <a href="" id="---------mbam-2-5-known-issues"></a> MBAM 2,5 problemas conhecidos


Esta seção contém notas de versão do MBAM 2,5.

### Navegador da Web executado de forma não intencional como administrador

Os links de ajuda na ferramenta de configuração do MBAM Server podem fazer com que as janelas do navegador sejam abertas com direitos de administrador.

**Solução alternativa:** Habilitar a configuração de segurança reforçada do Internet Explorer (IESC) ou fechar o navegador da Web antes de navegar para outros sites.

**Observação**  Isso foi corrigido no MBAM 2,5 SP1.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> MBAM relatórios como não compatíveis um cliente criptografado com chaves de criptografia AES de 256 bits e difusor

Se um computador tiver o cliente do MBAM 2,5 instalado e for criptografado usando o AES de 256 bits com força de codificação do difusor, o cliente MBAM será relatado como não compatível nos relatórios de conformidade do MBAM.

**Solução alternativa:** Instale o hotfix em [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> O MBAM não criptografa um volume e informa um erro se você definir um protetor TPM + PIN em um dispositivo tablet

Se os usuários finais tentarem definir um protetor TPM + PIN em um dispositivo tablet, o MBAM não criptografará, e ele reportará um erro. Esse problema ocorre porque os dispositivos Tablet não têm um teclado de ambiente de pré-inicialização.

**Solução alternativa:** Habilite o **uso da autenticação do BitLocker exigindo a entrada do teclado de pré-inicialização na configuração da política de grupo do tablets** . Essa configuração é uma configuração de política de grupo do BitLocker e não está disponível nos modelos de política de grupo do MBAM.

### O nome UPN do usuário é necessário para todas as contas de serviço

Um nome UPN deve ser definido para todas as contas de serviço no MBAM. Se você não conseguir criar um UPN para uma conta, uma mensagem de erro aparecerá durante o processo de configuração para indicar que o usuário ou grupo não foi encontrado no Active Directory.

**Solução alternativa:** Adicione o UPN à conta de serviço.

### O portal de autoatendimento requer configuração adicional se os computadores cliente não puderem acessar a rede de distribuição de conteúdo do Microsoft Ajax

Se seus computadores cliente não tiverem acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, você deve configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível. Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, somente o nome da empresa e a conta na qual você fez logon será exibido. Nenhuma mensagem de erro será exibida.

**Solução alternativa:** Instale o MBAM 2,5 SP1. ou configure o portal de autoatendimento seguindo estas instruções: [como configurar o portal de autoatendimento quando os computadores cliente não conseguem acessar a rede de distribuição de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).

### O portal de autoatendimento e o site de administração e monitoramento não abrem após a atualização do IIS para o .NET Framework 4,5

Quando você atualiza os serviços de informações da Internet (IIS) para o Microsoft .NET Framework 4,5, o portal de autoatendimento e o site de administração e monitoramento não abrem.

**Solução alternativa:** Veja a mensagem de erro do artigo [depois de instalar o .NET Framework 4,0: "não foi possível carregar o tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).

### Site de administração e monitoramento exibe uma mensagem de erro "não é possível encontrar o relatório" quando os relatórios não estão configurados

Se você configurar o site de administração e monitoramento e, em seguida, tentar exibir um relatório sem configurar o recurso relatórios primeiro, uma mensagem de erro indicará que o relatório não foi encontrado.

**Solução alternativa:** Configure o recurso relatórios antes de configurar os aplicativos Web.

### Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS

Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL do recurso de relatórios será definida como HTTP em vez de HTTPS quando você configurar o servidor MBAM. Se, em seguida, você abrir o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem de erro será exibida: "somente conteúdo seguro é exibido".

**Solução alternativa:** Para mostrar o relatório, clique em **mostrar todo o conteúdo**. Para corrigir esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**. Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.

### Clicar em "retornar" no relatório de Resumo de conformidade do BitLocker pode gerar um erro

Se você fizer buscas detalhadas em um relatório de Resumo de conformidade do BitLocker e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.

**Solução alternativa:** Nenhuma.

### O espaço usado apenas a criptografia não funciona corretamente

Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver configurado uma configuração de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco. Se um computador já está criptografado com espaço usado apenas quando você instala o cliente MBAM e configurou a mesma configuração de política de grupo, MBAM informa que a unidade está criptografada corretamente e não tenta criptografar novamente a unidade.

**Solução alternativa:** Nenhuma.

### O nível de codificação é exibido incorretamente no relatório de conformidade do computador BitLocker

Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação de codificação** , o relatório de conformidade do computador BitLocker na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits. O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.

**Solução alternativa:** Defina sempre um nível de codificação específico no objeto **escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação.

### A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração

Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.

**Solução alternativa:** Nenhuma. Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.

### A configuração de segurança reforçada pode fazer com que os relatórios exibam uma mensagem de erro incorretamente

Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de erro "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM. Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.

**Solução alternativa:** Se a mensagem de erro "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada. Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>Hotfixes e artigos da base de dados de conhecimento da MBAM 2,5


Esta tabela lista os hotfixes e artigos da KB para o MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artigo do KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2975636</p></td>
<td align="left"><p>Pacote de hotfix 1 para administração e monitoramento do Microsoft BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>Pacote de hotfix 2 para administração e monitoramento de BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>A instalação do MBAM 2,5 ou o relatório do Configuration Manager falha se o nome da instância do SSRS contiver um sublinhado</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>O cliente MBAM falharia com a ID de evento 4 e o código de erro 0x8004100E na descrição do evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Erro ao abrir relatórios corporativos ou de conformidade de computador no MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>A instalação do MBAM 2,0 falha durante o cenário de integração do Configuration Manager com o SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>Deadlocks SQL quando muitos clientes MBAM se conectam ao banco de dados de recuperação do MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados


[Sobre o MBAM 2.5](about-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





