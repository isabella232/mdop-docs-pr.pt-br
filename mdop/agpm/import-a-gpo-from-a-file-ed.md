---
title: Importar um GPO de um arquivo
description: Importar um GPO de um arquivo
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797782"
---
# <span data-ttu-id="01592-103">Importar um GPO de um arquivo</span><span class="sxs-lookup"><span data-stu-id="01592-103">Import a GPO from a File</span></span>


<span data-ttu-id="01592-104">No gerenciamento avançado de política de grupo (AGPM), se você exportou um objeto de política de grupo (GPO) para um arquivo CAB, poderá importar as configurações de política desse GPO para um GPO existente em um domínio de outra floresta.</span><span class="sxs-lookup"><span data-stu-id="01592-104">In Advanced Group Policy Management (AGPM), if you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="01592-105">Importar configurações de política para um GPO existente substitui todas as configurações de política dentro desse GPO.</span><span class="sxs-lookup"><span data-stu-id="01592-105">Importing policy settings into an existing GPO replaces all policy settings within that GPO.</span></span> <span data-ttu-id="01592-106">Para obter informações sobre como exportar configurações de GPO para um arquivo CAB, consulte [exportar um GPO para um arquivo](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="01592-106">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="01592-107">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="01592-107">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="01592-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="01592-108">Review the details in "Additional considerations" in this topic.</span></span>

## <a href="" id="bkmk-existing"></a>


**<span data-ttu-id="01592-109">Para importar configurações de política para um GPO existente</span><span class="sxs-lookup"><span data-stu-id="01592-109">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="01592-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="01592-110">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="01592-111">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="01592-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="01592-112">Verifique o GPO de destino para o qual você deseja importar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="01592-112">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="01592-113">Clique com o botão direito do mouse no GPO de destino, aponte para **importar de**e clique em **arquivo**.</span><span class="sxs-lookup"><span data-stu-id="01592-113">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="01592-114">Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar suas configurações de política para substituir as do GPO de destino e inserir um comentário para a faixa de auditoria do GPO de destino.</span><span class="sxs-lookup"><span data-stu-id="01592-114">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="01592-115">Por padrão, o GPO de destino é verificado quando o assistente é concluído.</span><span class="sxs-lookup"><span data-stu-id="01592-115">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="01592-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="01592-116">Additional considerations</span></span>

-   <span data-ttu-id="01592-117">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="01592-117">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="01592-118">Especificamente, você deve ter **conteúdo da lista**, **Editar configurações**e **importar** permissões de GPO para o domínio, e o GPO deve ser submetido a check-out por você.</span><span class="sxs-lookup"><span data-stu-id="01592-118">Specifically, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span>

-   <span data-ttu-id="01592-119">Embora um editor não possa importar configurações de política para um novo GPO durante sua criação, um editor pode solicitar a criação de um novo GPO e, em seguida, importar as configurações de política para ele após a criação.</span><span class="sxs-lookup"><span data-stu-id="01592-119">Although an Editor cannot import policy settings into a new GPO during its creation, an Editor can request the creation of a new GPO and then import policy settings into it after it is created.</span></span>

### <span data-ttu-id="01592-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="01592-120">Additional references</span></span>

-   [<span data-ttu-id="01592-121">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="01592-121">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





