---
title: Segurança do cliente da área de trabalho do App-V
description: Segurança do cliente da área de trabalho do App-V
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799048"
---
# <span data-ttu-id="3f836-103">Segurança do cliente da área de trabalho do App-V</span><span class="sxs-lookup"><span data-stu-id="3f836-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="3f836-104">O cliente da área de trabalho do App-V fornece muitos aprimoramentos de segurança que não estavam disponíveis nas versões anteriores do produto.</span><span class="sxs-lookup"><span data-stu-id="3f836-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="3f836-105">Essas alterações fornecem níveis mais altos de segurança por padrão e por meio da configuração das configurações do cliente.</span><span class="sxs-lookup"><span data-stu-id="3f836-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="3f836-106">**Observação**  Quando você instala o cliente da área de trabalho do App-V em um computador, o software é definido como padrão para as configurações mais seguras.</span><span class="sxs-lookup"><span data-stu-id="3f836-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="3f836-107">No entanto, ao atualizar, as configurações anteriores do cliente persistem.</span><span class="sxs-lookup"><span data-stu-id="3f836-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="3f836-108">Por padrão, o cliente da área de trabalho App-V é configurado somente com as permissões necessárias para permitir que um usuário não administrativo execute uma atualização de publicação e aplicativos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3f836-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="3f836-109">Aprimoramentos de segurança adicionais fornecidos no cliente da área de trabalho do App-V incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3f836-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="3f836-110">Por padrão, uma atualização de cache OSD é permitida apenas pelo processo de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="3f836-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="3f836-111">O arquivo de log ( `sftlog.txt` ) só pode ser acessado por contas com acesso administrativo local ao cliente.</span><span class="sxs-lookup"><span data-stu-id="3f836-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="3f836-112">O arquivo de log agora tem um tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="3f836-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="3f836-113">Os arquivos de log são gerenciados por meio das configurações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3f836-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="3f836-114">O log de eventos do sistema agora é executado.</span><span class="sxs-lookup"><span data-stu-id="3f836-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="3f836-115">Permissões</span><span class="sxs-lookup"><span data-stu-id="3f836-115">Permissions</span></span>


<span data-ttu-id="3f836-116">Depois de instalar o cliente de desktop, você pode definir outras configurações de segurança por meio do MMC ou de um cliente individual usando o registro ou o modelo ADM fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3f836-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="3f836-117">O cliente da área de trabalho App-V tem permissões que você pode definir para restringir o acesso de usuários não administrativos a todos os recursos do cliente da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3f836-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="3f836-118">Para obter uma lista completa de permissões, consulte o arquivo de ajuda do App-V Client ou o App-V Operations Guide.</span><span class="sxs-lookup"><span data-stu-id="3f836-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="3f836-119">**Importante**  Considere cuidadosamente as conseqüências da alteração dos direitos de acesso, especialmente em sistemas que são compartilhados por vários usuários, como servidores de terminal.</span><span class="sxs-lookup"><span data-stu-id="3f836-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="3f836-120">**Observação**  Se os usuários no ambiente tiverem privilégios de administrador local para seus computadores, as permissões serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="3f836-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="3f836-121">Modelo ADM</span><span class="sxs-lookup"><span data-stu-id="3f836-121">ADM Template</span></span>

<span data-ttu-id="3f836-122">O Microsoft Application Virtualization (App-V) introduz um modelo ADM que você pode usar para definir as configurações de cliente mais comuns por meio de políticas de grupo.</span><span class="sxs-lookup"><span data-stu-id="3f836-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="3f836-123">Este modelo permite que os administradores implementem e alterem muitas das configurações do cliente por meio de um modelo de administração centralizado.</span><span class="sxs-lookup"><span data-stu-id="3f836-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="3f836-124">Algumas das configurações disponíveis no modelo ADM são configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="3f836-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="3f836-125">**Importante**  Ao usar o modelo ADM, lembre-se de que as configurações são configurações de preferência de política de grupo e não diretivas de grupo totalmente gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="3f836-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="3f836-126">Para obter uma descrição completa do modelo ADM, as configurações específicas e a orientação para implantar clientes com êxito em seu ambiente, consulte o White Paper App-V ADM template at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="3f836-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="3f836-127">Removendo associações de tipo de arquivo OSD</span><span class="sxs-lookup"><span data-stu-id="3f836-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="3f836-128">Se a sua organização não exigir que os usuários abram aplicativos diretamente de um arquivo OSD, você pode melhorar a segurança removendo associações de tipo de arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="3f836-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="3f836-129">Remova as `HKEY_CURRENT_USERS` chaves para OSD e `Softgird.osd.file` use o editor de registro.</span><span class="sxs-lookup"><span data-stu-id="3f836-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="3f836-130">Você pode colocar esse processo em um script de logon ou em um script de pós-instalação para automatizar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="3f836-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





