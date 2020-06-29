---
title: Como fazer upgrade do Application Virtualization Client
description: Como fazer upgrade do Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796928"
---
# <span data-ttu-id="3e7a3-103">Como fazer upgrade do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="3e7a3-103">How to Upgrade the Application Virtualization Client</span></span>


<span data-ttu-id="3e7a3-104">Você pode usar os procedimentos a seguir para atualizar o cliente de área de trabalho do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal).</span><span class="sxs-lookup"><span data-stu-id="3e7a3-104">You can use the following procedures to upgrade the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="3e7a3-105">Você atualiza o cliente instalando uma nova versão sobre a versão anterior instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-105">You upgrade the client by installing a new version over the previously installed older version.</span></span> <span data-ttu-id="3e7a3-106">Quando você atualiza os clientes, o software do instalador preserva e migra automaticamente as configurações do usuário para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-106">When you upgrade the clients, the installer software automatically preserves and migrates the user’s settings for virtual applications.</span></span> <span data-ttu-id="3e7a3-107">É necessário ter direitos administrativos para executar o programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-107">Administrative rights are required to run the setup program.</span></span>

<span data-ttu-id="3e7a3-108">**Observação**  Durante a atualização para versões do Application Virtualization (App-V) 4.5 ou versões posteriores, as permissões para a chave do Registro HKCU são alteradas.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-108">**Note** During the upgrade to Application Virtualization (App-V)4.5 or later versions, the permissions to the HKCU registry key are changed.</span></span> <span data-ttu-id="3e7a3-109">Por isso, os usuários perderão as configurações de usuário que foram definidas anteriormente, como as configurações de modo desconectado do usuário definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-109">Because of this, users will lose user configurations that were set previously, such as user-configured Disconnected Mode settings.</span></span> <span data-ttu-id="3e7a3-110">Se o usuário não estiver ativamente importando a configuração do comportamento da interface de usuário do cliente por meio de um bloqueio de permissão, o usuário poderá redefinir essas preferências após uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-110">If the user is not actively restricted from configuring client user interface behavior through a permission lockdown, the user can reset these preferences after a publishing refresh.</span></span>

 

<span data-ttu-id="3e7a3-111">**Importante**  Ao atualizar para a versão 4.6 ou uma versão posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-111">**Important** When upgrading to version4.6 or a later version of the App-V Client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="3e7a3-112">A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-112">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

 

**<span data-ttu-id="3e7a3-113">Para atualizar o cliente da área de trabalho do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="3e7a3-113">To upgrade the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="3e7a3-114">Desligar todos os aplicativos virtuais, clique com o botão direito do mouse no ícone do cliente da área de trabalho do App-V exibido na área de notificação da área de trabalho do Windows e selecione **sair** para desligar o cliente existente.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-114">Shut down all virtual applications, right-click the App-V Desktop Client icon displayed in the Windows desktop notification area, and select **Exit** to shut down the existing client.</span></span>

2.  <span data-ttu-id="3e7a3-115">Depois de obter o arquivo morto correto do instalador e salvá-lo no seu computador, clique duas vezes nele para expandir o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-115">After you have obtained the correct installer archive file and saved it to your computer, double-click it to expand the archive.</span></span>

3.  <span data-ttu-id="3e7a3-116">Navegue até localizar o arquivo setup.exe e clique duas vezes setup.exe para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-116">Browse to find the setup.exe file, and double-click setup.exe to start the installation.</span></span>

4.  <span data-ttu-id="3e7a3-117">O assistente verifica o sistema para garantir que todos os softwares de pré-requisito estejam instalados e solicitará que você instale qualquer um dos seguintes, se ausente:</span><span class="sxs-lookup"><span data-stu-id="3e7a3-117">The wizard checks the system to ensure that all prerequisite software is installed and will prompt you to install any of the following, if missing:</span></span>

    -   <span data-ttu-id="3e7a3-118">Pacote redistribuível do Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="3e7a3-118">Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>

    -   <span data-ttu-id="3e7a3-119">Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="3e7a3-119">Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

    -   <span data-ttu-id="3e7a3-120">Relatório de erros do aplicativo Microsoft</span><span class="sxs-lookup"><span data-stu-id="3e7a3-120">Microsoft Application Error Reporting</span></span>

    <span data-ttu-id="3e7a3-121">**Observação**  Para a versão 4.6 ou superior, o assistente também instalará o seguinte pré-requisito de software:</span><span class="sxs-lookup"><span data-stu-id="3e7a3-121">**Note** For version4.6 and higher, the wizard will also install the following software prerequisite:</span></span>

    -   <span data-ttu-id="3e7a3-122">Pacote redistribuível do Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="3e7a3-122">Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

     

