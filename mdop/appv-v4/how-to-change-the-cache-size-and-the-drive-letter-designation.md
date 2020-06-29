---
title: Como alterar o tamanho do cache e a designação da letra da unidade
description: Como alterar o tamanho do cache e a designação da letra da unidade
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797245"
---
# <span data-ttu-id="180bf-103">Como alterar o tamanho do cache e a designação da letra da unidade</span><span class="sxs-lookup"><span data-stu-id="180bf-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="180bf-104">Você pode alterar o tamanho do cache e a designação da letra da unidade diretamente do nó do **Application Virtualization** no console de gerenciamento do cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="180bf-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="180bf-105">Observação</span><span class="sxs-lookup"><span data-stu-id="180bf-105">Note</span></span>**  
<span data-ttu-id="180bf-106">Após o tamanho do cache ter sido definido, ele não pode ser menor.</span><span class="sxs-lookup"><span data-stu-id="180bf-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="180bf-107">Para alterar o tamanho do cache</span><span class="sxs-lookup"><span data-stu-id="180bf-107">To change the cache size</span></span>**

1.  <span data-ttu-id="180bf-108">Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="180bf-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="180bf-109">Selecione a guia **sistema de arquivos** na caixa de diálogo **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="180bf-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="180bf-110">Na seção **configurações de configuração de cache do cliente** , clique em um dos seguintes botões de opção para escolher como gerenciar o espaço do cache:</span><span class="sxs-lookup"><span data-stu-id="180bf-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="180bf-111">Importante</span><span class="sxs-lookup"><span data-stu-id="180bf-111">Important</span></span>**  
    <span data-ttu-id="180bf-112">Se você selecionar a configuração de **limite de espaço livre em disco** , o valor inserido definirá o tamanho do cache para o tamanho total do disco menos o limite de espaço livre em disco que você inseriu.</span><span class="sxs-lookup"><span data-stu-id="180bf-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="180bf-113">Se, em seguida, você quiser reverter usando a configuração de **tamanho máximo do cache** , especifique um número maior do que o tamanho do cache existente.</span><span class="sxs-lookup"><span data-stu-id="180bf-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="180bf-114">Caso contrário, o erro "novo tamanho deve ser maior do que o tamanho do cache existente" será exibido.</span><span class="sxs-lookup"><span data-stu-id="180bf-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="180bf-115">Clique em **OK** ou **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="180bf-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="180bf-116">Para alterar a designação da letra da unidade</span><span class="sxs-lookup"><span data-stu-id="180bf-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="180bf-117">Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="180bf-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="180bf-118">Na guia **sistema de arquivos** na caixa de diálogo **Propriedades** , no campo **unidade a ser usado** , selecione a letra da unidade desejada na lista suspensa de letras de unidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="180bf-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="180bf-119">Essa configuração torna-se efetiva quando o computador é reinicializado.</span><span class="sxs-lookup"><span data-stu-id="180bf-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="180bf-120">Clique em **OK** ou **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="180bf-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="180bf-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="180bf-121">Related topics</span></span>


[<span data-ttu-id="180bf-122">Como configurar o Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="180bf-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









