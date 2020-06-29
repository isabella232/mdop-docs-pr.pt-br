---
title: Guia Servidor do AGPM
description: Guia Servidor do AGPM
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797494"
---
# <span data-ttu-id="8ec78-103">Guia Servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="8ec78-103">AGPM Server Tab</span></span>


<span data-ttu-id="8ec78-104">A guia **servidor do AGPM** no painel de **controle alterar** permite que você selecione um servidor do AGPM inserindo um nome de computador e uma porta totalmente qualificados e para excluir versões mais antigas dos objetos de política de grupo (GPOs) do arquivo para conservar o espaço em disco no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8ec78-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="8ec78-105">Especificando o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="8ec78-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="8ec78-106">O servidor do AGPM selecionado determina qual arquivo é exibido para você na guia **conteúdo** e para qual local as configurações de **delegação de domínio** são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="8ec78-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="8ec78-107">A porta padrão do AGPM (gerenciamento avançado de política de grupo) é a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="8ec78-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="8ec78-108">Se a conexão do servidor de AGPM estiver configurada de forma centralizada usando as configurações de modelo administrativo, as opções nesta guia para configurar a conexão não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8ec78-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="8ec78-109">Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="8ec78-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

## <span data-ttu-id="8ec78-110">Excluindo versões antigas do GPO</span><span class="sxs-lookup"><span data-stu-id="8ec78-110">Deleting old GPO versions</span></span>


<span data-ttu-id="8ec78-111">Por padrão, todas as versões de cada GPO controlado são mantidas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="8ec78-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="8ec78-112">No entanto, você pode configurar o serviço do AGPM para limitar o número de versões retidas para cada GPO e excluir automaticamente a versão mais antiga quando esse limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="8ec78-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="8ec78-113">Somente as versões de GPO exibidas na guia **versões exclusivas** da janela do **histórico** contam para o limite.</span><span class="sxs-lookup"><span data-stu-id="8ec78-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="8ec78-114">**Observação**  O número máximo de versões exclusivas a serem armazenadas para cada GPO não inclui a versão atual, portanto, digitar 0 retém somente a versão atual.</span><span class="sxs-lookup"><span data-stu-id="8ec78-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="8ec78-115">O limite não deve ser maior do que as versões do 999.</span><span class="sxs-lookup"><span data-stu-id="8ec78-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="8ec78-116">Quando uma versão do GPO é excluída, um registro dessa versão permanece no histórico do GPO, mas a própria versão do GPO é excluída do arquivamento.</span><span class="sxs-lookup"><span data-stu-id="8ec78-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="8ec78-117">Você pode impedir que uma versão do GPO seja excluída marcando-a no histórico como indispensável.</span><span class="sxs-lookup"><span data-stu-id="8ec78-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="8ec78-118">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="8ec78-118">Additional references</span></span>

-   [<span data-ttu-id="8ec78-119">Interface do usuário: Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="8ec78-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="8ec78-120">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="8ec78-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="8ec78-121">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="8ec78-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





