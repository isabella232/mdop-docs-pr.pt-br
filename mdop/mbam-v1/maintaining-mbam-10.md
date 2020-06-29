---
title: Manutenção do MBAM 1.0
description: Manutenção do MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799739"
---
# <span data-ttu-id="2a09c-103">Manutenção do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2a09c-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="2a09c-104">Depois de concluir todos os planejamentos necessários e, em seguida, implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurar o MBAM para ser executado de forma altamente disponível ao usá-lo para gerenciar operações de criptografia do BitLocker da empresa.</span><span class="sxs-lookup"><span data-stu-id="2a09c-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="2a09c-105">As informações nesta seção descrevem opções de alta disponibilidade para o MBAM, além de como mover recursos de servidor do MBAM, se necessário.</span><span class="sxs-lookup"><span data-stu-id="2a09c-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="2a09c-106">Pacote de gerenciamento MBAM</span><span class="sxs-lookup"><span data-stu-id="2a09c-106">MBAM Management Pack</span></span>


<span data-ttu-id="2a09c-107">O pacote de gerenciamento do MicrosoftSystemCenterOperationsManager para MBAM está disponível para download no centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a09c-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="2a09c-108">Esse pacote de gerenciamento monitora as interações críticas na infraestrutura do lado do servidor, como as conexões entre os serviços Web e bancos de dados e as chamadas operacionais entre sites e seu serviço Web de apoio.</span><span class="sxs-lookup"><span data-stu-id="2a09c-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="2a09c-109">Ele também carrega as solicitações entre os clientes da área de trabalho e seus respectivos pontos de extremidade do serviço Web de recebimento.</span><span class="sxs-lookup"><span data-stu-id="2a09c-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="2a09c-110">Pacote de gerenciamento de administração e monitoramento do Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="2a09c-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="2a09c-111">Garantir alta disponibilidade para o MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="2a09c-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="2a09c-112">O MBAM foi projetado para ser tolerante a falhas.</span><span class="sxs-lookup"><span data-stu-id="2a09c-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="2a09c-113">Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente.</span><span class="sxs-lookup"><span data-stu-id="2a09c-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="2a09c-114">As informações nesta seção podem ser usadas para configurar uma instalação do MBAM altamente disponível.</span><span class="sxs-lookup"><span data-stu-id="2a09c-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="2a09c-115">Alta disponibilidade para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2a09c-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="2a09c-116">Mover os recursos do MBAM 1,0 para outro servidor</span><span class="sxs-lookup"><span data-stu-id="2a09c-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="2a09c-117">Quando você precisa mover um recurso de servidor MBAM de um computador servidor para outro, há um pedido específico e as etapas necessárias que devem ser seguidas para evitar perda de produtividade ou dados.</span><span class="sxs-lookup"><span data-stu-id="2a09c-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="2a09c-118">Esta seção descreve as etapas que você deve seguir para mover um ou mais recursos de servidor do MBAM para um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="2a09c-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="2a09c-119">Como Mover os Recursos do MBAM 1.0 para Outro Computador</span><span class="sxs-lookup"><span data-stu-id="2a09c-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="2a09c-120">Outros recursos para manter o MBAM</span><span class="sxs-lookup"><span data-stu-id="2a09c-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="2a09c-121">Operações do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2a09c-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





