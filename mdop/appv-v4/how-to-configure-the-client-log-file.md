---
title: Como configurar o arquivo de log do cliente
description: Como configurar o arquivo de log do cliente
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797197"
---
# Como configurar o arquivo de log do cliente


Você pode usar os procedimentos a seguir para configurar o arquivo de log do cliente do Application Virtualization (App-V).

**Para alterar o local do arquivo de log**

-   Edite o seguinte valor da chave do registro para especificar o novo caminho para o arquivo de log. Você deve reiniciar o serviço **sftlist** após alterar esse valor. Este local também pode ser alterado interativamente após a instalação.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**Para alterar o nível de relatório de log**

-   Por padrão, o tipo de mensagens gravadas no log inclui todos os eventos de severidade nível 4 (informativo) ou superior. O nível de gravidade é armazenado no valor da chave a seguir. Defina esse valor de chave como 5 para habilitar o registro em log detalhado. Use o registro em log detalhado apenas por períodos curtos durante a solução de problemas, pois ele gerará um volume muito grande de mensagens e fará com que o log seja preenchido rapidamente.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**Para alterar o tamanho do log**

-   No Application Virtualization (App-V) 4,5, o tamanho do log é controlado pelo seguinte valor da chave do registro. Esse valor assume o valor padrão de 256MB e define o tamanho máximo, em MB, que o log pode crescer antes de ser redefinido.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **Cuidado**  Esse valor da chave do registro deve ser definido como um valor maior do que zero para garantir que o arquivo de log seja redefinido.

     

**Para alterar o número de cópias de backup**

-   Quando o arquivo de log atinge o tamanho máximo, uma redefinição é forçada quando ocorre a próxima gravação do log. Uma redefinição faz com que um novo arquivo de log seja criado, e o arquivo antigo é renomeado como um backup. A configuração do registro a seguir controla o número de cópias de backup do arquivo de log que são mantidas quando o arquivo é redefinido. O valor padrão é 4.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    O formato dos nomes dos arquivos de log de backup é: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** e é baseado no tempo de redefinição, no tempo universal coordenado (UTC). A tabela a seguir lista os símbolos usados na criação dos nomes de arquivo e suas descrições.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Símbolo</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>AAAA</p></td>
    <td align="left"><p>ano de 4 dígitos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>CM</p></td>
    <td align="left"><p>mês de 2 dígitos (01 – 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>MM</p></td>
    <td align="left"><p>2 dígitos no dia do mês (01 – 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>hh</p></td>
    <td align="left"><p>hora (00 – 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>cm</p></td>
    <td align="left"><p>minutos (00 a 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>segundos (00 a 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>milissegundos (000 – 999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





