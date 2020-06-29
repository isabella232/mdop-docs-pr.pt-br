---
title: Como atribuir as credenciais adequadas para o Windows Vista
description: Como atribuir as credenciais adequadas para o Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797911"
---
# <span data-ttu-id="ba9d1-103">Como atribuir as credenciais adequadas para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba9d1-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="ba9d1-104">Use o procedimento a seguir para configurar o cliente da área de trabalho App-V para credenciais WindowsVista adequadas.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="ba9d1-105">**Observação**  Este procedimento deve ser concluído em cada computador não associado ao domínio.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="ba9d1-106">Dependendo do número de computadores não associados ao domínio em seu ambiente, isso pode ser uma operação muito tediosa.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="ba9d1-107">Você pode usar scripts e a interface de linha de comando para o Gerenciador de credenciais para ajudar os administradores a automatizar esse processo.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="ba9d1-108">Para atribuir as credenciais adequadas para os clientes App-V que executam o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba9d1-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="ba9d1-109">Com privilégios de administrador no cliente da área de trabalho App-V executando o Windows Vista, abra o painel de controle de **contas de usuário** (painel de controle clássico).</span><span class="sxs-lookup"><span data-stu-id="ba9d1-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="ba9d1-110">Selecione **gerenciar suas senhas de rede** em **contas de usuário** no painel de tarefas à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="ba9d1-111">Selecione **Adicionar** na tela **nomes de usuário e senhas armazenados** .</span><span class="sxs-lookup"><span data-stu-id="ba9d1-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="ba9d1-112">Na tela **Propriedades de credenciais armazenadas** , forneça as informações para a infraestrutura do App-V:</span><span class="sxs-lookup"><span data-stu-id="ba9d1-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="ba9d1-113">**Faça logon em:** Nome externo do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="ba9d1-114">**Nome de usuário:** Nome de usuário do usuário externo na forma Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="ba9d1-115">**Senha:** Senha da conta de usuário inserida no campo **nome de usuário** .</span><span class="sxs-lookup"><span data-stu-id="ba9d1-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="ba9d1-116">Deixe o **tipo de credencial** selecionado e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="ba9d1-117">Clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-117">Click **Close**.</span></span> <span data-ttu-id="ba9d1-118">As credenciais são armazenadas no repositório de credenciais para autenticação adequada à infraestrutura do App-V.</span><span class="sxs-lookup"><span data-stu-id="ba9d1-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="ba9d1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba9d1-119">Related topics</span></span>


[<span data-ttu-id="ba9d1-120">Clientes ingressados no domínio e não ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="ba9d1-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="ba9d1-121">Como atribuir as credenciais adequadas para o Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba9d1-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





