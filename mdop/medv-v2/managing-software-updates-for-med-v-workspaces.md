---
title: Gerenciamento de atualizações de software para espaços de trabalho da MED-V
description: Gerenciamento de atualizações de software para espaços de trabalho da MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799547"
---
# <span data-ttu-id="b7a18-103">Gerenciamento de atualizações de software para espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="b7a18-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="b7a18-104">Você tem várias opções diferentes disponíveis para fornecer atualizações de software para os aplicativos no espaço de trabalho do MED-V implantado.</span><span class="sxs-lookup"><span data-stu-id="b7a18-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="b7a18-105">**Observação**  Para obter informações sobre como especificar as configurações de configuração que definem como o MED-V recebe atualizações automáticas, consulte [gerenciando atualizações automáticas para os espaços de trabalho do MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="b7a18-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="b7a18-106">Atualizando o software em um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b7a18-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="b7a18-107">Usando um sistema de distribuição de software eletrônico</span><span class="sxs-lookup"><span data-stu-id="b7a18-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="b7a18-108">Se a sua organização usa um sistema ESD (sistema de distribuição de software eletrônico) para implantar um software, você pode usá-lo para fornecer atualizações de software para aplicativos em espaços de trabalho do MED-V, da mesma forma que fornece atualizações para aplicativos em computadores físicos.</span><span class="sxs-lookup"><span data-stu-id="b7a18-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="b7a18-109">Usar a política de grupo</span><span class="sxs-lookup"><span data-stu-id="b7a18-109">Using Group Policy</span></span>**

    <span data-ttu-id="b7a18-110">Se a sua organização implantar o software usando a política de grupo, você poderá usá-lo para fornecer atualizações de software para aplicativos em espaços de trabalho do MED-V da mesma forma que fornece atualizações para aplicativos em computadores físicos.</span><span class="sxs-lookup"><span data-stu-id="b7a18-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="b7a18-111">Usando a virtualização de aplicativos (APP-V)</span><span class="sxs-lookup"><span data-stu-id="b7a18-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="b7a18-112">Se você usa MED-V juntamente com o App-V, é possível fornecer atualizações de software para aplicativos no espaço de trabalho do MED-V seguindo as etapas exigidas pela App-V para a atualização do software.</span><span class="sxs-lookup"><span data-stu-id="b7a18-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="b7a18-113">Para obter mais informações, consulte [virtualização de aplicativo](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="b7a18-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="b7a18-114">Atualização do software na imagem principal</span><span class="sxs-lookup"><span data-stu-id="b7a18-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="b7a18-115">Embora não seja considerada uma prática recomendada do MED-V, você pode instalar atualizações de software para aplicativos na imagem principal.</span><span class="sxs-lookup"><span data-stu-id="b7a18-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="b7a18-116">Depois de instalar as atualizações, você pode reimplantar o espaço de trabalho do MED-V novamente em sua empresa da mesma forma que o implantou originalmente.</span><span class="sxs-lookup"><span data-stu-id="b7a18-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="b7a18-117">**Importante**  Não recomendamos esse método de gerenciamento de atualizações de software.</span><span class="sxs-lookup"><span data-stu-id="b7a18-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="b7a18-118">Além disso, se você atualizar o software na imagem principal e reimplantar o espaço de trabalho do MED-V novamente em sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="b7a18-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="b7a18-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7a18-119">Related topics</span></span>


[<span data-ttu-id="b7a18-120">Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="b7a18-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="b7a18-121">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b7a18-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="b7a18-122">Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="b7a18-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





