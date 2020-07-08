---
title: Lista de verificação de upgrade do App-V
description: Lista de verificação de upgrade do App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797585"
---
# Lista de verificação de upgrade do App-V


Antes de tentar atualizar para versões do Microsoft Application Virtualization (App-V) 4,5 ou posterior, qualquer versão anterior ao App-V 4,1 deve ser atualizada para o App-V 4,1. Você deve planejar a atualização dos clientes primeiro e, em seguida, atualizar os componentes do servidor. Os clientes do App-V que foram atualizados para o App-V 4,5 continuam a funcionar com servidores App-V que ainda não foram atualizados. Não há suporte para versões anteriores do cliente em servidores que foram atualizados para o App-V 4,5.

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
<td align="left"><p>Atualize os clientes do App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">Como fazer upgrade do Application Virtualization Client</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Atualize o banco de dados e os servidores do App-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se você tiver mais de um servidor com acesso de compartilhamento ao banco de dados do App-V, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado. Você deve seguir as práticas comerciais regulares para a atualização do banco de dados, mas recomendamos testar a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste. Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados. Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar o software App-V nos outros servidores.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Como fazer upgrade dos componentes de servidores e do sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Atualize o serviço Web de gerenciamento do App-V.</p>
<p>Esta etapa se aplica apenas se o serviço Web de gerenciamento estiver em um servidor separado, o que exigirá que você execute o programa de instalação do servidor nesse servidor separado para atualizar o serviço Web de gerenciamento. Caso contrário, a etapa anterior de atualização do servidor atualizará automaticamente o serviço Web de gerenciamento.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Como fazer upgrade dos componentes de servidores e do sistema</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Atualize o console de gerenciamento do App-V.</p>
<p>Esta etapa se aplica apenas se o console de gerenciamento estiver em um computador separado, o que exigirá que você execute o programa de instalação do servidor nesse computador separado para atualizar o console. Caso contrário, a etapa anterior de atualização do servidor atualizará o console de gerenciamento.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Como fazer upgrade dos componentes de servidores e do sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Atualize o sequenciador do App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">Como fazer upgrade do Application Virtualization Sequencer</a></p></td>
</tr>
</tbody>
</table>



## Considerações de atualização adicionais


-   Qualquer pacote de aplicativos virtual sequenciado na versão 4,2 não terá que ser sequenciado novamente para uso com a versão 4,5. No entanto, você deve considerar a atualização dos pacotes virtuais para o formato 4,5 do Microsoft Application Virtualization se desejar aplicar ACLs (listas de controle de acesso) padrão ou gerar um arquivo do Windows Installer. Isso é um processo simples e requer que o pacote de aplicativo virtual existente seja aberto e salvo com o sequenciador do App-V 4,5. Isso pode ser automatizado usando a interface de linha de comando App-VSequencer. Para obter mais informações, consulte [como criar ou atualizar aplicativos virtuais usando o sequenciador App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

-   Um dos recursos do sequenciador 4,5 é a capacidade de criar arquivos do Windows Installer (. msi) como pontos de controle para interoperabilidade do pacote de aplicativos virtual com sistemas ESD (distribuição de software eletrônico), como o Microsoft Endpoint Configuration Manager. Os arquivos anteriores do Windows Installer criados com a ferramenta MSI para a virtualização de aplicativos que foram instalados em um cliente App-V 4,1 ou 4,2 que, em seguida, foi atualizado para o App-V 4,5 continuarão funcionando, embora não possam ser instalados no cliente App-V 4,5. No entanto, eles não podem ser removidos ou atualizados, a menos que eles sejam atualizados no sequenciador do App-V 4,5. O pacote App-V original anterior a 4,5 precisa ser aberto no sequenciador App-V 4,5 e salvo como um arquivo do Windows Installer.

    **Observação**  
    Se o cliente App-V 4,2 já tiver sido atualizado para o App-V 4,5, é possível criar um script de solução alternativa para preservar os pacotes da versão 4,2 nos clientes da versão 4,5 e permitir que eles sejam gerenciados. Esse script deve copiar dois arquivos, msvcp71.dll e msvcr71.dll, para a pasta de instalação do App-V e definir os seguintes valores de chave do registro na chave do registro: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

    "ClientVersion" = "4.2.1.20"

    "GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (um local gravável globalmente)



-   Os arquivos do Windows Installer gerados pela App-V 4,5 Sequencer exibem a mensagem de erro "Este pacote requer o cliente do Microsoft Application Virtualization 4,5 ou posterior" ao tentar executá-los em um cliente do App-V 4,6. Abra o pacote antigo com o sequenciador do App-V 4,5 SP1 ou o sequenciador do App-V 4,6 e gere um novo arquivo. msi para o pacote.

-   Quaisquer relatórios da versão 4,2 que foram criados e salvos serão substituídos quando o servidor for atualizado para a versão 4,5. Se precisar manter esses relatórios, você deve salvar uma cópia de backup do arquivo SftMMC. msc localizado na pasta do console de gerenciamento do SoftGrid no servidor e usar essa cópia para substituir o novo SftMMC. msc que é instalado durante a atualização.

-   Para obter informações adicionais sobre a atualização de versões anteriores, consulte [atualização para perguntas frequentes do Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Suporte ao pacote cliente do App-V 4,6


Você pode implantar pacotes criados em versões anteriores dos clientes do App-v para o App-V 4,6. No entanto, você deve modificar o arquivo. OSD associado para que ele inclua o sistema operacional apropriado e as informações sobre a arquitetura do chip. Os seguintes valores podem ser usados:

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



Para executar um pacote de 32 bits recém-criado, você deve sequenciar o aplicativo em um computador que executa um sistema operacional de 32 bits com o sequenciador do App-V 4,6 instalado. Depois de sequenciar o aplicativo, no console do sequenciador, clique na guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.

**Importante**  
Aplicativos sequenciados em um computador executando um sistema operacional de 64 bits devem ser implantados em computadores que executam um sistema operacional de 64 bits. Os novos pacotes de 32 bits criados usando o sequenciador do App-V 4,6 não são executados em computadores que executam o cliente App-V 4,5.



Para executar novos pacotes de 64 bits no cliente do App-V 4,6, você deve sequenciar o aplicativo em um computador que executa o sequenciador do App-V 4,6 e que está executando um sistema operacional de 64 bits. Depois de sequenciar o aplicativo, no console do sequenciador, clique na guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.

A tabela a seguir lista quais versões do cliente executarão pacotes criados usando as várias versões do sequenciador.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,2</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,5</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 de 32 bits</th>
<th align="left">Sequenciado usando o sequenciador do App-V 4,6 de 64 bits</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>cliente do 4,2</p></td>
<td align="left"><p>Sim</p></td>
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
</tr>
<tr class="odd">
<td align="left"><p>cliente do 4,6 (32 bits)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="even">
<td align="left"><p>cliente do 4,6 (64 bits)</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
</tbody>
</table>



o ¹ aplica-se a todas as versões do cliente App-V 4,5, incluindo o App-V 4,5, o App-V 4,5 CU1 e o App-V 4,5 SP1.









