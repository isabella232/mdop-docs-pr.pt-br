---
title: Página Arquivos de Instalação
description: Página Arquivos de Instalação
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796906"
---
# <span data-ttu-id="16de9-103">Página Arquivos de Instalação</span><span class="sxs-lookup"><span data-stu-id="16de9-103">Installation Files Page</span></span>


<span data-ttu-id="16de9-104">Use a página **arquivos de instalação** para especificar os arquivos de instalação que foram usados para criar o pacote de aplicativo virtual especificado na página **selecionar pacote** deste assistente.</span><span class="sxs-lookup"><span data-stu-id="16de9-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="16de9-105">Se você criou um pacote de aplicativo virtual que contém vários aplicativos, copie todos os arquivos de instalação necessários para uma única pasta no computador executando o Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="16de9-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="16de9-106">Esta página contém os seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="16de9-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="16de9-107">Arquivos de instalação originais</span><span class="sxs-lookup"><span data-stu-id="16de9-107">Original Installation Files</span></span>**  
<span data-ttu-id="16de9-108">Clique em **procurar** para especificar os arquivos de instalação que foram usados originalmente para criar o pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="16de9-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="16de9-109">O diretório pai que você especificar deve ser salvo localmente no computador que executa o sequenciador e deve conter todos os arquivos de instalação ou subpastas necessários que contenham os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="16de9-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="16de9-110">Os arquivos de instalação podem estar contidos na pasta pai ou em qualquer uma das subpastas da pasta pai especificada.</span><span class="sxs-lookup"><span data-stu-id="16de9-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="16de9-111">Arquivos instalados no sistema local</span><span class="sxs-lookup"><span data-stu-id="16de9-111">Files installed on local system</span></span>**  
<span data-ttu-id="16de9-112">Clique em **procurar** para especificar os arquivos de instalação que foram instalados localmente no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="16de9-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="16de9-113">Você só pode selecionar essa opção se os arquivos de instalação do aplicativo tiverem sido instalados no local padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16de9-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="16de9-114">**Observação**  O local de instalação padrão fornecido depende das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="16de9-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="16de9-115">A raiz do pacote especificada quando o pacote foi originalmente criado.</span><span class="sxs-lookup"><span data-stu-id="16de9-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="16de9-116">O local de instalação especificado no Windows Installer quando o pacote foi originalmente criado.</span><span class="sxs-lookup"><span data-stu-id="16de9-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="16de9-117">O caminho de instalação do aplicativo padrão.</span><span class="sxs-lookup"><span data-stu-id="16de9-117">The default application installation path.</span></span>

<span data-ttu-id="16de9-118">Por exemplo, se a raiz do pacote especificada for **Q:\\Office12** e durante a instalação, o local de instalação padrão será alterado de **c:\\Arquivos de Files\\Office12** para **Q:\\Office12**, o caminho especificado durante DEHYDRATION deve ser **c:\\Arquivos de Files\\Office 12**.</span><span class="sxs-lookup"><span data-stu-id="16de9-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="16de9-119">Se a raiz do pacote especificada for **Q:\\Microsoft** e durante a instalação, o local de instalação padrão será alterado de **c:\\Arquivos de Files\\Office12** para **Q:\\Microsoft\\Office12**, o caminho especificado durante DEHYDRATION deve ser c:\\Arquivos de **programas**.</span><span class="sxs-lookup"><span data-stu-id="16de9-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="16de9-120">Quando você cria um pacote usando um acelerador de pacote, cada arquivo no pacote, por exemplo **Q:\\Office12\\file.txt** é encontrado no computador local, substituindo o **Q:\\Office12** raiz do pacote pelo local padrão especificado quando o acelerador do pacote foi criado, por exemplo, **c:\\Arquivos de Files\\Office12**.</span><span class="sxs-lookup"><span data-stu-id="16de9-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="16de9-121">No exemplo anterior, o arquivo deve estar localizado em **c:\\Arquivos de Files\\Office12\\file.txt**.</span><span class="sxs-lookup"><span data-stu-id="16de9-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="16de9-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16de9-122">Related topics</span></span>


[<span data-ttu-id="16de9-123">Assistente para Criar Acelerador de Pacote (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="16de9-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





