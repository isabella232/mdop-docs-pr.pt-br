---
title: Notas de Versão do MBAM 1.0
description: Notas de Versão do MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799790"
---
# <span data-ttu-id="952ec-103">Notas de Versão do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="952ec-103">Release Notes for MBAM 1.0</span></span>


**<span data-ttu-id="952ec-104">Para procurar um problema específico nestas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="952ec-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="952ec-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="952ec-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

<span data-ttu-id="952ec-106">Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-106">These release notes contain information that is required to successfully install MBAM.</span></span> <span data-ttu-id="952ec-107">As notas de versão também contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="952ec-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="952ec-108">Se houver uma diferença entre essas notas de versão e outras documentações MBAM documentação, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="952ec-108">If there is a difference between these release notes and other MBAM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="952ec-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="952ec-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="952ec-110">Sobre a documentação do produto</span><span class="sxs-lookup"><span data-stu-id="952ec-110">About the Product Documentation</span></span>


<span data-ttu-id="952ec-111">Para obter informações sobre a documentação do MBAM, consulte a home page do MBAM no Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="952ec-111">For information about MBAM documentation, see the MBAM home page on Microsoft TechNet.</span></span>

<span data-ttu-id="952ec-112">Para obter uma cópia disponível para download da documentação do MBAM, consulte <https://go.microsoft.com/fwlink/p/?LinkId=225356> o centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="952ec-112">To obtain a downloadable copy of the MBAM documentation, see <https://go.microsoft.com/fwlink/p/?LinkId=225356> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="952ec-113">Fornecer comentários</span><span class="sxs-lookup"><span data-stu-id="952ec-113">Provide Feedback</span></span>


<span data-ttu-id="952ec-114">Estamos interessados em seus comentários sobre o MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-114">We are interested in your feedback on MBAM.</span></span> <span data-ttu-id="952ec-115">Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="952ec-115">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="952ec-116">**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras na nossa documentação e nas versões do produto.</span><span class="sxs-lookup"><span data-stu-id="952ec-116">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="952ec-117">Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="952ec-117">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="952ec-118">Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="952ec-118">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="952ec-119">Problemas conhecidos com o MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="952ec-119">Known Issues with MBAM 1.0</span></span>


<span data-ttu-id="952ec-120">Esta seção contém notas de versão sobre os problemas conhecidos com a instalação e a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-120">This section contains release notes about the known issues with MBAM setup and installation.</span></span>

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a><span data-ttu-id="952ec-121">Se você selecionar a opção "usar um certificado para criptografar a comunicação de rede" durante a instalação, as conexões de banco de dados existentes e os aplicativos dependentes podem parar de funcionar</span><span class="sxs-lookup"><span data-stu-id="952ec-121">If you select the “Use a certificate to encrypt the network communication” option during Setup, existing database connections and dependent applications can stop functioning</span></span>

<span data-ttu-id="952ec-122">Você pode configurar o MBAM para **comunicação de rede criptografada** depois de instalar os recursos de banco de dados de recuperação e de banco de dados de status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="952ec-122">You can configure MBAM for **Encrypted network communication** after you install either the Recovery and Hardware Database or the Compliance Status Database features.</span></span> <span data-ttu-id="952ec-123">Se você optar por configurar o MBAM para comunicação de rede criptografada, o programa de instalação do MBAM configura a instância do mecanismo de banco de dados do SQL Server para usar SSL (Secure Sockets Layer) para comunicação entre o banco de dados aplicável e os recursos do servidor de relatório de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="952ec-123">If you choose to configure MBAM for Encrypted network communication, MBAM Setup configures the instance of the SQL Server Database Engine to use Secure Sockets Layer (SSL) for communication between the applicable database and both the Administration and Monitoring Server and the Compliance and Audit Report Server features.</span></span>

