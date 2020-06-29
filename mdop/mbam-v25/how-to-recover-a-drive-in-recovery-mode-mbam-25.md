---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799258"
---
# <span data-ttu-id="65237-103">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="65237-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="65237-104">Este tópico explica como usar o site de administração e monitoramento (também conhecido como o Help Desk) para obter uma senha de recuperação para fornecer aos usuários finais se a unidade protegida pelo BitLocker entrar no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65237-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="65237-105">As unidades entram no modo de recuperação se os usuários perdem ou esquecem o PIN ou a senha ou se o chip TPM (Trusted Module Platform) detecta alterações nos arquivos do BIOS ou da inicialização de um computador.</span><span class="sxs-lookup"><span data-stu-id="65237-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="65237-106">Para obter uma senha de recuperação, use a área de **recuperação de unidade** do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="65237-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="65237-107">Você deve receber a função usuários da assistência técnica MBAM ou a função usuários avançados da assistência técnica do MBAM para acessar esta área do site.</span><span class="sxs-lookup"><span data-stu-id="65237-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="65237-108">Observação</span><span class="sxs-lookup"><span data-stu-id="65237-108">Note</span></span>**  
<span data-ttu-id="65237-109">Você pode ter atribuído a essas funções nomes diferentes quando você as criou.</span><span class="sxs-lookup"><span data-stu-id="65237-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="65237-110">Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="65237-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="65237-111">Importante</span><span class="sxs-lookup"><span data-stu-id="65237-111">Important</span></span>**  
<span data-ttu-id="65237-112">As senhas de recuperação expiram após um único uso.</span><span class="sxs-lookup"><span data-stu-id="65237-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="65237-113">Em unidades do sistema operacional e unidades de dados fixas, a regra de uso único é aplicada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="65237-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="65237-114">Em unidades removíveis, ele é aplicado quando a unidade é removida e, em seguida, reinserida e desbloqueada em um computador com configurações de política de grupo ativadas para gerenciar unidades removíveis.</span><span class="sxs-lookup"><span data-stu-id="65237-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="65237-115">Para recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="65237-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="65237-116">Abra um navegador da Web e navegue até o **site de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="65237-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="65237-117">No painel esquerdo, selecione **recuperação de unidade** para abrir a página **recuperar acesso a uma unidade criptografada** .</span><span class="sxs-lookup"><span data-stu-id="65237-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="65237-118">Insira o domínio de logon do Windows do usuário final e o nome de usuário para exibir informações de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65237-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="65237-119">Observação</span><span class="sxs-lookup"><span data-stu-id="65237-119">Note</span></span>**  
    <span data-ttu-id="65237-120">Se você estiver no grupo usuários da assistência avançada do MBAM, os campos domínio do usuário e ID do usuário não serão necessários.</span><span class="sxs-lookup"><span data-stu-id="65237-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="65237-121">Insira os primeiros oito dígitos da ID da chave de recuperação para ver uma lista de possíveis chaves de recuperação correspondentes ou digite a ID da chave de recuperação inteira para obter a chave de recuperação exata.</span><span class="sxs-lookup"><span data-stu-id="65237-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="65237-122">Na lista **motivo da desbloqueio de unidade** , selecione uma das opções predefinidas e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="65237-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="65237-123">MBAM retornará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="65237-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="65237-124">Uma mensagem de erro se nenhuma senha de recuperação correspondente for encontrada</span><span class="sxs-lookup"><span data-stu-id="65237-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="65237-125">Várias correspondências possíveis se o usuário tiver várias senhas de recuperação correspondentes</span><span class="sxs-lookup"><span data-stu-id="65237-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="65237-126">A senha de recuperação e o pacote de recuperação para o usuário enviado</span><span class="sxs-lookup"><span data-stu-id="65237-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="65237-127">Observação</span><span class="sxs-lookup"><span data-stu-id="65237-127">Note</span></span>**  
        <span data-ttu-id="65237-128">Se você estiver recuperando uma unidade danificada, a opção pacote de recuperação fornece o BitLocker com informações críticas necessárias para a recuperação da unidade.</span><span class="sxs-lookup"><span data-stu-id="65237-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="65237-129">Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="65237-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="65237-130">Ou, se preferir, clique em **salvar** para salvar a senha de recuperação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="65237-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="65237-131">Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="65237-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="65237-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65237-132">Related topics</span></span>


[<span data-ttu-id="65237-133">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="65237-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="65237-134">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="65237-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="65237-135">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="65237-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="65237-136">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="65237-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





