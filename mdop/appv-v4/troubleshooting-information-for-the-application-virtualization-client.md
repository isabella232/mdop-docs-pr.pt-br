---
title: Informações para solução de problemas do Application Virtualization Client
description: Informações para solução de problemas do Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796676"
---
# <span data-ttu-id="b875d-103">Informações para solução de problemas do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="b875d-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="b875d-104">Este tópico inclui informações que você pode usar para solucionar vários problemas no cliente do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="b875d-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="b875d-105">A atualização de publicação está muito lenta</span><span class="sxs-lookup"><span data-stu-id="b875d-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="b875d-106">Se a atualização de publicação em um computador específico demorar muito mais do que o esperado e se o cliente estiver configurado para usar a configuração **IconSourceRoot** , determine se **IconSourceRoot** contém uma URL inválida.</span><span class="sxs-lookup"><span data-stu-id="b875d-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="b875d-107">Uma URL inválida causará atrasos muito longos durante A atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="b875d-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="b875d-108">Os usuários não conseguem se conectar ao servidor e vão para o modo de operações desconectadas</span><span class="sxs-lookup"><span data-stu-id="b875d-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="b875d-109">Quando você estiver usando um servidor de gerenciamento App-V configurado com o protocolo RTSPs, se os usuários não conseguirem se conectar e entrarem no modo operações desconectadas, determine se o certificado que está sendo usado no servidor é válido.</span><span class="sxs-lookup"><span data-stu-id="b875d-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="b875d-110">Um certificado inválido impedirá que os usuários se conectem e farão com que eles entrem no modo operações desconectadas.</span><span class="sxs-lookup"><span data-stu-id="b875d-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="b875d-111">Os usuários experimentam desempenho lento quando os aplicativos não são totalmente armazenados em cache</span><span class="sxs-lookup"><span data-stu-id="b875d-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="b875d-112">Quando os aplicativos não são totalmente armazenados em cache, os usuários podem ocasionalmente sofrer um desempenho temporário lento ou intermitente ao iniciar ou usar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b875d-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="b875d-113">Há vários possíveis motivos pelos quais isso pode ocorrer — por exemplo, quando o cliente App-V está em processo de carregamento automático de um aplicativo ou quando uma solicitação fora da sequência está sendo processada.</span><span class="sxs-lookup"><span data-stu-id="b875d-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="b875d-114">Quando os aplicativos estiverem totalmente armazenados em cache, esses problemas não ocorrerão mais.</span><span class="sxs-lookup"><span data-stu-id="b875d-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="b875d-115">Erro exibido após a remoção de uma atualização</span><span class="sxs-lookup"><span data-stu-id="b875d-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="b875d-116">Você deve usar o formato de comando correto do Windows Installer 3,1 para remover uma atualização do cliente App-V da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b875d-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="b875d-117">Usar o formato de comando antigo causará o `msiexec /package <GUID> /uninstall <GUID>` erro 6003 "não foi possível iniciar o cliente do Application Virtualization".</span><span class="sxs-lookup"><span data-stu-id="b875d-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="b875d-118">Código de erro 0A-0000E01E ocorre quando você tenta iniciar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="b875d-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="b875d-119">O código de erro 0A-0000E01E indica que o pacote do aplicativo sequenciado pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b875d-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="b875d-120">A solução é resequenciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="b875d-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="b875d-121">Os usuários não podem acessar arquivos que eles criaram na unidade p:</span><span class="sxs-lookup"><span data-stu-id="b875d-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="b875d-122">Se os usuários salvarem arquivos na unidade **p:** , eles não poderão recuperá-los porque não têm direitos de leitura na unidade.</span><span class="sxs-lookup"><span data-stu-id="b875d-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="b875d-123">Os usuários não devem salvar arquivos na unidade **p:** .</span><span class="sxs-lookup"><span data-stu-id="b875d-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="b875d-124">O usuário é solicitado com um erro de 1D1</span><span class="sxs-lookup"><span data-stu-id="b875d-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="b875d-125">Quando a URL de streaming de arquivo está definida incorretamente no arquivo Open Software Descriptor (OSD), o cliente App-V retorna um erro 1D1 em vez de um erro "arquivo não encontrado".</span><span class="sxs-lookup"><span data-stu-id="b875d-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="b875d-126">Esse erro indica que o início do aplicativo falhou e o usuário foi forçado para o modo de operações desconectadas.</span><span class="sxs-lookup"><span data-stu-id="b875d-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="b875d-127">Corrija a URL de streaming de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b875d-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="b875d-128">Ícones incorretos associados a alguns aplicativos</span><span class="sxs-lookup"><span data-stu-id="b875d-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="b875d-129">Quando um ícone deve ser usado em uma operação de publicação, o cliente App-V primeiro determina se ele já tem uma cópia em cache do ícone, olhando o cache de ícone para um item cujo caminho de origem original corresponde ao caminho do ícone fornecido para a operação de publicação.</span><span class="sxs-lookup"><span data-stu-id="b875d-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="b875d-130">Se o cliente App-V encontrar uma correspondência, ele usará o ícone já em cache; caso contrário, ele fará o download do novo ícone no cache.</span><span class="sxs-lookup"><span data-stu-id="b875d-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="b875d-131">Se o caminho para o ícone for um diretório de rascunho ou se for reutilizado para novos ícones ou pacotes, a pesquisa no cache pode selecionar o ícone errado de uma operação anterior.</span><span class="sxs-lookup"><span data-stu-id="b875d-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="b875d-132">Os usuários são solicitados a fornecer credenciais ao iniciar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="b875d-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="b875d-133">Se um usuário tentar iniciar um aplicativo virtual ao qual o administrador do sistema restringiu o acesso, o usuário pode ser solicitado a inserir as credenciais.</span><span class="sxs-lookup"><span data-stu-id="b875d-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="b875d-134">O usuário deve digitar o nome de usuário e a senha de uma conta que tenha permissão para iniciar o aplicativo e, em seguida, pressionar ENTER.</span><span class="sxs-lookup"><span data-stu-id="b875d-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="b875d-135">Atualização de publicação falha após a atualização do cliente App-V para a versão 4,5</span><span class="sxs-lookup"><span data-stu-id="b875d-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="b875d-136">Se o diretório de dados do usuário era colocado anteriormente em um local não padrão (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nome_do_usuário*%), os usuários que não têm privilégios de administrador no computador descobrirão que a atualização de publicação falha após a atualização do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="b875d-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="b875d-137">Durante a atualização, o diretório de dados global do aplicativo App-V do cliente e todos os seus subdiretórios são configurados com direitos de acesso restritos somente para administradores.</span><span class="sxs-lookup"><span data-stu-id="b875d-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="b875d-138">Você pode evitar esse problema alterando o diretório de dados do usuário antes da atualização para que ele não seja um subdiretório do diretório de dados globais.</span><span class="sxs-lookup"><span data-stu-id="b875d-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="b875d-139">Reinicialização necessária após falha na instalação</span><span class="sxs-lookup"><span data-stu-id="b875d-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="b875d-140">Se a instalação do cliente falhar por qualquer motivo e se as tentativas subsequentes de instalar o cliente também falharem, verifique o log do Windows Installer para ver se ele mostra um erro "sftplay Failed, Error = 1072".</span><span class="sxs-lookup"><span data-stu-id="b875d-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="b875d-141">Em caso afirmativo, reinicie o computador antes de tentar instalar o cliente novamente.</span><span class="sxs-lookup"><span data-stu-id="b875d-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="b875d-142">Reparar um aplicativo virtual corrompido</span><span class="sxs-lookup"><span data-stu-id="b875d-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="b875d-143">Se, por qualquer motivo, um pacote de aplicativo virtual instalado usando um arquivo MSI (pacote do Windows Installer) for corrompido, reinstale o pacote.</span><span class="sxs-lookup"><span data-stu-id="b875d-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="b875d-144">A função de reparo disponível no Windows Installer não atualizará os volumes do usuário.</span><span class="sxs-lookup"><span data-stu-id="b875d-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="b875d-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b875d-145">Related topics</span></span>


[<span data-ttu-id="b875d-146">Referência do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="b875d-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





