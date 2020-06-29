---
title: Notas de versão do App-V 5.0 SP2
description: Notas de versão do App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796222"
---
# <span data-ttu-id="92793-103">Notas de versão do App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="92793-103">Release Notes for App-V 5.0 SP2</span></span>


**<span data-ttu-id="92793-104">Para procurar um problema específico nestas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="92793-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="92793-105">Leia estas notas de versão cuidadosamente antes de instalar o App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="92793-105">Read these release notes thoroughly before you install App-V 5.0 SP2.</span></span>

<span data-ttu-id="92793-106">Estas notas da versão contêm informações necessárias para instalar com êxito o App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="92793-106">These release notes contain information that is required to successfully install App-V 5.0 SP2.</span></span> <span data-ttu-id="92793-107">As notas de versão também contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="92793-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="92793-108">Se houver diferenças entre essas notas de versão e outras documentações do App-V 5,0, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="92793-108">If there are differences between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="92793-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="92793-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="92793-110">Sobre a documentação do produto</span><span class="sxs-lookup"><span data-stu-id="92793-110">About the Product Documentation</span></span>


<span data-ttu-id="92793-111">Para obter informações sobre a documentação do App-V 5,0, consulte a home page do App-V 5,0 no Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="92793-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="92793-112">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="92793-112">Provide Feedback</span></span>


<span data-ttu-id="92793-113">Estamos interessados em seus comentários sobre o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="92793-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="92793-114">Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="92793-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="92793-115">**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras na nossa documentação e nas versões do produto.</span><span class="sxs-lookup"><span data-stu-id="92793-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="92793-116">Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="92793-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="92793-117">Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="92793-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="92793-118">Problemas conhecidos com o pacote de hotfix 4 para Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="92793-118">Known Issues with Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>


### <span data-ttu-id="92793-119">Os pacotes param de funcionar após a desinstalação do pacote de hotfix 4 para Application Virtualization 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="92793-119">Packages stop working after you uninstall Hotfix Package 4 for Application Virtualization 5.0 SP2</span></span>

<span data-ttu-id="92793-120">Pacotes publicados quando o pacote de hotfix 4 para Application Virtualization 5,0 SP2 é aplicado pare de funcionar quando o pacote de hotfix 4 para o Application Virtualization 5,0 SP2 é removido.</span><span class="sxs-lookup"><span data-stu-id="92793-120">Packages published when Hotfix Package 4 for Application Virtualization 5.0 SP2 is applied stop working when Hotfix Package 4 for Application Virtualization 5.0 SP2 is removed.</span></span>

<span data-ttu-id="92793-121">POSSÍVEIS</span><span class="sxs-lookup"><span data-stu-id="92793-121">WORKAROUND:</span></span>

<span data-ttu-id="92793-122">Se a seguinte pasta existir, você deverá excluí-la:</span><span class="sxs-lookup"><span data-stu-id="92793-122">If the following folder exists, then you must delete it:</span></span>

<span data-ttu-id="92793-123">**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Cliente**  \\  **VFS**  \\  \*\* &lt; ID &gt; do pacote\*\* para cada pacote publicado.</span><span class="sxs-lookup"><span data-stu-id="92793-123">**%localappdata%** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **VFS** \\ **&lt;package ID&gt;** for each package that was published.</span></span>

<span data-ttu-id="92793-124">**Observação**  Você deve ter privilégios elevados para excluir esta pasta.</span><span class="sxs-lookup"><span data-stu-id="92793-124">**Note** You must have elevated privileges to delete this folder.</span></span>

 

<span data-ttu-id="92793-125">Para usar um script, para cada conta de usuário no computador e para cada ID de pacote publicada após a instalação do pacote de hotfix 4 para o Application Virtualization 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="92793-125">To use a script, for each user account on the computer and for each package id that was published after installing Hotfix Package 4 for Application Virtualization 5.0 SP2:</span></span>

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   <span data-ttu-id="92793-126">Os atalhos permanecerão com as sessões de usuário mesmo após a exclusão da pasta do diretório na seção anterior, para que você possa clicar no atalho para executar o aplicativo novamente.</span><span class="sxs-lookup"><span data-stu-id="92793-126">The shortcuts will remain with the user sessions even after deleting the folder from the directory in the previous section, so you can click on the shortcut to run the application again.</span></span> <span data-ttu-id="92793-127">Não é necessário publicar o aplicativo novamente.</span><span class="sxs-lookup"><span data-stu-id="92793-127">There is no need to re-publish the application.</span></span>

