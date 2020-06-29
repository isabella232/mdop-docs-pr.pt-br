---
title: Referência de esquema de modelo de aplicativo para UE-V 2. x
description: Referência de esquema de modelo de aplicativo para UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800066"
---
# <span data-ttu-id="68096-103">Referência de esquema de modelo de aplicativo para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="68096-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="68096-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usam modelos de localização de configurações XML para definir as configurações do aplicativo da área de trabalho e as configurações do Windows que são capturadas e aplicadas pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="68096-105">O UE-V inclui um conjunto de modelos de local de configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="68096-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="68096-106">Você também pode criar modelos de local de configurações personalizadas com o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="68096-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="68096-107">Um usuário avançado pode personalizar o arquivo XML de um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="68096-108">Este tópico detalha a estrutura XML dos modelos de localização de configurações do UE-V 2,1 (SP1) e do 2,0 e fornece orientação para a edição desses arquivos.</span><span class="sxs-lookup"><span data-stu-id="68096-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="68096-109">Referência de esquema de modelo de aplicativo do UE-V 2,1 e do 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="68096-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="68096-110">Esta seção detalha a estrutura XML do modelo de local de configurações do UE-V 2,1 e do 2,1 SP1 e fornece orientação para a edição desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="68096-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="68096-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="68096-111">In This Section</span></span>

