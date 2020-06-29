---
title: Como criar uma imagem do Windows Virtual PC para a MED-V
description: Como criar uma imagem do Windows Virtual PC para a MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796061"
---
# <span data-ttu-id="05382-103">Como criar uma imagem do Windows Virtual PC para a MED-V</span><span class="sxs-lookup"><span data-stu-id="05382-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="05382-104">Antes de poder entregar um espaço de trabalho do MED-V para os usuários, primeiro você precisa preparar um disco rígido virtual que você usa para criar o pacote de instalação do espaço de trabalho do MED-V para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="05382-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="05382-105">Para preparar o disco rígido virtual necessário, você deve criar uma imagem do Windows Virtual PC que contenha o sistema operacional, as atualizações e o software necessários para que você implante posteriormente as informações de aplicativos e de redirecionamento de URL para os usuários.</span><span class="sxs-lookup"><span data-stu-id="05382-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="05382-106">Esta seção fornece orientação sobre como criar o disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="05382-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="05382-107">Para criar uma imagem virtual do MED-V, você deve seguir estas etapas.</span><span class="sxs-lookup"><span data-stu-id="05382-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="05382-108">Criar uma imagem do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05382-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="05382-109">Instalar o Windows XP na imagem</span><span class="sxs-lookup"><span data-stu-id="05382-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="05382-110">Instalar o .NET Framework na imagem</span><span class="sxs-lookup"><span data-stu-id="05382-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="05382-111">Aplicar atualizações à imagem</span><span class="sxs-lookup"><span data-stu-id="05382-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="05382-112">Instalar componentes de integração</span><span class="sxs-lookup"><span data-stu-id="05382-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="05382-113">Criando uma imagem do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05382-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="05382-114">Para criar uma imagem do Windows Virtual PC, consulte a documentação do PC virtual do Windows:</span><span class="sxs-lookup"><span data-stu-id="05382-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="05382-115">[Página inicial do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="05382-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="05382-116">[Ajuda do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="05382-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="05382-117">Como alternativa, se você já tiver um arquivo de imagem do Windows (WIM) que deseja usar como base para a sua imagem virtual, é possível convertê-lo em um VHD que você usa para criar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="05382-118">Para obter mais informações sobre como converter um WIM em um disco rígido virtual, consulte [suporte a VHD nativo no Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="05382-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="05382-119">**Importante**  O MED-V aceita apenas um disco rígido virtual por máquina virtual e apenas uma partição em cada disco virtual.</span><span class="sxs-lookup"><span data-stu-id="05382-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="05382-120">Depois de criar seu disco rígido virtual, instale o Windows XP na imagem.</span><span class="sxs-lookup"><span data-stu-id="05382-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="05382-121">Instalar o Windows XP em uma imagem do PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="05382-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="05382-122">O MED-V exige que o Windows XP SP3 esteja instalado na imagem do PC virtual do Windows antes de criar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="05382-123">Para obter mais informações sobre como instalar o Windows XP, consulte [criar uma máquina virtual e instalar um sistema operacional convidado](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="05382-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="05382-124">Instalando o .NET Framework 3,5 SP1 em uma imagem do PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="05382-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="05382-125">Você deve instalar manualmente o .NET Framework 3,5 SP1 e o Update KB959209 na imagem do PC virtual do Windows que você prepara para usar com o MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="05382-126">A atualização [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) corrige vários problemas de compatibilidade de aplicativos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="05382-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="05382-127">Aplicando atualizações à imagem do PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="05382-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="05382-128">Depois de instalar o Windows XP em sua máquina virtual, instale todas as atualizações necessárias do Windows XP na imagem, como SP3.</span><span class="sxs-lookup"><span data-stu-id="05382-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="05382-129">Você também pode instalar algumas atualizações opcionais para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="05382-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="05382-130">**Importante**  O MED-V exige que o Windows XP SP3 esteja em execução no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05382-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="05382-131">**Aviso**  Ao instalar atualizações do Windows XP, certifique-se de que você permaneça na versão do Internet Explorer no convidado que pretende usar no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="05382-132">Por exemplo, se você pretende executar o Internet Explorer 6 no espaço de trabalho do MED-V, certifique-se de que todas as atualizações instaladas agora não incluam o Internet Explorer 7 ou o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="05382-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="05382-133">Além disso, recomendamos que você configure o registro para impedir que as atualizações automáticas atualizem o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="05382-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="05382-134">Instalar uma atualização de desempenho opcional</span><span class="sxs-lookup"><span data-stu-id="05382-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="05382-135">Embora seja opcional, recomendamos que você instale a seguinte atualização para o [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="05382-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="05382-136">Esta atualização aumenta o desempenho das pastas compartilhadas em uma sessão de serviços de terminal:</span><span class="sxs-lookup"><span data-stu-id="05382-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="05382-137">**Observação**  A atualização está disponível publicamente.</span><span class="sxs-lookup"><span data-stu-id="05382-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="05382-138">No entanto, você pode ser solicitado a aceitar um contrato de serviços da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05382-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="05382-139">Siga os prompts nas páginas da Web sucessivas para recuperar este hotfix.</span><span class="sxs-lookup"><span data-stu-id="05382-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="05382-140">Configurando uma atualização de desempenho de política de grupo</span><span class="sxs-lookup"><span data-stu-id="05382-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="05382-141">Por padrão, a política de grupo é baixada para um computador, um byte de cada vez.</span><span class="sxs-lookup"><span data-stu-id="05382-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="05382-142">Isso causa atrasos enquanto o MED-V está sendo associado ao domínio.</span><span class="sxs-lookup"><span data-stu-id="05382-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="05382-143">Para aumentar o desempenho da política de grupo, defina o seguinte valor da chave do registro para o registro:</span><span class="sxs-lookup"><span data-stu-id="05382-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="05382-144">Subchave do registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="05382-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="05382-145">Entrada: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="05382-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="05382-146">Tipo: DWORD</span><span class="sxs-lookup"><span data-stu-id="05382-146">Type: DWORD</span></span>

