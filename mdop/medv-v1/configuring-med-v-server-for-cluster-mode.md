---
title: Configurando o servidor do MED-V para o modo de cluster
description: Configurando o servidor do MED-V para o modo de cluster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799928"
---
# <span data-ttu-id="93347-103">Configurando o servidor do MED-V para o modo de cluster</span><span class="sxs-lookup"><span data-stu-id="93347-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="93347-104">Você pode configurar o servidor MED-V no modo de cluster.</span><span class="sxs-lookup"><span data-stu-id="93347-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="93347-105">No modo de cluster, dois servidores são usados e todos os arquivos identificados como mútuos nos dois servidores são colocados em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="93347-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="93347-106">O servidor acessa os arquivos do sistema de arquivos, em vez de armazenar os arquivos localmente.</span><span class="sxs-lookup"><span data-stu-id="93347-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="93347-107">Para configurar o servidor MED-V no modo de cluster</span><span class="sxs-lookup"><span data-stu-id="93347-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="93347-108">Instale e configure o MED-V em um dos servidores.</span><span class="sxs-lookup"><span data-stu-id="93347-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="93347-109">Crie uma rede compartilhada em um local central onde todos os servidores possam acessá-la.</span><span class="sxs-lookup"><span data-stu-id="93347-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="93347-110">Copie o conteúdo da pasta \* &lt; installdir &gt; /Servers/ConfigurationServer\* para a rede compartilhada.</span><span class="sxs-lookup"><span data-stu-id="93347-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="93347-111">Instale o MED-V Server em todos os servidores designados.</span><span class="sxs-lookup"><span data-stu-id="93347-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="93347-112">Na rede compartilhada, atribua acesso total a todas as contas de sistema do MED-V Server.</span><span class="sxs-lookup"><span data-stu-id="93347-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="93347-113">Em cada servidor, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="93347-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="93347-114">No arquivo \* &lt; InstallDir &gt; /Servers/ServerConfiguration.xml\* , defina o valor de \* &lt; StorePath &gt; \* para o caminho de rede compartilhada.</span><span class="sxs-lookup"><span data-stu-id="93347-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="93347-115">Copie o arquivo \* &lt; InstsallDir &gt; /Servers/KeyPair.xml\* do servidor original para todos os servidores MED-V.</span><span class="sxs-lookup"><span data-stu-id="93347-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="93347-116">Reinicie o serviço MED-V.</span><span class="sxs-lookup"><span data-stu-id="93347-116">Restart the MED-V service.</span></span>

<span data-ttu-id="93347-117">**Observação**  Se todos os servidores tiverem as mesmas configurações locais (como portas de escuta, servidor IIS, permissões de gerenciamento, banco de dados de relatório e assim por diante), a \* &lt; &gt; ServerSettings.xml/Servers/\* de um banco de dados do installdir também pode ser compartilhada por todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="93347-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="93347-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93347-118">Related topics</span></span>


[<span data-ttu-id="93347-119">Planejamento e design da infraestrutura do MED-V</span><span class="sxs-lookup"><span data-stu-id="93347-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





