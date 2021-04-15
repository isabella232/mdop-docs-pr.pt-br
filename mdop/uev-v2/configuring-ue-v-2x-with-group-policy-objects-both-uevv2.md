---
title: Configurando o UE-V 2.x com objetos de política de grupo
description: Configurando o UE-V 2.x com objetos de política de grupo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494056"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="c720e-103">Configurando o UE-V 2.x com objetos de política de grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="c720e-104">Algumas configurações da Política de Grupo da Experiência do Usuário da Microsoft (UE-V) 2.0, 2.1 e 2.1 SP1 podem ser definidas para computadores, e outras configurações de Política de Grupo podem ser definidas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="c720e-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="c720e-105">Para obter informações sobre como instalar arquivos ADMX da Política de Grupo UE-V, consulte [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="c720e-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="c720e-106">As configurações de política a seguir podem ser configuradas para o UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="c720e-107">Configurações da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c720e-108">Nome da configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="c720e-109">Target</span><span class="sxs-lookup"><span data-stu-id="c720e-109">Target</span></span></th>
<th align="left"><span data-ttu-id="c720e-110">Descrição da configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="c720e-111">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="c720e-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-112">Configurar o método Sync</span><span class="sxs-lookup"><span data-stu-id="c720e-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-113">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-114">Usando essa configuração de Política de Grupo, você pode configurar se a UE-V (User Experience Virtualization) usa o recurso do provedor de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c720e-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="c720e-115">Essa configuração de política também permite que uma notificação apareça quando a importação de configurações do usuário é adiada.</span><span class="sxs-lookup"><span data-stu-id="c720e-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-116">Habilita essa configuração para configurar o agente UE-V para não usar o provedor de sincronização ou para usar o mecanismo de sincronização externo.</span><span class="sxs-lookup"><span data-stu-id="c720e-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-117">Entrar em contato com o texto do link de IT</span><span class="sxs-lookup"><span data-stu-id="c720e-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-118">Somente computadores</span><span class="sxs-lookup"><span data-stu-id="c720e-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-119">Esta configuração de Política de Grupo especifica o texto do hiperlink da URL de Contato na Central de Configurações da Empresa.</span><span class="sxs-lookup"><span data-stu-id="c720e-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-120">Se você habilitar essa configuração de Política de Grupo, o Centro de Configurações da Empresa exibirá o texto especificado no link para a URL de TI de contato.</span><span class="sxs-lookup"><span data-stu-id="c720e-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-121">Entrar em contato com a URL de IT</span><span class="sxs-lookup"><span data-stu-id="c720e-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-122">Somente computadores</span><span class="sxs-lookup"><span data-stu-id="c720e-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-123">Esta configuração de Política de Grupo especifica a URL do link Contato de IT na Central de Configurações da Empresa.</span><span class="sxs-lookup"><span data-stu-id="c720e-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-124">Se você habilitar essa configuração, o Centro de Configurações da Empresa contatará links de texto de TI para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="c720e-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="c720e-125">O link pode ser de qualquer protocolo padrão, como HTTP ou mailto.</span><span class="sxs-lookup"><span data-stu-id="c720e-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-126">Notificação de Primeiro Uso</span><span class="sxs-lookup"><span data-stu-id="c720e-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-127">Somente computadores</span><span class="sxs-lookup"><span data-stu-id="c720e-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-128">Essa configuração de Política de Grupo habilita uma notificação na área de notificação que aparece quando o UE-V</span><span class="sxs-lookup"><span data-stu-id="c720e-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="c720e-129">o agente é executado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c720e-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-130">O padrão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c720e-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-131">Ping do local de armazenamento de configurações antes da sincronização</span><span class="sxs-lookup"><span data-stu-id="c720e-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-132">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-133">Essa configuração de política permite que a configuração do provedor de sincronização UE-V ping o caminho de armazenamento de configurações antes de tentar sincronizar as configurações para verificar a conexão.</span><span class="sxs-lookup"><span data-stu-id="c720e-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-134">Habilitar ou desabilitar essa configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="c720e-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-135">Limite de aviso de tamanho do pacote de configurações</span><span class="sxs-lookup"><span data-stu-id="c720e-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-136">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-137">Essa configuração de Política de Grupo permite que você configure o Agente UE-V para relatar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</span><span class="sxs-lookup"><span data-stu-id="c720e-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-138">Especifique o limite preferencial para configurações de tamanhos de pacote em quilobytes (KB).</span><span class="sxs-lookup"><span data-stu-id="c720e-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="c720e-139">Por padrão, o Agente UE-V não tem um limite de tamanho de arquivo de pacote.</span><span class="sxs-lookup"><span data-stu-id="c720e-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-140">Configurações de caminho de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c720e-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-141">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-142">Essa configuração de Política de Grupo configura onde as configurações do usuário devem ser armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c720e-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-143">Insira um caminho UNC (Convenção de Nomenização Universal) e variáveis como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="c720e-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-144">Caminho do catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="c720e-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-145">Somente computadores</span><span class="sxs-lookup"><span data-stu-id="c720e-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-146">Esta configuração de Política de Grupo configura onde os modelos de local de configurações personalizadas são armazenados.</span><span class="sxs-lookup"><span data-stu-id="c720e-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="c720e-147">Essa configuração de política também configura se o catálogo deve ser usado para substituir os modelos padrão da Microsoft instalados pelo Agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-148">Insira um caminho UNC (Convenção de Nomenização Universal), como \Server\TemplateShare ou um local de pasta no computador.</span><span class="sxs-lookup"><span data-stu-id="c720e-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="c720e-149">Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c720e-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-150">Configurações de sincronização em conexões com metros</span><span class="sxs-lookup"><span data-stu-id="c720e-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-151">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-152">Esta configuração de Política de Grupo define se o UE-V sincroniza configurações em conexões com metros.</span><span class="sxs-lookup"><span data-stu-id="c720e-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-153">Por padrão, o Agente UE-V não sincroniza configurações em uma conexão com metros.</span><span class="sxs-lookup"><span data-stu-id="c720e-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-154">Configurações de sincronização sobre conexões com medidor mesmo quando o roaming</span><span class="sxs-lookup"><span data-stu-id="c720e-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-155">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-156">Esta configuração de Política de Grupo define se o UE-V sincroniza configurações em conexões com metros fora da rede do provedor 1, por exemplo, quando a conexão de dados está no modo roaming.</span><span class="sxs-lookup"><span data-stu-id="c720e-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-157">Por padrão, o UE-V não sincroniza configurações em uma conexão com metros quando está no modo roaming.</span><span class="sxs-lookup"><span data-stu-id="c720e-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-158">Tempo de tempo de sincronização</span><span class="sxs-lookup"><span data-stu-id="c720e-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-159">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-160">Esta configuração de Política de Grupo configura o número de milissegundos que o computador aguarda antes de um tempo de espera quando recupera as configurações do usuário do local de configurações remotas.</span><span class="sxs-lookup"><span data-stu-id="c720e-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="c720e-161">Se o local de armazenamento remoto não estiver disponível e o usuário não usar o provedor de sincronização, o início do aplicativo será adiado por esse número de milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c720e-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-162">Especifique o tempo de tempo de sincronização preferencial em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c720e-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="c720e-163">O valor padrão é 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c720e-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-164">Sincronizar configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="c720e-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="c720e-165">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-166">Essa configuração de Política de Grupo configura a sincronização das configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-167">Selecione quais configurações do Windows sincronizam entre computadores.</span><span class="sxs-lookup"><span data-stu-id="c720e-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="c720e-168">Por padrão, temas do Windows, configurações de área de trabalho e configurações de Facilidade de Acesso sincronizam configurações entre computadores da mesma versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c720e-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-169">Ícone de bandeja</span><span class="sxs-lookup"><span data-stu-id="c720e-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-170">Somente computadores</span><span class="sxs-lookup"><span data-stu-id="c720e-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-171">Essa configuração de Política de Grupo habilita o ícone da bandeja UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-172">O padrão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c720e-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-173">Usar a Virtualização da Experiência do Usuário (UE-V)</span><span class="sxs-lookup"><span data-stu-id="c720e-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-174">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-175">Essa configuração de Política de Grupo permite habilitar ou desabilitar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-176">Habilitar ou desabilitar essa configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="c720e-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-177">Configuração VDI</span><span class="sxs-lookup"><span data-stu-id="c720e-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-178">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-179">Essa configuração de política configura a sincronização de informações de rebaixamento do UE-V para computadores em execução em um ambiente VDI em pool.</span><span class="sxs-lookup"><span data-stu-id="c720e-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="c720e-180">Se essa política estiver habilitada, o estado de rebaixamento UE-V será copiado para o local de armazenamento de configurações no logout e restaurado no logon.</span><span class="sxs-lookup"><span data-stu-id="c720e-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-181">Habilitar ou desabilitar essa configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="c720e-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c720e-182">Observação</span><span class="sxs-lookup"><span data-stu-id="c720e-182">Note</span></span>**  
<span data-ttu-id="c720e-183">Além disso, as configurações da Política de Grupo estão disponíveis para muitos aplicativos da área de trabalho e aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="c720e-184">Você pode usar essas configurações para habilitar ou desabilitar a sincronização de configurações para aplicativos específicos.</span><span class="sxs-lookup"><span data-stu-id="c720e-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="c720e-185">Configurações da Política de Grupo de Aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="c720e-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c720e-186">Nome da configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="c720e-187">Target</span><span class="sxs-lookup"><span data-stu-id="c720e-187">Target</span></span></th>
<th align="left"><span data-ttu-id="c720e-188">Descrição da configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c720e-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="c720e-189">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="c720e-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-190">Não sincronizar aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="c720e-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-191">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="c720e-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-192">Esta configuração de Política de Grupo define se o Agente UE-V sincroniza configurações para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-193">O padrão é sincronizar aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c720e-194">Lista de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="c720e-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-195">Computador e Usuário</span><span class="sxs-lookup"><span data-stu-id="c720e-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-196">Essa configuração lista os nomes de pacote da família dos aplicativos e estados do Windows expressamente se o UE-V sincroniza as configurações desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c720e-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-197">Você pode usar essa configuração para especificar que as configurações de um aplicativo nunca são sincronizadas pelo UE-V, mesmo que as configurações de todos os outros aplicativos do Windows sejam sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="c720e-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c720e-198">Sincronizar aplicativos do Windows não listados</span><span class="sxs-lookup"><span data-stu-id="c720e-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-199">Computador e Usuário</span><span class="sxs-lookup"><span data-stu-id="c720e-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-200">Esta configuração de Política de Grupo define o comportamento de sincronização de configurações padrão do Agente UE-V para aplicativos Windows que não estão explicitamente listados na lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c720e-201">Por padrão, o Agente UE-V sincroniza apenas as configurações desses aplicativos do Windows incluídos na lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c720e-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c720e-202">Para obter mais informações sobre como sincronizar aplicativos do Windows, consulte [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="c720e-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="c720e-203">Para configurar configurações de Política de Grupo direcionadas ao computador</span><span class="sxs-lookup"><span data-stu-id="c720e-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="c720e-204">Use o Console de Gerenciamento de Política de Grupo (GPMC) ou o AgPM (Gerenciamento Avançado de Política de Grupo) no computador que atua como controlador de domínio para gerenciar configurações de Política de Grupo para computadores UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="c720e-205">Navegue **até Configuração do computador,** selecione **Políticas,** selecione **Modelos Administrativos,** clique em **Componentes**do Windows e selecione **Virtualização da Experiência do Usuário da Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="c720e-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="c720e-206">Selecione a configuração de Política de Grupo a ser editada.</span><span class="sxs-lookup"><span data-stu-id="c720e-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="c720e-207">Para configurar configurações de Política de Grupo direcionadas ao usuário</span><span class="sxs-lookup"><span data-stu-id="c720e-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="c720e-208">Use o Console de Gerenciamento de Política de Grupo (GPMC) ou a ferramenta AgPM (Gerenciamento avançado de Política de Grupo) no Microsoft Desktop Optimization Pack (MDOP) no computador controlador de domínio para gerenciar as configurações de Política de Grupo para UE-V.</span><span class="sxs-lookup"><span data-stu-id="c720e-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="c720e-209">Navegue **até Configuração do usuário,** selecione **Políticas,** selecione **Modelos Administrativos,** clique em **Componentes**do Windows e selecione **Virtualização da Experiência**do Usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c720e-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="c720e-210">Selecione a configuração de Política de Grupo editada.</span><span class="sxs-lookup"><span data-stu-id="c720e-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="c720e-211">O Agente UE-V usa a seguinte ordem de precedência para determinar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="c720e-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="c720e-212">Ordem de precedência para configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="c720e-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="c720e-213">Configurações direcionadas ao usuário gerenciadas pelas configurações da Política de Grupo - Essas configurações são armazenadas na chave do Registro pela Política de Grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c720e-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="c720e-214">Configurações direcionadas ao computador gerenciadas pelas configurações da Política de Grupo - Essas configurações são armazenadas na chave do Registro pela Política de Grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c720e-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="c720e-215">Configurações definidas pelo usuário atual usando Windows PowerShell ou Instrumentação de Gerenciamento do Windows (WMI) - Essas configurações são armazenadas pelo Agente UE-V neste local do Registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c720e-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="c720e-216">Configurações definidas para o computador usando Windows PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="c720e-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="c720e-217">Essas configurações são armazenadas pelo Agente UE-V neste local do Registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c720e-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="c720e-218">**Tem uma sugestão para UE-V?**</span><span class="sxs-lookup"><span data-stu-id="c720e-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="c720e-219">Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c720e-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="c720e-220">**Tem um problema UE-V?**</span><span class="sxs-lookup"><span data-stu-id="c720e-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="c720e-221">Use o [Fórum do TechNet UE-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)</span><span class="sxs-lookup"><span data-stu-id="c720e-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c720e-222">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c720e-222">Related topics</span></span>


[<span data-ttu-id="c720e-223">Administrando o UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c720e-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="c720e-224">Gerenciar as configurações da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c720e-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
