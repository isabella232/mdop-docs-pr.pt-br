---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796011"
---
# <span data-ttu-id="6f5b2-103">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="6f5b2-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="6f5b2-104">Para pesquisar as notas de versão do Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="6f5b2-105">Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="6f5b2-106">As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="6f5b2-107">Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="6f5b2-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="6f5b2-109">Problemas conhecidos do UE-V</span><span class="sxs-lookup"><span data-stu-id="6f5b2-109">UE-V known issues</span></span>


<span data-ttu-id="6f5b2-110">Esta seção contém notas de versão para o User Experience Virtualization 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="6f5b2-111">As configurações do registro falham na sincronização entre aplicativos nativos e App-V no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="6f5b2-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="6f5b2-112">Quando um computador tem um aplicativo que está disponível por meio do aplicativo virtualização do aplicativo (App-V) e um aplicativo de instalação original instalado com um Windows Installer (. msi File), as configurações baseadas no registro não são sincronizadas entre as tecnologias.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="6f5b2-113">SOLUÇÃO alternativa: para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="6f5b2-114">A configuração do Windows 8 falha na sincronização quando o compartilhamento de rede está fora do domínio do usuário</span><span class="sxs-lookup"><span data-stu-id="6f5b2-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="6f5b2-115">Quando o Windows® 8 tenta a sincronização das configurações do sistema operacional, o synchrnization falha com a seguinte mensagem de erro: **Boost:: FileSystem:: Exists:: nome de usuário ou senha incorreto**.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="6f5b2-116">Esse erro pode indicar que o compartilhamento de rede está fora do domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="6f5b2-117">Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="6f5b2-118">Os compartilhamentos de rede usados para as configurações de UE-V armazenam locais de armazenamento devem residir no mesmo domínio do Active Directory que o usuário.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="6f5b2-119">SOLUÇÃO alternativa: Use compartilhamentos de rede do mesmo domínio do Active Directory que o usuário.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="6f5b2-120">.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-120">.</span></span>

### <span data-ttu-id="6f5b2-121">Roaming de assinatura de email do Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="6f5b2-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="6f5b2-122">O UE-V fará roaming dos arquivos de assinatura do Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="6f5b2-123">No entanto, as opções de assinatura padrão para novas mensagens e respostas/encaminhamentos não são móveis.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="6f5b2-124">Essas duas configurações são armazenadas no perfil do Outlook, do qual a UE-V não faz roaming.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="6f5b2-125">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="6f5b2-126">As configurações de sincronização não são sincronizadas no intervalo esperado durante a execução no modo de link lento</span><span class="sxs-lookup"><span data-stu-id="6f5b2-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="6f5b2-127">Em condições normais, as configurações locais de armazenamento devem estar disponíveis em uma conexão de rede de link rápido.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="6f5b2-128">No modo de link lento, a sincronização ocorrerá periodicamente periodicamente.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="6f5b2-129">Por padrão, o cronograma de sincronização do modo de link lento é definido para cada 360 minutos.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="6f5b2-130">SOLUÇÃO alternativa: para alterar a frequência da sincronização em segundo plano para computadores no modo de vínculo lento, você pode configurar a política de sincronização em segundo plano para **arquivos offline**.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="6f5b2-131">Os caracteres especiais não são sincronizados</span><span class="sxs-lookup"><span data-stu-id="6f5b2-131">Special characters do not synchronize</span></span>

<span data-ttu-id="6f5b2-132">Certos caracteres, como símbolos de moeda, não são sincronizados entre computadores com o Windows 7 e o Windows 8 que executam o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="6f5b2-133">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="6f5b2-134">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6f5b2-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="6f5b2-135">Recomendamos que você instale a versão de 32 bits do Microsoft Office para sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="6f5b2-136">Para escolher a versão do Microsoft Office que você precisa, clique aqui ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="6f5b2-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="6f5b2-137">O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="6f5b2-138">Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="6f5b2-139">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="6f5b2-140">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="6f5b2-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="6f5b2-141">Os MSI não estão localizados</span><span class="sxs-lookup"><span data-stu-id="6f5b2-141">MSI’s are not localized</span></span>

