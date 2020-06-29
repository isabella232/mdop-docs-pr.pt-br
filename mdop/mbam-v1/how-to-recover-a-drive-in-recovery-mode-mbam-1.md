---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796128"
---
# <span data-ttu-id="41d2e-103">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="41d2e-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="41d2e-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) incluem recursos de recuperação de unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="41d2e-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="41d2e-105">Esses recursos garantem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o BitLocker coloca esse volume em modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="41d2e-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="41d2e-106">Um volume protegido pelo BitLocker entra no modo de recuperação quando um PIN ou uma senha é perdido ou esquecido ou quando o chip TPM detecta uma alteração na BIOS ou arquivos de inicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="41d2e-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="41d2e-107">Use este procedimento para acessar o sistema de dados de recuperação de chave centralizada que pode fornecer uma senha de recuperação quando for fornecida uma ID de senha de recuperação e um identificador de usuário associado.</span><span class="sxs-lookup"><span data-stu-id="41d2e-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="41d2e-108">**Importante**  MBAM gera chaves de recuperação de uso único.</span><span class="sxs-lookup"><span data-stu-id="41d2e-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="41d2e-109">Sob essa limitação, uma chave de recuperação pode ser usada apenas uma vez e, em seguida, não é mais válida.</span><span class="sxs-lookup"><span data-stu-id="41d2e-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="41d2e-110">O uso único de uma senha de recuperação é aplicado automaticamente a unidades de sistema operacional e unidades fixas.</span><span class="sxs-lookup"><span data-stu-id="41d2e-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="41d2e-111">Em unidades removíveis, o uso único é aplicado quando a unidade é removida e, em seguida, reinserida e desbloqueada em um computador com as configurações de política de grupo ativadas para gerenciar unidades removíveis.</span><span class="sxs-lookup"><span data-stu-id="41d2e-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="41d2e-112">Para recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="41d2e-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="41d2e-113">Abra o site do MBAM.</span><span class="sxs-lookup"><span data-stu-id="41d2e-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="41d2e-114">No painel de navegação, clique em **recuperação de unidade**.</span><span class="sxs-lookup"><span data-stu-id="41d2e-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="41d2e-115">A página da Web de **recuperação de acesso a uma unidade criptografada** é aberta.</span><span class="sxs-lookup"><span data-stu-id="41d2e-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="41d2e-116">Insira o domínio de logon do Windows do usuário e o nome de usuário e os primeiros oito dígitos da ID da chave de recuperação para receber uma lista de possíveis chaves de recuperação correspondentes.</span><span class="sxs-lookup"><span data-stu-id="41d2e-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="41d2e-117">Você também pode inserir a ID da chave de recuperação inteira para receber a chave de recuperação exata.</span><span class="sxs-lookup"><span data-stu-id="41d2e-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="41d2e-118">Selecione uma das opções predefinidas na lista suspensa **razão para desbloquear unidade** e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="41d2e-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="41d2e-119">**Observação**  Se você for um usuário de helpdesk avançado do MBAM, as entradas de domínio de usuário e identificação de usuário não serão obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="41d2e-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="41d2e-120">MBAM retornará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="41d2e-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="41d2e-121">Uma mensagem de erro se nenhuma senha de recuperação correspondente for encontrada</span><span class="sxs-lookup"><span data-stu-id="41d2e-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="41d2e-122">Várias correspondências possíveis se o usuário tiver várias senhas de recuperação correspondentes</span><span class="sxs-lookup"><span data-stu-id="41d2e-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="41d2e-123">A senha de recuperação e o pacote de recuperação para o usuário enviado</span><span class="sxs-lookup"><span data-stu-id="41d2e-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="41d2e-124">**Observação**  Se você estiver recuperando uma unidade danificada, a opção pacote de recuperação fornece o BitLocker com as informações críticas necessárias para tentar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="41d2e-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="41d2e-125">Depois que a senha de recuperação e o pacote de recuperação forem recuperados, a senha de recuperação será exibida.</span><span class="sxs-lookup"><span data-stu-id="41d2e-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="41d2e-126">Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em um email ou em outro arquivo de texto para armazenamento temporário.</span><span class="sxs-lookup"><span data-stu-id="41d2e-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="41d2e-127">Ou, para salvar a senha de recuperação em um arquivo, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="41d2e-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="41d2e-128">Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="41d2e-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="41d2e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41d2e-129">Related topics</span></span>


[<span data-ttu-id="41d2e-130">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="41d2e-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





