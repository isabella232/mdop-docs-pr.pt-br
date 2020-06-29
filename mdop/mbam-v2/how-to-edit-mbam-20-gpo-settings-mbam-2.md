---
title: Como editar Configurações GPO do MBAM 2.0
description: Como editar Configurações GPO do MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799402"
---
# Como editar Configurações GPO do MBAM 2.0


Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), primeiro você precisa determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker. Consulte [planejando os requisitos da política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obter mais informações sobre as diferentes políticas disponíveis. Depois de determinar as políticas que você vai usar, você deve modificar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política para MBAM.

Você pode usar as etapas a seguir para configurar as configurações básicas e recomendadas do GPO para permitir que o MBAM gerencie a criptografia de BitLocker para os computadores cliente da sua organização.

**Para editar as configurações de GPO do cliente MBAM**

1.  Em um computador que tenha o modelo de política de grupo do MBAM instalado, verifique se os serviços do MBAM estão habilitados.

2.  Usando o console de gerenciamento de política de grupo (GPMC. msc) ou o produto avançado do MDOP do gerenciamento de política de grupo (AGPM) em um computador com o modelo de política de grupo do MBAM instalado, selecione **configuração do computador**, escolha **políticas**, clique em **modelos administrativos**, selecione **componentes do Windows**e clique em **MDOP MBAM (gerenciamento de BitLocker)**.

3.  Edite as configurações do objeto de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente. Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política**e, em seguida, defina a **configuração**:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Grupo de políticas</th>
    <th align="left">Política</th>
    <th align="left">Configuração</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gerenciamento de Clientes</p></td>
    <td align="left"><p>Configurar os serviços do MBAM</p></td>
    <td align="left"><p>Enabled. Defina o <strong> ponto de extremidade do serviço de hardware e recuperação do MBAM </strong> e <strong> Selecione informações de recuperação do BitLocker a serem armazenadas </strong> . Defina o <strong> ponto de extremidade do serviço de conformidade </strong> do MBAM e insira a frequência do relatório de status em (minutos).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidade do sistema operacional</p></td>
    <td align="left"><p>Configurações de criptografia de unidade do sistema operacional</p></td>
    <td align="left"><p>Enabled. Defina o <strong> protetor de seleção para unidade do sistema operacional </strong> . É necessário para salvar os dados da unidade do sistema operacional no servidor de recuperação do MBAMKey.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unidade de disco removível</p></td>
    <td align="left"><p>Controlar o uso do BitLocker em unidades removíveis</p></td>
    <td align="left"><p>Enabled. Obrigatório se o MBAM salvar os dados da unidade removível para o servidor de recuperação de chave do MBAM.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidade fixa</p></td>
    <td align="left"><p>Controlar o uso do BitLocker em unidades fixas</p></td>
    <td align="left"><p>Enabled. Obrigatório se o MBAM salvará os dados da unidade fixa no servidor de recuperação de chave do MBAM.</p>
    <p>Definir <strong> escolha como as unidades protegidas pelo BitLocker podem ser recuperadas </strong> e <strong> permitir o agente de recuperação de dados </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









