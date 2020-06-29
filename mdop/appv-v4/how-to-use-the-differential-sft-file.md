---
title: Como usar o arquivo SFT diferencial
description: Como usar o arquivo SFT diferencial
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796915"
---
# <span data-ttu-id="363ab-103">Como usar o arquivo SFT diferencial</span><span class="sxs-lookup"><span data-stu-id="363ab-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="363ab-104">Ao sequenciar um aplicativo, o sequenciador do Microsoft Application Virtualization (App-V) cria arquivos SFT (. SFT) para armazenar todos os arquivos de conteúdo e informações de configuração do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="363ab-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="363ab-105">Na versão 4.5 do App-V, foi introduzido o arquivo SFT (. dsft) diferencial.</span><span class="sxs-lookup"><span data-stu-id="363ab-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="363ab-106">Depois de usar o sequenciador para criar uma atualização para um pacote existente, você pode optar por gerar esse arquivo para armazenar apenas as diferenças entre o pacote do aplicativo sequenciado original e a nova versão.</span><span class="sxs-lookup"><span data-stu-id="363ab-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="363ab-107">Portanto, é muito menor do que o arquivo SFT completo seria para a nova versão do aplicativo e reduz o impacto do envio de atualizações de pacote por meio de conexões de rede de baixa largura de banda.</span><span class="sxs-lookup"><span data-stu-id="363ab-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="363ab-108">No entanto, seu uso só tem suporte em determinadas situações restritas.</span><span class="sxs-lookup"><span data-stu-id="363ab-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="363ab-109">Esse recurso foi projetado para ser usado especificamente em que você está usando um sistema de distribuição de software eletrônico (ESD) para gerenciar um grupo de usuários com um servidor de arquivos local por meio de uma conexão de baixa largura de banda e não está usando servidores de streaming do App-V.</span><span class="sxs-lookup"><span data-stu-id="363ab-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="363ab-110">Você não precisará usar o arquivo SFT diferencial se estiver usando o Manager2007 de configuração para gerenciar os usuários, pois o Configuration Manager tem suporte para implantações de baixa largura de banda já incorporadas.</span><span class="sxs-lookup"><span data-stu-id="363ab-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="363ab-111">Ele também não é necessário se você estiver usando os servidores de gerenciamento ou de streaming do Application Virtualization (App-V) com atualização ativa, pois o cliente recuperará somente as diferenças entre as versões de pacote antigo e novo.</span><span class="sxs-lookup"><span data-stu-id="363ab-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="363ab-112">O procedimento a seguir mostra como usar o mkdiffpkg.exe que está incluído na instalação do sequenciador para criar o arquivo SFT diferencial, após concluir a atualização do pacote de aplicativo virtual e implantar o arquivo SFT diferencial.</span><span class="sxs-lookup"><span data-stu-id="363ab-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="363ab-113">Concluir esse procedimento ajuda a garantir que, se o pacote for descarregado de algum computador cliente, na próxima vez que o usuário tentar executar o aplicativo, o cliente retornará para a URL de substituição, que é definida para transmitir o pacote completo v2. sft do compartilhamento de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="363ab-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="363ab-114">Isso evitará qualquer falha do usuário quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="363ab-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="363ab-115">Se o cliente inteiro for corrompido ou for desinstalado, é recomendável que o sistema ESD seja configurado para implantar a versão completa do pacote atualizado, v2. SFT, para o cliente.</span><span class="sxs-lookup"><span data-stu-id="363ab-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="363ab-116">Para obter mais informações sobre como atualizar um pacote, consulte "como atualizar um aplicativo virtual existente" no guia de operações do App-V 4.5 em</span><span class="sxs-lookup"><span data-stu-id="363ab-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="363ab-117">**Observação**  Como pré-requisito, todos os computadores de usuário destinados ao ESD devem ter o arquivo v1. sft totalmente carregado em seu cache local, e o fluxo de arquivos deve estar habilitado em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="363ab-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="363ab-118">Para usar o arquivo SFT Diferencial</span><span class="sxs-lookup"><span data-stu-id="363ab-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="363ab-119">Faça logon no computador do sequenciador usando uma conta com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="363ab-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="363ab-120">Abra o pacote original (v1) para atualização no sequenciador e, em seguida, atualize o pacote para a nova versão (v2) e salve-o como um novo v2. SFT.</span><span class="sxs-lookup"><span data-stu-id="363ab-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="363ab-121">Abra uma janela de comando na pasta de instalação do sequenciador do App-V 4.5 e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="363ab-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="363ab-122">Usando o sistema ESD ou outro processo de cópia de arquivo, copie o arquivo de conteúdo do pacote v2 completo, v2. SFT, para um compartilhamento de arquivos local acessível para os computadores dos usuários em uma conexão de rede bem conectada.</span><span class="sxs-lookup"><span data-stu-id="363ab-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="363ab-123">Usando o sistema ESD, coloque uma cópia do arquivo SFT diferencial, v2. dsft, em cada computador de usuário.</span><span class="sxs-lookup"><span data-stu-id="363ab-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="363ab-124">Para importar o arquivo V2. dsft, execute o seguinte comando SFTMIME em cada computador do usuário:</span><span class="sxs-lookup"><span data-stu-id="363ab-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="363ab-125">Execute o seguinte comando SFTMIME em cada computador do usuário para definir a anulação da URL para apontar para o arquivo V2. sft:</span><span class="sxs-lookup"><span data-stu-id="363ab-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="363ab-126">Observação</span><span class="sxs-lookup"><span data-stu-id="363ab-126">Note</span></span>**  
-   <span data-ttu-id="363ab-127">Arquivos SFT diferenciais devem ser aplicados a clientes na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="363ab-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="363ab-128">Por exemplo, v2. dsft deve ser aplicado a um aplicativo v1 antes de v3. dsft ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="363ab-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="363ab-129">A funcionalidade **gerar pacote do Microsoft Windows Installer (MSI)** no sequenciador não pode ser usada com o arquivo SFT diferencial.</span><span class="sxs-lookup"><span data-stu-id="363ab-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="363ab-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="363ab-130">Related topics</span></span>


[<span data-ttu-id="363ab-131">Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="363ab-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





