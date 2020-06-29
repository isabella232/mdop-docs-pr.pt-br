---
title: Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0
description: Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795994"
---
# <span data-ttu-id="72b6e-103">Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72b6e-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="72b6e-104">O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="72b6e-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="72b6e-105">O UE-V inclui um conjunto de modelos de locais de configurações predefinidos e também permite que os administradores criem modelos de localização de configurações personalizadas para aplicativos de terceiros ou de linha de negócios que são usados na empresa.</span><span class="sxs-lookup"><span data-stu-id="72b6e-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="72b6e-106">Como administrador, quando você considera quais aplicativos incluir em sua solução UE-V, considere quais configurações podem ser personalizadas pelos usuários e como e onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="72b6e-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="72b6e-107">Nem todos os aplicativos têm configurações que podem ser personalizadas ou que são rotineiramente personalizadas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="72b6e-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="72b6e-108">Além disso, nem todas as configurações de aplicativos podem fazer roaming segura entre vários computadores ou ambientes.</span><span class="sxs-lookup"><span data-stu-id="72b6e-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="72b6e-109">Sincronize as configurações que atendem aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="72b6e-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="72b6e-110">Configurações armazenadas em locais acessíveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="72b6e-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="72b6e-111">Por exemplo, não sincronize as configurações que são armazenadas na seção HKCU ou externa HKCU do registro.</span><span class="sxs-lookup"><span data-stu-id="72b6e-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="72b6e-112">Configurações que não são específicas do computador específico.</span><span class="sxs-lookup"><span data-stu-id="72b6e-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="72b6e-113">Por exemplo, exclua configurações de rede ou de hardware.</span><span class="sxs-lookup"><span data-stu-id="72b6e-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="72b6e-114">Configurações que podem ser sincronizadas entre computadores sem risco de dados corrompidos.</span><span class="sxs-lookup"><span data-stu-id="72b6e-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="72b6e-115">Por exemplo, não use configurações armazenadas em um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="72b6e-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="72b6e-116">Modelos de local de configurações incluídos na UE-V</span><span class="sxs-lookup"><span data-stu-id="72b6e-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="72b6e-117">Modelos de local das configurações do aplicativo UE-V</span><span class="sxs-lookup"><span data-stu-id="72b6e-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="72b6e-118">O software de instalação do UE-V Agent instala o agente e registra um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="72b6e-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="72b6e-119">Esses modelos de local de configurações capturam valores de configurações para os seguintes aplicativos:</span><span class="sxs-lookup"><span data-stu-id="72b6e-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="72b6e-120">Categoria do aplicativo</span><span class="sxs-lookup"><span data-stu-id="72b6e-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72b6e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="72b6e-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72b6e-122">Aplicativos do Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="72b6e-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="72b6e-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="72b6e-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="72b6e-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="72b6e-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="72b6e-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="72b6e-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="72b6e-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="72b6e-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="72b6e-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="72b6e-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="72b6e-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72b6e-135">Opções do navegador (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="72b6e-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-136">Favoritos, página inicial, guias e barras de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="72b6e-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72b6e-137">Acessórios do Windows</span><span class="sxs-lookup"><span data-stu-id="72b6e-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-138">Calculadora, bloco de notas, bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="72b6e-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72b6e-139">As configurações do aplicativo são aplicadas ao aplicativo quando o aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="72b6e-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="72b6e-140">Eles são salvos quando o aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="72b6e-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="72b6e-141">Modelos de localização de configurações do Windows para UE-V</span><span class="sxs-lookup"><span data-stu-id="72b6e-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="72b6e-142">A virtualização da experiência do usuário inclui modelos de local de configurações que capturam valores de configurações para as seguintes configurações do Windows:</span><span class="sxs-lookup"><span data-stu-id="72b6e-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72b6e-143">configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="72b6e-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="72b6e-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="72b6e-144">Description</span></span></th>
<th align="left"><span data-ttu-id="72b6e-145">Aplicar em</span><span class="sxs-lookup"><span data-stu-id="72b6e-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="72b6e-146">Estado padrão</span><span class="sxs-lookup"><span data-stu-id="72b6e-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72b6e-147">Tela de fundo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b6e-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-148">Plano de fundo da área de trabalho ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="72b6e-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-149">Logon, desbloquear, conexão remota.</span><span class="sxs-lookup"><span data-stu-id="72b6e-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-150">Habilitado</span><span class="sxs-lookup"><span data-stu-id="72b6e-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72b6e-151">Facilidade de Acesso</span><span class="sxs-lookup"><span data-stu-id="72b6e-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-152">As configurações de acessibilidade e de entrada, a lupa, o narrador e o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="72b6e-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-153">Logon, desbloquear, conexão remota.</span><span class="sxs-lookup"><span data-stu-id="72b6e-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-154">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="72b6e-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72b6e-155">Configurações da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="72b6e-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-156">Menu iniciar e configurações da barra de tarefas, opções de pasta, ícones da área de trabalho padrão, relógios adicionais e configurações de região e idioma.</span><span class="sxs-lookup"><span data-stu-id="72b6e-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-157">Somente logon.</span><span class="sxs-lookup"><span data-stu-id="72b6e-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="72b6e-158">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="72b6e-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72b6e-159">As configurações de plano de fundo da área de trabalho do Windows e facilidade de acesso são aplicadas quando o usuário faz logon, quando o computador é desbloqueado ou na conexão remota com outro computador.</span><span class="sxs-lookup"><span data-stu-id="72b6e-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="72b6e-160">O agente salva essas configurações quando o usuário faz logoff, quando o computador está bloqueado ou quando uma conexão remota é desconectada.</span><span class="sxs-lookup"><span data-stu-id="72b6e-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="72b6e-161">Por padrão, as configurações de plano de fundo da área de trabalho do Windows são feitas em roaming entre computadores da mesma versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="72b6e-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="72b6e-162">As configurações de facilidade de acesso e área de trabalho do Windows são aplicadas ao fazer logon antes que a área de trabalho seja apresentada ao usuário.</span><span class="sxs-lookup"><span data-stu-id="72b6e-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="72b6e-163">Para otimizar a experiência de logon, essas configurações não são em roaming por padrão.</span><span class="sxs-lookup"><span data-stu-id="72b6e-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="72b6e-164">As configurações de área de trabalho e facilidade de acesso podem ser habilitadas usando a política de grupo, o PowerShell e o WMI.</span><span class="sxs-lookup"><span data-stu-id="72b6e-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="72b6e-165">O UE-V não é compatível com o roaming de configurações entre sistemas operacionais com idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="72b6e-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="72b6e-166">Por exemplo, não há suporte para a sincronização entre inglês e alemão.</span><span class="sxs-lookup"><span data-stu-id="72b6e-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="72b6e-167">O idioma de todos os computadores para os quais o UE-V transfere as configurações do usuário devem coincidir.</span><span class="sxs-lookup"><span data-stu-id="72b6e-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="72b6e-168">**Observação**  Se você alterar os modelos de local de configurações fornecidos pela Microsoft, o User Experience Virtualization poderá não funcionar corretamente para o aplicativo designado ou o grupo de configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="72b6e-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="72b6e-169">Impedir a configuração de configurações do usuário não intencional</span><span class="sxs-lookup"><span data-stu-id="72b6e-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="72b6e-170">A virtualização da experiência do usuário verifica se há novas informações nas configurações do usuário e baixa essas informações de acordo com um local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="72b6e-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="72b6e-171">Em seguida, ele aplica as configurações ao computador local nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="72b6e-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="72b6e-172">Toda vez que um aplicativo é iniciado com um modelo UE-V registrado.</span><span class="sxs-lookup"><span data-stu-id="72b6e-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="72b6e-173">Quando um usuário faz logon no computador dele.</span><span class="sxs-lookup"><span data-stu-id="72b6e-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="72b6e-174">Quando um usuário desbloqueia o computador.</span><span class="sxs-lookup"><span data-stu-id="72b6e-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="72b6e-175">Quando é feita uma conexão com um computador de área de trabalho remota com UE-V instalado.</span><span class="sxs-lookup"><span data-stu-id="72b6e-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="72b6e-176">Se o UE-V estiver instalado no computador A e no computador B, e as configurações desejadas para o aplicativo estiverem no computador A, o computador A deve abrir e fechar o aplicativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="72b6e-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="72b6e-177">Se um aplicativo for aberto e fechado no computador B primeiro, as configurações do aplicativo no computador A serão configuradas para serem iguais às configurações do aplicativo no computador B.</span><span class="sxs-lookup"><span data-stu-id="72b6e-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="72b6e-178">Esse cenário também se aplica às configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="72b6e-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="72b6e-179">Se as configurações do Windows no computador B devem ser iguais às do Windows no computador A, o usuário deve fazer logon e logoff do computador primeiro.</span><span class="sxs-lookup"><span data-stu-id="72b6e-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="72b6e-180">Se as configurações de usuário desejadas forem aplicadas na ordem errada, poderão ser recuperadas ao executar uma operação de restauração para o aplicativo específico ou a configuração do Windows no computador em que as configurações foram sobrescritas.</span><span class="sxs-lookup"><span data-stu-id="72b6e-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="72b6e-181">Para obter mais informações, consulte [restaurando as configurações do aplicativo e do Windows sincronizadas com o UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="72b6e-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="72b6e-182">Modelos de localização de configurações personalizadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="72b6e-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="72b6e-183">Você pode criar modelos de local de configurações personalizadas usando o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="72b6e-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="72b6e-184">Depois de criar e testar um modelo de local de configurações personalizado em um ambiente de teste, você pode implantar os modelos de local de configurações em computadores na empresa.</span><span class="sxs-lookup"><span data-stu-id="72b6e-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="72b6e-185">Modelos de localização de configurações personalizadas devem ser implantados com uma infraestrutura de implantação existente, como o método ESD (Enterprise Software Distribution), com preferências ou configuração de um catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="72b6e-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="72b6e-186">Os modelos implantados com ESD ou política de grupo devem ser registrados usando o UE-V WMI ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72b6e-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="72b6e-187">Para obter mais informações sobre modelos de localização de configurações personalizadas, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="72b6e-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="72b6e-188">Para obter orientação sobre se um aplicativo de linha de negócios deve ser sincronizado, consulte a [lista de verificação para avaliar aplicativos de linha de negócios para o UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="72b6e-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="72b6e-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72b6e-189">Related topics</span></span>


[<span data-ttu-id="72b6e-190">Planejamento para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72b6e-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="72b6e-191">Planejar a implantação de modelo personalizado para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72b6e-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="72b6e-192">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72b6e-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





