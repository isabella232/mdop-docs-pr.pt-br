---
title: Criar modelos de localização de configurações da UE-V com o gerador da UE-V
description: Criar modelos de localização de configurações da UE-V com o gerador da UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799913"
---
# <span data-ttu-id="726f0-103">Criar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="726f0-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="726f0-104">O Microsoft User Experience Virtualization (UE-V Experience Virtualization) usa *modelos de local de configurações* para direcionar as configurações de aplicativo entre computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="726f0-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="726f0-105">Alguns modelos de local de configurações padrão estão incluídos na virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="726f0-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="726f0-106">Você também pode criar, editar ou validar modelos de local de configurações personalizadas com o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="726f0-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="726f0-107">O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="726f0-108">O aplicativo que está sendo monitorado deve ser um aplicativo tradicional.</span><span class="sxs-lookup"><span data-stu-id="726f0-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="726f0-109">O UE-V Generator não pode criar um modelo de local de configurações dos seguintes tipos de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="726f0-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="726f0-110">Aplicativos virtualizados</span><span class="sxs-lookup"><span data-stu-id="726f0-110">Virtualized applications</span></span>

-   <span data-ttu-id="726f0-111">Aplicativo oferecido por meio dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="726f0-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="726f0-112">Aplicativos Java</span><span class="sxs-lookup"><span data-stu-id="726f0-112">Java applications</span></span>

-   <span data-ttu-id="726f0-113">Aplicativos do Windows 8</span><span class="sxs-lookup"><span data-stu-id="726f0-113">Windows 8 applications</span></span>

<span data-ttu-id="726f0-114">**Observação**  Não é possível criar modelos UE-V em aplicativos virtualizados ou aplicativos de serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="726f0-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="726f0-115">No entanto, as configurações sincronizadas usando os modelos podem ser aplicadas a esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="726f0-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="726f0-116">Para criar modelos compatíveis com o VDI (Virtual Desktop Infrastructure) e aplicativos de serviços de terminal, abra um arquivo do Windows Installer (. msi) do aplicativo com o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="726f0-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="726f0-117">Locais excluídos</span><span class="sxs-lookup"><span data-stu-id="726f0-117">Excluded Locations</span></span>**

<span data-ttu-id="726f0-118">O processo de descoberta exclui locais que normalmente armazenam arquivos de software do aplicativo que não são bem transferidos entre computadores ou ambientes do usuário.</span><span class="sxs-lookup"><span data-stu-id="726f0-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="726f0-119">Os itens a seguir estão excluídos:</span><span class="sxs-lookup"><span data-stu-id="726f0-119">The following are excluded:</span></span>

-   <span data-ttu-id="726f0-120">HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores</span><span class="sxs-lookup"><span data-stu-id="726f0-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="726f0-121">HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows</span><span class="sxs-lookup"><span data-stu-id="726f0-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="726f0-122">Todas as chaves do registro localizadas na seção HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="726f0-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="726f0-123">Arquivos localizados em diretórios de arquivos de programas</span><span class="sxs-lookup"><span data-stu-id="726f0-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="726f0-124">Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="726f0-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="726f0-125">Arquivos do sistema operacional Windows localizado em% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="726f0-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="726f0-126">Se as chaves do registro e os arquivos armazenados nestes locais excluídos forem necessários para fazer roaming das configurações do aplicativo, os administradores poderão adicionar manualmente os locais ao modelo de local de configurações durante o processo de criação de modelos.</span><span class="sxs-lookup"><span data-stu-id="726f0-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="726f0-127">Criar modelos UE-V</span><span class="sxs-lookup"><span data-stu-id="726f0-127">Create UE-V templates</span></span>


