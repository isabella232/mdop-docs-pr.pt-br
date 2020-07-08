---
title: Notas de versão do App-V 5.1
description: Notas de versão do App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796217"
---
# Notas de versão do App-V 5.1


Estes são problemas conhecidos do Microsoft Application Virtualization (App-V) 5,1.

## Erro durante a atualização de publicação entre o aplicativo de gerenciamento do App-V 5,0 e o cliente do App-V 5,1 no Windows 10


Um erro é gerado durante a atualização de publicação durante a sincronização de pacotes do servidor de gerenciamento do App-V 5,0 SP3 para um cliente do App-V 5,1 no Windows 10. Esse erro ocorre porque o servidor do App-V 5,0 SP3 não compreende o sistema operacional Windows 10 especificado na URL de publicação. O problema foi corrigido para o servidor de publicação do App-V 5,1, mas não está reportado para versões do App-V 5,0 SP3 ou anterior.

**Solução alternativa**: Atualize o servidor de gerenciamento do App-v 5,0 para o servidor de gerenciamento do App-v 5,1 para clientes do Windows 10.

## Configurações personalizadas não são aplicadas para pacotes que serão publicados globalmente se estiverem definidas usando o servidor do App-V 5,1


Se você atribuir um pacote a um grupo de anúncios que contém contas do computador e aplicar uma configuração personalizada ao grupo usando o App-V Server, a configuração personalizada não será aplicada a essas máquinas. O cliente App-V 5,1 publicará pacotes atribuídos a uma conta de máquina globalmente. No entanto, ele armazena arquivos de configuração personalizada por usuário em cada perfil de usuário. Os pacotes publicados globalmente não terão acesso a essa configuração personalizada.

**Solução alternativa**: siga um destes procedimentos:

-   Atribua o pacote a grupos que contenham apenas contas de usuário. Isso garantirá que a configuração personalizada do pacote será armazenada no perfil de cada usuário e será aplicada corretamente.

-   Crie um arquivo de configuração de implantação personalizado e aplique-o ao pacote no cliente usando o cmdlet Add-AppvClientPackage com o parâmetro – DynamicDeploymentConfiguration. Consulte [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md) para obter mais informações.

-   Crie um novo pacote com a configuração personalizada usando o sequenciador do App-V 5,1.

## Arquivos do servidor não excluídos após a instalação do novo App-V 5,1 Server


Se você desinstalar o servidor App-V 5,0 SP1 e instalar o aplicativo App-V 5,1, a instalação falha, a versão errada do servidor de gerenciamento é instalada e uma mensagem de erro é retornada. O problema ocorre porque os arquivos do servidor não estão sendo excluídos ao desinstalar o App-V 5,0 SP1, portanto, o processo de instalação faz uma atualização em vez de uma nova instalação.

**Solução alternativa**: exclua esta chave do registro antes de começar a instalar o App-V 5,1:

Em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, localize e exclua a chave GUID de instalação que contém o valor DWORD "DisplayName" com dados de valor "Microsoft Application Virtualization (App-V) Server". Essa é a única tecla que deve ser excluída.

## Associações de tipo de arquivo adicionadas manualmente não são salvas corretamente


Associações de tipo de arquivo adicionadas manualmente a um pacote de aplicativo usando a guia atalhos e FTAs no final do assistente de atualização de aplicativos não são salvas corretamente. Elas não estarão disponíveis para o cliente App-V ou para o sequenciador ao atualizar o pacote salvo novamente.

**Solução alternativa**: para adicionar uma associação de tipo de arquivo, abra o pacote para modificação e execute o assistente de atualização. Durante a etapa de instalação, adicione a nova associação de tipo de arquivo pelo sistema operacional. O sequenciador detectará a nova associação no registro do sistema e a adicionará ao registro virtual do pacote, onde ele estará disponível para o cliente.

## Ao transmitir pacotes no modo de repositório de conteúdo compartilhado (SCS) para um cliente que também é gerenciado com o AppLocker, dados adicionais são gravados no disco local.


Para reduzir a quantidade de dados gravados no disco local de um cliente, você pode habilitar o modo SCS no cliente do App-V 5,1 para transmitir o conteúdo de um pacote por demanda. No entanto, se o AppLocker gerenciar um aplicativo dentro do pacote, alguns dados podem ser gravados no disco local do cliente que, de outra forma, não seriam gravados.

**Solução alternativa**: nenhum

## Na caixa de diálogo Adicionar pacote ao console de gerenciamento, o botão procurar não está disponível ao usar o Chrome ou Firefox


Na página pacotes do console de gerenciamento, se você clicar em **Adicionar ou atualizar** no canto inferior direito, a caixa de diálogo **Adicionar pacote** será exibida. Se você estiver acessando o console de gerenciamento usando o Chrome ou Firefox como navegador, não poderá navegar até o local do pacote.

**Solução alternativa**: digite ou copie e cole o caminho do pacote no campo **Adicionar pacote** de entrada. Se o console de gerenciamento tiver acesso a esse caminho, você poderá adicionar o pacote. Se o pacote estiver em um compartilhamento de rede, você poderá navegar até o local usando o explorador de arquivos seguindo estas etapas:

1.  Ao pressionar a **tecla Shift**, clique com o botão direito do mouse no arquivo do pacote

