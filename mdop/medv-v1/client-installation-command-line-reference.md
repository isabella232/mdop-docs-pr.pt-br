---
title: Referência de linha de comando para instalação do cliente
description: Referência de linha de comando para instalação do cliente
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799930"
---
# Referência de linha de comando para instalação do cliente


**Para instalar o MED-V na linha de comando**

1.  Na linha de comando, execute o pacote MED-V. msi seguido de qualquer um dos parâmetros opcionais descritos na tabela a seguir.

2.  O pacote MED-V. msi é chamado *MED-V\_x.msi*, em que *x* é o número da versão.

    Por exemplo, *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valor</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Instalação silenciosa</p></td>
</tr>
<tr class="even">
<td align="left"><p>/log &lt; caminho completo para o arquivo de log&gt;</p></td>
<td align="left"><p>O caminho completo para o arquivo de log.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>O caminho completo para o diretório de instalação.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>O caminho completo para a pasta da máquina virtual.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Padrão: <strong> 0</strong></p></td>
<td align="left"><p>Instala as ferramentas de administração do MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Padrão: <strong> 0</strong></p></td>
<td align="left"><p>Inicia automaticamente o cliente MED-V toda vez que o usuário faz logon no Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>nome do host ou IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>porta</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>para <strong> https </strong> ou <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Padrão: <strong> 1</strong></p></td>
<td align="left"><p>Inicia o MED-V na conclusão da instalação do MED-V.</p>
<div class="alert">
<strong>Observação</strong><br/><p>É recomendável definir START_MEDV = 0 em caso de caso o MED-V seja instalado pelo sistema.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>Padrão: <strong> 1</strong></p></td>
<td align="left"><p>Cria um atalho na área de trabalho, que inicia o cliente MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM em MB</p></td>
<td align="left"><p>Ao instalar o MED-V, verifica se o computador tem a quantidade mínima de RAM especificada. Caso contrário, a instalação será abortada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1, 0</strong></p></td>
<td align="left"><p>Omite a validação do sistema operacional.</p></td>
</tr>
</tbody>
</table>











