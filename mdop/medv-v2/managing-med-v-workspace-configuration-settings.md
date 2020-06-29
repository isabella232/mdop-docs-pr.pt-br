---
title: Gerenciamento de configurações do espaço de trabalho da MED-V
description: Gerenciamento de configurações do espaço de trabalho da MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799816"
---
# <span data-ttu-id="45ea1-103">Gerenciamento de configurações do espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="45ea1-103">Managing MED-V Workspace Configuration Settings</span></span>


<span data-ttu-id="45ea1-104">A virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 armazena suas configurações de configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 stores its configuration settings in the registry.</span></span> <span data-ttu-id="45ea1-105">As informações incluídas aqui sobre o registro podem ajudá-lo a gerenciar melhor seus serviços do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-105">The information we include here about the registry may help you better manage your MED-V services.</span></span>

<span data-ttu-id="45ea1-106">O MED-V usa o seguinte caminho de pesquisa ao procurar os valores de configurações resultantes:</span><span class="sxs-lookup"><span data-stu-id="45ea1-106">MED-V uses the following search path when looking for the resultant settings values:</span></span>

<span data-ttu-id="45ea1-107">O MED-V procura primeiro na política do computador.</span><span class="sxs-lookup"><span data-stu-id="45ea1-107">MED-V first looks in the machine policy.</span></span>

<span data-ttu-id="45ea1-108">Se o valor não for encontrado, o MED-V pesquisará na política de usuário.</span><span class="sxs-lookup"><span data-stu-id="45ea1-108">If the value is not found, MED-V looks in the user policy.</span></span>

<span data-ttu-id="45ea1-109">Se o valor não for encontrado, o MED-V procura na seção HKEY \ _LOCAL \ _MACHINE \\System.</span><span class="sxs-lookup"><span data-stu-id="45ea1-109">If the value is not found, MED-V looks in the HKEY\_LOCAL\_MACHINE\\System hive.</span></span>

<span data-ttu-id="45ea1-110">Se o valor não for encontrado, o MED-V pesquisará no hive do registro do usuário HKEY \ _CURRENT.</span><span class="sxs-lookup"><span data-stu-id="45ea1-110">If the value is not found, MED-V looks in the HKEY\_CURRENT USER registry hive.</span></span>

<span data-ttu-id="45ea1-111">Se o valor ainda não for encontrado, o MED-V usará o padrão.</span><span class="sxs-lookup"><span data-stu-id="45ea1-111">If the value is still not found, MED-V uses the default.</span></span>

<span data-ttu-id="45ea1-112">Uma prática recomendada geral é definir o valor na seção HKEY \ _LOCAL \ _MACHINE \\System ou na política do computador.</span><span class="sxs-lookup"><span data-stu-id="45ea1-112">A general best practice is to set the value in the HKEY\_LOCAL\_MACHINE\\System hive or in the machine policy.</span></span> <span data-ttu-id="45ea1-113">Mas se você quiser que o usuário final seja capaz de definir uma determinada configuração, você deve deixá-la.</span><span class="sxs-lookup"><span data-stu-id="45ea1-113">But if you want the end user to be able to configure a particular setting, then you should leave it out.</span></span>

**<span data-ttu-id="45ea1-114">Observação</span><span class="sxs-lookup"><span data-stu-id="45ea1-114">Note</span></span>**  
<span data-ttu-id="45ea1-115">Antes de implantar seus espaços de trabalho do MED-V, você pode usar um editor de script para alterar o script do Windows PowerShell (arquivo. ps1) criado pelo pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-115">Before you deploy your MED-V workspaces, you can use a script editor to change the Windows PowerShell script (.ps1 file) that the MED-V workspace packager created.</span></span> <span data-ttu-id="45ea1-116">Para obter mais informações, consulte [definindo as configurações avançadas usando o Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="45ea1-116">For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).</span></span>

<span data-ttu-id="45ea1-117">Depois de implantar seus espaços de trabalho do MED-V, você pode alterar determinadas configurações de configuração do MED-V editando as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-117">After you have deployed your MED-V workspaces, you can change certain MED-V configuration settings by editing the registry entries.</span></span>



<span data-ttu-id="45ea1-118">Esta seção lista todas as chaves de registro do MED-V configuráveis e explica seus usos.</span><span class="sxs-lookup"><span data-stu-id="45ea1-118">This section lists all the configurable MED-V registry keys and explains their uses.</span></span>

## <span data-ttu-id="45ea1-119">Chave de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="45ea1-119">Diagnostics Key</span></span>


<span data-ttu-id="45ea1-120">A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="45ea1-120">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45ea1-121">Nome</span><span class="sxs-lookup"><span data-stu-id="45ea1-121">Name</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="45ea1-122">Type</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-123">Dados/padrão</span><span class="sxs-lookup"><span data-stu-id="45ea1-123">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ea1-124">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-125">EventLogLevel</span><span class="sxs-lookup"><span data-stu-id="45ea1-125">EventLogLevel</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-126">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-127">Padrão = 3</span><span class="sxs-lookup"><span data-stu-id="45ea1-127">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-128">O tipo de informação que está registrada no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="45ea1-128">The type of information that is logged in the event log.</span></span> <span data-ttu-id="45ea1-129">Os níveis incluem o seguinte: 0 (nenhum), 1 (erro), 2 (aviso), 3 (informações), 4 (Depurar).</span><span class="sxs-lookup"><span data-stu-id="45ea1-129">Levels include the following: 0 (None), 1 (Error), 2 (Warning), 3 (Information), 4 (Debug).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="45ea1-130">Chave FTS</span><span class="sxs-lookup"><span data-stu-id="45ea1-130">Fts Key</span></span>


