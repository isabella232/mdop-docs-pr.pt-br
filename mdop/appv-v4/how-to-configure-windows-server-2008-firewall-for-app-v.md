---
title: Como configurar o Firewall do Windows Server 2008 para App-V
description: Como configurar o Firewall do Windows Server 2008 para App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797181"
---
# <span data-ttu-id="d4477-103">Como configurar o Firewall do Windows Server 2008 para App-V</span><span class="sxs-lookup"><span data-stu-id="d4477-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="d4477-104">Com a introdução do Windows Server2008, os componentes de firewall e IPsec foram mesclados em um serviço, e os recursos desse serviço foram aprimorados.</span><span class="sxs-lookup"><span data-stu-id="d4477-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="d4477-105">O novo serviço de firewall dá suporte à inspeção de entrada e de saída de estado.</span><span class="sxs-lookup"><span data-stu-id="d4477-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="d4477-106">Além disso, você pode configurar regras de firewall específicas e diretivas IPsec por meio de políticas de grupo.</span><span class="sxs-lookup"><span data-stu-id="d4477-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="d4477-107">Para obter informações adicionais sobre o Firewall do Windows no Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="d4477-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="d4477-108">O procedimento a seguir não inclui a adição de uma exceção para a publicação por ICO e OSD por SMB ou HTTP/HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d4477-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="d4477-109">Essas exceções são adicionadas automaticamente com base no perfil de rede e nas funções instaladas no firewall do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d4477-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="d4477-110">**Observação**  Se o servidor de gerenciamento estiver configurado para usar RTSP, repita este procedimento para adicionar o `sghwsvr.exe` programa como uma exceção.</span><span class="sxs-lookup"><span data-stu-id="d4477-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="d4477-111">O servidor de streaming do App-V requer a exceção do programa `sglwdsptr.exe` para comunicação entre RTSPS.</span><span class="sxs-lookup"><span data-stu-id="d4477-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="d4477-112">Um servidor de streaming do App-V que usa RTSP para comunicação também exige uma exceção do programa para `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="d4477-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="d4477-113">Para configurar o Windows Server2008 firewall para App-V</span><span class="sxs-lookup"><span data-stu-id="d4477-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="d4477-114">Abra o console **Firewall do Windows com gerenciamento de segurança avançada** por meio do painel de controle ou digite `wf.msc` na linha executar.</span><span class="sxs-lookup"><span data-stu-id="d4477-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="d4477-115">Crie uma nova regra de entrada e selecione **programa**.</span><span class="sxs-lookup"><span data-stu-id="d4477-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="d4477-116">Selecione o caminho do programa e navegue até `sghwdsptr.exe` , que está localizado por padrão em `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="d4477-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="d4477-117">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d4477-117">Click **Next**.</span></span>

5.  <span data-ttu-id="d4477-118">Na página **ação** , selecione **permitir a conexão**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d4477-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="d4477-119">Selecione os **perfis** apropriados para aplicar à regra de entrada.</span><span class="sxs-lookup"><span data-stu-id="d4477-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="d4477-120">Forneça um nome e uma descrição para a regra e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="d4477-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="d4477-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4477-121">Related topics</span></span>


[<span data-ttu-id="d4477-122">Como configurar o Firewall do Windows Server 2003 para App-V</span><span class="sxs-lookup"><span data-stu-id="d4477-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





