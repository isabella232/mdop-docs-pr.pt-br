---
title: Como usar o arquivo SFT diferencial
description: Como usar o arquivo SFT diferencial
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796915"
---
# Como usar o arquivo SFT diferencial


Ao sequenciar um aplicativo, o sequenciador do Microsoft Application Virtualization (App-V) cria arquivos SFT (. SFT) para armazenar todos os arquivos de conteúdo e informações de configuração do aplicativo virtual. Na versão 4.5 do App-V, foi introduzido o arquivo SFT (. dsft) diferencial. Depois de usar o sequenciador para criar uma atualização para um pacote existente, você pode optar por gerar esse arquivo para armazenar apenas as diferenças entre o pacote do aplicativo sequenciado original e a nova versão. Portanto, é muito menor do que o arquivo SFT completo seria para a nova versão do aplicativo e reduz o impacto do envio de atualizações de pacote por meio de conexões de rede de baixa largura de banda. No entanto, seu uso só tem suporte em determinadas situações restritas. Esse recurso foi projetado para ser usado especificamente em que você está usando um sistema de distribuição de software eletrônico (ESD) para gerenciar um grupo de usuários com um servidor de arquivos local por meio de uma conexão de baixa largura de banda e não está usando servidores de streaming do App-V.

Você não precisará usar o arquivo SFT diferencial se estiver usando o Manager2007 de configuração para gerenciar os usuários, pois o Configuration Manager tem suporte para implantações de baixa largura de banda já incorporadas. Ele também não é necessário se você estiver usando os servidores de gerenciamento ou de streaming do Application Virtualization (App-V) com atualização ativa, pois o cliente recuperará somente as diferenças entre as versões de pacote antigo e novo.

O procedimento a seguir mostra como usar o mkdiffpkg.exe que está incluído na instalação do sequenciador para criar o arquivo SFT diferencial, após concluir a atualização do pacote de aplicativo virtual e implantar o arquivo SFT diferencial. Concluir esse procedimento ajuda a garantir que, se o pacote for descarregado de algum computador cliente, na próxima vez que o usuário tentar executar o aplicativo, o cliente retornará para a URL de substituição, que é definida para transmitir o pacote completo v2. sft do compartilhamento de arquivos local. Isso evitará qualquer falha do usuário quando o aplicativo for iniciado. Se o cliente inteiro for corrompido ou for desinstalado, é recomendável que o sistema ESD seja configurado para implantar a versão completa do pacote atualizado, v2. SFT, para o cliente.

Para obter mais informações sobre como atualizar um pacote, consulte "como atualizar um aplicativo virtual existente" no guia de operações do App-V 4.5 em <https://go.microsoft.com/fwlink/?LinkId=133129>

**Observação**  Como pré-requisito, todos os computadores de usuário destinados ao ESD devem ter o arquivo v1. sft totalmente carregado em seu cache local, e o fluxo de arquivos deve estar habilitado em todos os computadores.

 

**Para usar o arquivo SFT Diferencial**

1.  Faça logon no computador do sequenciador usando uma conta com direitos de administrador. Abra o pacote original (v1) para atualização no sequenciador e, em seguida, atualize o pacote para a nova versão (v2) e salve-o como um novo v2. SFT.

2.  Abra uma janela de comando na pasta de instalação do sequenciador do App-V 4.5 e execute o seguinte comando:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  Usando o sistema ESD ou outro processo de cópia de arquivo, copie o arquivo de conteúdo do pacote v2 completo, v2. SFT, para um compartilhamento de arquivos local acessível para os computadores dos usuários em uma conexão de rede bem conectada.

4.  Usando o sistema ESD, coloque uma cópia do arquivo SFT diferencial, v2. dsft, em cada computador de usuário.

5.  Para importar o arquivo V2. dsft, execute o seguinte comando SFTMIME em cada computador do usuário:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Execute o seguinte comando SFTMIME em cada computador do usuário para definir a anulação da URL para apontar para o arquivo V2. sft:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Observação**  
-   Arquivos SFT diferenciais devem ser aplicados a clientes na ordem correta. Por exemplo, v2. dsft deve ser aplicado a um aplicativo v1 antes de v3. dsft ser aplicado.

-   A funcionalidade **gerar pacote do Microsoft Windows Installer (MSI)** no sequenciador não pode ser usada com o arquivo SFT diferencial.

 

## Tópicos relacionados


[Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





