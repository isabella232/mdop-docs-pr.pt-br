---
title: Como configurar a segurança do servidor de streaming após a instalação
description: Como configurar a segurança do servidor de streaming após a instalação
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797218"
---
# <span data-ttu-id="3b9a1-103">Como configurar a segurança do servidor de streaming após a instalação</span><span class="sxs-lookup"><span data-stu-id="3b9a1-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="3b9a1-104">Configure o servidor de streaming App-V para segurança aprimorada por meio do registro.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="3b9a1-105">Assim como no servidor de gerenciamento do App-V, um certificado deve ser provisionado corretamente com o identificador EKU correto para autenticação do servidor antes de concluir o seguinte procedimento de pós-instalação.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="3b9a1-106">Para configurar a pós-instalação do servidor de transmissão de segurança do Stream</span><span class="sxs-lookup"><span data-stu-id="3b9a1-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="3b9a1-107">Crie um MMC, adicione o snap-in **certificados** e selecione **repositório de certificados do computador local**.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="3b9a1-108">Abra os certificados **pessoais** do computador e abra o certificado provisionado para App-V.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="3b9a1-109">Na guia **detalhes** , role a tela para baixo até a impressão digital e copie o hash no painel detalhes.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="3b9a1-110">Abra o editor do registro e navegue até `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="3b9a1-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="3b9a1-111">Edite o `X509CertHash` valor, Cole o hash de impressão digital no campo valor e remova todos os espaços.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="3b9a1-112">Clique em **OK** para aceitar a edição.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="3b9a1-113">No editor do registro, navegue até `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="3b9a1-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="3b9a1-114">Crie um novo valor **DWORD** chamado "322" e insira o valor decimal como 322 ou o valor hexadecimal como 142.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="3b9a1-115">Reinicie o serviço de streaming.</span><span class="sxs-lookup"><span data-stu-id="3b9a1-115">Restart the streaming service.</span></span>

## <span data-ttu-id="3b9a1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b9a1-116">Related topics</span></span>


[<span data-ttu-id="3b9a1-117">Como configurar a segurança do servidor de gerenciamento após a instalação</span><span class="sxs-lookup"><span data-stu-id="3b9a1-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="3b9a1-118">Solução de problemas de permissão de certificado</span><span class="sxs-lookup"><span data-stu-id="3b9a1-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