-   <span data-ttu-id="92793-128">Esse problema ocorre para os dois usuários publicados no pacote e em pacotes publicados globalmente por exemplo, Microsoft Office2013.</span><span class="sxs-lookup"><span data-stu-id="92793-128">This issue happens for both user published packaged and globally published packages for example, Microsoft Office2013.</span></span> <span data-ttu-id="92793-129">A pasta deve ser excluída para ambos os tipos de pacotes.</span><span class="sxs-lookup"><span data-stu-id="92793-129">The folder must be deleted for both types of packages.</span></span>

-   <span data-ttu-id="92793-130">Você não precisa excluir a pasta VFS nos dados do aplicativo de roaming (**% AppData%**).</span><span class="sxs-lookup"><span data-stu-id="92793-130">You do not need to delete the VFS folder in the Roaming app data (**%appdata%**).</span></span> <span data-ttu-id="92793-131">Somente o **% LocalAppData%** deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="92793-131">Only the **%localappdata%** must be deleted.</span></span>

### <span data-ttu-id="92793-132">Pontos de integração do Microsoft Office com local de sistema de arquivos incorreto</span><span class="sxs-lookup"><span data-stu-id="92793-132">Microsoft Office integration points to wrong file system location</span></span>

<span data-ttu-id="92793-133">A integração do Microsoft Office aponta para um local incorreto do sistema de arquivos (Groove.exe mensagem de erro).</span><span class="sxs-lookup"><span data-stu-id="92793-133">Microsoft Office integration points to wrong file system location (Groove.exe error message).</span></span>

<span data-ttu-id="92793-134">POSSÍVEIS</span><span class="sxs-lookup"><span data-stu-id="92793-134">WORKAROUND:</span></span>

<span data-ttu-id="92793-135">Use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="92793-135">Use one of the following methods:</span></span>

1.  <span data-ttu-id="92793-136">Exclua o atalho na pasta inicialização após a atualização.</span><span class="sxs-lookup"><span data-stu-id="92793-136">Delete the shortcut in the start-up folder after upgrade.</span></span>

2.  <span data-ttu-id="92793-137">Altere o atalho na pasta inicialização usando um script.</span><span class="sxs-lookup"><span data-stu-id="92793-137">Change the shortcut in the start-up folder using a script.</span></span>

3.  <span data-ttu-id="92793-138">Use o arquivo de configuração de implantação para especificar o destino do atalho para a raiz de integração.</span><span class="sxs-lookup"><span data-stu-id="92793-138">Use the deployment configuration file to specify the shortcut target to the integration root.</span></span>

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> <span data-ttu-id="92793-139">Pacote de hotfix 4 para o Application Virtualization 5,0 o instalador do SP2 pode levar muito tempo</span><span class="sxs-lookup"><span data-stu-id="92793-139">Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can take a long time</span></span>

<span data-ttu-id="92793-140">O pacote de hotfix 4 para o instalador do SP2 do Application Virtualization 5,0 pode levar muito tempo, dependendo da quantidade de arquivos armazenados no cache do pacote existente.</span><span class="sxs-lookup"><span data-stu-id="92793-140">The Hotfix Package 4 for Application Virtualization 5.0 SP2 installer can potentially take a long time depending on how many files are stored in the existing package cache.</span></span>

