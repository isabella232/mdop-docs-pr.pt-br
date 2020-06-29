---
title: Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software
description: Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796436"
---
# <span data-ttu-id="4d426-103">Como implantar pacotes do App-V 5.1 usando a Distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="4d426-103">How to deploy App-V 5.1 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="4d426-104">Você pode usar um sistema ESD (Electronic Software Distribution) para implantar aplicativos virtuais do App-V 5,1 em clientes do App-V.</span><span class="sxs-lookup"><span data-stu-id="4d426-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.1 virtual applications to App-V clients.</span></span> <span data-ttu-id="4d426-105">Para obter detalhes, consulte a documentação disponível com o ESD que você está usando.</span><span class="sxs-lookup"><span data-stu-id="4d426-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="4d426-106">Para requisitos e opções de componentes para usar um ESD para implantar pacotes do App-V, consulte [planejando implantar o App-V 5,1 com um sistema de distribuição de software eletrônico](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="4d426-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.1 with an Electronic Software Distribution System](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="4d426-107">Use um dos seguintes métodos para publicar pacotes em computadores cliente do App-V com um ESD:</span><span class="sxs-lookup"><span data-stu-id="4d426-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4d426-108">Método</span><span class="sxs-lookup"><span data-stu-id="4d426-108">Method</span></span></th>
<th align="left"><span data-ttu-id="4d426-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d426-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d426-110">Funcionalidade fornecida por um ESD de terceiros</span><span class="sxs-lookup"><span data-stu-id="4d426-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d426-111">Use a funcionalidade em um ESD de terceiros.</span><span class="sxs-lookup"><span data-stu-id="4d426-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d426-112">Instalador autônomo do Windows</span><span class="sxs-lookup"><span data-stu-id="4d426-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d426-113">Instale o aplicativo no computador do cliente de destino usando o arquivo de instalação do Windows (. msi) associado que é criado quando você sequencia inicialmente um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d426-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="4d426-114">O arquivo do Windows Installer contém as informações do arquivo de pacote App-V 5,1 associadas usadas para configurar um pacote e copia os arquivos de pacote necessários para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4d426-114">The Windows Installer file contains the associated App-V 5.1 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d426-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="4d426-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d426-116">Use cmdlets do PowerShell para implantar aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="4d426-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="4d426-117">Para obter mais informações sobre como usar o PowerShell e o App-V 5,1, consulte <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> administrando o app-v 5,1 usando o PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="4d426-117">For more information about using PowerShell and App-V 5.1, see <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)">Administering App-V 5.1 by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="4d426-118">Para implantar pacotes do App-V 5,1 usando um ESD</span><span class="sxs-lookup"><span data-stu-id="4d426-118">To deploy App-V 5.1 packages by using an ESD</span></span>**

1.  <span data-ttu-id="4d426-119">Instale o sequenciador do App-V 5,1 em um computador no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="4d426-119">Install the App-V 5.1 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="4d426-120">Para obter mais informações sobre como instalar o sequenciador, consulte [como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="4d426-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="4d426-121">Use o sequenciador do App-V 5,1 para criar o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="4d426-121">Use the App-V 5.1 Sequencer to create virtual application.</span></span> <span data-ttu-id="4d426-122">Para obter informações sobre como criar um aplicativo virtual, consulte [criando e gerenciando aplicativos virtualizados do App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="4d426-122">For information about creating a virtual application, see [Creating and Managing App-V 5.1 Virtualized Applications](creating-and-managing-app-v-51-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="4d426-123">Depois de criar o aplicativo virtual, implante o pacote usando a solução ESD.</span><span class="sxs-lookup"><span data-stu-id="4d426-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="4d426-124">Se você estiver usando o System Center Configuration Manager, comece analisando [introdução ao gerenciamento de aplicativos no Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) para obter informações sobre como usar o App-V 5,1 e o System Center2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4d426-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.1 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="4d426-125">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="4d426-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4d426-126">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4d426-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4d426-127">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="4d426-127">Got an App-V issue?</span></span>** <span data-ttu-id="4d426-128">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4d426-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4d426-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d426-129">Related topics</span></span>


[<span data-ttu-id="4d426-130">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4d426-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