<span data-ttu-id="45ea1-131">A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.</span><span class="sxs-lookup"><span data-stu-id="45ea1-131">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\Fts key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45ea1-132">Nome</span><span class="sxs-lookup"><span data-stu-id="45ea1-132">Name</span></span></th>
<th align="left"><span data-ttu-id="45ea1-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="45ea1-133">Type</span></span></th>
<th align="left"><span data-ttu-id="45ea1-134">Dados/padrão</span><span class="sxs-lookup"><span data-stu-id="45ea1-134">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="45ea1-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ea1-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-136">AddUserToAdminGroupEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-136">AddUserToAdminGroupEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-137">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-137">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-138">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-138">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-139">Configura se a primeira vez que o programa de instalação adiciona automaticamente o usuário final ao grupo administrador&#39;s.</span><span class="sxs-lookup"><span data-stu-id="45ea1-139">Configures whether first time setup automatically adds the end user to the administrator&#39;s group.</span></span> <span data-ttu-id="45ea1-140">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-140">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-141">0 = falso: o programa de instalação da primeira vez não adiciona automaticamente o usuário final ao grupo administrador&#39;s.</span><span class="sxs-lookup"><span data-stu-id="45ea1-141">0 = false: First time setup does not automatically add the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-142">1 = verdadeiro: o programa de instalação da primeira vez adiciona automaticamente o usuário final ao grupo administrador&#39;s.</span><span class="sxs-lookup"><span data-stu-id="45ea1-142">1 = true: First time setup automatically adds the end user to the administrator&#39;s group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-143">ComputerNameMask</span><span class="sxs-lookup"><span data-stu-id="45ea1-143">ComputerNameMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-144">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-144">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-145">MEDV\*</span><span class="sxs-lookup"><span data-stu-id="45ea1-145">MEDV\*</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-146">A máscara de nome do computador que é usada para criar o nome do computador&#39;s da máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-146">The computer name mask that is used to create the guest virtual machine&#39;s computer name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-147">A máscara pode conter uma marca% username% para inserir o nome de usuário como parte do nome do computador.</span><span class="sxs-lookup"><span data-stu-id="45ea1-147">The mask can contain a %username% tag to insert the username as part of the computer name.</span></span> <span data-ttu-id="45ea1-148">Da mesma forma, a marca% hostname% insere o nome do computador host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-148">Likewise, the %hostname% tag inserts the name of the host computer.</span></span></p>
<p><span data-ttu-id="45ea1-149">Cada &quot; # &quot; caractere na máscara é substituído por um dígito aleatório.</span><span class="sxs-lookup"><span data-stu-id="45ea1-149">Every &quot;#&quot; character in the mask is replaced by a random digit.</span></span> <span data-ttu-id="45ea1-150">Um caractere de asterisco (\*) no final da máscara é substituído por caracteres alfanuméricos aleatórios.</span><span class="sxs-lookup"><span data-stu-id="45ea1-150">An asterisk (\*) character at the end of the mask is replaced by random alphanumeric characters.</span></span></p>
<p><span data-ttu-id="45ea1-151">Um número específico de caracteres de% hostname% e% username% pode ser capturado usando colchetes.</span><span class="sxs-lookup"><span data-stu-id="45ea1-151">A specific number of characters from %hostname% and %username% can be captured by using square brackets.</span></span> <span data-ttu-id="45ea1-152">Por exemplo, &quot; % username% [3] &quot; usaria os três primeiros caracteres do nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="45ea1-152">For example, &quot;%username%[3]&quot; would use the first three characters of the username.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-153">DeleteVMStateTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-153">DeleteVMStateTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-154">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-154">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-155">Padrão = 90</span><span class="sxs-lookup"><span data-stu-id="45ea1-155">Default=90</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-156">O valor de tempo limite, em segundos, quando a configuração tenta excluir a máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="45ea1-156">The time-out value, in seconds, when first time setup tries to delete the virtual machine.</span></span> <span data-ttu-id="45ea1-157">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-157">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-158">DetachVfdTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-158">DetachVfdTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-160">Padrão = 120</span><span class="sxs-lookup"><span data-stu-id="45ea1-160">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-161">O valor de tempo limite, em segundos, quando a configuração da primeira vez tenta desanexar o disquete virtual da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="45ea1-161">The time-out value, in seconds, when first time setup tries to detach the virtual floppy disk from the virtual machine.</span></span> <span data-ttu-id="45ea1-162">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-162">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-163">DialogUrl</span><span class="sxs-lookup"><span data-stu-id="45ea1-163">DialogUrl</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-164">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-164">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-165">URL personalizável que se vincula à página da Web interna e é exibida pela primeira vez que você configurar as mensagens de diálogo.</span><span class="sxs-lookup"><span data-stu-id="45ea1-165">Customizable URL that links to internal webpage and is displayed by first time setup dialog messages.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-166">ExplorerTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-166">ExplorerTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-167">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-167">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-168">Padrão = 900</span><span class="sxs-lookup"><span data-stu-id="45ea1-168">Default=900</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-169">O valor de tempo limite, em segundos, que a configuração de primeira vez aguarda para o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="45ea1-169">The time-out value, in seconds, that first time setup waits for Windows Explorer.</span></span> <span data-ttu-id="45ea1-170">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-170">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-171">FailureDialogMsg</span><span class="sxs-lookup"><span data-stu-id="45ea1-171">FailureDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-172">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-172">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-173">Mensagem encontrada no arquivo de recurso</span><span class="sxs-lookup"><span data-stu-id="45ea1-173">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-174">Mensagem personalizável que é exibida para o usuário final quando a configuração não pode ser concluída pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="45ea1-174">Customizable message that is displayed to the end user when first time setup cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-175">GiveUserGroupRightsMaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="45ea1-175">GiveUserGroupRightsMaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-176">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-176">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-177">Padrão = 3</span><span class="sxs-lookup"><span data-stu-id="45ea1-177">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-178">O número máximo de vezes que o MED-V tenta conceder a um usuário final direitos de grupo.</span><span class="sxs-lookup"><span data-stu-id="45ea1-178">The maximum number of times that MED-V tries to give an end user group rights.</span></span> <span data-ttu-id="45ea1-179">Exceder o valor de repetição especificado sem ser capaz de conceder com êxito a um grupo de usuários finais os direitos provavelmente causam uma falha de preparação da máquina virtual que, em seguida, está sujeito ao valor MaxRetryCount.</span><span class="sxs-lookup"><span data-stu-id="45ea1-179">Exceeding the specified retry value without being able to successfully give an end user group rights most likely causes a virtual machine preparation failure that is then subject to the MaxRetryCount value.</span></span> <span data-ttu-id="45ea1-180">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-180">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-181">GiveUserGroupRightsTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-181">GiveUserGroupRightsTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-182">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-182">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-183">Padrão = 300</span><span class="sxs-lookup"><span data-stu-id="45ea1-183">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-184">O valor de tempo limite, em segundos, ao conceder direitos a um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="45ea1-184">The time-out value, in seconds, when giving a user group rights.</span></span> <span data-ttu-id="45ea1-185">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-185">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-186">LogFilePaths</span><span class="sxs-lookup"><span data-stu-id="45ea1-186">LogFilePaths</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-187">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-187">MULTI_SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-188">Uma lista dos caminhos do arquivo de log que o MED-V coleta durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="45ea1-188">A list of the log file paths that MED-V collects during first time setup.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-189">MaxPostponeTime</span><span class="sxs-lookup"><span data-stu-id="45ea1-189">MaxPostponeTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-190">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-190">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-191">Padrão = 120</span><span class="sxs-lookup"><span data-stu-id="45ea1-191">Default=120</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-192">O número máximo de horas em que a configuração da primeira vez pode ser adiada pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="45ea1-192">The maximum number of hours that first time setup can be postponed by the end user.</span></span> <span data-ttu-id="45ea1-193">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-193">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-194">MaxRetryCount</span><span class="sxs-lookup"><span data-stu-id="45ea1-194">MaxRetryCount</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-195">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-195">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-196">Padrão = 3</span><span class="sxs-lookup"><span data-stu-id="45ea1-196">Default=3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-197">O número máximo de vezes que o MED-V tenta preparar uma máquina virtual se cada tentativa terminar em uma falha diferente de um erro de software.</span><span class="sxs-lookup"><span data-stu-id="45ea1-197">The maximum number of times that MED-V tries to prepare a virtual machine if each attempt ends in a failure other than a software error.</span></span> <span data-ttu-id="45ea1-198">Quando a preparação da máquina virtual falha e o número da primeira tentativa de configuração é excedido, o MED-V informa o usuário final sobre a falha e não dá a opção de tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="45ea1-198">When virtual machine preparation fails and the number of first time setup retries is exceeded, then MED-V informs the end user about the failure and does not give the option to retry.</span></span> <span data-ttu-id="45ea1-199">A contagem é reativada sempre que o MED-V é iniciado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-199">The count is re-set every time that MED-V is started.</span></span> <span data-ttu-id="45ea1-200">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-200">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-201">Modo</span><span class="sxs-lookup"><span data-stu-id="45ea1-201">Mode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-202">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-202">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-203">Padrão = autônomo</span><span class="sxs-lookup"><span data-stu-id="45ea1-203">Default=Unattended</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-204">Configura a primeira vez que a configuração interage com o usuário.</span><span class="sxs-lookup"><span data-stu-id="45ea1-204">Configures how first time setup interacts with the user.</span></span> <span data-ttu-id="45ea1-205">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="45ea1-205">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-206">Compromissos.</span><span class="sxs-lookup"><span data-stu-id="45ea1-206">Attended.</span></span></strong> <span data-ttu-id="45ea1-207">O usuário final deve inserir informações durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="45ea1-207">The end user must enter information during first time setup.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="45ea1-208">Observação</span><span class="sxs-lookup"><span data-stu-id="45ea1-208">Note</span></span></strong><br/><p><span data-ttu-id="45ea1-209">Se você criou o arquivo Sysprep. inf para que a mini-instalação exija que a entrada do usuário seja concluída, você deve <strong> selecionar </strong> modo assistido ou problemas podem ocorrer durante a configuração inicial.</span><span class="sxs-lookup"><span data-stu-id="45ea1-209">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, then you must select <strong>Attended</strong> mode or problems might occur during first time setup.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-210">Autônomo </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-210">Unattended</strong>.</span></span> <span data-ttu-id="45ea1-211">A máquina virtual não é mostrada para o usuário final durante a primeira instalação, mas o usuário final é solicitado antes do início da configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="45ea1-211">The virtual machine is not shown to the end user during first time setup, but the end user is prompted before first time setup starts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-212">Silencioso </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-212">Silent</strong>.</span></span> <span data-ttu-id="45ea1-213">A máquina virtual não é mostrada para o usuário final durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="45ea1-213">The virtual machine is not shown to the end user at all during first time setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-214">NonInteractiveRetryTimeoutInc</span><span class="sxs-lookup"><span data-stu-id="45ea1-214">NonInteractiveRetryTimeoutInc</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-215">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-215">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-216">Padrão = 15</span><span class="sxs-lookup"><span data-stu-id="45ea1-216">Default=15</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-217">O valor de tempo limite, em minutos, que a configuração inicial deve ser completada na primeira vez que a instalação é feita ao tentar novamente a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ea1-217">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode when re-attempting setup.</span></span> <span data-ttu-id="45ea1-218">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-218">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-219">NonInteractiveTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-219">NonInteractiveTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-220">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-220">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-221">Padrão = 45</span><span class="sxs-lookup"><span data-stu-id="45ea1-221">Default=45</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-222">O valor de tempo limite, em minutos, que a configuração inicial deve ser completada na primeira vez em que você configurar o modo interativo.</span><span class="sxs-lookup"><span data-stu-id="45ea1-222">The time-out value, in minutes, that first time setup must be completed in first time setup interactive mode.</span></span> <span data-ttu-id="45ea1-223">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-223">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-224">PostponeUtcDateTimeLimit</span><span class="sxs-lookup"><span data-stu-id="45ea1-224">PostponeUtcDateTimeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-225">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-225">SZ</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-226">A data e a hora, no formato DateTime UTC, que pode ser adiada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="45ea1-226">The date and time, in UTC DateTime format, that first time setup can be postponed.</span></span> <span data-ttu-id="45ea1-227">Insira no formato &quot; aaaa-mm-dd hh: mm &quot; com horas especificadas usando o padrão de relógio de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="45ea1-227">Enter in the format &quot;yyyy-MM-dd hh:mm&quot; with hours specified by using the 24-hour clock standard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-228">RetryDialogMsg</span><span class="sxs-lookup"><span data-stu-id="45ea1-228">RetryDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-229">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-229">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-230">Mensagem encontrada no arquivo de recurso</span><span class="sxs-lookup"><span data-stu-id="45ea1-230">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-231">Mensagem personalizável que é exibida para o usuário final quando a configuração da primeira vez precisa ser feita novamente.</span><span class="sxs-lookup"><span data-stu-id="45ea1-231">Customizable message that is displayed to the end user when first time setup must re-attempt setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-232">SetComputerNameEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-232">SetComputerNameEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-233">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-233">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-234">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-234">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-235">Configura se a entrada ComputerName na seção [UserData] do arquivo Sysprep. inf no convidado deve ser atualizada de acordo com a ComputerNameMask especificada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-235">Configures whether the ComputerName entry under the [UserData] section of the Sysprep.inf file in the guest should be updated according to the specified ComputerNameMask.</span></span>   <span data-ttu-id="45ea1-236">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-236">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-237">0 = falso: a entrada ComputerName no arquivo Sysprep. inf não é atualizada de acordo com o ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="45ea1-237">0 = false: The ComputerName entry in the Sysprep.inf file is not updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-238">1 = verdadeiro: a entrada ComputerName no arquivo Sysprep. inf é atualizada de acordo com o ComputerNameMask.</span><span class="sxs-lookup"><span data-stu-id="45ea1-238">1 = true: The ComputerName entry in the Sysprep.inf file is updated according to the ComputerNameMask.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-239">SetJoinDomainEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-239">SetJoinDomainEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-240">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-240">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-241">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-241">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-242">Configura se a configuração JoinDomain na seção [identificação] do arquivo Sysprep. inf no convidado deve ser atualizada para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-242">Configures whether the JoinDomain setting under the [Identification] section of the Sysprep.inf file in the guest should be updated to match the settings on the host.</span></span>  <span data-ttu-id="45ea1-243">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-243">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-244">0 = falso: a configuração JoinDomain no arquivo Sysprep. inf não é atualizada para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-244">0 = false: The JoinDomain setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-245">1 = verdadeiro: a configuração JoinDomain no arquivo Sysprep. inf é atualizada para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-245">1 = true: The JoinDomain setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-246">SetMachineObjectOUEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-246">SetMachineObjectOUEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-247">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-247">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-248">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-248">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-249">Configura se a configuração MachineObjectOU na seção [identificação] do arquivo Sysprep. inf no convidado é atualizada para corresponder ao host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-249">Configures whether the MachineObjectOU setting under the [Identification] section of the Sysprep.inf file in the guest is updated to match the host.</span></span>  <span data-ttu-id="45ea1-250">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-250">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-251">0 = falso: a configuração MachineObjectOU no arquivo Sysprep. inf não é atualizada para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-251">0 = false: The MachineObjectOU setting in the Sysprep.inf file is not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-252">1 = verdadeiro: a configuração MachineObjectOU no arquivo Sysprep. inf é atualizada para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-252">1 = true: The MachineObjectOU setting in the Sysprep.inf file is updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-253">SetRegionalSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-253">SetRegionalSettingsEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-254">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-254">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-255">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-255">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-256">Configura se as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado são atualizadas para corresponderem ao host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-256">Configures whether the settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span>  <span data-ttu-id="45ea1-257">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-257">0 = false; 1 = true.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="45ea1-258">Observação</span><span class="sxs-lookup"><span data-stu-id="45ea1-258">Note</span></span></strong><br/><p><span data-ttu-id="45ea1-259">Por padrão, a configuração de fuso horário no convidado sempre é sincronizada com a configuração de fuso horário no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-259">By default, the setting for TimeZone in the guest is always synchronized with the TimeZone setting in the host.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-260">0 = falso: as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado não são atualizadas para corresponderem ao host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-260">0 = false: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are not updated to match the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-261">1 = verdadeiro: as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado são atualizadas para corresponderem ao host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-261">1 = true: The settings under the [RegionalSettings] section of the Sysprep.inf file in the guest are updated to match the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-262">SetUserDataEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-262">SetUserDataEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-263">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-263">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-264">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-264">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-265">Configura se as configurações FullName e OrgName na seção [UserData] do arquivo Sysprep. inf no convidado são atualizadas para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-265">Configures whether the FullName and the OrgName settings under the [UserData] section of the Sysprep.inf file in the guest are updated to match the settings on the host.</span></span>  <span data-ttu-id="45ea1-266">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-266">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-267">0 = falso: as configurações FullName e OrgName no arquivo Sysprep. inf não são atualizadas para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-267">0 = false: The FullName and OrgName settings in the Sysprep.inf file are not updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-268">1 = verdadeiro: as configurações FullName e OrgName no arquivo Sysprep. inf são atualizadas para corresponder às configurações no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-268">1 = true: The FullName and OrgName settings in the Sysprep.inf file are updated to match the settings on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-269">StartDialogMsg</span><span class="sxs-lookup"><span data-stu-id="45ea1-269">StartDialogMsg</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-270">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-270">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-271">Mensagem encontrada no arquivo de recurso</span><span class="sxs-lookup"><span data-stu-id="45ea1-271">Message is found in resource file</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-272">Mensagem personalizável que é exibida para o usuário final quando a configuração está pronta para começar.</span><span class="sxs-lookup"><span data-stu-id="45ea1-272">Customizable message that is displayed to the end user when first time setup is ready to start.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-273">TaskCancelTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-273">TaskCancelTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-274">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-275">Padrão = 30</span><span class="sxs-lookup"><span data-stu-id="45ea1-275">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-276">O valor de tempo limite, em segundos, que a configuração inicial aguarda pela primeira vez para obter uma resposta da máquina virtual para uma operação de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="45ea1-276">The time-out value, in seconds, that first time setup waits for a response from the virtual machine for a Cancel operation.</span></span> <span data-ttu-id="45ea1-277">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-277">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-278">TaskVMTurnOffTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-278">TaskVMTurnOffTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-279">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-279">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-280">Padrão = 60</span><span class="sxs-lookup"><span data-stu-id="45ea1-280">Default=60</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-281">O valor de tempo limite, em segundos, que a configuração da primeira vez aguarda para que a máquina virtual seja encerrada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-281">The time-out value, in seconds, that first time setup waits for the virtual machine to shut down.</span></span> <span data-ttu-id="45ea1-282">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-282">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-283">UpgradeTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-283">UpgradeTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-284">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-285">Padrão = 600</span><span class="sxs-lookup"><span data-stu-id="45ea1-285">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-286">O tempo, em segundos, antes que uma tentativa de atualização do software do agente de convidado do MED-V expire. Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-286">The time, in seconds, before an attempted upgrade of the MED-V Guest Agent software times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="45ea1-287">Chave userexperience</span><span class="sxs-lookup"><span data-stu-id="45ea1-287">UserExperience Key</span></span>