-   <span data-ttu-id="952ec-124">Se a instância do mecanismo de banco de dados do SQL Server ainda não estiver configurada para usar SSL, a instalação do MBAM a configurará para fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="952ec-124">If the instance of the SQL Server Database Engine is not already configured to use SSL, MBAM Setup configures it to do so.</span></span> <span data-ttu-id="952ec-125">Isso pode evitar que aplicativos que tentam usar bancos de dados não MBAM na instância do mecanismo de banco de dados do SQL Server se comuniquem com seus bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="952ec-125">This can prevent applications that try to use non-MBAM databases on the instance of the SQL Server Database Engine from communicating with their databases.</span></span>

-   <span data-ttu-id="952ec-126">Se a instância do mecanismo de banco de dados do SQL Server já estiver configurada para usar SSL, ela será configurada para usar o certificado selecionado pelo usuário durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="952ec-126">If the instance of the SQL Server Database Engine is already configured to use SSL, it is configured to use the certificate that the user selected during setup.</span></span> <span data-ttu-id="952ec-127">Se esse certificado for diferente do que já estava em uso, ele pode impedir que aplicativos que usam bancos de dados do SQL Server na instância do mecanismo de banco de dados do SQL Server sejam executados.</span><span class="sxs-lookup"><span data-stu-id="952ec-127">If this certificate differs from the one that was already in use, it can prevent applications that use SQL Server databases on the instance of the SQL Server Database Engine from running.</span></span>

<span data-ttu-id="952ec-128">**Solução alternativa:** Nenhuma</span><span class="sxs-lookup"><span data-stu-id="952ec-128">**WORKAROUND:** None</span></span>

### <span data-ttu-id="952ec-129">A instalação do MBAM falha durante a instalação quando você usa uma conta de administrador local</span><span class="sxs-lookup"><span data-stu-id="952ec-129">MBAM Setup fails during installation when you use a local Administrator account</span></span>

<span data-ttu-id="952ec-130">A instalação do MBAM falha quando você usa uma conta de administrador local.</span><span class="sxs-lookup"><span data-stu-id="952ec-130">MBAM Setup fails when you use a local Administrator account.</span></span> <span data-ttu-id="952ec-131">O arquivo de log contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="952ec-131">The log file contains the following information:</span></span>

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

<span data-ttu-id="952ec-132">**Solução alternativa:** Use uma conta de domínio com credenciais administrativas no computador servidor ao instalar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-132">**WORKAROUND:** Use a domain account with administrative credentials on the server computer when you install MBAM.</span></span>

### <span data-ttu-id="952ec-133">A instalação do MBAM reconfigura a instância do mecanismo de banco de dados do SQL Server para não usar SSL se você selecionar "não criptografar comunicação de rede"</span><span class="sxs-lookup"><span data-stu-id="952ec-133">MBAM Setup reconfigures the instance of the SQL Server Database Engine to not use SSL if you select “Do not encrypt network communication”</span></span>

<span data-ttu-id="952ec-134">Ao instalar o banco de dados de recuperação e de hardware ou o status de conformidade, você pode usar a instalação para configurar o MBAM selecionando **comunicação de rede criptografada**.</span><span class="sxs-lookup"><span data-stu-id="952ec-134">When you install either the Recovery and Hardware Database or the Compliance Status Database, you can use Setup to configure MBAM by selecting **Encrypted network communication**.</span></span> <span data-ttu-id="952ec-135">Se você decidir não criptografar a comunicação de rede, o MBAM setup reconfigurará a instância do mecanismo de banco de dados do SQL Server para que ele não use SSL.</span><span class="sxs-lookup"><span data-stu-id="952ec-135">If you decide not to encrypt the network communication, MBAM Setup reconfigures the instance of the SQL Server Database Engine so that it does not use SSL.</span></span>

-   <span data-ttu-id="952ec-136">Se a instância do mecanismo de banco de dados do SQL Server já estiver configurada para usar SSL, a instalação do MBAM desabilitará a SSL na instância do mecanismo de banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="952ec-136">If the instance of the SQL Server Database Engine is already configured to use SSL, MBAM Setup disables SSL on the instance of the SQL Server Database Engine.</span></span> <span data-ttu-id="952ec-137">Isso altera a segurança de comunicação entre os aplicativos que usam bancos de dados que não estão relacionados a bancos de dados do MBAM na instância do mecanismo de banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="952ec-137">This changes the communication security between the applications that use databases that are not related to MBAM databases on the instance of the SQL Server Database Engine.</span></span>

