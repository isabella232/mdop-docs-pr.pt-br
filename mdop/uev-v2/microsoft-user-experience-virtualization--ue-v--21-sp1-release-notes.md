---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft
author: dansimp
ms.assetid: 561988c4-cc5c-4e15-970b-16e942c8f2ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/30/2017
ms.openlocfilehash: 974914421c61c829b5a32e336bddf8ea1addf514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799691"
---
# <span data-ttu-id="d615c-103">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="d615c-103">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>


<span data-ttu-id="d615c-104">Para pesquisar as notas de versão do Microsoft User Experience Virtualization 2,1 SP1, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="d615c-104">To search Microsoft User Experience Virtualization 2.1 SP1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d615c-105">Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="d615c-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="d615c-106">As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="d615c-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="d615c-107">Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="d615c-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d615c-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="d615c-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d615c-109">Fornecendo comentários</span><span class="sxs-lookup"><span data-stu-id="d615c-109">Providing feedback</span></span>


<span data-ttu-id="d615c-110">Diga-nos o que você acha da nossa documentação do MDOP, enviando-nos seus comentários e comentários.</span><span class="sxs-lookup"><span data-stu-id="d615c-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="d615c-111">Envie seus comentários sobre a documentação para [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="d615c-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="d615c-112">Problemas conhecidos do UE-V</span><span class="sxs-lookup"><span data-stu-id="d615c-112">UE-V known issues</span></span>


<span data-ttu-id="d615c-113">Esta seção contém notas de versão para o User Experience Virtualization 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="d615c-113">This section contains release notes for User Experience Virtualization 2.1 SP1.</span></span>

### <span data-ttu-id="d615c-114">Modelos de local das configurações do UE-V para o Skype causa falha no Skype</span><span class="sxs-lookup"><span data-stu-id="d615c-114">UE-V settings location templates for Skype cause Skype to crash</span></span>

<span data-ttu-id="d615c-115">Quando um usuário gera um modelo de local de configurações válido para o aplicativo da área de trabalho do Skype, registra-o e, em seguida, inicia o aplicativo da área de trabalho do Skype, o Skype falha.</span><span class="sxs-lookup"><span data-stu-id="d615c-115">When a user generates a valid settings location template for the Skype desktop application, registers it, and then launches the Skype desktop application, Skype crashes.</span></span> <span data-ttu-id="d615c-116">Um _VIOLATION de acesso é registrado no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d615c-116">An ACCESS\_VIOLATION is recorded in the Application Event Log.</span></span>

<span data-ttu-id="d615c-117">SOLUÇÃO alternativa: remova ou cancele o registro do modelo do Skype para permitir que o Skype funcione novamente.</span><span class="sxs-lookup"><span data-stu-id="d615c-117">WORKAROUND: Remove or unregister the Skype template to allow Skype to work again.</span></span>

### <span data-ttu-id="d615c-118">Scripts existentes para instalações silenciosas do UE-V podem falhar</span><span class="sxs-lookup"><span data-stu-id="d615c-118">Existing scripts for silent installations of UE-V may fail</span></span>

<span data-ttu-id="d615c-119">Duas alterações feitas no UE-V Installer podem fazer com que scripts de instalação silenciosa que funcionavam para versões anteriores do UE-V falhem ao instalar o UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="d615c-119">Two changes made to the UE-V installer can cause silent installation scripts that worked for previous versions of UE-V to fail when installing UE-V 2.1 SP1.</span></span> <span data-ttu-id="d615c-120">O primeiro é um novo requisito para que os usuários aceitem os termos de licença e concordem ou recusem a participação no programa de aperfeiçoamento da experiência do usuário (CEIP), mesmo durante uma instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="d615c-120">The first is a new requirement that users must accept the license terms and agree to or decline participation in the Customer Experience Improvement Program (CEIP), even during a silent installation.</span></span> <span data-ttu-id="d615c-121">Usar o parâmetro/q não é mais suficiente para indicar a aceitação dos termos e do contrato de licença para participar do CEIP.</span><span class="sxs-lookup"><span data-stu-id="d615c-121">Using the /q parameter is no longer sufficient to indicate acceptance of the license terms and agreement to participate in CEIP.</span></span>

<span data-ttu-id="d615c-122">Em segundo lugar, o instalador agora força uma reinicialização do computador após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d615c-122">Second, the installer now forces a computer restart after installing the UE-V Agent.</span></span> <span data-ttu-id="d615c-123">Isso pode causar uma falha em um script de instalação se ele não estiver esperando a reinicialização (por exemplo, instalar primeiro o UE-V Agent e, em seguida, instalar imediatamente o gerador).</span><span class="sxs-lookup"><span data-stu-id="d615c-123">This can cause an install script to fail if it is not expecting the restart (for example, it installs the UE-V Agent first and then immediately installs the generator).</span></span>

