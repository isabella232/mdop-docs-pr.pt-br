---
title: Identificação do número e dos tipos de espaços de trabalho da MED-V
description: Identificação do número e dos tipos de espaços de trabalho da MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800037"
---
# Identificação do número e dos tipos de espaços de trabalho da MED-V


O MED-V cria um ambiente virtual para executar aplicativos que exijam o Windows XP ou que exijam uma versão do Internet Explorer diferente da versão do computador host. Esse ambiente virtual é conhecido como um espaço de trabalho do MED-V.

Dependendo dos requisitos de compatibilidade do aplicativo enfrentados pela sua organização durante a migração para o Windows 7, apenas determinados usuários ou departamentos podem exigir espaços de trabalho do MED-V. Ao planejar sua implantação, você precisa determinar o número de espaços de trabalho do MED-V necessários na sua empresa. Você também precisa definir os requisitos de cada espaço de trabalho do MED-V.

## Identificar o número e os tipos de espaços de trabalho do MED-V


Identifique os computadores e grupos da sua empresa para os quais você criará os espaços de trabalho do MED-V. Geralmente, estes são os usuários que precisam de acesso a esses aplicativos que não podem ser migrados para o Windows 7. Identifique os aplicativos que não podem ser migrados e os usuários que precisam de um espaço de trabalho do MED-V para executar esses aplicativos.

Você também pode ter endereços de intranet que ainda não foram otimizados para o Windows 7. O espaço de trabalho do MED-V fornece um navegador do Internet Explorer pelo qual os usuários finais podem acessar melhor os endereços da Web que ainda não estão prontos para a migração para o Windows 7. À medida que você estiver preparando e planejando a implantação do MED-V, será preciso identificar e compilar uma lista dos endereços de URL para redirecionar do Internet Explorer no computador host para o Internet Explorer no espaço de trabalho do MED-V.

Por fim, avalie os requisitos de espaço em disco. A maioria dos espaços de trabalho do MED-V tem 2 gigabytes (GB) ou mais. O espaço disponível em disco em um sistema pode ser resumido rapidamente, dependendo do número de usuários e a configuração do MED-V. Além disso, o método de distribuição preferido da sua empresa pode exigir espaço adicional. Geralmente, você deve liberar um mínimo de 10 GB de espaço em disco para um espaço de trabalho do MED-V, mas isso varia muito, dependendo do tamanho da imagem.

### Calcular os requisitos de espaço em disco para os espaços de trabalho do MED-V

Um espaço de trabalho do MED-V requer memória e espaço em disco do computador host no qual ele está instalado. É preciso ter no mínimo 2 GB de espaço em disco no host. O espaço em disco é variável e depende do número de aplicativos e dos dados em um espaço de trabalho do MED-V do usuário.

Recomendamos um mínimo de 10 GB de espaço em disco para o MED-V. Esse valor permite um espaço de trabalho básico do Windows XP e alguns aplicativos e redirecionamento de Web instalados. Ele também fornece espaço disponível para a unidade de troca de host. Em uma configuração básica, o MED-V e um único espaço de trabalho do MED-V implantado consomem até 6 a 8 GB. Se você incluir muitos aplicativos no espaço de trabalho do MED-V ou tiver mais de um usuário por computador, poderá usar o seguinte cálculo para determinar o espaço em disco que o seu espaço de trabalho do MED-V requer:

*VHD + base (usuário por computador x (disco de diferença + estado salvo))*

Para calcular o espaço em disco necessário, determine o seguinte:

-   **Tamanho do VHD base** – o disco rígido virtual que foi usado para criar o espaço de trabalho do MED-V.

    **Importante**  Não use o tamanho do arquivo. medv para o seu cálculo porque o arquivo. medv está compactado.

     

-   **Usuários por computador** – med-v cria um espaço de trabalho do MED-v para cada usuário em um computador; o espaço de trabalho do MED-V consome espaço em disco quando cada usuário se conecta e o espaço de trabalho do MED-V é criado.

-   **Tamanho do disco diferencial** – usado para acompanhar a diferença do VHD base. Esse tamanho varia à medida que você adiciona aplicativos e atualizações de software ao disco rígido virtual. Um disco diferencial é criado para cada usuário do MED-V quando eles iniciam MED-V pela primeira vez.

-   **Tamanho do arquivo de estado salvo** – usado para manter o estado na máquina virtual. Geralmente, isso é um pouco maior do que a RAM alocada para a máquina virtual. Por exemplo, 1 GB de RAM alocado cria um arquivo sobre 1.081.000 KB.

O exemplo a seguir mostra um cálculo com base em três usuários de um espaço de trabalho do MED-V que tem um disco rígido virtual de 2,6 GB:

*2.6 GB + (3 x (1,5 GB + 1GB)) = 10.1 GB*

**Observação**  Uma prática recomendada do MED-V é calcular o espaço necessário usando uma implantação de laboratório para validar os requisitos.

 

### Localizar os arquivos para determinar o tamanho do arquivo

Os seguintes locais contêm os arquivos para as configurações do computador e do usuário:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo</th>
<th align="left">Localização</th>
<th align="left">Arquivos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VHD base</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> . vhd-Where <em> InternalName </em> é o nome do disco rígido virtual selecionado no pacote do espaço de trabalho do MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disco diferencial</p></td>
<td align="left"><p>Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . vhd</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivo de estado salvo</p></td>
<td align="left"><p>Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . VSV</p></td>
</tr>
</tbody>
</table>

 

### Calcular os requisitos de espaço em disco para espaços de trabalho do MED-V compartilhados

Se você estiver calculando uma implantação do espaço de trabalho do MED-V compartilhado em um único computador, o número de usuários por computador em seu cálculo será sempre "1" porque o MED-V configura apenas um único disco diferencial para todos os usuários.

Você pode encontrar o disco diferencial e o arquivo de estado salvo para os espaços de trabalho do MED-V compartilhados no%ProgramData%\\Microsoft\\Medv\\AllUsers.

## Tópicos relacionados


[Definir e planejar sua implantação da MED-V](define-and-plan-your-med-v-deployment.md)

[Planejamento para o MED-V](planning-for-med-v.md)

 

 





