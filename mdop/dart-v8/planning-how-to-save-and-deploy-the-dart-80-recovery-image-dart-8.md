---
title: Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0
description: Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797886"
---
# <span data-ttu-id="51f37-103">Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="51f37-103">Planning How to Save and Deploy the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="51f37-104">Você pode salvar e implantar a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 usando os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="51f37-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image by using the following methods.</span></span> <span data-ttu-id="51f37-105">Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um.</span><span class="sxs-lookup"><span data-stu-id="51f37-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="51f37-106">Você também deve considerar sua infraestrutura e sua equipe de suporte.</span><span class="sxs-lookup"><span data-stu-id="51f37-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="51f37-107">Se você tiver uma pequena infra-estrutura, talvez queira implantar o DaRT 8,0 usando mídia removível, pois a imagem de recuperação sempre estará disponível se você instalá-la no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="51f37-107">If you have a small infrastructure, you might want to deploy DaRT 8.0 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="51f37-108">Se a sua organização usa os serviços de domínio Active Directory (AD DS), talvez você queira implantar imagens de recuperação como um serviço de rede usando o Windows DS.</span><span class="sxs-lookup"><span data-stu-id="51f37-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="51f37-109">As imagens de recuperação sempre estão disponíveis para qualquer computador conectado.</span><span class="sxs-lookup"><span data-stu-id="51f37-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="51f37-110">Você pode implantar várias imagens do Windows DS e mantê-las todas em um só lugar.</span><span class="sxs-lookup"><span data-stu-id="51f37-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="51f37-111">**Observação**  Talvez você queira usar mais de um método em sua organização.</span><span class="sxs-lookup"><span data-stu-id="51f37-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="51f37-112">Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.</span><span class="sxs-lookup"><span data-stu-id="51f37-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="51f37-113">A tabela a seguir mostra algumas vantagens e desvantagens de cada método de usar o DaRT em sua organização.</span><span class="sxs-lookup"><span data-stu-id="51f37-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="51f37-114">Método para inicializar o DaRT</span><span class="sxs-lookup"><span data-stu-id="51f37-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="51f37-115">Vantagens</span><span class="sxs-lookup"><span data-stu-id="51f37-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="51f37-116">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="51f37-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="51f37-117">Mídia removível</span><span class="sxs-lookup"><span data-stu-id="51f37-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="51f37-118">A imagem de recuperação é gravada em um CD, DVD ou unidade USB para permitir que a equipe de suporte leve as ferramentas de recuperação para o computador instável.</span><span class="sxs-lookup"><span data-stu-id="51f37-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-119">Dá suporte a cenários em que o registro de inicialização mestre (MBR) está corrompido e não é possível acessar o disco rígido e dá suporte a casos em que não há conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="51f37-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="51f37-120">Permite que você crie várias imagens de recuperação com diferentes ferramentas para fornecer níveis diferentes de suporte.</span><span class="sxs-lookup"><span data-stu-id="51f37-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="51f37-121">Fornece uma ferramenta interna para gravar imagens de recuperação em mídias removíveis.</span><span class="sxs-lookup"><span data-stu-id="51f37-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-122">Requer que a equipe de suporte esteja fisicamente no computador do usuário final para inicializar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="51f37-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="51f37-123">Requer tempo e manutenção para criar várias mídias com configurações diferentes para computadores de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51f37-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="51f37-124">De uma partição remota (rede)</span><span class="sxs-lookup"><span data-stu-id="51f37-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="51f37-125">A imagem de recuperação está hospedada em um servidor de inicialização de rede, como os serviços de implantação do Windows (Windows DS), que permite que os usuários ou a equipe de suporte o transmitam para os computadores sob demanda.</span><span class="sxs-lookup"><span data-stu-id="51f37-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-126">Disponível para todos os computadores que têm acesso ao servidor de inicialização de rede.</span><span class="sxs-lookup"><span data-stu-id="51f37-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="51f37-127">As imagens de recuperação são hospedadas em um servidor central, o que permite atualizações centralizadas.</span><span class="sxs-lookup"><span data-stu-id="51f37-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="51f37-128">A equipe de suporte técnico centralizado pode fornecer reparos usando a conectividade remota.</span><span class="sxs-lookup"><span data-stu-id="51f37-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="51f37-129">Não há requisitos de armazenamento local nos clientes.</span><span class="sxs-lookup"><span data-stu-id="51f37-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="51f37-130">Capacidade de criar várias imagens de recuperação com diferentes ferramentas para níveis de suporte específicos.</span><span class="sxs-lookup"><span data-stu-id="51f37-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-131">A necessidade de proteger a infraestrutura do Windows DS para garantir que os usuários normais possam iniciar somente a imagem de recuperação do DaRT e não o processo completo de imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="51f37-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="51f37-132">Requer que o computador do usuário final esteja conectado à rede em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="51f37-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="51f37-133">Requer que a imagem de recuperação seja trazida pela rede.</span><span class="sxs-lookup"><span data-stu-id="51f37-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="51f37-134">De uma partição de recuperação na unidade de disco rígido local</span><span class="sxs-lookup"><span data-stu-id="51f37-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="51f37-135">A imagem de recuperação é instalada em um disco rígido local manualmente ou por meio de sistemas de distribuição de software eletrônico, como o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="51f37-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-136">A imagem de recuperação está sempre disponível porque está em pré-teste no computador.</span><span class="sxs-lookup"><span data-stu-id="51f37-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="51f37-137">A equipe de suporte técnico centralizado pode oferecer suporte usando a conexão remota.</span><span class="sxs-lookup"><span data-stu-id="51f37-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="51f37-138">A imagem de recuperação é gerenciada de forma centralizada e implantada.</span><span class="sxs-lookup"><span data-stu-id="51f37-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="51f37-139">Outras solicitações de chave de recuperação em computadores protegidos por criptografia de unidade de disco BitLocker do Windows são eliminadas.</span><span class="sxs-lookup"><span data-stu-id="51f37-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f37-140">O armazenamento local é necessário.</span><span class="sxs-lookup"><span data-stu-id="51f37-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="51f37-141">Uma partição não criptografada e dedicada para posicionamento de imagens de recuperação é recomendada para reduzir o risco de uma partição de inicialização com falha.</span><span class="sxs-lookup"><span data-stu-id="51f37-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="51f37-142">Ao atualizar o DaRT, você deve atualizar todos os computadores na sua empresa, em vez de apenas uma partição (na rede) ou dispositivo removível.</span><span class="sxs-lookup"><span data-stu-id="51f37-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="51f37-143">Será necessária uma consideração adicional se você implantar a imagem de recuperação após o BitLocker ter sido habilitado.</span><span class="sxs-lookup"><span data-stu-id="51f37-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="51f37-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51f37-144">Related topics</span></span>


[<span data-ttu-id="51f37-145">Planejamento da implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="51f37-145">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





