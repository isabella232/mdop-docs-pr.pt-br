---
title: Como configurar o cliente para o Modo de Operação Desconectada
description: Como configurar o cliente para o Modo de Operação Desconectada
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797201"
---
# <span data-ttu-id="a8360-103">Como configurar o cliente para o Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="a8360-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="a8360-104">O modo de operação desconectado habilita o cliente de desktop do Application Virtualization (App-V) ou o cliente do Application Virtualization (App-V) para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal) para executar aplicativos armazenados no cache do sistema de arquivos do cliente quando o cliente não consegue se conectar ao servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="a8360-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="a8360-105">**Importante**  Em uma organização de grande porte em que vários servidores de host de sessão de área de trabalho remota (host de Sessão RD °) (anteriormente chamado de Terminal Server) são vinculados a um farm para dar suporte a muitos usuários, usar um servidor de gerenciamento do App-V único para dar suporte ao farm representa um único ponto de falha.</span><span class="sxs-lookup"><span data-stu-id="a8360-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="a8360-106">Para fornecer alta disponibilidade para dar suporte ao farm de hosts do RDSession, considere vincular dois ou mais servidores de gerenciamento do App-V para usar o mesmo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8360-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="a8360-107">Para habilitar o modo de operação desconectado</span><span class="sxs-lookup"><span data-stu-id="a8360-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="a8360-108">Defina o seguinte valor da chave do registro igual a 1 para habilitar o modo de operação desconectada:</span><span class="sxs-lookup"><span data-stu-id="a8360-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="a8360-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="a8360-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="a8360-110">Para definir um limite de tempo no modo de operação desconectado, use</span><span class="sxs-lookup"><span data-stu-id="a8360-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="a8360-111">Defina o seguinte valor da chave do registro como 1:</span><span class="sxs-lookup"><span data-stu-id="a8360-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="a8360-112">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="a8360-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="a8360-113">Defina o seguinte valor da chave do registro como o número de minutos que você deseja limitar o modo de operação desconectado.</span><span class="sxs-lookup"><span data-stu-id="a8360-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="a8360-114">O intervalo válido de valores é 1 – 999999.</span><span class="sxs-lookup"><span data-stu-id="a8360-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="a8360-115">O valor padrão é 90 dias ou 129.600 minutos.</span><span class="sxs-lookup"><span data-stu-id="a8360-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="a8360-116">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="a8360-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="a8360-117">Configurar o modo de operação cliente para serviços de área de trabalho remota para desconexão</span><span class="sxs-lookup"><span data-stu-id="a8360-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="a8360-118">Defina o seguinte valor da chave do registro como 1 para habilitar o modo de operação desconectada:</span><span class="sxs-lookup"><span data-stu-id="a8360-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="a8360-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="a8360-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="a8360-120">Defina o seguinte valor da chave do registro como 0 (zero) para permitir o uso ilimitado do modo de operação desconectado:</span><span class="sxs-lookup"><span data-stu-id="a8360-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="a8360-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="a8360-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="a8360-122">Certifique-se de que todos os pacotes sejam pré-carregados no cache para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a8360-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="a8360-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8360-123">Related topics</span></span>


[<span data-ttu-id="a8360-124">Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="a8360-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="a8360-125">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a8360-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





