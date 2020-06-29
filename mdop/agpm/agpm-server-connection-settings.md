---
title: Configurações de conexão do servidor do AGPM
description: Configurações de conexão do servidor do AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796145"
---
# <span data-ttu-id="4fb3f-103">Configurações de conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="4fb3f-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="4fb3f-104">Você pode usar as configurações de modelo administrativo para o gerenciamento avançado de política de grupo (AGPM) para configurar de forma centralizada as conexões do servidor do AGPM para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="4fb3f-105">As configurações a seguir estão disponíveis em User Configuration\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="4fb3f-106">Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4fb3f-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="4fb3f-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="4fb3f-108">Efeito</span><span class="sxs-lookup"><span data-stu-id="4fb3f-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4fb3f-109">Servidor do AGPM (todos os domínios)</span><span class="sxs-lookup"><span data-stu-id="4fb3f-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4fb3f-110">Se habilitada, essa configuração configura centralmente uma conexão do servidor do AGPM para ser usada por todos os domínios e desabilita as configurações na <strong> Guia do servidor </strong> do AGPM para administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="4fb3f-111">Para vários servidores de AGPM, defina essa configuração com um servidor padrão e, em seguida, defina a <strong> configuração do servidor do AGPM </strong> no modelo administrativo para substituir esse servidor para outros domínios.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="4fb3f-112">Se desabilitada ou não configurada, cada administrador de política de grupo deve selecionar o servidor do AGPM a ser exibido para cada domínio na <strong> guia servidor do AGPM </strong> no AGPM.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4fb3f-113">Servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="4fb3f-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4fb3f-114">Se habilitada, essa configuração configura centralmente vários servidores de AGPM específicos do domínio, substituindo a <strong> configuração do servidor do AGPM (todos os domínios) </strong> no modelo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="4fb3f-115">Se o seu ambiente exigir apenas um único servidor do AGPM, use apenas a <strong> configuração servidor do AGPM (todos os domínios) </strong> no modelo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="4fb3f-116">Se desabilitada ou não configurada, a <strong> configuração do servidor do AGPM (todos os domínios) </strong> no modelo administrativo configura a conexão do servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="4fb3f-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4fb3f-117">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="4fb3f-117">Additional references</span></span>

-   [<span data-ttu-id="4fb3f-118">Configurações de Modelo Administrativo</span><span class="sxs-lookup"><span data-stu-id="4fb3f-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="4fb3f-119">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="4fb3f-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





