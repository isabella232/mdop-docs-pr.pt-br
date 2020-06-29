---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799249"
---
# <span data-ttu-id="8f05a-103">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="8f05a-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="8f05a-104">Este tópico explica como usar o site de administração e monitoramento (também chamado de suporte técnico) para redefinir um bloqueio do TPM.</span><span class="sxs-lookup"><span data-stu-id="8f05a-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="8f05a-105">Os bloqueios do TPM podem ocorrer se um usuário final digitar o PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="8f05a-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="8f05a-106">O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="8f05a-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="8f05a-107">Na área **gerenciar TPM** do site de administração e monitoramento, você pode acessar o sistema de dados de recuperação de chave centralizada, que fornece um arquivo de senha de proprietário do TPM quando você fornecer uma ID de computador e um identificador de usuário associado.</span><span class="sxs-lookup"><span data-stu-id="8f05a-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="8f05a-108">Para acessar a área gerenciar TPM do site de administração e monitoramento, você deve receber a função usuários da assistência técnica MBAM ou a função usuários avançados da assistência técnica do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8f05a-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="8f05a-109">Essas funções são grupos que os administradores criam no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f05a-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="8f05a-110">Você pode usar qualquer nome para estes grupos.</span><span class="sxs-lookup"><span data-stu-id="8f05a-110">You can use any name for these groups.</span></span> <span data-ttu-id="8f05a-111">Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="8f05a-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="8f05a-112">Para obter informações sobre a propriedade MBAM e TPM, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="8f05a-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="8f05a-113">Para redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="8f05a-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="8f05a-114">Abra um navegador da Web e navegue até o **site de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="8f05a-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="8f05a-115">No painel esquerdo, clique em **gerenciar TPM** para abrir a página **gerenciar TPM** .</span><span class="sxs-lookup"><span data-stu-id="8f05a-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="8f05a-116">Digite o nome de domínio totalmente qualificado para o computador e o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="8f05a-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="8f05a-117">Insira o domínio de logon do Windows do usuário final e o nome de usuário para recuperar o arquivo de senha de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="8f05a-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="8f05a-118">**Observação**  Se você estiver no grupo usuários da assistência avançada do MBAM, os campos domínio do usuário e ID do usuário não serão necessários.</span><span class="sxs-lookup"><span data-stu-id="8f05a-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="8f05a-119">Na lista o motivo da solicitação **de arquivo de senha de proprietário do TPM** , selecione um motivo para a solicitação e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="8f05a-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="8f05a-120">MBAM retorna um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="8f05a-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="8f05a-121">Uma mensagem de erro se não for encontrado um arquivo de senha de proprietário do TPM correspondente</span><span class="sxs-lookup"><span data-stu-id="8f05a-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="8f05a-122">O arquivo de senha de proprietário do TPM para o computador enviado</span><span class="sxs-lookup"><span data-stu-id="8f05a-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="8f05a-123">Depois que a senha de proprietário do TPM for recuperada, a senha de proprietário será exibida.</span><span class="sxs-lookup"><span data-stu-id="8f05a-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="8f05a-124">Para salvar a senha em um arquivo. TPM, clique no botão **salvar** .</span><span class="sxs-lookup"><span data-stu-id="8f05a-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="8f05a-125">Na área **gerenciar TPM** do site de **Administração e monitoramento**, selecione a opção **Redefinir bloqueio do TPM** e forneça o arquivo de senha de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="8f05a-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="8f05a-126">O bloqueio do TPM é redefinido e o acesso do usuário final é restaurado.</span><span class="sxs-lookup"><span data-stu-id="8f05a-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="8f05a-127">**Importante**  Não forneça o valor de hash TPM ou o arquivo de senha de proprietário do TPM aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="8f05a-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="8f05a-128">Como as informações do TPM não são alteradas, a atribuição de um arquivo aos usuários finais cria um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="8f05a-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="8f05a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f05a-129">Related topics</span></span>


[<span data-ttu-id="8f05a-130">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8f05a-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="8f05a-131">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="8f05a-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8f05a-132">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8f05a-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8f05a-133">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8f05a-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





