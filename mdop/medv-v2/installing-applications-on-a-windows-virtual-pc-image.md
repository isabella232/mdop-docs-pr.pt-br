---
title: Instalar aplicativos em uma imagem do Windows Virtual PC
description: Instalar aplicativos em uma imagem do Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799951"
---
# Instalar aplicativos em uma imagem do Windows Virtual PC


Depois de criar uma imagem do PC virtual do Windows para uso com o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, você pode instalar outros componentes que sejam úteis ao executar o MED-V, como um sistema ESD (distribuição de software eletrônico) e um software antivírus.

A seção a seguir fornece informações para ajudá-lo a instalar o software na imagem do MED-V.

**Cuidado**  Para facilitar o gerenciamento do espaço de trabalho do MED-V após a implantação, recomendamos que você limite o número de componentes que você instala na imagem do MED-V para os componentes necessários ou que sejam úteis ao usar o MED-V. Por exemplo, embora não seja necessário executar o MED-V, você pode instalar um sistema ESD para usar mais tarde para instalar aplicativos em um espaço de trabalho do MED-V e software antivírus para segurança na imagem.

 

**Instalando o software em uma imagem do MED-V**

1.  Se não estiver sendo executado no momento, abra sua máquina virtual do MED-V.

    1.  Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows** e clique em **PC virtual do Windows**.

    2.  Clique duas vezes em sua máquina virtual do MED-V.

2.  De dentro do sistema operacional da máquina virtual, localize os arquivos de instalação do software que você deseja instalar.

3.  Siga as instruções de instalação fornecidas pelo fornecedor do software.

    **Observação**  Após a conclusão da instalação, talvez seja necessário fechar e reiniciar a máquina virtual.

     

Repita essas etapas para qualquer software ou aplicativo que você queira instalar na imagem do MED-V. Recomendamos que você limite o número de aplicativos que você pré-instalando na imagem. O processo recomendado para instalar aplicativos e outros softwares na imagem é pré-instalar um sistema ESD agora e usá-lo posteriormente para implantar o software na imagem. Como alternativa, você também pode usar a política de grupo ou o App-V para adicionar ou remover aplicativos em um espaço de trabalho do MED-V. Para obter mais informações, consulte [Gerenciando aplicativos implantados em espaços de trabalho do MED-V](managing-applications-deployed-to-med-v-workspaces.md).

Para obter mais informações sobre como instalar software em uma imagem virtual, consulte os seguintes artigos:

-   [Publicar e usar aplicativos virtuais](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Ajuda do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Depois de instalar todo o software que você deseja na imagem do MED-V, sua imagem estará pronta para ser empacotada.

## Tópicos relacionados


[Como configurar uma imagem do Windows Virtual PC para a MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Preparar uma imagem da MED-V](prepare-a-med-v-image.md)

 

 





