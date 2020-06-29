---
title: Instalação e remoção de um aplicativo no espaço de trabalho da MED-V
description: Instalação e remoção de um aplicativo no espaço de trabalho da MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800028"
---
# <span data-ttu-id="5a191-103">Instalação e remoção de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="5a191-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="5a191-104">Os aplicativos que são incompatíveis com o sistema operacional do host podem ser executados no espaço de trabalho do MED-V e abertos no espaço de trabalho do MED-V da mesma maneira que eles são abertos a partir do computador host, no menu **Iniciar** ou usando um atalho de localhost.</span><span class="sxs-lookup"><span data-stu-id="5a191-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="5a191-105">Depois de implantar um espaço de trabalho do MED-V, você tem várias opções diferentes disponíveis para instalar e remover aplicativos no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5a191-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="5a191-106">Essas opções incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5a191-106">These options include the following:</span></span>

-   [<span data-ttu-id="5a191-107">Usar a política de grupo</span><span class="sxs-lookup"><span data-stu-id="5a191-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="5a191-108">Usando um sistema de distribuição de software eletrônico</span><span class="sxs-lookup"><span data-stu-id="5a191-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="5a191-109">Usando a virtualização de aplicativos (APP-V)</span><span class="sxs-lookup"><span data-stu-id="5a191-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="5a191-110">Atualizando a imagem principal</span><span class="sxs-lookup"><span data-stu-id="5a191-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="5a191-111">**Importante**  Para garantir que um aplicativo instalado seja automaticamente publicado no host, instale o aplicativo na máquina virtual para **todos os usuários**.</span><span class="sxs-lookup"><span data-stu-id="5a191-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="5a191-112">Para obter mais informações sobre a publicação de aplicativos, consulte [como publicar e cancelar a publicação de um aplicativo no espaço de trabalho do MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="5a191-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="5a191-113">**Dica**  O MED-V não é compatível com o redirecionamento de convidado para host para manipulação de conteúdo, como clicar duas vezes em um documento do Microsoft Word no Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5a191-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="5a191-114">Portanto, os aplicativos necessários, como o Microsoft Word, devem ser instalados no espaço de trabalho do MED-V para fornecer a funcionalidade padrão de manipulação de conteúdo que um usuário final pode esperar.</span><span class="sxs-lookup"><span data-stu-id="5a191-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="5a191-115">Adicionando e removendo aplicativos usando a política de grupo</span><span class="sxs-lookup"><span data-stu-id="5a191-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="5a191-116">Você pode usar a política de grupo e os objetos de política de grupo para atribuir ou publicar aplicativos em todos ou alguns espaços de trabalho do MED-V na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="5a191-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="5a191-117">Para aplicativos atribuídos, quando um usuário final faz logon em seu computador, o aplicativo é exibido no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5a191-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="5a191-118">Quando eles selecionarem o novo aplicativo pela primeira vez, o aplicativo será instalado e estará pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="5a191-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="5a191-119">Para aplicativos publicados, o aplicativo não é exibido no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5a191-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="5a191-120">Ele só está disponível para o usuário final instalar usando **Adicionar ou remover programas** no painel de **controle** ou abrindo um arquivo associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a191-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="5a191-121">Você também pode usar a política de grupo e objetos de política de grupo da mesma maneira para remover aplicativos do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5a191-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="5a191-122">Para obter mais informações sobre como adicionar e remover aplicativos usando a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="5a191-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="5a191-123">Adicionar e remover aplicativos usando um sistema ESD</span><span class="sxs-lookup"><span data-stu-id="5a191-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="5a191-124">Um sistema ESD (Electronic Software Distribution) foi projetado para a implantação eficiente de software e outras informações para vários computadores diferentes em conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="5a191-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="5a191-125">Se a sua organização usa um sistema ESD para implantar o software, você pode usá-lo para adicionar e remover aplicativos em espaços de trabalho do MED-V da mesma forma que adiciona e remove aplicativos em computadores físicos.</span><span class="sxs-lookup"><span data-stu-id="5a191-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="5a191-126">Adicionando e removendo aplicativos usando o APP-V</span><span class="sxs-lookup"><span data-stu-id="5a191-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="5a191-127">O Microsoft Application Virtualization (App-V) fornece a funcionalidade administrativa para disponibilizar aplicativos para os computadores de usuários finais sem precisar instalar os aplicativos diretamente nesses computadores.</span><span class="sxs-lookup"><span data-stu-id="5a191-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="5a191-128">Você pode querer usar o MED-V e o App-V juntos, se, por exemplo, a sua organização tiver aplicativos que você tenha sequenciado com o App-V no Windows XP, e resequenciar os mesmos atrasaria a migração para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a191-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="5a191-129">Você pode usar o MED-V em conjunto com o App-V para adicionar e remover aplicativos virtuais em um espaço de trabalho do MED-V implantado.</span><span class="sxs-lookup"><span data-stu-id="5a191-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="5a191-130">Para gerenciar aplicativos dessa maneira, primeiro você deve instalar o agente do App-V no sistema operacional de convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5a191-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="5a191-131">Em seguida, você pode usar o App-V no espaço de trabalho do MED-V para adicionar e remover os aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="5a191-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="5a191-132">Para obter informações sobre como instalar e usar o App-V, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="5a191-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="5a191-133">**Importante**  Os aplicativos do App-V que você publica no espaço de trabalho do MED-V têm associações de tipo de arquivo que não podem ser redirecionadas do computador host para a máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="5a191-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="5a191-134">No entanto, o usuário final ainda pode acessar esses tipos de arquivo clicando em **arquivo**e, em seguida, clicando em **abrir** no aplicativo publicado do App-V.</span><span class="sxs-lookup"><span data-stu-id="5a191-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="5a191-135">Para forçar o redirecionamento dessas associações de tipo de arquivo, consulte App-V para associações de tipo de arquivo mapeado digitando o seguinte em um prompt de comando na máquina virtual convidada: **SFTMIME/QUERY OBJ: Type**.</span><span class="sxs-lookup"><span data-stu-id="5a191-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="5a191-136">Em seguida, mapeie essas associações de tipo de arquivo no computador host.</span><span class="sxs-lookup"><span data-stu-id="5a191-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="5a191-137">Adicionar e remover aplicativos na imagem principal</span><span class="sxs-lookup"><span data-stu-id="5a191-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="5a191-138">Embora não seja considerada uma prática recomendada do MED-V, você pode adicionar e remover aplicativos diretamente na imagem principal.</span><span class="sxs-lookup"><span data-stu-id="5a191-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="5a191-139">Depois de adicionar ou remover um aplicativo, você pode reimplantar o espaço de trabalho do MED-V novamente em sua empresa da mesma forma que o implantou originalmente.</span><span class="sxs-lookup"><span data-stu-id="5a191-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="5a191-140">Para obter mais informações sobre como adicionar ou remover aplicativos na imagem principal, consulte [Instalando aplicativos em uma imagem do Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).</span><span class="sxs-lookup"><span data-stu-id="5a191-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="5a191-141">**Importante**  Não recomendamos esse método de gerenciamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5a191-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="5a191-142">Se você adicionar ou remover aplicativos da imagem principal e reimplantar o espaço de trabalho do MED-V novamente em sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="5a191-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="5a191-143">**Observação**  Embora um aplicativo seja instalado em um espaço de trabalho do MED-V, você também pode ter que publicar o aplicativo antes que ele fique disponível para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="5a191-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="5a191-144">Por exemplo, talvez seja necessário publicar um aplicativo instalado se a instalação não criar automaticamente um atalho no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5a191-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="5a191-145">Da mesma forma, para cancelar a publicação de um aplicativo, talvez seja necessário remover manualmente um atalho do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="5a191-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="5a191-146">Por padrão, a maioria dos aplicativos é publicada no momento em que eles são instalados, quando os atalhos são automaticamente criados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="5a191-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="5a191-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a191-147">Related topics</span></span>


[<span data-ttu-id="5a191-148">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="5a191-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="5a191-149">Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="5a191-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





