---
title: Como implantar o DaRT 7.0
description: Como implantar o DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796152"
---
# <span data-ttu-id="a96fd-103">Como implantar o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a96fd-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="a96fd-104">Este tópico fornece instruções para implantar o Microsoft Diagnostic and Recovery Toolset (DaRT) 7 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="a96fd-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="a96fd-105">O primeiro procedimento deste tópico pressupõe que você está instalando toda a funcionalidade em um computador administrador.</span><span class="sxs-lookup"><span data-stu-id="a96fd-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="a96fd-106">Quando você precisa implantar ou desinstalar o DaRT em vários computadores, usando um sistema de distribuição de software eletrônico por exemplo, pode ser mais fácil usar as opções de instalação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a96fd-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="a96fd-107">Essas opções são definidas no segundo procedimento deste tópico, que fornece um exemplo de uso para as opções de linha de comando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a96fd-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="a96fd-108">**Importante**  Antes de instalar o DaRT, verifique se o computador atende aos requisitos mínimos de sistema listados nas [configurações compatíveis com o DaRT 7,0](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="a96fd-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="a96fd-109">Para instalar o DaRT em um computador administrador</span><span class="sxs-lookup"><span data-stu-id="a96fd-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="a96fd-110">Localize os arquivos de instalação do DaRT que você recebeu como parte do download do software.</span><span class="sxs-lookup"><span data-stu-id="a96fd-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="a96fd-111">Clique duas vezes no arquivo de instalação do DaRT que corresponde aos requisitos do sistema, seja 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a96fd-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="a96fd-112">O arquivo de instalação do DaRT é chamado de **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="a96fd-113">Aceite os termos de licença para software Microsoft e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="a96fd-114">Selecione a pasta de destino para instalar o DaRT, selecione se o DaRT deve ser instalado para todos os usuários ou apenas para o usuário atual e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="a96fd-115">Selecione se a instalação deve ser **típica**, **personalizada**ou **completa**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="a96fd-116">**Típica** instala as ferramentas que são usadas com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="a96fd-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="a96fd-117">Esse método é recomendado para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="a96fd-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="a96fd-118">**Personalizado** permite que você selecione as ferramentas que estão instaladas e onde elas serão instaladas.</span><span class="sxs-lookup"><span data-stu-id="a96fd-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="a96fd-119">Isso é recomendado para usuários avançados, especialmente se você estiver instalando diferentes ferramentas DaRT em diferentes computadores de helpdesk.</span><span class="sxs-lookup"><span data-stu-id="a96fd-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="a96fd-120">**Concluído** instala todas as ferramentas DART e requer mais espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="a96fd-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="a96fd-121">Depois de selecionar o método de instalação, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="a96fd-122">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="a96fd-123">Depois que a instalação for concluída com êxito, clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="a96fd-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="a96fd-124">Para instalar o DaRT no prompt de comando</span><span class="sxs-lookup"><span data-stu-id="a96fd-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="a96fd-125">O exemplo a seguir mostra como instalar toda a funcionalidade do DaRT.</span><span class="sxs-lookup"><span data-stu-id="a96fd-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="a96fd-126">O exemplo a seguir mostra como instalar apenas o **Assistente de imagem de recuperação do DART**.</span><span class="sxs-lookup"><span data-stu-id="a96fd-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="a96fd-127">O exemplo a seguir mostra como instalar somente o Crash Analyzer e o Visualizador de conexão remota do DaRT.</span><span class="sxs-lookup"><span data-stu-id="a96fd-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="a96fd-128">O exemplo a seguir cria um log de configuração para o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a96fd-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="a96fd-129">Isso é importante para a depuração.</span><span class="sxs-lookup"><span data-stu-id="a96fd-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="a96fd-130">**Observação**  Você pode adicionar/qn ou/QB a qualquer uma das opções de prompt de comando de instalação do DaRT para executar uma instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="a96fd-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="a96fd-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a96fd-131">Related topics</span></span>


[<span data-ttu-id="a96fd-132">Implantar o DaRT 7.0 em computadores de administrador</span><span class="sxs-lookup"><span data-stu-id="a96fd-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





