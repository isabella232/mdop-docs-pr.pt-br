---
title: Configurando o UE-V 2. x com objetos de política de grupo
description: Configurando o UE-V 2. x com objetos de política de grupo
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799469"
---
# <span data-ttu-id="e99d6-103">Configurando o UE-V 2. x com objetos de política de grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="e99d6-104">Algumas configurações da política de grupo do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 podem ser definidas para computadores e outras configurações de política de grupo podem ser definidas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="e99d6-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="e99d6-105">Para obter informações sobre como instalar os arquivos ADMX da política de grupo do UE-V, consulte [instalando os modelos ADMX da política de grupo UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="e99d6-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="e99d6-106">As configurações de política a seguir podem ser configuradas para UE-V.</span><span class="sxs-lookup"><span data-stu-id="e99d6-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="e99d6-107">Configurações da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e99d6-108">Nome da configuração da política de grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="e99d6-109">Target</span><span class="sxs-lookup"><span data-stu-id="e99d6-109">Target</span></span></th>
<th align="left"><span data-ttu-id="e99d6-110">Descrição da configuração da política de grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="e99d6-111">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="e99d6-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-112">Texto do link de ti de contato</span><span class="sxs-lookup"><span data-stu-id="e99d6-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-113">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="e99d6-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-114">Essa configuração de política de grupo especifica o texto do hiperlink de URL do contato no centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="e99d6-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-115">Se você habilitar essa configuração de política de grupo, o centro de configurações da empresa exibirá o texto especificado no link para a URL do contato.</span><span class="sxs-lookup"><span data-stu-id="e99d6-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-116">URL de contato</span><span class="sxs-lookup"><span data-stu-id="e99d6-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-117">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="e99d6-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-118">Essa configuração de política de grupo especifica a URL do link para o contato no centro de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="e99d6-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-119">Se você habilitar essa configuração, o texto de contato do centro de configurações da empresa entrará em contato com a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="e99d6-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="e99d6-120">O link pode ser de qualquer protocolo padrão, como HTTP ou mailto.</span><span class="sxs-lookup"><span data-stu-id="e99d6-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-121">Não usar o provedor de sincronização</span><span class="sxs-lookup"><span data-stu-id="e99d6-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-122">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-123">Usando essa configuração de política de grupo, você pode configurar se o UE-V usa o recurso do provedor de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e99d6-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="e99d6-124">Essa configuração de política também permite que você habilite a notificação para que ela seja exibida quando a importação das configurações do usuário for adiada.</span><span class="sxs-lookup"><span data-stu-id="e99d6-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-125">Habilite essa configuração para configurar o UE-V Agent para não usar o provedor de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e99d6-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-126">Notificação de primeira utilização</span><span class="sxs-lookup"><span data-stu-id="e99d6-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-127">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="e99d6-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-128">Essa configuração de política de grupo permite uma notificação na área de notificação que aparece quando a UE-V</span><span class="sxs-lookup"><span data-stu-id="e99d6-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="e99d6-129">o agente é executado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e99d6-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-130">O padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="e99d6-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-131">Configurações de roaming do Windows</span><span class="sxs-lookup"><span data-stu-id="e99d6-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-132">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-133">Essa configuração de política de grupo define a sincronização das configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-134">Selecione as configurações do Windows que são sincronizadas entre computadores.</span><span class="sxs-lookup"><span data-stu-id="e99d6-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="e99d6-135">Por padrão, os temas do Windows, as configurações da área de trabalho e as configurações de facilidade de acesso sincronizam as configurações entre computadores da mesma versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e99d6-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-136">Limite de aviso de tamanho do pacote de configurações</span><span class="sxs-lookup"><span data-stu-id="e99d6-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-137">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-138">Essa configuração de política de grupo permite que você configure o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</span><span class="sxs-lookup"><span data-stu-id="e99d6-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-139">Especifique o limite preferencial para o tamanho do pacote de configurações em kilobytes (KB).</span><span class="sxs-lookup"><span data-stu-id="e99d6-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="e99d6-140">Por padrão, o UE-V Agent não tem um limite de tamanho de arquivo de pacote.</span><span class="sxs-lookup"><span data-stu-id="e99d6-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-141">Caminho de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="e99d6-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-142">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-143">Essa configuração de política de grupo define onde as configurações do usuário devem ser armazenadas.</span><span class="sxs-lookup"><span data-stu-id="e99d6-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-144">Digite um caminho UNC (Convenção Universal de nomenclatura) e variáveis como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="e99d6-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-145">Caminho do catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="e99d6-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-146">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="e99d6-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-147">Essa configuração de política de grupo define onde os modelos de localização de configurações personalizadas são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e99d6-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="e99d6-148">Essa configuração de política também define se o catálogo deve ser usado para substituir os modelos padrão da Microsoft que são instalados com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="e99d6-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-149">Insira um caminho UNC (Convenção Universal de nomenclatura) como \Server\TemplateShare ou um local de pasta no computador.</span><span class="sxs-lookup"><span data-stu-id="e99d6-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="e99d6-150">Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e99d6-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-151">Sincronizar configurações em conexões limitadas</span><span class="sxs-lookup"><span data-stu-id="e99d6-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-152">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-153">Essa configuração de política de grupo define se o UE-V sincroniza as configurações em conexões limitadas.</span><span class="sxs-lookup"><span data-stu-id="e99d6-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-154">Por padrão, o UE-V Agent não sincroniza as configurações em uma conexão limitada.</span><span class="sxs-lookup"><span data-stu-id="e99d6-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-155">Sincronizar configurações em conexões limitadas, mesmo durante o roaming</span><span class="sxs-lookup"><span data-stu-id="e99d6-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-156">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-157">Essa configuração de política de grupo define se o UE-V sincronizará as configurações em conexões limitadas fora da rede do provedor primário, por exemplo, quando a conexão de dados estiver em modo de roaming.</span><span class="sxs-lookup"><span data-stu-id="e99d6-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-158">Por padrão, o UE-V não sincroniza as configurações em uma conexão limitada quando está em modo de roaming.</span><span class="sxs-lookup"><span data-stu-id="e99d6-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-159">Tempo limite de sincronização</span><span class="sxs-lookup"><span data-stu-id="e99d6-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-160">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-161">Essa configuração de política de grupo configura o número de milissegundos que o computador aguarda antes de um tempo limite quando ele recupera as configurações de usuário do local de configurações remotas.</span><span class="sxs-lookup"><span data-stu-id="e99d6-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="e99d6-162">Se o local do armazenamento remoto não estiver disponível e o usuário não usar o provedor de sincronização, o início do aplicativo será atrasado por esse número de milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e99d6-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-163">Especifique o tempo limite de sincronização preferencial em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e99d6-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="e99d6-164">O valor padrão é 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="e99d6-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-165">Ícone de bandeja</span><span class="sxs-lookup"><span data-stu-id="e99d6-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-166">Computadores apenas</span><span class="sxs-lookup"><span data-stu-id="e99d6-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-167">Essa configuração de política de grupo habilita o ícone de bandeja do User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="e99d6-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-168">O padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="e99d6-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-169">Usar a User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="e99d6-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-170">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-171">Essa configuração de política de grupo permite habilitar ou desabilitar a virtualização da experiência do usuário (UE-V).</span><span class="sxs-lookup"><span data-stu-id="e99d6-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-172">Habilitar ou desabilitar essa configuração de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="e99d6-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e99d6-173">**Observação**  Além disso, as configurações de política de grupo estão disponíveis para muitos aplicativos da área de trabalho e aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="e99d6-174">Você pode usar essas configurações para habilitar ou desabilitar a sincronização de configurações para aplicativos específicos.</span><span class="sxs-lookup"><span data-stu-id="e99d6-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="e99d6-175">Configurações da política de grupo do aplicativo Windows</span><span class="sxs-lookup"><span data-stu-id="e99d6-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e99d6-176">Nome da configuração da política de grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="e99d6-177">Target</span><span class="sxs-lookup"><span data-stu-id="e99d6-177">Target</span></span></th>
<th align="left"><span data-ttu-id="e99d6-178">Descrição da configuração da política de grupo</span><span class="sxs-lookup"><span data-stu-id="e99d6-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="e99d6-179">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="e99d6-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-180">Não sincronizar aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="e99d6-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-181">Computadores e usuários</span><span class="sxs-lookup"><span data-stu-id="e99d6-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-182">Essa configuração de política de grupo define se o UE-V Agent sincroniza as configurações para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-183">O padrão é sincronizar aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e99d6-184">Lista de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="e99d6-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-185">Computador e usuário</span><span class="sxs-lookup"><span data-stu-id="e99d6-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-186">Esta configuração lista os nomes dos pacotes familiares dos aplicativos e Estados do Windows expressamente se a UE-V sincroniza as configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e99d6-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-187">Você pode usar essa configuração para especificar que as configurações de um aplicativo nunca sejam sincronizadas pelo UE-V, mesmo se as configurações de todos os outros aplicativos do Windows estiverem sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="e99d6-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e99d6-188">Sincronizar aplicativos do Windows não listados</span><span class="sxs-lookup"><span data-stu-id="e99d6-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-189">Computador e usuário</span><span class="sxs-lookup"><span data-stu-id="e99d6-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-190">Essa configuração de política de grupo define o comportamento de sincronização de configurações padrão do UE-V Agent para aplicativos do Windows que não estão explicitamente listados na lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e99d6-191">Por padrão, o UE-V Agent sincroniza apenas as configurações dos aplicativos do Windows que estão incluídos na lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="e99d6-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e99d6-192">Para obter mais informações sobre a sincronização de aplicativos do Windows, consulte [lista de aplicativos do Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="e99d6-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="e99d6-193">Para definir configurações de política de grupo direcionadas a computador</span><span class="sxs-lookup"><span data-stu-id="e99d6-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="e99d6-194">Use o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) no computador que atua como um controlador de domínio para gerenciar as configurações de política de grupo para computadores UE-V.</span><span class="sxs-lookup"><span data-stu-id="e99d6-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="e99d6-195">Navegue até **configuração do computador**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e99d6-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="e99d6-196">Selecione a configuração de política de grupo a ser editada.</span><span class="sxs-lookup"><span data-stu-id="e99d6-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="e99d6-197">Para definir configurações de política de grupo direcionadas ao usuário</span><span class="sxs-lookup"><span data-stu-id="e99d6-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="e99d6-198">Use o GPMC (console de gerenciamento de política de grupo) ou a ferramenta de gerenciamento avançado de política de grupo (AGPM) no Microsoft Desktop Optimization Pack (MDOP) no computador do controlador de domínio para gerenciar as configurações de política de grupo para UE-V.</span><span class="sxs-lookup"><span data-stu-id="e99d6-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="e99d6-199">Navegue até **configuração do usuário**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e99d6-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="e99d6-200">Selecione a configuração de política de grupo editada.</span><span class="sxs-lookup"><span data-stu-id="e99d6-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="e99d6-201">O UE-V Agent usa a seguinte ordem de precedência para determinar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="e99d6-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="e99d6-202">Ordem de precedência para configurações de UE-V</span><span class="sxs-lookup"><span data-stu-id="e99d6-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="e99d6-203">Configurações direcionadas ao usuário que são gerenciadas por configurações de política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="e99d6-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="e99d6-204">Configurações direcionadas por computador que são gerenciadas por configurações de política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="e99d6-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="e99d6-205">As definições de configuração que são definidas pelo usuário atual usando o Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)-essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="e99d6-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="e99d6-206">Configurações definidas para o computador usando o Windows PowerShell ou o WMI.</span><span class="sxs-lookup"><span data-stu-id="e99d6-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="e99d6-207">Essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="e99d6-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="e99d6-208">**Tem uma sugestão para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="e99d6-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="e99d6-209">Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="e99d6-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="e99d6-210">**Tem um problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="e99d6-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="e99d6-211">Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="e99d6-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="e99d6-212">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e99d6-212">Related topics</span></span>


[<span data-ttu-id="e99d6-213">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e99d6-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="e99d6-214">Gerenciar as configurações da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e99d6-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





