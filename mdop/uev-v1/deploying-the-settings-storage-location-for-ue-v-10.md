---
title: Implantação da localização do armazenamento de configurações para a UE-V 1.0
description: Implantação da localização do armazenamento de configurações para a UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799912"
---
# <span data-ttu-id="d0e28-103">Implantação da localização do armazenamento de configurações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0e28-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="d0e28-104">A implantação do Microsoft User Experience Virtualization (UE-V Virtualization) requer um local de armazenamento de configurações onde as configurações do usuário estão armazenadas em um arquivo de pacote de configurações.</span><span class="sxs-lookup"><span data-stu-id="d0e28-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="d0e28-105">O local de armazenamento de configurações pode ser configurado de uma destas duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="d0e28-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="d0e28-106">**Active Directory Home Directory** – se um diretório base for definido para o usuário no Active Directory, o UE-V Agent usará esse local para armazenar pacotes de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="d0e28-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="d0e28-107">O UE-V Agent cria dinamicamente a pasta de armazenamento específica do usuário abaixo da raiz do diretório base.</span><span class="sxs-lookup"><span data-stu-id="d0e28-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="d0e28-108">O agente só usará o diretório base do Active Directory se um local de armazenamento de configurações não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="d0e28-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="d0e28-109">**Criar um compartilhamento de armazenamento de configurações** – o compartilhamento de armazenamento de configurações é um compartilhamento de rede padrão acessível a usuários do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0e28-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="d0e28-110">Implantar um compartilhamento de armazenamento de configurações de UE-V</span><span class="sxs-lookup"><span data-stu-id="d0e28-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="d0e28-111">Ao criar o compartilhamento de armazenamento de configurações, você deve limitar o acesso somente aos usuários que precisam de acesso.</span><span class="sxs-lookup"><span data-stu-id="d0e28-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="d0e28-112">As permissões necessárias são mostradas nas tabelas abaixo.</span><span class="sxs-lookup"><span data-stu-id="d0e28-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="d0e28-113">Para implantar o compartilhamento de rede UE-V</span><span class="sxs-lookup"><span data-stu-id="d0e28-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="d0e28-114">Crie um novo grupo de segurança para usuários do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d0e28-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="d0e28-115">Crie uma nova pasta no computador centralizado que armazenará os pacotes de configurações do UE-V e conceda os usuários do UE-V com permissões de grupo para a pasta.</span><span class="sxs-lookup"><span data-stu-id="d0e28-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="d0e28-116">O administrador que suporta UE-V precisará de permissões para essa pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="d0e28-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="d0e28-117">Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta de local de armazenamento de configuração:</span><span class="sxs-lookup"><span data-stu-id="d0e28-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="d0e28-118">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="d0e28-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="d0e28-119">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="d0e28-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d0e28-120">Todos</span><span class="sxs-lookup"><span data-stu-id="d0e28-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-121">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="d0e28-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d0e28-122">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="d0e28-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-123">Controle total</span><span class="sxs-lookup"><span data-stu-id="d0e28-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="d0e28-124">Defina as seguintes permissões de NTFS para a pasta de local de armazenamento de configurações:</span><span class="sxs-lookup"><span data-stu-id="d0e28-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="d0e28-125">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="d0e28-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="d0e28-126">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="d0e28-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="d0e28-127">Pasta</span><span class="sxs-lookup"><span data-stu-id="d0e28-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d0e28-128">Criador/proprietário</span><span class="sxs-lookup"><span data-stu-id="d0e28-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-129">Controle total</span><span class="sxs-lookup"><span data-stu-id="d0e28-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-130">Somente subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="d0e28-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d0e28-131">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="d0e28-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-132">Listar pasta/ler dados, criar pastas/acrescentar dados</span><span class="sxs-lookup"><span data-stu-id="d0e28-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d0e28-133">Somente esta pasta</span><span class="sxs-lookup"><span data-stu-id="d0e28-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="d0e28-134">Clique em **OK** para fechar as caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0e28-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="d0e28-135">Esta configuração de permissão permite que os usuários criem pastas para armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="d0e28-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="d0e28-136">O UE-V Agent cria e protege uma `settingspackage` pasta durante a execução no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0e28-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="d0e28-137">O usuário recebe controle total para a `settingspackage` pasta.</span><span class="sxs-lookup"><span data-stu-id="d0e28-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="d0e28-138">Outros usuários não herdam o acesso a essa pasta.</span><span class="sxs-lookup"><span data-stu-id="d0e28-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="d0e28-139">Você não precisa criar e proteger diretórios de usuário individuais, pois isso será feito automaticamente pelo agente que é executado no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0e28-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="d0e28-140">**Observação**  É possível configurar mais segurança quando um Windows Server é utilizado para o compartilhamento de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="d0e28-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="d0e28-141">O UE-V pode ser configurado para verificar se o grupo do administrador local ou o usuário atual é o proprietário da pasta na qual os pacotes de configurações são armazenados.</span><span class="sxs-lookup"><span data-stu-id="d0e28-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="d0e28-142">Para habilitar a segurança adicional, conclua o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d0e28-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="d0e28-143">Adicione uma chave do registro **reg \ _DWORD** chamada "RepositoryOwnerCheckEnabled" ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="d0e28-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="d0e28-144">Defina o valor da chave do registro como 1.</span><span class="sxs-lookup"><span data-stu-id="d0e28-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="d0e28-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0e28-145">Related topics</span></span>


[<span data-ttu-id="d0e28-146">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0e28-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="d0e28-147">Configurações com suporte para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d0e28-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="d0e28-148">Implantar o armazenamento central para configurações de virtualização de experiência do usuário modelos de configurações e pacotes [de configurações instalando o UE-V Generator](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="d0e28-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="d0e28-149">Implantação do agente da UE-V</span><span class="sxs-lookup"><span data-stu-id="d0e28-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





