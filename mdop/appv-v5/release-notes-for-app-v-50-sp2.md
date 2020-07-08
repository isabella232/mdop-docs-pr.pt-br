---
title: Notas de versão do App-V 5.0 SP2
description: Notas de versão do App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796222"
---
# Notas de versão do App-V 5.0 SP2


**Para procurar um problema específico nestas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o App-V 5,0 SP2.

Estas notas da versão contêm informações necessárias para instalar com êxito o App-V 5,0 SP2. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver diferenças entre essas notas de versão e outras documentações do App-V 5,0, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Sobre a documentação do produto


Para obter informações sobre a documentação do App-V 5,0, consulte a home page do App-V 5,0 no Microsoft TechNet.

## Fornecer comentários


Estamos interessados em seus comentários sobre o App-V 5,0. Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .

**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras na nossa documentação e nas versões do produto.

 

Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conhecidos com o pacote de hotfix 4 para Application Virtualization 5,0 SP2


### Os pacotes param de funcionar após a desinstalação do pacote de hotfix 4 para Application Virtualization 5,0 SP2

Pacotes publicados quando o pacote de hotfix 4 para Application Virtualization 5,0 SP2 é aplicado pare de funcionar quando o pacote de hotfix 4 para o Application Virtualization 5,0 SP2 é removido.

POSSÍVEIS

Se a seguinte pasta existir, você deverá excluí-la:

**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Cliente**  \\  **VFS**  \\  ** &lt; ID &gt; do pacote** para cada pacote publicado.

**Observação**  Você deve ter privilégios elevados para excluir esta pasta.

 

Para usar um script, para cada conta de usuário no computador e para cada ID de pacote publicada após a instalação do pacote de hotfix 4 para o Application Virtualization 5,0 SP2:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   Os atalhos permanecerão com as sessões de usuário mesmo após a exclusão da pasta do diretório na seção anterior, para que você possa clicar no atalho para executar o aplicativo novamente. Não é necessário publicar o aplicativo novamente.

-   Esse problema ocorre para os dois usuários publicados no pacote e em pacotes publicados globalmente por exemplo, Microsoft Office2013. A pasta deve ser excluída para ambos os tipos de pacotes.

-   Você não precisa excluir a pasta VFS nos dados do aplicativo de roaming (**% AppData%**). Somente o **% LocalAppData%** deve ser excluído.

### Pontos de integração do Microsoft Office com local de sistema de arquivos incorreto

A integração do Microsoft Office aponta para um local incorreto do sistema de arquivos (Groove.exe mensagem de erro).

POSSÍVEIS

Use um dos seguintes métodos:

1.  Exclua o atalho na pasta inicialização após a atualização.

2.  Altere o atalho na pasta inicialização usando um script.

3.  Use o arquivo de configuração de implantação para especificar o destino do atalho para a raiz de integração.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> Pacote de hotfix 4 para o Application Virtualization 5,0 o instalador do SP2 pode levar muito tempo

O pacote de hotfix 4 para o instalador do SP2 do Application Virtualization 5,0 pode levar muito tempo, dependendo da quantidade de arquivos armazenados no cache do pacote existente.

A atualização dos descritores de segurança do pacote associado durante o pacote de hotfix 4 para a instalação do Application Virtualization 5,0 SP2 tem um impacto significativo na duração da instalação. Anteriormente, a instalação da instalação era padrão em Duration. No entanto, ele depende de quantos arquivos você fez no cache do pacote.

SOLUÇÃO alternativa: nenhum

### Desinstalação do pacote de hotfix 4 para Application Virtualization 5,0 SP2 falha se o pacote do JIT-V estiver em uso

Se você instalar o pacote de hotfix 4 para o Application Virtualization 5,0 SP2 e tentar desinstalar o hotfix quando a virtualização just-in-time (JIT-V) estiver sendo usada, a operação falhará se todas as seguintes condições forem verdadeiras:

-   Você instalou usando um arquivo do Windows Installer (. msi) e, em seguida, aplica atualizações usando um arquivo de patch do instalador da Microsoft (. msp).

-   Você tenta desinstalar uma atualização usando o item Adicionar ou remover programas no painel de controle.

-   Um pacote habilitado para JIT-V está em execução no computador.

SOLUÇÃO alternativa: conclua as seguintes etapas:

1.  Abra o Windows PowerShell e execute os seguintes comandos:

    -   **Import-Module appvclient**

    -   **Get-AppvClientPackage | Parar-AppvClientPackage**

2.  Desinstale a atualização usando Adicionar ou remover programas.

## Problemas conhecidos com o App-V 5,0 SP2


### <a href="" id="bkmk-folderredirection"></a>O redirecionamento de pastas do cliente App-V também falha ao mover arquivos de% AppData% para% LocalAppData%

Quando% AppData% é uma pasta de rede compartilhada que você configurou para o redirecionamento de pastas, as alterações que os usuários finais fazem em AppData (roaming) podem ser perdidas ao alternar entre computadores ou quando seus AppData locais são desmarcadas quando eles fazem logoff e logon novamente. Esse erro ocorre porque a chave do registro (AppDatatime), que indica o último carregamento conhecido, fica fora da sincronização com os AppData armazenados em cache.

SOLUÇÃO alternativa: exclua manualmente a seguinte chave do registro para cada pacote relevante quando um usuário final fizer logon ou logoff:

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

Na primeira vez que os usuários finais iniciarem um aplicativo no pacote depois de entrarem, o App-V força o download do% AppData% AppData%, mesmo se% LocalAppData% já estiver atualizado.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> App-V 5,0 Service Pack 2 (App-V 5,0 SP2) não inclui uma nova versão do App-V Server

O App-V 5.0 SP2 não inclui uma nova versão do App-V Server. Se você implanta clientes do App-V 5,0 SP2 executando o Windows 8,1 em seu ambiente e planeja gerenciar os clientes usando a infraestrutura do App-V, instale o [pacote de hotfix 2 para o Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634). (https://go.microsoft.com/fwlink/?LinkId=386634)

Se você estiver executando e Gerenciando clientes do App-V 5,0 SP2 usando qualquer um dos seguintes métodos, nenhuma atualização de cliente será necessária:

-   Modo autônomo.

-   Gerenciador de Configurações.

-   ESD de terceiros.

O cliente do App-V 5,0 SP2 é totalmente compatível com o Windows 8,1

SOLUÇÃO alternativa: nenhum.

## Informações de direitos autorais da versão


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft. Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.








## Tópicos relacionados


[Sobre o App-V 5.0 SP2](about-app-v-50-sp2.md)

 

 





