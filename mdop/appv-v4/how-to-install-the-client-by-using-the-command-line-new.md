---
title: Como instalar o cliente usando a linha de comando
description: Como instalar o cliente usando a linha de comando
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797102"
---
# <span data-ttu-id="960dc-103">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="960dc-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="960dc-104">Os tópicos desta seção incluem procedimentos para instalar o cliente de desktop do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal) usando setup.exe ou setup.msi.</span><span class="sxs-lookup"><span data-stu-id="960dc-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="960dc-105">É necessário ter direitos administrativos para executar o programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="960dc-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="960dc-106">Você pode usar parâmetros de linha de comando opcionais para aplicar configurações específicas ao cliente App-V durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="960dc-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="960dc-107">Para obter mais informações sobre como usar parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="960dc-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="960dc-108">Se você tiver aplicado configurações do registro a um computador antes de implantar um cliente — por exemplo, usando a política de grupo, essas configurações serão mantidas e todos os parâmetros de linha de comando adicionais serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="960dc-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="960dc-109">Os valores de parâmetro de linha de comando substituirão qualquer valor existente na mesma configuração.</span><span class="sxs-lookup"><span data-stu-id="960dc-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="960dc-110">**Observação**  Ao instalar o cliente App-V para usar com um cache somente leitura, por exemplo, com uma implementação de servidor VDI, você deve definir o parâmetro *AUTOLOADTARGET* como None para impedir que o cliente tente atualizar aplicativos quando o cache for somente leitura.</span><span class="sxs-lookup"><span data-stu-id="960dc-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="960dc-111">Para obter mais informações sobre como definir esses valores de parâmetro após a instalação, consulte [como definir as configurações do registro do cliente App-V usando a linha de comando](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) no guia de operações do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="960dc-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="960dc-112">**Observação**  Se uma configuração no computador do usuário depende do caminho de instalação do cliente, observe que o aplicativo virtualização do aplicativo (App-V) 4.5 copia seus arquivos de instalação para uma pasta diferente das versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="960dc-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="960dc-113">Por padrão, uma nova instalação do aplicativo App-V 4.5 copiará seus arquivos de instalação para a pasta do cliente \\Program Files\\Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="960dc-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="960dc-114">Se uma versão anterior do cliente já estiver instalada, executar o instalador do cliente do App-V 4,5 executará uma atualização do cliente existente usando a pasta de instalação existente.</span><span class="sxs-lookup"><span data-stu-id="960dc-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="960dc-115">\ [Valor do token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="960dc-115">\[Template Token Value\]</span></span>

<span data-ttu-id="960dc-116">**Observação**  Para o App-V versão 4.6 e posterior, quando o cliente App-V estiver instalado, o SFTLDR.DLL será copiado para o diretório Windows\\system32.</span><span class="sxs-lookup"><span data-stu-id="960dc-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="960dc-117">Se o cliente App-V estiver instalado em um sistema de 64 bits, o SFTLDR\_WOW64.DLL será copiado para o diretório Windows\\SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="960dc-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="960dc-118">\ [Valor do token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="960dc-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="960dc-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="960dc-119">In This Section</span></span>


<span data-ttu-id="960dc-120">Os tópicos a seguir descrevem como instalar o cliente de desktop do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal) usando setup.exe ou setup.msi.</span><span class="sxs-lookup"><span data-stu-id="960dc-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="960dc-121">Como instalar o cliente do App-V usando Setup.exe</span><span class="sxs-lookup"><span data-stu-id="960dc-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="960dc-122">Fornece um procedimento passo a passo para instalar o cliente App-V usando o programa setup.exe.</span><span class="sxs-lookup"><span data-stu-id="960dc-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="960dc-123">Como instalar o cliente do App-V usando Setup.msi</span><span class="sxs-lookup"><span data-stu-id="960dc-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="960dc-124">Fornece procedimentos passo a passo para instalar qualquer software de pré-requisito e também o cliente App-V usando o programa setup.msi.</span><span class="sxs-lookup"><span data-stu-id="960dc-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="960dc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="960dc-125">Related topics</span></span>


[<span data-ttu-id="960dc-126">Parâmetros de linha de comando do instalador do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="960dc-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="960dc-127">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="960dc-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="960dc-128">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="960dc-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="960dc-129">Como desinstalar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="960dc-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





