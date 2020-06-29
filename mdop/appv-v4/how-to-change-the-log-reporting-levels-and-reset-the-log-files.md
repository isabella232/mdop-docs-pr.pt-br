---
title: Como alterar os níveis de relatório de log e redefinir arquivos de log
description: Como alterar os níveis de relatório de log e redefinir arquivos de log
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797247"
---
# <span data-ttu-id="cbdd6-103">Como alterar os níveis de relatório de log e redefinir arquivos de log</span><span class="sxs-lookup"><span data-stu-id="cbdd6-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="cbdd6-104">Você pode usar o procedimento a seguir para alterar o nível de relatório de log do nó **virtualização de aplicativos** no console de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="cbdd6-105">Quando o arquivo de log atinge o tamanho máximo (o padrão é 256 MB), uma redefinição é forçada quando ocorre a próxima gravação do log.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="cbdd6-106">Uma redefinição faz com que um novo arquivo de log seja criado, e o arquivo antigo é renomeado como um backup.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="cbdd6-107">Para alterar o nível de relatório de log</span><span class="sxs-lookup"><span data-stu-id="cbdd6-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="cbdd6-108">Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cbdd6-109">Na guia **geral** da caixa de diálogo **Propriedades** , na lista suspensa **nível de log** , selecione o nível de log desejado.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="cbdd6-110">**Observação**  Se você escolher **Verbose** como o nível de log, os arquivos de log aumentarão muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="cbdd6-111">Isso pode inibir o desempenho do cliente, portanto a prática recomendada é usar esse nível de log somente para diagnosticar problemas específicos.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="cbdd6-112">Na guia **geral** da caixa de diálogo **Propriedades** , na lista suspensa **nível de log do sistema** , selecione o nível de log desejado.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="cbdd6-113">**Observação**  A configuração de **nível de log do sistema** controla o nível de mensagens enviadas ao log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="cbdd6-114">As mensagens registradas são idênticas às mensagens que são registradas no log de eventos do cliente, mas são armazenadas em um local diferente.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="cbdd6-115">Clique em **OK** ou **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="cbdd6-116">Para redefinir o arquivo de log</span><span class="sxs-lookup"><span data-stu-id="cbdd6-116">To reset the log file</span></span>**

1.  <span data-ttu-id="cbdd6-117">Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="cbdd6-118">Na guia **geral** da caixa de diálogo **Propriedades** , clique em **Redefinir log** para fazer backup do arquivo de log atual e iniciar imediatamente um novo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="cbdd6-119">Os arquivos de log de backup são armazenados na mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="cbdd6-120">Clique em **OK** ou **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="cbdd6-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="cbdd6-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbdd6-121">Related topics</span></span>


[<span data-ttu-id="cbdd6-122">Como configurar o Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="cbdd6-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="cbdd6-123">Permissões de acesso de usuário no Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="cbdd6-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





