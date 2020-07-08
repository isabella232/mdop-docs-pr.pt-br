---
title: Opções de linha de comando para arquivos de instalação da MED-V
description: Opções de linha de comando para arquivos de instalação da MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799878"
---
# Opções de linha de comando para arquivos de instalação da MED-V


Ao instalar ou desinstalar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, você tem a opção de executar os arquivos de instalação no prompt de comando. Esta seção descreve diferentes opções que você pode especificar ao instalar ou desinstalar o MED-V no prompt de comando.

### Argumentos de linha de comando

Você pode usar os seguintes argumentos de linha de comando juntamente com seus respectivos arquivos de instalação do MED-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquivo de instalação</th>
<th align="left">Argumento</th>
<th align="left">Valores aceitos</th>
<th align="left">Tipo</th>
<th align="left">Descrição</th>
<th align="left">Padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agente do host</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;caminho de instalação&gt;</p></td>
<td align="left"><p>Instalação</p></td>
<td align="left"><p>Alterar diretório de instalação</p></td>
<td align="left"><p>A instalação vai para o programa Files\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pacote de espaço de trabalho do MED-V</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;caminho de instalação&gt;</p></td>
<td align="left"><p>Instalação</p></td>
<td align="left"><p>Alterar diretório de instalação</p></td>
<td align="left"><p>A instalação vai para o programa Files\Microsoft Enterprise Desktop Virtualization.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço de trabalho do MED-V</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;caminho de instalação&gt;</p></td>
<td align="left"><p>Instalação</p></td>
<td align="left"><p>Alterar diretório de instalação</p></td>
<td align="left"><p>A instalação vai para o ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espaço de trabalho do MED-V</p></td>
<td align="left"><p>SUBSTITUIR VHD</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Instalação</p></td>
<td align="left"><p>Falha na instalação se o VHD existir (0) ou substituir o VHD existente (1).</p></td>
<td align="left"><p>Substituir não ocorrerá e a instalação falhará se um VHD (disco rígido virtual) já existir.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espaço de trabalho do MED-V</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Instalação</p></td>
<td align="left"><p>Iniciar (0) ou não iniciar (1) MED-V após a instalação do espaço de trabalho do MED-V.</p></td>
<td align="left"><p>Se o espaço de trabalho do MED-V foi instalado com a interface do usuário (IU), uma caixa de seleção na <strong> </strong> página concluir controlará se o MED-v deve ser iniciado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espaço de trabalho do MED-V</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 ou 1</p></td>
<td align="left"><p>Desinstalação</p></td>
<td align="left"><p>Manter (0) ou excluir (1) VHDs criados pelo MED-V</p></td>
<td align="left"><p>Nenhum VHDs é excluído.</p></td>
</tr>
</tbody>
</table>

 

### Exemplos de argumentos de linha de comando

O exemplo a seguir instala o espaço de trabalho do MED-V criado pelo pacote do espaço de trabalho do MED-V. O arquivo de instalação cria um arquivo de log no diretório temp e executa o arquivo de instalação no modo silencioso, mas não inicia o agente do host do MED-V na conclusão. O arquivo de instalação substitui qualquer VHD deixado por trás de uma instalação anterior com o mesmo nome.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

O exemplo a seguir desinstala o espaço de trabalho do MED-V que foi instalado anteriormente. O arquivo de instalação cria um arquivo de log no diretório temp e executa o arquivo de instalação no modo silencioso. O arquivo de instalação exclui todos os arquivos de disco rígido virtual restantes do sistema de arquivos.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Tópicos relacionados


[Implantar os componentes da MED-V](deploy-the-med-v-components.md)

[Referência técnica da MED-V](technical-reference-for-med-v.md)

 

 





