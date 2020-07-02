---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795442"
---
# <span data-ttu-id="8b3c1-103">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="8b3c1-104">Esta documentação é uma versão do para o UE-V incluída no Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="8b3c1-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="8b3c1-105">Para obter informações sobre a versão mais recente do UE-V que está incluída no Windows 10 Enterprise, consulte [introdução ao UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="8b3c1-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="8b3c1-106">Capture e centralize as configurações do aplicativo do usuário e as configurações do sistema operacional do Windows implementando o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="8b3c1-107">Em seguida, aplique essas configurações aos dispositivos que os usuários acessam na sua empresa, como computadores de mesa, laptops ou sessões do Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="8b3c1-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="8b3c1-108">Com a UE-V, você pode...</span><span class="sxs-lookup"><span data-stu-id="8b3c1-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="8b3c1-109">Especificar quais configurações de aplicativo e área de trabalho sincronizar</span><span class="sxs-lookup"><span data-stu-id="8b3c1-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="8b3c1-110">Oferecer as configurações a qualquer momento e em qualquer lugar onde os usuários trabalhem em toda a empresa</span><span class="sxs-lookup"><span data-stu-id="8b3c1-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="8b3c1-111">Criar modelos personalizados para os aplicativos de terceiros ou de linha de negócios</span><span class="sxs-lookup"><span data-stu-id="8b3c1-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="8b3c1-112">Recuperar as configurações após a substituição ou atualização de hardware ou depois de refazer a criação de uma nova imagem de uma máquina virtual para seu estado inicial</span><span class="sxs-lookup"><span data-stu-id="8b3c1-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="8b3c1-113">Componentes da UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="8b3c1-114">Este diagrama mostra como implantados componentes do UE-V trabalham em conjunto para sincronizar as configurações.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![diagrama arquitetônico uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b3c1-116">Componente</span><span class="sxs-lookup"><span data-stu-id="8b3c1-116">Component</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-117">Função</span><span class="sxs-lookup"><span data-stu-id="8b3c1-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8b3c1-118">UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="8b3c1-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-119">Instalado em cada computador que precisa sincronizar as configurações, o <strong> UE-V Agent </strong> monitora os aplicativos registrados e o sistema operacional em busca de alterações de configurações e, em seguida, sincroniza essas configurações entre computadores.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8b3c1-120">Pacotes de configurações</span><span class="sxs-lookup"><span data-stu-id="8b3c1-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-121">As configurações do aplicativo e as configurações do Windows são armazenadas em <strong> pacotes de configurações </strong> criados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="8b3c1-122">Os pacotes de configurações são criados, armazenados localmente e copiados para o local de armazenamento das configurações.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="8b3c1-123">Os valores de configuração para <strong> aplicativos da área de trabalho </strong> são armazenados quando o usuário fecha o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="8b3c1-124">Os valores das <strong> configurações do Windows </strong> são armazenados quando o usuário faz logoff, quando o computador está bloqueado ou quando o usuário se desconecta remotamente de um computador.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="8b3c1-125">O provedor de sincronização determina quando as configurações do aplicativo ou do sistema operacional são lidas a partir dos <strong> pacotes de configurações </strong> e sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8b3c1-126">Local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="8b3c1-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-127">Esse é um compartilhamento de rede padrão que os usuários podem acessar.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="8b3c1-128">O UE-V Agent verifica o local e cria uma pasta de sistema oculta para armazenar e recuperar as configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8b3c1-129">Modelos de local de configurações</span><span class="sxs-lookup"><span data-stu-id="8b3c1-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-130">O UE-V usa os arquivos XML como modelos de localização de configurações para monitorar e sincronizar as configurações de aplicativo da área de trabalho e as configurações da área de trabalho do Windows entre computadores</span><span class="sxs-lookup"><span data-stu-id="8b3c1-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="8b3c1-131">Por padrão, alguns modelos de local de configurações estão incluídos na UE-V.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="8b3c1-132">Você também pode criar, editar ou validar modelos de local de configurações personalizadas ao <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gerenciar a sincronização de configurações para aplicativos personalizados </a> .</span><span class="sxs-lookup"><span data-stu-id="8b3c1-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8b3c1-133">Observação</span><span class="sxs-lookup"><span data-stu-id="8b3c1-133">Note</span></span></strong><br/><p><span data-ttu-id="8b3c1-134">Os modelos de local de configurações não são necessários para aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8b3c1-135">Lista de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="8b3c1-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-136">As configurações para aplicativos do Windows são capturadas e aplicadas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="8b3c1-137">O desenvolvedor do aplicativo especifica as configurações que são sincronizadas para cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="8b3c1-138">O UE-V determina quais aplicativos do Windows estão habilitados para sincronização de configurações usando uma lista gerenciada de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="8b3c1-139">Por padrão, essa lista inclui a maioria dos aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="8b3c1-140">Você pode adicionar ou remover aplicativos na lista de aplicativos do Windows seguindo os procedimentos mostrados <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> aqui </a> .</span><span class="sxs-lookup"><span data-stu-id="8b3c1-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="8b3c1-141">Gerenciando a sincronização de configurações para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="8b3c1-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="8b3c1-142">Use estes componentes UE-V para criar e gerenciar modelos personalizados para seus aplicativos de terceiros ou de linha de negócios.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8b3c1-143">Gerador de UE-V</span><span class="sxs-lookup"><span data-stu-id="8b3c1-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-144">Use o <strong> UE-V Generator </strong> para criar modelos de localização de configurações personalizadas que você pode distribuir para os computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="8b3c1-145">O gerador UE-V também permite que você edite um modelo existente ou valide um modelo que foi criado usando outro editor de XML.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8b3c1-146">Catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="8b3c1-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-147">O <strong> Catálogo de modelos de configurações </strong> é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens de servidor (SMB) que armazena os modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="8b3c1-148">O UE-V Agent verifica esse local uma vez por dia, recupera modelos novos ou atualizados e atualiza seu comportamento de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="8b3c1-149">Se você usar somente os modelos de local de configurações padrão do UE-V, um catálogo de modelos de configurações será desnecessário.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="8b3c1-150">Para obter mais informações sobre os catálogos de implantação de configurações, consulte <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurar um catálogo de modelos de configurações de UE-V </a> .</span><span class="sxs-lookup"><span data-stu-id="8b3c1-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![processo de gerador de UE-v](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="8b3c1-152">Configurações sincronizadas por padrão</span><span class="sxs-lookup"><span data-stu-id="8b3c1-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="8b3c1-153">Por padrão, o UE-V sincroniza as configurações desses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="8b3c1-154">Para obter uma lista completa e informações mais detalhadas, consulte [configurações que são sincronizadas automaticamente em uma implantação do UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="8b3c1-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="8b3c1-155">Aplicativos do Microsoft Office 2013 (UE-V 2,1 SP1 e 2,1)</span><span class="sxs-lookup"><span data-stu-id="8b3c1-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="8b3c1-156">Aplicativos do Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 e 2,0)</span><span class="sxs-lookup"><span data-stu-id="8b3c1-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="8b3c1-157">Aplicativos do Microsoft Office 2007 (somente para o UE-V 2,0)</span><span class="sxs-lookup"><span data-stu-id="8b3c1-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="8b3c1-158">Internet Explorer 8, 9 e 10</span><span class="sxs-lookup"><span data-stu-id="8b3c1-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="8b3c1-159">Internet Explorer 11 no UE-V 2,1 SP1 e 2,1</span><span class="sxs-lookup"><span data-stu-id="8b3c1-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="8b3c1-160">Muitos aplicativos do Windows, como o Xbox</span><span class="sxs-lookup"><span data-stu-id="8b3c1-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="8b3c1-161">Muitos aplicativos da área de trabalho do Windows, como o bloco de notas</span><span class="sxs-lookup"><span data-stu-id="8b3c1-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="8b3c1-162">Muitas configurações do Windows, como plano de fundo da área de trabalho ou papel de parede</span><span class="sxs-lookup"><span data-stu-id="8b3c1-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="8b3c1-163">Observação</span><span class="sxs-lookup"><span data-stu-id="8b3c1-163">Note</span></span>**  
<span data-ttu-id="8b3c1-164">Você também pode [Personalizar o UE-V para sincronizar as configurações](https://technet.microsoft.com/library/dn458942.aspx) de aplicativos diferentes das sincronizadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="8b3c1-165">Comparar o UE-V com outros produtos da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3c1-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="8b3c1-166">Use esta tabela para comparar o UE-V para sincronizar perfis no Windows 7, sincronizar perfis no Windows 8 e o recurso configurações do computador de sincronização da conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b3c1-167">Recurso</span><span class="sxs-lookup"><span data-stu-id="8b3c1-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-168">Sincronizar perfis usando o Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b3c1-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-169">Sincronizar perfis usando o Windows 8</span><span class="sxs-lookup"><span data-stu-id="8b3c1-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-170">Sincronizar perfis usando o Windows 10</span><span class="sxs-lookup"><span data-stu-id="8b3c1-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-171">Conta Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3c1-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="8b3c1-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="8b3c1-173">UE-V 2,1 e 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="8b3c1-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-174">Sincronizar configurações entre vários computadores</span><span class="sxs-lookup"><span data-stu-id="8b3c1-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-175">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-176">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-177">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-178">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-179">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-180">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-181">Sincronizar configurações entre aplicativos físicos e virtuais</span><span class="sxs-lookup"><span data-stu-id="8b3c1-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-182">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-183">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-184">Sincronizar configurações do aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="8b3c1-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-185">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-186">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-187">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-188">Gerenciar via WMI</span><span class="sxs-lookup"><span data-stu-id="8b3c1-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-189">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-190">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-191">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-192">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-193">Sincronizar alterações de configurações regularmente</span><span class="sxs-lookup"><span data-stu-id="8b3c1-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-194">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-195">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-196">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-197">Configuração mínima para a instalação</span><span class="sxs-lookup"><span data-stu-id="8b3c1-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-198">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-199">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-200">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-201">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-202">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-203">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-204">Com suporte em computadores não associados ao domínio</span><span class="sxs-lookup"><span data-stu-id="8b3c1-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-205">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-206">Compatível com o atributo do Active Directory do computador principal</span><span class="sxs-lookup"><span data-stu-id="8b3c1-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-207">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-208">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-209">Sincroniza as configurações entre os serviços de área de trabalho (RDS) e os serviços de área de trabalho avançados do Virtual Desktop Infrastructure (VDI)</span><span class="sxs-lookup"><span data-stu-id="8b3c1-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-210">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-211">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-212">Espaço de armazenamento de configuração ilimitada</span><span class="sxs-lookup"><span data-stu-id="8b3c1-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-213">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-214">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-215">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-216">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-217">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b3c1-218">Escolha de quais configurações do aplicativo sincronizar</span><span class="sxs-lookup"><span data-stu-id="8b3c1-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-219">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-220">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b3c1-221">Backup/restauração para profissionais de ti</span><span class="sxs-lookup"><span data-stu-id="8b3c1-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-222">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-223">Parcial</span><span class="sxs-lookup"><span data-stu-id="8b3c1-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b3c1-224">●</span><span class="sxs-lookup"><span data-stu-id="8b3c1-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8b3c1-225">Notas da versão do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="8b3c1-226">Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, consulte</span><span class="sxs-lookup"><span data-stu-id="8b3c1-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="8b3c1-227">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3c1-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="8b3c1-228">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3c1-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="8b3c1-229">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8b3c1-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="8b3c1-230">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="8b3c1-230">Other resources for this product</span></span>


-   [<span data-ttu-id="8b3c1-231">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="8b3c1-232">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="8b3c1-233">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="8b3c1-234">Solução de problemas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="8b3c1-235">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="8b3c1-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="8b3c1-236">Mais informações</span><span class="sxs-lookup"><span data-stu-id="8b3c1-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="8b3c1-237">[Página do TechCenter do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Saiba mais sobre as informações e os recursos mais recentes do MDOP.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="8b3c1-238">[Experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Encontre documentação, vídeos e outros recursos para tecnologias do MDOP.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="8b3c1-239">Você também pode [enviar comentários](mailto:MDOPDocs@microsoft.com) ou saber mais sobre atualizações seguindo-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="8b3c1-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














