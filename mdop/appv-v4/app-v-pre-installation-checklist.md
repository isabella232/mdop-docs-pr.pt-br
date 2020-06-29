---
title: Lista de verificação pré-instalação do App-V
description: Lista de verificação pré-instalação do App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797595"
---
# <span data-ttu-id="c4f71-103">Lista de verificação pré-instalação do App-V</span><span class="sxs-lookup"><span data-stu-id="c4f71-103">App-V Pre-Installation Checklist</span></span>


<span data-ttu-id="c4f71-104">A lista de verificação a seguir destina-se a fornecer uma lista de alto nível de itens a serem considerados e descreve as etapas que devem ser tomadas antes de instalar os servidores do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c4f71-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take before you install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4f71-105">Etapa</span><span class="sxs-lookup"><span data-stu-id="c4f71-105">Step</span></span></th>
<th align="left"><span data-ttu-id="c4f71-106">Referência</span><span class="sxs-lookup"><span data-stu-id="c4f71-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4f71-107">Assegure-se de que seu ambiente computacional atenda às configurações compatíveis necessárias para o App-V.</span><span class="sxs-lookup"><span data-stu-id="c4f71-107">Ensure your computing environment meets the supported configurations required for App-V.</span></span></p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)"><span data-ttu-id="c4f71-108">Requisitos para implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c4f71-108">Application Virtualization Deployment Requirements</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4f71-109">Configurar grupos e contas necessárias do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c4f71-109">Configure the necessary Active Directory groups and accounts.</span></span></p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)"><span data-ttu-id="c4f71-110">Configurando grupos de pré-requisitos no Active Directory para o App-V</span><span class="sxs-lookup"><span data-stu-id="c4f71-110">Configuring Prerequisite Groups in Active Directory for App-V</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4f71-111">Defina as configurações dos serviços de informações da Internet (IIS) no servidor que está executando o IIS.</span><span class="sxs-lookup"><span data-stu-id="c4f71-111">Configure the Internet Information Services (IIS) settings on the server that is running IIS.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)"><span data-ttu-id="c4f71-112">Como configurar o Windows Server 2008 paro App-V Management Servers</span><span class="sxs-lookup"><span data-stu-id="c4f71-112">How to Configure Windows Server 2008 for App-V Management Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4f71-113">Configurar o servidor que está executando o IIS para ser confiável para delegação.</span><span class="sxs-lookup"><span data-stu-id="c4f71-113">Configure the server that is running IIS to be trusted for delegation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c4f71-114">Observação</span><span class="sxs-lookup"><span data-stu-id="c4f71-114">Note</span></span></strong><br/><p><span data-ttu-id="c4f71-115">Isso é necessário apenas se você estiver instalando o servidor de gerenciamento do App-V usando uma arquitetura de sistema distribuído, isto é, se você instalar o console de gerenciamento do App-V, o serviço de gerenciamento da Web e o banco de dados em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="c4f71-115">This is required only if you are installing the App-V Management Server by using a distributed system architecture, that is, if you install the App-V Management Console, the Management Web Service, and the database on different computers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)"><span data-ttu-id="c4f71-116">Como configurar o servidor para ser confiável para delegação</span><span class="sxs-lookup"><span data-stu-id="c4f71-116">How to Configure the Server to be Trusted for Delegation</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4f71-117">Instale o Microsoft SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c4f71-117">Install Microsoft SQL Server 2008.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)"><span data-ttu-id="c4f71-118">Instale o SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</span><span class="sxs-lookup"><span data-stu-id="c4f71-118">Install SQL Server 2008</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924">https://go.microsoft.com/fwlink/?LinkId=181924</a>).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c4f71-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4f71-119">Related topics</span></span>


[<span data-ttu-id="c4f71-120">Listas de verificação de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c4f71-120">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="c4f71-121">Lista de verificação para instalação do App-V</span><span class="sxs-lookup"><span data-stu-id="c4f71-121">App-V Installation Checklist</span></span>](app-v-installation-checklist.md)









