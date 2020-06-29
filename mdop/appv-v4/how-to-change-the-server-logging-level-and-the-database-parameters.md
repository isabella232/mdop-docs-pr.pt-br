---
title: Como alterar o nível de log do servidor e os parâmetros do banco de dados
description: Como alterar o nível de log do servidor e os parâmetros do banco de dados
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797244"
---
# <span data-ttu-id="e5cee-103">Como alterar o nível de log do servidor e os parâmetros do banco de dados</span><span class="sxs-lookup"><span data-stu-id="e5cee-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="e5cee-104">Você pode usar os procedimentos a seguir para alterar o nível de log e os parâmetros do log de banco de dados do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="e5cee-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="e5cee-105">Os seguintes níveis de log estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="e5cee-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="e5cee-106">Somente transação</span><span class="sxs-lookup"><span data-stu-id="e5cee-106">Transaction Only</span></span>

-   <span data-ttu-id="e5cee-107">Erros fatais</span><span class="sxs-lookup"><span data-stu-id="e5cee-107">Fatal Errors</span></span>

-   <span data-ttu-id="e5cee-108">Erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-108">Errors</span></span>

-   <span data-ttu-id="e5cee-109">Avisos/erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-109">Warnings/Errors</span></span>

-   <span data-ttu-id="e5cee-110">Informações/avisos/erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="e5cee-111">Detalha</span><span class="sxs-lookup"><span data-stu-id="e5cee-111">Verbose</span></span>

<span data-ttu-id="e5cee-112">**Observação**  Devido ao tamanho do arquivo de log produzido quando você usa o modo **Verbose** , a recomendação é que você não execute servidores de produção com esse nível de log definido.</span><span class="sxs-lookup"><span data-stu-id="e5cee-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="e5cee-113">Os parâmetros de log de banco de dados determinam o tipo de driver de banco de dados, credenciais de acesso e local do banco de dados de log.</span><span class="sxs-lookup"><span data-stu-id="e5cee-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="e5cee-114">Para alterar o nível de log para servidores de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e5cee-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="e5cee-115">Clique no nó **Server groups** para exibir os grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="e5cee-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="e5cee-116">Clique com o botão direito do mouse no grupo servidor e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="e5cee-117">Na caixa de diálogo **Propriedades** , selecione a guia **registro em log** .</span><span class="sxs-lookup"><span data-stu-id="e5cee-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="e5cee-118">Na caixa de diálogo **Propriedades do grupo de servidores** , selecione o servidor e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="e5cee-119">Na caixa de diálogo **Adicionar/editar módulo de log** , selecione o nível de registro em log na lista suspensa **tipo de evento** .</span><span class="sxs-lookup"><span data-stu-id="e5cee-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="e5cee-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-120">Click **OK**.</span></span>

7.  <span data-ttu-id="e5cee-121">Na caixa de diálogo **Propriedades do grupo de servidores** , clique em **OK** ou **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="e5cee-122">Para alterar o nível de registro em log para servidores de streaming</span><span class="sxs-lookup"><span data-stu-id="e5cee-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="e5cee-123">Edite o seguinte valor da chave do registro para alterar o nível de log:</span><span class="sxs-lookup"><span data-stu-id="e5cee-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="e5cee-124">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span><span class="sxs-lookup"><span data-stu-id="e5cee-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="e5cee-125">Selecione um dos seguintes valores para definir o nível de registro em log.</span><span class="sxs-lookup"><span data-stu-id="e5cee-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="e5cee-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e5cee-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="e5cee-127">Nível de log</span><span class="sxs-lookup"><span data-stu-id="e5cee-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e5cee-128">0</span><span class="sxs-lookup"><span data-stu-id="e5cee-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-129">Somente transações</span><span class="sxs-lookup"><span data-stu-id="e5cee-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e5cee-130">um</span><span class="sxs-lookup"><span data-stu-id="e5cee-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-131">Erros fatais</span><span class="sxs-lookup"><span data-stu-id="e5cee-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e5cee-132">2</span><span class="sxs-lookup"><span data-stu-id="e5cee-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-133">Erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e5cee-134">3D</span><span class="sxs-lookup"><span data-stu-id="e5cee-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-135">Avisos/erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e5cee-136">4</span><span class="sxs-lookup"><span data-stu-id="e5cee-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-137">Informações/avisos/erros</span><span class="sxs-lookup"><span data-stu-id="e5cee-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e5cee-138">5</span><span class="sxs-lookup"><span data-stu-id="e5cee-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e5cee-139">Detalha</span><span class="sxs-lookup"><span data-stu-id="e5cee-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="e5cee-140">Para alterar os parâmetros do log de banco de dados</span><span class="sxs-lookup"><span data-stu-id="e5cee-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="e5cee-141">Clique no nó **Server groups** para exibir os grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="e5cee-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="e5cee-142">Clique com o botão direito do mouse no grupo servidor e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="e5cee-143">Na caixa de diálogo **Propriedades** , selecione a guia **registro em log** .</span><span class="sxs-lookup"><span data-stu-id="e5cee-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="e5cee-144">Na caixa de diálogo **Propriedades do grupo de servidores** , selecione o servidor e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="e5cee-145">Na caixa de diálogo **Adicionar/editar módulo de log** , selecione um driver de banco de dados na lista suspensa **Driver de banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="e5cee-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="e5cee-146">Digite um **nome de host DNS**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="e5cee-147">Clique na caixa de seleção **determinar porta dinamicamente** ou digite um número de porta no campo **porta** .</span><span class="sxs-lookup"><span data-stu-id="e5cee-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="e5cee-148">Insira um **nome de serviço** no campo correspondente.</span><span class="sxs-lookup"><span data-stu-id="e5cee-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="e5cee-149">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-149">Click **OK**.</span></span>

10. <span data-ttu-id="e5cee-150">Na caixa de diálogo **Propriedades do grupo de servidores** , clique em **OK** ou **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="e5cee-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="e5cee-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5cee-151">Related topics</span></span>


[<span data-ttu-id="e5cee-152">Como personalizar um Application Virtualization System no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="e5cee-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