-   [<span data-ttu-id="68096-112">Atributo XML de declaração e codificação</span><span class="sxs-lookup"><span data-stu-id="68096-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="68096-113">Namespace e elemento raiz</span><span class="sxs-lookup"><span data-stu-id="68096-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="68096-114">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="68096-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="68096-115">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="68096-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="68096-116">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="68096-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="68096-117">Elemento Version</span><span class="sxs-lookup"><span data-stu-id="68096-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="68096-118">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="68096-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="68096-119">Elemento processos e processo</span><span class="sxs-lookup"><span data-stu-id="68096-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="68096-120">Elemento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="68096-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="68096-121">Elemento comum</span><span class="sxs-lookup"><span data-stu-id="68096-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="68096-122">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="68096-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="68096-123">Apêndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="68096-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="68096-124">Atributo XML de declaração e codificação</span><span class="sxs-lookup"><span data-stu-id="68096-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="68096-125">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-125">Mandatory: True</span></span>**

**<span data-ttu-id="68096-126">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-126">Type: String</span></span>**

<span data-ttu-id="68096-127">A declaração XML deve especificar o atributo XML versão 1,0 ( &lt; ? XML Version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="68096-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="68096-128">Os modelos de local de configurações criados pelo UE-V Generator são salvos na codificação UTF-8, embora a codificação não seja especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="68096-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="68096-129">Recomendamos que você inclua o atributo encoding = "UTF-8" nesse elemento como prática recomendada.</span><span class="sxs-lookup"><span data-stu-id="68096-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="68096-130">Todos os modelos incluídos com o produto também especificam essa marca (veja os documentos na experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\Templates para fins de referência).</span><span class="sxs-lookup"><span data-stu-id="68096-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="68096-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="68096-132">Namespace e elemento raiz</span><span class="sxs-lookup"><span data-stu-id="68096-132">Namespace and Root Element</span></span>

**<span data-ttu-id="68096-133">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-133">Mandatory: True</span></span>**

**<span data-ttu-id="68096-134">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-134">Type: String</span></span>**

<span data-ttu-id="68096-135">O UE-V usa o https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="68096-136">SettingsLocationTemplate é o elemento raiz e contém todos os outros elementos.</span><span class="sxs-lookup"><span data-stu-id="68096-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="68096-137">Referência SettingsLocationTemplate em todos os modelos usando esta marca:</span><span class="sxs-lookup"><span data-stu-id="68096-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="68096-138">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="68096-138">Data types</span></span>

<span data-ttu-id="68096-139">Estes são os tipos de dados do esquema de modelo de aplicativo do UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="68096-140">**GUID** GUID descreve uma expressão regular de identificador global exclusivo padrão no formulário "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="68096-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="68096-141">Isso é usado no elemento Filesetting\\Root\\KnownFolder para verificar a formatação de pastas bem conhecidas.</span><span class="sxs-lookup"><span data-stu-id="68096-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="68096-142">**Filenamestring** Filenamestring refere-se ao nome de arquivo de um processo a ser monitorado.</span><span class="sxs-lookup"><span data-stu-id="68096-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="68096-143">Seus valores são restritos pelo Regex \ [^ \ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, (ou seja, eles podem não conter caracteres de barra invertida, asterisco ou ponto de interrogação caracteres curinga, o caractere de pipe, o sinal de maior ou menor que, barra de encaminhamento ou caracteres de dois pontos).</span><span class="sxs-lookup"><span data-stu-id="68096-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="68096-144">**IDString** IDString refere-se ao valor ID dos elementos do aplicativo, SettingsLocationTemplate e dos elementos comuns (usados para descrever os pacotes de aplicativos que compartilham configurações comuns).</span><span class="sxs-lookup"><span data-stu-id="68096-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="68096-145">Ele é restrito pelo mesmo Regex como filenamestring (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="68096-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="68096-146">**TemplateVersion** TemplateVersion é um valor inteiro usado para descrever a revisão do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="68096-147">Seu valor pode variar de 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="68096-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="68096-148">Em **branco** Vazio refere-se a um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="68096-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="68096-149">Isso é usado no Process\\ShellProcess para indicar que não há processo para monitorar.</span><span class="sxs-lookup"><span data-stu-id="68096-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="68096-150">Esse valor não deve ser usado em nenhum modelo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="68096-151">**Criar** O tipo de dados autor é um tipo complexo que identifica o autor de um modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="68096-152">Ele contém dois elementos filho: **Name** e **email**.</span><span class="sxs-lookup"><span data-stu-id="68096-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="68096-153">Dentro do tipo de dados autor, o elemento Name é obrigatório enquanto o elemento de email é opcional.</span><span class="sxs-lookup"><span data-stu-id="68096-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="68096-154">Esse tipo é descrito em mais detalhes sob o elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="68096-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="68096-155">**Intervalo** de Range define uma classe Integer que consiste em dois elementos filho: **mínimo** e **máximo**.</span><span class="sxs-lookup"><span data-stu-id="68096-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="68096-156">Esse tipo de dados é implementado no tipo de dados ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="68096-157">Se especificado, os valores mínimo e máximo devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="68096-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="68096-158">**ProcessVersion** ProcessVersion define um tipo com quatro elementos filho: **Major**, **Minor**, **Build**e **patch**.</span><span class="sxs-lookup"><span data-stu-id="68096-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="68096-159">Esse tipo de dados é usado pelo elemento processo para preencher seus valores ProductVersion e FileVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="68096-160">Os dados desse tipo são um valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="68096-160">The data for this type is a Range value.</span></span> <span data-ttu-id="68096-161">O principal elemento filho é obrigatório e os outros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="68096-162">**Arquitetura** do A arquitetura enumera dois valores possíveis: **Win32** e **Win64**.</span><span class="sxs-lookup"><span data-stu-id="68096-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="68096-163">Esses valores são usados para especificar a arquitetura do processo.</span><span class="sxs-lookup"><span data-stu-id="68096-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="68096-164">**Processo** O tipo de dados processo é um contêiner usado para descrever os processos a serem monitorados pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="68096-165">Ele contém seis elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="68096-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="68096-166">Esta tabela detalha os respectivos tipos de dados de cada elemento:</span><span class="sxs-lookup"><span data-stu-id="68096-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68096-167">Elemento</span><span class="sxs-lookup"><span data-stu-id="68096-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-168">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="68096-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-169">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68096-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-170">Arq</span><span class="sxs-lookup"><span data-stu-id="68096-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-171">Filenamestring</span><span class="sxs-lookup"><span data-stu-id="68096-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-172">True</span><span class="sxs-lookup"><span data-stu-id="68096-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-173">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-174">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-175">False</span><span class="sxs-lookup"><span data-stu-id="68096-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="68096-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-177">String</span><span class="sxs-lookup"><span data-stu-id="68096-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-178">False</span><span class="sxs-lookup"><span data-stu-id="68096-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="68096-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-180">String</span><span class="sxs-lookup"><span data-stu-id="68096-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-181">False</span><span class="sxs-lookup"><span data-stu-id="68096-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="68096-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="68096-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-184">False</span><span class="sxs-lookup"><span data-stu-id="68096-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="68096-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="68096-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-187">False</span><span class="sxs-lookup"><span data-stu-id="68096-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="68096-188">**Processar** O tipo de dados Processes representa um contêiner para uma coleção de um ou mais elementos de processo.</span><span class="sxs-lookup"><span data-stu-id="68096-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="68096-189">Dois elementos filho são compatíveis com o tipo de sequência Processes: **process** e **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="68096-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="68096-190">Processo é um elemento do tipo processo e ShellProcess é do tipo de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="68096-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="68096-191">Pelo menos um item deve ser identificado na sequência.</span><span class="sxs-lookup"><span data-stu-id="68096-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="68096-192">**Caminho** Path é consumido pela configuração RegistrySetting e filepara se referir a caminhos de arquivo e registro.</span><span class="sxs-lookup"><span data-stu-id="68096-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="68096-193">Esse elemento dá suporte a dois atributos opcionais: **recursive** e **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="68096-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="68096-194">Ambos os valores são definidos como default = "false".</span><span class="sxs-lookup"><span data-stu-id="68096-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="68096-195">Recursiva indica que o caminho e todas as subpastas estão incluídos para configurações de arquivo ou que todas as chaves do registro filho estão incluídas para as configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="68096-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="68096-196">Em ambos os casos, todos os itens no nível atual são incluídos nos dados capturados.</span><span class="sxs-lookup"><span data-stu-id="68096-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="68096-197">Para um objeto filesettings, todos os arquivos na pasta especificada são incluídos nos dados capturados pela UE-V, mas as pastas não estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="68096-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="68096-198">Para caminhos de registro, todos os valores no caminho atual são capturados, mas as chaves do registro filho não são capturadas.</span><span class="sxs-lookup"><span data-stu-id="68096-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="68096-199">Em ambos os casos, deve-se tomar cuidado para evitar a captura de grandes conjuntos de dados ou grandes números de itens.</span><span class="sxs-lookup"><span data-stu-id="68096-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="68096-200">O atributo DeleteIfNotFound remove a configuração dos dados do caminho de armazenamento das configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="68096-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="68096-201">Isso pode ser desejável em casos em que a remoção dessas configurações do pacote irá salvar uma grande quantidade de espaço em disco no servidor de arquivos do caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="68096-202">**Máscara** de Filemask especifica apenas determinados tipos de arquivo para a pasta que é definida por path.</span><span class="sxs-lookup"><span data-stu-id="68096-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="68096-203">Por exemplo, o caminho pode ser `C:\users\username\files` e filemask poderia ser `*.txt` apenas incluir arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="68096-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="68096-204">**RegistrySetting** RegistrySetting representa um contêiner para chaves do registro e valores e o comportamento desejado associado na parte do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="68096-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="68096-205">Quatro elementos filho são definidos neste tipo: **Path**, **Name**, **Exclude**e uma sequência do **caminho** e **nome**do valor.</span><span class="sxs-lookup"><span data-stu-id="68096-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="68096-206">**Configuração** do Filesetting contém parâmetros associados a arquivos e caminhos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68096-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="68096-207">Quatro elementos filho são definidos: **root**, **Path**, **filemask**e **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="68096-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="68096-208">A raiz é obrigatória e as outras são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="68096-209">**Configurações** de Configurações é um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-210">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68096-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="68096-211">Além disso, ele também pode conter os seguintes elementos filho com comportamentos descritos:</span><span class="sxs-lookup"><span data-stu-id="68096-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68096-212">Elemento</span><span class="sxs-lookup"><span data-stu-id="68096-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-213">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-214">Assíncrono</span><span class="sxs-lookup"><span data-stu-id="68096-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-215">Os pacotes de configurações assíncronas são aplicados sem bloquear a inicialização do aplicativo para que o início do aplicativo continue enquanto as configurações ainda estiverem sendo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="68096-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="68096-216">Isso é útil para configurações que podem ser aplicadas de forma assíncrona, como aquelas <code>get/set</code> por meio de uma API, como SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="68096-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="68096-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-218">Por padrão, o UE-V salva apenas as configurações de um aplicativo quando a última instância de um aplicativo que usa o modelo é fechada.</span><span class="sxs-lookup"><span data-stu-id="68096-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="68096-219">Quando esse elemento é definido como ' false ', o UE-V exporta as configurações mesmo se outras instâncias de um aplicativo estiverem em execução.</span><span class="sxs-lookup"><span data-stu-id="68096-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="68096-220">Modelos adequados – aqueles que incluem uma seção de elementos comuns – que são fornecidos com o UE-V usam esse sinalizador para habilitar as configurações compartilhadas para sempre exportar no aplicativo e, ao mesmo tempo, impedir que as configurações específicas do aplicativo sejam exportadas até que a última instância seja fechada.</span><span class="sxs-lookup"><span data-stu-id="68096-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="68096-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-222">(apresentado em 2,1)</span><span class="sxs-lookup"><span data-stu-id="68096-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="68096-223">Esse parâmetro obriga um pacote de configurações importada a ser aplicado mesmo se não houver nenhuma diferença entre o pacote e o estado atual do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="68096-224">Esse parâmetro deve ser usado apenas em casos especiais, pois ele pode retardar a importação das configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="68096-225">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="68096-225">Name Element</span></span>

**<span data-ttu-id="68096-226">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-226">Mandatory: True</span></span>**

**<span data-ttu-id="68096-227">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-227">Type: String</span></span>**

<span data-ttu-id="68096-228">Nome especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-229">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-230">Em geral, evite fazer referência a informações de versão, pois isso pode ser objeto do elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="68096-231">Por exemplo, especifique `<Name>My Application</Name>` em vez de `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="68096-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="68096-232">**Observação**  O UE-V não faz referência a DTDs externos, portanto, não é possível usar entidades nomeadas em um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="68096-233">Por exemplo, não use &reg; para se referir ao símbolo de marca comercial registrado®.</span><span class="sxs-lookup"><span data-stu-id="68096-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="68096-234">Em vez disso, use referências numeradas canônicas para incluir esses tipos de caracteres especiais, por exemplo, & \ #174 para o caractere®.</span><span class="sxs-lookup"><span data-stu-id="68096-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="68096-235">Esta regra se aplica a todos os valores de cadeias de caracteres neste documento.</span><span class="sxs-lookup"><span data-stu-id="68096-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="68096-236">Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obter uma lista completa de entidades de caractere.</span><span class="sxs-lookup"><span data-stu-id="68096-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="68096-237">Os documentos codificados em UTF-8 podem incluir os caracteres Unicode diretamente.</span><span class="sxs-lookup"><span data-stu-id="68096-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="68096-238">Salvar modelos pelo UE-V Generator converte as entidades de caracteres em representações Unicode automaticamente.</span><span class="sxs-lookup"><span data-stu-id="68096-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="68096-239">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="68096-239">ID Element</span></span>

**<span data-ttu-id="68096-240">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-240">Mandatory: True</span></span>**

**<span data-ttu-id="68096-241">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-241">Type: String</span></span>**

<span data-ttu-id="68096-242">ID preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-243">Essa marca se tornará o identificador primário que o agente do UE-V usa para fazer referência ao modelo no tempo de execução (por exemplo, veja a saída dos cmdlets Get-UevTemplate e Get-UevTemplateProgram do PowerShell).</span><span class="sxs-lookup"><span data-stu-id="68096-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="68096-244">Por convenção, essa marca não deve conter espaços, o que simplifica o script.</span><span class="sxs-lookup"><span data-stu-id="68096-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="68096-245">Os números de versão de aplicativos devem ser especificados nesse elemento para permitir a fácil identificação do modelo, como `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="68096-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="68096-246">Elemento Version</span><span class="sxs-lookup"><span data-stu-id="68096-246">Version Element</span></span>

**<span data-ttu-id="68096-247">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-247">Mandatory: True</span></span>**

**<span data-ttu-id="68096-248">Tipo: inteiro</span><span class="sxs-lookup"><span data-stu-id="68096-248">Type: Integer</span></span>**

**<span data-ttu-id="68096-249">Valor mínimo: 0</span><span class="sxs-lookup"><span data-stu-id="68096-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="68096-250">Valor máximo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="68096-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="68096-251">A versão identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-252">O UE-V Generator automaticamente incrementa esse número a cada vez que o modelo é salvo.</span><span class="sxs-lookup"><span data-stu-id="68096-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="68096-253">Observe que esse campo deve ser um inteiro de número inteiro; valores fracionários, como `<Version>2.5</Version>` não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="68096-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="68096-254">**Dica:** Você pode salvar anotações sobre alterações de versão usando marcas de comentário XML `<!-- -->` , por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="68096-255">**Importante**  Esse valor é consultado para determinar se uma nova versão de um modelo deve ser aplicada a um modelo existente nestes casos:</span><span class="sxs-lookup"><span data-stu-id="68096-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="68096-256">Quando a tarefa de atualização automática do modelo agendado é executada</span><span class="sxs-lookup"><span data-stu-id="68096-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="68096-257">Quando o cmdlet Update-UevTemplate do PowerShell é executado</span><span class="sxs-lookup"><span data-stu-id="68096-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="68096-258">Quando o método de atualização microsoft\\uev: SettingsLocationTemplate é chamado por meio do WMI</span><span class="sxs-lookup"><span data-stu-id="68096-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="68096-259">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="68096-259">Author Element</span></span>

**<span data-ttu-id="68096-260">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-260">Mandatory: False</span></span>**

**<span data-ttu-id="68096-261">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-261">Type: String</span></span>**

<span data-ttu-id="68096-262">O autor identifica o criador do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="68096-263">Há suporte para dois elementos filho opcionais: **nome** e **email**.</span><span class="sxs-lookup"><span data-stu-id="68096-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="68096-264">Os dois atributos são opcionais, mas, se o elemento filho do email for especificado, ele deve ser acompanhado pelo elemento Name.</span><span class="sxs-lookup"><span data-stu-id="68096-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="68096-265">O autor se refere ao nome completo do contato do modelo de local de configurações e o email deve se referir a um endereço de email para o autor.</span><span class="sxs-lookup"><span data-stu-id="68096-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="68096-266">Recomendamos que você inclua essas informações nos modelos publicados publicamente, por exemplo, na [Galeria de modelos do UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="68096-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="68096-267">Elemento processos e processo</span><span class="sxs-lookup"><span data-stu-id="68096-267">Processes and Process Element</span></span>

**<span data-ttu-id="68096-268">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-268">Mandatory: True</span></span>**

**<span data-ttu-id="68096-269">Tipo: Element</span><span class="sxs-lookup"><span data-stu-id="68096-269">Type: Element</span></span>**

<span data-ttu-id="68096-270">Os processos contêm pelo menos `<Process>` um elemento, que, por sua vez, contém os seguintes elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="68096-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="68096-271">O elemento filho filename é obrigatório e os outros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="68096-272">Um elemento totalmente preenchido contém marcas semelhantes a este exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="68096-273">Arq</span><span class="sxs-lookup"><span data-stu-id="68096-273">Filename</span></span>

**<span data-ttu-id="68096-274">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-274">Mandatory: True</span></span>**

**<span data-ttu-id="68096-275">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-275">Type: String</span></span>**

<span data-ttu-id="68096-276">O nome do arquivo refere-se ao nome de arquivo real do executável exibido no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68096-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="68096-277">Esse elemento Especifica o critério principal que o UE-V usa para avaliar se um modelo se aplica a um processo ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="68096-278">Esse elemento deve ser especificado no modelo de local de configurações XML.</span><span class="sxs-lookup"><span data-stu-id="68096-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="68096-279">Nomes de fileválidas não devem coincidir com a expressão regular \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, ou seja, eles podem não conter caracteres de barra invertida, asterisco ou interrogação de caracteres curinga, o caractere de tubo, o sinal de maior ou menor que, barra ou dois pontos (o \ \?</span><span class="sxs-lookup"><span data-stu-id="68096-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="68096-280">\* | &lt; &gt; /ou: caracteres.).</span><span class="sxs-lookup"><span data-stu-id="68096-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="68096-281">**Dica:** Para testar uma cadeia de caracteres nesse Regex, use uma janela de comando do PowerShell e substitua o nome do seu executável para **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="68096-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="68096-282">Um valor **true** indica que a cadeia de caracteres contém caracteres ilegais.</span><span class="sxs-lookup"><span data-stu-id="68096-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="68096-283">Veja alguns exemplos de valores ilegais:</span><span class="sxs-lookup"><span data-stu-id="68096-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="68096-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="68096-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="68096-285">Programa \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="68096-285">Program\*.exe</span></span>

-   <span data-ttu-id="68096-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="68096-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="68096-287">Programa &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="68096-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="68096-288">**Observação**  O gerador do UE-V codifica o maior que e menor que os caracteres como &gt; e &lt; respectivamente.</span><span class="sxs-lookup"><span data-stu-id="68096-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="68096-289">Em circunstâncias raras, o valor FileName não inclui necessariamente a extensão. exe, mas ele deve ser especificado como parte do valor.</span><span class="sxs-lookup"><span data-stu-id="68096-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="68096-290">Por exemplo, `<Filename>MyApplictication.exe</Filename>` deve ser especificado em vez de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="68096-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="68096-291">O segundo exemplo não aplicará o modelo ao processo, se o nome real do arquivo executável for "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="68096-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="68096-292">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-292">Architecture</span></span>

**<span data-ttu-id="68096-293">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-293">Mandatory: False</span></span>**

**<span data-ttu-id="68096-294">Tipo: Architecture (cadeia)</span><span class="sxs-lookup"><span data-stu-id="68096-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="68096-295">Arquitetura refere-se à arquitetura do processador para a qual o executável de destino foi compilado.</span><span class="sxs-lookup"><span data-stu-id="68096-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="68096-296">Os valores válidos são Win32 para aplicativos de 32 bits ou Win64 para aplicativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="68096-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="68096-297">Se presente, essa marca limita a aplicabilidade do modelo de local de configurações a uma arquitetura de aplicativo específica.</span><span class="sxs-lookup"><span data-stu-id="68096-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="68096-298">Para obter um exemplo disso, compare a experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e arquivos de MicrosoftOffice2010Win64.xml incluídos na UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="68096-299">Isso é útil quando caminhos relativos mudam entre versões diferentes de um executável ou se as configurações foram adicionadas ou removidas ao passar de uma arquitetura de processador para outra.</span><span class="sxs-lookup"><span data-stu-id="68096-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="68096-300">Se esse elemento estiver ausente, o modelo de local de configurações ignorará a arquitetura do processo e se aplicará aos processos do 32 e do 64-bit se o nome do arquivo e outros atributos se aplicarem.</span><span class="sxs-lookup"><span data-stu-id="68096-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="68096-301">**Observação**  A UE-V não oferece suporte a processadores ARM nesta versão.</span><span class="sxs-lookup"><span data-stu-id="68096-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="68096-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="68096-302">ProductName</span></span>

**<span data-ttu-id="68096-303">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-303">Mandatory: False</span></span>**

**<span data-ttu-id="68096-304">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-304">Type: String</span></span>**

<span data-ttu-id="68096-305">O NomeDoProduto é um elemento opcional usado para identificar um produto para fins administrativos ou relatórios.</span><span class="sxs-lookup"><span data-stu-id="68096-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="68096-306">O NomeDoProduto é diferente do nome do arquivo, pois não há restrições de expressão regular em seu valor.</span><span class="sxs-lookup"><span data-stu-id="68096-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="68096-307">Isso permite descrições mais facilmente compreendidas de um processo em que o nome do executável pode não ser óbvio.</span><span class="sxs-lookup"><span data-stu-id="68096-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="68096-308">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="68096-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="68096-309">FileDescription</span></span>

**<span data-ttu-id="68096-310">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-310">Mandatory: False</span></span>**

**<span data-ttu-id="68096-311">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-311">Type: String</span></span>**

<span data-ttu-id="68096-312">FileDescription é uma marca opcional que permite uma descrição administrativa do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="68096-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="68096-313">Esse é um campo de texto gratuito e pode ser útil para distinguir vários executáveis dentro de um pacote de software onde há necessidade de identificar a função do executável.</span><span class="sxs-lookup"><span data-stu-id="68096-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="68096-314">Por exemplo, em um aplicativo adequado, pode ser útil fornecer lembretes sobre a função de dois executáveis (MyApplication.exe e MyApplicationHelper.exe), como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="68096-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="68096-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="68096-315">ProductVersion</span></span>

**<span data-ttu-id="68096-316">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-316">Mandatory: False</span></span>**

**<span data-ttu-id="68096-317">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-317">Type: String</span></span>**

<span data-ttu-id="68096-318">ProductVersion refere-se às versões de produto principais e secundárias de um arquivo, bem como um nível de compilação e patch.</span><span class="sxs-lookup"><span data-stu-id="68096-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="68096-319">ProductVersion é um elemento opcional, mas, se especificado, ele deve conter pelo menos o elemento filho Major.</span><span class="sxs-lookup"><span data-stu-id="68096-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="68096-320">O valor deve expressar um intervalo no formato Minimum = "X" Maximum = "Y", em que X e Y são inteiros.</span><span class="sxs-lookup"><span data-stu-id="68096-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="68096-321">Os valores mínimo e máximo podem ser idênticos.</span><span class="sxs-lookup"><span data-stu-id="68096-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="68096-322">Os elementos da versão do produto e do arquivo podem não ser especificados.</span><span class="sxs-lookup"><span data-stu-id="68096-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="68096-323">Fazer isso torna o modelo "versão independente", o que significa que o modelo será aplicado a todas as versões do executável especificado.</span><span class="sxs-lookup"><span data-stu-id="68096-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="68096-324">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="68096-324">Example 1:</span></span>**

<span data-ttu-id="68096-325">Versão do produto: 1,0 especificado no UE-V Generator produz o seguinte XML:</span><span class="sxs-lookup"><span data-stu-id="68096-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="68096-326">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="68096-326">Example 2:</span></span>**

<span data-ttu-id="68096-327">Versão do arquivo: 5.0.2.1000 especificado no UE-V Generator produz o seguinte XML:</span><span class="sxs-lookup"><span data-stu-id="68096-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="68096-328">Exemplo 1 incorreto – intervalo incompleto:</span><span class="sxs-lookup"><span data-stu-id="68096-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="68096-329">Somente o atributo mínimo está presente.</span><span class="sxs-lookup"><span data-stu-id="68096-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="68096-330">O máximo também deve ser incluído em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="68096-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="68096-331">Exemplo 2 incorreto – especificado secundário sem elemento principal:</span><span class="sxs-lookup"><span data-stu-id="68096-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="68096-332">Somente o elemento secundário está presente.</span><span class="sxs-lookup"><span data-stu-id="68096-332">Only the Minor element is present.</span></span> <span data-ttu-id="68096-333">Importante também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="68096-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="68096-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="68096-334">FileVersion</span></span>

**<span data-ttu-id="68096-335">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-335">Mandatory: False</span></span>**

**<span data-ttu-id="68096-336">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-336">Type: String</span></span>**

<span data-ttu-id="68096-337">FileVersion diferencia a versão de lançamento de um aplicativo publicado e os detalhes de compilação interna de um executável de componente.</span><span class="sxs-lookup"><span data-stu-id="68096-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="68096-338">Para a maioria dos aplicativos comerciais, esses números são idênticos.</span><span class="sxs-lookup"><span data-stu-id="68096-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="68096-339">Onde elas variam, a versão do produto de um arquivo indica uma identificação genérica de versão de um arquivo, enquanto a versão do arquivo indica uma compilação específica de um arquivo (como no caso de um hotfix ou atualização).</span><span class="sxs-lookup"><span data-stu-id="68096-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="68096-340">Isso identifica arquivos com exclusividade sem interromper a lógica de detecção.</span><span class="sxs-lookup"><span data-stu-id="68096-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="68096-341">Para determinar a versão do produto e o arquivo de um determinado executável, clique com o botão direito do mouse no arquivo no Windows Explorer, selecione Propriedades e, em seguida, clique na guia detalhes.</span><span class="sxs-lookup"><span data-stu-id="68096-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="68096-342">Incluir um elemento FileVersion para um aplicativo permite uma lógica de detecção de ajuste de precisão mais granular, mas não é necessário para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="68096-343">As configurações do elemento ProductVersion são verificadas primeiro e, em seguida, FileVersion está marcada.</span><span class="sxs-lookup"><span data-stu-id="68096-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="68096-344">A configuração mais restritiva será aplicada.</span><span class="sxs-lookup"><span data-stu-id="68096-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="68096-345">Os elementos filho e as regras de sintaxe para FileVersion são idênticos aos do ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="68096-346">Elemento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="68096-346">Application Element</span></span>

<span data-ttu-id="68096-347">Aplicativo é um contêiner para configurações que se aplicam a um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="68096-348">Ele é uma coleção dos seguintes campos/tipos.</span><span class="sxs-lookup"><span data-stu-id="68096-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68096-349">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-350">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-351">Name</span><span class="sxs-lookup"><span data-stu-id="68096-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-352">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-353">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-354">Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-355">ID</span><span class="sxs-lookup"><span data-stu-id="68096-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-356">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-357">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-358">Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-359">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-360">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-361">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-362">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-364">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-365">Versão</span><span class="sxs-lookup"><span data-stu-id="68096-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-366">Identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-367">Para obter mais informações, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versão </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="68096-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-369">Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="68096-370">Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="68096-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-372">Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365.</span><span class="sxs-lookup"><span data-stu-id="68096-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="68096-373">Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-374">FixedProfile (apresentado em 2,1)</span><span class="sxs-lookup"><span data-stu-id="68096-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-375">Especifica que este modelo só pode ser associado ao perfil especificado dentro desse elemento e não pode ser alterado via WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68096-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-376">Processos</span><span class="sxs-lookup"><span data-stu-id="68096-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-377">Um contêiner para uma coleção de um ou mais elementos de processo.</span><span class="sxs-lookup"><span data-stu-id="68096-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="68096-378">Para obter mais informações, consulte <a href="#processes21" data-raw-source="[Processes](#processes21)"> processos </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-379">Configurações</span><span class="sxs-lookup"><span data-stu-id="68096-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-380">Um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-381">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="68096-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="68096-382">Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="68096-383">Elemento comum</span><span class="sxs-lookup"><span data-stu-id="68096-383">Common Element</span></span>

<span data-ttu-id="68096-384">Comum é semelhante a um elemento de aplicativo, mas ele sempre é associado a dois ou mais elementos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="68096-385">A seção comum representa o conjunto de configurações compartilhadas entre essas instâncias de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="68096-386">Ele é uma coleção dos seguintes campos/tipos.</span><span class="sxs-lookup"><span data-stu-id="68096-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68096-387">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-388">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-389">Name</span><span class="sxs-lookup"><span data-stu-id="68096-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-390">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-391">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-392">Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-393">ID</span><span class="sxs-lookup"><span data-stu-id="68096-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-394">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-395">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-396">Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-397">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-398">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-399">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-400">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-402">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-403">Versão</span><span class="sxs-lookup"><span data-stu-id="68096-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-404">Identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-405">Para obter mais informações, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versão </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="68096-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-407">Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="68096-408">Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="68096-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-410">Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365.</span><span class="sxs-lookup"><span data-stu-id="68096-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="68096-411">Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-412">FixedProfile (apresentado em 2,1)</span><span class="sxs-lookup"><span data-stu-id="68096-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-413">Especifica que este modelo só pode ser associado ao perfil especificado dentro desse elemento e não pode ser alterado via WMI ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68096-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-414">Configurações</span><span class="sxs-lookup"><span data-stu-id="68096-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-415">Um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-416">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="68096-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="68096-417">Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="68096-418">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="68096-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="68096-419">Esse elemento define as configurações para um único aplicativo ou um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="68096-420">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="68096-421">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-422">Name</span><span class="sxs-lookup"><span data-stu-id="68096-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-423">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-424">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-425">Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-426">ID</span><span class="sxs-lookup"><span data-stu-id="68096-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-427">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-428">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-429">Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-430">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-431">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-432">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-433">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-435">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="68096-436">Apêndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="68096-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="68096-437">Aqui está o arquivo SettingsLocationTemplate. xsd que mostra seus elementos, elementos filho, atributos e parâmetros:</span><span class="sxs-lookup"><span data-stu-id="68096-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="68096-438">Referência de esquema de modelo de aplicativo do UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="68096-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="68096-439">Esta seção detalha a estrutura XML do modelo de local de configurações do UE-V 2,0 e fornece orientação para a edição desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="68096-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="68096-440">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="68096-440">In This Section</span></span>

-   [<span data-ttu-id="68096-441">Atributo XML de declaração e codificação</span><span class="sxs-lookup"><span data-stu-id="68096-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="68096-442">Namespace e elemento raiz</span><span class="sxs-lookup"><span data-stu-id="68096-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="68096-443">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="68096-443">Data types</span></span>](#data)

-   [<span data-ttu-id="68096-444">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="68096-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="68096-445">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="68096-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="68096-446">Elemento Version</span><span class="sxs-lookup"><span data-stu-id="68096-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="68096-447">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="68096-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="68096-448">Elemento processos e processo</span><span class="sxs-lookup"><span data-stu-id="68096-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="68096-449">Elemento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="68096-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="68096-450">Elemento comum</span><span class="sxs-lookup"><span data-stu-id="68096-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="68096-451">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="68096-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="68096-452">Apêndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="68096-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="68096-453">Atributo XML de declaração e codificação</span><span class="sxs-lookup"><span data-stu-id="68096-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="68096-454">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-454">Mandatory: True</span></span>**

**<span data-ttu-id="68096-455">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-455">Type: String</span></span>**

<span data-ttu-id="68096-456">A declaração XML deve especificar o atributo XML versão 1,0 ( &lt; ? XML Version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="68096-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="68096-457">Os modelos de local de configurações criados pelo UE-V Generator são salvos na codificação UTF-8, embora a codificação não seja especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="68096-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="68096-458">Recomendamos que você inclua o atributo encoding = "UTF-8" nesse elemento como prática recomendada.</span><span class="sxs-lookup"><span data-stu-id="68096-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="68096-459">Todos os modelos incluídos com o produto também especificam essa marca (veja os documentos na experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\Templates para fins de referência).</span><span class="sxs-lookup"><span data-stu-id="68096-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="68096-460">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="68096-461">Namespace e elemento raiz</span><span class="sxs-lookup"><span data-stu-id="68096-461">Namespace and Root Element</span></span>

**<span data-ttu-id="68096-462">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-462">Mandatory: True</span></span>**

**<span data-ttu-id="68096-463">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-463">Type: String</span></span>**

<span data-ttu-id="68096-464">O UE-V usa o https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="68096-465">SettingsLocationTemplate é o elemento raiz e contém todos os outros elementos.</span><span class="sxs-lookup"><span data-stu-id="68096-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="68096-466">Referência SettingsLocationTemplate em todos os modelos usando esta marca:</span><span class="sxs-lookup"><span data-stu-id="68096-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="68096-467">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="68096-467">Data types</span></span>

<span data-ttu-id="68096-468">Estes são os tipos de dados do esquema de modelo de aplicativo do UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="68096-469">**GUID** GUID descreve uma expressão regular de identificador global exclusivo padrão no formulário "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}".</span><span class="sxs-lookup"><span data-stu-id="68096-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="68096-470">Isso é usado no elemento Filesetting\\Root\\KnownFolder para verificar a formatação de pastas bem conhecidas.</span><span class="sxs-lookup"><span data-stu-id="68096-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="68096-471">**Filenamestring** Filenamestring refere-se ao nome de arquivo de um processo a ser monitorado.</span><span class="sxs-lookup"><span data-stu-id="68096-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="68096-472">Seus valores são restritos pelo Regex \ [^ \ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, (ou seja, eles podem não conter caracteres de barra invertida, asterisco ou ponto de interrogação caracteres curinga, o caractere de pipe, o sinal de maior ou menor que, barra de encaminhamento ou caracteres de dois pontos).</span><span class="sxs-lookup"><span data-stu-id="68096-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="68096-473">**IDString** IDString refere-se ao valor ID dos elementos do aplicativo, SettingsLocationTemplate e dos elementos comuns (usados para descrever os pacotes de aplicativos que compartilham configurações comuns).</span><span class="sxs-lookup"><span data-stu-id="68096-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="68096-474">Ele é restrito pelo mesmo Regex como filenamestring (\ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /:\]+).</span><span class="sxs-lookup"><span data-stu-id="68096-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="68096-475">**TemplateVersion** TemplateVersion é um valor inteiro usado para descrever a revisão do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="68096-476">Seu valor pode variar de 0 a 2147483647.</span><span class="sxs-lookup"><span data-stu-id="68096-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="68096-477">Em **branco** Vazio refere-se a um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="68096-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="68096-478">Isso é usado no Process\\ShellProcess para indicar que não há processo para monitorar.</span><span class="sxs-lookup"><span data-stu-id="68096-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="68096-479">Esse valor não deve ser usado em nenhum modelo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="68096-480">**Criar** O tipo de dados autor é um tipo complexo que identifica o autor de um modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="68096-481">Ele contém dois elementos filho: **Name** e **email**.</span><span class="sxs-lookup"><span data-stu-id="68096-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="68096-482">Dentro do tipo de dados autor, o elemento Name é obrigatório enquanto o elemento de email é opcional.</span><span class="sxs-lookup"><span data-stu-id="68096-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="68096-483">Esse tipo é descrito em mais detalhes sob o elemento SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="68096-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="68096-484">**Intervalo** de Range define uma classe Integer que consiste em dois elementos filho: **mínimo** e **máximo**.</span><span class="sxs-lookup"><span data-stu-id="68096-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="68096-485">Esse tipo de dados é implementado no tipo de dados ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="68096-486">Se especificado, os valores mínimo e máximo devem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="68096-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="68096-487">**ProcessVersion** ProcessVersion define um tipo com quatro elementos filho: **Major**, **Minor**, **Build**e **patch**.</span><span class="sxs-lookup"><span data-stu-id="68096-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="68096-488">Esse tipo de dados é usado pelo elemento processo para preencher seus valores ProductVersion e FileVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="68096-489">Os dados desse tipo são um valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="68096-489">The data for this type is a Range value.</span></span> <span data-ttu-id="68096-490">O principal elemento filho é obrigatório e os outros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="68096-491">**Arquitetura** do A arquitetura enumera dois valores possíveis: **Win32** e **Win64**.</span><span class="sxs-lookup"><span data-stu-id="68096-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="68096-492">Esses valores são usados para especificar a arquitetura do processo.</span><span class="sxs-lookup"><span data-stu-id="68096-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="68096-493">**Processo** O tipo de dados processo é um contêiner usado para descrever os processos a serem monitorados pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="68096-494">Ele contém seis elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="68096-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="68096-495">Esta tabela detalha os respectivos tipos de dados de cada elemento:</span><span class="sxs-lookup"><span data-stu-id="68096-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68096-496">Elemento</span><span class="sxs-lookup"><span data-stu-id="68096-496">Element</span></span></th>
<th align="left"><span data-ttu-id="68096-497">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="68096-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="68096-498">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68096-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-499">Arq</span><span class="sxs-lookup"><span data-stu-id="68096-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-500">Filenamestring</span><span class="sxs-lookup"><span data-stu-id="68096-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-501">True</span><span class="sxs-lookup"><span data-stu-id="68096-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-502">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-503">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-504">False</span><span class="sxs-lookup"><span data-stu-id="68096-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="68096-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-506">String</span><span class="sxs-lookup"><span data-stu-id="68096-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-507">False</span><span class="sxs-lookup"><span data-stu-id="68096-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="68096-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-509">String</span><span class="sxs-lookup"><span data-stu-id="68096-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-510">False</span><span class="sxs-lookup"><span data-stu-id="68096-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="68096-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="68096-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-513">False</span><span class="sxs-lookup"><span data-stu-id="68096-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="68096-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="68096-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-516">False</span><span class="sxs-lookup"><span data-stu-id="68096-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="68096-517">**Processar** O tipo de dados Processes representa um contêiner para uma coleção de um ou mais elementos de processo.</span><span class="sxs-lookup"><span data-stu-id="68096-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="68096-518">Dois elementos filho são compatíveis com o tipo de sequência Processes: **process** e **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="68096-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="68096-519">Processo é um elemento do tipo processo e ShellProcess é do tipo de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="68096-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="68096-520">Pelo menos um item deve ser identificado na sequência.</span><span class="sxs-lookup"><span data-stu-id="68096-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="68096-521">**Caminho** Path é consumido pela configuração RegistrySetting e filepara se referir a caminhos de arquivo e registro.</span><span class="sxs-lookup"><span data-stu-id="68096-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="68096-522">Esse elemento dá suporte a dois atributos opcionais: **recursive** e **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="68096-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="68096-523">Ambos os valores são definidos como default = "false".</span><span class="sxs-lookup"><span data-stu-id="68096-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="68096-524">Recursiva indica que o caminho e todas as subpastas estão incluídos para configurações de arquivo ou que todas as chaves do registro filho estão incluídas para as configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="68096-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="68096-525">Em ambos os casos, todos os itens no nível atual são incluídos nos dados capturados.</span><span class="sxs-lookup"><span data-stu-id="68096-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="68096-526">Para um objeto filesettings, todos os arquivos na pasta especificada são incluídos nos dados capturados pela UE-V, mas as pastas não estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="68096-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="68096-527">Para caminhos de registro, todos os valores no caminho atual são capturados, mas as chaves do registro filho não são capturadas.</span><span class="sxs-lookup"><span data-stu-id="68096-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="68096-528">Em ambos os casos, deve-se tomar cuidado para evitar a captura de grandes conjuntos de dados ou grandes números de itens.</span><span class="sxs-lookup"><span data-stu-id="68096-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="68096-529">O atributo DeleteIfNotFound remove a configuração dos dados do caminho de armazenamento das configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="68096-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="68096-530">Isso pode ser desejável em casos em que a remoção dessas configurações do pacote irá salvar uma grande quantidade de espaço em disco no servidor de arquivos do caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="68096-531">**Máscara** de Filemask especifica apenas determinados tipos de arquivo para a pasta que é definida por path.</span><span class="sxs-lookup"><span data-stu-id="68096-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="68096-532">Por exemplo, o caminho pode ser `C:\users\username\files` e filemask poderia ser `*.txt` apenas incluir arquivos de texto.</span><span class="sxs-lookup"><span data-stu-id="68096-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="68096-533">**RegistrySetting** RegistrySetting representa um contêiner para chaves do registro e valores e o comportamento desejado associado na parte do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="68096-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="68096-534">Quatro elementos filho são definidos neste tipo: **Path**, **Name**, **Exclude**e uma sequência do **caminho** e **nome**do valor.</span><span class="sxs-lookup"><span data-stu-id="68096-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="68096-535">**Configuração** do Filesetting contém parâmetros associados a arquivos e caminhos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68096-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="68096-536">Quatro elementos filho são definidos: **root**, **Path**, **filemask**e **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="68096-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="68096-537">A raiz é obrigatória e as outras são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="68096-538">**Configurações** de Configurações é um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-539">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="68096-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="68096-540">Além disso, ele também pode conter os seguintes elementos filho com comportamentos descritos:</span><span class="sxs-lookup"><span data-stu-id="68096-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68096-541">Elemento</span><span class="sxs-lookup"><span data-stu-id="68096-541">Element</span></span></th>
<th align="left"><span data-ttu-id="68096-542">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-543">Assíncrono</span><span class="sxs-lookup"><span data-stu-id="68096-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-544">Os pacotes de configurações assíncronas são aplicados sem bloquear a inicialização do aplicativo para que o início do aplicativo continue enquanto as configurações ainda estiverem sendo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="68096-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="68096-545">Isso é útil para configurações que podem ser aplicadas de forma assíncrona, como aquelas <code>get/set</code> por meio de uma API, como SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="68096-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="68096-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-547">Por padrão, o UE-V salva apenas as configurações de um aplicativo quando a última instância de um aplicativo que usa o modelo é fechada.</span><span class="sxs-lookup"><span data-stu-id="68096-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="68096-548">Quando esse elemento é definido como ' false ', o UE-V exporta as configurações mesmo se outras instâncias de um aplicativo estiverem em execução.</span><span class="sxs-lookup"><span data-stu-id="68096-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="68096-549">Modelos adequados – aqueles que incluem uma seção de elementos comuns – que são fornecidos com o UE-V usam esse sinalizador para habilitar as configurações compartilhadas para sempre exportar no aplicativo e, ao mesmo tempo, impedir que as configurações específicas do aplicativo sejam exportadas até que a última instância seja fechada.</span><span class="sxs-lookup"><span data-stu-id="68096-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="68096-550">Elemento Name</span><span class="sxs-lookup"><span data-stu-id="68096-550">Name Element</span></span>

**<span data-ttu-id="68096-551">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-551">Mandatory: True</span></span>**

**<span data-ttu-id="68096-552">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-552">Type: String</span></span>**

<span data-ttu-id="68096-553">Nome especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-554">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-555">Em geral, evite fazer referência a informações de versão, pois isso pode ser objeto do elemento ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="68096-556">Por exemplo, especifique `<Name>My Application</Name>` em vez de `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="68096-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="68096-557">**Observação**  O UE-V não faz referência a DTDs externos, portanto, não é possível usar entidades nomeadas em um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="68096-558">Por exemplo, não use &reg; para se referir ao símbolo de marca comercial registrado®.</span><span class="sxs-lookup"><span data-stu-id="68096-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="68096-559">Em vez disso, use referências numeradas canônicas para incluir esses tipos de caracteres especiais, por exemplo, & \ #174 para o caractere®.</span><span class="sxs-lookup"><span data-stu-id="68096-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="68096-560">Esta regra se aplica a todos os valores de cadeias de caracteres neste documento.</span><span class="sxs-lookup"><span data-stu-id="68096-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="68096-561">Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obter uma lista completa de entidades de caractere.</span><span class="sxs-lookup"><span data-stu-id="68096-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="68096-562">Os documentos codificados em UTF-8 podem incluir os caracteres Unicode diretamente.</span><span class="sxs-lookup"><span data-stu-id="68096-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="68096-563">Salvar modelos pelo UE-V Generator converte as entidades de caracteres em representações Unicode automaticamente.</span><span class="sxs-lookup"><span data-stu-id="68096-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="68096-564">Elemento ID</span><span class="sxs-lookup"><span data-stu-id="68096-564">ID Element</span></span>

**<span data-ttu-id="68096-565">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-565">Mandatory: True</span></span>**

**<span data-ttu-id="68096-566">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-566">Type: String</span></span>**

<span data-ttu-id="68096-567">ID preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-568">Essa marca se tornará o identificador primário que o agente do UE-V usa para fazer referência ao modelo no tempo de execução (por exemplo, veja a saída dos cmdlets Get-UevTemplate e Get-UevTemplateProgram do PowerShell).</span><span class="sxs-lookup"><span data-stu-id="68096-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="68096-569">Por convenção, essa marca não deve conter espaços, o que simplifica o script.</span><span class="sxs-lookup"><span data-stu-id="68096-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="68096-570">Os números de versão de aplicativos devem ser especificados nesse elemento para permitir a fácil identificação do modelo, como `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="68096-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="68096-571">Elemento Version</span><span class="sxs-lookup"><span data-stu-id="68096-571">Version Element</span></span>

**<span data-ttu-id="68096-572">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-572">Mandatory: True</span></span>**

**<span data-ttu-id="68096-573">Tipo: inteiro</span><span class="sxs-lookup"><span data-stu-id="68096-573">Type: Integer</span></span>**

**<span data-ttu-id="68096-574">Valor mínimo: 0</span><span class="sxs-lookup"><span data-stu-id="68096-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="68096-575">Valor máximo: 2147483647</span><span class="sxs-lookup"><span data-stu-id="68096-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="68096-576">A versão identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-577">O UE-V Generator automaticamente incrementa esse número a cada vez que o modelo é salvo.</span><span class="sxs-lookup"><span data-stu-id="68096-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="68096-578">Observe que esse campo deve ser um inteiro de número inteiro; valores fracionários, como `<Version>2.5</Version>` não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="68096-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="68096-579">**Dica:** Você pode salvar anotações sobre alterações de versão usando marcas de comentário XML `<!-- -->` , por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="68096-580">**Importante**  Esse valor é consultado para determinar se uma nova versão de um modelo deve ser aplicada a um modelo existente nestes casos:</span><span class="sxs-lookup"><span data-stu-id="68096-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="68096-581">Quando a tarefa de atualização automática do modelo agendado é executada</span><span class="sxs-lookup"><span data-stu-id="68096-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="68096-582">Quando o cmdlet Update-UevTemplate do PowerShell é executado</span><span class="sxs-lookup"><span data-stu-id="68096-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="68096-583">Quando o método de atualização microsoft\\uev: SettingsLocationTemplate é chamado por meio do WMI</span><span class="sxs-lookup"><span data-stu-id="68096-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="68096-584">Elemento Author</span><span class="sxs-lookup"><span data-stu-id="68096-584">Author Element</span></span>

**<span data-ttu-id="68096-585">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-585">Mandatory: False</span></span>**

**<span data-ttu-id="68096-586">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-586">Type: String</span></span>**

<span data-ttu-id="68096-587">O autor identifica o criador do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="68096-588">Há suporte para dois elementos filho opcionais: **nome** e **email**.</span><span class="sxs-lookup"><span data-stu-id="68096-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="68096-589">Os dois atributos são opcionais, mas, se o elemento filho do email for especificado, ele deve ser acompanhado pelo elemento Name.</span><span class="sxs-lookup"><span data-stu-id="68096-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="68096-590">O autor se refere ao nome completo do contato do modelo de local de configurações e o email deve se referir a um endereço de email para o autor.</span><span class="sxs-lookup"><span data-stu-id="68096-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="68096-591">Recomendamos que você inclua essas informações nos modelos publicados publicamente, por exemplo, na [Galeria de modelos do UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="68096-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="68096-592">Elemento processos e processo</span><span class="sxs-lookup"><span data-stu-id="68096-592">Processes and Process Element</span></span>

**<span data-ttu-id="68096-593">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-593">Mandatory: True</span></span>**

**<span data-ttu-id="68096-594">Tipo: Element</span><span class="sxs-lookup"><span data-stu-id="68096-594">Type: Element</span></span>**

<span data-ttu-id="68096-595">Os processos contêm pelo menos `<Process>` um elemento, que, por sua vez, contém os seguintes elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="68096-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="68096-596">O elemento filho filename é obrigatório e os outros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="68096-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="68096-597">Um elemento totalmente preenchido contém marcas semelhantes a este exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="68096-598">Arq</span><span class="sxs-lookup"><span data-stu-id="68096-598">Filename</span></span>

**<span data-ttu-id="68096-599">Obrigatório: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="68096-599">Mandatory: True</span></span>**

**<span data-ttu-id="68096-600">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-600">Type: String</span></span>**

<span data-ttu-id="68096-601">O nome do arquivo refere-se ao nome de arquivo real do executável exibido no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="68096-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="68096-602">Esse elemento Especifica o critério principal que o UE-V usa para avaliar se um modelo se aplica a um processo ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="68096-603">Esse elemento deve ser especificado no modelo de local de configurações XML.</span><span class="sxs-lookup"><span data-stu-id="68096-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="68096-604">Nomes de fileválidas não devem coincidir com a expressão regular \ [^ \ \ \ \ \ \? \ \ \ \* \ \ | &lt; &gt; /: \] +, ou seja, eles podem não conter caracteres de barra invertida, asterisco ou interrogação de caracteres curinga, o caractere de tubo, o sinal de maior ou menor que, barra ou dois pontos (o \ \?</span><span class="sxs-lookup"><span data-stu-id="68096-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="68096-605">\* | &lt; &gt; /ou: caracteres.).</span><span class="sxs-lookup"><span data-stu-id="68096-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="68096-606">**Dica:** Para testar uma cadeia de caracteres nesse Regex, use uma janela de comando do PowerShell e substitua o nome do seu executável para **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="68096-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="68096-607">Um valor **true** indica que a cadeia de caracteres contém caracteres ilegais.</span><span class="sxs-lookup"><span data-stu-id="68096-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="68096-608">Veja alguns exemplos de valores ilegais:</span><span class="sxs-lookup"><span data-stu-id="68096-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="68096-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="68096-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="68096-610">Programa \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="68096-610">Program\*.exe</span></span>

-   <span data-ttu-id="68096-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="68096-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="68096-612">Programa &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="68096-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="68096-613">**Observação**  O gerador do UE-V codifica o maior que e menor que os caracteres como &gt; e &lt; respectivamente.</span><span class="sxs-lookup"><span data-stu-id="68096-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="68096-614">Em circunstâncias raras, o valor FileName não inclui necessariamente a extensão. exe, mas ele deve ser especificado como parte do valor.</span><span class="sxs-lookup"><span data-stu-id="68096-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="68096-615">Por exemplo, `<Filename>MyApplictication.exe</Filename>` deve ser especificado em vez de `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="68096-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="68096-616">O segundo exemplo não aplicará o modelo ao processo, se o nome real do arquivo executável for "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="68096-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="68096-617">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="68096-617">Architecture</span></span>

**<span data-ttu-id="68096-618">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-618">Mandatory: False</span></span>**

**<span data-ttu-id="68096-619">Tipo: Architecture (cadeia)</span><span class="sxs-lookup"><span data-stu-id="68096-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="68096-620">Arquitetura refere-se à arquitetura do processador para a qual o executável de destino foi compilado.</span><span class="sxs-lookup"><span data-stu-id="68096-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="68096-621">Os valores válidos são Win32 para aplicativos de 32 bits ou Win64 para aplicativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="68096-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="68096-622">Se presente, essa marca limita a aplicabilidade do modelo de local de configurações a uma arquitetura de aplicativo específica.</span><span class="sxs-lookup"><span data-stu-id="68096-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="68096-623">Para obter um exemplo disso, compare a experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e arquivos de MicrosoftOffice2010Win64.xml incluídos na UE-V.</span><span class="sxs-lookup"><span data-stu-id="68096-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="68096-624">Isso é útil quando caminhos relativos mudam entre versões diferentes de um executável ou se as configurações foram adicionadas ou removidas ao passar de uma arquitetura de processador para outra.</span><span class="sxs-lookup"><span data-stu-id="68096-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="68096-625">Se esse elemento estiver ausente, o modelo de local de configurações ignorará a arquitetura do processo e se aplicará aos processos do 32 e do 64-bit se o nome do arquivo e outros atributos se aplicarem.</span><span class="sxs-lookup"><span data-stu-id="68096-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="68096-626">**Observação**  A UE-V não oferece suporte a processadores ARM nesta versão.</span><span class="sxs-lookup"><span data-stu-id="68096-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="68096-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="68096-627">ProductName</span></span>

**<span data-ttu-id="68096-628">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-628">Mandatory: False</span></span>**

**<span data-ttu-id="68096-629">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-629">Type: String</span></span>**

<span data-ttu-id="68096-630">O NomeDoProduto é um elemento opcional usado para identificar um produto para fins administrativos ou relatórios.</span><span class="sxs-lookup"><span data-stu-id="68096-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="68096-631">O NomeDoProduto é diferente do nome do arquivo, pois não há restrições de expressão regular em seu valor.</span><span class="sxs-lookup"><span data-stu-id="68096-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="68096-632">Isso permite descrições mais facilmente compreendidas de um processo em que o nome do executável pode não ser óbvio.</span><span class="sxs-lookup"><span data-stu-id="68096-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="68096-633">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="68096-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="68096-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="68096-634">FileDescription</span></span>

**<span data-ttu-id="68096-635">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-635">Mandatory: False</span></span>**

**<span data-ttu-id="68096-636">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-636">Type: String</span></span>**

<span data-ttu-id="68096-637">FileDescription é uma marca opcional que permite uma descrição administrativa do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="68096-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="68096-638">Esse é um campo de texto gratuito e pode ser útil para distinguir vários executáveis dentro de um pacote de software onde há necessidade de identificar a função do executável.</span><span class="sxs-lookup"><span data-stu-id="68096-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="68096-639">Por exemplo, em um aplicativo adequado, pode ser útil fornecer lembretes sobre a função de dois executáveis (MyApplication.exe e MyApplicationHelper.exe), como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="68096-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="68096-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="68096-640">ProductVersion</span></span>

**<span data-ttu-id="68096-641">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-641">Mandatory: False</span></span>**

**<span data-ttu-id="68096-642">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-642">Type: String</span></span>**

<span data-ttu-id="68096-643">ProductVersion refere-se às versões de produto principais e secundárias de um arquivo, bem como um nível de compilação e patch.</span><span class="sxs-lookup"><span data-stu-id="68096-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="68096-644">ProductVersion é um elemento opcional, mas, se especificado, ele deve conter pelo menos o elemento filho Major.</span><span class="sxs-lookup"><span data-stu-id="68096-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="68096-645">O valor deve expressar um intervalo no formato Minimum = "X" Maximum = "Y", em que X e Y são inteiros.</span><span class="sxs-lookup"><span data-stu-id="68096-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="68096-646">Os valores mínimo e máximo podem ser idênticos.</span><span class="sxs-lookup"><span data-stu-id="68096-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="68096-647">Os elementos da versão do produto e do arquivo podem não ser especificados.</span><span class="sxs-lookup"><span data-stu-id="68096-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="68096-648">Fazer isso torna o modelo "versão independente", o que significa que o modelo será aplicado a todas as versões do executável especificado.</span><span class="sxs-lookup"><span data-stu-id="68096-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="68096-649">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="68096-649">Example 1:</span></span>**

<span data-ttu-id="68096-650">Versão do produto: 1,0 especificado no UE-V Generator produz o seguinte XML:</span><span class="sxs-lookup"><span data-stu-id="68096-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="68096-651">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="68096-651">Example 2:</span></span>**

<span data-ttu-id="68096-652">Versão do arquivo: 5.0.2.1000 especificado no UE-V Generator produz o seguinte XML:</span><span class="sxs-lookup"><span data-stu-id="68096-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="68096-653">Exemplo 1 incorreto – intervalo incompleto:</span><span class="sxs-lookup"><span data-stu-id="68096-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="68096-654">Somente o atributo mínimo está presente.</span><span class="sxs-lookup"><span data-stu-id="68096-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="68096-655">O máximo também deve ser incluído em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="68096-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="68096-656">Exemplo 2 incorreto – especificado secundário sem elemento principal:</span><span class="sxs-lookup"><span data-stu-id="68096-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="68096-657">Somente o elemento secundário está presente.</span><span class="sxs-lookup"><span data-stu-id="68096-657">Only the Minor element is present.</span></span> <span data-ttu-id="68096-658">Importante também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="68096-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="68096-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="68096-659">FileVersion</span></span>

**<span data-ttu-id="68096-660">Obrigatório: falso</span><span class="sxs-lookup"><span data-stu-id="68096-660">Mandatory: False</span></span>**

**<span data-ttu-id="68096-661">Tipo: cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="68096-661">Type: String</span></span>**

<span data-ttu-id="68096-662">FileVersion diferencia a versão de lançamento de um aplicativo publicado e os detalhes de compilação interna de um executável de componente.</span><span class="sxs-lookup"><span data-stu-id="68096-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="68096-663">Para a maioria dos aplicativos comerciais, esses números são idênticos.</span><span class="sxs-lookup"><span data-stu-id="68096-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="68096-664">Onde elas variam, a versão do produto de um arquivo indica uma identificação genérica de versão de um arquivo, enquanto a versão do arquivo indica uma compilação específica de um arquivo (como no caso de um hotfix ou atualização).</span><span class="sxs-lookup"><span data-stu-id="68096-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="68096-665">Isso identifica arquivos com exclusividade sem interromper a lógica de detecção.</span><span class="sxs-lookup"><span data-stu-id="68096-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="68096-666">Para determinar a versão do produto e o arquivo de um determinado executável, clique com o botão direito do mouse no arquivo no Windows Explorer, selecione Propriedades e, em seguida, clique na guia detalhes.</span><span class="sxs-lookup"><span data-stu-id="68096-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="68096-667">Incluir um elemento FileVersion para um aplicativo permite uma lógica de detecção de ajuste de precisão mais granular, mas não é necessário para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="68096-668">As configurações do elemento ProductVersion são verificadas primeiro e, em seguida, FileVersion está marcada.</span><span class="sxs-lookup"><span data-stu-id="68096-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="68096-669">A configuração mais restritiva será aplicada.</span><span class="sxs-lookup"><span data-stu-id="68096-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="68096-670">Os elementos filho e as regras de sintaxe para FileVersion são idênticos aos do ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="68096-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="68096-671">Elemento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="68096-671">Application Element</span></span>

<span data-ttu-id="68096-672">Aplicativo é um contêiner para configurações que se aplicam a um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="68096-673">Ele é uma coleção dos seguintes campos/tipos.</span><span class="sxs-lookup"><span data-stu-id="68096-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68096-674">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="68096-675">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-676">Name</span><span class="sxs-lookup"><span data-stu-id="68096-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-677">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-678">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-679">Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-680">ID</span><span class="sxs-lookup"><span data-stu-id="68096-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-681">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-682">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-683">Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-684">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-685">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-686">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-687">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-689">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-690">Versão</span><span class="sxs-lookup"><span data-stu-id="68096-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-691">Identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-692">Para obter mais informações, consulte <a href="#version" data-raw-source="[Version](#version)"> versão </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="68096-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-694">Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="68096-695">Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="68096-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-697">Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365.</span><span class="sxs-lookup"><span data-stu-id="68096-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="68096-698">Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-699">Processos</span><span class="sxs-lookup"><span data-stu-id="68096-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-700">Um contêiner para uma coleção de um ou mais elementos de processo.</span><span class="sxs-lookup"><span data-stu-id="68096-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="68096-701">Para obter mais informações, consulte <a href="#processes" data-raw-source="[Processes](#processes)"> processos </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-702">Configurações</span><span class="sxs-lookup"><span data-stu-id="68096-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-703">Um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-704">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="68096-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="68096-705">Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data" data-raw-source="[Data types](#data)"> tipos de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="68096-706">Elemento comum</span><span class="sxs-lookup"><span data-stu-id="68096-706">Common Element</span></span>

<span data-ttu-id="68096-707">Comum é semelhante a um elemento de aplicativo, mas ele sempre é associado a dois ou mais elementos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="68096-708">A seção comum representa o conjunto de configurações compartilhadas entre essas instâncias de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68096-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="68096-709">Ele é uma coleção dos seguintes campos/tipos.</span><span class="sxs-lookup"><span data-stu-id="68096-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68096-710">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="68096-711">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-712">Name</span><span class="sxs-lookup"><span data-stu-id="68096-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-713">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-714">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-715">Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-716">ID</span><span class="sxs-lookup"><span data-stu-id="68096-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-717">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-718">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-719">Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-720">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-721">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-722">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-723">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-725">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-726">Versão</span><span class="sxs-lookup"><span data-stu-id="68096-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-727">Identifica a versão do modelo de local de configurações para o controle administrativo de alterações.</span><span class="sxs-lookup"><span data-stu-id="68096-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="68096-728">Para obter mais informações, consulte <a href="#version" data-raw-source="[Version](#version)"> versão </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="68096-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-730">Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não.</span><span class="sxs-lookup"><span data-stu-id="68096-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="68096-731">Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="68096-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-733">Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365.</span><span class="sxs-lookup"><span data-stu-id="68096-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="68096-734">Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="68096-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-735">Configurações</span><span class="sxs-lookup"><span data-stu-id="68096-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-736">Um contêiner para todas as configurações que se aplicam a um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="68096-737">Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction.</span><span class="sxs-lookup"><span data-stu-id="68096-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="68096-738">Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data" data-raw-source="[Data types](#data)"> tipos de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="68096-739">Elemento SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="68096-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="68096-740">Esse elemento define as configurações para um único aplicativo ou um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68096-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="68096-741">Campo/tipo</span><span class="sxs-lookup"><span data-stu-id="68096-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="68096-742">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-743">Name</span><span class="sxs-lookup"><span data-stu-id="68096-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-744">Especifica um nome exclusivo para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="68096-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="68096-745">Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração.</span><span class="sxs-lookup"><span data-stu-id="68096-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="68096-746">Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-747">ID</span><span class="sxs-lookup"><span data-stu-id="68096-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-748">Preenche um identificador exclusivo para um modelo específico.</span><span class="sxs-lookup"><span data-stu-id="68096-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="68096-749">Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="68096-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="68096-750">Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="68096-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-751">Descrição</span><span class="sxs-lookup"><span data-stu-id="68096-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-752">Uma descrição opcional do modelo.</span><span class="sxs-lookup"><span data-stu-id="68096-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="68096-753">Localizadores</span><span class="sxs-lookup"><span data-stu-id="68096-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-754">Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="68096-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="68096-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="68096-756">Uma descrição de modelo opcional localizada por uma localidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="68096-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="68096-757">Apêndice: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="68096-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="68096-758">Aqui está o arquivo SettingsLocationTemplate. xsd que mostra seus elementos, elementos filho, atributos e parâmetros:</span><span class="sxs-lookup"><span data-stu-id="68096-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="68096-759">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68096-759">Related topics</span></span>


[<span data-ttu-id="68096-760">Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator</span><span class="sxs-lookup"><span data-stu-id="68096-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="68096-761">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="68096-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