<span data-ttu-id="05382-147">Valor: 1</span><span class="sxs-lookup"><span data-stu-id="05382-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="05382-148">Instalando componentes de integração</span><span class="sxs-lookup"><span data-stu-id="05382-148">Installing Integration Components</span></span>


<span data-ttu-id="05382-149">O Windows Virtual PC inclui o pacote de componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="05382-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="05382-150">Isso fornece recursos que melhoram a interação entre o ambiente virtual e o computador físico.</span><span class="sxs-lookup"><span data-stu-id="05382-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="05382-151">Por exemplo, o pacote de componentes de integração permite que o mouse se movimente entre o host e os computadores convidados.</span><span class="sxs-lookup"><span data-stu-id="05382-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="05382-152">**Importante**  O MED-V requer a instalação do pacote de componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="05382-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="05382-153">Ao configurar a imagem virtual para funcionar com o MED-V, você deve instalar manualmente o pacote de componentes de integração no sistema operacional convidado para disponibilizar os recursos de integração disponíveis.</span><span class="sxs-lookup"><span data-stu-id="05382-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="05382-154">Para obter mais informações sobre como instalar e usar o pacote de componentes de integração, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05382-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="05382-155">[Instalar ou atualizar o pacote de componentes de integração](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="05382-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="05382-156">[Sobre os recursos de integração](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="05382-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="05382-157">Instalando a atualização do RemoteApp</span><span class="sxs-lookup"><span data-stu-id="05382-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="05382-158">Depois de instalar o pacote de componentes de integração, você será solicitado a instalar a seguinte atualização: "atualização para Windows XP SP3 para habilitar o RemoteApp".</span><span class="sxs-lookup"><span data-stu-id="05382-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="05382-159">Este é um componente obrigatório do MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="05382-160">**Importante**  Se você não for solicitado a instalar a atualização do RemoteApp, será necessário baixá-la e instalá-la manualmente.</span><span class="sxs-lookup"><span data-stu-id="05382-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="05382-161">Para obter mais informações e instruções sobre como baixar essa atualização, consulte [atualização para Windows XP SP3 para habilitar o RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="05382-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="05382-162">Habilitando a área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="05382-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="05382-163">Por padrão, a área de trabalho remota é habilitada após a instalação do pacote de componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="05382-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="05382-164">Para que o MED-V seja operacional, verifique se a área de trabalho remota está habilitada e não distribua nenhuma política de grupo que desativasse.</span><span class="sxs-lookup"><span data-stu-id="05382-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="05382-165">Para obter informações sobre como habilitar a área de trabalho remota, consulte [habilitar ou desabilitar a área de trabalho remota](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="05382-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="05382-166">Personalizando o Internet Explorer usando o kit de administração do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="05382-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="05382-167">Se desejar, você pode usar o kit de administração do Internet Explorer para personalizar o Internet Explorer no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="05382-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="05382-168">Para obter mais informações, consulte o [Kit de administração e o guia de implantação do Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?linkid=200007).</span><span class="sxs-lookup"><span data-stu-id="05382-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="05382-169">**Aviso**  Você deve considerar as questões de segurança associadas à personalização do Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="05382-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="05382-170">Para obter mais informações, consulte [práticas recomendadas de segurança para operações do MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="05382-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="05382-171">Depois que o disco rígido virtual for instalado com um sistema operacional convidado atualizado, você poderá instalar aplicativos na imagem.</span><span class="sxs-lookup"><span data-stu-id="05382-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="05382-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05382-172">Related topics</span></span>


[<span data-ttu-id="05382-173">Instalar aplicativos em uma imagem do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05382-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="05382-174">Como configurar uma imagem do Windows Virtual PC para a MED-V</span><span class="sxs-lookup"><span data-stu-id="05382-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





