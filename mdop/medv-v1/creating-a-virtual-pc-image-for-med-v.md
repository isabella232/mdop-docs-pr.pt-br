---
title: Criando uma imagem do Virtual PC para o MED-V
description: Criando uma imagem do Virtual PC para o MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799317"
---
# <span data-ttu-id="b68c6-103">Criando uma imagem do Virtual PC para o MED-V</span><span class="sxs-lookup"><span data-stu-id="b68c6-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="b68c6-104">Para criar uma imagem do Virtual PC (VPC) para MED-V, você deve executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b68c6-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="b68c6-105">[Crie uma imagem do VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="b68c6-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="b68c6-106">[Instale o pacote do espaço de trabalho do MED-V. msi na imagem do VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="b68c6-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="b68c6-107">[Execute a ferramenta de pré-requisitos da máquina virtual MED-V na imagem do VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="b68c6-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="b68c6-108">[Configurar manualmente os pré-requisitos da máquina virtual na imagem do VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span><span class="sxs-lookup"><span data-stu-id="b68c6-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="b68c6-109">[Configurar o Sysprep para imagens do MED-V](#bkmk-howtoconfiguresysprepformedvimages) (opcional).</span><span class="sxs-lookup"><span data-stu-id="b68c6-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="b68c6-110">[Desative o Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="b68c6-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="b68c6-111">Criando uma imagem do Virtual PC usando o Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b68c6-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="b68c6-112">Para criar uma imagem do Virtual PC usando o Microsoft Virtual PC, consulte a documentação do Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b68c6-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="b68c6-113">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="b68c6-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="b68c6-114">Ajuda do PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="b68c6-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="b68c6-115">Criar uma máquina virtual e instalar um sistema operacional convidado</span><span class="sxs-lookup"><span data-stu-id="b68c6-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="b68c6-116">Como instalar o pacote do espaço de trabalho do MED-V. msi</span><span class="sxs-lookup"><span data-stu-id="b68c6-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="b68c6-117">Após a criação da imagem do Virtual PC, instale o pacote do espaço de trabalho do MED-V. msi na imagem.</span><span class="sxs-lookup"><span data-stu-id="b68c6-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="b68c6-118">Para instalar a imagem do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b68c6-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="b68c6-119">Inicie a máquina virtual e copie o pacote do espaço de trabalho do MED-V. msi dentro.</span><span class="sxs-lookup"><span data-stu-id="b68c6-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="b68c6-120">O pacote do espaço de trabalho do MED-V. msi é chamado *MED-V\_workspace\_x.msi*, em que *x* é o número da versão.</span><span class="sxs-lookup"><span data-stu-id="b68c6-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="b68c6-121">Por exemplo, *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="b68c6-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="b68c6-122">Clique duas vezes no pacote do espaço de trabalho do MED-V. msi e siga as instruções do assistente de instalação.</span><span class="sxs-lookup"><span data-stu-id="b68c6-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="b68c6-123">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-123">Note</span></span>**  
    <span data-ttu-id="b68c6-124">Quando uma nova versão do MED-V for lançada e uma imagem do Virtual PC existente for atualizada, desinstale o pacote do pacote de trabalho do MED-V existente. msi, reinicialize o computador e instale o novo pacote do espaço de trabalho do MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="b68c6-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="b68c6-125">Como executar a ferramenta de pré-requisitos da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b68c6-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="b68c6-126">A ferramenta de pré-requisitos da máquina virtual (VM) é um assistente que automatiza vários dos pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="b68c6-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="b68c6-127">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-127">Note</span></span>**  
<span data-ttu-id="b68c6-128">Embora muitos parâmetros sejam configuráveis no assistente, as propriedades necessárias para o funcionamento adequado do MED-V não são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="b68c6-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="b68c6-129">Para executar a ferramenta de pré-requisitos da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b68c6-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="b68c6-130">Após a instalação do pacote do espaço de trabalho do MED-V. msi, no menu **Iniciar** do Windows, selecione **todos os programas da &gt; &gt; ferramenta de pré-requisitos da VM do MED-v VM**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="b68c6-131">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-131">Note</span></span>**  
    <span data-ttu-id="b68c6-132">O usuário que está executando a ferramenta pré-requisitos de máquina virtual deve ter direitos de administrador local e deve ser o único usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="b68c6-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="b68c6-133">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-133">Click **Next**.</span></span>

3. <span data-ttu-id="b68c6-134">Na página **configurações do Windows** , a partir das seguintes propriedades configuráveis, selecione as que deseja configurar:</span><span class="sxs-lookup"><span data-stu-id="b68c6-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="b68c6-135">Limpar informações do histórico pessoal dos usuários</span><span class="sxs-lookup"><span data-stu-id="b68c6-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="b68c6-136">Limpar diretório temporário de perfis locais</span><span class="sxs-lookup"><span data-stu-id="b68c6-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="b68c6-137">Desabilite os sons nos seguintes eventos do Windows: Iniciar, fazer logon, fazer logoff</span><span class="sxs-lookup"><span data-stu-id="b68c6-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="b68c6-138">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-138">Note</span></span>**  
   <span data-ttu-id="b68c6-139">Não habilite a proteção de página do Windows em uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="b68c6-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="b68c6-140">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-140">Click **Next**.</span></span>

