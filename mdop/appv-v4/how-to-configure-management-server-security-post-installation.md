---
title: Como configurar a segurança do servidor de gerenciamento após a instalação
description: Como configurar a segurança do servidor de gerenciamento após a instalação
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797225"
---
# <span data-ttu-id="597a7-103">Como configurar a segurança do servidor de gerenciamento após a instalação</span><span class="sxs-lookup"><span data-stu-id="597a7-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="597a7-104">Use o console de gerenciamento do App-V para adicionar o certificado e configurar o servidor de gerenciamento do App-V para segurança aprimorada.</span><span class="sxs-lookup"><span data-stu-id="597a7-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="597a7-105">Você pode usar o procedimento a seguir para configurar a pós-instalação de segurança.</span><span class="sxs-lookup"><span data-stu-id="597a7-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="597a7-106">Para configurar a instalação de segurança do servidor de gerenciamento após a instalação</span><span class="sxs-lookup"><span data-stu-id="597a7-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="597a7-107">Abra o console de gerenciamento do App-V e conecte-se ao **serviço de gerenciamento** com privilégios de administrador do App-v.</span><span class="sxs-lookup"><span data-stu-id="597a7-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="597a7-108">Expanda o servidor, expanda **grupos de servidores**e selecione o grupo de servidores apropriado com o qual o servidor de gerenciamento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="597a7-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="597a7-109">Clique com o botão direito do mouse no objeto do servidor de gerenciamento e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="597a7-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="597a7-110">Na guia **portas** , clique em **certificado de servidor** e conclua o assistente para selecionar o certificado provisionado corretamente.</span><span class="sxs-lookup"><span data-stu-id="597a7-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="597a7-111">**Observação**  Se nenhum certificado for exibido no assistente, um certificado não foi provisionado ou o certificado atende aos requisitos do App-V.</span><span class="sxs-lookup"><span data-stu-id="597a7-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="597a7-112">Clique em **Avançar** para continuar na página **Bem-vindo ao assistente de certificado** .</span><span class="sxs-lookup"><span data-stu-id="597a7-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="597a7-113">Selecione o certificado correto na tela **certificados disponíveis** .</span><span class="sxs-lookup"><span data-stu-id="597a7-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="597a7-114">Clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="597a7-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="597a7-115">Depois de concluir o assistente, limpe **RTSP** como uma porta de escuta disponível.</span><span class="sxs-lookup"><span data-stu-id="597a7-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="597a7-116">Isso impede que as conexões sejam feitas em um canal de comunicação não seguro.</span><span class="sxs-lookup"><span data-stu-id="597a7-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="597a7-117">Clique em **aplicar**e reinicie o serviço **Microsoft Virtual Application Server** .</span><span class="sxs-lookup"><span data-stu-id="597a7-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="597a7-118">Use o snap-in do MMC do serviço para realizar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="597a7-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="597a7-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="597a7-119">Related topics</span></span>


[<span data-ttu-id="597a7-120">Como configurar a segurança do servidor de streaming após a instalação</span><span class="sxs-lookup"><span data-stu-id="597a7-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="597a7-121">Solução de problemas de permissão de certificado</span><span class="sxs-lookup"><span data-stu-id="597a7-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





