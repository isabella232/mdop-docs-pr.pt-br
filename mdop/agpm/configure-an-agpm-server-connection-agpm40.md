---
title: Configurar uma conexão de servidor do AGPM
description: Configurar uma conexão de servidor do AGPM
author: dansimp
ms.assetid: 409cbbcf-3b0e-459d-9bd2-75cb7b9430b0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7fdc26045b478da14957cdfe6000d58ab72a064
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797454"
---
# <span data-ttu-id="274b7-103">Configurar uma conexão de servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="274b7-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="274b7-104">Para garantir que você esteja conectado ao arquivo central correto, examine a configuração da conexão do servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="274b7-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="274b7-105">Se um administrador do AGPM (controle total) não configurou uma conexão do servidor do AGPM para você, você deve configurá-lo manualmente.</span><span class="sxs-lookup"><span data-stu-id="274b7-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="274b7-106">Para selecionar um servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="274b7-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="274b7-107">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="274b7-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="274b7-108">No painel detalhes, clique na guia **servidor do AGPM** :</span><span class="sxs-lookup"><span data-stu-id="274b7-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="274b7-109">Se as opções na guia **servidor do AGPM** não estiverem disponíveis, elas foram configuradas centralmente por um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="274b7-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="274b7-110">Se as opções na guia **servidor do AGPM** estiverem disponíveis, digite o nome do computador totalmente qualificado para o servidor do AGPM (por exemplo, Server.contoso.com) e a porta na qual o serviço do AGPM escuta (por padrão, a porta 4600).</span><span class="sxs-lookup"><span data-stu-id="274b7-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="274b7-111">Clique em **aplicar**e, em seguida, clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="274b7-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="274b7-112">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="274b7-112">Additional considerations</span></span>

-   <span data-ttu-id="274b7-113">Os servidores de AGPM selecionados determinam quais GPOs são exibidos na guia **conteúdo** e em que local as configurações da guia de **delegação de domínio** são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="274b7-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="274b7-114">Se não for gerenciado centralmente por meio do modelo administrativo, cada administrador da política de grupo deve definir essa configuração para apontar para o servidor do AGPM do domínio.</span><span class="sxs-lookup"><span data-stu-id="274b7-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="274b7-115">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="274b7-115">Additional references</span></span>

-   [<span data-ttu-id="274b7-116">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="274b7-116">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





