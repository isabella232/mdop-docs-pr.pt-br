---
title: Como alterar as propriedades da implantação
description: Como alterar as propriedades da implantação
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797250"
---
# Como alterar as propriedades da implantação


Você pode usar os procedimentos a seguir para alterar as informações da guia de **implantação** para um aplicativo que você está sequenciando, incluindo a URL do servidor de virtualização de aplicativos, os sistemas operacionais necessários para os aplicativos virtualizados e as opções de saída para o aplicativo virtual a ser instalado.

**Para alterar a URL do servidor**

1.  Selecione o protocolo de streaming na caixa de listagem suspensa.

2.  Digite o nome do host do servidor de aplicativos virtual ou o balanceador de carga do grupo do servidor. Você pode usar o nome do host ou endereço IP real.

3.  Especifique o número da porta na qual o servidor de aplicativos virtual ou o balanceador de carga escutará uma solicitação de cliente da área de trabalho do aplicativo Virtualization para o aplicativo em fluxo.

4.  Especifique o caminho relativo no servidor de aplicativos virtual em que o pacote do software está armazenado.

**Para alterar os requisitos do sistema operacional do aplicativo**

1.  Para adicionar o (s) sistema (es) operacional necessário (s), selecione-o na lista **disponível** e clique no botão de seta apontando para o controle de lista de sistemas operacionais **selecionados** .

2.  Para remover um sistema operacional, selecione-o no controle de lista **selecionado** e clique no botão de seta apontando para o controle de lista de sistemas operacionais **disponíveis** .

**Para alterar as opções de saída do aplicativo**

1.  Na lista suspensa **algoritmo de compactação** , selecione o método de compactação a ser usado ao transmitir o aplicativo.

2.  Marque a caixa de seleção **impor descritores de segurança** para garantir que os descritores de segurança dos aplicativos em pacotes sejam aplicados quando implantados.

3.  Selecione **gerar arquivo de diferença** para gerar um arquivo de diferença para o aplicativo da versão sequenciada anterior.

4.  Selecione **gerar pacote do Microsoft Windows Installer (MSI)** para criar um pacote de instalação.

## Tópicos relacionados


[Sobre a guia Implantação](about-the-deployment-tab.md)

[Console do Sequencer](sequencer-console.md)

 

 