<span data-ttu-id="45ea1-288">A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience e a tecla HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.</span><span class="sxs-lookup"><span data-stu-id="45ea1-288">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\UserExperience key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45ea1-289">Nome</span><span class="sxs-lookup"><span data-stu-id="45ea1-289">Name</span></span></th>
<th align="left"><span data-ttu-id="45ea1-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="45ea1-290">Type</span></span></th>
<th align="left"><span data-ttu-id="45ea1-291">Dados/padrão</span><span class="sxs-lookup"><span data-stu-id="45ea1-291">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="45ea1-292">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ea1-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-293">AppPublishingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-293">AppPublishingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-294">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-295">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-295">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-296">Configura se a publicação do aplicativo do convidado para o host está habilitada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-296">Configures whether application publication from the guest to the host is enabled.</span></span>  <span data-ttu-id="45ea1-297">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-297">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-298">0 = falso: desabilita a publicação de aplicativos do convidado para o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-298">0 = false: Disables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-299">1 = verdadeiro: habilita a publicação de aplicativos do convidado para o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-299">1 = true: Enables application publishing from the guest to the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-300">AudioSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-300">AudioSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-301">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-302">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-302">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-303">Configura se o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-303">Configures whether the sharing of the audio I/O device between the guest and the host is enabled.</span></span>  <span data-ttu-id="45ea1-304">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-304">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-305">0 = falso: desabilita o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-305">0 = false: Disables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-306">1 = verdadeiro: habilita o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-306">1 = true: Enables the sharing of the audio I/O device between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-307">ClipboardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-307">ClipboardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-308">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-308">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-309">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-309">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-310">Configura se o compartilhamento da área de transferência entre o convidado e o host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-310">Configures whether the sharing of the Clipboard between the guest and the host is enabled.</span></span>  <span data-ttu-id="45ea1-311">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-311">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-312">0 = falso: desabilita o compartilhamento da área de transferência entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-312">0 = false: Disables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-313">1 = verdadeiro: permite o compartilhamento da área de transferência entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-313">1 = true: Enables the sharing of the Clipboard between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-314">DialogTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-314">DialogTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-315">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-316">Padrão = 300</span><span class="sxs-lookup"><span data-stu-id="45ea1-316">Default=300</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-317">O tempo, em segundos, antes da primeira vez em que a configuração iniciar a caixa de diálogo Iniciar. Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-317">The time, in seconds, before the first time setup Start Dialog times out. Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-318">HideVmTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-318">HideVmTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-319">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-320">Padrão = 30</span><span class="sxs-lookup"><span data-stu-id="45ea1-320">Default=30</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-321">O valor de tempo limite, em minutos, que a janela da máquina virtual de tela inteira está oculta do usuário final durante uma tentativa de logon longa.</span><span class="sxs-lookup"><span data-stu-id="45ea1-321">The time-out value, in minutes, that the full-screen virtual machine window is hidden from the end user during a long logon attempt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-322">LogonStartEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-322">LogonStartEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-323">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-323">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-324">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-324">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-325">Configura se o convidado deve ser iniciado quando o usuário final se conecta à área de trabalho ou quando o primeiro aplicativo convidado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-325">Configures whether the guest should be started when the end user logs on to the desktop or when the first guest application is started.</span></span>  <span data-ttu-id="45ea1-326">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-326">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-327">0 = falso: o convidado é iniciado quando o primeiro aplicativo convidado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-327">0 = false: The guest is started when the first guest application is started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-328">1 = verdadeiro: o convidado é iniciado quando o usuário final faz logon na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="45ea1-328">1 = true: The guest is started when the end user logs on to the desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-329">PrinterSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-329">PrinterSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-330">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-330">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-331">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-331">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-332">Configura se o compartilhamento de impressoras entre o convidado e o host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-332">Configures whether the sharing of printers between the guest and the host is enabled.</span></span>  <span data-ttu-id="45ea1-333">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-333">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-334">0 = falso: desabilita o compartilhamento de impressoras entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-334">0 = false: Disables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-335">1 = verdadeiro: habilita o compartilhamento de impressoras entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-335">1 = true: Enables the sharing of printers between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-336">RebootAbsoluteDelayTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-336">RebootAbsoluteDelayTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-337">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-338">Padrão = 1440</span><span class="sxs-lookup"><span data-stu-id="45ea1-338">Default=1440</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-339">O valor de tempo limite, em minutos, que a configuração inicial aguarda durante uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="45ea1-339">The time-out value, in minutes, that first time setup waits for a restart.</span></span> <span data-ttu-id="45ea1-340">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-340">Range = 0 to 2147483647.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-341">RedirectUrls</span><span class="sxs-lookup"><span data-stu-id="45ea1-341">RedirectUrls</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-342">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-342">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-343">Lista de URLs especificada</span><span class="sxs-lookup"><span data-stu-id="45ea1-343">Specified URL list</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-344">Especifica uma lista de URLs a serem redirecionadas do host para o convidado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-344">Specifies a list of URLs to be redirected from the host to the guest.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-345">SmartCardLogonEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-345">SmartCardLogonEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-346">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-346">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-347">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-347">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-348">Configura se os cartões inteligentes podem ser usados para autenticar usuários no MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-348">Configures whether smart cards can be used to authenticate users to MED-V.</span></span> <span data-ttu-id="45ea1-349">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-349">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-350">0 = falso: não permite que os cartões inteligentes autentiquem usuários finais para o MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-350">0 = false: Does not let Smart Cards authenticate end users to MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-351">1 = verdadeiro: permite que os cartões inteligentes autentiquem os usuários finais para o MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-351">1 = true: Lets Smart Cards authenticate end users to MED-V.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="45ea1-352">Importante</span><span class="sxs-lookup"><span data-stu-id="45ea1-352">Important</span></span></strong><br/><p><span data-ttu-id="45ea1-353">Se SmartCardLogonEnabled e CredentialCacheEnabled estiverem habilitados, SmartCardLogonEnabled substituirá CredentialCacheEnabled.</span><span class="sxs-lookup"><span data-stu-id="45ea1-353">If SmartCardLogonEnabled and CredentialCacheEnabled are both enabled, SmartCardLogonEnabled overrides CredentialCacheEnabled.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-354">SmartCardSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-354">SmartCardSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-356">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-356">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-357">Configura se o compartilhamento de cartões inteligentes entre o convidado e o host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-357">Configures whether the sharing of Smart Cards between the guest and the host is enabled.</span></span>  <span data-ttu-id="45ea1-358">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-358">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-359">0 = falso: desabilita o compartilhamento de cartões inteligentes entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-359">0 = false: Disables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-360">1 = verdadeiro: habilita o compartilhamento de cartões inteligentes entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-360">1 = true: Enables the sharing of Smart Cards between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-361">USBDeviceSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-361">USBDeviceSharingEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-363">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-363">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-364">Configura se o compartilhamento de dispositivos USB entre o convidado e o host está habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-364">Configures whether the sharing of USB devices between the guest and the host is enabled.</span></span>  <span data-ttu-id="45ea1-365">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-365">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-366">0 = falso: desabilita o compartilhamento de dispositivos USB entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-366">0 = false: Disables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-367">1 = verdadeiro: habilita o compartilhamento de dispositivos USB entre o convidado e o host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-367">1 = true: Enables the sharing of USB devices between the guest and the host.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="45ea1-368">Chave de VM</span><span class="sxs-lookup"><span data-stu-id="45ea1-368">VM Key</span></span>


