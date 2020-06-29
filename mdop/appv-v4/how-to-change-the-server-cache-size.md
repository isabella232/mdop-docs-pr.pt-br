---
title: Como alterar o tamanho do cache do servidor
description: Como alterar o tamanho do cache do servidor
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797243"
---
# <span data-ttu-id="b40b3-103">Como alterar o tamanho do cache do servidor</span><span class="sxs-lookup"><span data-stu-id="b40b3-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="b40b3-104">Você pode usar o procedimento a seguir para alterar o tamanho do cache de qualquer servidor diretamente do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b40b3-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="b40b3-105">**Observação**  Embora você possa alterar o tamanho do cache, a menos que sua configuração exija especificamente que você altere o tamanho, é recomendável deixar o tamanho do cache definido para os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="b40b3-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="b40b3-106">Para alterar o tamanho do cache do servidor</span><span class="sxs-lookup"><span data-stu-id="b40b3-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="b40b3-107">Clique no nó **Server groups** no painel esquerdo para expandir a lista de grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="b40b3-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="b40b3-108">No painel de **resultados** , clique duas vezes no grupo de servidores desejado para exibir a lista de servidores do grupo.</span><span class="sxs-lookup"><span data-stu-id="b40b3-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="b40b3-109">No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="b40b3-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="b40b3-110">Selecione a guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="b40b3-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="b40b3-111">Insira um valor no campo de **alocação máxima de memória** para o cache do servidor e insira um valor para o nível de aviso de limite no campo aviso de **alocação de memória** .</span><span class="sxs-lookup"><span data-stu-id="b40b3-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="b40b3-112">Insira um valor no campo **tamanho máximo do bloco** .</span><span class="sxs-lookup"><span data-stu-id="b40b3-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="b40b3-113">Esse número deve ser maior ou igual ao tamanho máximo do bloco do maior pacote que será transmitido do servidor.</span><span class="sxs-lookup"><span data-stu-id="b40b3-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="b40b3-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b40b3-114">Click **OK**.</span></span>

## <span data-ttu-id="b40b3-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b40b3-115">Related topics</span></span>


[<span data-ttu-id="b40b3-116">Como alterar a porta do servidor</span><span class="sxs-lookup"><span data-stu-id="b40b3-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="b40b3-117">Como gerenciar servidores no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b40b3-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





