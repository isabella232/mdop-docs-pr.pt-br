---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799159"
---
# <span data-ttu-id="2e59c-103">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="2e59c-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="2e59c-104">Para recuperar uma unidade corrompida protegida pelo BitLocker, um usuário de suporte técnico do Microsoft BitLocker Administration and Monitoring (MBAM) precisará criar um arquivo de pacote de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e59c-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="2e59c-105">Esse arquivo de pacote pode ser copiado para o computador que contém a unidade corrompida e, em seguida, usado para recuperar a unidade.</span><span class="sxs-lookup"><span data-stu-id="2e59c-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="2e59c-106">Use o procedimento a seguir para as etapas necessárias para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="2e59c-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="2e59c-107">**Importante**  Para evitar uma possível perda de dados, é altamente recomendável que você leia a ajuda "reparar-bde" e entenda claramente como usar o comando antes de concluir as instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e59c-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="2e59c-108">Para recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="2e59c-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="2e59c-109">Para criar o pacote de chave de recuperação necessário para recuperar uma unidade corrompida, inicie um navegador da Web e abra o site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2e59c-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="2e59c-110">Selecione **recuperação de unidade** no painel de navegação à esquerda.</span><span class="sxs-lookup"><span data-stu-id="2e59c-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="2e59c-111">Digite o nome de domínio do usuário, o nome de usuário, motivo para desbloquear a unidade e a ID da senha de recuperação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2e59c-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="2e59c-112">**Observação**  Se você for membro da função Administradores de suporte técnico, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="2e59c-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="2e59c-113">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="2e59c-113">Click **Submit**.</span></span> <span data-ttu-id="2e59c-114">A chave de recuperação será exibida.</span><span class="sxs-lookup"><span data-stu-id="2e59c-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="2e59c-115">Clique em **salvar**e selecione **pacote de chave de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="2e59c-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="2e59c-116">O pacote da chave de recuperação será criado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="2e59c-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="2e59c-117">Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="2e59c-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="2e59c-118">Abra um prompt de comando com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2e59c-118">Open an elevated command prompt.</span></span> <span data-ttu-id="2e59c-119">Para fazer isso, clique em **Iniciar** e digite `cmd` na **caixa Pesquisar programas e arquivos**.</span><span class="sxs-lookup"><span data-stu-id="2e59c-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="2e59c-120">Clique com o botão direito do mouse **cmd.exe** e selecione **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="2e59c-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="2e59c-121">No prompt de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2e59c-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="2e59c-122">**Observação**  Substitua &lt; unidade fixa &gt; por uma unidade de disco rígido disponível com espaço livre igual ou maior que os dados na unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="2e59c-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="2e59c-123">Os dados na unidade corrompida são recuperados e movidos para a unidade de disco rígido especificada.</span><span class="sxs-lookup"><span data-stu-id="2e59c-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="2e59c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e59c-124">Related topics</span></span>


[<span data-ttu-id="2e59c-125">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="2e59c-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





