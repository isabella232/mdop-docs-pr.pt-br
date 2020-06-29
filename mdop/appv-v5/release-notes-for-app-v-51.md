---
title: Notas de versão do App-V 5.1
description: Notas de versão do App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796217"
---
# <span data-ttu-id="55556-103">Notas de versão do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="55556-103">Release Notes for App-V 5.1</span></span>


<span data-ttu-id="55556-104">Estes são problemas conhecidos do Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="55556-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.1.</span></span>

## <span data-ttu-id="55556-105">Erro durante a atualização de publicação entre o aplicativo de gerenciamento do App-V 5,0 e o cliente do App-V 5,1 no Windows 10</span><span class="sxs-lookup"><span data-stu-id="55556-105">Error occurs during publishing refresh between App-V 5.0 SP3 Management Server and App-V 5.1 Client on Windows 10</span></span>


<span data-ttu-id="55556-106">Um erro é gerado durante a atualização de publicação durante a sincronização de pacotes do servidor de gerenciamento do App-V 5,0 SP3 para um cliente do App-V 5,1 no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55556-106">An error is generated during publishing refresh when synchronizing packages from the App-V 5.0 SP3 management server to an App-V 5.1 client on Windows 10 .</span></span> <span data-ttu-id="55556-107">Esse erro ocorre porque o servidor do App-V 5,0 SP3 não compreende o sistema operacional Windows 10 especificado na URL de publicação.</span><span class="sxs-lookup"><span data-stu-id="55556-107">This error occurs because the App-V 5.0 SP3 server does not understand the Windows 10 operating system that is specified in the publishing URL.</span></span> <span data-ttu-id="55556-108">O problema foi corrigido para o servidor de publicação do App-V 5,1, mas não está reportado para versões do App-V 5,0 SP3 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="55556-108">The issue is fixed for App-V 5.1 publishing server, but is not backported to versions of App-V 5.0 SP3 or earlier.</span></span>

<span data-ttu-id="55556-109">**Solução alternativa**: Atualize o servidor de gerenciamento do App-v 5,0 para o servidor de gerenciamento do App-v 5,1 para clientes do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="55556-109">**Workaround**: Upgrade the App-V 5.0 Management server to the App-V 5.1 Management server for Windows 10 Clients.</span></span>

## <span data-ttu-id="55556-110">Configurações personalizadas não são aplicadas para pacotes que serão publicados globalmente se estiverem definidas usando o servidor do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="55556-110">Custom configurations do not get applied for packages that will be published globally if they are set using the App-V 5.1 Server</span></span>


<span data-ttu-id="55556-111">Se você atribuir um pacote a um grupo de anúncios que contém contas do computador e aplicar uma configuração personalizada ao grupo usando o App-V Server, a configuração personalizada não será aplicada a essas máquinas.</span><span class="sxs-lookup"><span data-stu-id="55556-111">If you assign a package to an AD group that contains machine accounts and apply a custom configuration to that group using the App-V Server, the custom configuration will not be applied to those machines.</span></span> <span data-ttu-id="55556-112">O cliente App-V 5,1 publicará pacotes atribuídos a uma conta de máquina globalmente.</span><span class="sxs-lookup"><span data-stu-id="55556-112">The App-V 5.1 Client will publish packages assigned to a machine account globally.</span></span> <span data-ttu-id="55556-113">No entanto, ele armazena arquivos de configuração personalizada por usuário em cada perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="55556-113">However, it stores custom configuration files per user in each user’s profile.</span></span> <span data-ttu-id="55556-114">Os pacotes publicados globalmente não terão acesso a essa configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="55556-114">Globally published packages will not have access to this custom configuration.</span></span>

<span data-ttu-id="55556-115">**Solução alternativa**: siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="55556-115">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="55556-116">Atribua o pacote a grupos que contenham apenas contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="55556-116">Assign the package to groups containing only user accounts.</span></span> <span data-ttu-id="55556-117">Isso garantirá que a configuração personalizada do pacote será armazenada no perfil de cada usuário e será aplicada corretamente.</span><span class="sxs-lookup"><span data-stu-id="55556-117">This will ensure that the package’s custom configuration will be stored in each user’s profile and will be applied correctly.</span></span>

