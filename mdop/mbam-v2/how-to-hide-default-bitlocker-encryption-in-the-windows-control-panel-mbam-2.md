---
title: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
description: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799401"
---
# Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows


O monitoramento e administração do Microsoft BitLocker (MBAM) oferece um painel de controle personalizado para os computadores cliente de administração e monitoramento do Microsoft BitLocker, chamados opções de criptografia do BitLocker. Este painel de controle personalizado pode substituir o painel de controle padrão do Windows BitLocker, que é chamado de criptografia de unidade de disco BitLocker. O painel de controle personalizado, que está no painel de controle, em sistema e segurança, permite que os usuários gerenciem seu PIN e senhas e desbloqueiem unidades e ocultam a interface que permite que os administradores descriptografem uma unidade ou suspendam ou retomem a criptografia de unidade de disco BitLocker.

**Para ocultar a criptografia de unidade de disco BitLocker padrão no painel de controle do Windows**

1.  No GPMC (console de gerenciamento de política de grupo), no gerenciamento avançado de política de grupo (AGPM) ou no editor de política de grupo local no computador de políticas de grupo do BitLocker, navegue até **configuração do usuário**.

2.  Em seguida, clique em **políticas**, selecione **modelos administrativos**e, em seguida, clique em **painel de controle**.

3.  Clique duas vezes em **ocultar itens do painel de controle especificado** no painel **detalhes** e selecione **habilitado**.

4.  Clique em **Mostrar**, clique em **Adicionar**e, em seguida, digite **Microsoft. BitLockerDriveEncryption**. Essa política oculta a ferramenta de gerenciamento do Windows BitLocker padrão no painel de controle do Windows e, no painel de controle, permite ao usuário abrir a ferramenta de opções de criptografia do BitLocker MBAM atualizada em sistema e segurança.

## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





