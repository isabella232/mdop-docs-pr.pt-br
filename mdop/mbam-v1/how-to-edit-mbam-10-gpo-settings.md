---
title: Como editar Configurações GPO do MBAM 1.0
description: Como editar Configurações GPO do MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799441"
---
# Como editar Configurações GPO do MBAM 1.0


Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), você deve primeiro determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker. Para obter mais informações sobre as várias políticas disponíveis, consulte [planejando os requisitos da política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Depois de determinar as políticas que você vai usar, você deve modificar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política de MBAM.

As etapas a seguir descrevem como configurar as configurações de objeto de política de grupo (GPO) recomendadas e básicas para permitir que o MBAM gerencie a criptografia de BitLocker para os computadores cliente da sua organização.

**Para editar as configurações de GPO do cliente MBAM**

1.  Em um computador que tenha o modelo de política de grupo do MBAM instalado, verifique se os serviços do MBAM estão habilitados.

2.  Use o console de gerenciamento de política de grupo (GPMC. msc) ou o produto avançado do MDOP de gerenciamento de política de grupo (AGPM) para estas ações: selecione **configuração do computador**, escolha **políticas**, clique em **modelos administrativos**, selecione **componentes do Windows**e clique em **MDOP MBAM (gerenciamento de BitLocker)**.

3.  Edite as configurações do objeto de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente. Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política**e, em seguida, defina a **configuração**.

    Grupo de políticas

    Política

    Configuração

    Gerenciamento de Clientes

    Configurar os serviços do MBAM

    Enabled. Defina o **ponto de extremidade do serviço de hardware e recuperação do MBAM** e **Selecione informações de recuperação do BitLocker a serem armazenadas**.

    Defina o **ponto de extremidade do serviço de conformidade do MBAM** e insira a **frequência do relatório de status em (minutos)**.

    Permitir verificação de compatibilidade de hardware

    Desabilitado. Essa política é habilitada por padrão, mas não é necessária para uma implementação de MBAM básica.

    Unidade do sistema operacional

    Configurações de criptografia de unidade do sistema operacional

    Enabled. Defina o **protetor de seleção para unidade do sistema operacional**. Isso é necessário para salvar os dados da unidade do sistema operacional no servidor de recuperação de chave MBAM.

    Unidade de disco removível

    Controlar o uso do BitLocker em unidades removíveis

    Enabled. Isso é necessário se o MBAM salvará os dados da unidade removível para o servidor de recuperação de chave do MBAM.

    Unidade fixa

    Controlar o uso do BitLocker em unidades fixas

    Enabled. Isso é necessário se o MBAM salvará os dados da unidade fixa no servidor de recuperação de chave do MBAM.

    Definir **escolha como as unidades protegidas pelo BitLocker podem ser recuperadas** e **permitir o agente de recuperação de dados**.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 1.0](deploying-mbam-10-group-policy-objects.md)









