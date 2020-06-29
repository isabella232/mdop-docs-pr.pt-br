---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796126"
---
# <span data-ttu-id="8bdb3-103">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="8bdb3-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="8bdb3-104">Para recuperar uma unidade corrompida que foi protegida pelo BitLocker, um usuário de suporte técnico de administração e monitoramento do Microsoft BitLocker (MBAM) deve criar um arquivo de pacote de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="8bdb3-105">Este arquivo de pacote pode ser copiado para o computador que contém a unidade corrompida e, em seguida, usado para recuperar a unidade.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="8bdb3-106">Para fazer isso, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="8bdb3-107">Para recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="8bdb3-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="8bdb3-108">Abra o site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="8bdb3-109">Selecione **recuperação de unidade** no painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="8bdb3-110">Digite o nome de domínio e o nome de usuário do usuário, o motivo para desbloquear a unidade e a ID da senha de recuperação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="8bdb3-111">**Observação**  Se você for membro da função Administradores de suporte técnico, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="8bdb3-112">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-112">Click **Submit**.</span></span> <span data-ttu-id="8bdb3-113">A chave de recuperação será exibida.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="8bdb3-114">Clique em **salvar**e selecione **pacote de chave de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="8bdb3-115">O pacote da chave de recuperação será criado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="8bdb3-116">Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="8bdb3-117">Abra um prompt de comando com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-117">Open an elevated command prompt.</span></span> <span data-ttu-id="8bdb3-118">Para fazer isso, clique em **Iniciar** e digite `cmd` na caixa **Pesquisar programas e arquivos** .</span><span class="sxs-lookup"><span data-stu-id="8bdb3-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="8bdb3-119">Na lista de resultados da pesquisa, clique com o botão direito do mouse em **cmd.exe** e selecione **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="8bdb3-120">No prompt de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8bdb3-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="8bdb3-121">**Observação**  Para a &lt; unidade fixa &gt; no comando, especifique um dispositivo de armazenamento disponível com espaço livre igual ou maior que os dados na unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="8bdb3-122">Os dados na unidade corrompida são recuperados e movidos para a unidade fixa especificada.</span><span class="sxs-lookup"><span data-stu-id="8bdb3-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="8bdb3-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bdb3-123">Related topics</span></span>


[<span data-ttu-id="8bdb3-124">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="8bdb3-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





