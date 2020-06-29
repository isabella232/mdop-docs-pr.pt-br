---
title: Como definir as configurações de Registro do cliente do App-V usando a linha de comando
description: Como definir as configurações de Registro do cliente do App-V usando a linha de comando
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797217"
---
# <span data-ttu-id="146d7-103">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="146d7-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="146d7-104">Após a implantação e configuração do cliente do Application Virtualization (App-V) durante a instalação usando a linha de comando, talvez seja necessário alterar uma ou mais configurações de cliente.</span><span class="sxs-lookup"><span data-stu-id="146d7-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="146d7-105">Isso é feito editando-se as chaves do registro apropriadas usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="146d7-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="146d7-106">Usar o editor de registro diretamente</span><span class="sxs-lookup"><span data-stu-id="146d7-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="146d7-107">Usando um arquivo. reg</span><span class="sxs-lookup"><span data-stu-id="146d7-107">Using a .reg file</span></span>

-   <span data-ttu-id="146d7-108">Usando uma linguagem de script como VBScript ou Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="146d7-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="146d7-109">Também há um modelo ADM que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="146d7-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="146d7-110">Para obter mais informações sobre o modelo ADM, consulte <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="146d7-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="146d7-111">**Cuidado**  Tome cuidado ao editar o registro porque os erros podem deixar o computador em um estado inutilizável.</span><span class="sxs-lookup"><span data-stu-id="146d7-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="146d7-112">Certifique-se de seguir as práticas comerciais padrão relacionadas às edições do registro.</span><span class="sxs-lookup"><span data-stu-id="146d7-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="146d7-113">Teste completamente todas as alterações propostas em um ambiente de teste antes de implantá-las nos computadores de produção.</span><span class="sxs-lookup"><span data-stu-id="146d7-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="146d7-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="146d7-114">In This Section</span></span>


<span data-ttu-id="146d7-115">**Importante**  Em um computador de 64 bits, as chaves e os valores descritos nas seções a seguir estarão em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="146d7-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="146d7-116">Como redefinir o cache do FileSystem</span><span class="sxs-lookup"><span data-stu-id="146d7-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="146d7-117">Fornece as informações necessárias para redefinir o cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="146d7-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="146d7-118">Como alterar o tamanho do cache do FileSystem</span><span class="sxs-lookup"><span data-stu-id="146d7-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="146d7-119">Explica como você pode alterar o tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="146d7-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="146d7-120">Como Usar o Recurso de Gerenciamento de Espaço do Cache</span><span class="sxs-lookup"><span data-stu-id="146d7-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="146d7-121">Descreve como você pode configurar o recurso de gerenciamento de espaço em cache.</span><span class="sxs-lookup"><span data-stu-id="146d7-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="146d7-122">Como configurar o arquivo de log do cliente</span><span class="sxs-lookup"><span data-stu-id="146d7-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="146d7-123">Descreve os vários valores da chave do registro que controlam o arquivo de log do cliente e como você pode alterá-los.</span><span class="sxs-lookup"><span data-stu-id="146d7-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="146d7-124">Como configurar permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="146d7-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="146d7-125">Identifica a chave do registro que controla as permissões do usuário e fornece exemplos de como você pode alterar algumas permissões.</span><span class="sxs-lookup"><span data-stu-id="146d7-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="146d7-126">Como configurar o cliente para recuperação de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="146d7-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="146d7-127">Explica como configurar o cliente para recuperar conteúdo do pacote, ícones e associações de tipo de arquivo de fontes diferentes e fornece vários exemplos de formato de caminho correto.</span><span class="sxs-lookup"><span data-stu-id="146d7-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="146d7-128">Como configurar o cliente para o Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="146d7-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="146d7-129">Fornece informações sobre como definir as várias configurações associadas ao modo de operações desconectadas.</span><span class="sxs-lookup"><span data-stu-id="146d7-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="146d7-130">Como configurar o comportamento de atalhos e de associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="146d7-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="146d7-131">Descreve os valores da chave do registro que controlam atalhos e associações de tipo de arquivo no cliente App-V e fornece detalhes sobre como configurá-los.</span><span class="sxs-lookup"><span data-stu-id="146d7-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="146d7-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="146d7-132">Related topics</span></span>


[<span data-ttu-id="146d7-133">Cliente do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="146d7-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





