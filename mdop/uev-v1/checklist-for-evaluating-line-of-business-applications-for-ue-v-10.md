---
title: Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0
description: Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799876"
---
# <span data-ttu-id="8a1df-103">Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8a1df-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="8a1df-104">Para avaliar quais aplicativos de linha de negócios devem ser incluídos na sua implantação do UE-V, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a1df-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="8a1df-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a1df-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-106">Este aplicativo contém configurações que o usuário pode personalizar?</span><span class="sxs-lookup"><span data-stu-id="8a1df-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-107">É importante para o usuário que essas configurações são de roaming?</span><span class="sxs-lookup"><span data-stu-id="8a1df-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-108">Essas configurações de usuário já são gerenciadas por uma solução de política de gerenciamento ou configurações de aplicativo?</span><span class="sxs-lookup"><span data-stu-id="8a1df-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="8a1df-109">O UE-V aplica as configurações do aplicativo nas configurações de inicialização do aplicativo e do Windows durante os eventos de logon, desbloqueio ou conexão remota.</span><span class="sxs-lookup"><span data-stu-id="8a1df-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="8a1df-110">Se você usa o UE-V com outras soluções de política de configurações, os usuários podem enfrentar inconsistência nas configurações de roaming.</span><span class="sxs-lookup"><span data-stu-id="8a1df-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-111">As configurações do aplicativo são específicas do computador?</span><span class="sxs-lookup"><span data-stu-id="8a1df-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="8a1df-112">Preferências de aplicativo e personalizações associadas a hardware ou configurações de computador específicas não fazem roaming consistente entre as sessões e podem causar uma experiência de aplicativo ruim.</span><span class="sxs-lookup"><span data-stu-id="8a1df-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-113">As configurações da loja de aplicativos são encontradas no diretório arquivos de programas ou no diretório de arquivos localizado no diretório <strong> usuários </strong> \ [nome de usuário] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="8a1df-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="8a1df-114">Os dados de aplicativo armazenados em qualquer um desses locais geralmente não devem ser movidos com o usuário, pois esses dados são específicos do computador ou porque os dados são muito grandes para o roaming.</span><span class="sxs-lookup"><span data-stu-id="8a1df-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-115">O aplicativo armazena todas as configurações em um arquivo que contém outros dados de aplicativo que não devem ser movidos?</span><span class="sxs-lookup"><span data-stu-id="8a1df-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="8a1df-116">O UE-V sincroniza arquivos como uma unidade única.</span><span class="sxs-lookup"><span data-stu-id="8a1df-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="8a1df-117">Se as configurações forem armazenadas em arquivos que incluam dados do aplicativo além das configurações, a sincronização desses dados adicionais poderá causar uma experiência de aplicativo ruim.</span><span class="sxs-lookup"><span data-stu-id="8a1df-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8a1df-118">Qual é o tamanho dos arquivos que contêm as configurações?</span><span class="sxs-lookup"><span data-stu-id="8a1df-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="8a1df-119">O desempenho da sincronização de configurações pode ser afetado por arquivos grandes.</span><span class="sxs-lookup"><span data-stu-id="8a1df-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="8a1df-120">Incluir arquivos grandes pode afetar o desempenho da sincronização das configurações.</span><span class="sxs-lookup"><span data-stu-id="8a1df-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8a1df-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a1df-121">Related topics</span></span>


[<span data-ttu-id="8a1df-122">Planejamento para os métodos de configuração da UE-V</span><span class="sxs-lookup"><span data-stu-id="8a1df-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="8a1df-123">Planejamento para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="8a1df-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





