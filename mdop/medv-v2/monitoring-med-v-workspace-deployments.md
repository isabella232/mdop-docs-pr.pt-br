---
title: Monitoramento de implantações de espaço de trabalho da MED-V
description: Monitoramento de implantações de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800027"
---
# Monitoramento de implantações de espaço de trabalho da MED-V


O recurso de monitoramento na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 permite executar consultas em espaços de trabalho do MED-V individuais para determinar se a configuração foi bem-sucedida em toda a sua empresa após a implantação do tempo de execução dos espaços de trabalho do MED-V. Monitorar o sucesso da configuração pela primeira vez é importante porque o MED-V não está em um estado utilizável até que a configuração inicial seja concluída com êxito.

Esta seção fornece informações e instruções para ajudá-lo a monitorar o êxito ou a falha da configuração inicial.

## Para monitorar implantações de espaço de trabalho do MED-V


O recurso de monitoramento consiste em um provedor de instrumentação de gerenciamento do Windows (WMI) que você pode consultar usando a linguagem de consulta WMI para descobrir o status da primeira configuração para todos os usuários finais em um espaço de trabalho do MED-V.

O provedor WMI é implementado usando a estrutura de extensão do provedor WMI do Microsoft .NET Framework 3,5. O provedor WMI é executado no contexto de LocalService e armazena na primeira vez que o estado da configuração é seguro em \\ProgramData.

O provedor WMI é implementado no namespace **root\\microsoft\\medv** e implementa a classe **FTS \ _Status**, que expõe o método **SetFtsState**. O MED-V usa **SetFtsState** para definir o estado de configuração da primeira vez.

A classe contém as propriedades a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computador</strong></p></td>
<td align="left"><p><strong>Propriedade somente leitura </strong> que contém o nome da máquina virtual convidada provisionada pela primeira configuração de tempo. Esta chave contém o nome que o convidado teria na primeira falha na configuração da primeira vez.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong>Propriedade somente leitura </strong> que contém zero se a configuração da primeira vez for bem-sucedida. Qualquer outro valor retornado será igual à identificação do evento que é registrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Hora</strong></p></td>
<td align="left"><p>A hora UTC em que a configuração da primeira vez foi concluída.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Usuário</strong></p></td>
<td align="left"><p>O usuário pela primeira vez em que a configuração foi executada.</p></td>
</tr>
</tbody>
</table>

 

O código a seguir mostra o arquivo MOF (formato de objeto gerenciado) que define a classe **FTS \ _Status** .

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Como sua principal preocupação é mais provável que os espaços de trabalho do MED-V para os quais a configuração da primeira configuração não foram concluídas com êxito, você pode gravar sua consulta para retornar apenas aquelas que falharam na configuração inicial, por exemplo:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

Nesse caso, o recurso de monitoramento retorna uma lista dos espaços de trabalho do MED-V que falharam durante a configuração inicial, que você pode usar para realizar as ações adequadas para resolver a falha.

## Tópicos relacionados


[Monitorar espaços de trabalho da MED-V](monitor-med-v-workspaces.md)

[Como verificar as configurações da primeira instalação](how-to-verify-first-time-setup-settings.md)

 

 





