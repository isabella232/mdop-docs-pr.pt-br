---
title: Implantação do catálogo de modelos de configurações para a UE-V 1.0
description: Implantação do catálogo de modelos de configurações para a UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799911"
---
# Implantação do catálogo de modelos de configurações para a UE-V 1.0


Modelos de local de configurações personalizadas podem ser armazenados em um caminho de pasta nos computadores Microsoft User Experience Virtualization (UE-V) ou em um compartilhamento de rede SMB (bloco de mensagens de servidor). Uma tarefa agendada do computador verifica se há modelos novos ou atualizados deste local. A tarefa verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta. Os modelos adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V Agent. O UE-V Agent cancela o registro de modelos que foram removidos desta pasta. A tarefa agendada é executada como sistema. No mínimo, o compartilhamento de rede deve conceder permissões para o grupo computadores do domínio. Além disso, conceda permissões de acesso à pasta de compartilhamento de rede para administradores que gerenciam os modelos armazenados. Para obter mais informações sobre modelos de localização de configuração personalizada, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**Para configurar o catálogo de modelos de configurações para UE-V**

1.  Crie uma nova pasta no computador que irá armazenar o catálogo de modelos de configurações do UE-V.

2.  Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta catálogo de modelos de configurações.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computadores do domínio</p></td>
    <td align="left"><p>Ler níveis de permissão</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Níveis de permissão de leitura/gravação</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Defina as seguintes permissões de NTFS para a pasta catálogo de modelos de configurações.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Conta de usuário</th>
    <th align="left">Permissões recomendadas</th>
    <th align="left">Aplicar a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Criador/proprietário</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computadores do domínio</p></td>
    <td align="left"><p>Listar conteúdo da pasta e ler</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Clique em **OK** para fechar as caixas de diálogo.

## Tópicos relacionados


[Implantação da UE-V 1.0](deploying-ue-v-10.md)

[Planejar a implantação de modelo personalizado para a UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