<span data-ttu-id="45ea1-369">A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM e a tecla HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="45ea1-369">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\VM key and the HKEY\_CURRENT\_USER\\Software\\Microsoft\\Medv\\v2\\VM key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45ea1-370">Nome</span><span class="sxs-lookup"><span data-stu-id="45ea1-370">Name</span></span></th>
<th align="left"><span data-ttu-id="45ea1-371">Tipo</span><span class="sxs-lookup"><span data-stu-id="45ea1-371">Type</span></span></th>
<th align="left"><span data-ttu-id="45ea1-372">Dados/padrão</span><span class="sxs-lookup"><span data-stu-id="45ea1-372">Data/Default</span></span></th>
<th align="left"><span data-ttu-id="45ea1-373">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ea1-373">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-374">Fecharaction</span><span class="sxs-lookup"><span data-stu-id="45ea1-374">CloseAction</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-375">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-375">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-376">Padrão = HIBERNAr</span><span class="sxs-lookup"><span data-stu-id="45ea1-376">Default=HIBERNATE</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-377">A ação que a máquina virtual executa após o último aplicativo em execução é fechada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-377">The action that the virtual machine performs after the last application that is running is closed.</span></span> <span data-ttu-id="45ea1-378">Essa configuração será ignorada se o valor LogonStartEnabled estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-378">This setting is ignored if the LogonStartEnabled value is enabled.</span></span> <span data-ttu-id="45ea1-379">As opções possíveis são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="45ea1-379">Possible options are as follows:</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-380">HIBERNAr </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-380">HIBERNATE</strong> .</span></span> <span data-ttu-id="45ea1-381">Esta opção libera todos os recursos físicos que a máquina virtual está usando, como memória e CPU, e salva o estado de todos os aplicativos e operações em execução.</span><span class="sxs-lookup"><span data-stu-id="45ea1-381">This option releases all physical resources that the virtual machine is using, such as memory and CPU, and saves the state of all running applications and operations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-382">DESLIGAR </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-382">SHUTDOWN</strong> .</span></span> <span data-ttu-id="45ea1-383">Esta opção desliga o sistema operacional convidado com segurança e, em seguida, libera todos os recursos físicos que a máquina virtual está usando, como memória e CPU.</span><span class="sxs-lookup"><span data-stu-id="45ea1-383">This option shuts down the guest operating system safely and then releases all physical resources that the virtual machine is using, such as memory and CPU.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-384">desativar </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-384">TURN-OFF</strong>.</span></span> <span data-ttu-id="45ea1-385">Essa opção pode causar perda de dados porque é o mesmo que desativar o botão de energia ou retirar o cabo de alimentação em um computador físico.</span><span class="sxs-lookup"><span data-stu-id="45ea1-385">This option can cause data loss because it is the same as turning off the power button or pulling out the power cord on a physical computer.</span></span> <span data-ttu-id="45ea1-386">Use essa opção somente se não for possível usar uma das outras duas opções.</span><span class="sxs-lookup"><span data-stu-id="45ea1-386">Use this option only if you cannot use one of the other two options.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-387">GuestMemFromHostMem</span><span class="sxs-lookup"><span data-stu-id="45ea1-387">GuestMemFromHostMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-388">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-388">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-389">378, 512, 1024, 1536, 2048</span><span class="sxs-lookup"><span data-stu-id="45ea1-389">378, 512, 1024, 1536, 2048</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-390">Uma lista de valores de memória (MB) para o convidado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-390">A list of memory (MB) values for the guest.</span></span> <span data-ttu-id="45ea1-391">Esse valor é usado para determinar a quantidade de RAM disponível para o convidado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-391">This value is used to determine how much RAM is available to the guest.</span></span> <span data-ttu-id="45ea1-392">Combinado com HostMemToGuestMem, uma tabela de pesquisa é criada para determinar a quantidade de memória RAM a ser alocada na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-392">Combined with HostMemToGuestMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="45ea1-393">Os valores possíveis podem ser de 128 a 3712.</span><span class="sxs-lookup"><span data-stu-id="45ea1-393">Possible values can be from 128 to 3712.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-394">GuestUpdateDuration</span><span class="sxs-lookup"><span data-stu-id="45ea1-394">GuestUpdateDuration</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-396">Padrão = 240</span><span class="sxs-lookup"><span data-stu-id="45ea1-396">Default=240</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-397">O número de minutos que o MED-V deve manter o convidado ativo para a atualização automática, a partir do momento especificado no valor GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="45ea1-397">The number of minutes that MED-V should keep the guest awake for automatic updating, starting at the time specified in the GuestUpdateTime value.</span></span> <span data-ttu-id="45ea1-398">Intervalo = 0 a 1440.</span><span class="sxs-lookup"><span data-stu-id="45ea1-398">Range = 0 to 1440.</span></span> <span data-ttu-id="45ea1-399">Definir esse valor como zero (0) desabilita a funcionalidade de correção de convidado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-399">Setting this value to zero (0) disables the guest patching functionality.</span></span></p>
<p><span data-ttu-id="45ea1-400">Para obter mais informações sobre o patch de convidado para atualizações automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gerenciando atualizações automáticas para espaços de trabalho do MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-400">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-401">GuestUpdateTime</span><span class="sxs-lookup"><span data-stu-id="45ea1-401">GuestUpdateTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-402">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-402">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-403">Padrão = 00:00</span><span class="sxs-lookup"><span data-stu-id="45ea1-403">Default=00:00</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-404">A hora e os minutos todos os dias em que o MED-V deve ativar o convidado para atualizações automáticas usando o padrão de relógio de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="45ea1-404">The hour and minute each day when MED-V should wake up the guest for automatic updating, by using the 24-hour clock standard.</span></span> <span data-ttu-id="45ea1-405">Especificar a hora no formato HH: MM</span><span class="sxs-lookup"><span data-stu-id="45ea1-405">Specify the time in the format HH:MM</span></span>  </p>
<p><span data-ttu-id="45ea1-406">Para obter mais informações sobre o patch de convidado para atualizações automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gerenciando atualizações automáticas para espaços de trabalho do MED-V </a> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-406">For more information about guest patching for automatic updating, see <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)">Managing Automatic Updates for MED-V Workspaces</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-407">HostMemToGuestMem</span><span class="sxs-lookup"><span data-stu-id="45ea1-407">HostMemToGuestMem</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-408">MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="45ea1-408">MULTI_SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-409">1024, 2048, 4096, 8192, 16384</span><span class="sxs-lookup"><span data-stu-id="45ea1-409">1024, 2048, 4096, 8192, 16384</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-410">Uma lista de valores de memória (MB) para o convidado, determinada pela RAM disponível no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-410">A list of memory (MB) values for the guest, determined by the RAM available on the host.</span></span> <span data-ttu-id="45ea1-411">Combinado com GuestMemFromHostMem, uma tabela de pesquisa é criada para determinar a quantidade de memória RAM a ser alocada na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-411">Combined with GuestMemFromHostMem, a lookup table is created to determine how much RAM to allocate on the guest virtual machine.</span></span> <span data-ttu-id="45ea1-412">Os valores possíveis podem ser de 1024 a 16384.</span><span class="sxs-lookup"><span data-stu-id="45ea1-412">Possible values can be from 1024 to 16384.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-413">HostMemToGuestMemCalcEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-413">HostMemToGuestMemCalcEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-414">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-414">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-415">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-415">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-416">Configura se a memória alocada para o convidado é calculada a partir da memória presente no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-416">Configures whether the memory allocated for the guest is calculated from the memory present on the host.</span></span>  <span data-ttu-id="45ea1-417">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-417">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-418">0 = falso: a memória alocada para o convidado não é calculada a partir da memória presente no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-418">0 = false: The memory allocated for the guest is not calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-419">1 = verdadeiro: a memória alocada para o convidado é calculada a partir da memória presente no host.</span><span class="sxs-lookup"><span data-stu-id="45ea1-419">1 = true: The memory allocated for the guest is calculated from the memory present on the host.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-420">Memória</span><span class="sxs-lookup"><span data-stu-id="45ea1-420">Memory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-421">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-421">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-422">Padrão = 512</span><span class="sxs-lookup"><span data-stu-id="45ea1-422">Default=512</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-423">A RAM (MB) que deve ser alocada para a máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-423">The RAM (MB) that should be allocated for the guest virtual machine.</span></span> <span data-ttu-id="45ea1-424">Essa configuração será ignorada se a configuração HostMemToGuestMemEnabled estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="45ea1-424">This setting is ignored if the HostMemToGuestMemEnabled setting is enabled.</span></span> <span data-ttu-id="45ea1-425">Intervalo = de 128 a 2048.</span><span class="sxs-lookup"><span data-stu-id="45ea1-425">Range=128 to 2048.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-426">MultiUserEnabled</span><span class="sxs-lookup"><span data-stu-id="45ea1-426">MultiUserEnabled</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-427">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-427">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-428">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="45ea1-428">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-429">Configura se vários usuários compartilham o mesmo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-429">Configures whether multiple users share the same MED-V workspace.</span></span>  <span data-ttu-id="45ea1-430">0 = falso; 1 = verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="45ea1-430">0 = false; 1 = true.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-431">0 = falso: vários usuários não compartilham o mesmo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-431">0 = false: Multiple users do not share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-432">1 = verdadeiro: vários usuários compartilham o mesmo espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45ea1-432">1 = true: Multiple users share the same MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ea1-433">Networkingmode</span><span class="sxs-lookup"><span data-stu-id="45ea1-433">NetworkingMode</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-434">St</span><span class="sxs-lookup"><span data-stu-id="45ea1-434">SZ</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-435">Padrão = NAT</span><span class="sxs-lookup"><span data-stu-id="45ea1-435">Default=NAT</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-436">O tipo de conexão de rede usado no convidado.</span><span class="sxs-lookup"><span data-stu-id="45ea1-436">The kind of network connection used on the guest.</span></span> <span data-ttu-id="45ea1-437">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="45ea1-437">Possible values are as follows:</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-438">Com ponte </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-438">Bridged</strong>.</span></span> <span data-ttu-id="45ea1-439">O MED-V tem seu próprio endereço de rede, normalmente obtido por meio de DHCP.</span><span class="sxs-lookup"><span data-stu-id="45ea1-439">MED-V has its own network address, typically obtained through DHCP.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong><span data-ttu-id="45ea1-440">NAT </strong> .</span><span class="sxs-lookup"><span data-stu-id="45ea1-440">NAT</strong>.</span></span> <span data-ttu-id="45ea1-441">O MED-V usa a NAT (conversão de endereços de rede) para compartilhar o host&#39;s de IP para o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="45ea1-441">MED-V uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-442">TaskTimeout</span><span class="sxs-lookup"><span data-stu-id="45ea1-442">TaskTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-443">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-443">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-444">Padrão = 600</span><span class="sxs-lookup"><span data-stu-id="45ea1-444">Default=600</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-445">Um valor de tempo limite geral, em segundos, em que o MED-V aguarda a conclusão de uma tarefa, como reinício e desligamento.</span><span class="sxs-lookup"><span data-stu-id="45ea1-445">A general time-out value, in seconds, that MED-V waits for a task to be completed, such as restarting and shutting down.</span></span> <span data-ttu-id="45ea1-446">Intervalo = 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="45ea1-446">Range = 0 to 2147483647.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="45ea1-447">Configurações do registro de convidado</span><span class="sxs-lookup"><span data-stu-id="45ea1-447">Guest Registry Settings</span></span>


