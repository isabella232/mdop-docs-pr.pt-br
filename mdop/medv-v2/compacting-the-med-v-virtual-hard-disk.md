---
title: Compactação do disco rígido virtual da MED-V
description: Compactação do disco rígido virtual da MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799240"
---
# <span data-ttu-id="11af2-103">Compactação do disco rígido virtual da MED-V</span><span class="sxs-lookup"><span data-stu-id="11af2-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="11af2-104">Embora seja opcional, você pode compactar o disco rígido virtual (VHD) para recuperar espaço em disco vazio e reduzir o tamanho do VHD antes de configurar a imagem do PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="11af2-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="11af2-105">**Importante**  Antes de prosseguir, crie uma cópia de backup da sua imagem do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11af2-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="11af2-106">Preparando o disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="11af2-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="11af2-107">Abra a imagem do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11af2-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="11af2-108">Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**, clique em **PC virtual do Windows**e, em seguida, clique duas vezes em sua imagem do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11af2-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="11af2-109">Limpe o cache de DLL.</span><span class="sxs-lookup"><span data-stu-id="11af2-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="11af2-110">Em um prompt de comando na máquina virtual, digite **sfc/cachesize = 1**.</span><span class="sxs-lookup"><span data-stu-id="11af2-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="11af2-111">Reinicie a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11af2-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="11af2-112">Em um prompt de comando na máquina virtual, digite **Sfc/purgecache**.</span><span class="sxs-lookup"><span data-stu-id="11af2-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="11af2-113">Exclua arquivos desnecessários, como desinstaladores, arquivos temporários, arquivos de log, arquivos de página, pastas compartilhadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="11af2-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="11af2-114">Desative a restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="11af2-114">Turn off System Restore.</span></span> <span data-ttu-id="11af2-115">Você também pode especificar essa etapa no seu arquivo Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="11af2-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="11af2-116">No **painel de controle**, clique duas vezes em **sistema**e selecione a guia **restauração do sistema** .</span><span class="sxs-lookup"><span data-stu-id="11af2-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="11af2-117">Selecione **Desativar restauração do sistema**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="11af2-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="11af2-118">Definir tamanhos máximos de log de eventos e limpar todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="11af2-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="11af2-119">Abra o Visualizador de eventos.</span><span class="sxs-lookup"><span data-stu-id="11af2-119">Open the event viewer.</span></span>

        <span data-ttu-id="11af2-120">Clique em **Iniciar**, clique em **painel de controle**, clique duas vezes em **Ferramentas administrativas**e clique duas vezes em **Visualizador de eventos**.</span><span class="sxs-lookup"><span data-stu-id="11af2-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="11af2-121">Clique com o botão direito do mouse em **aplicativo**e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="11af2-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="11af2-122">Na área **tamanho do log** , defina o **tamanho máximo do log** como 512KB e, em seguida, selecione **substituir eventos conforme necessário**.</span><span class="sxs-lookup"><span data-stu-id="11af2-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="11af2-123">Clique em **Limpar registro**.</span><span class="sxs-lookup"><span data-stu-id="11af2-123">Click **Clear Log**.</span></span> <span data-ttu-id="11af2-124">Na caixa de diálogo **Visualizador de eventos** exibida, clique em **não**.</span><span class="sxs-lookup"><span data-stu-id="11af2-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="11af2-125">Na janela **Propriedades** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="11af2-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="11af2-126">Repita as etapas a a e para os logs de **segurança** e do **sistema** .</span><span class="sxs-lookup"><span data-stu-id="11af2-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="11af2-127">Execute a ferramenta de limpeza de disco.</span><span class="sxs-lookup"><span data-stu-id="11af2-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="11af2-128">Clique em **Iniciar**, **em todos os programas**, em **acessórios**, em **Ferramentas do sistema**e, em seguida, clique em limpeza de **disco**.</span><span class="sxs-lookup"><span data-stu-id="11af2-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="11af2-129">Configure o arquivo de página conforme necessário para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="11af2-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="11af2-130">No **painel de controle**, clique duas vezes em **sistema**e selecione a guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="11af2-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="11af2-131">Na área **desempenho** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="11af2-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="11af2-132">Na área **memória virtual** , clique em **alterar**.</span><span class="sxs-lookup"><span data-stu-id="11af2-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="11af2-133">Defina as configurações do arquivo de página.</span><span class="sxs-lookup"><span data-stu-id="11af2-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="11af2-134">Desligue a imagem do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11af2-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="11af2-135">Desfragmentando e compactando o disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="11af2-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="11af2-136">No **painel de controle** do computador host executando o Windows 7, clique em **Ferramentas administrativas**, clique duas vezes em **Gerenciamento do computador**e clique em gerenciamento de **disco**.</span><span class="sxs-lookup"><span data-stu-id="11af2-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="11af2-137">Usando o console de gerenciamento de disco, anexe (Monte) o disco rígido virtual e Desfragmente o disco.</span><span class="sxs-lookup"><span data-stu-id="11af2-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="11af2-138">Usando uma ferramenta de extração ISO, extraia o precompacto. ISO localizado na pasta \\Program Files\\Windows virtual PC\\Integration Components.</span><span class="sxs-lookup"><span data-stu-id="11af2-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="11af2-139">Use o programa precompact.exe para compactar o disco rígido virtual do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11af2-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="11af2-140">Usando o console de gerenciamento de disco, desconecte o disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="11af2-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="11af2-141">Compactar o disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="11af2-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="11af2-142">Abra o Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="11af2-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="11af2-143">Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.</span><span class="sxs-lookup"><span data-stu-id="11af2-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="11af2-144">Clique com o botão direito do mouse na imagem do Windows XP e selecione **configurações**.</span><span class="sxs-lookup"><span data-stu-id="11af2-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="11af2-145">Clique em **disco rígido** para aquele que corresponde à sua imagem do Windows XP e clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="11af2-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="11af2-146">Clique em **compactar disco rígido virtual**.</span><span class="sxs-lookup"><span data-stu-id="11af2-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="11af2-147">Clique em **compactar** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="11af2-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="11af2-148">Crie uma cópia de backup do seu disco rígido virtual compactado.</span><span class="sxs-lookup"><span data-stu-id="11af2-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="11af2-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11af2-149">Related topics</span></span>


[<span data-ttu-id="11af2-150">Como configurar uma imagem do Windows Virtual PC para a MED-V</span><span class="sxs-lookup"><span data-stu-id="11af2-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="11af2-151">Referência técnica da MED-V</span><span class="sxs-lookup"><span data-stu-id="11af2-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





