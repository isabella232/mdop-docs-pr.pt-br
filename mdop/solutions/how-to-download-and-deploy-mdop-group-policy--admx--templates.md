---
title: Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)
description: Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799968"
---
# <span data-ttu-id="de521-103">Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)</span><span class="sxs-lookup"><span data-stu-id="de521-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="de521-104">Você pode gerenciar as configurações de recursos de determinadas tecnologias do Microsoft Desktop Optimization Pack (MDOP) (por exemplo, App-V, UE-V ou MBAM) usando os modelos de política de grupo, os arquivos. admx e. adml.</span><span class="sxs-lookup"><span data-stu-id="de521-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="de521-105">Os modelos de política de grupo do MDOP estão disponíveis para download em um arquivo auto-extraível compactado, agrupado por tecnologia e versão.</span><span class="sxs-lookup"><span data-stu-id="de521-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="de521-106">Modelos de política de grupo do MDOP</span><span class="sxs-lookup"><span data-stu-id="de521-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="de521-107">Como baixar e implantar os modelos de política de grupo do MDOP</span><span class="sxs-lookup"><span data-stu-id="de521-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="de521-108">Baixar os últimos [modelos de política de grupo do MDOP](https://www.microsoft.com/download/details.aspx?id=55531)</span><span class="sxs-lookup"><span data-stu-id="de521-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="de521-109">Expanda o arquivo. cab baixado executando</span><span class="sxs-lookup"><span data-stu-id="de521-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="de521-110">Aviso</span><span class="sxs-lookup"><span data-stu-id="de521-110">Warning</span></span>**  
   <span data-ttu-id="de521-111">Não extraia os modelos diretamente para o diretório de implantação da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="de521-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="de521-112">Várias tecnologias e versões são agrupadas nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="de521-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="de521-113">Na pasta extraída, localize o arquivo Technology-Version. admx.</span><span class="sxs-lookup"><span data-stu-id="de521-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="de521-114">Determinadas tecnologias do MDOP têm vários conjuntos de objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="de521-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="de521-115">Por exemplo, MBAM inclui configurações de gerenciamento MBAM e MBAM de usuário.</span><span class="sxs-lookup"><span data-stu-id="de521-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="de521-116">Localize o arquivo. adml apropriado por cultura de idioma (ou seja, *en-US* para inglês-Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="de521-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="de521-117">Copie os arquivos. admx e. adml para uma pasta de definição de política.</span><span class="sxs-lookup"><span data-stu-id="de521-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="de521-118">Dependendo de onde você armazenar os modelos, você pode definir as configurações de política de grupo do dispositivo local ou de qualquer computador no domínio.</span><span class="sxs-lookup"><span data-stu-id="de521-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="de521-119">**Arquivos locais:** Para definir as configurações de política de grupo do dispositivo local, copie os arquivos de modelo para os seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="de521-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="de521-120">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="de521-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="de521-121">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="de521-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="de521-122">Modelo de política de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="de521-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="de521-123">&lt;&gt;policyDefinitionss fortes</span><span class="sxs-lookup"><span data-stu-id="de521-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="de521-124">Arquivo de idioma da política de grupo (. adml)</span><span class="sxs-lookup"><span data-stu-id="de521-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="de521-125">&lt;&gt;policyDefinitionss fortes</span><span class="sxs-lookup"><span data-stu-id="de521-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="de521-126">**Repositório central do domínio:** Para habilitar a configuração de configurações de política de grupo por um administrador de política de grupo de qualquer computador no domínio, copie os arquivos para os seguintes locais no controlador de domínio:</span><span class="sxs-lookup"><span data-stu-id="de521-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="de521-127">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="de521-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="de521-128">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="de521-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="de521-129">Modelo de política de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="de521-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="de521-130">&lt;&gt;sysvol\domain\policies\PolicyDefinitionss fortes</span><span class="sxs-lookup"><span data-stu-id="de521-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="de521-131">Arquivo de idioma da política de grupo (. adml)</span><span class="sxs-lookup"><span data-stu-id="de521-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="de521-132">&lt;alta segurança &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="de521-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="de521-133">Por exemplo, o arquivo específico da linguagem ADML inglês americano será armazenado no%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span><span class="sxs-lookup"><span data-stu-id="de521-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="de521-134">Edite as configurações de política de grupo usando o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM) para definir configurações de política de grupo para a tecnologia do MDOP.</span><span class="sxs-lookup"><span data-stu-id="de521-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="de521-135">Política de grupo do MDOP por tecnologia</span><span class="sxs-lookup"><span data-stu-id="de521-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="de521-136">Para obter mais informações sobre a política de grupo do MDOP com suporte, consulte a documentação específica da tecnologia.</span><span class="sxs-lookup"><span data-stu-id="de521-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de521-137">Tecnologia do MDOP</span><span class="sxs-lookup"><span data-stu-id="de521-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="de521-138">Pacotes de versão</span><span class="sxs-lookup"><span data-stu-id="de521-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="de521-139">Observações</span><span class="sxs-lookup"><span data-stu-id="de521-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="de521-140">Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="de521-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="de521-141">Service Packs do App-V 5,0 e do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="de521-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="de521-142">Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="de521-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="de521-143">User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="de521-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="de521-144">UE-V 2,0 e UE-V 2,1</span><span class="sxs-lookup"><span data-stu-id="de521-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="de521-145">Configurando o UE-V 2. x com objetos de política de grupo</span><span class="sxs-lookup"><span data-stu-id="de521-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="de521-146">UE-V 1,0 incluindo 1,0 SP1</span><span class="sxs-lookup"><span data-stu-id="de521-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="de521-147">Configurando o UE-V com objetos de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="de521-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="de521-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span><span class="sxs-lookup"><span data-stu-id="de521-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="de521-149">MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="de521-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="de521-150">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="de521-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="de521-151">MBAM 2,0, incluindo 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="de521-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="de521-152">Planejar Requisitos de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="de521-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="de521-153">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="de521-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="de521-154">MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="de521-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="de521-155">Como editar Configurações GPO do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="de521-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





