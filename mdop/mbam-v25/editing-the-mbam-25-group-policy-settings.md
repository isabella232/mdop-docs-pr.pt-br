---
title: Editando as configurações de Política de Grupo do MBAM 2.5
description: Editando as configurações de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796039"
---
# Editando as configurações de Política de Grupo do MBAM 2.5


Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), você precisa:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copie os modelos de política de grupo do MBAM 2,5.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copiando os modelos de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determine quais objetos de política de grupo (GPOs) você deseja usar na implementação do MBAM. Com base nas necessidades da sua organização, talvez seja necessário definir configurações adicionais de política de grupo.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planejando os requisitos da política de grupo do MBAM 2,5 </a> – contém descrições dos GPOs</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Defina as configurações de política de grupo da sua organização.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente. Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.

 

**Para editar configurações de política de grupo do cliente MBAM**

1.  Em um computador que tenha os modelos de política de grupo do MBAM instalados, verifique se os serviços do MBAM estão habilitados.

2.  Usando o console de gerenciamento de política de grupo (GPMC. msc) ou o produto do MDOP gerenciamento de política de grupo avançado da Microsoft em um computador com os modelos de política de grupo do MBAM instalados, selecione políticas de **configuração do computador** &gt; **Policies** &gt; **modelos** &gt; **Windows Components** &gt; **do Windows MDOP MBAM (gerenciamento de BitLocker)**.

3.  Edite as configurações de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente. Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política** desejada e, em seguida, defina as configurações.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Grupo de políticas</th>
    <th align="left">Política</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gerenciamento de Clientes</p></td>
    <td align="left"><p>Configurar os serviços do MBAM</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidade do sistema operacional</p></td>
    <td align="left"><p>Configurações de criptografia de unidade do sistema operacional</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unidade de disco removível</p></td>
    <td align="left"><p>Controlar o uso do BitLocker em unidades removíveis</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidade fixa</p></td>
    <td align="left"><p>Controlar o uso do BitLocker em unidades fixas</p></td>
    </tr>
    </tbody>
    </table>

     

## Tópicos relacionados


[Planejamento para os requisitos de Política de Grupo do MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)

[Copiando os modelos de Política de Grupo do MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