<span data-ttu-id="d615c-124">SOLUÇÃO alternativa: o UE-V Installer (. msi) tem dois novos parâmetros de linha de comando que dão suporte a instalações silenciosas.</span><span class="sxs-lookup"><span data-stu-id="d615c-124">WORKAROUND: The UE-V installer (.msi) has two new command-line parameters that support silent installations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d615c-125">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d615c-125">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d615c-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="d615c-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d615c-127">/ACCEPTLICENSETERMS = true</span><span class="sxs-lookup"><span data-stu-id="d615c-127">/ACCEPTLICENSETERMS=True</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d615c-128">Defina esse parâmetro como <strong> true </strong> para instalar o UE-V silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="d615c-128">Set this parameter to <strong>True</strong> to install UE-V silently.</span></span> <span data-ttu-id="d615c-129">Adicionar esse parâmetro implica que o usuário aceite os termos de licença do UE-V, que são encontrados (por padrão) aqui:%ProgramFiles%\Microsoft User Experience Virtualization\Agent</span><span class="sxs-lookup"><span data-stu-id="d615c-129">Adding this parameter implies that the user accepts the UE-V license terms, which are found (by default) here: %ProgramFiles%\Microsoft User Experience Virtualization\Agent</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d615c-130">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="d615c-130">/NORESTART</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d615c-131">Esse parâmetro impede o reinício obrigatório após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d615c-131">This parameter prevents the mandatory restart after the UE-V agent is installed.</span></span> <span data-ttu-id="d615c-132">Um código de retorno de 3010 indica que uma reinicialização é necessária antes de usar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="d615c-132">A return code of 3010 indicates that a restart is required prior to using UE-V.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d615c-133">As configurações do registro não são sincronizadas entre aplicativos nativos e App-V no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="d615c-133">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="d615c-134">Quando um computador tem um aplicativo instalado por meio da virtualização de aplicativos (App-V) e localmente com um arquivo do Windows Installer (. msi), as configurações baseadas em registro não são sincronizadas entre as tecnologias.</span><span class="sxs-lookup"><span data-stu-id="d615c-134">When a computer has an application that is installed through both Application Virtualization (App-V) and locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="d615c-135">SOLUÇÃO alternativa: para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.</span><span class="sxs-lookup"><span data-stu-id="d615c-135">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="d615c-136">Resultados imprevisíveis com o Office 2010 e o Office 2013 instalados</span><span class="sxs-lookup"><span data-stu-id="d615c-136">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="d615c-137">Quando um usuário tem o Office 2010 e o Office 2013 instalados, todas as configurações comuns entre as duas versões do Office são móveis pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="d615c-137">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="d615c-138">Isso pode fazer com que o tamanho do pacote do Office 2010 seja muito grande ou resulte em conflitos imprevisíveis com o 2013, principalmente se o Office 365 for usado.</span><span class="sxs-lookup"><span data-stu-id="d615c-138">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="d615c-139">SOLUÇÃO alternativa: Instale apenas uma versão do Office ou limite quais configurações serão sincronizadas por UE-V.</span><span class="sxs-lookup"><span data-stu-id="d615c-139">WORKAROUND: Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="d615c-140">Desinstalar e reinstalar o aplicativo Windows 8 reverte as configurações para o estado inicial</span><span class="sxs-lookup"><span data-stu-id="d615c-140">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="d615c-141">Ao usar a sincronização de configurações do UE-V para um aplicativo do Windows 8, se o usuário desinstalar o aplicativo e reinstalar o aplicativo, as configurações do aplicativo retornarão aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="d615c-141">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="d615c-142">Isso acontece porque a desinstalação remove a cópia local (em cache) das configurações do aplicativo, mas não remove o pacote de configurações local do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d615c-142"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="d615c-143">Quando o aplicativo é reinstalado e iniciado, o UE-V coleta as configurações do aplicativo que foram redefinidas para os padrões do aplicativo e, em seguida, carrega as configurações padrão para o local de armazenamento central.</span><span class="sxs-lookup"><span data-stu-id="d615c-143"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="d615c-144">Outros computadores executando o aplicativo e, em seguida, baixar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="d615c-144"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="d615c-145">Esse comportamento é idêntico ao comportamento dos aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d615c-145"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="d615c-146">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="d615c-146">WORKAROUND: None.</span></span>

