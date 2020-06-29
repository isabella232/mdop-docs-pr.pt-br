---
title: Exibição e configuração de logs da MED-V
description: Exibição e configuração de logs da MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799330"
---
# <span data-ttu-id="0d07f-103">Exibição e configuração de logs da MED-V</span><span class="sxs-lookup"><span data-stu-id="0d07f-103">Viewing and Configuring MED-V Logs</span></span>


<span data-ttu-id="0d07f-104">Ao solucionar problemas e problemas do MED-V, talvez você ache útil ou necessário acessar os logs de eventos do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d07f-104">When you are troubleshooting MED-V issues and problems, you may find it helpful or necessary to access the MED-V event logs.</span></span> <span data-ttu-id="0d07f-105">Você pode abrir o Visualizador de eventos para o computador host e para a máquina virtual convidada usando o kit de ferramentas de administração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d07f-105">You can open Event Viewer for the host computer and the guest virtual machine by using the MED-V Administration Toolkit.</span></span> <span data-ttu-id="0d07f-106">Você também pode usar o kit de ferramentas de administração do MED-V para definir o nível de log no qual os logs de eventos do MED-V relatam eventos do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d07f-106">You can also use the MED-V Administration Toolkit to set the logging level at which the MED-V event logs report MED-V events.</span></span>

<span data-ttu-id="0d07f-107">Para obter informações sobre como abrir o kit de ferramentas de administração do MED-V, consulte [solução de problemas do MED-v usando o kit de ferramentas de administração](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="0d07f-107">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

## <span data-ttu-id="0d07f-108">Exibir logs de eventos do MED-V</span><span class="sxs-lookup"><span data-stu-id="0d07f-108">Viewing MED-V Event Logs</span></span>


<span data-ttu-id="0d07f-109">Na janela do **Kit de ferramentas de administração do MED-V** , clique em eventos do **host** para abrir o Visualizador de eventos para o computador host.</span><span class="sxs-lookup"><span data-stu-id="0d07f-109">On the **MED-V Administration Toolkit** window, click **Host Events** to open the event viewer for the host computer.</span></span> <span data-ttu-id="0d07f-110">Ou clique em **eventos de convidado** para abrir o Visualizador de eventos para a máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="0d07f-110">Or, click **Guest Events** to open Event Viewer for the guest virtual machine.</span></span>

<span data-ttu-id="0d07f-111">O Visualizador de eventos abre e exibe os logs de eventos correspondentes que você pode usar para solucionar os problemas que podem ocorrer ao implantar ou gerenciar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d07f-111">Event Viewer opens and displays the corresponding event logs that you can use to troubleshoot the issues that you might encounter when you deploy or manage MED-V.</span></span> <span data-ttu-id="0d07f-112">Por padrão, somente erros e avisos são exibidos.</span><span class="sxs-lookup"><span data-stu-id="0d07f-112">By default, only errors and warnings are displayed.</span></span> <span data-ttu-id="0d07f-113">Para obter mais informações sobre IDs e mensagens específicas do evento, consulte [mensagens de log de eventos do MED-V](med-v-event-log-messages.md).</span><span class="sxs-lookup"><span data-stu-id="0d07f-113">For more information about specific event IDs and messages, see [MED-V Event Log Messages](med-v-event-log-messages.md).</span></span>

<span data-ttu-id="0d07f-114">**Observação**  Os usuários finais só poderão salvar arquivos de log de eventos no convidado se tiverem permissões administrativas.</span><span class="sxs-lookup"><span data-stu-id="0d07f-114">**Note** End users can only save event log files in the guest if they have administrative permissions.</span></span>

 

### <span data-ttu-id="0d07f-115">Para abrir manualmente o Visualizador de eventos no computador host</span><span class="sxs-lookup"><span data-stu-id="0d07f-115">To manually open the Event Viewer in the host computer</span></span>

1.  <span data-ttu-id="0d07f-116">Clique em **Iniciar**, em **painel de controle**e em **Ferramentas administrativas**.</span><span class="sxs-lookup"><span data-stu-id="0d07f-116">Click **Start**, click **Control Panel**, and then click **Administrative Tools**.</span></span>

2.  <span data-ttu-id="0d07f-117">Clique duas vezes em **Visualizador de eventos**e, em seguida, clique em **logs de aplicativos e serviços**.</span><span class="sxs-lookup"><span data-stu-id="0d07f-117">Double-click **Event Viewer**, and then click **Applications and Services Logs**.</span></span>

3.  <span data-ttu-id="0d07f-118">Clique duas vezes em **medv**.</span><span class="sxs-lookup"><span data-stu-id="0d07f-118">Double-click **MEDV**.</span></span>

## <span data-ttu-id="0d07f-119">Configurando logs de eventos do MED-V</span><span class="sxs-lookup"><span data-stu-id="0d07f-119">Configuring MED-V Event Logs</span></span>


<span data-ttu-id="0d07f-120">Você pode especificar o nível do log de eventos do MED-V selecionando o botão de opção correspondente no kit de ferramentas de administração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0d07f-120">You can specify the MED-V event logging level by selecting the corresponding option button on the MED-V Administration Toolkit.</span></span> <span data-ttu-id="0d07f-121">Você pode decidir se o log de eventos inclui apenas erros, erros e avisos ou mensagens informativas e erros.</span><span class="sxs-lookup"><span data-stu-id="0d07f-121">You can decide whether event logging includes errors only, errors and warnings, or errors, warnings and informational messages.</span></span> <span data-ttu-id="0d07f-122">O nível de log de eventos especificado é definido para o computador host e para a máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="0d07f-122">The event logging level specified is set for both the host computer and the guest virtual machine.</span></span>

<span data-ttu-id="0d07f-123">Você também pode especificar o nível de log de eventos editando o valor do registro EventLogLevel.</span><span class="sxs-lookup"><span data-stu-id="0d07f-123">You can also specify the event logging level by editing the EventLogLevel registry value.</span></span> <span data-ttu-id="0d07f-124">Para obter mais informações, consulte [Gerenciando as configurações do espaço de trabalho do MED-V](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0d07f-124">For more information, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="0d07f-125">**Observação**  O nível que você especifica na janela do **Kit de ferramentas de administração do MED-v** se aplica a futuros registros de eventos do MED-v.</span><span class="sxs-lookup"><span data-stu-id="0d07f-125">**Note** The level you specify on the **MED-V Administration Toolkit** window applies to future MED-V event logging.</span></span> <span data-ttu-id="0d07f-126">Se você definir o nível para capturar todos os erros, avisos e mensagens informativas, os logs de eventos serão preenchidos mais rapidamente e os eventos mais antigos serão removidos.</span><span class="sxs-lookup"><span data-stu-id="0d07f-126">If you set the level to capture all errors, warnings, and informational messages, then the event logs fill more quickly and older events are removed.</span></span>

 

## <span data-ttu-id="0d07f-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d07f-127">Related topics</span></span>


[<span data-ttu-id="0d07f-128">Reiniciar e redefinir um espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="0d07f-128">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)

[<span data-ttu-id="0d07f-129">Exibição de configurações do espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="0d07f-129">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