5. <span data-ttu-id="b68c6-141">Na página **configurações do Internet Explorer** , nas seguintes propriedades configuráveis, selecione as que deseja configurar:</span><span class="sxs-lookup"><span data-stu-id="b68c6-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="b68c6-142">Não use recursos de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="b68c6-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="b68c6-143">Desabilitar a reutilização de janelas para iniciar atalhos</span><span class="sxs-lookup"><span data-stu-id="b68c6-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="b68c6-144">Limpar histórico de navegação</span><span class="sxs-lookup"><span data-stu-id="b68c6-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="b68c6-145">Habilitar a navegação com guias no Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="b68c6-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="b68c6-146">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-146">Click **Next**.</span></span>

7. <span data-ttu-id="b68c6-147">Na página **Serviços do Windows** , nas seguintes propriedades configuráveis, selecione as opções a serem configuradas:</span><span class="sxs-lookup"><span data-stu-id="b68c6-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="b68c6-148">Serviço da central de segurança</span><span class="sxs-lookup"><span data-stu-id="b68c6-148">Security center service</span></span>**

   -   **<span data-ttu-id="b68c6-149">Serviço Agendador de tarefas</span><span class="sxs-lookup"><span data-stu-id="b68c6-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="b68c6-150">Serviço de atualizações automáticas</span><span class="sxs-lookup"><span data-stu-id="b68c6-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="b68c6-151">Serviço de restauração do sistema</span><span class="sxs-lookup"><span data-stu-id="b68c6-151">System restore service</span></span>**

   -   **<span data-ttu-id="b68c6-152">Serviço de indexação</span><span class="sxs-lookup"><span data-stu-id="b68c6-152">Indexing service</span></span>**

   -   **<span data-ttu-id="b68c6-153">Configuração zero sem fio</span><span class="sxs-lookup"><span data-stu-id="b68c6-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="b68c6-154">Compatibilidade com troca rápida de usuário</span><span class="sxs-lookup"><span data-stu-id="b68c6-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="b68c6-155">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-155">Click **Next**.</span></span>

