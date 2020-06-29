---
title: Como configurar um usuário ou grupo de domínio
description: Como configurar um usuário ou grupo de domínio
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800024"
---
# <span data-ttu-id="5f7c1-103">Como configurar um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="5f7c1-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="5f7c1-104">As configurações de implantação permitem controlar quais usuários ou grupos podem acessar o espaço de trabalho do MED-V, bem como quanto tempo o espaço de trabalho do MED-V pode ser utilizado e se ele pode ser usado offline.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="5f7c1-105">Você também pode configurar regras adicionais para controlar o acesso entre o espaço de trabalho do MED-V e o host.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="5f7c1-106">Todas as permissões do espaço de trabalho do MED-V são configuradas no módulo de **política** , na guia **implantação** .</span><span class="sxs-lookup"><span data-stu-id="5f7c1-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="5f7c1-107">Para permitir que os usuários utilizem o espaço de trabalho do MED-V, você deve primeiro adicionar usuários ou grupos do domínio às permissões do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="5f7c1-108">Em seguida, você pode definir permissões para cada usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="5f7c1-109">Como adicionar um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="5f7c1-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="5f7c1-110">Para adicionar um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="5f7c1-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="5f7c1-111">Na janela **usuários/grupos** , clique em **Adicionar.**</span><span class="sxs-lookup"><span data-stu-id="5f7c1-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="5f7c1-112">Na caixa de diálogo **Inserir nomes de usuário ou grupo** , selecione usuários de domínio ou grupos seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="5f7c1-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="5f7c1-113">No campo **Inserir nomes de usuário ou grupo** , digite um usuário ou grupo que exista no domínio ou como um usuário ou grupo local no computador.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="5f7c1-114">Em seguida, clique em **verificar nomes** para resolvê-lo para o nome completo existente.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="5f7c1-115">Clique em **Localizar** para abrir a caixa de diálogo **Selecionar usuários ou grupos** padrão.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="5f7c1-116">Em seguida, selecione usuários ou grupos do domínio.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="5f7c1-117">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-117">Click **OK**.</span></span>

    <span data-ttu-id="5f7c1-118">Os usuários do domínio ou grupos são adicionados.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="5f7c1-119">Observação</span><span class="sxs-lookup"><span data-stu-id="5f7c1-119">Note</span></span>**  
    <span data-ttu-id="5f7c1-120">Os usuários de domínios confiáveis devem ser adicionados manualmente.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="5f7c1-121">Como remover um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="5f7c1-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="5f7c1-122">Para remover um usuário ou grupo de domínio</span><span class="sxs-lookup"><span data-stu-id="5f7c1-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="5f7c1-123">Na janela **usuários/grupos** , selecione um usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="5f7c1-124">Clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-124">Click **Remove**.</span></span>

    <span data-ttu-id="5f7c1-125">O usuário ou grupo é excluído.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-125">The user or group is deleted.</span></span>

## <span data-ttu-id="5f7c1-126">Como definir permissões para um usuário ou um grupo</span><span class="sxs-lookup"><span data-stu-id="5f7c1-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="5f7c1-127">Para definir permissões para um usuário ou um grupo</span><span class="sxs-lookup"><span data-stu-id="5f7c1-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="5f7c1-128">Clique no usuário ou grupo para o qual você está configurando as permissões.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="5f7c1-129">Configure as propriedades do espaço de trabalho do MED-V conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="5f7c1-130">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="5f7c1-131">Propriedades de implantação do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5f7c1-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="5f7c1-132">Descrição da propriedade *geral*</span><span class="sxs-lookup"><span data-stu-id="5f7c1-132">Property Description *General*</span></span>

<span data-ttu-id="5f7c1-133">Habilitar espaço de trabalho para &lt; usuário ou grupo&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7c1-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="5f7c1-134">Marque esta caixa de seleção para habilitar o espaço de trabalho do MED-V para este usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="5f7c1-135">O espaço de trabalho vence nesta data</span><span class="sxs-lookup"><span data-stu-id="5f7c1-135">Workspace expires on this date</span></span>

<span data-ttu-id="5f7c1-136">Marque esta caixa de seleção para atribuir uma data de expiração para as permissões definidas para este usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="5f7c1-137">Quando selecionada, a caixa data é habilitada.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="5f7c1-138">Defina a data e as permissões vencerão no final da data especificada.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="5f7c1-139">O trabalho offline está restrito a</span><span class="sxs-lookup"><span data-stu-id="5f7c1-139">Offline work is restricted to</span></span>