<span data-ttu-id="92793-141">A atualização dos descritores de segurança do pacote associado durante o pacote de hotfix 4 para a instalação do Application Virtualization 5,0 SP2 tem um impacto significativo na duração da instalação.</span><span class="sxs-lookup"><span data-stu-id="92793-141">Updating associated package security descriptors during the Hotfix Package 4 for Application Virtualization 5.0 SP2 installation has a significant impact on how long it takes the installation will take.</span></span> <span data-ttu-id="92793-142">Anteriormente, a instalação da instalação era padrão em Duration.</span><span class="sxs-lookup"><span data-stu-id="92793-142">Previously, the installation install was standard in duration.</span></span> <span data-ttu-id="92793-143">No entanto, ele depende de quantos arquivos você fez no cache do pacote.</span><span class="sxs-lookup"><span data-stu-id="92793-143">However, it now depends on how many files you have staged in the package cache.</span></span>

<span data-ttu-id="92793-144">SOLUÇÃO alternativa: nenhum</span><span class="sxs-lookup"><span data-stu-id="92793-144">WORKAROUND: None</span></span>

### <span data-ttu-id="92793-145">Desinstalação do pacote de hotfix 4 para Application Virtualization 5,0 SP2 falha se o pacote do JIT-V estiver em uso</span><span class="sxs-lookup"><span data-stu-id="92793-145">Uninstalling Hotfix Package 4 for Application Virtualization 5.0 SP2 fails if JIT-V package is in use</span></span>

<span data-ttu-id="92793-146">Se você instalar o pacote de hotfix 4 para o Application Virtualization 5,0 SP2 e tentar desinstalar o hotfix quando a virtualização just-in-time (JIT-V) estiver sendo usada, a operação falhará se todas as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="92793-146">If you install Hotfix Package 4 for Application Virtualization 5.0 SP2 and then try to uninstall the hotfix when just-in-time virtualization (JIT-V) is being used, the operation will fail if all of the following conditions are true:</span></span>

-   <span data-ttu-id="92793-147">Você instalou usando um arquivo do Windows Installer (. msi) e, em seguida, aplica atualizações usando um arquivo de patch do instalador da Microsoft (. msp).</span><span class="sxs-lookup"><span data-stu-id="92793-147">You installed by using a Windows Installer file (.msi), and then you apply updates by using a Microsoft Installer Patch File (.msp).</span></span>

-   <span data-ttu-id="92793-148">Você tenta desinstalar uma atualização usando o item Adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="92793-148">You try to uninstall an update by using the Add or Remove Programs item in Control Panel.</span></span>

-   <span data-ttu-id="92793-149">Um pacote habilitado para JIT-V está em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="92793-149">A JIT-V-enabled package is running on the computer.</span></span>

<span data-ttu-id="92793-150">SOLUÇÃO alternativa: conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="92793-150">WORKAROUND: Complete the following steps:</span></span>

1.  <span data-ttu-id="92793-151">Abra o Windows PowerShell e execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="92793-151">Open Windows PowerShell and run the following commands:</span></span>

    -   **<span data-ttu-id="92793-152">Import-Module appvclient</span><span class="sxs-lookup"><span data-stu-id="92793-152">Import-module appvclient</span></span>**

    -   **<span data-ttu-id="92793-153">Get-AppvClientPackage | Parar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="92793-153">Get-AppvClientPackage | Stop-AppvClientPackage</span></span>**

2.  <span data-ttu-id="92793-154">Desinstale a atualização usando Adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="92793-154">Uninstall the update using Add or Remove Programs.</span></span>

## <span data-ttu-id="92793-155">Problemas conhecidos com o App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="92793-155">Known Issues with App-V 5.0 SP2</span></span>


### <a href="" id="bkmk-folderredirection"></a><span data-ttu-id="92793-156">O redirecionamento de pastas do cliente App-V também falha ao mover arquivos de% AppData% para% LocalAppData%</span><span class="sxs-lookup"><span data-stu-id="92793-156">App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%</span></span>