<span data-ttu-id="952ec-138">**Solução alternativa:** Nenhuma</span><span class="sxs-lookup"><span data-stu-id="952ec-138">**WORKAROUND:** None</span></span>

### <span data-ttu-id="952ec-139">Pré-requisito ausente para o recurso de servidor Web de ferramentas e scripts de gerenciamento de serviços de informações da Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="952ec-139">Missing prerequisite for the Internet Information Services (IIS) Management Scripts and Tools web server feature</span></span>

<span data-ttu-id="952ec-140">A configuração do MBAM depende do recurso de servidor Web de scripts e ferramentas de gerenciamento do IIS, mas não é um pré-requisito imposto.</span><span class="sxs-lookup"><span data-stu-id="952ec-140">MBAM Setup is dependent on the IIS Management Scripts and Tools web server feature, but it is not an enforced prerequisite.</span></span> <span data-ttu-id="952ec-141">A instalação do servidor permite que você instale o MBAM quando esse recurso estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="952ec-141">Server setup lets you install MBAM when this feature is missing.</span></span> <span data-ttu-id="952ec-142">No entanto, isso fará com que o serviço de backup MBAM o gravador VSS inicie e, em seguida, parar porque não consegue localizar a instrumentação de gerenciamento do Windows (WMI) e o provedor de serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="952ec-142">However, this will cause the backup service MBAM VSS Writer to start and then stop, because it cannot locate the Windows Management Instrumentation (WMI) and the Internet Information Services (IIS) provider.</span></span> <span data-ttu-id="952ec-143">Não há nenhuma mensagem de erro para essa condição, exceto que ocorra no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="952ec-143">There is no error message for this condition, except that which occurs in the event log.</span></span> <span data-ttu-id="952ec-144">A instalação do MBAM sem scripts e ferramentas de gerenciamento do IIS faz com que as operações de backup não sejam executadas para MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-144">Installation of MBAM without IIS Management Scripts and Tools causes the backup operations not to run for MBAM.</span></span>

<span data-ttu-id="952ec-145">**Solução alternativa:** Verifique se o recurso do servidor Web de ferramentas e scripts de gerenciamento do IIS está instalado antes de iniciar a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-145">**WORKAROUND:** Ensure that the IIS Management Scripts and Tools web server feature is installed before you start the MBAM Setup.</span></span>

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a><span data-ttu-id="952ec-146">MBAM a instalação parar de responder durante a fase "Instalando recursos selecionados" quando a configuração estiver configurada para usar um certificado</span><span class="sxs-lookup"><span data-stu-id="952ec-146">MBAM Setup stops responding during the “Installing selected features” phase when setup is configured to use a certificate</span></span>

<span data-ttu-id="952ec-147">MBAM a instalação parar de responder durante a fase de instalação dos **recursos selecionados** da instalação.</span><span class="sxs-lookup"><span data-stu-id="952ec-147">MBAM Setup stops responding during the **Installing selected features** phase of setup.</span></span> <span data-ttu-id="952ec-148">Isso ocorre durante a instalação do banco de dados de recuperação e do banco de dados de hardware ou de status de conformidade após a seleção da opção **usar um certificado para criptografar a comunicação de rede** .</span><span class="sxs-lookup"><span data-stu-id="952ec-148">This occurs during the installation of the Recovery and Hardware Database or the Compliance Status Database, after you select the **Use a certificate to encrypt the network communication** option.</span></span> <span data-ttu-id="952ec-149">Além disso, a configuração do MBAM para de responder se a instância do mecanismo de banco de dados do SQL Server não puder acessar o certificado especificado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="952ec-149">Furthermore, the MBAM Setup stops responding if the instance of the SQL Server Database Engine cannot access the certificate that was specified during setup.</span></span>