<span data-ttu-id="6f5b2-142">O UE-V 1,0 SP1 inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="6f5b2-143">Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="6f5b2-144">Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="6f5b2-145">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="6f5b2-145">WORKAROUND: None</span></span>

### <span data-ttu-id="6f5b2-146">Outras pastas do compartilhamento com o local de armazenamento de configuração não estão disponíveis no modo de conexão lenta</span><span class="sxs-lookup"><span data-stu-id="6f5b2-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="6f5b2-147">Os compartilhamentos de repositório de configurações não devem estar localizados em um compartilhamento de rede que é usado para outras pastas que sempre devem estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="6f5b2-148">Quando o compartilhamento de rede que hospeda a configuração local de armazenamento entrar em modo de conexão lenta, a única pasta disponível será a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="6f5b2-149">Outras pastas no compartilhamento não estão disponíveis no modo de conexão lenta.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="6f5b2-150">Solução alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="6f5b2-150">Workaround: None</span></span>

### <span data-ttu-id="6f5b2-151">Favicons associados ao Internet Explorer 9 favoritos não fazem roaming</span><span class="sxs-lookup"><span data-stu-id="6f5b2-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="6f5b2-152">Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="6f5b2-153">SOLUÇÃO alternativa: o favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado no navegador do Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="6f5b2-154">Caminhos de configurações de arquivo são armazenados no registro</span><span class="sxs-lookup"><span data-stu-id="6f5b2-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="6f5b2-155">Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="6f5b2-156">Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="6f5b2-157">SOLUÇÃO alternativa: Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="6f5b2-158">Caminhos de armazenamento de configurações longos podem causar um erro</span><span class="sxs-lookup"><span data-stu-id="6f5b2-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="6f5b2-159">Mantenha as configurações dos caminhos de armazenamento o mais breve possível.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="6f5b2-160">Caminhos longos podem impedir a resolução ou a sincronização.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="6f5b2-161">O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="6f5b2-162">Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo).</span><span class="sxs-lookup"><span data-stu-id="6f5b2-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="6f5b2-163">Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:</span><span class="sxs-lookup"><span data-stu-id="6f5b2-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="6f5b2-164">Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="6f5b2-165">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="6f5b2-166">O UE-V Agent atrasa após logoff ou logon</span><span class="sxs-lookup"><span data-stu-id="6f5b2-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="6f5b2-167">Se ocorrer um logon ou logout antes que os arquivos offline determinem que um link lento está em vigor, o logout ou o logon podem ser adiados.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="6f5b2-168">O recurso arquivos offline pode levar até três minutos para detectar o estado atual da rede.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="6f5b2-169">Se o logon ou o desligamento ocorrer antes de os arquivos offline determinarem que o computador está conectado a um link lento, o pacote de configurações do UE-V será enviado ao servidor em vez do cache local.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="6f5b2-170">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="6f5b2-171">As configurações estão em conflito ao tentar fazer roaming das configurações do sistema operacional no Windows 8</span><span class="sxs-lookup"><span data-stu-id="6f5b2-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="6f5b2-172">No Windows 8 se a sincronização da conta da Microsoft estiver habilitada juntamente com o UE-V para configurações do sistema operacional, as configurações aplicadas podem ser inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="6f5b2-173">SOLUÇÃO alternativa: siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="6f5b2-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="6f5b2-174">Desabilitar a sincronização de conta da Microsoft se você estiver usando o UE-V para fazer roaming das configurações do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6f5b2-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="6f5b2-175">Desabilitar o UE-V para configurações do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6f5b2-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="6f5b2-176">Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6f5b2-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="6f5b2-177">As configurações do sistema operacional para o narrador e caracteres monetários específicos para a localidade só serão transferidas para versões de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="6f5b2-178">Por exemplo, os caracteres de moeda só serão movidos do Windows 7 para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="6f5b2-179">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="6f5b2-179">WORKAROUND: None</span></span>

 

 