<span data-ttu-id="92793-157">Quando% AppData% é uma pasta de rede compartilhada que você configurou para o redirecionamento de pastas, as alterações que os usuários finais fazem em AppData (roaming) podem ser perdidas ao alternar entre computadores ou quando seus AppData locais são desmarcadas quando eles fazem logoff e logon novamente.</span><span class="sxs-lookup"><span data-stu-id="92793-157">When %AppData% is a shared network folder that you have configured for folder redirection, the changes that end users make to AppData (Roaming) can be lost when they switch computers or when their local AppData is cleared when they log off and then log back on.</span></span> <span data-ttu-id="92793-158">Esse erro ocorre porque a chave do registro (AppDatatime), que indica o último carregamento conhecido, fica fora da sincronização com os AppData armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="92793-158">This error occurs because the registry key (AppDataTime), which indicates the last known upload, gets out of synchronization with the local cached AppData.</span></span>

<span data-ttu-id="92793-159">SOLUÇÃO alternativa: exclua manualmente a seguinte chave do registro para cada pacote relevante quando um usuário final fizer logon ou logoff:</span><span class="sxs-lookup"><span data-stu-id="92793-159">WORKAROUND: Manually delete the following registry key for each relevant package when an end user logs on or off:</span></span>

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

<span data-ttu-id="92793-160">Na primeira vez que os usuários finais iniciarem um aplicativo no pacote depois de entrarem, o App-V força o download do% AppData% AppData%, mesmo se% LocalAppData% já estiver atualizado.</span><span class="sxs-lookup"><span data-stu-id="92793-160">The first time that end users start an application in the package after they log in, App-V forces a download of the zipped %AppData%, even if %LocalAppData% is already up to date.</span></span>

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> <span data-ttu-id="92793-161">App-V 5,0 Service Pack 2 (App-V 5,0 SP2) não inclui uma nova versão do App-V Server</span><span class="sxs-lookup"><span data-stu-id="92793-161">App-V 5.0 Service Pack 2 (App-V 5.0 SP2) does not include a new version of the App-V Server</span></span>

<span data-ttu-id="92793-162">O App-V 5.0 SP2 não inclui uma nova versão do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="92793-162">App-V 5.0SP2 does not include a new version of the App-V Server.</span></span> <span data-ttu-id="92793-163">Se você implanta clientes do App-V 5,0 SP2 executando o Windows 8,1 em seu ambiente e planeja gerenciar os clientes usando a infraestrutura do App-V, instale o [pacote de hotfix 2 para o Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span><span class="sxs-lookup"><span data-stu-id="92793-163">If you deploy App-V 5.0 SP2 clients running Windows 8.1 in your environment and plan to manage the clients using the App-V infrastructure, you must install [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634).</span></span> <span data-ttu-id="92793-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span><span class="sxs-lookup"><span data-stu-id="92793-164">(https://go.microsoft.com/fwlink/?LinkId=386634)</span></span>

<span data-ttu-id="92793-165">Se você estiver executando e Gerenciando clientes do App-V 5,0 SP2 usando qualquer um dos seguintes métodos, nenhuma atualização de cliente será necessária:</span><span class="sxs-lookup"><span data-stu-id="92793-165">If you are running and managing App-V 5.0 SP2 clients using any of the following methods no client update is required:</span></span>

-   <span data-ttu-id="92793-166">Modo autônomo.</span><span class="sxs-lookup"><span data-stu-id="92793-166">Standalone mode.</span></span>

-   <span data-ttu-id="92793-167">Gerenciador de Configurações.</span><span class="sxs-lookup"><span data-stu-id="92793-167">Configuration Manager.</span></span>

-   <span data-ttu-id="92793-168">ESD de terceiros.</span><span class="sxs-lookup"><span data-stu-id="92793-168">Third party ESD.</span></span>

<span data-ttu-id="92793-169">O cliente do App-V 5,0 SP2 é totalmente compatível com o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="92793-169">The App-V 5.0 SP2 client is fully compatible with Windows 8.1</span></span>

<span data-ttu-id="92793-170">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="92793-170">WORKAROUND: None.</span></span>

## <span data-ttu-id="92793-171">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="92793-171">Release Notes Copyright Information</span></span>


<span data-ttu-id="92793-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92793-172">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="92793-173">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="92793-173">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="92793-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92793-174">Related topics</span></span>


[<span data-ttu-id="92793-175">Sobre o App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="92793-175">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

 

 





