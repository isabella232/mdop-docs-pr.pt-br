---
title: Configuração do IIS para streaming seguro
description: Configuração do IIS para streaming seguro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798014"
---
# <span data-ttu-id="00a09-103">Configuração do IIS para streaming seguro</span><span class="sxs-lookup"><span data-stu-id="00a09-103">Configuring IIS for Secure Streaming</span></span>


<span data-ttu-id="00a09-104">Com o lançamento do Microsoft Application Virtualization (App-V) versão 4,5, você pode usar HTTP e HTTPS como protocolos para transmitir pacotes de aplicativos para os clientes do App-V.</span><span class="sxs-lookup"><span data-stu-id="00a09-104">With the release of Microsoft Application Virtualization (App-V) version 4.5, you can use HTTP and HTTPS as protocols for streaming application packages to the App-V clients.</span></span> <span data-ttu-id="00a09-105">Essa opção permite que as organizações aproveitem a escalabilidade adicional que o IIS geralmente oferece.</span><span class="sxs-lookup"><span data-stu-id="00a09-105">This option enables organizations to leverage the additional scalability that IIS typically offers.</span></span> <span data-ttu-id="00a09-106">Ao usar o IIS como um servidor de streaming, você pode ajudar a proteger a comunicação entre o cliente e o servidor usando HTTPS em vez de HTTP.</span><span class="sxs-lookup"><span data-stu-id="00a09-106">When you use IIS as a streaming server, you can help secure the communications between the client and server by using HTTPS instead of HTTP.</span></span>

<span data-ttu-id="00a09-107">**Observação**  Se quiser transmitir aplicativos de um servidor de arquivos, você deve melhorar a segurança das comunicações com os pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="00a09-107">**Note** If you want to stream applications from a file server, you should enhance the security of the communications to the application packages.</span></span> <span data-ttu-id="00a09-108">Isso pode ser conseguido com o IPsec.</span><span class="sxs-lookup"><span data-stu-id="00a09-108">This can be achieved using IPsec.</span></span> <span data-ttu-id="00a09-109">Para obter mais informações, consulte os seguintes tópicos na biblioteca do TechNet:</span><span class="sxs-lookup"><span data-stu-id="00a09-109">For more information see the following topics in the TechNet Library:</span></span>

-   <span data-ttu-id="00a09-110">Para Windows Server2003,</span><span class="sxs-lookup"><span data-stu-id="00a09-110">For Windows Server2003,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133226>

-   <span data-ttu-id="00a09-111">Para o Windows Server 2008,</span><span class="sxs-lookup"><span data-stu-id="00a09-111">For Windows Server 2008,</span></span> <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## <span data-ttu-id="00a09-112">Tipos de MIME</span><span class="sxs-lookup"><span data-stu-id="00a09-112">MIME Types</span></span>


<span data-ttu-id="00a09-113">Quando você usa o IIS para transmitir aplicativos virtuais com HTTP ou HTTPS, para dar suporte ao App-V, os seguintes tipos de MIME devem ser adicionados ao servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="00a09-113">When you use IIS to stream virtual applications with HTTP or HTTPS, to support App-V, the following MIME types must be added to the IIS server:</span></span>

-   <span data-ttu-id="00a09-114">. OSD = TXT</span><span class="sxs-lookup"><span data-stu-id="00a09-114">.OSD=TXT</span></span>

-   <span data-ttu-id="00a09-115">. SFT = binário</span><span class="sxs-lookup"><span data-stu-id="00a09-115">.SFT=Binary</span></span>

<span data-ttu-id="00a09-116">Use os seguintes artigos da KB como orientação para adicionar tipos de MIME:</span><span class="sxs-lookup"><span data-stu-id="00a09-116">Use the following KB articles as guidance for adding MIME types:</span></span>

<span data-ttu-id="00a09-117">IIS 6,0:</span><span class="sxs-lookup"><span data-stu-id="00a09-117">IIS 6.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151973>

<span data-ttu-id="00a09-118">IIS 7,0:</span><span class="sxs-lookup"><span data-stu-id="00a09-118">IIS 7.0:</span></span> <https://go.microsoft.com/fwlink/?LinkId=151977>

## <span data-ttu-id="00a09-119">Autenticação Kerberos</span><span class="sxs-lookup"><span data-stu-id="00a09-119">Kerberos Authentication</span></span>


<span data-ttu-id="00a09-120">Ao usar a autenticação HTTP ou HTTPS e Kerberos para transmitir arquivos ICO, OSD ou SFT, você está aprimorando a segurança do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="00a09-120">When you use HTTP or HTTPS and Kerberos authentication to stream ICO, OSD, or SFT files, you are enhancing the security of your environment.</span></span> <span data-ttu-id="00a09-121">No entanto, para que o IIS ofereça suporte à autenticação Kerberos, você deve configurar um SPN (nome da entidade de serviço) adequado.</span><span class="sxs-lookup"><span data-stu-id="00a09-121">However, for IIS to support Kerberos authentication, you must configure a proper Service Principal Name (SPN).</span></span> <span data-ttu-id="00a09-122">A `setspn.exe` ferramenta está disponível para Windows Server2003 nas ferramentas de suporte no CD de instalação e está integrada ao Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="00a09-122">The `setspn.exe` tool is available for Windows Server2003 from the Support Tools on the installation CD and is built-in to Windows Server2008.</span></span>

<span data-ttu-id="00a09-123">Para criar um SPN, execute `setspn.exe` a partir de um prompt de comando enquanto estiver conectado como membro de administradores de domínio, por exemplo, `setspn.exe –A HTTP/FQDN of Server ServerName` .</span><span class="sxs-lookup"><span data-stu-id="00a09-123">To create an SPN, run `setspn.exe` from a command prompt while logged in as a member of Domain Administrators—for example, `setspn.exe –A HTTP/FQDN of Server ServerName`.</span></span>

## <span data-ttu-id="00a09-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00a09-124">Related topics</span></span>


[<span data-ttu-id="00a09-125">Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação</span><span class="sxs-lookup"><span data-stu-id="00a09-125">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





