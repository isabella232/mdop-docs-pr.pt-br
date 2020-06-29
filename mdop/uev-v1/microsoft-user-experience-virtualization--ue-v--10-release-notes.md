---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 da Microsoft
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796012"
---
# <span data-ttu-id="62d73-103">Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="62d73-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="62d73-104">Para pesquisar notas de versão do Microsoft User Experience Virtualization (UE-V), pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="62d73-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="62d73-105">Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="62d73-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="62d73-106">As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="62d73-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="62d73-107">Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="62d73-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="62d73-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="62d73-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="62d73-109">Fornecendo comentários</span><span class="sxs-lookup"><span data-stu-id="62d73-109">Providing feedback</span></span>


<span data-ttu-id="62d73-110">Diga-nos o que você acha da nossa documentação do MDOP, enviando-nos seus comentários e comentários.</span><span class="sxs-lookup"><span data-stu-id="62d73-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="62d73-111">Envie seus comentários sobre a documentação para [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="62d73-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="62d73-112">Problemas conhecidos do UE-V</span><span class="sxs-lookup"><span data-stu-id="62d73-112">UE-V known issues</span></span>


<span data-ttu-id="62d73-113">Esta seção contém notas de versão para a virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="62d73-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="62d73-114">As configurações do registro falham na sincronização entre aplicativos nativos e App-V no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="62d73-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="62d73-115">Quando um computador tem um aplicativo que está disponível por meio do aplicativo virtualização do aplicativo (App-V) e um aplicativo de instalação original (instalado com um arquivo. msi), as configurações baseadas no registro não são sincronizadas entre as tecnologias.</span><span class="sxs-lookup"><span data-stu-id="62d73-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="62d73-116">SOLUÇÃO alternativa: para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.</span><span class="sxs-lookup"><span data-stu-id="62d73-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="62d73-117">A configuração do Windows 8 falha na sincronização com o erro: "Boost:: FileSystem:: existe:: nome de usuário ou senha incorreto"</span><span class="sxs-lookup"><span data-stu-id="62d73-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="62d73-118">A sincronização das configurações do sistema operacional Windows® 8 falha com a seguinte mensagem de erro: **Boost:: FileSystem:: existe:: nome de usuário ou senha incorreto**.</span><span class="sxs-lookup"><span data-stu-id="62d73-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="62d73-119">Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="62d73-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="62d73-120">Os compartilhamentos de rede usados para as configurações de UE-V armazenam locais de armazenamento devem residir no mesmo domínio do Active Directory que o usuário.</span><span class="sxs-lookup"><span data-stu-id="62d73-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="62d73-121">Caso contrário, pode ocorrer o seguinte erro: "nome de usuário ou senha incorretos".</span><span class="sxs-lookup"><span data-stu-id="62d73-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="62d73-122">SOLUÇÃO alternativa: Use compartilhamentos de rede do mesmo domínio do Active Directory que o usuário.</span><span class="sxs-lookup"><span data-stu-id="62d73-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="62d73-123">.</span><span class="sxs-lookup"><span data-stu-id="62d73-123">.</span></span>

### <span data-ttu-id="62d73-124">Roaming de assinatura de email do Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="62d73-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="62d73-125">O UE-V fará roaming dos arquivos de assinatura do Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="62d73-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="62d73-126">No entanto, as opções de assinatura padrão para novas mensagens e respostas/encaminhamentos não são.</span><span class="sxs-lookup"><span data-stu-id="62d73-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="62d73-127">Essas duas configurações são armazenadas no perfil do Outlook, que a UE-Vdoes não faz roaming.</span><span class="sxs-lookup"><span data-stu-id="62d73-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="62d73-128">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="62d73-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="62d73-129">As configurações de sincronização não são sincronizadas no intervalo esperado durante a execução no modo de link lento</span><span class="sxs-lookup"><span data-stu-id="62d73-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="62d73-130">Em condições normais, as configurações locais de armazenamento devem estar disponíveis em uma conexão de rede de link rápido.</span><span class="sxs-lookup"><span data-stu-id="62d73-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="62d73-131">No modo de link lento, a sincronização ocorrerá periodicamente periodicamente.</span><span class="sxs-lookup"><span data-stu-id="62d73-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="62d73-132">Por padrão, o cronograma de sincronização do modo de link lento é definido para cada 360 minutos.</span><span class="sxs-lookup"><span data-stu-id="62d73-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="62d73-133">SOLUÇÃO alternativa: para alterar a frequência da sincronização em segundo plano para computadores no modo de vínculo lento, você pode configurar a política de sincronização em segundo plano para **arquivos offline**.</span><span class="sxs-lookup"><span data-stu-id="62d73-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="62d73-134">Os caracteres especiais não são sincronizados</span><span class="sxs-lookup"><span data-stu-id="62d73-134">Special characters do not synchronize</span></span>

<span data-ttu-id="62d73-135">Certos caracteres, como símbolos de moeda, não são sincronizados entre computadores com o Windows 7 e o Windows 8 que executam o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="62d73-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="62d73-136">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="62d73-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="62d73-137">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="62d73-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="62d73-138">Recomendamos que você instale a versão de 32 bits do Microsoft Office para sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="62d73-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="62d73-139">Para escolher a versão do Microsoft Office que você precisa, clique aqui.</span><span class="sxs-lookup"><span data-stu-id="62d73-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="62d73-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="62d73-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="62d73-141">O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office.</span><span class="sxs-lookup"><span data-stu-id="62d73-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="62d73-142">Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="62d73-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="62d73-143">O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="62d73-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="62d73-144">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="62d73-144">WORKAROUND: None</span></span>

