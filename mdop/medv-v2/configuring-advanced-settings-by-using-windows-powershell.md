---
title: Definição das configurações avançadas usando o Windows PowerShell
description: Definição das configurações avançadas usando o Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800063"
---
# <span data-ttu-id="4411f-103">Definição das configurações avançadas usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4411f-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="4411f-104">O pacote do espaço de trabalho do MED-V que você cria inclui um arquivo de script do Windows PowerShell (. ps1) que você pode editar antes de testar e implantar o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="4411f-105">Esta seção fornece informações e orientação para ajudá-lo a gerenciar as configurações de configuração do MED-V usando o Windows PowerShell antes de implantar os espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="4411f-106">Usando cmdlets do Windows PowerShell no MED-V</span><span class="sxs-lookup"><span data-stu-id="4411f-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="4411f-107">Os seguintes cmdlets do Windows PowerShell estão disponíveis na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="4411f-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="4411f-108">New-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="4411f-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="4411f-109">Export-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="4411f-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="4411f-110">New-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="4411f-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="4411f-111">Export-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="4411f-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="4411f-112">Para acessar cmdlets do Windows PowerShell para MED-V, abra o Windows PowerShell e digite o seguinte comando para importar os módulos MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="4411f-113">Depois que os módulos forem importados, você poderá acessar a ajuda embutida para os cmdlets usando os comandos de ajuda padrão do Windows PowerShell, **Man** ou **Get-Help**.</span><span class="sxs-lookup"><span data-stu-id="4411f-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="4411f-114">Por exemplo, para acessar uma descrição do cmdlet **New-MedvConfiguration** incluindo uma lista completa de parâmetros disponíveis, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="4411f-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="4411f-115">Você também pode exibir a ajuda para parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="4411f-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="4411f-116">Por exemplo, para exibir a ajuda para o parâmetro VmMemory, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4411f-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="4411f-117">Para exibir uma lista de todas as configurações do MED-V e seus padrões, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="4411f-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="4411f-118">Para exibir uma lista de todas as definições de configuração do MED-V e seus valores atuais, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="4411f-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="4411f-119">Criando um espaço de trabalho do MED-V com configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="4411f-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="4411f-120">Depois de criar com êxito um pacote do espaço de trabalho do MED-V usando o pacote do espaço de trabalho do MED-V, um script do Windows PowerShell é gerado na pasta que você especificou para salvar os arquivos do pacote.</span><span class="sxs-lookup"><span data-stu-id="4411f-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="4411f-121">O conteúdo desse script mostra algumas das configurações de configuração do MED-V disponíveis que você pode editar.</span><span class="sxs-lookup"><span data-stu-id="4411f-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="4411f-122">Seguindo estas etapas, você pode personalizar o script e executá-lo no Windows PowerShell para criar um espaço de trabalho do MED-V com as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="4411f-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="4411f-123">**Importante**  Execute o Windows PowerShell com credenciais administrativas e certifique-se de que a política de execução do Windows PowerShell permita a execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="4411f-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="4411f-124">Edite o script do Windows PowerShell gerado pelo pacote do espaço de trabalho do MED-V ou crie um novo script com as definições de configuração desejadas.</span><span class="sxs-lookup"><span data-stu-id="4411f-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="4411f-125">Execute o Windows PowerShell com credenciais administrativas e, no prompt de comando, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="4411f-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="4411f-126">Esse comando executa o script do Windows PowerShell e executa o cmdlet **New-MedvWorkspace** para gerar um novo pacote de espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="4411f-127">Os novos arquivos do packager são salvos na pasta que você especificou originalmente para armazenar os arquivos do pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="4411f-128">Para obter ajuda adicional sobre esse cmdlet, consulte a ajuda do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4411f-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="4411f-129">Exportar uma configuração do MED-V para um arquivo do registro</span><span class="sxs-lookup"><span data-stu-id="4411f-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="4411f-130">Você pode atualizar as configurações de configuração do MED-V após a instalação do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4411f-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="4411f-131">Use o cmdlet **New-MedvConfiguration** para especificar os parâmetros que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="4411f-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="4411f-132">Por exemplo, para criar um arquivo de registro que altere a configuração de memória da máquina virtual, digite os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4411f-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="4411f-133">Você pode importar o arquivo resultante do registro do computador host para um espaço de trabalho do MED-V para aplicar as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="4411f-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="4411f-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4411f-134">Related topics</span></span>


[<span data-ttu-id="4411f-135">Gerenciamento de configurações do espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="4411f-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="4411f-136">Testar e implantar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="4411f-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





