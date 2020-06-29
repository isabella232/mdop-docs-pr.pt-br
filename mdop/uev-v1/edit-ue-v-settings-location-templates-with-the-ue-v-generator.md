---
title: Editar modelos de localização de configurações da UE-V com o gerador da UE-V
description: Editar modelos de localização de configurações da UE-V com o gerador da UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800007"
---
# <span data-ttu-id="7fc69-103">Editar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="7fc69-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="7fc69-104">Use o gerador do Microsoft User Experience Virtualization (UE-V) para editar modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="7fc69-105">Quando as configurações revisadas são adicionadas aos modelos usando o UE-V Generator, as informações de versão no modelo são atualizadas automaticamente para garantir que os modelos existentes implantados na empresa sejam atualizados corretamente.</span><span class="sxs-lookup"><span data-stu-id="7fc69-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="7fc69-106">Como editar um modelo de local de configurações do UE-V com o UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="7fc69-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="7fc69-107">Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="7fc69-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="7fc69-108">Clique em **Editar um modelo de local de configurações**.</span><span class="sxs-lookup"><span data-stu-id="7fc69-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="7fc69-109">Na lista de modelos usados recentemente, selecione o modelo a ser editado.</span><span class="sxs-lookup"><span data-stu-id="7fc69-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="7fc69-110">Ou, se preferir, **navegue** até o arquivo de modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="7fc69-111">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="7fc69-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="7fc69-112">Examine as **Propriedades**, locais **do registro** e locais de **arquivos** do modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="7fc69-113">Edite conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7fc69-113">Edit as needed.</span></span>

    -   <span data-ttu-id="7fc69-114">A guia **Propriedades** permite que você exiba e edite as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="7fc69-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="7fc69-115">**Nome do aplicativo**: o nome do aplicativo escrito na descrição das propriedades do arquivo de programa.</span><span class="sxs-lookup"><span data-stu-id="7fc69-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="7fc69-116">**Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa.</span><span class="sxs-lookup"><span data-stu-id="7fc69-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="7fc69-117">Esse nome geralmente tem a extensão. exe.</span><span class="sxs-lookup"><span data-stu-id="7fc69-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="7fc69-118">**Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="7fc69-119">Essa propriedade, juntamente com a **versão do arquivo**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7fc69-120">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="7fc69-120">This property accepts a major version number.</span></span> <span data-ttu-id="7fc69-121">Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do produto.</span><span class="sxs-lookup"><span data-stu-id="7fc69-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="7fc69-122">**Versão do arquivo**: o número da versão do arquivo the.exe arquivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="7fc69-123">Essa propriedade, juntamente com a **versão do produto**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="7fc69-124">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="7fc69-124">This property accepts a major version number.</span></span> <span data-ttu-id="7fc69-125">Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do programa.</span><span class="sxs-lookup"><span data-stu-id="7fc69-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="7fc69-126">**Nome do autor do modelo** (opcional): o nome do autor do modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="7fc69-127">**Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="7fc69-128">A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="7fc69-129">Você pode editar os locais do registro usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="7fc69-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7fc69-130">As tarefas incluem adicionar novas chaves, editar o nome ou o escopo de chaves existentes, excluir chaves e navegar pelo registro no qual as chaves estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="7fc69-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="7fc69-131">Ao definir o escopo do registro, você pode usar o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada.</span><span class="sxs-lookup"><span data-stu-id="7fc69-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="7fc69-132">Use **todas as configurações** e **subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.</span><span class="sxs-lookup"><span data-stu-id="7fc69-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="7fc69-133">A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais do arquivo incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="7fc69-134">Você pode editar os locais de arquivos usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="7fc69-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="7fc69-135">As tarefas para locais de arquivos incluem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7fc69-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="7fc69-136">Para incluir todos os arquivos na pasta especificada, deixe a máscara de arquivo vazia.</span><span class="sxs-lookup"><span data-stu-id="7fc69-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="7fc69-137">Clique em **salvar** para salvar as alterações no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="7fc69-138">Clique em **fechar** para fechar o assistente de modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="7fc69-139">Saia do aplicativo do gerador do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7fc69-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="7fc69-140">Depois de editar o modelo de local de configurações para um aplicativo, você deve testar o modelo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="7fc69-141">Implante o modelo de local de configurações revisado em um ambiente de laboratório antes de colocá-lo em produção na empresa.</span><span class="sxs-lookup"><span data-stu-id="7fc69-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="7fc69-142">Como editar manualmente um modelo de local de configurações</span><span class="sxs-lookup"><span data-stu-id="7fc69-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="7fc69-143">Criar uma cópia local do modelo de local de configurações (arquivo. xml).</span><span class="sxs-lookup"><span data-stu-id="7fc69-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="7fc69-144">Os modelos de local das configurações do UE-V são arquivos. xml identificando os locais onde os valores das configurações de repositório do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fc69-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="7fc69-145">Abra o arquivo de modelo de local de configurações com um editor de XML.</span><span class="sxs-lookup"><span data-stu-id="7fc69-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="7fc69-146">Edite o arquivo de modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="7fc69-146">Edit the settings location template file.</span></span> <span data-ttu-id="7fc69-147">Todas as alterações devem estar de acordo com o arquivo de esquema do UE-V definido em SettingsLocationTempate. xsd.</span><span class="sxs-lookup"><span data-stu-id="7fc69-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="7fc69-148">Uma cópia do arquivo. xsd está localizada `\ProgramData\Microsoft\UEV\Templates` por padrão.</span><span class="sxs-lookup"><span data-stu-id="7fc69-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="7fc69-149">Salve o arquivo de modelo de local de configurações e feche o editor de XML.</span><span class="sxs-lookup"><span data-stu-id="7fc69-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="7fc69-150">Valide o arquivo de modelo de local de configurações modificadas com o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="7fc69-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="7fc69-151">Para obter mais informações sobre como validar com o UE-V Generator, consulte [validar modelos de local de configurações do UE-v com o UE-v Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="7fc69-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="7fc69-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fc69-152">Related topics</span></span>


[<span data-ttu-id="7fc69-153">Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="7fc69-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="7fc69-154">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7fc69-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





