---
title: Lista de verificação pós-instalação do App-V
description: Lista de verificação pós-instalação do App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797598"
---
# <span data-ttu-id="8038a-103">Lista de verificação pós-instalação do App-V</span><span class="sxs-lookup"><span data-stu-id="8038a-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="8038a-104">A lista de verificação a seguir fornece uma lista de alto nível de itens que devem ser considerados e descreve as etapas que devem ser tomadas após a conclusão da instalação do servidor de gerenciamento do Microsoft Application Virtualization (App-V), do App-V Streaming Server e do cliente da área de trabalho do App-V.</span><span class="sxs-lookup"><span data-stu-id="8038a-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8038a-105">Etapa</span><span class="sxs-lookup"><span data-stu-id="8038a-105">Step</span></span></th>
<th align="left"><span data-ttu-id="8038a-106">Referência</span><span class="sxs-lookup"><span data-stu-id="8038a-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8038a-107">Crie exceções de firewall para o servidor de gerenciamento do App-V ou serviços do servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="8038a-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="8038a-108">Configurando o firewall para os App-V Servers</span><span class="sxs-lookup"><span data-stu-id="8038a-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8038a-109">Verifique se o sistema App-V está funcionando corretamente publicando, transmitindo e testando o aplicativo padrão.</span><span class="sxs-lookup"><span data-stu-id="8038a-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="8038a-110">Como instalar e configurar o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="8038a-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8038a-111">Configure o cliente App-V para usar o servidor de streaming App-V ou outro servidor para streaming por meio das <strong> </strong> configurações APPLICATIONSOURCEROOT, <strong> IconSourceRoot </strong> e <strong> OSDSourceRoot </strong> .</span><span class="sxs-lookup"><span data-stu-id="8038a-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="8038a-112">Como configurar o cliente para recuperação de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8038a-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8038a-113">Saiba como usar a versão do arquivo. msi dos pacotes de aplicativos sequenciados para implantação offline.</span><span class="sxs-lookup"><span data-stu-id="8038a-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="8038a-114">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="8038a-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8038a-115">Adicionais Configure o espelhamento de banco de dados do SQL Server para o banco de dados do App-V.</span><span class="sxs-lookup"><span data-stu-id="8038a-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="8038a-116">Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V</span><span class="sxs-lookup"><span data-stu-id="8038a-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8038a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8038a-117">Related topics</span></span>


[<span data-ttu-id="8038a-118">Listas de verificação de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8038a-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





