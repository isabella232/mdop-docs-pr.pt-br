---
title: Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0
description: Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799144"
---
# <span data-ttu-id="53838-103">Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="53838-103">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="53838-104">Use as informações desta seção quando planejar salvar e implantar a imagem de recuperação do Microsoft (diagnóstico e recuperação) do Microsoft (Microsoft Diagnostics and Recovery Toolset) 7.</span><span class="sxs-lookup"><span data-stu-id="53838-104">Use the information in this section when you plan for saving and deploying the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="53838-105">Planejar como salvar e implantar a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="53838-105">Planning How to Save and Deploy the DaRT Recovery Image</span></span>


<span data-ttu-id="53838-106">Você pode salvar e implantar a imagem de recuperação do DaRT usando os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="53838-106">You can save and deploy the DaRT recovery image by using the following methods.</span></span> <span data-ttu-id="53838-107">Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um.</span><span class="sxs-lookup"><span data-stu-id="53838-107">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="53838-108">Além disso, considere como você deseja usar o DaRT na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="53838-108">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="53838-109">**Observação**  Talvez você queira usar mais de um método em sua organização.</span><span class="sxs-lookup"><span data-stu-id="53838-109">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="53838-110">Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.</span><span class="sxs-lookup"><span data-stu-id="53838-110">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="53838-111">A tabela a seguir mostra algumas vantagens e desvantagens de cada método de usar o DaRT em sua organização.</span><span class="sxs-lookup"><span data-stu-id="53838-111">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53838-112">Método para inicializar o DaRT</span><span class="sxs-lookup"><span data-stu-id="53838-112">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="53838-113">Vantagens</span><span class="sxs-lookup"><span data-stu-id="53838-113">Advantages</span></span></th>
<th align="left"><span data-ttu-id="53838-114">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="53838-114">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53838-115">A partir de um CD ou DVD</span><span class="sxs-lookup"><span data-stu-id="53838-115">From a CD or DVD</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-116">Oferece suporte a cenários em que o registro de inicialização mestre (MBR) está corrompido e não é possível acessar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="53838-116">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk.</span></span> <span data-ttu-id="53838-117">Também oferece suporte a casos em que não há conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="53838-117">Also supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="53838-118">Isso é mais familiar para os usuários de versões anteriores do DaRT, e um CD ou DVD pode ser gravado diretamente do <strong> Assistente de recuperação de imagem de DART </strong> .</span><span class="sxs-lookup"><span data-stu-id="53838-118">This is most familiar to users of earlier versions of DaRT, and a CD or DVD can be burned directly from the <strong>DaRT Recovery Image Wizard</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-119">Requer que alguém com acesso ao CD ou DVD esteja fisicamente no computador do usuário final para inicializar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="53838-119">Requires that someone with access to the CD or DVD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53838-120">De uma unidade flash USB (UFD)</span><span class="sxs-lookup"><span data-stu-id="53838-120">From a USB flash drive (UFD)</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-121">Fornece as mesmas vantagens que a inicialização a partir de um CD ou DVD e também fornece suporte a computadores que não têm unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="53838-121">Provides same advantages as booting from a CD or DVD and also provides support to computers that have no CD or DVD drive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-122">Requer que você formate o UFD antes de poder usá-lo para inicializar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="53838-122">Requires you to format the UFD before you can use it to boot into DaRT.</span></span> <span data-ttu-id="53838-123">Também requer que alguém com acesso à unidade UFD seja fisicamente no computador do usuário final para inicializar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="53838-123">Also requires that someone with access to the UFD is physically at the end-user computer to boot into DaRT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53838-124">De uma partição remota (rede)</span><span class="sxs-lookup"><span data-stu-id="53838-124">From a remote (network) partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-125">Permite que você inicialize no DaRT sem precisar de um CD, DVD ou UFD.</span><span class="sxs-lookup"><span data-stu-id="53838-125">Lets you boot into DaRT without needing a CD, DVD, or UFD.</span></span> <span data-ttu-id="53838-126">Também permite atualizações fáceis do DaRT porque só há um local de arquivo para atualizar.</span><span class="sxs-lookup"><span data-stu-id="53838-126">Also allows for easy upgrades of DaRT because there is only one file location to update.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-127">Não funcionará se o computador do usuário final não estiver conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="53838-127">Does not work if the end-user computer is not connected to the network.</span></span></p>
<p><span data-ttu-id="53838-128">Amplamente disponível para usuários finais e pode exigir considerações de segurança adicionais ao criar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="53838-128">Widely available to end users and might require additional security considerations when you are creating the recovery image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53838-129">De uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="53838-129">From a recovery partition</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-130">Permite que você inicialize no DaRT sem precisar de um CD, DVD ou UFD que inclua instâncias em que não há conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="53838-130">Lets you boot into DaRT without needing a CD, DVD, or UFD that includes instances in which there is no network connectivity.</span></span></p>
<p><span data-ttu-id="53838-131">Além disso, pode ser implementada e gerenciada como parte do processo de imagem padrão do Windows usando ferramentas de distribuição automatizadas, como o Gerenciador de configuração do Microsoft Endpoint.</span><span class="sxs-lookup"><span data-stu-id="53838-131">Also, can be implemented and managed as part of your standard Windows image process by using automated distribution tools, such as Microsoft Endpoint Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="53838-132">Ao atualizar o DaRT, você precisa atualizar todos os computadores na sua empresa, em vez de apenas uma partição (na rede) ou dispositivo (CD, DVD ou UFD).</span><span class="sxs-lookup"><span data-stu-id="53838-132">When updating DaRT, requires you to update all computers in your enterprise instead of just one partition (on the network) or device (CD, DVD, or UFD).</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="53838-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53838-133">Related topics</span></span>


[<span data-ttu-id="53838-134">Planejamento da implantação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="53838-134">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





