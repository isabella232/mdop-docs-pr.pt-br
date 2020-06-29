---
title: Como configurar ações de script
description: Como configurar ações de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795987"
---
# <span data-ttu-id="d6438-103">Como configurar ações de script</span><span class="sxs-lookup"><span data-stu-id="d6438-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="d6438-104">O editor de ações de script permite que o administrador crie ações a serem executadas durante a configuração do espaço de trabalho do MED-V, bem como definir a ordem na qual elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="d6438-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="d6438-105">Veja a seguir uma lista de ações que podem ser adicionadas ao script de configuração de domínio:</span><span class="sxs-lookup"><span data-stu-id="d6438-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="d6438-106">**Reinicie o Windows**— reinicie o Windows.</span><span class="sxs-lookup"><span data-stu-id="d6438-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="d6438-107">**Ingressar no domínio**— se estiver ingressando em um domínio, inclua esta ação e configure o nome de usuário, a senha, o nome de domínio totalmente qualificado, o nome de domínio NetBIOS e a unidade organizacional (opcional).</span><span class="sxs-lookup"><span data-stu-id="d6438-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="d6438-108">**Verifique a conectividade**-configure um servidor para se conectar e verifique se o espaço de trabalho do MED-V pode se conectar a um recurso de rede (como o servidor de domínio).</span><span class="sxs-lookup"><span data-stu-id="d6438-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="d6438-109">**Linha de comando**— configure um script no espaço de trabalho do MED-V e insira uma linha de comando que inclua o caminho do script e os argumentos do script.</span><span class="sxs-lookup"><span data-stu-id="d6438-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="d6438-110">**Renomear computador**— renomeie o computador da máquina virtual com base nas configurações definidas.</span><span class="sxs-lookup"><span data-stu-id="d6438-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="d6438-111">**Desabilitar o logon automático**— desabilitar o logon automático do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6438-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="d6438-112">Esta ação deve ser adicionada ao final dos scripts que adicionam o computador ao domínio.</span><span class="sxs-lookup"><span data-stu-id="d6438-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="d6438-113">Como configurar ações de script</span><span class="sxs-lookup"><span data-stu-id="d6438-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="d6438-114">Para configurar as ações de script</span><span class="sxs-lookup"><span data-stu-id="d6438-114">To set up script actions</span></span>**

1.  <span data-ttu-id="d6438-115">Na guia **configuração da VM** , clique em **Editor de script**.</span><span class="sxs-lookup"><span data-stu-id="d6438-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="d6438-116">Na caixa de diálogo **ações de script** , clique em **Adicionar**e, no submenu, clique nas ações desejadas.</span><span class="sxs-lookup"><span data-stu-id="d6438-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="d6438-117">Configure as ações conforme descrito nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6438-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="d6438-118">**Observação** 
     **Renomear computador** está configurado na guia **configurações da VM** . Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="d6438-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="d6438-119">Defina a ordem das ações selecionando uma ação e clicando em **para cima** ou **para baixo**.</span><span class="sxs-lookup"><span data-stu-id="d6438-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="d6438-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6438-120">Click **OK**.</span></span>

