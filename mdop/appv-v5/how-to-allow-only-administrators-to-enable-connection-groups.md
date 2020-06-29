---
title: Como permitir que apenas administradores habilitem grupos de conexão
description: Como permitir que apenas administradores habilitem grupos de conexão
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796505"
---
# <span data-ttu-id="8cb39-103">Como permitir que apenas administradores habilitem grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="8cb39-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="8cb39-104">Você pode configurar o cliente App-V para que somente administradores (não usuários finais) possam habilitar ou desabilitar grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="8cb39-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="8cb39-105">Em versões anteriores do App-V, você não pode impedir que os usuários finais executem essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="8cb39-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="8cb39-106">**Observação** 
 **Este recurso tem suporte a partir do App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="8cb39-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="8cb39-107">Use um dos seguintes métodos para permitir que apenas administradores habilitem ou desabilitem grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="8cb39-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8cb39-108">Método</span><span class="sxs-lookup"><span data-stu-id="8cb39-108">Method</span></span></th>
<th align="left"><span data-ttu-id="8cb39-109">Etapas</span><span class="sxs-lookup"><span data-stu-id="8cb39-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8cb39-110">Configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="8cb39-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="8cb39-111">Habilite a configuração da política de grupo "exigir publicação como administrador", localizada no seguinte nó de objeto de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="8cb39-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="8cb39-112">Política de configuração do computador &gt; &gt; modelos administrativos do &gt; &gt; App-V &gt; Publishing</span><span class="sxs-lookup"><span data-stu-id="8cb39-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8cb39-113">Cmdlet do PowerShell</span><span class="sxs-lookup"><span data-stu-id="8cb39-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="8cb39-114">Execute o <strong> cmdlet Set-AppvClientConfiguration </strong> com o <strong> parâmetro – RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="8cb39-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="8cb39-115">Valores de parâmetro:</span><span class="sxs-lookup"><span data-stu-id="8cb39-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="8cb39-116">0-falso</span><span class="sxs-lookup"><span data-stu-id="8cb39-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="8cb39-117">1-verdadeiro</span><span class="sxs-lookup"><span data-stu-id="8cb39-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="8cb39-118">Exemplo: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="8cb39-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8cb39-119">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="8cb39-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8cb39-120">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="8cb39-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8cb39-121">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="8cb39-121">Got an App-V issue?</span></span>** <span data-ttu-id="8cb39-122">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="8cb39-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8cb39-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cb39-123">Related topics</span></span>


[<span data-ttu-id="8cb39-124">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="8cb39-124">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





