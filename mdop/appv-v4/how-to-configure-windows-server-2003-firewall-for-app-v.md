---
title: Como configurar o Firewall do Windows Server 2003 para App-V
description: Como configurar o Firewall do Windows Server 2003 para App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797183"
---
# <span data-ttu-id="906b6-103">Como configurar o Firewall do Windows Server 2003 para App-V</span><span class="sxs-lookup"><span data-stu-id="906b6-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="906b6-104">Use o procedimento a seguir para configurar o Firewall do WindowsServer 2003 para o App-V.</span><span class="sxs-lookup"><span data-stu-id="906b6-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="906b6-105">Para configurar o WindowsServer 2003 firewall para o App-V</span><span class="sxs-lookup"><span data-stu-id="906b6-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="906b6-106">No **painel de controle**, abra o **Firewall do Windows**.</span><span class="sxs-lookup"><span data-stu-id="906b6-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="906b6-107">**Observação**  Se o servidor não tiver sido configurado para executar o serviço de firewall antes desta etapa, você será solicitado a iniciar o serviço de firewall.</span><span class="sxs-lookup"><span data-stu-id="906b6-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="906b6-108">Se os arquivos ICO e OSD forem publicados por SMB, verifique se o **compartilhamento de arquivos e impressoras** está habilitado na guia **exceções** .</span><span class="sxs-lookup"><span data-stu-id="906b6-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="906b6-109">**Observação**  Se os arquivos ICO e OSD forem publicados por HTTP/HTTPS no servidor de gerenciamento, talvez seja necessário adicionar uma exceção para HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="906b6-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="906b6-110">Se o servidor IIS que hospeda os arquivos ICO e OSD estiver hospedado em um computador separado do servidor de gerenciamento, você precisará adicionar a exceção a esse computador.</span><span class="sxs-lookup"><span data-stu-id="906b6-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="906b6-111">Para maximizar o desempenho, é recomendável que você hospede os arquivos ICO e OSD em um servidor separado do servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="906b6-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="906b6-112">Adicione uma exceção do programa para `sghwdsptr.exe` , que é o executável do serviço de servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="906b6-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="906b6-113">O caminho padrão para esse executável é `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="906b6-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="906b6-114">**Observação**  Se o servidor de gerenciamento usar RTSP para comunicação, você também deverá adicionar uma exceção do programa `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="906b6-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="906b6-115">O servidor de streaming App-V requer uma exceção `sglwdsptr.exe` do programa para comunicação entre RTSPS.</span><span class="sxs-lookup"><span data-stu-id="906b6-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="906b6-116">O servidor de streaming App-V que usa RTSP para comunicação também exige uma exceção do programa para `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="906b6-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="906b6-117">Verifique se o escopo correto está configurado para cada exceção.</span><span class="sxs-lookup"><span data-stu-id="906b6-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="906b6-118">Para reduzir o risco, remova qualquer computador e limite estritamente os endereços IP aos quais o servidor irá responder.</span><span class="sxs-lookup"><span data-stu-id="906b6-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="906b6-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="906b6-119">Related topics</span></span>


[<span data-ttu-id="906b6-120">Como configurar o Firewall do Windows Server 2008 para App-V</span><span class="sxs-lookup"><span data-stu-id="906b6-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





