---
title: Modo de Operação Desconectada
description: Modo de Operação Desconectada
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797962"
---
# <span data-ttu-id="9d673-103">Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="9d673-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="9d673-104">As configurações do modo de operação desconectado — acessíveis ao clicar com o botão direito do mouse no nó **virtualização do aplicativo** , selecionar **Propriedades**e clicar na guia **conectividade** — habilita o cliente ou cliente da área de trabalho do aplicativo para os serviços de área de trabalho remota (anteriormente serviços de terminal) para executar aplicativos armazenados no cache do sistema</span><span class="sxs-lookup"><span data-stu-id="9d673-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="9d673-105">Os motivos da falha na conexão com o servidor incluem falha no servidor, falha na rede ou desconexão da rede.</span><span class="sxs-lookup"><span data-stu-id="9d673-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="9d673-106">Se ocorrer uma falha, o cliente será alternado automaticamente para a operação desconectada.</span><span class="sxs-lookup"><span data-stu-id="9d673-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="9d673-107">Depois que ele for desconectado, se o cliente precisar de dados adicionais do servidor para continuar a executar um aplicativo ou se a operação desconectada expirar, o cliente tentará se reconectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9d673-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="9d673-108">Se essa tentativa de conexão falhar, o aplicativo será encerrado.</span><span class="sxs-lookup"><span data-stu-id="9d673-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="9d673-109">Por padrão, a operação desconectada está habilitada e o tempo limite é definido como 90 dias.</span><span class="sxs-lookup"><span data-stu-id="9d673-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="9d673-110">O valor de tempo limite é especificado como o número de dias durante os quais você deseja limitar o modo de operação desconectada, e você pode inserir um valor de 1 – 999.</span><span class="sxs-lookup"><span data-stu-id="9d673-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="9d673-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d673-111">Related topics</span></span>


[<span data-ttu-id="9d673-112">Como desabilitar ou Modificar as configurações de Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="9d673-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