<span data-ttu-id="45ea1-448">Esta seção lista as chaves configuráveis do registro de convidado do MED-V e explica seus usos.</span><span class="sxs-lookup"><span data-stu-id="45ea1-448">This section lists the configurable MED-V guest registry keys and explains their uses.</span></span>

### <span data-ttu-id="45ea1-449">v2</span><span class="sxs-lookup"><span data-stu-id="45ea1-449">v2</span></span>

<span data-ttu-id="45ea1-450">A tabela a seguir fornece informações sobre o valor do registro Guest associado à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.</span><span class="sxs-lookup"><span data-stu-id="45ea1-450">The following table provides information about the guest registry value associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv\\v2\\ key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45ea1-451">Nome</span><span class="sxs-lookup"><span data-stu-id="45ea1-451">Name</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-452">Tipo</span><span class="sxs-lookup"><span data-stu-id="45ea1-452">Type</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-453">Dados/padrão</span><span class="sxs-lookup"><span data-stu-id="45ea1-453">Data/Default</span></span> </th>
<th align="left"><span data-ttu-id="45ea1-454">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ea1-454">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ea1-455">EnableGPWorkarounds</span><span class="sxs-lookup"><span data-stu-id="45ea1-455">EnableGPWorkarounds</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ea1-456">DWORD</span><span class="sxs-lookup"><span data-stu-id="45ea1-456">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-457">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="45ea1-457">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="45ea1-458">Configura como o MED-V manipula as chaves BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="45ea1-458">Configures how MED-V handles the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45ea1-459">Por padrão, o MED-V define estas chaves da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="45ea1-459">By default, MED-V sets these keys as follows:</span></span></p>
<p><span data-ttu-id="45ea1-460">BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0.</span><span class="sxs-lookup"><span data-stu-id="45ea1-460">BufferPolicyReads=1 and GroupPolicyMinTransferRate=0.</span></span></p>
<p><span data-ttu-id="45ea1-461">Crie a chave EnableGPWorkarounds, se for necessário, e defina a chave como zero se você não quiser que o MED-V altere as configurações padrão de BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="45ea1-461">Create the EnableGPWorkarounds  key, if it is necessary, and set the key to zero if you do not want MED-V to change the default settings of BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="45ea1-462">Observação</span><span class="sxs-lookup"><span data-stu-id="45ea1-462">Note</span></span></strong><br/><p><span data-ttu-id="45ea1-463">Se o seu espaço de trabalho do MED-V estiver em execução no modo NAT, o EnableGPWorkarounds afetará as chaves do registro BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="45ea1-463">If your MED-V workspace is running in NAT mode, EnableGPWorkarounds affects the registry keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span> <span data-ttu-id="45ea1-464">Se o seu espaço de trabalho do MED-V estiver em execução no modo de ponte, o EnableGPWorkarounds afetará apenas a chave do registro BufferPolicyReads.</span><span class="sxs-lookup"><span data-stu-id="45ea1-464">If your MED-V workspace is running in BRIDGED mode, EnableGPWorkarounds only affects the registry key BufferPolicyReads.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="45ea1-465">1 = verdadeiro: o MED-V define as chaves BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0 (se estiver em execução no modo NAT) ou apenas BufferPolicyReads = 1 (se estiver em execução no modo de ponte).</span><span class="sxs-lookup"><span data-stu-id="45ea1-465">1=true: MED-V sets the keys BufferPolicyReads=1 and GroupPolicyMinTransferRate=0 (if running in NAT mode) or just BufferPolicyReads=1 (if running in BRIDGED mode).</span></span></p>
<p><span data-ttu-id="45ea1-466">0 = falso: o MED-V não faz nenhuma alteração nas chaves BufferPolicyReads e GroupPolicyMinTransferRate.</span><span class="sxs-lookup"><span data-stu-id="45ea1-466">0=false: MED-V does not make any changes to the keys BufferPolicyReads and GroupPolicyMinTransferRate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="45ea1-467">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45ea1-467">Related topics</span></span>


[<span data-ttu-id="45ea1-468">Gerenciar aplicativos de área de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="45ea1-468">Manage MED-V Workspace Applications</span></span>](manage-med-v-workspace-applications.md)

[<span data-ttu-id="45ea1-469">Gerenciar o redirecionamento da URL da MED-V</span><span class="sxs-lookup"><span data-stu-id="45ea1-469">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)

[<span data-ttu-id="45ea1-470">Gerenciar configurações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="45ea1-470">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)