### <span data-ttu-id="d615c-147">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="d615c-147">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="d615c-148">Recomendamos que você instale a versão de 32 bits do Microsoft Office para sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d615c-148">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="d615c-149">Para escolher a versão do Microsoft Office que você precisa, clique aqui.</span><span class="sxs-lookup"><span data-stu-id="d615c-149">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="d615c-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="d615c-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="d615c-151">O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office.</span><span class="sxs-lookup"><span data-stu-id="d615c-151">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="d615c-152">Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d615c-152">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="d615c-153">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="d615c-153">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="d615c-154">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="d615c-154">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="d615c-155">Os MSI não estão localizados</span><span class="sxs-lookup"><span data-stu-id="d615c-155">MSI’s are not localized</span></span>

<span data-ttu-id="d615c-156">O UE-V inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="d615c-156">UE-V includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="d615c-157">Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês.</span><span class="sxs-lookup"><span data-stu-id="d615c-157">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="d615c-158">Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="d615c-158">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="d615c-159">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="d615c-159">WORKAROUND: None</span></span>

### <span data-ttu-id="d615c-160">Favicons associados ao Internet Explorer 9 favoritos não fazem roaming</span><span class="sxs-lookup"><span data-stu-id="d615c-160">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="d615c-161">Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.</span><span class="sxs-lookup"><span data-stu-id="d615c-161">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="d615c-162">SOLUÇÃO alternativa: o favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado no navegador do Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d615c-162">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="d615c-163">Caminhos de configurações de arquivo são armazenados no registro</span><span class="sxs-lookup"><span data-stu-id="d615c-163">File settings paths are stored in registry</span></span>

<span data-ttu-id="d615c-164">Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro.</span><span class="sxs-lookup"><span data-stu-id="d615c-164">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="d615c-165">Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.</span><span class="sxs-lookup"><span data-stu-id="d615c-165">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="d615c-166">SOLUÇÃO alternativa: Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.</span><span class="sxs-lookup"><span data-stu-id="d615c-166">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="d615c-167">Caminhos de armazenamento de configurações longos podem causar um erro</span><span class="sxs-lookup"><span data-stu-id="d615c-167">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="d615c-168">Mantenha as configurações dos caminhos de armazenamento o mais breve possível.</span><span class="sxs-lookup"><span data-stu-id="d615c-168">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="d615c-169">Caminhos longos podem impedir a resolução ou a sincronização.</span><span class="sxs-lookup"><span data-stu-id="d615c-169">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="d615c-170">O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações.</span><span class="sxs-lookup"><span data-stu-id="d615c-170">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="d615c-171">Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="d615c-171">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="d615c-172">Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:</span><span class="sxs-lookup"><span data-stu-id="d615c-172">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="d615c-173">Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="d615c-173">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="d615c-174">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="d615c-174">WORKAROUND: None.</span></span>

### <span data-ttu-id="d615c-175">Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d615c-175">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="d615c-176">As configurações do sistema operacional para o narrador e caracteres monetários específicos para o local (por exemplo, configurações de idioma e regionais) só serão transferidas para versões de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="d615c-176">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="d615c-177">Por exemplo, os caracteres monetários não serão movidos entre o Windows 7 e o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d615c-177">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="d615c-178">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="d615c-178">WORKAROUND: None</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="d615c-179">O agente do UE-V 1 gera erros ao executar modelos do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="d615c-179">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="d615c-180">Se um modelo de local de configurações do UE-V 2 for distribuído para um computador instalado com um agente UE-V 1, algumas configurações falharão na sincronização entre computadores e o agente reportará erros no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="d615c-180">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="d615c-181">SOLUÇÃO alternativa: ao migrar do UE-V 1 para o UE-V 2, é provável que você tenha computadores executando a versão anterior do agente, crie um catálogo do UE-V 2. x separado para dar suporte ao agente e modelos do UE-V 2. x.</span><span class="sxs-lookup"><span data-stu-id="d615c-181">WORKAROUND: When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.x catalog to support the UE-V 2.x Agent and templates.</span></span>

### <span data-ttu-id="d615c-182">Atraso de logoff do UE-V</span><span class="sxs-lookup"><span data-stu-id="d615c-182">UE-V logoff delay</span></span>

