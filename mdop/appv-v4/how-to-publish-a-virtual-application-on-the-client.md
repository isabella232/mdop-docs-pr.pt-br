---
title: Como publicar um aplicativo virtual no cliente
description: Como publicar um aplicativo virtual no cliente
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797012"
---
# <span data-ttu-id="424b5-103">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="424b5-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="424b5-104">Ao implantar o Application Virtualization usando um sistema de distribuição de software eletrônico, você pode usar um dos procedimentos a seguir para publicar um pacote de aplicativo para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="424b5-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="424b5-105">Para publicar um pacote usando um arquivo autônomo do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="424b5-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="424b5-106">O cliente deve ser instalado com o parâmetro *RequireAuthorizationIfCached* definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="424b5-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="424b5-107">Para obter mais informações sobre como definir esse parâmetro, consulte [parâmetros da linha de comando do instalador do cliente do aplicativo virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="424b5-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="424b5-108">Copie o arquivo do Windows Installer e o arquivo SFT para a mesma pasta no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="424b5-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="424b5-109">Execute o seguinte comando no computador:</span><span class="sxs-lookup"><span data-stu-id="424b5-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="424b5-110">Para publicar um pacote usando o Windows Installer e o manifesto do pacote</span><span class="sxs-lookup"><span data-stu-id="424b5-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="424b5-111">Copie o arquivo do Windows Installer para o computador de destino e o arquivo SFT para o compartilhamento de conteúdo no servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="424b5-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="424b5-112">Execute o seguinte comando no computador de cada usuário:</span><span class="sxs-lookup"><span data-stu-id="424b5-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="424b5-113">**Importante**  Para OVERRIDEURL, todos os caracteres de barra invertida devem ter escape usando a barra invertida precedente ou o caminho OVERRIDEURL não será analisado corretamente.</span><span class="sxs-lookup"><span data-stu-id="424b5-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="424b5-114">Além disso, propriedades e valores devem ser inseridos em letras maiúsculas, exceto quando o valor for um caminho para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="424b5-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="424b5-115">Para publicar um pacote usando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="424b5-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="424b5-116">Para obter um exemplo de como publicar um aplicativo para todos os usuários em um computador, execute o seguinte comando no computador do usuário:</span><span class="sxs-lookup"><span data-stu-id="424b5-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="424b5-117">Para obter mais detalhes sobre esses e outros comandos do SFTMIME, consulte [referência de comandos do SFTMIME](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="424b5-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="424b5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="424b5-118">Related topics</span></span>


[<span data-ttu-id="424b5-119">Determinar o método de publicação</span><span class="sxs-lookup"><span data-stu-id="424b5-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="424b5-120">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="424b5-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="424b5-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="424b5-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="424b5-122">Cenário de Entrega Autônoma Application Virtualization Clients</span><span class="sxs-lookup"><span data-stu-id="424b5-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