5.  <span data-ttu-id="3e7a3-123">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-123">Click **Install**.</span></span> <span data-ttu-id="3e7a3-124">O progresso da instalação é exibido, e o status muda de **pendente** para **instalação**.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-124">Installation progress is displayed, and the status changes from **Pending** to **Installing**.</span></span> <span data-ttu-id="3e7a3-125">O status de instalação muda para **bem-sucedida** à medida que cada etapa é concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-125">Installation status changes to **Succeeded** as each step is completed successfully.</span></span>

6.  <span data-ttu-id="3e7a3-126">Quando a caixa de diálogo de **cliente da área de trabalho do Application Virtualization** for exibida e exibir uma mensagem informando que uma versão mais antiga do cliente foi encontrada no computador, clique em **Avançar** para atualizar para a nova versão.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-126">When the **Application Virtualization Desktop Client** dialog appears and displays a message stating that an older version of the client has been found on the computer, click **Next** to upgrade to the new version.</span></span>

7.  <span data-ttu-id="3e7a3-127">Quando a tela **contrato de licença** for exibida, leia o contrato de licença e, se você concordar, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-127">When the **License Agreement** screen is displayed, read the license agreement, and if you agree, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

8.  <span data-ttu-id="3e7a3-128">Quando o Assistente InstallShield exibir a tela de diálogo **pronto para atualizar o programa** , clique em **Atualizar** para iniciar a atualização.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-128">When the InstallShield Wizard displays the **Ready to Upgrade the Program** dialog screen, click **Upgrade** to begin the upgrade.</span></span> <span data-ttu-id="3e7a3-129">A tela seguinte indica que o cliente está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-129">The next screen indicates that the client is being installed.</span></span>

    <span data-ttu-id="3e7a3-130">**Aviso**  Se você não tiver desligado o programa cliente na etapa 1, talvez veja um aviso **arquivos em uso** exibido.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-130">**Warning** If you did not shut down the client program in step 1, you might see a **Files In Use** warning displayed.</span></span> <span data-ttu-id="3e7a3-131">Se isso acontecer, clique com o botão direito do mouse no ícone do cliente App-V exibido na área de notificação da área de trabalho e selecione **sair** para desligar o cliente existente.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-131">If this happens, right-click the App-V Client icon displayed in the desktop notification area and select **Exit** to shut down the existing client.</span></span> <span data-ttu-id="3e7a3-132">Em seguida, clique em **repetir** para continuar.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-132">Then click **Retry** to continue.</span></span>

     

9.  <span data-ttu-id="3e7a3-133">Quando a instalação for concluída com êxito, você será solicitado a reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-133">When the installation completes successfully, you will be prompted to restart the computer.</span></span> <span data-ttu-id="3e7a3-134">Você precisa reiniciar o computador para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-134">You need to restart the computer to complete the installation.</span></span>

    <span data-ttu-id="3e7a3-135">**Cuidado**  Se a atualização falhar por algum motivo, será preciso reiniciar o computador antes de tentar a atualização novamente.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-135">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

**<span data-ttu-id="3e7a3-136">Para atualizar o cliente do Application Virtualization usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="3e7a3-136">To upgrade the Application Virtualization Client by Using the Command Line</span></span>**

1.  <span data-ttu-id="3e7a3-137">Se estiver atualizando o cliente App-V usando o programa setup.msi, certifique-se de que todos os softwares de pré-requisito necessários foram instalados.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-137">If upgrading the App-V client using the setup.msi program, ensure that any necessary prerequisite software has been installed.</span></span>

    **<span data-ttu-id="3e7a3-138">Importante</span><span class="sxs-lookup"><span data-stu-id="3e7a3-138">Important</span></span>**  
    -   <span data-ttu-id="3e7a3-139">Para a versão 4.6 e posterior do cliente App-V, o programa setup.msi verifica o sistema e irá falhar com uma mensagem de erro indicando que a instalação não pode continuar se o software de pré-requisito não estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-139">For version4.6 and later of the App-V client, the setup.msi program checks the system and will fail with an error message indicating that installation cannot continue if prerequisite software is not installed.</span></span>

    -   <span data-ttu-id="3e7a3-140">Para o App-V versão 4.6, os parâmetros de linha de comando não podem ser usados durante uma atualização e serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-140">For App-V version4.6, command-line parameters cannot be used during an upgrade and will be ignored.</span></span>

     

