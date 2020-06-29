---
title: Reiniciar e redefinir um espaço de trabalho da MED-V
description: Reiniciar e redefinir um espaço de trabalho da MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799669"
---
# <span data-ttu-id="1dbd1-103">Reiniciar e redefinir um espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="1dbd1-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="1dbd1-104">Durante a solução de problemas, às vezes você pode achar necessário reiniciar ou redefinir o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="1dbd1-105">Reiniciar o espaço de trabalho do MED-V é basicamente igual a reiniciar um computador físico.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="1dbd1-106">Redefinir o espaço de trabalho do MED-V reexecuta primeiro a configuração e exclui todos os dados armazenados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="1dbd1-107">Como todos os dados armazenados são excluídos, você normalmente só deve redefinir o espaço de trabalho do MED-V para resolver os problemas de solução de problemas mais sérios ou restaurar um espaço de trabalho do MED-V em funcionamento anterior para um estado de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="1dbd1-108">Para obter informações sobre como abrir o kit de ferramentas de administração do MED-V, consulte [solução de problemas do MED-v usando o kit de ferramentas de administração](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd1-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="1dbd1-109">Reiniciando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1dbd1-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="1dbd1-110">Na janela do **Kit de ferramentas de administração do MED-v** , clique em reiniciar o **espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="1dbd1-111">Uma janela de diálogo é aberta, na qual você deve confirmar que deseja reiniciar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="1dbd1-112">Clique em **reiniciar**.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-112">Click **Restart**.</span></span>

    <span data-ttu-id="1dbd1-113">Todos os aplicativos publicados que estiverem em execução ou redirecionados sites que estiverem abertos serão fechados quando o espaço de trabalho do MED-V for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="1dbd1-114">Redefinir um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1dbd1-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="1dbd1-115">Na janela do **Kit de ferramentas de administração do MED-v** , clique em **redefinir espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="1dbd1-116">Uma janela de diálogo é aberta, na qual você deve confirmar que deseja redefinir o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="1dbd1-117">**Aviso**  Redefinir o espaço de trabalho do MED-V faz com que a instalação seja novamente executada novamente e, assim, recarregar o disco rígido virtual original.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="1dbd1-118">Todos os dados armazenados no espaço de trabalho do MED-V desde a primeira vez em que a configuração foi executada originalmente serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="1dbd1-119">Clique em **Redefinir**.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-119">Click **Reset**.</span></span>

    <span data-ttu-id="1dbd1-120">Todos os aplicativos publicados que estiverem em execução ou redirecionados sites que estiverem abertos serão fechados quando o espaço de trabalho do MED-V for redefinido.</span><span class="sxs-lookup"><span data-stu-id="1dbd1-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="1dbd1-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dbd1-121">Related topics</span></span>


[<span data-ttu-id="1dbd1-122">Exibição e configuração de logs da MED-V</span><span class="sxs-lookup"><span data-stu-id="1dbd1-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="1dbd1-123">Exibição de configurações do espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="1dbd1-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