2.  Selecione **Copiar como caminho**

3.  Colar o caminho no campo de entrada da caixa de diálogo **Adicionar pacote**

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>Atualizar o servidor de gerenciamento do App-V para 5,1 às vezes falha com a mensagem "ocorreu um erro de banco de dados"


Se você instalar o servidor de gerenciamento do App-V 5,0 SP1 e, em seguida, tentar atualizar para o App-V 5,1 Server quando vários grupos de conexão estiverem configurados e habilitados, o seguinte erro será exibido: "ocorreu um erro de banco de dados. Motivo: ' nome de coluna inválido ' PackageOptional '. Nome de coluna inválido ' VersionOptional '. "

**Solução alternativa**: Execute este comando no seu banco de dados SQL:

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

onde "AppVManagement" é o nome do banco de dados.

## Os usuários não podem abrir um pacote em um grupo de conexão publicada pelo usuário se você adicionar ou remover um pacote opcional


Em ambientes que executam o cliente RDS ou que têm vários usuários simultâneos por computador, os usuários conectados não podem abrir aplicativos em pacotes que estejam em um grupo de conexão publicada pelo usuário se um pacote opcional for adicionado ou removido do grupo de conexão.

**Solução alternativa**: faça com que os usuários façam logoff e, em seguida, faça logon novamente.

## A mensagem de erro é exibida erroneamente quando o grupo de conexão é publicado somente para o usuário


Quando você executa o Repair-AppvClientConnectionGroup, o seguinte erro é exibido, mesmo quando o grupo de conexão é publicado somente para o usuário: "erro de integração interno do App-V: pacote não integrado para o usuário. Certifique-se de que o pacote seja adicionado ao computador e publicado ao usuário. "

**Solução alternativa**: siga um destes procedimentos:

-   Publicar todos os pacotes em um grupo de conexão.

    O problema surge quando o grupo de conexão que está sendo reparada tem pacotes que estão ausentes ou não estão disponíveis para o usuário (ou seja, não são publicados globalmente ou para o usuário). No entanto, o reparo funcionará se todos os pacotes do grupo de conexão estiverem disponíveis, portanto, certifique-se de que todos os pacotes sejam publicados.

-   Reparar pacotes individualmente usando o comando Repair-AppvClientPackage em vez do comando Repair-AppvClientConnectionGroup.

    Determine quais pacotes estão disponíveis para os usuários e execute o comando Repair-AppvClientPackage uma vez para cada pacote. Use cmdlets do PowerShell para fazer o seguinte:

    1.  Obter todos os pacotes em um grupo de conexão.

    2.  Verifique se cada pacote está publicado no momento.

    3.  Se o pacote estiver publicado no momento, execute Repair-AppvClientPackage nesse pacote.

## Ícones não exibidos corretamente no sequenciador


Os ícones na guia atalhos e associações de tipo de arquivo não são exibidos corretamente ao modificar um pacote no sequenciador App-V. Esse problema ocorre quando o tamanho dos ícones não é 16x16 ou 32x32.

**Solução alternativa**: Use apenas ícones que sejam 16x16 ou 32x32.

## O script InsertVersionInfo. SQL não é mais necessário para o banco de dados de gerenciamento


O script InsertVersionInfo. SQL não é necessário para versões do banco de dados de gerenciamento do App-V posterior à App-V 5,0 SP3.

O script Permissions. SQL deve ser atualizado de acordo com a **etapa 2** no [artigo do KB 3031340](https://support.microsoft.com/kb/3031340).

**Importante** 
 A **etapa 1** não é necessária para versões do App-v posteriores ao app-v 5,0 SP3.

 

## Microsoft Visual Studio 2012 não suportado


O App-V 5,1 não oferece suporte ao Visual Studio 2012.

**Solução alternativa**: nenhum

## Restrições de nome de arquivo do aplicativo para o App-V 5. x Sequencer


O sequenciador App-V 5. x não pode sequenciar aplicativos com nomes de filecorrespondentes a "CO_ &lt; x &gt; ", onde x é qualquer numeral. O erro 0x8007139F será gerado.

**Solução alternativa**: Use um nome de arquivo diferente

## Erro intermitente "arquivo não encontrado" ao montar um pacote


Às vezes, ao montar um pacote, um erro de "arquivo não encontrado" (0x80070002) é gerado. Geralmente, isso ocorre quando uma pasta em um pacote do App-V contém muitos arquivos (por exemplo, 20K ou mais). Isso pode fazer com que o fluxo de transmissão demorasse mais tempo do que o esperado e até o tempo limite que gera o erro "arquivo não encontrado".

**Solução alternativa**: Iniciando com HF06, uma nova chave do registro foi introduzida para habilitar a extensão desse período de tempo limite.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">Caminho</td>
<td align="left">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</td>
</tr>
<tr>
<td align="left">Configuração</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">UDT</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">Americanas</td>
<td align="left">Second</td>
</tr>
<tr>
<td align="left">Padrão</td>
<td align="left">5<br />
<strong>Observação </strong> : esse valor será o padrão se a chave do registro não for definida ou um valor &lt; = 5 for especificado.
</td>
</tr>
</tbody>
</table>






## Tópicos relacionados


[Sobre o App-V 5.1](about-app-v-51.md)

 

 





