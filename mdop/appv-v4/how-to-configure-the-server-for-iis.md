---
title: Como configurar o servidor para o IIS
description: Como configurar o servidor para o IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797186"
---
# <span data-ttu-id="e67ff-103">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="e67ff-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="e67ff-104">Antes que os aplicativos virtuais possam ser transmitidos para o cliente da área de trabalho do Application Virtualization e para o cliente para serviços de área de trabalho remota (antes serviços de terminal), os servidores IIS devem ser configurados.</span><span class="sxs-lookup"><span data-stu-id="e67ff-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="e67ff-105">Ao configurar os servidores, você está configurando o diretório de conteúdo em que os arquivos SFT são carregados e armazenados.</span><span class="sxs-lookup"><span data-stu-id="e67ff-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="e67ff-106">Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).</span><span class="sxs-lookup"><span data-stu-id="e67ff-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="e67ff-107">Para configurar o diretório de conteúdo no servidor IIS</span><span class="sxs-lookup"><span data-stu-id="e67ff-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="e67ff-108">No servidor que está executando o IIS, localize o diretório que você deseja usar como o diretório de conteúdo ou crie o diretório, caso ele não exista.</span><span class="sxs-lookup"><span data-stu-id="e67ff-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="e67ff-109">Configurar esse diretório como um compartilhamento de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="e67ff-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="e67ff-110">No servidor que está executando o IIS, abra o **Gerenciador do IIS**e, no site padrão, crie um diretório virtual que corresponda ao diretório de conteúdo que você criou no servidor.</span><span class="sxs-lookup"><span data-stu-id="e67ff-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="e67ff-111">Verifique se a opção **leitura** está marcada.</span><span class="sxs-lookup"><span data-stu-id="e67ff-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="e67ff-112">Dê ao diretório virtual recém-criado o **conteúdo**do alias.</span><span class="sxs-lookup"><span data-stu-id="e67ff-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="e67ff-113">Aceite todas as outras configurações padrão para este diretório virtual.</span><span class="sxs-lookup"><span data-stu-id="e67ff-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="e67ff-114">Configure as permissões do sistema de arquivos NTFS para o diretório de conteúdo e as pastas de pacote sob o diretório de conteúdo usando os grupos de segurança nos serviços de domínio do Active Directory que você definiu anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e67ff-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="e67ff-115">**Observação**  Se você estiver usando o IIS para publicar os arquivos ICO e OSD, será preciso configurar um tipo MIME para OSD = TXT; caso contrário, o IIS não servirá os arquivos ICO e OSD para clientes.</span><span class="sxs-lookup"><span data-stu-id="e67ff-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="e67ff-116">Se estiver usando o IIS para publicar pacotes (arquivos SFT), você deve configurar um tipo MIME para SFT = Binary; caso contrário, o IIS não servirá os arquivos SFT para clientes.</span><span class="sxs-lookup"><span data-stu-id="e67ff-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="e67ff-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e67ff-117">Related topics</span></span>


[<span data-ttu-id="e67ff-118">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="e67ff-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="e67ff-119">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="e67ff-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="e67ff-120">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="e67ff-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="e67ff-121">Como configurar os Application Virtualization Streaming Servers</span><span class="sxs-lookup"><span data-stu-id="e67ff-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="e67ff-122">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="e67ff-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





