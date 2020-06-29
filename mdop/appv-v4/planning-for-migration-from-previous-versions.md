---
title: Planejamento da migração de versões anteriores
description: Planejamento da migração de versões anteriores
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796823"
---
# Planejamento da migração de versões anteriores


Antes de tentar atualizar para o Microsoft Application Virtualization 4.5 ou versões posteriores, qualquer versão anterior a 4.1 deve ser atualizada para a versão 4.1. Você deve planejar a atualização dos seus clientes primeiro e, em seguida, atualizar os componentes do servidor. Os clientes que foram atualizados para o 4.5 continuarão a funcionar com os servidores do Application Virtualization que ainda não foram atualizados. Não há suporte para versões anteriores do cliente em servidores que foram atualizados para 4.5. Para obter mais informações sobre a atualização dos componentes do sistema, consulte [Considerações sobre implantação e atualização do Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md).

Para ajudar a garantir uma migração bem-sucedida, os componentes do sistema do Application Virtualization devem ser atualizados na seguinte ordem:

1.  **Clientes de virtualização de aplicativos Microsoft.** Para obter instruções passo a passo de atualização, consulte [como atualizar o cliente do Application Virtualization](how-to-upgrade-the-application-virtualization-client.md).

2.  **Servidores e banco de dados de virtualização de aplicativos Microsoft.** Para obter instruções passo a passo de atualização, consulte [como atualizar os servidores e componentes do sistema](how-to-upgrade-the-servers-and-system-components.md).

    **Observação**  Se você tiver mais de um servidor que compartilha o acesso ao banco de dados do Application Virtualization, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado. Você deve seguir as práticas comerciais normais para a atualização do banco de dados, mas é altamente recomendável que você teste a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste. Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados. Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar os outros servidores.

     

3.  **Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization.** Esta etapa se aplica apenas se o serviço Web de gerenciamento estiver em um servidor separado, o que exigirá que você execute o programa de instalação do servidor nesse servidor separado para atualizar o serviço Web. Caso contrário, a etapa anterior de atualização do servidor atualizará automaticamente o serviço Web de gerenciamento.

4.  **Console de gerenciamento do Microsoft Application Virtualization.** Esta etapa se aplica apenas se o console de gerenciamento estiver em um computador separado, o que exigirá que você execute o programa de instalação do servidor nesse computador separado para atualizar o console. Caso contrário, a etapa anterior de atualização do servidor atualizará o console de gerenciamento.

5.  **Microsoft Application Virtualization Sequencer.** Para obter instruções passo a passo, consulte [como instalar o Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md). Qualquer pacote de aplicativos virtual sequenciado na versão 4.2 não precisará ser novamente sequenciado para uso com a versão 4.5. No entanto, você deve considerar a atualização dos pacotes virtuais para o formato do Microsoft Application Virtualization 4.5 se quiser aplicar ACLs (listas de controle de acesso) padrão ou gerar um arquivo do Windows Installer. Isso é um processo simples e requer que o pacote de aplicativo virtual existente seja aberto e salvo com o 4,5 Sequencer. Isso pode ser automatizado usando a interface de linha de comando do sequenciador do Application Virtualization.

## <a href="" id="app-v-4-6-client-package-support-"></a>Suporte ao pacote do cliente do App-V 4.6


Você pode implantar pacotes criados em versões anteriores do App-V para os clientes do App-V 4.6. No entanto, você deve modificar o arquivo **. OSD** associado para que ele inclua o sistema operacional apropriado e as informações sobre a arquitetura do chip. Use os valores a seguir.

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor do sistema operacional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR do sistema operacional = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR do sistema operacional = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR do sistema operacional = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>

 

Para executar um pacote de 32 bits recém-criado, você deve sequenciar o aplicativo em um computador executando um sistema operacional de 32 bits com o sequenciador App-V 4.6 instalado. Depois de sequenciar o aplicativo, no console do sequenciador, selecione a guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.

**Importante**  Aplicativos sequenciados em um computador executando um sistema operacional de 64 bits devem ser implantados em computadores que executam um sistema operacional de 64 bits. Novos pacotes de 32 bits criados usando o App-V 4.6 Sequencer não serão executados em computadores que executam o cliente App-V 4,5.

 

Para executar novos pacotes de 64 bits no cliente App-V 4.6, você deve sequenciar o aplicativo em um computador executando o sequenciador do App-V 4.6 e que esteja executando um sistema operacional de 64 bits. Depois de sequenciar o aplicativo, no console do sequenciador, selecione a guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.

A tabela a seguir lista quais versões do cliente executarão pacotes criados usando as várias versões do sequenciador.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,2</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,5</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 de 32 bits</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 de 64 bits</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 SP1 do 32-bit App-V</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 SP1 do 64-bit App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>cliente do 4,2</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="even">
<td align="left"><p>¹ Client 4,5</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cliente do 4,6 (32 bits)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="even">
<td align="left"><p>cliente do 4,6 (64 bits)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente do 4,6 SP1</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente do 4,6 SP1 (64 bits)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
</tbody>
</table>

 

¹ aplica-se a todas as versões do cliente App-V 4.5, incluindo App-V 4.5, App-V 4.5 CU1 e App-V 4.5 SP1.

## Considerações adicionais sobre a migração


Um dos recursos do sequenciador App-V 4.5 é a capacidade de criar arquivos do Windows Installer (. msi) como pontos de controle para interoperabilidade do pacote de aplicativos virtual com sistemas ESD (distribuição de software eletrônico), como o Microsoft Endpoint Configuration Manager. Os arquivos anteriores do Windows Installer criados com a ferramenta. msi para a virtualização de aplicativos que foram instalados em um cliente App-V 4.1 ou 4.2 que, em seguida, foi atualizado para o 4.5 continuam funcionando, embora não possam ser instalados no cliente 4.5. No entanto, eles não podem ser removidos ou atualizados, a menos que eles sejam atualizados no sequenciador de 4,5. O pacote de aplicativo virtual anterior ao 4,5 precisaria ser aberto no sequenciador de 4,5 e salvo como um arquivo do Windows Installer.

**Observação**  Se o cliente App-V 4.2 já tiver sido atualizado para o 4.5, é possível usar o script como solução alternativa para preservar os pacotes 4.2 em clientes 4.5 e permitir que eles sejam gerenciados. Esse script deve copiar dois arquivos, msvcp71.dll e msvcr71.dll, para a pasta de instalação do App-V e definir os seguintes valores de chave do registro na chave do registro \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

"ClientVersion" = "4.2.1.20"

"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (um local gravável globalmente)

 

Os arquivos do Windows Installer gerados pela App-V 4,5 Sequencer exibem a mensagem de erro "Este pacote requer o cliente do Microsoft Application Virtualization 4,5 ou posterior" quando você tenta executá-los em um cliente do App-V 4,6. Abra o pacote antigo com o sequenciador do App-V 4,5 SP1 ou o sequenciador do App-V 4,6 e gere um novo. msi para o pacote.

Quaisquer relatórios do 4.2 que foram criados e salvos serão substituídos quando o servidor for atualizado para o 4.5. Se precisar manter esses relatórios, você deve salvar uma cópia de backup do arquivo SftMMC. msc localizado na pasta do console de gerenciamento do SoftGrid no servidor e usar essa cópia para substituir o novo SftMMC. msc que é instalado durante a atualização.

Para obter informações adicionais sobre a atualização de versões anteriores, consulte [atualização para perguntas frequentes do Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## Tópicos relacionados


[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

 

 





