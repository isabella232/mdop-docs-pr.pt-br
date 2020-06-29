---
title: Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0
description: Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799144"
---
# Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0


Use as informações desta seção quando planejar salvar e implantar a imagem de recuperação do Microsoft (diagnóstico e recuperação) do Microsoft (Microsoft Diagnostics and Recovery Toolset) 7.

## Planejar como salvar e implantar a imagem de recuperação do DaRT


Você pode salvar e implantar a imagem de recuperação do DaRT usando os métodos a seguir. Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um. Além disso, considere como você deseja usar o DaRT na sua empresa.

**Observação**  Talvez você queira usar mais de um método em sua organização. Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.

 

A tabela a seguir mostra algumas vantagens e desvantagens de cada método de usar o DaRT em sua organização.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método para inicializar o DaRT</th>
<th align="left">Vantagens</th>
<th align="left">Desvantagens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>A partir de um CD ou DVD</p></td>
<td align="left"><p>Oferece suporte a cenários em que o registro de inicialização mestre (MBR) está corrompido e não é possível acessar o disco rígido. Também oferece suporte a casos em que não há conexão de rede.</p>
<p>Isso é mais familiar para os usuários de versões anteriores do DaRT, e um CD ou DVD pode ser gravado diretamente do <strong> Assistente de recuperação de imagem de DART </strong> .</p></td>
<td align="left"><p>Requer que alguém com acesso ao CD ou DVD esteja fisicamente no computador do usuário final para inicializar o DaRT.</p></td>
</tr>
<tr class="even">
<td align="left"><p>De uma unidade flash USB (UFD)</p></td>
<td align="left"><p>Fornece as mesmas vantagens que a inicialização a partir de um CD ou DVD e também fornece suporte a computadores que não têm unidade de CD ou DVD.</p></td>
<td align="left"><p>Requer que você formate o UFD antes de poder usá-lo para inicializar o DaRT. Também requer que alguém com acesso à unidade UFD seja fisicamente no computador do usuário final para inicializar o DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>De uma partição remota (rede)</p></td>
<td align="left"><p>Permite que você inicialize no DaRT sem precisar de um CD, DVD ou UFD. Também permite atualizações fáceis do DaRT porque só há um local de arquivo para atualizar.</p></td>
<td align="left"><p>Não funcionará se o computador do usuário final não estiver conectado à rede.</p>
<p>Amplamente disponível para usuários finais e pode exigir considerações de segurança adicionais ao criar a imagem de recuperação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>De uma partição de recuperação</p></td>
<td align="left"><p>Permite que você inicialize no DaRT sem precisar de um CD, DVD ou UFD que inclua instâncias em que não há conectividade de rede.</p>
<p>Além disso, pode ser implementada e gerenciada como parte do processo de imagem padrão do Windows usando ferramentas de distribuição automatizadas, como o Gerenciador de configuração do Microsoft Endpoint.</p></td>
<td align="left"><p>Ao atualizar o DaRT, você precisa atualizar todos os computadores na sua empresa, em vez de apenas uma partição (na rede) ou dispositivo (CD, DVD ou UFD).</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejamento da implantação do DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





