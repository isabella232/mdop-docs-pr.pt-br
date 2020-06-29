---
title: Configurando o UE-V com objetos de Política de Grupo
description: Configurando o UE-V com objetos de Política de Grupo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799924"
---
# <span data-ttu-id="31ccb-103">Configurando o UE-V com objetos de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="31ccb-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="31ccb-104">Algumas configurações da política de grupo do Microsoft User Experience Virtualization (UE-V Microsoft Virtualization) podem ser definidas para computadores e outras pessoas podem ser definidas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="31ccb-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="31ccb-105">As configurações da política de configuração do UE-V Agent podem ser definidas para computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="31ccb-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="31ccb-106">Para obter informações sobre como instalar os arquivos ADMX da política de grupo do UE-V, consulte [instalando os modelos ADMX da política de grupo UE-v](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="31ccb-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="31ccb-107">As seguintes configurações de política podem ser configuradas para UE-V:</span><span class="sxs-lookup"><span data-stu-id="31ccb-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ccb-108">Nome da configuração de política</span><span class="sxs-lookup"><span data-stu-id="31ccb-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="31ccb-109">Target</span><span class="sxs-lookup"><span data-stu-id="31ccb-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="31ccb-110">Descrição da configuração de política</span><span class="sxs-lookup"><span data-stu-id="31ccb-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="31ccb-111">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="31ccb-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ccb-112">Usar a User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="31ccb-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-113">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-114">Essa configuração de política permite habilitar ou desabilitar a virtualização da experiência do usuário (UE-V).</span><span class="sxs-lookup"><span data-stu-id="31ccb-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-115">Habilitar ou desabilitar essa configuração de política.</span><span class="sxs-lookup"><span data-stu-id="31ccb-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ccb-116">Caminho de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="31ccb-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-117">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-118">Essa configuração de política define onde as configurações de usuário serão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="31ccb-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-119">Fornecer um caminho e variáveis UNC (Convenção Universal de nomenclatura), como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="31ccb-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ccb-120">Caminho do catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="31ccb-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-121">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="31ccb-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-122">Essa configuração de política define onde os modelos de localização de configurações personalizadas são armazenados.</span><span class="sxs-lookup"><span data-stu-id="31ccb-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="31ccb-123">Essa configuração de política também define se o catálogo será usado para substituir os modelos padrão do Microsoft que são instalados com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="31ccb-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-124">Forneça um caminho UNC (Convenção Universal de nomenclatura), como \Server\TemplateShare ou um local de pasta no computador.</span><span class="sxs-lookup"><span data-stu-id="31ccb-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="31ccb-125">Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31ccb-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ccb-126">Não usar arquivos offline</span><span class="sxs-lookup"><span data-stu-id="31ccb-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-127">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-128">Essa configuração de política permite que você defina se a UE-V usará o recurso arquivos offline do Windows.</span><span class="sxs-lookup"><span data-stu-id="31ccb-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="31ccb-129">Essa configuração de política também permite que você habilite a notificação para ocorrer quando a importação das configurações do usuário é atrasada.</span><span class="sxs-lookup"><span data-stu-id="31ccb-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-130">Para configurar o UE-V Agent para não usar arquivos offline, habilite essa configuração.</span><span class="sxs-lookup"><span data-stu-id="31ccb-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="31ccb-131">Especifique se as notificações devem ser fornecidas quando a importação de configurações está atrasada.</span><span class="sxs-lookup"><span data-stu-id="31ccb-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="31ccb-132">Especifique a duração do tempo em segundos a ser aguardada até que a notificação seja exibida.</span><span class="sxs-lookup"><span data-stu-id="31ccb-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ccb-133">Tempo limite de sincronização</span><span class="sxs-lookup"><span data-stu-id="31ccb-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-134">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-135">Essa configuração de política configura o número de milissegundos que o computador aguarda antes do tempo limite ao recuperar as configurações de usuário do local de configurações remotas.</span><span class="sxs-lookup"><span data-stu-id="31ccb-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="31ccb-136">Se o local do armazenamento remoto não estiver disponível, a inicialização do aplicativo será adiada por esse número de milissegundos.</span><span class="sxs-lookup"><span data-stu-id="31ccb-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-137">Especifique o tempo limite de sincronização preferencial em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="31ccb-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="31ccb-138">O valor padrão de 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="31ccb-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ccb-139">Limite de aviso de tamanho do pacote</span><span class="sxs-lookup"><span data-stu-id="31ccb-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-140">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-141">Essa configuração de política permite que você configure o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</span><span class="sxs-lookup"><span data-stu-id="31ccb-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-142">Especificado o limite preferencial para configurações de tamanhos de pacote em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="31ccb-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="31ccb-143">Por padrão, o UE-V Agent não tem um limite de tamanho de arquivo de pacote.</span><span class="sxs-lookup"><span data-stu-id="31ccb-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ccb-144">Configurações de aplicativo de roaming</span><span class="sxs-lookup"><span data-stu-id="31ccb-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-145">Somente usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-146">Essa configuração de política define o roaming das configurações de usuário dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="31ccb-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-147">Selecione as configurações do Windows que serão transferidas entre computadores.</span><span class="sxs-lookup"><span data-stu-id="31ccb-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="31ccb-148">Por padrão, as configurações do usuário de aplicativos com o modelo de configurações fornecidas pela UE-V são móveis entre computadores.</span><span class="sxs-lookup"><span data-stu-id="31ccb-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ccb-149">Configurações de roaming do Windows</span><span class="sxs-lookup"><span data-stu-id="31ccb-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-150">Somente usuários</span><span class="sxs-lookup"><span data-stu-id="31ccb-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-151">Essa configuração de política define o roaming das configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="31ccb-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ccb-152">Selecione quais aplicativos serão movidos entre computadores.</span><span class="sxs-lookup"><span data-stu-id="31ccb-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="31ccb-153">Por padrão, os temas do Windows são movidos entre computadores da mesma versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="31ccb-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="31ccb-154">As configurações da área de trabalho do Windows e da facilidade de acesso não são roamas.</span><span class="sxs-lookup"><span data-stu-id="31ccb-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="31ccb-155">Para configurar políticas direcionadas a computador</span><span class="sxs-lookup"><span data-stu-id="31ccb-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="31ccb-156">Use o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) no computador do controlador de domínio que gerencia a política de grupo para computadores UE-V.</span><span class="sxs-lookup"><span data-stu-id="31ccb-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="31ccb-157">Navegue até **configuração do computador**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="31ccb-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="31ccb-158">Selecione a configuração de política a ser editada.</span><span class="sxs-lookup"><span data-stu-id="31ccb-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="31ccb-159">Para configurar políticas direcionadas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="31ccb-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="31ccb-160">Use o GPMC (console de gerenciamento de política de grupo) ou a ferramenta de gerenciamento avançado de política de grupo (AGPM) no Microsoft Desktop Optimization Pack (MDOP) no computador do controlador de domínio que gerencia a política de grupo para UE-V.</span><span class="sxs-lookup"><span data-stu-id="31ccb-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="31ccb-161">Navegue até **configuração do usuário**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="31ccb-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="31ccb-162">Selecione a configuração de política editada.</span><span class="sxs-lookup"><span data-stu-id="31ccb-162">Select the policy setting edited.</span></span>

<span data-ttu-id="31ccb-163">O UE-V Agent usa a seguinte ordem de precedência para determinar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="31ccb-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="31ccb-164">Ordem de precedência para configurações de UE-V</span><span class="sxs-lookup"><span data-stu-id="31ccb-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="31ccb-165">Configurações direcionadas pelo usuário gerenciadas pela política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="31ccb-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="31ccb-166">Configurações direcionadas por computador gerenciadas pela política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="31ccb-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="31ccb-167">Configurações definidas pelo usuário atual usando o PowerShell ou o WMI-essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="31ccb-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="31ccb-168">Configurações definidas para o computador usando o PowerShell ou o WMI.</span><span class="sxs-lookup"><span data-stu-id="31ccb-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="31ccb-169">Esses parâmetros de configuração são armazenados pelo UE-V Agent em `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="31ccb-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="31ccb-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31ccb-170">Related topics</span></span>


[<span data-ttu-id="31ccb-171">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="31ccb-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="31ccb-172">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="31ccb-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





