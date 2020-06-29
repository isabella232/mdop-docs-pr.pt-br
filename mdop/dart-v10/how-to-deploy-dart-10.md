---
title: Como implantar o DaRT 10
description: Como implantar o DaRT 10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796158"
---
# <span data-ttu-id="eadbe-103">Como implantar o DaRT 10</span><span class="sxs-lookup"><span data-stu-id="eadbe-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="eadbe-104">As instruções a seguir explicam como implantar o diagnóstico e o conjunto de ferramentas de recuperação (DaRT) 10 da Microsoft no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="eadbe-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="eadbe-105">Para obter o software DaRT, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="eadbe-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="eadbe-106">Presume-se que você esteja instalando toda a funcionalidade em um computador administrador.</span><span class="sxs-lookup"><span data-stu-id="eadbe-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="eadbe-107">Se você precisar implantar ou desinstalar o DaRT 10 em vários computadores, usando um sistema de distribuição de software eletrônico, por exemplo, talvez seja mais fácil usar as opções de instalação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="eadbe-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="eadbe-108">Descrições e exemplos das opções de linha de comando disponíveis são fornecidas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="eadbe-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="eadbe-109">**Importante**  Antes de instalar o DaRT, consulte [configurações compatíveis com o DART 10](dart-10-supported-configurations.md) para garantir que você tenha instalado todo o software de pré-requisito e que o computador atenda aos requisitos mínimos do sistema.</span><span class="sxs-lookup"><span data-stu-id="eadbe-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="eadbe-110">O computador no qual você instala o DaRT deve estar executando o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="eadbe-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="eadbe-111">Você pode instalar o DaRT usando uma das duas configurações diferentes:</span><span class="sxs-lookup"><span data-stu-id="eadbe-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="eadbe-112">Instale o DaRT e todas as ferramentas do DaRT no computador administrador.</span><span class="sxs-lookup"><span data-stu-id="eadbe-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="eadbe-113">Instalar no computador do administrador somente as ferramentas de que você precisa para criar a imagem de recuperação do DaRT e, em seguida, instalar o **Visualizador de conexão remota** e, opcionalmente, o **Crash Analyzer** em um computador de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="eadbe-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="eadbe-114">O arquivo de instalação do DaRT está disponível nas versões de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="eadbe-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="eadbe-115">Instale a versão que corresponde à arquitetura do computador no qual você está executando o assistente de imagem de recuperação DaRT, não a arquitetura de computador da imagem de recuperação que você está criando.</span><span class="sxs-lookup"><span data-stu-id="eadbe-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="eadbe-116">Você pode usar qualquer versão do arquivo de instalação do DaRT para criar uma imagem de recuperação para computadores de 32 bits ou 64 bits, mas não pode criar uma imagem de recuperação para computadores de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="eadbe-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="eadbe-117">Para instalar o DaRT e todas as ferramentas DaRT em um computador administrador</span><span class="sxs-lookup"><span data-stu-id="eadbe-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="eadbe-118">Baixe a versão de 32 bits ou 64 bits do arquivo de instalação do DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="eadbe-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="eadbe-119">Escolha a arquitetura que corresponde ao computador no qual você está instalando o DaRT e executando o assistente de recuperação de imagem de DaRT.</span><span class="sxs-lookup"><span data-stu-id="eadbe-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="eadbe-120">Na pasta para a qual você baixou o DaRT 10, execute o arquivo de instalação **MSDaRT.msi** que corresponde aos requisitos do sistema.</span><span class="sxs-lookup"><span data-stu-id="eadbe-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="eadbe-121">Na página **Bem-vindo ao assistente de configuração do Microsoft DART 10** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="eadbe-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="eadbe-122">Aceite os termos de licença para software Microsoft e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="eadbe-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="eadbe-123">Na página **Microsoft Update** , selecione **usar o Microsoft Update quando eu verificar se há atualizações**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="eadbe-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="eadbe-124">Na página **Selecionar pasta de instalação** , selecione uma pasta ou clique em **Avançar** para instalar o DART no local de instalação padrão.</span><span class="sxs-lookup"><span data-stu-id="eadbe-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="eadbe-125">Na página **Opções de instalação** , selecione os recursos DART que você deseja instalar ou clique em **Avançar** para instalar o DART com todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="eadbe-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="eadbe-126">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="eadbe-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="eadbe-127">Depois que a instalação for concluída com êxito, clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="eadbe-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="eadbe-128">Para instalar o DaRT e todas as ferramentas DaRT em um computador administrador usando um prompt de comando</span><span class="sxs-lookup"><span data-stu-id="eadbe-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="eadbe-129">Ao instalar ou desinstalar o DaRT, você tem a opção de executar os arquivos de instalação no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="eadbe-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="eadbe-130">Esta seção descreve alguns exemplos de opções diferentes que você pode especificar ao instalar ou desinstalar o DaRT no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="eadbe-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="eadbe-131">O exemplo a seguir mostra como instalar toda a funcionalidade do DaRT.</span><span class="sxs-lookup"><span data-stu-id="eadbe-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="eadbe-132">O exemplo a seguir mostra como instalar apenas o assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="eadbe-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="eadbe-133">O exemplo a seguir mostra como instalar somente o Crash Analyzer e o Visualizador de conexão remota do DaRT.</span><span class="sxs-lookup"><span data-stu-id="eadbe-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="eadbe-134">O exemplo a seguir cria um log de configuração para o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="eadbe-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="eadbe-135">Isso é importante para a depuração.</span><span class="sxs-lookup"><span data-stu-id="eadbe-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="eadbe-136">**Observação**  Você pode adicionar/qn ou/QB para executar uma instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="eadbe-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="eadbe-137">Para validar a instalação do DaRT</span><span class="sxs-lookup"><span data-stu-id="eadbe-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="eadbe-138">Clique em **Iniciar**e selecione **conjunto de ferramentas de diagnóstico e recuperação**.</span><span class="sxs-lookup"><span data-stu-id="eadbe-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="eadbe-139">A janela **diagnóstico e Recovery Toolset** é aberta.</span><span class="sxs-lookup"><span data-stu-id="eadbe-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="eadbe-140">Verifique se todas as ferramentas do DaRT selecionadas para instalação foram instaladas com sucesso.</span><span class="sxs-lookup"><span data-stu-id="eadbe-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="eadbe-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eadbe-141">Related topics</span></span>


[<span data-ttu-id="eadbe-142">Implantar o DaRT 10 em computadores de administrador</span><span class="sxs-lookup"><span data-stu-id="eadbe-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





