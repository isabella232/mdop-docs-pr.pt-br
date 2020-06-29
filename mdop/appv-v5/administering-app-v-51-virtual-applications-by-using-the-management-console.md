---
title: Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento
description: Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796606"
---
# Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento


Use o servidor de gerenciamento do Microsoft Application Virtualization (App-V) 5,1 para gerenciar pacotes, grupos de conexão e acesso a pacotes em seu ambiente. O servidor publica os ícones de aplicativo, atalhos e associações de tipo de arquivo para computadores autorizados que executam o cliente App-V 5,1. Um ou mais servidores de gerenciamento geralmente compartilham um repositório de dados comum para informações de configuração e pacote.

O servidor de gerenciamento usa os grupos dos serviços de domínio Active Directory (AD DS) para gerenciar a autorização do usuário e tem o SQL Server instalado para gerenciar o banco de dados e o repositório de dados.

Como os servidores de gerenciamento transmitem aplicativos para usuários finais sob demanda, esses servidores são adequados para configurações de sistema que têm LANs confiáveis e de alta largura de banda. O servidor de gerenciamento consiste nos seguintes componentes:

-   Servidor de gerenciamento – Use o servidor de gerenciamento para gerenciar pacotes e grupos de conexão.

-   Publishing Server – use o Publishing Server para implantar pacotes em computadores que executam o cliente App-V 5,1.

-   Banco de dados de gerenciamento – Use o banco de dados de gerenciamento para gerenciar o acesso ao pacote e publicar a sincronização do servidor com o servidor de gerenciamento.

## Tarefas do console de gerenciamento


As tarefas mais comuns que você pode executar com o console de gerenciamento do App-V 5,1 são:

-   [Como conectar-se ao Console de Gerenciamento](how-to-connect-to-the-management-console-51.md)

-   [Como adicionar ou atualizar pacotes usando o Console de Gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [Como configurar o acesso a pacotes usando o Console de Gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [Como publicar um pacote usando o Console de Gerenciamento](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [Como excluir um pacote no Console de Gerenciamento](how-to-delete-a-package-in-the-management-console-51.md)

-   [Como adicionar ou remover um administrador usando o Console de Gerenciamento](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [Como transferir configurações e acesso para outra versão de um pacote usando o Console de Gerenciamento](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [Como exibir e configurar aplicativos e extensões de aplicativos virtuais padrão usando o Console de Gerenciamento](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Os principais elementos do console de gerenciamento do App-V 5,1 são:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Guia Console de gerenciamento</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Guia pacotes</p></td>
<td align="left"><p>Use a <strong> </strong> guia pacotes para adicionar ou atualizar pacotes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia grupos de conexão</p></td>
<td align="left"><p>Use a <strong> guia grupos de conexão </strong> para gerenciar grupos de conexão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Guia servidores</p></td>
<td align="left"><p>Use a <strong> </strong> guia servidores para registrar um novo servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia administradores</p></td>
<td align="left"><p>Use a <strong> </strong> guia administradores para registrar, adicionar ou remover administradores em seu ambiente do App-V 5,1.</p></td>
</tr>
</tbody>
</table>

 

**Importante**  O JavaScript deve estar ativado no navegador que abre o console de gerenciamento da Web.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Outros recursos para esta implantação do App-V 5,1


-   [Guia do administrador do Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





