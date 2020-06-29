---
title: Como criar ou editar os arquivos mof
description: Como criar ou editar os arquivos mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799649"
---
# <span data-ttu-id="7d4ed-103">Como criar ou editar os arquivos mof</span><span class="sxs-lookup"><span data-stu-id="7d4ed-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="7d4ed-104">Antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, você precisa editar o arquivo Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="7d4ed-105">Você também precisará editar ou criar o arquivo SMS \ _def. MOF, dependendo de qual versão do Configuration Manager você está usando.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="7d4ed-106">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="7d4ed-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="7d4ed-107">Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo Configuration. mof do Microsoft System Center Configuration Manager 2007 e do SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="7d4ed-108">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="7d4ed-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="7d4ed-109">Criar ou editar o arquivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="7d4ed-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="7d4ed-110">Para permitir que os computadores cliente relatem os detalhes de conformidade do BitLocker nos relatórios do Gerenciador de configuração do MBAM, você precisa criar ou editar o arquivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="7d4ed-111">No Configuration Manager 2007, o arquivo já existe, portanto, você precisa editar, mas não substituir, o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="7d4ed-112">Se estiver usando o SystemCenter2012 ConfigurationManager, você deve criar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d4ed-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="7d4ed-113">Criar ou editar o arquivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="7d4ed-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="7d4ed-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d4ed-114">Related topics</span></span>


[<span data-ttu-id="7d4ed-115">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7d4ed-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





