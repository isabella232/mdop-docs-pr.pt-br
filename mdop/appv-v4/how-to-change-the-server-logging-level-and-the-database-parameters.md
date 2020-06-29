---
title: Como alterar o nível de log do servidor e os parâmetros do banco de dados
description: Como alterar o nível de log do servidor e os parâmetros do banco de dados
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797244"
---
# Como alterar o nível de log do servidor e os parâmetros do banco de dados


Você pode usar os procedimentos a seguir para alterar o nível de log e os parâmetros do log de banco de dados do console de gerenciamento do servidor do Application Virtualization.

Os seguintes níveis de log estão disponíveis:

-   Somente transação

-   Erros fatais

-   Erros

-   Avisos/erros

-   Informações/avisos/erros

-   Detalha

**Observação**  Devido ao tamanho do arquivo de log produzido quando você usa o modo **Verbose** , a recomendação é que você não execute servidores de produção com esse nível de log definido.

 

Os parâmetros de log de banco de dados determinam o tipo de driver de banco de dados, credenciais de acesso e local do banco de dados de log.

**Para alterar o nível de log para servidores de gerenciamento**

1.  Clique no nó **Server groups** para exibir os grupos de servidores.

2.  Clique com o botão direito do mouse no grupo servidor e selecione **Propriedades**.

3.  Na caixa de diálogo **Propriedades** , selecione a guia **registro em log** .

4.  Na caixa de diálogo **Propriedades do grupo de servidores** , selecione o servidor e, em seguida, clique em **Editar**.

5.  Na caixa de diálogo **Adicionar/editar módulo de log** , selecione o nível de registro em log na lista suspensa **tipo de evento** .

6.  Clique em **OK**.

7.  Na caixa de diálogo **Propriedades do grupo de servidores** , clique em **OK** ou **aplicar**.

**Para alterar o nível de registro em log para servidores de streaming**

1.  Edite o seguinte valor da chave do registro para alterar o nível de log:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel

2.  Selecione um dos seguintes valores para definir o nível de registro em log.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Valor</th>
    <th align="left">Nível de log</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>0</p></td>
    <td align="left"><p>Somente transações</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>um</p></td>
    <td align="left"><p>Erros fatais</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>2</p></td>
    <td align="left"><p>Erros</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>3D</p></td>
    <td align="left"><p>Avisos/erros</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>4</p></td>
    <td align="left"><p>Informações/avisos/erros</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>5</p></td>
    <td align="left"><p>Detalha</p></td>
    </tr>
    </tbody>
    </table>

     

**Para alterar os parâmetros do log de banco de dados**

1.  Clique no nó **Server groups** para exibir os grupos de servidores.

2.  Clique com o botão direito do mouse no grupo servidor e selecione **Propriedades**.

3.  Na caixa de diálogo **Propriedades** , selecione a guia **registro em log** .

4.  Na caixa de diálogo **Propriedades do grupo de servidores** , selecione o servidor e, em seguida, clique em **Editar**.

5.  Na caixa de diálogo **Adicionar/editar módulo de log** , selecione um driver de banco de dados na lista suspensa **Driver de banco de dados** .

6.  Digite um **nome de host DNS**.

7.  Clique na caixa de seleção **determinar porta dinamicamente** ou digite um número de porta no campo **porta** .

8.  Insira um **nome de serviço** no campo correspondente.

9.  Clique em **OK**.

10. Na caixa de diálogo **Propriedades do grupo de servidores** , clique em **OK** ou **aplicar**.

## Tópicos relacionados


[Como personalizar um Application Virtualization System no Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