-   <span data-ttu-id="55556-118">Crie um arquivo de configuração de implantação personalizado e aplique-o ao pacote no cliente usando o cmdlet Add-AppvClientPackage com o parâmetro – DynamicDeploymentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="55556-118">Create a custom deployment configuration file and apply it to the package on the client using the Add-AppvClientPackage cmdlet with the –DynamicDeploymentConfiguration parameter.</span></span> <span data-ttu-id="55556-119">Consulte [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="55556-119">See [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md) for more information.</span></span>

-   <span data-ttu-id="55556-120">Crie um novo pacote com a configuração personalizada usando o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="55556-120">Create a new package with the custom configuration using the App-V 5.1 Sequencer.</span></span>

## <span data-ttu-id="55556-121">Arquivos do servidor não excluídos após a instalação do novo App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="55556-121">Server files not deleted after new App-V 5.1 Server installation</span></span>


<span data-ttu-id="55556-122">Se você desinstalar o servidor App-V 5,0 SP1 e instalar o aplicativo App-V 5,1, a instalação falha, a versão errada do servidor de gerenciamento é instalada e uma mensagem de erro é retornada.</span><span class="sxs-lookup"><span data-stu-id="55556-122">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.1 Server, the installation fails, the wrong version of the Management server is installed, and an error message is returned.</span></span> <span data-ttu-id="55556-123">O problema ocorre porque os arquivos do servidor não estão sendo excluídos ao desinstalar o App-V 5,0 SP1, portanto, o processo de instalação faz uma atualização em vez de uma nova instalação.</span><span class="sxs-lookup"><span data-stu-id="55556-123">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the installation process does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="55556-124">**Solução alternativa**: exclua esta chave do registro antes de começar a instalar o App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="55556-124">**Workaround**: Delete this registry key before you start installing App-V 5.1:</span></span>

<span data-ttu-id="55556-125">Em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, localize e exclua a chave GUID de instalação que contém o valor DWORD "DisplayName" com dados de valor "Microsoft Application Virtualization (App-V) Server".</span><span class="sxs-lookup"><span data-stu-id="55556-125">Under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, locate and delete the installation GUID key that contains the DWORD value "DisplayName" with value data "Microsoft Application Virtualization (App-V) Server".</span></span> <span data-ttu-id="55556-126">Essa é a única tecla que deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="55556-126">This is the only key that should be deleted.</span></span>

## <span data-ttu-id="55556-127">Associações de tipo de arquivo adicionadas manualmente não são salvas corretamente</span><span class="sxs-lookup"><span data-stu-id="55556-127">File type associations added manually are not saved correctly</span></span>


<span data-ttu-id="55556-128">Associações de tipo de arquivo adicionadas manualmente a um pacote de aplicativo usando a guia atalhos e FTAs no final do assistente de atualização de aplicativos não são salvas corretamente.</span><span class="sxs-lookup"><span data-stu-id="55556-128">File type associations added to an application package manually using the Shortcuts and FTAs tab at the end of the application upgrade wizard are not saved correctly.</span></span> <span data-ttu-id="55556-129">Elas não estarão disponíveis para o cliente App-V ou para o sequenciador ao atualizar o pacote salvo novamente.</span><span class="sxs-lookup"><span data-stu-id="55556-129">They will not be available to the App-V Client or to the Sequencer when updating the saved package again.</span></span>

<span data-ttu-id="55556-130">**Solução alternativa**: para adicionar uma associação de tipo de arquivo, abra o pacote para modificação e execute o assistente de atualização.</span><span class="sxs-lookup"><span data-stu-id="55556-130">**Workaround**: To add a file type association, open the package for modification and run the update wizard.</span></span> <span data-ttu-id="55556-131">Durante a etapa de instalação, adicione a nova associação de tipo de arquivo pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="55556-131">During the Installation step, add the new file type association through the operating system.</span></span> <span data-ttu-id="55556-132">O sequenciador detectará a nova associação no registro do sistema e a adicionará ao registro virtual do pacote, onde ele estará disponível para o cliente.</span><span class="sxs-lookup"><span data-stu-id="55556-132">The sequencer will detect the new association in the system registry and add it to the package’s virtual registry, where it will be available to the client.</span></span>

## <span data-ttu-id="55556-133">Ao transmitir pacotes no modo de repositório de conteúdo compartilhado (SCS) para um cliente que também é gerenciado com o AppLocker, dados adicionais são gravados no disco local.</span><span class="sxs-lookup"><span data-stu-id="55556-133">When streaming packages in Shared Content Store (SCS) mode to a client that is also managed with AppLocker, additional data is written to the local disk.</span></span>


<span data-ttu-id="55556-134">Para reduzir a quantidade de dados gravados no disco local de um cliente, você pode habilitar o modo SCS no cliente do App-V 5,1 para transmitir o conteúdo de um pacote por demanda.</span><span class="sxs-lookup"><span data-stu-id="55556-134">To decrease the amount of data written to a client’s local disk, you can enable SCS mode on the App-V 5.1 Client to stream the contents of a package on demand.</span></span> <span data-ttu-id="55556-135">No entanto, se o AppLocker gerenciar um aplicativo dentro do pacote, alguns dados podem ser gravados no disco local do cliente que, de outra forma, não seriam gravados.</span><span class="sxs-lookup"><span data-stu-id="55556-135">However, if AppLocker manages an application within the package, some data might be written to the client’s local disk that would not otherwise be written.</span></span>

<span data-ttu-id="55556-136">**Solução alternativa**: nenhum</span><span class="sxs-lookup"><span data-stu-id="55556-136">**Workaround**: None</span></span>

## <span data-ttu-id="55556-137">Na caixa de diálogo Adicionar pacote ao console de gerenciamento, o botão procurar não está disponível ao usar o Chrome ou Firefox</span><span class="sxs-lookup"><span data-stu-id="55556-137">In the Management Console Add Package dialog box, the Browse button is not available when using Chrome or Firefox</span></span>


<span data-ttu-id="55556-138">Na página pacotes do console de gerenciamento, se você clicar em **Adicionar ou atualizar** no canto inferior direito, a caixa de diálogo **Adicionar pacote** será exibida.</span><span class="sxs-lookup"><span data-stu-id="55556-138">On the Packages page of the Management Console, if you click **Add or Upgrade** in the lower-right corner, the **Add Package** dialog box appears.</span></span> <span data-ttu-id="55556-139">Se você estiver acessando o console de gerenciamento usando o Chrome ou Firefox como navegador, não poderá navegar até o local do pacote.</span><span class="sxs-lookup"><span data-stu-id="55556-139">If you are accessing the Management Console using Chrome or Firefox as your browser, you will not be able to browse to the location of the package.</span></span>

<span data-ttu-id="55556-140">**Solução alternativa**: digite ou copie e cole o caminho do pacote no campo **Adicionar pacote** de entrada.</span><span class="sxs-lookup"><span data-stu-id="55556-140">**Workaround**: Type or copy and paste the path to the package into the **Add Package** input field.</span></span> <span data-ttu-id="55556-141">Se o console de gerenciamento tiver acesso a esse caminho, você poderá adicionar o pacote.</span><span class="sxs-lookup"><span data-stu-id="55556-141">If the Management Console has access to this path, you will be able to add the package.</span></span> <span data-ttu-id="55556-142">Se o pacote estiver em um compartilhamento de rede, você poderá navegar até o local usando o explorador de arquivos seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="55556-142">If the package is on a network share, you can browse to the location using File Explorer by doing these steps:</span></span>

1.  <span data-ttu-id="55556-143">Ao pressionar a **tecla Shift**, clique com o botão direito do mouse no arquivo do pacote</span><span class="sxs-lookup"><span data-stu-id="55556-143">While pressing **Shift**, right-click on the package file</span></span>

2.  <span data-ttu-id="55556-144">Selecione **Copiar como caminho**</span><span class="sxs-lookup"><span data-stu-id="55556-144">Select **Copy as path**</span></span>

3.  <span data-ttu-id="55556-145">Colar o caminho no campo de entrada da caixa de diálogo **Adicionar pacote**</span><span class="sxs-lookup"><span data-stu-id="55556-145">Paste the path into the **Add Package** dialog box input field</span></span>

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a><span data-ttu-id="55556-146">Atualizar o servidor de gerenciamento do App-V para 5,1 às vezes falha com a mensagem "ocorreu um erro de banco de dados"</span><span class="sxs-lookup"><span data-stu-id="55556-146">Upgrading App-V Management Server to 5.1 sometimes fails with the message “A database error occurred”</span></span>


<span data-ttu-id="55556-147">Se você instalar o servidor de gerenciamento do App-V 5,0 SP1 e, em seguida, tentar atualizar para o App-V 5,1 Server quando vários grupos de conexão estiverem configurados e habilitados, o seguinte erro será exibido: "ocorreu um erro de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="55556-147">If you install the App-V 5.0 SP1 Management Server, and then try to upgrade to App-V 5.1 Server when multiple connection groups are configured and enabled, the following error is displayed: “A database error occurred.</span></span> <span data-ttu-id="55556-148">Motivo: ' nome de coluna inválido ' PackageOptional '.</span><span class="sxs-lookup"><span data-stu-id="55556-148">Reason: 'Invalid column name 'PackageOptional'.</span></span> <span data-ttu-id="55556-149">Nome de coluna inválido ' VersionOptional '. "</span><span class="sxs-lookup"><span data-stu-id="55556-149">Invalid column name 'VersionOptional'.”</span></span>

<span data-ttu-id="55556-150">**Solução alternativa**: Execute este comando no seu banco de dados SQL:</span><span class="sxs-lookup"><span data-stu-id="55556-150">**Workaround**: Run this command on your SQL database:</span></span>

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

<span data-ttu-id="55556-151">onde "AppVManagement" é o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="55556-151">where “AppVManagement” is the name of the database.</span></span>

## <span data-ttu-id="55556-152">Os usuários não podem abrir um pacote em um grupo de conexão publicada pelo usuário se você adicionar ou remover um pacote opcional</span><span class="sxs-lookup"><span data-stu-id="55556-152">Users cannot open a package in a user-published connection group if you add or remove an optional package</span></span>


<span data-ttu-id="55556-153">Em ambientes que executam o cliente RDS ou que têm vários usuários simultâneos por computador, os usuários conectados não podem abrir aplicativos em pacotes que estejam em um grupo de conexão publicada pelo usuário se um pacote opcional for adicionado ou removido do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="55556-153">In environments that are running the RDS Client or that have multiple concurrent users per computer, logged-in users cannot open applications in packages that are in a user-published connection group if an optional package is added to or removed from the connection group.</span></span>

<span data-ttu-id="55556-154">**Solução alternativa**: faça com que os usuários façam logoff e, em seguida, faça logon novamente.</span><span class="sxs-lookup"><span data-stu-id="55556-154">**Workaround**: Have users log out and then log back in.</span></span>

## <span data-ttu-id="55556-155">A mensagem de erro é exibida erroneamente quando o grupo de conexão é publicado somente para o usuário</span><span class="sxs-lookup"><span data-stu-id="55556-155">Error message is erroneously displayed when the connection group is published only to the user</span></span>


<span data-ttu-id="55556-156">Quando você executa o Repair-AppvClientConnectionGroup, o seguinte erro é exibido, mesmo quando o grupo de conexão é publicado somente para o usuário: "erro de integração interno do App-V: pacote não integrado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="55556-156">When you run Repair-AppvClientConnectionGroup, the following error is displayed, even when the connection group is published only to the user: “Internal App-V Integration error: Package not integrated for the user.</span></span> <span data-ttu-id="55556-157">Certifique-se de que o pacote seja adicionado ao computador e publicado ao usuário. "</span><span class="sxs-lookup"><span data-stu-id="55556-157">Please ensure that the package is added to the machine and published to the user.”</span></span>

<span data-ttu-id="55556-158">**Solução alternativa**: siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="55556-158">**Workaround**: Do one of the following:</span></span>

-   <span data-ttu-id="55556-159">Publicar todos os pacotes em um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="55556-159">Publish all packages in a connection group.</span></span>

    <span data-ttu-id="55556-160">O problema surge quando o grupo de conexão que está sendo reparada tem pacotes que estão ausentes ou não estão disponíveis para o usuário (ou seja, não são publicados globalmente ou para o usuário).</span><span class="sxs-lookup"><span data-stu-id="55556-160">The problem arises when the connection group being repaired has packages that are missing or not available to the user (that is, not published globally or to the user).</span></span> <span data-ttu-id="55556-161">No entanto, o reparo funcionará se todos os pacotes do grupo de conexão estiverem disponíveis, portanto, certifique-se de que todos os pacotes sejam publicados.</span><span class="sxs-lookup"><span data-stu-id="55556-161">However, the repair will work if all of the connection group’s packages are available, so ensure that all packages are published.</span></span>

-   <span data-ttu-id="55556-162">Reparar pacotes individualmente usando o comando Repair-AppvClientPackage em vez do comando Repair-AppvClientConnectionGroup.</span><span class="sxs-lookup"><span data-stu-id="55556-162">Repair packages individually using the Repair-AppvClientPackage command rather than the Repair-AppvClientConnectionGroup command.</span></span>

    <span data-ttu-id="55556-163">Determine quais pacotes estão disponíveis para os usuários e execute o comando Repair-AppvClientPackage uma vez para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="55556-163">Determine which packages are available to users and then run the Repair-AppvClientPackage command once for each package.</span></span> <span data-ttu-id="55556-164">Use cmdlets do PowerShell para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="55556-164">Use PowerShell cmdlets to do the following:</span></span>

    1.  <span data-ttu-id="55556-165">Obter todos os pacotes em um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="55556-165">Get all the packages in a connection group.</span></span>

    2.  <span data-ttu-id="55556-166">Verifique se cada pacote está publicado no momento.</span><span class="sxs-lookup"><span data-stu-id="55556-166">Check to see if each package is currently published.</span></span>

    3.  <span data-ttu-id="55556-167">Se o pacote estiver publicado no momento, execute Repair-AppvClientPackage nesse pacote.</span><span class="sxs-lookup"><span data-stu-id="55556-167">If the package is currently published, run Repair-AppvClientPackage on that package.</span></span>

## <span data-ttu-id="55556-168">Ícones não exibidos corretamente no sequenciador</span><span class="sxs-lookup"><span data-stu-id="55556-168">Icons not displayed properly in Sequencer</span></span>


<span data-ttu-id="55556-169">Os ícones na guia atalhos e associações de tipo de arquivo não são exibidos corretamente ao modificar um pacote no sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="55556-169">Icons in the Shortcuts and File Type Associations tab are not displayed correctly when modifying a package in the App-V Sequencer.</span></span> <span data-ttu-id="55556-170">Esse problema ocorre quando o tamanho dos ícones não é 16x16 ou 32x32.</span><span class="sxs-lookup"><span data-stu-id="55556-170">This problem occurs when the size of the icons are not 16x16 or 32x32.</span></span>

<span data-ttu-id="55556-171">**Solução alternativa**: Use apenas ícones que sejam 16x16 ou 32x32.</span><span class="sxs-lookup"><span data-stu-id="55556-171">**Workaround**: Only use icons that are 16x16 or 32x32.</span></span>

## <span data-ttu-id="55556-172">O script InsertVersionInfo. SQL não é mais necessário para o banco de dados de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="55556-172">InsertVersionInfo.sql script no longer required for the Management Database</span></span>


<span data-ttu-id="55556-173">O script InsertVersionInfo. SQL não é necessário para versões do banco de dados de gerenciamento do App-V posterior à App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="55556-173">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="55556-174">O script Permissions. SQL deve ser atualizado de acordo com a **etapa 2** no [artigo do KB 3031340](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="55556-174">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span>

<span data-ttu-id="55556-175">**Importante** 
 A **etapa 1** não é necessária para versões do App-v posteriores ao app-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="55556-175">**Important**
**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

 

## <span data-ttu-id="55556-176">Microsoft Visual Studio 2012 não suportado</span><span class="sxs-lookup"><span data-stu-id="55556-176">Microsoft Visual Studio 2012 not supported</span></span>


<span data-ttu-id="55556-177">O App-V 5,1 não oferece suporte ao Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="55556-177">App-V 5.1 does not support Visual Studio 2012.</span></span>

<span data-ttu-id="55556-178">**Solução alternativa**: nenhum</span><span class="sxs-lookup"><span data-stu-id="55556-178">**Workaround**: None</span></span>

## <span data-ttu-id="55556-179">Restrições de nome de arquivo do aplicativo para o App-V 5. x Sequencer</span><span class="sxs-lookup"><span data-stu-id="55556-179">Application filename restrictions for App-V 5.x Sequencer</span></span>


<span data-ttu-id="55556-180">O sequenciador App-V 5. x não pode sequenciar aplicativos com nomes de filecorrespondentes a "CO_ &lt; x &gt; ", onde x é qualquer numeral.</span><span class="sxs-lookup"><span data-stu-id="55556-180">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="55556-181">O erro 0x8007139F será gerado.</span><span class="sxs-lookup"><span data-stu-id="55556-181">Error 0x8007139F will be generated.</span></span>

<span data-ttu-id="55556-182">**Solução alternativa**: Use um nome de arquivo diferente</span><span class="sxs-lookup"><span data-stu-id="55556-182">**Workaround**: Use a different filename</span></span>

## <span data-ttu-id="55556-183">Erro intermitente "arquivo não encontrado" ao montar um pacote</span><span class="sxs-lookup"><span data-stu-id="55556-183">Intermittent "File Not Found" error when Mounting a Package</span></span>


<span data-ttu-id="55556-184">Às vezes, ao montar um pacote, um erro de "arquivo não encontrado" (0x80070002) é gerado.</span><span class="sxs-lookup"><span data-stu-id="55556-184">Occasionally when mounting a package, a "File Not Found" (0x80070002) error is generated.</span></span> <span data-ttu-id="55556-185">Geralmente, isso ocorre quando uma pasta em um pacote do App-V contém muitos arquivos (por exemplo, 20K ou mais).</span><span class="sxs-lookup"><span data-stu-id="55556-185">Typically, this occurs when a folder in an App-V package contains many files ( i.e. 20K or more).</span></span> <span data-ttu-id="55556-186">Isso pode fazer com que o fluxo de transmissão demorasse mais tempo do que o esperado e até o tempo limite que gera o erro "arquivo não encontrado".</span><span class="sxs-lookup"><span data-stu-id="55556-186">This can cause streaming to take longer than expected and to time out which generates the "File Not Found" error.</span></span>

<span data-ttu-id="55556-187">**Solução alternativa**: Iniciando com HF06, uma nova chave do registro foi introduzida para habilitar a extensão desse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="55556-187">**Workaround**: Starting with HF06, a new registry key has been introduced to enable extending this time-out period.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left"><span data-ttu-id="55556-188">Caminho</span><span class="sxs-lookup"><span data-stu-id="55556-188">Path</span></span></td>
<td align="left"><span data-ttu-id="55556-189">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</span><span class="sxs-lookup"><span data-stu-id="55556-189">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Streaming</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="55556-190">Configuração</span><span class="sxs-lookup"><span data-stu-id="55556-190">Setting</span></span></td>
<td align="left"><span data-ttu-id="55556-191">StreamResponseWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="55556-191">StreamResponseWaitTimeout</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="55556-192">UDT</span><span class="sxs-lookup"><span data-stu-id="55556-192">DataType</span></span></td>
<td align="left"><span data-ttu-id="55556-193">DWORD</span><span class="sxs-lookup"><span data-stu-id="55556-193">DWORD</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="55556-194">Americanas</span><span class="sxs-lookup"><span data-stu-id="55556-194">Units</span></span></td>
<td align="left"><span data-ttu-id="55556-195">Second</span><span class="sxs-lookup"><span data-stu-id="55556-195">Seconds</span></span></td>
</tr>
<tr>
<td align="left"><span data-ttu-id="55556-196">Padrão</span><span class="sxs-lookup"><span data-stu-id="55556-196">Default</span></span></td>
<td align="left"><span data-ttu-id="55556-197">5</span><span class="sxs-lookup"><span data-stu-id="55556-197">5</span></span><br />
<strong><span data-ttu-id="55556-198">Observação </strong> : esse valor será o padrão se a chave do registro não for definida ou um valor &lt; = 5 for especificado.</span><span class="sxs-lookup"><span data-stu-id="55556-198">Note</strong>: this value is the default if the registry key is not defined or a value &lt;=5 is specified.</span></span>
</td>
</tr>
</tbody>
</table>






## <span data-ttu-id="55556-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55556-199">Related topics</span></span>


[<span data-ttu-id="55556-200">Sobre o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="55556-200">About App-V 5.1</span></span>](about-app-v-51.md)

 

 





