---
title: Lista de verificação para atualização do MED-V 1.0 SP1
description: Lista de verificação para atualização do MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800038"
---
# <span data-ttu-id="82eba-103">Lista de verificação para atualização do MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="82eba-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="82eba-104">Para atualizar o Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 para o MED-V 1.0 Service Pack1 (SP1), o cliente deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="82eba-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="82eba-105">Opcionalmente, o servidor pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="82eba-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="82eba-106">Atualização do servidor</span><span class="sxs-lookup"><span data-stu-id="82eba-106">Server Upgrade</span></span>


**<span data-ttu-id="82eba-107">Para atualizar o servidor MED-V 1.0 para o MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="82eba-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="82eba-108">Faça backup dos seguintes arquivos localizados no diretório \* &lt; installdir &gt; /Servers/ConfigurationServer\* :</span><span class="sxs-lookup"><span data-stu-id="82eba-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="82eba-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="82eba-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="82eba-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="82eba-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="82eba-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="82eba-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="82eba-112">Faça backup do arquivo \* &lt; installdir &gt; /servers/ServerSettings.xml\* .</span><span class="sxs-lookup"><span data-stu-id="82eba-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="82eba-113">Desinstale o servidor do MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="82eba-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="82eba-114">Instale o servidor MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="82eba-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="82eba-115">Restaure os arquivos de backup para os diretórios apropriados.</span><span class="sxs-lookup"><span data-stu-id="82eba-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="82eba-116">Reinicie o serviço do servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="82eba-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="82eba-117">**Observação**  Se a configuração do servidor tiver sido alterada do padrão, os arquivos poderão estar armazenados em um local diferente.</span><span class="sxs-lookup"><span data-stu-id="82eba-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="82eba-118">Atualização do cliente</span><span class="sxs-lookup"><span data-stu-id="82eba-118">Client Upgrade</span></span>


<span data-ttu-id="82eba-119">Para atualizar o cliente do MED-V 1.0 para o MED-V 1.0 SP1, instale o arquivo. msp em um cliente MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="82eba-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="82eba-120">O cliente e o MED-V são atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="82eba-120">The client and MED-V are automatically upgraded.</span></span>

 

 





