---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799596"
---
# <span data-ttu-id="7aaa9-103">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="7aaa9-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="7aaa9-104">Os recursos de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) garantem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o BitLocker entra no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="7aaa9-105">Um volume protegido pelo BitLocker entra no modo de recuperação quando um PIN ou uma senha é perdido ou esquecido, ou quando o chip TPM (plataforma de módulo confiável) detecta alterações nos arquivos do BIOS ou da inicialização de um computador.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="7aaa9-106">Use este procedimento para acessar o sistema de dados de recuperação de chave centralizada, que pode fornecer uma senha de recuperação se uma ID de senha de recuperação e um identificador de usuário associado forem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="7aaa9-107">Importante</span><span class="sxs-lookup"><span data-stu-id="7aaa9-107">Important</span></span>**  
<span data-ttu-id="7aaa9-108">A administração e o monitoramento do Microsoft BitLocker usam chaves de recuperação de uso único que expiram em uso.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="7aaa9-109">O uso único de uma senha de recuperação é aplicado automaticamente a unidades de sistema operacional e unidades fixas.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="7aaa9-110">Em unidades removíveis, ele é aplicado quando a unidade é removida e, em seguida, reinserida em um computador com configurações de política de grupo ativadas para gerenciar unidades removíveis.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="7aaa9-111">Para recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="7aaa9-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="7aaa9-112">Abra um navegador da Web e navegue até o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="7aaa9-113">No painel de navegação, clique em **recuperação de unidade**.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="7aaa9-114">A página da Web "recuperação do acesso a uma unidade criptografada" é aberta.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="7aaa9-115">Insira o domínio de logon do Windows e o nome de usuário do usuário para exibir informações de recuperação e os primeiros oito dígitos da ID da chave de recuperação para receber uma lista de chaves de recuperação correspondentes ou a ID da chave de recuperação inteira para receber a chave de recuperação exata.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="7aaa9-116">Selecione uma das opções predefinidas da lista **motivo da desbloqueio de unidade** e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="7aaa9-117">Observação</span><span class="sxs-lookup"><span data-stu-id="7aaa9-117">Note</span></span>**  
    <span data-ttu-id="7aaa9-118">Se você for um usuário de helpdesk avançado do MBAM, as entradas de domínio de usuário e identificação de usuário não serão obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="7aaa9-119">Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="7aaa9-120">Ou, se preferir, clique em **salvar** para salvar a senha de recuperação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="7aaa9-121">Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="7aaa9-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="7aaa9-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7aaa9-122">Related topics</span></span>


[<span data-ttu-id="7aaa9-123">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="7aaa9-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









