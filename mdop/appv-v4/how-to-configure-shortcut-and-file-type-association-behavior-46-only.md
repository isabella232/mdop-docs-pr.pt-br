---
title: Como configurar o comportamento de atalhos e de associações de tipo de arquivo
description: Como configurar o comportamento de atalhos e de associações de tipo de arquivo
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797220"
---
# <span data-ttu-id="6ae15-103">Como configurar o comportamento de atalhos e de associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6ae15-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="6ae15-104">A política de publicação de atalho e de associação de tipo de arquivo (FTA) é definida e controlada pelo arquivo XML de publicação, que é enviado aos clientes por um servidor de publicação durante uma operação de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="6ae15-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="6ae15-105">Quando o cliente recebe essas informações, adiciona quaisquer dados publicados recentemente sobre aplicativos como os ícones e FTAs.</span><span class="sxs-lookup"><span data-stu-id="6ae15-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="6ae15-106">Em seguida, ele remove todos os dados de publicação desatualizados.</span><span class="sxs-lookup"><span data-stu-id="6ae15-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="6ae15-107">Na versão 4,6 do App-V, dois valores da chave do registro foram definidos para permitir que os administradores controlem esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="6ae15-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="6ae15-108">Por padrão, os atalhos criados localmente usando o console cliente agora são mantidos.</span><span class="sxs-lookup"><span data-stu-id="6ae15-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="6ae15-109">Como alterar o comportamento do atalho e do FTA</span><span class="sxs-lookup"><span data-stu-id="6ae15-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="6ae15-110">Dois novos valores do Registro DWORD foram definidos para a chave do registro de configuração do cliente, "FileTypePolicy" e "ShortcutPolicy".</span><span class="sxs-lookup"><span data-stu-id="6ae15-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="6ae15-111">Esses valores do Registro DWORD não estão presentes por padrão, mas podem ser adicionados manualmente.</span><span class="sxs-lookup"><span data-stu-id="6ae15-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="6ae15-112">A chave do registro de configuração está localizada em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="6ae15-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="6ae15-113">Há quatro valores de política definidos na tabela a seguir, que se aplicam a ambos os valores de chave do registro.</span><span class="sxs-lookup"><span data-stu-id="6ae15-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="6ae15-114">A lista a seguir mostra os valores numéricos das configurações do registro e o comportamento aplicado a tipos de arquivo ou atalhos em uma operação de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="6ae15-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ae15-115">Nome</span><span class="sxs-lookup"><span data-stu-id="6ae15-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ae15-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-117">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="6ae15-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ae15-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ae15-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="6ae15-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="6ae15-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-121">Padrão = 0x2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="6ae15-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-122">(0x0) – "ClientOnly"-remover itens existentes da mesma fonte de informações de publicação e manter somente os itens que são adicionados localmente</span><span class="sxs-lookup"><span data-stu-id="6ae15-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="6ae15-123">(0x1) – "ServerOnly"-Remova os itens desatualizados da mesma fonte de informações de publicação e os itens que são adicionados localmente e adicione os novos itens</span><span class="sxs-lookup"><span data-stu-id="6ae15-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="6ae15-124">(0x2) – "ClientAndServer"-Remova todos os itens desatualizados da mesma fonte de informações de publicação, mantenha os itens adicionados localmente e adicione os novos itens (padrão se não estiverem presentes para o App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="6ae15-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="6ae15-125">(0x3) – "NoChange"-não fazer alterações em tipos de arquivo ou atalhos</span><span class="sxs-lookup"><span data-stu-id="6ae15-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ae15-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="6ae15-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="6ae15-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-128">Padrão = 0x2</span><span class="sxs-lookup"><span data-stu-id="6ae15-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ae15-129">(0x0) – "ClientOnly"-remover itens existentes da mesma fonte de informações de publicação e manter somente os itens adicionados localmente</span><span class="sxs-lookup"><span data-stu-id="6ae15-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="6ae15-130">(0x1) – "ServerOnly"-Remova todos os itens desatualizados da mesma fonte de informações de publicação e itens adicionados localmente e adicione os novos itens</span><span class="sxs-lookup"><span data-stu-id="6ae15-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="6ae15-131">(0x2) – "ClientAndServer"-Remova todos os itens desatualizados da mesma fonte de informações de publicação, mantenha os itens adicionados localmente e adicione os novos itens (padrão, se não estiverem presentes)</span><span class="sxs-lookup"><span data-stu-id="6ae15-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="6ae15-132">(0x3) – "NoChange"-não fazer alterações em tipos de arquivo ou atalhos</span><span class="sxs-lookup"><span data-stu-id="6ae15-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6ae15-133">**Observação**  Os valores de texto referem-se aos valores dos atributos XML no arquivo XML de publicação.</span><span class="sxs-lookup"><span data-stu-id="6ae15-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="6ae15-134">Você pode definir esses valores manualmente se tiver implementado uma solução de publicação HTTP personalizada.</span><span class="sxs-lookup"><span data-stu-id="6ae15-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