2.  <span data-ttu-id="3e7a3-141">O exemplo de linha de comando a seguir usa o arquivo setup.msi para atualizar o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-141">The following command-line example uses the setup.msi file to upgrade the App-V Client.</span></span> <span data-ttu-id="3e7a3-142">Você precisará usar o programa de instalação do cliente correto, dependendo se estiver atualizando o cliente da área de trabalho do App-V ou o cliente App-V para serviços de área de trabalho remota (anteriormente serviços de terminal).</span><span class="sxs-lookup"><span data-stu-id="3e7a3-142">You will need to use the correct client installer program depending on whether you are upgrading the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span>

    **<span data-ttu-id="3e7a3-143">msiexec.exe/i "setup.msi"</span><span class="sxs-lookup"><span data-stu-id="3e7a3-143">msiexec.exe /i "setup.msi"</span></span>**

    <span data-ttu-id="3e7a3-144">**Importante**  As aspas são necessárias somente quando o valor contém um espaço.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-144">**Important** The quotation marks are required only when the value contains a space.</span></span> <span data-ttu-id="3e7a3-145">Para a consistência, todas as instâncias no exemplo anterior são mostradas como tendo aspas.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-145">For consistency, all instances in the preceding example are shown as having quotation marks.</span></span>

     

**<span data-ttu-id="3e7a3-146">Para atualizar o cliente do Application Virtualization para serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="3e7a3-146">To upgrade the Application Virtualization Client for Remote Desktop Services</span></span>**

1.  <span data-ttu-id="3e7a3-147">Siga as políticas padrão da sua organização para instalar ou atualizar aplicativos no servidor host da sessão da área de trabalho remota (host RDSession).</span><span class="sxs-lookup"><span data-stu-id="3e7a3-147">Follow your organization’s standard policies for installing or upgrading applications on the Remote Desktop Session Host (RDSession Host) server.</span></span> <span data-ttu-id="3e7a3-148">Se o sistema fizer parte de um farm, remova o host RDSession do farm de servidores.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-148">If the system is part of a farm, remove the RDSession Host from the server farm.</span></span>

2.  <span data-ttu-id="3e7a3-149">Para atualizar o cliente App-V para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal), você deve usar a linha de comando porque não é possível atualizar o cliente manualmente no host RDSession.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-149">To upgrade the App-V Client for Remote Desktop Services (formerly Terminal Services), you must use the command line because you cannot upgrade the client manually on the RDSession Host.</span></span>

    <span data-ttu-id="3e7a3-150">**Observação**  Na versão 4,6 e posterior da App-V, além de usar a linha de comando para atualizar o cliente, você também pode usar uma sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-150">**Note** In App-V version 4.6 and later, in addition to using the command line to upgrade the client, you can also use a Remote Desktop session.</span></span> <span data-ttu-id="3e7a3-151">Nenhum parâmetro especial é necessário para iniciar a sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-151">No special parameters are required to start the Remote Desktop session.</span></span>

     

3.  <span data-ttu-id="3e7a3-152">Após concluir a atualização do cliente para serviços de área de trabalho remota, reinicie e conecte-se ao host RDSession.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-152">After the Client for Remote Desktop Services upgrade is complete, restart and log in to the RDSession Host.</span></span>

4.  <span data-ttu-id="3e7a3-153">Após a reinicialização do sistema, adicione o servidor ao farm de servidores.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-153">After the system is restarted, add the server to the server farm.</span></span>

    <span data-ttu-id="3e7a3-154">**Cuidado**  Se a atualização falhar por algum motivo, será preciso reiniciar o computador antes de tentar a atualização novamente.</span><span class="sxs-lookup"><span data-stu-id="3e7a3-154">**Caution** If the upgrade fails for any reason, you will need to restart the computer before attempting the upgrade again.</span></span>

     

## <span data-ttu-id="3e7a3-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e7a3-155">Related topics</span></span>


[<span data-ttu-id="3e7a3-156">Considerações de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="3e7a3-156">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





