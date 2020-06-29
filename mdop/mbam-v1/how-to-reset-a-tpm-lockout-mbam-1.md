---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796120"
---
# <span data-ttu-id="bb022-103">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="bb022-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="bb022-104">O recurso de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) abrange tanto a captura quanto o armazenamento de dados quanto a disponibilidade para ferramentas necessárias para gerenciar o TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="bb022-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="bb022-105">Este tópico aborda como acessar o sistema de dados de recuperação de chave centralizada no site de administração do bit \ _admmon \ _tlanextref.</span><span class="sxs-lookup"><span data-stu-id="bb022-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="bb022-106">O sistema de dados de recuperação de chave pode fornecer um arquivo de senha de proprietário do TPM quando a identidade do computador e o identificador de usuário associado são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bb022-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="bb022-107">Um bloqueio de TPM pode ocorrer se um usuário inserir um PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="bb022-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="bb022-108">O número de vezes que um usuário pode inserir um PIN incorreto antes de o bloqueio do TPM se basear na especificação do fabricante do computador.</span><span class="sxs-lookup"><span data-stu-id="bb022-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="bb022-109">Para redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="bb022-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="bb022-110">Abra o site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="bb022-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="bb022-111">No painel de navegação, selecione **gerenciar TPM**.</span><span class="sxs-lookup"><span data-stu-id="bb022-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="bb022-112">Isso abre a página **gerenciar TPM** .</span><span class="sxs-lookup"><span data-stu-id="bb022-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="bb022-113">Digite o nome de domínio totalmente qualificado (FQDN) para o computador e o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="bb022-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="bb022-114">Insira o domínio de logon do Windows do usuário e o nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb022-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="bb022-115">Selecione uma das opções predefinidas no menu suspenso o **arquivo de senha de proprietário do TPM** .</span><span class="sxs-lookup"><span data-stu-id="bb022-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="bb022-116">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="bb022-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="bb022-117">MBAM retornará um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb022-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="bb022-118">Uma mensagem de erro se não for encontrado um arquivo de senha de proprietário do TPM correspondente</span><span class="sxs-lookup"><span data-stu-id="bb022-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="bb022-119">O arquivo de senha de proprietário do TPM para o computador enviado</span><span class="sxs-lookup"><span data-stu-id="bb022-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="bb022-120">**Observação**  Se você for um usuário avançado da assistência técnica, os campos de usuário e ID de usuário do usuário não são necessários.</span><span class="sxs-lookup"><span data-stu-id="bb022-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="bb022-121">Após a recuperação, a senha do proprietário será exibida.</span><span class="sxs-lookup"><span data-stu-id="bb022-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="bb022-122">Para salvar esta senha em um arquivo. TPM, clique no botão **salvar** .</span><span class="sxs-lookup"><span data-stu-id="bb022-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="bb022-123">O usuário executará o console de gerenciamento do TPM e selecionará a opção **Redefinir bloqueio do TPM** e fornecerá o arquivo de senha de proprietário do TPM para redefinir o bloqueio do TPM.</span><span class="sxs-lookup"><span data-stu-id="bb022-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="bb022-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb022-124">Related topics</span></span>


[<span data-ttu-id="bb022-125">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="bb022-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





