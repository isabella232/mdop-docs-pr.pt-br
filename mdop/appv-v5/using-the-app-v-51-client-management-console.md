---
title: Como usar o Console de Gerenciamento de Clientes do App-V 5.1
description: Como usar o Console de Gerenciamento de Clientes do App-V 5.1
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796204"
---
# Como usar o Console de Gerenciamento de Clientes do App-V 5.1


Este tópico fornece informações sobre como você pode configurar e gerenciar o cliente do Microsoft Application Virtualization (App-V) 5,1.

## Modificar a configuração do cliente do App-V 5,1


O cliente App-V 5,1 tem configurações associadas que podem ser configuradas para determinar como o cliente será executado em seu ambiente. Você pode gerenciar essas configurações no computador que executa o cliente ou usando o PowerShell ou a política de grupo. Para obter mais informações sobre como modificar o cliente usando a configuração do PowerShell ou da política de grupo, consulte [como modificar a configuração do cliente usando o PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).

## <a href="" id="the-app-v-5-1-client-management-console-"></a>O console de gerenciamento do cliente do App-V 5,1


Você pode obter informações sobre o cliente App-V 5,1 ou executar tarefas específicas usando o console de gerenciamento do App-V 5,1 Client. Muitas das tarefas que você pode executar no console de gerenciamento de cliente também pode executar usando o PowerShell. Os cmdlets associados do PowerShell para cada ação também são exibidos na tabela a seguir. Para obter mais informações sobre como usar o PowerShell, consulte [administrando o App-V 5,1 usando o PowerShell](administering-app-v-51-by-using-powershell.md).

O console de gerenciamento de cliente contém as guias principais descritas a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tab</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visão geral</p></td>
<td align="left"><p>A <strong> guia Visão geral </strong> contém os seguintes elementos:</p>
<ul>
<li><p>Update – use o <strong> </strong> bloco Update para atualizar um aplicativo virtualizado ou receber um novo pacote virtualizado.</p>
<p>A <strong> última atualização </strong> exibe a versão atual do pacote virtualizado.</p></li>
<li><p>Baixar todos os aplicativos virtuais – use <strong> o </strong> bloco de download para baixar todos os pacotes provisionados para o usuário atual.</p>
<p>(Cmdlet associado do PowerShell: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>Trabalhar offline – Use este bloco para impedir todas as atualizações automáticas e manuais do aplicativo virtual.</p>
<p>(Cmdlet associado do PowerShell: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicativos virtuais</p></td>
<td align="left"><p>A <strong> guia aplicativos virtuais </strong> exibe todos os pacotes que foram publicados para o usuário. Você também pode clicar em um pacote específico e ver todos os aplicativos que fazem parte do pacote. Isso exibe informações sobre pacotes que estão sendo usados no momento e quanto de cada pacote foi baixado para o computador. Você também pode iniciar e parar downloads de pacotes. Além disso, você pode reparar o estado do usuário. Um reparo excluirá todos os dados do usuário associados a um pacote.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupos de conexão do aplicativo</p></td>
<td align="left"><p>A <strong> guia grupos de conexão de aplicativos </strong> exibe todos os grupos de conexão que estão disponíveis para o usuário atual. Clique em um grupo de conexão específico para ver todos os pacotes que fazem parte do grupo selecionado. Isso exibe informações sobre grupos de conexão que já estão em uso e quanto do conteúdo do grupo de conexão foram baixados para o computador. Além disso, você pode iniciar e parar downloads do grupo de conexão. Você pode usar esta seção para iniciar um reparo. Um reparo removerá todo o estado do usuário associado a um grupo de conexão.</p>
<p>(Cmdlets associados do PowerShell: Download- <strong> Mount-AppvClientConnectionGroup </strong> . Repair- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[Como acessar o Console de Gerenciamento do cliente](how-to-access-the-client-management-console51.md)

[Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