<span data-ttu-id="952ec-150">**Solução alternativa:** Atualize as permissões no certificado, para que o serviço do Windows para a instância aplicável do mecanismo de banco de dados do SQL Server possa acessar o certificado.</span><span class="sxs-lookup"><span data-stu-id="952ec-150">**WORKAROUND:** Update the permissions on the certificate, so that the Windows service for the applicable instance of the SQL Server Database Engine can access the certificate.</span></span> <span data-ttu-id="952ec-151">Você também pode alterar a conta na qual a instância do mecanismo de banco de dados do SQL Server é executada, para o mecanismo de banco de dados usar o certificado.</span><span class="sxs-lookup"><span data-stu-id="952ec-151">You can also change the account under which the instance of the SQL Server Database Engine runs, for the database engine to use the certificate.</span></span> <span data-ttu-id="952ec-152">Para determinar as permissões do certificado, digite o seguinte comando no prompt de comando: **certutil-v-armazenar minha**</span><span class="sxs-lookup"><span data-stu-id="952ec-152">To determine the permissions for the certificate, type the following command at the command prompt: **certutil -v -store MY**</span></span>

### <span data-ttu-id="952ec-153">A instalação do MBAM pausará ao instalar o SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="952ec-153">MBAM Setup pauses when you install SQL Server Reporting Services</span></span>

<span data-ttu-id="952ec-154">Durante a instalação do MBAM, quando você seleciona uma instância do SQL Server Reporting Services (SSRS) e a instância do SSRS não está disponível ou está configurada incorretamente, a configuração do MBAM pode pausar por até um minuto enquanto tenta se comunicar com a instância do SSRS.</span><span class="sxs-lookup"><span data-stu-id="952ec-154">During MBAM installation, when you select an instance of SQL Server Reporting Services (SSRS) and SSRS instance is not available or it is configured incorrectly, the MBAM Setup might pause for up to one minute while it attempts to communicate with the SSRS instance.</span></span>

<span data-ttu-id="952ec-155">**Solução alternativa:** Aguarde pelo menos um minuto para que a instalação do MBAM retome enquanto o programa de instalação tenta entrar em contato com a instância do SSRS.</span><span class="sxs-lookup"><span data-stu-id="952ec-155">**WORKAROUND:** Wait for at least one minute for MBAM Setup to resume while the Setup program attempts to contact the instance of SSRS.</span></span>

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a><span data-ttu-id="952ec-156">O servidor de administração e monitoramento não é executado após a instalação</span><span class="sxs-lookup"><span data-stu-id="952ec-156">Administration and Monitoring Server does not run after setup</span></span>

<span data-ttu-id="952ec-157">Após a instalação do MBAM instalar com êxito o recurso de servidor de administração e monitoramento, o MBAM exibe mensagens de erro quando você tenta acessar o site do administrador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-157">After MBAM Setup successfully installs the Administration and Monitoring Server feature, MBAM displays error messages when you try to access the MBAM administrator website.</span></span> <span data-ttu-id="952ec-158">Esse problema ocorre por um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="952ec-158">This issue occurs for one of the following reasons:</span></span>

-   <span data-ttu-id="952ec-159">Um ou mais pré-requisitos no servidor de administração e monitoramento foram removidos após a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-159">One or more prerequisites on the Administration and Monitoring Server were removed after the MBAM installation.</span></span>

-   <span data-ttu-id="952ec-160">Um ou mais pré-requisitos foram instalados no servidor e mais tarde foram removidos antes de executar a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="952ec-160">One or more prerequisites were installed on the server and later they were removed before running the MBAM Setup.</span></span>

<span data-ttu-id="952ec-161">**Solução alternativa:** Examine a documentação do MBAM e confirme se todos os pré-requisitos do MBAM estão instalados.</span><span class="sxs-lookup"><span data-stu-id="952ec-161">**WORKAROUND:** Review the MBAM documentation and confirm that all MBAM prerequisites are installed.</span></span>

