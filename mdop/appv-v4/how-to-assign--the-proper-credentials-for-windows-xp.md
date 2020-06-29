---
title: Como atribuir as credenciais adequadas para o Windows XP
description: Como atribuir as credenciais adequadas para o Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797502"
---
# <span data-ttu-id="8386f-103">Como atribuir as credenciais adequadas para o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8386f-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="8386f-104">Use o procedimento a seguir para configurar o cliente da área de trabalho do App-V para credenciais corretas do WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="8386f-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="8386f-105">**Observação**  Depois de concluir esse procedimento, o cliente que não ingressou no domínio pode executar uma atualização de publicação sem ingressar em um domínio.</span><span class="sxs-lookup"><span data-stu-id="8386f-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="8386f-106">Para atribuir as credenciais adequadas para clientes App-V que executam o WindowsXP</span><span class="sxs-lookup"><span data-stu-id="8386f-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="8386f-107">Com privilégios de administrador no aplicativo App-V executando WindowsXP, abra o painel de controle de **contas de usuário** (painel de controle clássico).</span><span class="sxs-lookup"><span data-stu-id="8386f-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="8386f-108">Clique na **guia Avançado**e selecione **gerenciar senhas**.</span><span class="sxs-lookup"><span data-stu-id="8386f-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="8386f-109">Na tela **nomes de usuário e senhas armazenados** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8386f-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="8386f-110">Na tela **Propriedades de informações de logon** , preencha os seguintes campos com informações da infraestrutura do App-V:</span><span class="sxs-lookup"><span data-stu-id="8386f-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="8386f-111">**Servidor:** Nome externo do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="8386f-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="8386f-112">**Nome de usuário:** Nome de usuário para usuário externo na forma Domain\\username.</span><span class="sxs-lookup"><span data-stu-id="8386f-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="8386f-113">**Senha:** Senha da conta de usuário inserida no campo **nome de usuário** .</span><span class="sxs-lookup"><span data-stu-id="8386f-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="8386f-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8386f-114">Click **OK**.</span></span> <span data-ttu-id="8386f-115">As credenciais serão armazenadas no cliente.</span><span class="sxs-lookup"><span data-stu-id="8386f-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="8386f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8386f-116">Related topics</span></span>


[<span data-ttu-id="8386f-117">Clientes ingressados no domínio e não ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="8386f-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="8386f-118">Como atribuir as credenciais adequadas para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8386f-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





