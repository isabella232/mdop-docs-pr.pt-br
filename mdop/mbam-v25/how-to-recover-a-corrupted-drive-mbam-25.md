---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799095"
---
# <span data-ttu-id="94ae5-103">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="94ae5-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="94ae5-104">Você pode usar esse procedimento com o site de administração e monitoramento (também conhecido como o Help Desk) para recuperar uma unidade corrompida protegida pelo BitLocker.</span><span class="sxs-lookup"><span data-stu-id="94ae5-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="94ae5-105">Para fazer isso, você irá concluir as tarefas descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="94ae5-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="94ae5-106">Tarefa</span><span class="sxs-lookup"><span data-stu-id="94ae5-106">Task</span></span></th>
<th align="left"><span data-ttu-id="94ae5-107">Detalhes e mais informações</span><span class="sxs-lookup"><span data-stu-id="94ae5-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94ae5-108">Crie um arquivo de pacote de chave de recuperação acessando a <strong> </strong> área de recuperação de unidade do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="94ae5-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="94ae5-109">Para acessar a <strong> área de recuperação da unidade </strong> , você deve ser atribuído à função usuários da assistência técnica do MBAM ou à função usuários avançados da assistência técnica do MBAM.</span><span class="sxs-lookup"><span data-stu-id="94ae5-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="94ae5-110">Você pode ter atribuído a essas funções nomes diferentes quando você as criou.</span><span class="sxs-lookup"><span data-stu-id="94ae5-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="94ae5-111">Para obter mais informações, consulte <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> planejando para contas e grupos do MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="94ae5-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="94ae5-112">Copie o arquivo do pacote para o computador que contém a unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="94ae5-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="94ae5-113">Use o <code>repair-bde</code> comando para concluir o processo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="94ae5-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="94ae5-114">Para evitar uma possível perda de dados, é altamente recomendável que você examine o <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-bde </a> antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="94ae5-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="94ae5-115">Para recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="94ae5-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="94ae5-116">Abra um navegador da Web e navegue até o **site de administração e monitoramento**.</span><span class="sxs-lookup"><span data-stu-id="94ae5-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="94ae5-117">No painel esquerdo, selecione **recuperação de unidade** para abrir a página **recuperar acesso a uma unidade criptografada** .</span><span class="sxs-lookup"><span data-stu-id="94ae5-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="94ae5-118">Insira o domínio de logon do Windows do usuário final e o nome de usuário, o motivo para desbloquear a unidade e a ID da senha de recuperação do usuário final.</span><span class="sxs-lookup"><span data-stu-id="94ae5-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="94ae5-119">**Observação**  Se você for membro do grupo de acesso de usuários avançados da assistência técnica, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="94ae5-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="94ae5-120">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="94ae5-120">Click **Submit**.</span></span> <span data-ttu-id="94ae5-121">A chave de recuperação será exibida.</span><span class="sxs-lookup"><span data-stu-id="94ae5-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="94ae5-122">Clique em **salvar**e selecione **pacote de chave de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="94ae5-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="94ae5-123">O pacote da chave de recuperação será criado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="94ae5-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="94ae5-124">Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="94ae5-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="94ae5-125">Abra um prompt de comando com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="94ae5-125">Open an elevated command prompt.</span></span> <span data-ttu-id="94ae5-126">Para fazer isso, clique em **Iniciar** e digite `cmd` na caixa de texto **Pesquisar programas e arquivos** .</span><span class="sxs-lookup"><span data-stu-id="94ae5-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="94ae5-127">Clique com o botão direito do mouse **cmd.exe**e selecione **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="94ae5-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="94ae5-128">No prompt de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="94ae5-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="94ae5-129">**Observação**  Substitua &lt; *unidade fixa* &gt; por uma unidade de disco rígido disponível com espaço livre igual ou maior que os dados na unidade corrompida.</span><span class="sxs-lookup"><span data-stu-id="94ae5-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="94ae5-130">Os dados na unidade corrompida são recuperados e movidos para a unidade de disco rígido especificada.</span><span class="sxs-lookup"><span data-stu-id="94ae5-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="94ae5-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94ae5-131">Related topics</span></span>


[<span data-ttu-id="94ae5-132">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="94ae5-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="94ae5-133">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="94ae5-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="94ae5-134">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="94ae5-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="94ae5-135">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="94ae5-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