<span data-ttu-id="d615c-183">Ocasionalmente, no logoff, o UE-V leva muito tempo para sincronizar as configurações.</span><span class="sxs-lookup"><span data-stu-id="d615c-183">Occasionally on logoff, UE-V takes a long time to sync settings.</span></span> <span data-ttu-id="d615c-184">Geralmente, isso se deve a uma rede de alta latência ou uso incorreto do sistema de arquivos distrubuted (DFS).</span><span class="sxs-lookup"><span data-stu-id="d615c-184">Typically, this is due to a high latency network or incorrect use of Distrubuted File System (DFS).</span></span>
<span data-ttu-id="d615c-185">Para suporte a DFS, consulte a [declaração de suporte da Microsoft em torno de dados de perfil de usuário replicados](https://support.microsoft.com/kb/2533009) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="d615c-185">For DFS support, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://support.microsoft.com/kb/2533009) for further details.</span></span>

<span data-ttu-id="d615c-186">SOLUÇÃO alternativa: Iniciando com HF03, uma nova chave do registro foi introduzida a chave do registro a seguir fornece um mecanismo pelo qual o atraso de logoff máximo pode ser especificado \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span><span class="sxs-lookup"><span data-stu-id="d615c-186">WORKAROUND: Starting with HF03, a new registry key has been introduced The following registry key provides a mechanism by which the maximum logoff delay can be specified \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span></span>

<span data-ttu-id="d615c-187">Consulte [configurações do UE-V Registry](https://support.microsoft.com/kb/2770042) para obter mais detalhes</span><span class="sxs-lookup"><span data-stu-id="d615c-187">See [UE-V registry settings](https://support.microsoft.com/kb/2770042) for further details</span></span>

## <span data-ttu-id="d615c-188">Hotfixes e artigos da base de dados de conhecimento para UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="d615c-188">Hotfixes and Knowledge Base articles for UE-V 2.1 SP1</span></span>


<span data-ttu-id="d615c-189">Esta seção contém hotfixes e artigos da KB para o UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="d615c-189">This section contains hotfixes and KB articles for UE-V 2.1 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="d615c-190">Artigo do KB</span><span class="sxs-lookup"><span data-stu-id="d615c-190">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="d615c-191">Title</span><span class="sxs-lookup"><span data-stu-id="d615c-191">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="d615c-192">Link</span><span class="sxs-lookup"><span data-stu-id="d615c-192">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-193">3018608</span><span class="sxs-lookup"><span data-stu-id="d615c-193">3018608</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-194">UE-V 2,1-TemplateConsole.exe falha quando as classes do UE-V WMI estão ausentes</span><span class="sxs-lookup"><span data-stu-id="d615c-194">UE-V 2.1 - TemplateConsole.exe crashes when UE-V WMI classes are missing</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)"><span data-ttu-id="d615c-195">support.microsoft.com/kb/3018608/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-195">support.microsoft.com/kb/3018608/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-196">2903501</span><span class="sxs-lookup"><span data-stu-id="d615c-196">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-197">UE-V: compatibilidade com o User Experience Virtualization (UE-V) com perfis de usuário</span><span class="sxs-lookup"><span data-stu-id="d615c-197">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="d615c-198">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-198">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-199">2770042</span><span class="sxs-lookup"><span data-stu-id="d615c-199">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-200">Configurações do UE-V Registry</span><span class="sxs-lookup"><span data-stu-id="d615c-200">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="d615c-201">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-201">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-202">2847017</span><span class="sxs-lookup"><span data-stu-id="d615c-202">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-203">Configurações do UE-V replicadas pelo Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="d615c-203">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="d615c-204">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-204">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-205">2769631</span><span class="sxs-lookup"><span data-stu-id="d615c-205">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-206">Como reparar uma instalação corrompida do UE-V</span><span class="sxs-lookup"><span data-stu-id="d615c-206">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="d615c-207">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-207">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-208">2850989</span><span class="sxs-lookup"><span data-stu-id="d615c-208">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-209">Não há suporte para a migração de perfis MAPI com o Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="d615c-209">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="d615c-210">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-210">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-211">2769586</span><span class="sxs-lookup"><span data-stu-id="d615c-211">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-212">O UE-V transfere pastas vazias e chaves do registro</span><span class="sxs-lookup"><span data-stu-id="d615c-212">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="d615c-213">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-213">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-214">2782997</span><span class="sxs-lookup"><span data-stu-id="d615c-214">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-215">Como habilitar o log de depuração na Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="d615c-215">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="d615c-216">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-216">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-217">2769570</span><span class="sxs-lookup"><span data-stu-id="d615c-217">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-218">O UE-V não atualiza o tema nas sessões do RDS ou da VDI</span><span class="sxs-lookup"><span data-stu-id="d615c-218">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="d615c-219">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-219">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-220">2850582</span><span class="sxs-lookup"><span data-stu-id="d615c-220">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-221">Como usar a virtualização da experiência do usuário da Microsoft com aplicativos App-V</span><span class="sxs-lookup"><span data-stu-id="d615c-221">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="d615c-222">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-222">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d615c-223">3041879</span><span class="sxs-lookup"><span data-stu-id="d615c-223">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-224">Versões de arquivo atuais para a virtualização da experiência do usuário da Microsoft</span><span class="sxs-lookup"><span data-stu-id="d615c-224">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="d615c-225">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-225">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d615c-226">2843592</span><span class="sxs-lookup"><span data-stu-id="d615c-226">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="d615c-227">Informações sobre a virtualização da experiência do usuário e alta disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d615c-227">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="d615c-228">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="d615c-228">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 






 

 





