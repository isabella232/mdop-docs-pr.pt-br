---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799595"
---
# <span data-ttu-id="d1a23-103">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="d1a23-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="d1a23-104">O recurso de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) abrange tanto a captura quanto o armazenamento de dados quanto a disponibilidade para ferramentas necessárias para gerenciar o TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="d1a23-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="d1a23-105">Este tópico aborda como acessar o sistema de dados de recuperação de chave centralizada no site de administração e monitoramento, que pode fornecer um arquivo de senha de proprietário do TPM quando uma ID de computador e um identificador de usuário associado são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d1a23-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="d1a23-106">Um bloqueio de TPM pode ocorrer se um usuário inserir o PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="d1a23-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="d1a23-107">O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="d1a23-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="d1a23-108">Você só pode redefinir um bloqueio de TPM se MBAM for proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d1a23-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="d1a23-109">Para redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="d1a23-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="d1a23-110">Abra um navegador da Web e navegue até o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d1a23-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="d1a23-111">No painel de navegação à esquerda, selecione **gerenciar TPM** para abrir a página **gerenciar TPM** .</span><span class="sxs-lookup"><span data-stu-id="d1a23-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="d1a23-112">Digite o nome de domínio totalmente qualificado para o computador e o nome do computador e insira o domínio de logon do Windows do usuário e o nome de usuário do usuário para recuperar o arquivo de senha de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d1a23-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="d1a23-113">Na lista o motivo da solicitação **de arquivo de senha de proprietário do TPM** , selecione um motivo para a solicitação e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="d1a23-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="d1a23-114">MBAM retorna um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d1a23-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="d1a23-115">Uma mensagem de erro, se não for encontrado um arquivo de senha de proprietário do TPM correspondente</span><span class="sxs-lookup"><span data-stu-id="d1a23-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="d1a23-116">O arquivo de senha de proprietário do TPM para o computador enviado</span><span class="sxs-lookup"><span data-stu-id="d1a23-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="d1a23-117">Observação</span><span class="sxs-lookup"><span data-stu-id="d1a23-117">Note</span></span>**  
    <span data-ttu-id="d1a23-118">Se você for um usuário avançado da assistência técnica, os campos de usuário e ID de usuário do usuário não são necessários.</span><span class="sxs-lookup"><span data-stu-id="d1a23-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="d1a23-119">Para salvar a senha em um arquivo. TPM, clique no botão **salvar** .</span><span class="sxs-lookup"><span data-stu-id="d1a23-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="d1a23-120">O usuário executará o console de gerenciamento do TPM, selecionará a opção **Redefinir bloqueio do TPM** e fornecerá o arquivo de senha de proprietário do TPM para redefinir o bloqueio do TPM.</span><span class="sxs-lookup"><span data-stu-id="d1a23-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="d1a23-121">Importante</span><span class="sxs-lookup"><span data-stu-id="d1a23-121">Important</span></span>**  
   <span data-ttu-id="d1a23-122">Os administradores de suporte técnico não devem fornecer o valor de hash TPM ou o arquivo de senha de proprietário do TPM aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="d1a23-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="d1a23-123">As informações do TPM não são alteradas, portanto, ele pode representar um risco de segurança se o arquivo for fornecido para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="d1a23-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="d1a23-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1a23-124">Related topics</span></span>


[<span data-ttu-id="d1a23-125">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="d1a23-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









