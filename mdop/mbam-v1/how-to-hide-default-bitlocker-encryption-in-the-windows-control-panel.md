---
title: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
description: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799486"
---
# Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows


O monitoramento e administração do Microsoft BitLocker (MBAM) oferece um painel de controle personalizado para computadores cliente MBAM nomeados como opções de criptografia BitLocker. Este painel de controle personalizado pode substituir o painel de controle padrão do Windows BitLocker chamado de criptografia de unidade de disco BitLocker. O painel de controle opções de criptografia do BitLocker, localizado em sistema e segurança, no painel de controle do Windows, permite que os usuários gerenciem seu PIN e senhas, desbloqueiem unidades e ocultem a interface que permite que os administradores descriptografem uma unidade ou suspendam ou retomem a criptografia do BitLocker.

**Para ocultar a criptografia do BitLocker padrão no painel de controle do Windows**

1.  Navegue até **configuração do usuário** usando o GPMC (console de gerenciamento de política de grupo), o gerenciamento avançado de política de grupo (AGPM) ou o editor de política de grupo local no computador de políticas de grupo do BitLocker.

2.  Clique em **políticas**, selecione **modelos administrativos**e, em seguida, clique em **painel de controle**.

3.  No painel **detalhes** , clique duas vezes em **ocultar itens do painel de controle especificado**e selecione **habilitado**.

4.  Clique em **Mostrar**, **clique em Adicionar...** e digite Microsoft. BitLockerDriveEncryption. Essa política oculta a ferramenta de gerenciamento do Windows BitLocker padrão do painel de controle do Windows e permite ao usuário abrir a ferramenta de opções de criptografia do BitLocker MBAM atualizada a partir do painel de controle do Windows.

## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





