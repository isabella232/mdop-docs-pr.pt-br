---
title: Migrando pacotes de configurações do UE-V 2. x
description: Migrando pacotes de configurações do UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799688"
---
# Migrando pacotes de configurações do UE-V 2. x


No ciclo de vida de uma implantação do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, talvez seja necessário realocar os pacotes de configurações do usuário quando migrar para um novo servidor ou quando executar backups. Os pacotes de configurações podem precisar ser migrados nos seguintes cenários:

-   Atualização do hardware do servidor existente para um servidor mais moderno.

-   Migração de um local de armazenamento de configurações compartilhar de um servidor de teste para um servidor de produção.

Simplesmente copiar os arquivos e pastas não preserva as permissões e as configurações de segurança. As etapas a seguir descrevem como copiar corretamente o pacote de configurações juntamente com as permissões do sistema de arquivos NTFS para um novo compartilhamento.

**Para preservar pacotes de configurações do UE-V 2 ao migrar para um novo servidor**

1.  Em um novo local em um servidor diferente, crie uma nova pasta, por exemplo, MySettings.

2.  Desabilite o compartilhamento para o compartilhamento de pasta antiga no servidor antigo.

3.  Para copiar os pacotes de configurações existentes para o novo servidor com Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Observação**  Para monitorar o progresso da cópia, abra MySettings.txt com um visualizador de log, como Trace32.

     

4.  Conceda permissões no nível do compartilhamento para o novo compartilhamento. Deixe as permissões do sistema de arquivos NTFS como foram definidas pelo Robocopy.

    Em computadores que executam o UE-V Agent, atualize a configuração **SettingsStoragePath** para o caminho da Convenção Universal de nomenclatura (UNC) do novo compartilhamento.

    **Tem uma sugestão para UE-V**? Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Tem um problema de UE-V**? Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





