---
title: Migrando pacotes de configurações do UE-V
description: Migrando pacotes de configurações do UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799226"
---
# Migrando pacotes de configurações do UE-V


No ciclo de vida de uma implantação do Microsoft User Experience Virtualization (UE-V), talvez seja necessário realocar os pacotes de configurações do usuário ao migrar para um novo servidor ou para fins de backup. A migração de pacotes de configurações pode ser necessária nos seguintes cenários:

-   Atualização do hardware do servidor existente para um servidor mais moderno.

-   Migração de um local de armazenamento de configurações compartilhar de um laboratório para um servidor de produção.

Basta copiar os arquivos e as pastas não preservará as permissões e as configurações de segurança. As etapas descritas a seguir copiarão corretamente os arquivos de pacote de configurações com suas permissões de NTFS para um novo compartilhamento.

**Como preservar pacotes de configurações do UE-V ao migrar para um novo servidor**

1.  Em um novo local em um servidor diferente, crie uma nova pasta; por exemplo, MySettings.

2.  Desabilite o compartilhamento para o compartilhamento de pasta antiga no servidor antigo.

3.  Mova os pacotes de configurações existentes para o novo servidor com Robocopy na linha de comando. Por exemplo:

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Observação**  Para monitorar o progresso da cópia, abra MySettings.txt com um leitor de arquivo de log, como Trace32.

     

4.  Conceda permissões no nível do compartilhamento para o novo compartilhamento. Deixe as permissões de NTFS como foram definidas pelo Robocopy.

    Em computadores que executam o UE-V Agent, atualize a configuração SettingsStoragePath para o caminho UNC do novo compartilhamento.

## Tópicos relacionados


[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





