---
title: Copiando os modelos de Política de Grupo do MBAM 2.5
description: Copiando os modelos de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799629"
---
# <span data-ttu-id="5ce2a-103">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5ce2a-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="5ce2a-104">Antes de implantar a instalação do cliente do MBAM, você deve baixar os modelos de política de grupo do MBAM, que contêm configurações de política de grupo que definem as configurações de implementação MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="5ce2a-105">Depois de baixar os modelos, você define as configurações de política de grupo para implementar em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="5ce2a-106">Baixar e implantar os modelos de política de grupo do MDOP</span><span class="sxs-lookup"><span data-stu-id="5ce2a-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="5ce2a-107">Os modelos de política de grupo do MDOP estão disponíveis para download em um arquivo auto-extraível compactado, agrupado por tecnologia e versão.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="5ce2a-108">Como baixar e implantar os modelos de política de grupo do MDOP</span><span class="sxs-lookup"><span data-stu-id="5ce2a-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="5ce2a-109">Baixe os modelos de política de grupo do MDOP nos [modelos administrativos de política de grupo do Microsoft Desktop Optimization Pack Pack](https://www.microsoft.com/download/details.aspx?id=55531).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="5ce2a-110">Execute o arquivo baixado para extrair as pastas de modelo.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="5ce2a-111">Aviso</span><span class="sxs-lookup"><span data-stu-id="5ce2a-111">Warning</span></span>**  
   <span data-ttu-id="5ce2a-112">Não extraia os modelos diretamente para o diretório de implantação da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="5ce2a-113">Várias tecnologias e versões são agrupadas nesse arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="5ce2a-114">Na pasta extraída, localize o arquivo Technology-Version. admx.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="5ce2a-115">Determinadas tecnologias do MDOP têm vários conjuntos de objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="5ce2a-116">Por exemplo, MBAM inclui configurações de gerenciamento MBAM e MBAM de usuário.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="5ce2a-117">Localize o arquivo. adml apropriado por cultura de idioma (ou seja, *en* para inglês-Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="5ce2a-118">Copie os arquivos. admx e. adml para uma pasta de definição de política.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="5ce2a-119">Dependendo de onde você armazenar os modelos, você pode definir as configurações de política de grupo do dispositivo local ou de qualquer computador no domínio.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="5ce2a-120">Arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-120">Local files.</span></span>** <span data-ttu-id="5ce2a-121">Para definir as configurações de política de grupo do dispositivo local, copie os arquivos de modelo para os seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="5ce2a-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5ce2a-122">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="5ce2a-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="5ce2a-123">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="5ce2a-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5ce2a-124">Modelo de política de grupo (. admx)</span><span class="sxs-lookup"><span data-stu-id="5ce2a-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5ce2a-125">&lt;&gt;policyDefinitionss fortes</span><span class="sxs-lookup"><span data-stu-id="5ce2a-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5ce2a-126">Arquivo de idioma da política de grupo (. adml)</span><span class="sxs-lookup"><span data-stu-id="5ce2a-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="5ce2a-127">&lt;&gt;policyDefinitionss fortes</span><span class="sxs-lookup"><span data-stu-id="5ce2a-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="5ce2a-128">Edite as configurações de política de grupo usando o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM) para definir configurações de política de grupo para a tecnologia do MDOP.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="5ce2a-129">Consulte [editando as configurações de política de grupo do MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="5ce2a-130">Para obter descrições das configurações de política de grupo, consulte [planejando requisitos de política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="5ce2a-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ce2a-131">Related topics</span></span>


[<span data-ttu-id="5ce2a-132">Implantando objetos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5ce2a-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="5ce2a-133">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="5ce2a-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5ce2a-134">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5ce2a-135">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5ce2a-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






