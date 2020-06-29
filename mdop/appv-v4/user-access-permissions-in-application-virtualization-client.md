---
title: Permissões de acesso de usuário no Application Virtualization Client
description: Permissões de acesso de usuário no Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796661"
---
# <span data-ttu-id="53582-103">Permissões de acesso de usuário no Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="53582-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="53582-104">Na guia **permissões** , na caixa de diálogo **Propriedades** , acessível ao clicar com o botão direito do mouse no nó **virtualização do aplicativo** no console de gerenciamento do aplicativo virtualização de aplicativos, os administradores podem conceder permissões aos usuários para usar as várias funções de cliente.</span><span class="sxs-lookup"><span data-stu-id="53582-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="53582-105">**Observação**  Antes de alterar as permissões de usuários, certifique-se de que as alterações de permissões sejam consistentes com as diretrizes da organização para conceder permissões de usuário.</span><span class="sxs-lookup"><span data-stu-id="53582-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="53582-106">A tabela a seguir lista e descreve as permissões que podem ser concedidas aos usuários.</span><span class="sxs-lookup"><span data-stu-id="53582-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="53582-107">Nome da permissão</span><span class="sxs-lookup"><span data-stu-id="53582-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="53582-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="53582-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-109">Adicionar aplicativos</span><span class="sxs-lookup"><span data-stu-id="53582-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-110">Registre novos aplicativos passando um novo arquivo OSD para o cliente usando sfttray.exe, sftmime.exe ou o MMC.</span><span class="sxs-lookup"><span data-stu-id="53582-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-111">Alterar o tamanho do cache do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="53582-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-112">Aumente o tamanho do cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="53582-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-113">Alterar unidade do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="53582-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-114">Selecione uma letra de unidade preferida diferente para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="53582-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-115">Alterar configurações de log</span><span class="sxs-lookup"><span data-stu-id="53582-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-116">Altere o nível de log ou o caminho do log para o arquivo de log do cliente.</span><span class="sxs-lookup"><span data-stu-id="53582-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-117">Alterar arquivos OSD</span><span class="sxs-lookup"><span data-stu-id="53582-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-118">Modifique arquivos OSD para aplicativos registrados e passe-os para o cliente.</span><span class="sxs-lookup"><span data-stu-id="53582-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="53582-119">Isso não afeta a publicação de atualização.</span><span class="sxs-lookup"><span data-stu-id="53582-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-120">Limpar configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="53582-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-121">Exclua tipos de arquivo, atalhos e todas as configurações do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="53582-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-122">Excluir aplicativos</span><span class="sxs-lookup"><span data-stu-id="53582-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-123">Remova todas as referências a um aplicativo do sistema de arquivos e do cache do OSD para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="53582-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-124">Importar aplicativos para o cache</span><span class="sxs-lookup"><span data-stu-id="53582-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-125">Carregar dados de aplicativo diretamente de um arquivo SFT especificado no cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="53582-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="53582-126">Isso afeta todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="53582-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-127">Carregar aplicativos no cache</span><span class="sxs-lookup"><span data-stu-id="53582-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-128">Inicie uma carga do arquivo SFT para um aplicativo da fonte configurada, como um servidor de streaming App-V.</span><span class="sxs-lookup"><span data-stu-id="53582-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="53582-129">Isso carrega o aplicativo para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="53582-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-130">Bloquear e desbloquear aplicativos no cache</span><span class="sxs-lookup"><span data-stu-id="53582-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-131">Impedir ou permitir que os aplicativos sejam descarregados do cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="53582-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="53582-132">Isso afetará todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="53582-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-133">Gerenciar associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="53582-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-134">Adicionar, modificar ou excluir associações de tipo de arquivo somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="53582-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-135">Gerenciar configurações de atualização de publicação</span><span class="sxs-lookup"><span data-stu-id="53582-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-136">Altere as configurações que controlam o tempo de publicação de atualizações para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="53582-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-137">Gerenciar servidores de publicação</span><span class="sxs-lookup"><span data-stu-id="53582-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-138">Adicionar, modificar ou excluir servidores de publicação para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="53582-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="53582-139">Essa permissão implicitamente inclui permissão para gerenciar as configurações de atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="53582-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-140">Publicar atalhos</span><span class="sxs-lookup"><span data-stu-id="53582-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-141">Crie novos atalhos para aplicativos registrados.</span><span class="sxs-lookup"><span data-stu-id="53582-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="53582-142">O usuário também deve ter permissão para criar arquivos no sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="53582-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-143">Reparar aplicativos</span><span class="sxs-lookup"><span data-stu-id="53582-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-144">Remover configurações específicas do aplicativo para o usuário atual sem remover atalhos ou associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="53582-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-145">Iniciar uma atualização de publicação</span><span class="sxs-lookup"><span data-stu-id="53582-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-146">Iniciar uma atualização de publicação não agendada para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="53582-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-147">Alternar o modo offline</span><span class="sxs-lookup"><span data-stu-id="53582-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-148">Altere o cliente inteiro de online para o modo offline para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="53582-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="53582-149">Descarregar aplicativos do cache</span><span class="sxs-lookup"><span data-stu-id="53582-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-150">Limpar dados de aplicativo do cache do sistema de arquivos para todos os usuários sem remover configurações específicas do usuário, atalhos ou associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="53582-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="53582-151">Exibir todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="53582-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="53582-152">Permita que o usuário veja os aplicativos virtuais para todos os usuários registrados no computador.</span><span class="sxs-lookup"><span data-stu-id="53582-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="53582-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53582-153">Related topics</span></span>


[<span data-ttu-id="53582-154">Como alterar permissões de acesso de usuário</span><span class="sxs-lookup"><span data-stu-id="53582-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





