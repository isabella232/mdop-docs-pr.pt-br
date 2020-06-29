---
title: Como usar o Portal de Assistência Técnica
description: Como usar o Portal de Assistência Técnica
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799850"
---
# <span data-ttu-id="1cf8a-103">Como usar o Portal de Assistência Técnica</span><span class="sxs-lookup"><span data-stu-id="1cf8a-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="1cf8a-104">O site de administração e monitoramento do MBAM, também chamado de portal de suporte técnico, é uma interface administrativa para a criptografia de unidade de disco BitLocker instalada como parte da infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="1cf8a-105">As seções a seguir descrevem como você pode usar este site para analisar relatórios, recuperar unidades de usuários finais e gerenciar os usuários finais TPMs.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="1cf8a-106">Relatórios</span><span class="sxs-lookup"><span data-stu-id="1cf8a-106">Reports</span></span>


<span data-ttu-id="1cf8a-107">O MBAM coleta informações dos computadores do Active Directory e do cliente, o que permite que você execute relatórios diferentes para monitorar o uso e a conformidade do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="1cf8a-108">Usando a seção **relatórios** do site Administração e monitoramento, você pode gerar relatórios sobre conformidade empresarial, computadores individuais e atividades de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="1cf8a-109">Para obter uma descrição de cada relatório, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="1cf8a-110">Para acessar relatórios</span><span class="sxs-lookup"><span data-stu-id="1cf8a-110">To access reports</span></span>**

1.  <span data-ttu-id="1cf8a-111">Abra um navegador da Web e navegue até o site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="1cf8a-112">Selecione **relatórios** no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="1cf8a-113">Na barra de menus superior, selecione o tipo de relatório que deseja gerar.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="1cf8a-114">Para salvar relatórios, clique no botão **Exportar** na barra de menus relatórios.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="1cf8a-115">Para obter informações adicionais sobre como executar relatórios do MBAM, consulte [como gerar relatórios do MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="1cf8a-116">Recuperação de unidade</span><span class="sxs-lookup"><span data-stu-id="1cf8a-116">Drive Recovery</span></span>


<span data-ttu-id="1cf8a-117">O recurso de **recuperação de unidade** do site de administração e monitoramento permite aos usuários com funções específicas de administrador (por exemplo, usuários de suporte técnico) para acessar dados de chave de recuperação coletados pelo cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="1cf8a-118">Esses dados podem ser usados para acessar uma unidade protegida pelo BitLocker quando o BitLocker entra no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="1cf8a-119">Para obter instruções sobre como recuperar uma unidade que está no modo de recuperação, consulte [como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="1cf8a-120">Você também pode recuperar unidades que foram movidas ou que estão corrompidas:</span><span class="sxs-lookup"><span data-stu-id="1cf8a-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="1cf8a-121">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="1cf8a-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="1cf8a-122">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="1cf8a-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="1cf8a-123">Para obter informações adicionais sobre como recuperar uma unidade protegida pelo BitLocker, consulte [executando o gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="1cf8a-124">Gerenciar TPM</span><span class="sxs-lookup"><span data-stu-id="1cf8a-124">Manage TPM</span></span>


<span data-ttu-id="1cf8a-125">O recurso gerenciar TPM do site de administração e monitoramento oferece aos usuários certas funções de administrador (por exemplo, "usuários da assistência técnica MBAM") acessados com dados do TPM que foram coletados pelo cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="1cf8a-126">Em um bloqueio de TPM, um administrador pode usar o site de administração e monitoramento para recuperar o arquivo de senha necessário para desbloquear o TPM.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="1cf8a-127">Para obter instruções sobre como redefinir um TPM após um bloqueio de TPM, consulte [como redefinir um bloqueio de TPM](how-to-reset-a-tpm-lockout-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="1cf8a-128">Tarefas do suporte técnico do MBAM</span><span class="sxs-lookup"><span data-stu-id="1cf8a-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="1cf8a-129">Você pode usar o site de administração e monitoramento para várias tarefas administrativas, como o gerenciamento de hardware protegido pelo BitLocker, a recuperação de unidades e a execução de relatórios.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="1cf8a-130">Por padrão, a URL para o site de administração e monitoramento é http:// &lt; *MBAMAdministrationServername* &gt; , embora você possa personalizá-lo durante o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="1cf8a-131">**Observação**  Para acessar os vários recursos oferecidos pelo site de administração e monitoramento, você deve ter as funções adequadas associadas à sua conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="1cf8a-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="1cf8a-132">Para obter mais informações sobre noções básicas sobre funções de usuário, consulte [como gerenciar funções de administrador MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1cf8a-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="1cf8a-133">Use os links a seguir para encontrar informações sobre as tarefas que você pode executar usando o site Administração e monitoramento:</span><span class="sxs-lookup"><span data-stu-id="1cf8a-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="1cf8a-134">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="1cf8a-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="1cf8a-135">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="1cf8a-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="1cf8a-136">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="1cf8a-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="1cf8a-137">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="1cf8a-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="1cf8a-138">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="1cf8a-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





