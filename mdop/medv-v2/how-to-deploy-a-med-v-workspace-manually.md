---
title: Como implantar manualmente um espaço de trabalho da MED-V
description: Como implantar manualmente um espaço de trabalho da MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800040"
---
# Como implantar manualmente um espaço de trabalho da MED-V


Em alguns casos, talvez você queira implantar seu espaço de trabalho do MED-V manualmente, por exemplo, se a sua empresa não usar um sistema de distribuição de software eletrônico para implantar aplicativos.

Esta seção fornece instruções sobre como implantar manualmente um espaço de trabalho do MED-V.

**Para implantar um espaço de trabalho do MED-V manualmente**

1.  Copie todos os aplicativos de pré-requisito e os arquivos de pacote do espaço de trabalho do MED-V para uma unidade compartilhada ou um DVD. Veja a seguir uma lista dos aplicativos e arquivos necessários.

    -   **PC virtual do Windows**. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    -   **Adições e atualizações do Windows Virtual PC**. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    -   **Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação).

        **Aviso**  
        Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL. Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Instale o seguinte na ordem listada. O usuário final pode executar essa tarefa manualmente ou você pode criar um script para instalar o seguinte:

   -   O Windows Virtual PC e o Windows Virtual PC Additions e atualizações. É preciso reiniciar o computador.

   -   O agente de host do MED-V.

       **Observação**  
       Se estiver em execução, o Internet Explorer deve ser reiniciado para que a instalação do agente de host MED-V possa ser concluída.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Conclua a configuração da primeira vez.

   Após a instalação do espaço de trabalho do MED-V, você tem a opção de iniciar o MED-V. Isso inicia o agente do host MED-V. Você pode iniciar MED-V nesse momento ou iniciar o agente de host do MED-V mais tarde para concluir a configuração do primeiro horário.

   Para iniciar o agente de host do MED-V, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-v**.

## Tópicos relacionados


[Como implantar um espaço de trabalho da MED-V por meio de um sistema de distribuição eletrônica de software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Como implantar o pacote de espaço de trabalho da MED-V](deploying-the-med-v-workspace-package.md)









