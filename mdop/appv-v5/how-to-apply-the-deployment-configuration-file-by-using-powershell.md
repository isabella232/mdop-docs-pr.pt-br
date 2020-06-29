---
title: Como aplicar o arquivo de configuração da implantação usando o PowerShell
description: Como aplicar o arquivo de configuração da implantação usando o PowerShell
author: dansimp
ms.assetid: 5df5d5bc-6c72-4087-8b93-d6d4b502a1f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6764f07dfe8cff1fb30c354937a405202468428
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796501"
---
# <span data-ttu-id="90652-103">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="90652-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="90652-104">O arquivo de configuração de implantação dinâmica é aplicado quando um pacote é adicionado ou definido como um computador executando o cliente App-V 5,0 antes do pacote ser publicado.</span><span class="sxs-lookup"><span data-stu-id="90652-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.0 client before the package has been published.</span></span> <span data-ttu-id="90652-105">O arquivo define as configurações padrão do pacote para todos os usuários do computador que executam o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="90652-105">The file configures the default settings for package for all users on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="90652-106">Esta seção descreve as etapas usadas para usar um arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="90652-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="90652-107">O procedimento se baseia no exemplo a seguir e pressupõe que os seguintes arquivos de pacote e configuração existam em um computador:</span><span class="sxs-lookup"><span data-stu-id="90652-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="90652-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="90652-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="90652-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="90652-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="90652-110">Para aplicar o arquivo de configuração de implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="90652-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="90652-111">Para especificar um novo conjunto padrão de configurações para todos os usuários que executarão o pacote em um computador específico, usando um console do PowerShell, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="90652-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="90652-112">Add-AppVClientPackage – caminho c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="90652-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="90652-113">Observação</span><span class="sxs-lookup"><span data-stu-id="90652-113">Note</span></span>**  
    <span data-ttu-id="90652-114">Esse comando captura o objeto resultante em $pkg.</span><span class="sxs-lookup"><span data-stu-id="90652-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="90652-115">Se o pacote já estiver presente no computador, o cmdlet **set-AppVclientPackage** pode ser usado para aplicar o documento de configuração de implantação:</span><span class="sxs-lookup"><span data-stu-id="90652-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="90652-116">Set-AppVClientPackage – Name MyApp-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="90652-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="90652-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90652-117">Related topics</span></span>


[<span data-ttu-id="90652-118">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="90652-118">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