<span data-ttu-id="5f7c1-140">Marque esta caixa de seleção para atribuir um período de tempo no qual a política deve ser atualizada para este usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="5f7c1-141">Quando selecionada, a caixa período de tempo é habilitada.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="5f7c1-142">Defina o número de dias ou horas e, no final do período de tempo especificado, o usuário ou grupo não poderá se conectar se a política não for atualizada.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="5f7c1-143">Opções de exclusão do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5f7c1-143">Workspace deletion options</span></span>

<span data-ttu-id="5f7c1-144">Clique para definir as opções de exclusão do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="5f7c1-145">Para obter mais informações, consulte [como definir as opções de exclusão do espaço de trabalho do MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="5f7c1-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="5f7c1-146">Transferência de dados</span><span class="sxs-lookup"><span data-stu-id="5f7c1-146">Data Transfer</span></span>*

<span data-ttu-id="5f7c1-147">Área de transferência de suporte entre host e espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5f7c1-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="5f7c1-148">Marque esta caixa de seleção para habilitar a cópia e a colagem entre o host e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="5f7c1-149">Suporte para transferência de arquivos entre o host e o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5f7c1-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="5f7c1-150">Marque esta caixa de seleção para habilitar a transferência de arquivos entre o host e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="5f7c1-151">Selecione uma das seguintes opções na caixa **transferência de arquivo** :</span><span class="sxs-lookup"><span data-stu-id="5f7c1-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="5f7c1-152">**Ambos**— permitem transferir arquivos entre o host e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="5f7c1-153">**Host para espaço de trabalho**— habilite a transferência de arquivos do host para o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="5f7c1-154">**Espaço de trabalho para o host**— habilite a transferência de arquivos do espaço de trabalho do MED-V para o host.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="5f7c1-155">Observação</span><span class="sxs-lookup"><span data-stu-id="5f7c1-155">Note</span></span>**  
<span data-ttu-id="5f7c1-156">Se um usuário sem permissões tentar transferir arquivos, será exibida uma janela solicitando que ele Insira as credenciais de um usuário com permissões para executar a transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="5f7c1-157">Importante</span><span class="sxs-lookup"><span data-stu-id="5f7c1-157">Important</span></span>**  
<span data-ttu-id="5f7c1-158">Para dar suporte à transferência de arquivos no Windows XP SP3, você deve desativar a sincronização de arquivos offline editando o registro da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5f7c1-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="5f7c1-159">Avançado</span><span class="sxs-lookup"><span data-stu-id="5f7c1-159">Advanced</span></span>

<span data-ttu-id="5f7c1-160">Clique para definir as opções avançadas de transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="5f7c1-161">Para obter mais informações, consulte [como definir opções avançadas de transferência de arquivo](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="5f7c1-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="5f7c1-162">Controle de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f7c1-162">Device Control</span></span>*

<span data-ttu-id="5f7c1-163">Habilitar a impressão em impressoras conectadas ao host</span><span class="sxs-lookup"><span data-stu-id="5f7c1-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="5f7c1-164">Marque esta caixa de seleção para permitir que os usuários imprimam a partir do espaço de trabalho do MED-V usando a impressora host.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="5f7c1-165">Observação</span><span class="sxs-lookup"><span data-stu-id="5f7c1-165">Note</span></span>**  
<span data-ttu-id="5f7c1-166">A impressão é realizada pelas impressoras definidas no host.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="5f7c1-167">Habilitar o acesso ao CD/DVD</span><span class="sxs-lookup"><span data-stu-id="5f7c1-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="5f7c1-168">Marque esta caixa de seleção para permitir o acesso a uma unidade de CD ou DVD deste espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="5f7c1-169">Várias associações</span><span class="sxs-lookup"><span data-stu-id="5f7c1-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="5f7c1-170">Se o usuário fizer parte de um grupo e as permissões forem aplicadas ao usuário e ao grupo do qual elas fazem parte, todas as permissões serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="5f7c1-171">Se o usuário for membro de dois grupos diferentes, as permissões menos restritivas serão aplicadas.</span><span class="sxs-lookup"><span data-stu-id="5f7c1-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="5f7c1-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f7c1-172">Related topics</span></span>


[<span data-ttu-id="5f7c1-173">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="5f7c1-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="5f7c1-174">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="5f7c1-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="5f7c1-175">Como definir opções de exclusão de espaços de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="5f7c1-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="5f7c1-176">Como definir opções avançadas de transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="5f7c1-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









