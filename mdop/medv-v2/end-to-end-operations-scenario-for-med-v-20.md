---
title: Cenário de operações de ponta a ponta para a MED-V 2.0
description: Cenário de operações de ponta a ponta para a MED-V 2.0
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799818"
---
# Cenário de operações de ponta a ponta para a MED-V 2.0


Este cenário de exemplo para a virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 ajuda você a implantar e gerenciar o MED-V usando vários cenários de ponta a ponta. Você pode pensar nesse exemplo de cenário como um estudo de caso que ajuda a colocar os cenários e procedimentos individuais em contexto.

Esta seção fornece informações básicas e instruções para criar, implantar e gerenciar os espaços de trabalho do MED-V como uma solução completa na sua empresa.

## Cenário passo a passo de operações do MED-V


Os procedimentos passo a passo que você segue em um cenário de operações do MED-V incluem o seguinte:

-   A [criação de uma imagem do Windows Virtual PC para o MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) analisa como criar e configurar uma imagem do Windows Virtual PC para o MED-v. Antes de distribuir um espaço de trabalho do MED-V para os usuários, você deve primeiro preparar um VHD (disco rígido virtual) que você usa para criar o pacote de instalação do espaço de trabalho do MED-V para o MED-V.

-   A [criação de uma imagem do Windows Virtual PC para o MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) analisa como instalar o sistema operacional Windows XP SP3 na sua imagem do PC virtual do Windows. O MED-V exige que o Windows XP SP3 esteja instalado na imagem do PC virtual do Windows antes de criar o espaço de trabalho do MED-V.

-   A [criação de uma imagem do Windows Virtual PC para o MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) analisa como instalar manualmente o .net Framework 3,5 SP1 e a atualização KB959209 na imagem do PC virtual do Windows que você prepara para usar com o MED-V. O MED-V requer o .NET Framework 3,5 SP1 e a atualização [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) corrige vários problemas de compatibilidade de aplicativos conhecidos.

-   A [criação de uma imagem do Windows Virtual PC para o MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) analisa a atualização de sua imagem do Windows XP com as últimas atualizações de software e outros hotfixes necessários ou importantes para executar o MED-V.

-   A [criação de uma imagem do Windows Virtual PC para o MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) analisa como instalar o pacote de componentes de integração na sua imagem do Windows XP. Elas fornecem recursos que melhoram a interação entre o ambiente virtual e o computador físico.

-   [A instalação de aplicativos em uma imagem do PC virtual do Windows](installing-applications-on-a-windows-virtual-pc-image.md) revisa como você pode instalar determinados tipos de software na sua imagem do Windows XP que são úteis quando você está executando o MED-V, como um sistema de distribuição de software eletrônico e um software antivírus.

-   A [configuração de uma imagem de PC virtual do Windows para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md) descreve como configurar a imagem usando o Sysprep para garantir que ela esteja pronta para uso com o MED-v. A imagem do MED-V preparada é usada para criar seu pacote de espaço de trabalho do MED-V.

-   [Criar um pacote de espaço de trabalho do MED-v](create-a-med-v-workspace-package.md) revisa como criar o pacote de espaço de trabalho do MED-v que você implanta em toda a sua empresa. Implante o pacote do espaço de trabalho do MED-V para instalar o espaço de trabalho do MED-V nos computadores dos usuários finais. Um espaço de trabalho do MED-V é o ambiente de área de trabalho do Windows XP do qual os usuários finais interagem com a máquina virtual fornecida pelo MED-V.

-   [Testar o pacote do espaço de trabalho do MED-V](testing-the-med-v-workspace-package.md) descreve como criar um ambiente de teste no qual você pode testar a funcionalidade do pacote do espaço de trabalho do MED-v, como configurações de configuração e publicação de aplicativos pela primeira vez. Depois de concluir o teste do pacote do espaço de trabalho do MED-V e verificar se ele está funcionando conforme o esperado, você pode implantá-lo em toda a empresa.

-   [A implantação do pacote do espaço de trabalho do MED-v](deploying-the-med-v-workspace-package.md) discute como implantar o espaço de trabalho do MED-v usando um sistema de distribuição de software eletrônico ou uma imagem do Windows 7. Ou, se preferir, esta seção também mostra como você pode implantar o espaço de trabalho do MED-V manualmente.

-   [Monitorar os espaços de trabalho do MED-v](monitor-med-v-workspaces.md) analisa como monitorar a implantação de espaços de trabalho do MED-v para determinar se a configuração da primeira vez concluída com êxito. Monitorar o sucesso da configuração pela primeira vez é importante porque o MED-V não está em um estado utilizável até que a configuração inicial seja concluída com êxito. Esta seção também mostra que você pode configurar seu ambiente para detectar as alterações de rede que podem afetar o MED-V.

-   [Gerenciar aplicativos do espaço de trabalho do MED-V](manage-med-v-workspace-applications.md) revisa como instalar e remover ou publicar e cancelar a publicação de aplicativos em um espaço de trabalho do MED-v implantado. Esta seção também mostra como atualizar manualmente o software em um espaço de trabalho do MED-V e como gerenciar as atualizações automáticas. O espaço de trabalho do MED-V é uma máquina virtual que contém um sistema operacional separado cujo processo de atualização automática de software deve ser gerenciado exatamente como os computadores físicos da sua empresa.

-   [Gerenciar o redirecionamento de URL do MED-V](manage-med-v-url-redirection.md) revisa como adicionar e remover configurações de redirecionamento de endereço Web no espaço de trabalho do MED-v implantado. Você pode adicionar ou remover informações de redirecionamento de URL por meio do registro ou recriando o espaço de trabalho do MED-V. Você também pode usar o assistente no pacote do espaço de trabalho do MED-V para gerenciar o redirecionamento de endereço da Web.

-   [Gerenciar as configurações do espaço de trabalho do MED-v](manage-med-v-workspace-settings.md) analisa como exibir e editar as configurações de configuração do MED-v usando o pacote do espaço de trabalho do MED-v. Esta seção lista todas as chaves de registro do MED-V configuráveis e inclui o tipo, o padrão e a descrição de cada um. Esta seção também inclui informações sobre como gerenciar impressoras em espaços de trabalho do MED-V. No MED-V 2,0, o redirecionamento de impressora oferece aos usuários uma experiência de impressão consistente entre a máquina virtual do MED-V e o computador host.

## Tópicos relacionados


[Operações da MED-V](operations-for-med-v.md)

[Cenário de planejamento de ponta a ponta para a MED-V 2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Cenário de implantação de ponta a ponta para a MED-V 2.0](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