**<span data-ttu-id="d6438-121">Observação</span><span class="sxs-lookup"><span data-stu-id="d6438-121">Note</span></span>**  
<span data-ttu-id="d6438-122">Ao executar o script de domínio de junção, para que o script funcione, o usuário conectado na máquina virtual do espaço de trabalho do MED-V deve ter direitos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="d6438-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="d6438-123">Observação</span><span class="sxs-lookup"><span data-stu-id="d6438-123">Note</span></span>**  
<span data-ttu-id="d6438-124">Ao executar o script Disable auto-logon, é recomendável desabilitar a conta de convidado local usada para o logon automático quando a configuração inicial for concluída.</span><span class="sxs-lookup"><span data-stu-id="d6438-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="d6438-125">Ingressar em Propriedades de domínio</span><span class="sxs-lookup"><span data-stu-id="d6438-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6438-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d6438-126">Property</span></span></th>
<th align="left"><span data-ttu-id="d6438-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6438-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-128">Credenciais a serem usadas ao ingressar na VM no domínio</span><span class="sxs-lookup"><span data-stu-id="d6438-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-129">Selecione uma das seguintes credenciais para usar ao ingressar na VM no domínio:</span><span class="sxs-lookup"><span data-stu-id="d6438-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d6438-130">Use as credenciais do MED-V </strong> – as credenciais do usuário final.</span><span class="sxs-lookup"><span data-stu-id="d6438-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="d6438-131">Use as seguintes credenciais </strong> : as credenciais especificadas; Insira um nome de usuário e senha nos campos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d6438-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="d6438-132">Observação</span><span class="sxs-lookup"><span data-stu-id="d6438-132">Note</span></span></strong><br/><p><span data-ttu-id="d6438-133">As credenciais que você insere são visíveis para todos os usuários do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6438-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="d6438-134">Não é recomendável fornecer credenciais de administrador do domínio.</span><span class="sxs-lookup"><span data-stu-id="d6438-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-135">Domínio no qual ingressar</span><span class="sxs-lookup"><span data-stu-id="d6438-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-136">Selecione uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="d6438-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d6438-137">Use o nome de domínio utilizado ao iniciar o espaço de trabalho </strong> — ingresse no domínio inserido pelo usuário final ao fazer logon no cliente MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6438-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="d6438-138">Para definir o mapeamento do NetBIOS para nomes de domínio totalmente qualificados, clique em <strong> tabela de mapeamento de domínio global </strong> .</span><span class="sxs-lookup"><span data-stu-id="d6438-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="d6438-139">Na tabela de mapeamento de domínio global, clique em <strong> Adicionar </strong> , insira um <strong> nome de domínio NetBIOS </strong> e um <strong> nome de domínio totalmente qualificado </strong> e clique em <strong> OK </strong> .</span><span class="sxs-lookup"><span data-stu-id="d6438-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="d6438-140">Use o nome de domínio a seguir </strong> — ingresse no domínio especificado; Insira um nome de domínio e um nome de domínio NetBIOS nos campos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d6438-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-141">Unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="d6438-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-142">Uma unidade organizacional (OU) pode ser especificada para ingressar o computador em uma UO específica.</span><span class="sxs-lookup"><span data-stu-id="d6438-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="d6438-143">O formato deve seguir um nome diferenciado da OU: OU = &lt; unidade organizacional &gt; , &lt; controlador &gt; de domínio (por exemplo, ou = QATest, DC = Il, DC = MED-V, DC = com).</span><span class="sxs-lookup"><span data-stu-id="d6438-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d6438-144">Aviso</span><span class="sxs-lookup"><span data-stu-id="d6438-144">Warning</span></span></strong><br/><p><span data-ttu-id="d6438-145">Só há suporte para uma única OU de nível, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="d6438-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="d6438-146">Verificar Propriedades de conectividade</span><span class="sxs-lookup"><span data-stu-id="d6438-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6438-147">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d6438-147">Property</span></span></th>
<th align="left"><span data-ttu-id="d6438-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6438-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-149">Endereço IP</span><span class="sxs-lookup"><span data-stu-id="d6438-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-150">O endereço IP do servidor para o qual você está verificando a conexão.</span><span class="sxs-lookup"><span data-stu-id="d6438-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-151">Port</span><span class="sxs-lookup"><span data-stu-id="d6438-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-152">A porta do servidor para a qual você está verificando a conexão.</span><span class="sxs-lookup"><span data-stu-id="d6438-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-153">Tempo limite</span><span class="sxs-lookup"><span data-stu-id="d6438-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-154">O número de segundos para esperar por uma resposta antes do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="d6438-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="d6438-155">Propriedades da linha de comando</span><span class="sxs-lookup"><span data-stu-id="d6438-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6438-156">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d6438-156">Property</span></span></th>
<th align="left"><span data-ttu-id="d6438-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6438-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="d6438-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-159">O caminho da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d6438-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-160">Argumentos</span><span class="sxs-lookup"><span data-stu-id="d6438-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-161">Argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d6438-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-162">Aguardar saída</span><span class="sxs-lookup"><span data-stu-id="d6438-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-163">Marque a caixa de seleção para aguardar um retorno antes de continuar com as ações do script.</span><span class="sxs-lookup"><span data-stu-id="d6438-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-164">Falha em erro</span><span class="sxs-lookup"><span data-stu-id="d6438-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-165">Marque esta caixa de seleção se o retorno for algo diferente do valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d6438-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="d6438-166">Digite o valor que indicará o comando como sucesso.</span><span class="sxs-lookup"><span data-stu-id="d6438-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="d6438-167">Padrão: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="d6438-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-168">Executar apenas uma vez</span><span class="sxs-lookup"><span data-stu-id="d6438-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-169">Marque esta caixa de seleção para executar a linha de comando somente uma vez.</span><span class="sxs-lookup"><span data-stu-id="d6438-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="d6438-170">Se o script falhar ou for cancelado, esse comando não será executado novamente.</span><span class="sxs-lookup"><span data-stu-id="d6438-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-171">Esta linha de comando causa uma reinicialização do Windows no espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d6438-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-172">Marque esta caixa de seleção se a linha de comando causar uma reinicialização após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="d6438-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-173">Permitir interação</span><span class="sxs-lookup"><span data-stu-id="d6438-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-174">Marque esta caixa de seleção se o comando exigir a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d6438-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-175">Mensagem de progresso</span><span class="sxs-lookup"><span data-stu-id="d6438-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-176">Mensagem a ser exibida para o usuário enquanto o comando está em execução.</span><span class="sxs-lookup"><span data-stu-id="d6438-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-177">Mensagem de falha</span><span class="sxs-lookup"><span data-stu-id="d6438-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-178">Mensagem a ser exibida para o usuário se o comando falhar.</span><span class="sxs-lookup"><span data-stu-id="d6438-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d6438-179">Durante a configuração da ação da linha de comando, várias variáveis podem ser usadas conforme definido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6438-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6438-180">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6438-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d6438-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d6438-181">Value</span></span></th>
<th align="left"><span data-ttu-id="d6438-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6438-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="d6438-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-184">Um nome de usuário autenticado.</span><span class="sxs-lookup"><span data-stu-id="d6438-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-185">Nome de usuário autenticado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6438-185">MED-V authenticated user name.</span></span> <span data-ttu-id="d6438-186">O nome de usuário e a senha podem ser usados no script de configuração de VM de domínio ingressar.</span><span class="sxs-lookup"><span data-stu-id="d6438-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="d6438-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-188">Uma senha autenticada.</span><span class="sxs-lookup"><span data-stu-id="d6438-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-189">Senha autenticada do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6438-189">MED-V authenticated password.</span></span> <span data-ttu-id="d6438-190">O nome de usuário e a senha podem ser usados no script de configuração de VM de domínio ingressar.</span><span class="sxs-lookup"><span data-stu-id="d6438-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6438-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="d6438-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-192">Domínio configurado.</span><span class="sxs-lookup"><span data-stu-id="d6438-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-193">O domínio configurado na autenticação do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d6438-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="d6438-194">Ele pode ser usado no script de configuração da VM.</span><span class="sxs-lookup"><span data-stu-id="d6438-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6438-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="d6438-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-196">Nome do computador.</span><span class="sxs-lookup"><span data-stu-id="d6438-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6438-197">O nome de computador exclusivo configurado no aplicativo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d6438-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="d6438-198">Ele pode ser usado no script de configuração da VM.</span><span class="sxs-lookup"><span data-stu-id="d6438-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d6438-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6438-199">Related topics</span></span>


[<span data-ttu-id="d6438-200">Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="d6438-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="d6438-201">Como configurar as propriedades de padrão de nomes do computador VM</span><span class="sxs-lookup"><span data-stu-id="d6438-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





