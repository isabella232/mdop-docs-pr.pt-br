---
title: Configurando grupos de pré-requisitos no Active Directory para o App-V
description: Configurando grupos de pré-requisitos no Active Directory para o App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798010"
---
# Configurando grupos de pré-requisitos no Active Directory para o App-V


Antes de instalar o servidor de gerenciamento do Microsoft Application Virtualization (App-V), você deve criar os seguintes objetos no Active Directory. O App-V usa grupos do Active Directory para controlar o acesso a aplicativos e funções administrativas. Você usará esses grupos durante o processo de instalação do servidor e durante a publicação de aplicativos.

## Configurando grupos de pré-requisitos no Active Directory para virtualização de aplicativos


Esta tabela lista os grupos do Active Directory necessários para a instalação do App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Objeto</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unidade organizacional (UO)</p></td>
<td align="left"><p>Crie uma OU no Active Directory para os grupos específicos necessários para o App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo administrativo do App-V</p></td>
<td align="left"><p>Durante a instalação do servidor de gerenciamento do App-V, você deve selecionar um grupo do Active Directory para usá-lo como o grupo de administradores do App-V para controlar o acesso administrativo ao console de gerenciamento. Crie um grupo de segurança para administradores do App-V e adicione a esse grupo todos os usuários que precisam usar o console de gerenciamento. Você não pode criar esse grupo diretamente do instalador do App-V Management Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo usuários do App-V</p></td>
<td align="left"><p>O App-V requer que todas as contas de usuário que acessam as funções do App-V sejam um membro de uma política de provedor associada a um único grupo para acesso geral à plataforma. Usar um grupo existente; por exemplo, usuários do domínio, se todos os usuários tiverem acesso ao App-V ou criarem um novo grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupos de aplicativos</p></td>
<td align="left"><p>O App-V associa o direito de usar um aplicativo individual com um grupo do Active Directory. Crie um grupo do Active Directory para cada aplicativo e atribua usuários a esses grupos conforme necessário para controlar o acesso do usuário aos aplicativos.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Requisitos para implantação do Application Virtualization](application-virtualization-deployment-requirements.md)

[Como configurar o Windows Server 2008 paro App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





