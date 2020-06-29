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
# Lista de verificação pré-instalação do App-V


A lista de verificação a seguir destina-se a fornecer uma lista de alto nível de itens a serem considerados e descreve as etapas que devem ser tomadas antes de instalar os servidores do Microsoft Application Virtualization (App-V).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Referência</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Assegure-se de que seu ambiente computacional atenda às configurações compatíveis necessárias para o App-V.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Requisitos para implantação do Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar grupos e contas necessárias do Active Directory.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Configurando grupos de pré-requisitos no Active Directory para o App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Defina as configurações dos serviços de informações da Internet (IIS) no servidor que está executando o IIS.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Como configurar o Windows Server 2008 paro App-V Management Servers</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o servidor que está executando o IIS para ser confiável para delegação.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isso é necessário apenas se você estiver instalando o servidor de gerenciamento do App-V usando uma arquitetura de sistema distribuído, isto é, se você instalar o console de gerenciamento do App-V, o serviço de gerenciamento da Web e o banco de dados em computadores diferentes.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">Como configurar o servidor para ser confiável para delegação</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale o Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Instale o SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Listas de verificação de atualização e implantação do Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Lista de verificação para instalação do App-V](app-v-installation-checklist.md)









