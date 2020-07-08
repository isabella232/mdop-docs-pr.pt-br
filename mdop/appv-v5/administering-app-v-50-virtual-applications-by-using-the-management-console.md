---
title: Administrar aplicativos virtuais do App-V 5.0 usando o Console de Gerenciamento
description: Administrar aplicativos virtuais do App-V 5.0 usando o Console de Gerenciamento
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796607"
---
# Administrar aplicativos virtuais do App-V 5.0 usando o Console de Gerenciamento


Use o servidor de gerenciamento do Microsoft Application Virtualization (App-V) 5,0 para gerenciar pacotes, grupos de conexão e acesso a pacotes em seu ambiente. O servidor publica os ícones de aplicativo, atalhos e associações de tipo de arquivo para computadores autorizados que executam o cliente App-V 5,0. Um ou mais servidores de gerenciamento geralmente compartilham um repositório de dados comum para informações de configuração e pacote.

O servidor de gerenciamento usa os grupos dos serviços de domínio Active Directory (AD DS) para gerenciar a autorização do usuário e tem o SQL Server instalado para gerenciar o banco de dados e o repositório de dados.

Como os servidores de gerenciamento transmitem aplicativos para usuários finais sob demanda, esses servidores são adequados para configurações de sistema que têm LANs confiáveis e de alta largura de banda. O servidor de gerenciamento consiste nos seguintes componentes:

-   Servidor de gerenciamento – Use o servidor de gerenciamento para gerenciar pacotes e grupos de conexão.

-   Publishing Server – use o Publishing Server para implantar pacotes em computadores que executam o cliente App-V 5,0.

-   Banco de dados de gerenciamento – Use o banco de dados de gerenciamento para gerenciar o acesso ao pacote e publicar a sincronização do servidor com o servidor de gerenciamento.

## Tarefas do console de gerenciamento


As tarefas mais comuns que você pode executar com o console de gerenciamento do App-V 5,0 são:

-   [Como conectar-se ao Console de Gerenciamento](how-to-connect-to-the-management-console-beta.md)

-   [Como adicionar ou atualizar pacotes usando o Console de Gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [Como configurar o acesso a pacotes usando o Console de Gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [Como publicar um pacote usando o Console de Gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [Como excluir um pacote no Console de Gerenciamento](how-to-delete-a-package-in-the-management-console-beta.md)

-   [Como adicionar ou remover um administrador usando o Console de Gerenciamento](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [Como transferir configurações e acesso para outra versão de um pacote usando o Console de Gerenciamento](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [Configurar aplicativos e extensões de aplicativo virtual padrão no console de gerenciamento](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

Os principais elementos do console de gerenciamento do App-V 5,0 são:

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
<td align="left"><p>Visão geral</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>Sequenciador do App-V </strong> - Selecione esta opção para analisar informações gerais sobre como usar o sequenciador do App-v 5,0.</p></li>
<li><p><strong>Biblioteca de pacotes </strong> de aplicativos – Selecione esta opção para abrir a <strong> </strong> página pacotes do console de gerenciamento. Use esta página para revisar os pacotes que foram adicionados ao servidor. Você também pode gerenciar os grupos de conexão, bem como adicionar ou atualizar pacotes.</p></li>
<li><p><strong>SERVIDORES </strong> – Selecione esta opção para abrir a <strong> </strong> página servidores do console de gerenciamento. Use esta página para examinar a lista de servidores que foram registrados com sua infraestrutura do App-V 5,0.</p></li>
<li><p><strong>CLIENTES </strong> – Selecione esta opção para examinar informações gerais sobre clientes do App-V 5,0.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Guia pacotes</p></td>
<td align="left"><p>Use a <strong> </strong> guia pacotes para adicionar ou atualizar pacotes. Você também pode gerenciar grupos de conexão clicando em <strong> grupos de conexão </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Guia servidores</p></td>
<td align="left"><p>Use a <strong> </strong> guia servidores para registrar um novo servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia administradores</p></td>
<td align="left"><p>Use a <strong> </strong> guia administradores para registrar, adicionar ou remover administradores em seu ambiente do App-V 5,0.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>Outros recursos para esta implantação do App-V 5,0


-   [Guia do administrador do Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





