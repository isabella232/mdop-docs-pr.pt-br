---
title: Sobre o Microsoft Application Virtualization 4.6 SP2
description: Sobre o Microsoft Application Virtualization 4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797641"
---
# Sobre o Microsoft Application Virtualization 4.6 SP2


O Microsoft Application Virtualization (App-V) 4.6 SP2 oferece vários aprimoramentos e novos recursos, que estão descritos neste tópico.

**Cuidado**  Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.

 

**Suporte para Windows 8 e Windows Server 2012**

O App-V 4.6 SP2 adiciona suporte para serviços de área de trabalho remota do Windows 8 e do Windows Server 2012.

**Suporte para a coexistência com o cliente App-V 5,0**

O App-V 4.6 SP2 oferece suporte à coexistência com o cliente do Microsoft Application Virtualization 5,0. Examine a documentação do App-V 5,0 para obter instruções sobre como configurar o cliente do App-V 5,0 para coexistência com o cliente App-V 4.6 SP2. Para obter mais informações sobre o App-V 5,0, consulte [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on technet.

**Capacidade de virtualização do Adobe Reader X com modo protegido**

Você pode virtualizar o Adobe Reader X com o recurso modo protegido ativado usando os procedimentos a seguir. Antes, era preciso desabilitar o modo protegido para virtualizar o Adobe Reader X.

Antes de iniciar o sequenciador do App-V, crie o seguinte valor do registro em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nome</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Dados</p></td>
<td align="left"><p>Descrição</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>um</p></td>
<td align="left"><p>Defina esse valor como <strong> 1 para </strong> iniciar o Adobe Reader X no modo protegido durante a fase de início.</p></td>
</tr>
</tbody>
</table>

 

**Observação**  Em um computador que executa um sistema operacional de 64 bits, crie o valor do registro em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.

 

Para cada arquivo OSD-em seu pacote Adobe Reader X, adicione os seguintes itens no &lt; elemento policies &gt; :

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Novo parâmetro de linha de comando do sequenciador**

Ao criar um acelerador de pacote (PA) por meio da GUI do sequenciador, você pode selecionar um arquivo RTF ou TXT que forneça diretrizes de empacotamento e implantação para os administradores que aplicarão o acelerador de pacote. Esta funcionalidade já está disponível usando a CLI do sequenciador.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Especifique um caminho para um arquivo RTF ou TXT que fornece diretrizes de empacotamento e implantação ao criar um acelerador de pacote.

**Não é mais necessário instalar o relatório de erros do aplicativo Microsoft**

Ao instalar o cliente App-V 4.6 SP2 usando o setup.msi, você não precisa mais instalar o relatório de erros do aplicativo Microsoft (dw20shared.msi). O App-V 4.6 SP2 agora usa o relatório de erros da Microsoft. Para obter mais informações, consulte [como instalar o cliente App-V usando Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Feedback do cliente e pacote cumulativo de hotfix**

O App-V 4.6 SP2 inclui um pacote cumulativo de correções para solucionar problemas encontrados desde a versão App-V 4,6 SP1. O App-V 4.6 SP2 contém as correções mais recentes até e incluindo o hotfix 6 do Microsoft Application Virtualization 4,6 SP1.

## Nesta seção


<a href="" id="app-v-4-6-sp2-release-notes"></a>[Notas de versão do App-V 4.6 SP2](https://go.microsoft.com/fwlink/?LinkId=267600)  
Fornece as informações mais atualizadas sobre problemas conhecidos com o App-V 4.6 SP2.

 

 