### <span data-ttu-id="62d73-145">Outras pastas do compartilhamento com o local de armazenamento de configuração não estão disponíveis no modo de conexão lenta</span><span class="sxs-lookup"><span data-stu-id="62d73-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="62d73-146">Os compartilhamentos de repositório de configurações não devem estar localizados em um compartilhamento de rede que é usado para outras pastas que sempre devem estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="62d73-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="62d73-147">Quando o compartilhamento de rede que hospeda a configuração local de armazenamento entrar em modo de conexão lenta, a única pasta disponível será a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="62d73-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="62d73-148">Outras pastas no compartilhamento não estão disponíveis no modo de conexão lenta.</span><span class="sxs-lookup"><span data-stu-id="62d73-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="62d73-149">Solução alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="62d73-149">Workaround: None</span></span>

### <span data-ttu-id="62d73-150">Favicons associados ao Internet Explorer 9 favoritos não fazem roaming</span><span class="sxs-lookup"><span data-stu-id="62d73-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="62d73-151">Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.</span><span class="sxs-lookup"><span data-stu-id="62d73-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="62d73-152">SOLUÇÃO alternativa: o favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado no navegador do Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="62d73-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="62d73-153">Caminhos de configurações de arquivo são armazenados no registro</span><span class="sxs-lookup"><span data-stu-id="62d73-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="62d73-154">Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro.</span><span class="sxs-lookup"><span data-stu-id="62d73-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="62d73-155">Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.</span><span class="sxs-lookup"><span data-stu-id="62d73-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="62d73-156">SOLUÇÃO alternativa: Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.</span><span class="sxs-lookup"><span data-stu-id="62d73-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="62d73-157">Não há suporte para caminhos com mais de 260 caracteres</span><span class="sxs-lookup"><span data-stu-id="62d73-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="62d73-158">Não há suporte para configurações de caminhos de armazenamento com mais de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="62d73-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="62d73-159">Copiar os pacotes de configurações do UE-V para configurações caminhos de armazenamento com mais de 260 caracteres falharão e gerará a seguinte mensagem de exceção no log de eventos operacional do UE-V: **\ [Boost:: FileSystem:: Copy \ _file: o sistema não pode encontrar o caminho especificado \]**.</span><span class="sxs-lookup"><span data-stu-id="62d73-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="62d73-160">Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="62d73-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="62d73-161">Não há suporte para caminhos de configurações de arquivo que tenham mais de 260 caracteres no momento.</span><span class="sxs-lookup"><span data-stu-id="62d73-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="62d73-162">As configurações de arquivo referenciadas nos modelos de local de configurações do UE-V não podem estar localizadas em um caminho de diretório que tenha mais de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="62d73-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="62d73-163">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="62d73-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="62d73-164">O UE-V Agent atrasa após logoff ou logon</span><span class="sxs-lookup"><span data-stu-id="62d73-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="62d73-165">Se ocorrer um logon ou logout antes que os arquivos offline determinem que um link lento está em vigor, o logout ou o logon podem ser adiados.</span><span class="sxs-lookup"><span data-stu-id="62d73-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="62d73-166">O recurso arquivos offline pode levar até três minutos para detectar o estado atual da rede.</span><span class="sxs-lookup"><span data-stu-id="62d73-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="62d73-167">Se o logon ou o desligamento ocorrer antes de os arquivos offline determinarem que o computador está conectado a um link lento, o pacote de configurações do UE-V será enviado ao servidor em vez do cache local.</span><span class="sxs-lookup"><span data-stu-id="62d73-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="62d73-168">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="62d73-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="62d73-169">As configurações estão em conflito ao tentar fazer roaming das configurações do sistema operacional no Windows 8</span><span class="sxs-lookup"><span data-stu-id="62d73-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="62d73-170">No Windows 8 se a sincronização da conta da Microsoft estiver habilitada juntamente com o UE-V para configurações do sistema operacional, as configurações aplicadas podem ser inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="62d73-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="62d73-171">SOLUÇÃO alternativa: siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="62d73-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="62d73-172">Desabilitar a sincronização de conta da Microsoft se você estiver usando o UE-V para fazer roaming das configurações do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="62d73-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="62d73-173">Desabilitar o UE-V para configurações do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="62d73-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="62d73-174">Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="62d73-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="62d73-175">As configurações do sistema operacional para o narrador e caracteres monetários específicos para a localidade só serão transferidas para versões de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="62d73-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="62d73-176">Por exemplo, os caracteres de moeda só serão movidos do Windows 7 para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62d73-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="62d73-177">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="62d73-177">WORKAROUND: None</span></span>

### <span data-ttu-id="62d73-178">Os indicadores do Internet Explorer não aparecem no Internet Explorer SmartBar</span><span class="sxs-lookup"><span data-stu-id="62d73-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="62d73-179">Quando os indicadores do Internet Explorer são movidos de um computador para outro, o índice no segundo computador não pode ser atualizado, portanto, ao digitar na barra de endereços, o favorito não aparece como um resultado de pesquisa possível no computador 2.</span><span class="sxs-lookup"><span data-stu-id="62d73-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="62d73-180">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="62d73-180">WORKAROUND: None</span></span>

 

 





