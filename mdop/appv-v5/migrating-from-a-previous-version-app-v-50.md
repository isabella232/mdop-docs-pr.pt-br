---
title: Migração de uma versão anterior
description: Migração de uma versão anterior
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796279"
---
# Migração de uma versão anterior


Com o App-V 5,0, você pode migrar sua infraestrutura existente do App-V 4,6 para a infraestrutura mais flexível, integrada e mais fácil de gerenciar do App-V 5,0.

Considere as seguintes seções quando planejar a estratégia de migração:

**Observação**  Para obter mais informações sobre as diferenças entre o App-V 4,6 e o App-V 5,0, consulte a **seção diferenças entre o app-v 4,6 e o app-v 5,0** de [sobre o app-v 5,0](about-app-v-50.md).

 

## Convertendo pacotes criados usando uma versão anterior do App-V


Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões anteriores do App-V. O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.

**Importante**  Depois de converter um pacote existente, você deve testar o pacote antes de implantar o pacote para garantir que o processo de conversão foi bem-sucedido.

 

**O que saber antes de converter pacotes existentes**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problema</th>
<th align="left">Solução alternativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Os scripts de pacote não são convertidos.</p></td>
<td align="left"><p>Testar o pacote convertido. Se necessário, converta o script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>As substituições de configuração do registro do pacote não são convertidas.</p></td>
<td align="left"><p>Testar o pacote convertido. Se necessário, adicione novamente as substituições do registro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Os pacotes virtuais que usam o DSC não são vinculados após a conversão.</p></td>
<td align="left"><p>Vincule os pacotes usando grupos de conexão. Consulte <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Gerenciando grupos de conexão </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conflitos de variáveis de ambiente são detectados durante a conversão.</p></td>
<td align="left"><p>Resolva os conflitos no <strong> arquivo. OSD associado </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caminhos de código fixo são detectados durante a conversão.</p></td>
<td align="left"><p>Os caminhos embutidos em código são difíceis de serem convertidos corretamente. O conversor de pacote detecta e retorna pacotes com arquivos que contêm caminhos embutidos em código. Exiba o arquivo com o caminho embutido e determine se o pacote requer o arquivo. Em caso afirmativo, é recomendável resequenciar o pacote.</p></td>
</tr>
</tbody>
</table>

 

Ao converter um pacote, verifique se há arquivos ou atalhos com falha. Localize o item no pacote App-V 4,6. Pode ser um caminho embutido. Converter o caminho.

**Observação**  É recomendável que você use o sequenciador do App-V 5,0 para converter aplicativos críticos ou aplicativos que precisam tirar proveito dos recursos. Veja [como sequenciar um novo aplicativo com o App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).

Se um pacote convertido não abrir após você convertê-lo, também é recomendável que você reaplique a sequência do aplicativo usando o sequenciador do App-V 5,0.

 

[Como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## Migrando clientes


A tabela a seguir exibe o método recomendado para a atualização de clientes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualizar seu ambiente para o App-V 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerações de atualização e implantação do Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instale o cliente do App-V 5,0 com coexistência habilitada.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciar e distribuir pacotes do App-V 5,0. Conforme necessário, cancele a publicação de pacotes do App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">Como sequenciar um novo aplicativo com o App-V 5,0 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  Você deve estar executando o App-V 4.6 SP3 para usar o modo de coexistência. Além disso, quando você sequenciar um pacote, você deve definir a configuração de **autoridade de gerenciamento** , que está localizada na seção **configuração do usuário** .

 

## Migrando a infraestrutura completa do App-V 5,0 Server


Não há um método direto para atualizar para uma infraestrutura completa do App-V 5,0. Use as informações na seção a seguir para obter informações sobre como atualizar o servidor App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualize seu ambiente para o App-V 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerações de atualização e implantação do Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implante a versão do App-V 5,0 do cliente.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Como implantar o cliente App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale o App-V 5,0 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Como implantar o servidor do App-V 5,0 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrar pacotes existentes.</p></td>
<td align="left"><p>Veja a <strong> seção convertendo pacotes criados usando uma versão anterior do App-V </strong> deste artigo.</p></td>
</tr>
</tbody>
</table>

 

## Tarefas de migração adicionais


Você também pode executar tarefas de migração adicionais, como reconfiguração de pontos de extremidade, bem como abrir um pacote criado usando uma versão anterior em um computador que executa o cliente App-V 5,0. Os links a seguir fornecem mais informações sobre como executar essas tarefas.

[Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para um usuário específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Outros recursos para executar tarefas de migração do App-V


[Operações para o App-V 5.0](operations-for-app-v-50.md)

[Um procedimento simplificado de atualização do servidor de gerenciamento do Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





