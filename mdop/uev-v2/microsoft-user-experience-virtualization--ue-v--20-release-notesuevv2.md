---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799641"
---
# <span data-ttu-id="772f8-103">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="772f8-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="772f8-104">Para pesquisar as notas de versão do Microsoft User Experience Virtualization (UE-V) 2,0, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="772f8-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="772f8-105">Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="772f8-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="772f8-106">As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="772f8-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="772f8-107">Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="772f8-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="772f8-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="772f8-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="772f8-109">Fornecendo comentários</span><span class="sxs-lookup"><span data-stu-id="772f8-109">Providing feedback</span></span>


<span data-ttu-id="772f8-110">Diga-nos o que você acha da nossa documentação do MDOP, enviando-nos seus comentários e comentários.</span><span class="sxs-lookup"><span data-stu-id="772f8-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="772f8-111">Envie seus comentários sobre a documentação para [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="772f8-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="772f8-112">Problemas conhecidos do UE-V</span><span class="sxs-lookup"><span data-stu-id="772f8-112">UE-V known issues</span></span>


<span data-ttu-id="772f8-113">Esta seção contém notas de versão para a virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="772f8-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="772f8-114">As configurações do registro não são sincronizadas entre aplicativos nativos e App-V no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="772f8-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="772f8-115">Quando um computador tem um aplicativo instalado por meio da virtualização de aplicativos (App-V) e um local com um arquivo do Windows Installer (. msi), as configurações baseadas em registro não são sincronizadas entre as tecnologias.</span><span class="sxs-lookup"><span data-stu-id="772f8-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="772f8-116">**Solução alternativa:** Para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.</span><span class="sxs-lookup"><span data-stu-id="772f8-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="772f8-117">As configurações não sincronizam quando o compartilhamento de rede está fora do domínio do usuário</span><span class="sxs-lookup"><span data-stu-id="772f8-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="772f8-118">Quando o Windows® 8 tenta a sincronização das configurações do sistema operacional, a sincronização falha com a seguinte mensagem de erro: **Boost:: FileSystem:: Exists:: nome de usuário ou senha incorreto**.</span><span class="sxs-lookup"><span data-stu-id="772f8-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="772f8-119">Esse erro pode indicar que o compartilhamento de rede está fora do domínio do usuário ou um domínio com uma relação de confiança para esse domínio.</span><span class="sxs-lookup"><span data-stu-id="772f8-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="772f8-120">Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="772f8-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="772f8-121">Os compartilhamentos de rede usados para as configurações de UE-V armazenam locais de armazenamento devem residir no mesmo domínio do Active Directory que o usuário ou um domínio confiável do domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="772f8-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="772f8-122">**Solução alternativa:** Use compartilhamentos de rede do mesmo domínio do Active Directory que o usuário.</span><span class="sxs-lookup"><span data-stu-id="772f8-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="772f8-123">Resultados imprevisíveis com o Office 2010 e o Office 2013 instalados</span><span class="sxs-lookup"><span data-stu-id="772f8-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="772f8-124">Quando um usuário tem o Office 2010 e o Office 2013 instalados, todas as configurações comuns entre as duas versões do Office são móveis pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="772f8-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="772f8-125">Isso pode fazer com que o tamanho do pacote do Office 2010 seja muito grande ou resulte em conflitos imprevisíveis com o 2013, principalmente se o Office 365 for usado.</span><span class="sxs-lookup"><span data-stu-id="772f8-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="772f8-126">**Solução alternativa:** Instale apenas uma versão do Office ou limite quais configurações são sincronizadas por UE-V.</span><span class="sxs-lookup"><span data-stu-id="772f8-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="772f8-127">Desinstalar e reinstalar o aplicativo Windows 8 reverte as configurações para o estado inicial</span><span class="sxs-lookup"><span data-stu-id="772f8-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="772f8-128">Ao usar a sincronização de configurações do UE-V para um aplicativo do Windows 8, se o usuário desinstalar o aplicativo e reinstalar o aplicativo, as configurações do aplicativo retornarão aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="772f8-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="772f8-129">Isso acontece porque a desinstalação remove a cópia local (em cache) das configurações do aplicativo, mas não remove o pacote de configurações local do UE-V.</span><span class="sxs-lookup"><span data-stu-id="772f8-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="772f8-130">Quando o aplicativo é reinstalado e iniciado, o UE-V coleta as configurações do aplicativo que foram redefinidas para os padrões do aplicativo e, em seguida, carrega as configurações padrão para o local de armazenamento central.</span><span class="sxs-lookup"><span data-stu-id="772f8-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="772f8-131">Outros computadores executando o aplicativo e, em seguida, baixar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="772f8-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="772f8-132">Esse comportamento é idêntico ao comportamento dos aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="772f8-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="772f8-133">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="772f8-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="772f8-134">Roaming de assinatura de email do Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="772f8-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="772f8-135">O UE-V fará roaming dos arquivos de assinatura do Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="772f8-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="772f8-136">No entanto, as opções de assinatura padrão para novas mensagens e respostas ou encaminhamentos não são sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="772f8-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="772f8-137">Essas duas configurações são armazenadas no perfil do Outlook, do qual a UE-V não faz roaming.</span><span class="sxs-lookup"><span data-stu-id="772f8-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="772f8-138">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="772f8-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="772f8-139">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="772f8-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="772f8-140">Recomendamos que você instale a versão de 64 bits do Microsoft Office para computadores modernos.</span><span class="sxs-lookup"><span data-stu-id="772f8-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="772f8-141">Para determinar qual versão você precisa, [clique aqui](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="772f8-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="772f8-142">O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office.</span><span class="sxs-lookup"><span data-stu-id="772f8-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="772f8-143">Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="772f8-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="772f8-144">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="772f8-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="772f8-145">**Solução alternativa:** Nenhuma</span><span class="sxs-lookup"><span data-stu-id="772f8-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="772f8-146">Os MSI não estão localizados</span><span class="sxs-lookup"><span data-stu-id="772f8-146">MSI’s are not localized</span></span>

<span data-ttu-id="772f8-147">O UE-V 2,0 inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="772f8-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="772f8-148">Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês.</span><span class="sxs-lookup"><span data-stu-id="772f8-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="772f8-149">Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="772f8-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="772f8-150">**Solução alternativa:** Nenhuma</span><span class="sxs-lookup"><span data-stu-id="772f8-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="772f8-151">Favicons associados ao Internet Explorer 9 favoritos não fazem roaming</span><span class="sxs-lookup"><span data-stu-id="772f8-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="772f8-152">Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.</span><span class="sxs-lookup"><span data-stu-id="772f8-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="772f8-153">**Solução alternativa:** O favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado em cache no navegador Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="772f8-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="772f8-154">Caminhos de configurações de arquivo são armazenados no registro</span><span class="sxs-lookup"><span data-stu-id="772f8-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="772f8-155">Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro.</span><span class="sxs-lookup"><span data-stu-id="772f8-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="772f8-156">Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.</span><span class="sxs-lookup"><span data-stu-id="772f8-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="772f8-157">**Solução alternativa:** Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.</span><span class="sxs-lookup"><span data-stu-id="772f8-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="772f8-158">Caminhos de armazenamento de configurações longos podem causar um erro</span><span class="sxs-lookup"><span data-stu-id="772f8-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="772f8-159">Mantenha as configurações dos caminhos de armazenamento o mais breve possível.</span><span class="sxs-lookup"><span data-stu-id="772f8-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="772f8-160">Caminhos longos podem impedir a resolução ou a sincronização.</span><span class="sxs-lookup"><span data-stu-id="772f8-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="772f8-161">O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações.</span><span class="sxs-lookup"><span data-stu-id="772f8-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="772f8-162">Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="772f8-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="772f8-163">Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:</span><span class="sxs-lookup"><span data-stu-id="772f8-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="772f8-164">Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="772f8-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="772f8-165">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="772f8-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="772f8-166">Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="772f8-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="772f8-167">As configurações do sistema operacional para o narrador e caracteres monetários específicos para o local (por exemplo, configurações de idioma e regionais) só serão transferidas para versões de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="772f8-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="772f8-168">Por exemplo, os caracteres monetários não serão movidos entre o Windows 7 e o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="772f8-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="772f8-169">**Solução alternativa:** Nenhuma</span><span class="sxs-lookup"><span data-stu-id="772f8-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="772f8-170">Os aplicativos do Windows 8 não sincronizam as configurações quando o aplicativo é reiniciado após fechar inesperadamente</span><span class="sxs-lookup"><span data-stu-id="772f8-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="772f8-171">Se um aplicativo do Windows 8 for fechado inesperadamente logo após a inicialização, as configurações do aplicativo poderão não ser sincronizadas quando o aplicativo for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="772f8-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="772f8-172">**Solução alternativa:** Feche o aplicativo do Windows 8, feche e reinicie o aplicativo UevAppMonitor.exe (pode usar o TaskManager) e reinicie o aplicativo do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="772f8-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="772f8-173">O agente do UE-V 1 gera erros ao executar modelos do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="772f8-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="772f8-174">Se um modelo de local de configurações do UE-V 2 for distribuído para um computador instalado com um agente UE-V 1, algumas configurações falharão na sincronização entre computadores e o agente reportará erros no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="772f8-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="772f8-175">**Solução alternativa:** Ao migrar do UE-V 1 para o UE-V 2 e é provável que você tenha computadores executando a versão anterior do agente, crie um catálogo do UE-V 2,0 separado para dar suporte ao UE-V 2,0 Agent e aos modelos.</span><span class="sxs-lookup"><span data-stu-id="772f8-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="772f8-176">Hotfixes e artigos da base de dados de conhecimento para UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="772f8-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="772f8-177">Esta seção contém hotfixes e artigos da KB para o UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="772f8-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="772f8-178">Artigo do KB</span><span class="sxs-lookup"><span data-stu-id="772f8-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="772f8-179">Title</span><span class="sxs-lookup"><span data-stu-id="772f8-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="772f8-180">Link</span><span class="sxs-lookup"><span data-stu-id="772f8-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-181">2927019</span><span class="sxs-lookup"><span data-stu-id="772f8-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-182">Pacote de hotfix 1 para Microsoft User Experience Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="772f8-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="772f8-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="772f8-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-184">2903501</span><span class="sxs-lookup"><span data-stu-id="772f8-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-185">UE-V: compatibilidade com o User Experience Virtualization (UE-V) com perfis de usuário</span><span class="sxs-lookup"><span data-stu-id="772f8-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="772f8-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-187">2770042</span><span class="sxs-lookup"><span data-stu-id="772f8-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-188">Configurações do UE-V Registry</span><span class="sxs-lookup"><span data-stu-id="772f8-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="772f8-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-190">2847017</span><span class="sxs-lookup"><span data-stu-id="772f8-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-191">Configurações do UE-V replicadas pelo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="772f8-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="772f8-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-193">2930271</span><span class="sxs-lookup"><span data-stu-id="772f8-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-194">Noções básicas sobre as limitações de assinaturas do Outlook em roaming no Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="772f8-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="772f8-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-196">2769631</span><span class="sxs-lookup"><span data-stu-id="772f8-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-197">Como reparar uma instalação corrompida do UE-V</span><span class="sxs-lookup"><span data-stu-id="772f8-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="772f8-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-199">2850989</span><span class="sxs-lookup"><span data-stu-id="772f8-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-200">Não há suporte para a migração de perfis MAPI com o Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="772f8-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="772f8-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-202">2769586</span><span class="sxs-lookup"><span data-stu-id="772f8-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-203">O UE-V transfere pastas vazias e chaves do registro</span><span class="sxs-lookup"><span data-stu-id="772f8-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="772f8-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-205">2782997</span><span class="sxs-lookup"><span data-stu-id="772f8-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-206">Como habilitar o log de depuração na Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="772f8-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="772f8-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-208">2769570</span><span class="sxs-lookup"><span data-stu-id="772f8-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-209">O UE-V não atualiza o tema nas sessões do RDS ou da VDI</span><span class="sxs-lookup"><span data-stu-id="772f8-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="772f8-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-211">2901856</span><span class="sxs-lookup"><span data-stu-id="772f8-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-212">As configurações do aplicativo não sincronizam após você forçar uma reinicialização em um computador habilitado para UE-V</span><span class="sxs-lookup"><span data-stu-id="772f8-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="772f8-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-214">2850582</span><span class="sxs-lookup"><span data-stu-id="772f8-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-215">Como usar a virtualização da experiência do usuário da Microsoft com aplicativos App-V</span><span class="sxs-lookup"><span data-stu-id="772f8-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="772f8-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="772f8-217">3041879</span><span class="sxs-lookup"><span data-stu-id="772f8-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-218">Versões de arquivo atuais para a virtualização da experiência do usuário da Microsoft</span><span class="sxs-lookup"><span data-stu-id="772f8-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="772f8-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="772f8-220">2843592</span><span class="sxs-lookup"><span data-stu-id="772f8-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="772f8-221">Informações sobre a virtualização da experiência do usuário e alta disponibilidade</span><span class="sxs-lookup"><span data-stu-id="772f8-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="772f8-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="772f8-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