9. <span data-ttu-id="b68c6-156">Na página de **logon automático do Windows** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b68c6-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="b68c6-157">Marque a caixa de seleção **habilitar logon automático do Windows** .</span><span class="sxs-lookup"><span data-stu-id="b68c6-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="b68c6-158">Atribua um **nome de usuário** e **senha**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="b68c6-159">Clique em **aplicar**e, na caixa de confirmação que aparece, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="b68c6-160">Na página **Resumo** , clique em **concluir** para fechar o assistente</span><span class="sxs-lookup"><span data-stu-id="b68c6-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="b68c6-161">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-161">Note</span></span>**  
<span data-ttu-id="b68c6-162">Verifique se as políticas de grupo não substituem as configurações obrigatórias definidas na ferramenta pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="b68c6-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="b68c6-163">Como configurar os pré-requisitos de instalação manual da máquina virtual do MED-V</span><span class="sxs-lookup"><span data-stu-id="b68c6-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="b68c6-164">Várias das configurações não podem ser configuradas por meio da ferramenta de pré-requisitos de máquina virtual e devem ser realizadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="b68c6-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="b68c6-165">Configurações da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b68c6-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="b68c6-166">É recomendável definir as seguintes configurações de máquina virtual no console do Microsoft Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="b68c6-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="b68c6-167">Desative as unidades de disquete.</span><span class="sxs-lookup"><span data-stu-id="b68c6-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="b68c6-168">Desabilitar desfazer-discos (\*\* &gt; desfazer configurações-discos\*\*).</span><span class="sxs-lookup"><span data-stu-id="b68c6-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="b68c6-169">Verifique se a imagem tem apenas uma CPU virtual.</span><span class="sxs-lookup"><span data-stu-id="b68c6-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="b68c6-170">Elimine as interações entre a máquina virtual e o usuário, onde eles não estão relacionados a aplicativos publicados (como mensagens que exigem entrada do usuário).</span><span class="sxs-lookup"><span data-stu-id="b68c6-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="b68c6-171">Configurações de imagem</span><span class="sxs-lookup"><span data-stu-id="b68c6-171">Image Settings</span></span>

    <span data-ttu-id="b68c6-172">Defina as seguintes configurações manuais dentro da imagem:</span><span class="sxs-lookup"><span data-stu-id="b68c6-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="b68c6-173">Na janela **Propriedades de opções de energia** , desabilite hibernação e suspensão.</span><span class="sxs-lookup"><span data-stu-id="b68c6-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="b68c6-174">Aplicar as atualizações mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="b68c6-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="b68c6-175">Na caixa de diálogo **inicialização e recuperação do Windows** , na seção **falha do sistema** , desmarque a caixa de seleção **reinicialização automática** .</span><span class="sxs-lookup"><span data-stu-id="b68c6-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="b68c6-176">Verifique se a imagem usa uma chave de licença VLK.</span><span class="sxs-lookup"><span data-stu-id="b68c6-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="b68c6-177">Instalando o VPC Additions</span><span class="sxs-lookup"><span data-stu-id="b68c6-177">Installing VPC Additions</span></span>

    <span data-ttu-id="b68c6-178">No menu **ação** , selecione **instalar ou atualizar adições de máquina virtual**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="b68c6-179">Configurando a impressão</span><span class="sxs-lookup"><span data-stu-id="b68c6-179">Configuring Printing</span></span>

    <span data-ttu-id="b68c6-180">Você pode configurar a impressão a partir do espaço de trabalho do MED-V de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="b68c6-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="b68c6-181">Adicionar uma impressora à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b68c6-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="b68c6-182">Permitir a impressão com impressoras configuradas no computador host.</span><span class="sxs-lookup"><span data-stu-id="b68c6-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="b68c6-183">Como configurar o Sysprep para imagens do MED-V</span><span class="sxs-lookup"><span data-stu-id="b68c6-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="b68c6-184">Em um espaço de trabalho do MED-V, o Sysprep pode ser configurado para atribuir um identificador de segurança exclusivo (SID), especialmente quando vários espaços de trabalho do MED-V são executados em um único computador.</span><span class="sxs-lookup"><span data-stu-id="b68c6-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="b68c6-185">Não é recomendável usar o Sysprep para ingressar em um domínio; em vez disso, use a ação de script do domínio de ingresso no MED-V conforme descrito em [como configurar ações de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b68c6-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="b68c6-186">Observação</span><span class="sxs-lookup"><span data-stu-id="b68c6-186">Note</span></span>**  
<span data-ttu-id="b68c6-187">Sysprep é o utilitário de preparação do sistema da Microsoft para o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="b68c6-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="b68c6-188">Para configurar o Sysprep em um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="b68c6-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="b68c6-189">Crie um diretório na raiz da unidade do sistema chamada *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="b68c6-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="b68c6-190">No CD de instalação do Windows, extraia *deploy.cab* para a raiz da unidade do sistema ou baixe a atualização mais recente das ferramentas de implantação do site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b68c6-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="b68c6-191">Para o Windows 2000, consulte [atualização de ferramentas de implantação para windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="b68c6-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="b68c6-192">Para Windows XP, consulte [atualização de ferramentas de implantação para Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="b68c6-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="b68c6-193">Executar o **Gerenciador de instalação** (setupmgr.exe).</span><span class="sxs-lookup"><span data-stu-id="b68c6-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="b68c6-194">Siga o assistente do Gerenciador de instalação.</span><span class="sxs-lookup"><span data-stu-id="b68c6-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="b68c6-195">Após a configuração do Sysprep e da criação do espaço de trabalho do MED-V, o Sysprep deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="b68c6-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="b68c6-196">Para executar o Sysprep</span><span class="sxs-lookup"><span data-stu-id="b68c6-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="b68c6-197">Na pasta Sysprep localizada na raiz da unidade do sistema, execute a ferramenta de preparação do sistema (Sysprep.exe).</span><span class="sxs-lookup"><span data-stu-id="b68c6-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="b68c6-198">Na caixa de mensagem de aviso que aparecerá, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="b68c6-199">Na caixa de diálogo **Propriedades do Sysprep** , marque as caixas de seleção **não redefinir período de cortesia para ativação** e **usar a mini-instalação** .</span><span class="sxs-lookup"><span data-stu-id="b68c6-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="b68c6-200">Clique em **lacrar novamente**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="b68c6-201">Se você não estiver satisfeito com as informações listadas na caixa de mensagem de confirmação que aparece, clique em **Cancelar** e altere as opções.</span><span class="sxs-lookup"><span data-stu-id="b68c6-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="b68c6-202">Clique em **OK** para concluir o processo de preparação do sistema.</span><span class="sxs-lookup"><span data-stu-id="b68c6-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="b68c6-203">Desativando o Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b68c6-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="b68c6-204">Após a instalação e a configuração de todos os componentes, feche o Microsoft Virtual PC **e selecione Desativar**.</span><span class="sxs-lookup"><span data-stu-id="b68c6-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="b68c6-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b68c6-205">Related topics</span></span>


<span data-ttu-id="b68c6-206">Criando uma imagem do MED-V [como configurar ações de script](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="b68c6-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









