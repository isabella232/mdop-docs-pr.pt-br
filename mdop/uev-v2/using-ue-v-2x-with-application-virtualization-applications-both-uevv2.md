---
title: Usar o UE-V 2. x com aplicativos do Application Virtualization
description: Usar o UE-V 2. x com aplicativos do Application Virtualization
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800039"
---
# <span data-ttu-id="8d9a2-103">Usar o UE-V 2. x com aplicativos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8d9a2-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="8d9a2-104">O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 dão suporte a aplicativos Microsoft Application Virtualization (App-V) sem modificações obrigatórias no pacote do App-V ou no modelo UE-V.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="8d9a2-105">No entanto, uma etapa adicional é necessária porque não é possível executar o gerador do UE-V diretamente em um aplicativo virtualizado do V App-V.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="8d9a2-106">Em vez disso, você deve instalar o aplicativo localmente, gerar o modelo e, em seguida, aplicar o modelo ao aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="8d9a2-107">O UE-V é compatível com pacotes do App-v 4,5, App-V 4,6 e App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="8d9a2-108">Sincronização de configurações do UE-V para aplicativos App-V</span><span class="sxs-lookup"><span data-stu-id="8d9a2-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="8d9a2-109">O UE-V monitora quando um aplicativo é aberto pelo nome do programa e, opcionalmente, por números de versão do arquivo e números de versão do produto, se o aplicativo é instalado localmente ou virtualmente usando o App-V.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="8d9a2-110">Quando o aplicativo é iniciado, o UE-V monitora o processo App-V, aplica todas as configurações armazenadas no caminho de armazenamento de configurações do usuário e, em seguida, permite que o aplicativo inicie normalmente.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="8d9a2-111">O UE-V monitora aplicativos do App-V e traduz automaticamente o arquivo relevante e os caminhos do registro para o local virtualizado, em oposição ao local físico fora do ambiente de computação do App-V.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="8d9a2-112">Para implementar a sincronização de configurações para um aplicativo virtualizado</span><span class="sxs-lookup"><span data-stu-id="8d9a2-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="8d9a2-113">Execute o UE-V Generator para coletar as configurações do aplicativo instalado localmente cujas configurações você deseja sincronizar entre computadores.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="8d9a2-114">Esse processo cria um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-114">This process creates a settings location template.</span></span> <span data-ttu-id="8d9a2-115">Se você usar um modelo interno, como o modelo do Microsoft Office 2010, pule esta etapa.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="8d9a2-116">Para obter mais informações sobre como executar o UE-V Generator, consulte [implantar o UE-v 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="8d9a2-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="8d9a2-117">Instale o pacote do aplicativo App-V se ainda não tiver feito isso.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="8d9a2-118">Publique o modelo no local do catálogo de modelos de configurações ou instale manualmente o modelo usando o `Register-UEVTemplate` cmdlet do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="8d9a2-119">**Observação**  Se você publicar o modelo recém-criado no catálogo de modelos de configurações, o cliente não receberá o modelo até que o provedor de sincronização atualize as configurações.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="8d9a2-120">Para iniciar manualmente esse processo, abra o **Agendador de tarefas**, expanda **biblioteca do Agendador de tarefas**, expanda **Microsoft**e expanda **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="8d9a2-121">No painel de resultados, clique com o botão direito do mouse em **atualização automática de modelo**e clique em **executar**.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="8d9a2-122">Inicie o pacote App-V.</span><span class="sxs-lookup"><span data-stu-id="8d9a2-122">Start the App-V package.</span></span>






## <span data-ttu-id="8d9a2-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d9a2-123">Related topics</span></span>


[<span data-ttu-id="8d9a2-124">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8d9a2-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





