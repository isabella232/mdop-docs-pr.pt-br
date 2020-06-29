---
title: Como aplicar o arquivo de configuração do usuário usando o PowerShell
description: Como aplicar o arquivo de configuração do usuário usando o PowerShell
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796497"
---
# <span data-ttu-id="42416-103">Como aplicar o arquivo de configuração do usuário usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="42416-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="42416-104">O arquivo de configuração de usuário dinâmico é aplicado quando um pacote é publicado em um usuário específico e determina como o pacote será executado.</span><span class="sxs-lookup"><span data-stu-id="42416-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="42416-105">Use o procedimento a seguir para especificar um arquivo de configuração específico do usuário.</span><span class="sxs-lookup"><span data-stu-id="42416-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="42416-106">O procedimento a seguir se baseia no exemplo:</span><span class="sxs-lookup"><span data-stu-id="42416-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="42416-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="42416-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="42416-108">Para aplicar um arquivo de configuração do usuário</span><span class="sxs-lookup"><span data-stu-id="42416-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="42416-109">Para adicionar o pacote ao computador usando o console do PowerShell, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="42416-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="42416-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.</span><span class="sxs-lookup"><span data-stu-id="42416-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="42416-111">Use o comando a seguir para publicar o pacote para o usuário e especificar o arquivo de configuração do usuário dinâmico atualizado:</span><span class="sxs-lookup"><span data-stu-id="42416-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="42416-112">Publish-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="42416-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="42416-113">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="42416-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="42416-114">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="42416-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="42416-115">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="42416-115">Got an App-V issue?</span></span>** <span data-ttu-id="42416-116">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="42416-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="42416-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42416-117">Related topics</span></span>


[<span data-ttu-id="42416-118">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="42416-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





