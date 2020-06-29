---
title: Como aplicar o arquivo de configuração da implantação usando o PowerShell
description: Como aplicar o arquivo de configuração da implantação usando o PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796500"
---
# <span data-ttu-id="b98fc-103">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="b98fc-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="b98fc-104">O arquivo de configuração de implantação dinâmica é aplicado quando um pacote é adicionado ou definido como um computador executando o cliente App-V 5,1 antes do pacote ser publicado.</span><span class="sxs-lookup"><span data-stu-id="b98fc-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="b98fc-105">O arquivo define as configurações padrão do pacote para todos os usuários do computador que executam o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b98fc-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="b98fc-106">Esta seção descreve as etapas usadas para usar um arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="b98fc-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="b98fc-107">O procedimento se baseia no exemplo a seguir e pressupõe que os seguintes arquivos de pacote e configuração existam em um computador:</span><span class="sxs-lookup"><span data-stu-id="b98fc-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="b98fc-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="b98fc-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="b98fc-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b98fc-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="b98fc-110">Para aplicar o arquivo de configuração de implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="b98fc-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="b98fc-111">Para especificar um novo conjunto padrão de configurações para todos os usuários que executarão o pacote em um computador específico, usando um console do PowerShell, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b98fc-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="b98fc-112">Add-AppVClientPackage – caminho c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b98fc-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="b98fc-113">Observação</span><span class="sxs-lookup"><span data-stu-id="b98fc-113">Note</span></span>**  
    <span data-ttu-id="b98fc-114">Esse comando captura o objeto resultante em $pkg.</span><span class="sxs-lookup"><span data-stu-id="b98fc-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="b98fc-115">Se o pacote já estiver presente no computador, o cmdlet **set-AppVclientPackage** pode ser usado para aplicar o documento de configuração de implantação:</span><span class="sxs-lookup"><span data-stu-id="b98fc-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="b98fc-116">Set-AppVClientPackage – Name MyApp-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b98fc-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="b98fc-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b98fc-117">Related topics</span></span>


[<span data-ttu-id="b98fc-118">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b98fc-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