<span data-ttu-id="726f0-128">Use o UE-V Generator para criar modelos de local de configurações para aplicativos de linha de negócios ou outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="726f0-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="726f0-129">Após a criação do modelo de um aplicativo, você pode implantar o modelo nos computadores para que os usuários possam fazer roaming das configurações desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="726f0-130">Para criar um modelo de local de configurações de UE-V com o UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="726f0-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="726f0-131">Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="726f0-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="726f0-132">Clique em **criar um modelo de local de configurações**.</span><span class="sxs-lookup"><span data-stu-id="726f0-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="726f0-133">Especifique o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-133">Specify the application.</span></span> <span data-ttu-id="726f0-134">Navegue até o caminho do arquivo do aplicativo (. exe) ou o atalho do aplicativo (. lnk) para o qual você deseja criar um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="726f0-135">Especifique os argumentos de linha de comando, se houver e em diretório de trabalho, se houver.</span><span class="sxs-lookup"><span data-stu-id="726f0-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="726f0-136">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="726f0-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="726f0-137">**Observação**  Antes de o aplicativo ser iniciado, o sistema exibe uma solicitação de **controle de conta de usuário**.</span><span class="sxs-lookup"><span data-stu-id="726f0-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="726f0-138">É necessário ter permissão para monitorar o registro e os locais de arquivo que o aplicativo usa para armazenar as configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="726f0-139">Depois que o aplicativo for iniciado, feche o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-139">After the application starts, close the application.</span></span> <span data-ttu-id="726f0-140">O gerador do UE-V registra os locais onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="726f0-141">Depois que o processo for concluído, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="726f0-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="726f0-142">Revise e marque as caixas de seleção ao lado dos locais de arquivos de configurações e locais de configurações do registro para fazer roaming deste aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="726f0-143">A lista inclui as duas categorias a seguir para locais de configurações:</span><span class="sxs-lookup"><span data-stu-id="726f0-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="726f0-144">**Padrão**: configurações de aplicativo que são armazenadas no registro nas chaves hKey \ _CURRENT \ _USER ou nas pastas de arquivo em \ \ **Users** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="726f0-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="726f0-145">O gerador do UE-V inclui essas configurações por padrão.</span><span class="sxs-lookup"><span data-stu-id="726f0-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="726f0-146">Não **padrão**: configurações do aplicativo armazenadas fora dos locais especificados nas práticas recomendadas para armazenamento de dados de configurações (opcional).</span><span class="sxs-lookup"><span data-stu-id="726f0-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="726f0-147">Isso inclui arquivos e pastas em **usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="726f0-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="726f0-148">Revise esses locais para determinar se devem ser incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="726f0-149">Marque as caixas de seleção de locais para incluí-las.</span><span class="sxs-lookup"><span data-stu-id="726f0-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="726f0-150">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="726f0-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="726f0-151">Revise e edite quaisquer **Propriedades**, locais **do registro** e locais de **arquivos** para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="726f0-152">Edite as seguintes propriedades na guia **Propriedades** :</span><span class="sxs-lookup"><span data-stu-id="726f0-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="726f0-153">**Nome do aplicativo**: o nome do aplicativo escrito na descrição das propriedades dos arquivos de programa.</span><span class="sxs-lookup"><span data-stu-id="726f0-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="726f0-154">**Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa.</span><span class="sxs-lookup"><span data-stu-id="726f0-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="726f0-155">Esse nome geralmente tem a extensão. exe.</span><span class="sxs-lookup"><span data-stu-id="726f0-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="726f0-156">**Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="726f0-157">Essa propriedade, em conjunto com a versão do arquivo, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="726f0-158">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="726f0-158">This property accepts a major version number.</span></span> <span data-ttu-id="726f0-159">Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do produto.</span><span class="sxs-lookup"><span data-stu-id="726f0-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="726f0-160">**Versão do arquivo**: o número da versão do arquivo the.exe arquivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="726f0-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="726f0-161">Essa propriedade, em conjunto com a versão do produto, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="726f0-162">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="726f0-162">This property accepts a major version number.</span></span> <span data-ttu-id="726f0-163">Se essa propriedade estiver vazia, o modelo de local de configurações será aplicado a todas as versões do programa.</span><span class="sxs-lookup"><span data-stu-id="726f0-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="726f0-164">**Nome do autor do modelo** (opcional): o nome do autor do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="726f0-165">**Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="726f0-166">A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="726f0-167">Edite os locais do registro usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="726f0-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="726f0-168">As tarefas incluem adicionar novas chaves, editar o nome ou o escopo de chaves existentes, excluir chaves e navegar no registro em que as chaves estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="726f0-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="726f0-169">Use o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada.</span><span class="sxs-lookup"><span data-stu-id="726f0-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="726f0-170">Use **todas as configurações e subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.</span><span class="sxs-lookup"><span data-stu-id="726f0-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="726f0-171">A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais do arquivo incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="726f0-172">Edite os locais de arquivos usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="726f0-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="726f0-173">As tarefas para locais de arquivos incluem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="726f0-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="726f0-174">Deixe a máscara de arquivo vazia para incluir todos os arquivos na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="726f0-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="726f0-175">Clique em **criar** e salvar o modelo de local de configurações no computador.</span><span class="sxs-lookup"><span data-stu-id="726f0-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="726f0-176">Clique em **fechar** para fechar o assistente de modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="726f0-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="726f0-177">Saia do aplicativo do gerador do UE-V.</span><span class="sxs-lookup"><span data-stu-id="726f0-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="726f0-178">Depois de criar o modelo de local de configurações para um aplicativo, você deve testar o modelo.</span><span class="sxs-lookup"><span data-stu-id="726f0-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="726f0-179">Implante o modelo em um ambiente de laboratório antes de colocá-lo em produção na empresa.</span><span class="sxs-lookup"><span data-stu-id="726f0-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="726f0-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="726f0-180">Related topics</span></span>


[<span data-ttu-id="726f0-181">Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="726f0-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="726f0-182">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="726f0-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