### <span data-ttu-id="952ec-162">Clicar em links de documentação durante a instalação resulta em um erro de aplicativo após a conclusão da instalação</span><span class="sxs-lookup"><span data-stu-id="952ec-162">Clicking documentation links during Setup results in an application error after Setup is finished</span></span>

<span data-ttu-id="952ec-163">Quando você clica em um link de documentação durante a instalação e, em seguida, fecha o programa de instalação clicando em **Cancelar** ou em **concluir** após a conclusão da instalação, uma mensagem de erro do aplicativo é exibida...</span><span class="sxs-lookup"><span data-stu-id="952ec-163">When you click a documentation link during setup and then close the Setup program by clicking **Cancel** or **Finish** after Setup has successfully finished, an application error message appears..</span></span> <span data-ttu-id="952ec-164">O problema é causado por um erro de violação de acesso no Agendador de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="952ec-164">The problem is caused by an access violation error in the Windows Task Scheduler.</span></span>

<span data-ttu-id="952ec-165">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="952ec-165">**WORKAROUND:** None.</span></span> <span data-ttu-id="952ec-166">Você pode ignorar esse erro.</span><span class="sxs-lookup"><span data-stu-id="952ec-166">You can ignore this error.</span></span>

### <span data-ttu-id="952ec-167">Falha na configuração do MBAM não remove novos bancos de dados</span><span class="sxs-lookup"><span data-stu-id="952ec-167">Failed MBAM Setup does not remove new databases</span></span>

<span data-ttu-id="952ec-168">Se a configuração do MBAM falhar, a instalação pode não remover os bancos de dados recém-criados.</span><span class="sxs-lookup"><span data-stu-id="952ec-168">If the MBAM Setup fails, Setup might not remove the newly created databases.</span></span> <span data-ttu-id="952ec-169">Isso pode causar falhas durante instalações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="952ec-169">This can cause failures during subsequent installations.</span></span>

<span data-ttu-id="952ec-170">**Solução alternativa:** Escolha um nome diferente para a instância do banco de dados durante a instalação subsequente.</span><span class="sxs-lookup"><span data-stu-id="952ec-170">**WORKAROUND:** Choose a different name for the database instance during the subsequent installation.</span></span>

### <span data-ttu-id="952ec-171">A instalação do MBAM não reconhece certificados de cluster de balanceamento de carga de rede válidos</span><span class="sxs-lookup"><span data-stu-id="952ec-171">MBAM Setup does not recognize valid network load-balancing cluster certificates</span></span>

<span data-ttu-id="952ec-172">Durante a instalação do MBAM Administration and Monitoring Server, com a opção de criptografia de rede selecionada, o certificado do cluster não é reconhecido como um certificado válido.</span><span class="sxs-lookup"><span data-stu-id="952ec-172">During the MBAM Administration and Monitoring Server installation, with the network encryption option selected, the cluster certificate is not recognized as a valid certificate.</span></span> <span data-ttu-id="952ec-173">Ele é reconhecido como válido quando o certificado para comunicação com o banco de dados é instalado, mas é rejeitado para comunicação pelo cluster de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="952ec-173">It is recognized as valid when the certificate for communication with the database is installed, but it is rejected for communication by the load-balancing cluster.</span></span>

<span data-ttu-id="952ec-174">**Solução alternativa:** Confirme se a lista de certificados revogados (CRL) associada ao certificado está acessível ou use um certificado que não exija validação usando a CRL.</span><span class="sxs-lookup"><span data-stu-id="952ec-174">**WORKAROUND:** Confirm that the certificate revocation list (CRL) associated with the certificate is accessible, or use a certificate that does not require validation by using the CRL.</span></span>

## <span data-ttu-id="952ec-175">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="952ec-175">Release Notes Copyright Information</span></span>


<span data-ttu-id="952ec-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="952ec-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="952ec-177">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="952ec-177">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="952ec-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="952ec-178">Related topics</span></span>


[<span data-ttu-id="952ec-179">Sobre o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="952ec-179">About MBAM 1.0</span></span>](about-mbam-10.md)

 

 





