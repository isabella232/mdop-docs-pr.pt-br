---
title: Página de opções avançadas do assistente de sequenciamento do Application Virtualization
description: Página de opções avançadas do assistente de sequenciamento do Application Virtualization
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797557"
---
# Página de opções avançadas do assistente de sequenciamento do Application Virtualization


Use a página de **Opções avançadas** do assistente de sequenciamento do Application Virtualization (App-V) para especificar opções avançadas para o aplicativo a ser instalado. A página contém os elementos descritos na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Tamanho do bloco</strong></p></td>
<td align="left"><p>Use para especificar o tamanho dos blocos dos quais o arquivo SFT será dividido quando transmitido em uma rede. Todos os blocos são iguais ao tamanho especificado; no entanto, o último bloco pode ser menor do que o especificado. Selecione um dos seguintes valores:</p>
<ul>
<li><p><strong>4 KB</strong></p></li>
<li><p><strong>16 KB</strong></p></li>
<li><p><strong>32 KB</strong></p></li>
<li><p><strong>64 KB</strong></p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Quando você selecionar um tamanho de bloco, considere o tamanho do arquivo SFT e a largura de banda da rede. Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda. Arquivos com tamanhos de blocos maiores podem ser usados com mais rapidez, mas usam mais largura de banda de rede. Por meio da experimentação, você pode descobrir o tamanho de bloco ideal para aplicativos de streaming na sua rede.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Habilitar o Microsoft Update durante o monitoramento</strong></p></td>
<td align="left"><p>Permite a instalação de atualizações da Microsoft durante o assistente de sequenciamento&#39;fase de monitoramento de s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Alterar a base das DLLs</strong></p></td>
<td align="left"><p>Permite o remapeamento de bibliotecas de vínculo dinâmico compatíveis para um espaço contíguo na RAM, economizando memória e melhorando o desempenho.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Voltar</strong></p></td>
<td align="left"><p>Acessa o assistente de sequenciamento&#39;a página anterior.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Próxima</strong></p></td>
<td align="left"><p>Acessa o assistente de sequenciamento&#39;s próxima página.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cancelar</strong></p></td>
<td align="left"><p>Finaliza a operação do assistente de sequenciamento.</p></td>
</tr>
</tbody>
</table>



\ [Valor do token do modelo \]

Use a página de **Opções avançadas** do assistente de sequenciamento do App-V para especificar opções avançadas para o aplicativo que você está sequenciando. Esta página contém os elementos descritos na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Permitir que o Microsoft Update seja executado durante o monitoramento</strong></p></td>
<td align="left"><p>Especifica se as atualizações de software serão aplicadas ao aplicativo durante a fase de monitoramento do sequenciamento do aplicativo. Esta opção será útil se as atualizações forem necessárias para concluir a instalação do aplicativo com êxito. Essa opção não é selecionada por padrão.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Alterar a base das DLLs</strong></p></td>
<td align="left"><p>Permite o remapeamento de bibliotecas de vínculo dinâmico compatíveis para um espaço contíguo na RAM. Selecionar essa opção pode ajudar a gerenciar a memória e melhorar o desempenho do aplicativo. Essa opção não é selecionada por padrão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Voltar</strong></p></td>
<td align="left"><p>Vai para a página anterior do assistente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Próxima</strong></p></td>
<td align="left"><p>Vai para a próxima página do assistente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cancelar</strong></p></td>
<td align="left"><p>Descarta as configurações e sai do assistente.</p></td>
</tr>
</tbody>
</table>



\ [Valor do token do modelo \]

## Tópicos relacionados


[Assistente de Sequenciamento](sequencing-wizard.md)









