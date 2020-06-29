---
title: Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V
description: Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799873"
---
# <span data-ttu-id="b198d-103">Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V</span><span class="sxs-lookup"><span data-stu-id="b198d-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="b198d-104">Para editar informações de redirecionamento de URL em um espaço de trabalho do MED-V implantado, recomendamos que você atualize o registro do sistema usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b198d-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="b198d-105">Embora não recomendemos isso, você também pode recriar e reimplantar o espaço de trabalho do MED-V com as informações atualizadas de redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="b198d-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="b198d-106">A chave do registro geralmente está localizada em:</span><span class="sxs-lookup"><span data-stu-id="b198d-106">The registry key is usually located at:</span></span>

<span data-ttu-id="b198d-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="b198d-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="b198d-108">O seguinte valor de cadeia de caracteres múltipla deve estar presente:</span><span class="sxs-lookup"><span data-stu-id="b198d-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="b198d-109">Os dados de valor para `RedirectUrls` são uma lista de todas as URLs que você especificou para redirecionamento quando criou o pacote do espaço de trabalho do MED-v usando o **pacote do espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="b198d-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="b198d-110">Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="b198d-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="b198d-111">Você pode adicionar e remover informações de redirecionamento de URL executando uma das seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b198d-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="b198d-112">Editar a chave do registro de redirecionamento de URL e implantar usando a política de grupo</span><span class="sxs-lookup"><span data-stu-id="b198d-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="b198d-113">Editar o arquivo de texto de redirecionamento de URL e recriar o espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b198d-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="b198d-114">Para atualizar as informações de redirecionamento de URL usando a política de grupo</span><span class="sxs-lookup"><span data-stu-id="b198d-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="b198d-115">Edite o valor da chave múltipla da chave do registro que é chamado `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="b198d-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="b198d-116">Esse valor geralmente está localizado em:</span><span class="sxs-lookup"><span data-stu-id="b198d-116">This value is typically located at:</span></span>

    <span data-ttu-id="b198d-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="b198d-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="b198d-118">Se você estiver adicionando URLs à chave do registro, insira uma por linha, conforme necessário, quando criou o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b198d-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="b198d-119">Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="b198d-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="b198d-120">Implante a chave do registro atualizada usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b198d-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="b198d-121">Para obter mais informações sobre como usar a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="b198d-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="b198d-122">**Observação**  Esse método de edição de informações de redirecionamento de URL é uma prática recomendada do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b198d-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="b198d-123">Para recriar o espaço de trabalho do MED-V usando um arquivo de texto de URL atualizado</span><span class="sxs-lookup"><span data-stu-id="b198d-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="b198d-124">Outro método para adicionar e remover URLs da lista de redirecionamento é atualizar o arquivo de texto de redirecionamento de URL e usá-lo para criar um novo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="b198d-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="b198d-125">Em seguida, você pode reimplantar o espaço de trabalho do MED-V como antes, usando o processo padrão de implantação, como um sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="b198d-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="b198d-126">**Importante**  Não recomendamos esse método de edição de informações de redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="b198d-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="b198d-127">Além disso, a qualquer momento em que você reimplantar o espaço de trabalho do MED-V para a sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="b198d-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="b198d-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b198d-128">Related topics</span></span>


[<span data-ttu-id="b198d-129">Como testar o redirecionamento da URL</span><span class="sxs-lookup"><span data-stu-id="b198d-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="b198d-130">Gerenciamento de aplicativos implantados em espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="b198d-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="b198d-131">Criar um pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="b198d-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





