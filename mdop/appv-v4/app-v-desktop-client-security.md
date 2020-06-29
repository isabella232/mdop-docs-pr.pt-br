---
title: Segurança do cliente da área de trabalho do App-V
description: Segurança do cliente da área de trabalho do App-V
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799048"
---
# Segurança do cliente da área de trabalho do App-V


O cliente da área de trabalho do App-V fornece muitos aprimoramentos de segurança que não estavam disponíveis nas versões anteriores do produto. Essas alterações fornecem níveis mais altos de segurança por padrão e por meio da configuração das configurações do cliente.

**Observação**  Quando você instala o cliente da área de trabalho do App-V em um computador, o software é definido como padrão para as configurações mais seguras. No entanto, ao atualizar, as configurações anteriores do cliente persistem.

 

Por padrão, o cliente da área de trabalho App-V é configurado somente com as permissões necessárias para permitir que um usuário não administrativo execute uma atualização de publicação e aplicativos de fluxo. Aprimoramentos de segurança adicionais fornecidos no cliente da área de trabalho do App-V incluem o seguinte:

-   Por padrão, uma atualização de cache OSD é permitida apenas pelo processo de atualização de publicação.

-   O arquivo de log ( `sftlog.txt` ) só pode ser acessado por contas com acesso administrativo local ao cliente.

-   O arquivo de log agora tem um tamanho máximo.

-   Os arquivos de log são gerenciados por meio das configurações de arquivo.

-   O log de eventos do sistema agora é executado.

## Permissões


Depois de instalar o cliente de desktop, você pode definir outras configurações de segurança por meio do MMC ou de um cliente individual usando o registro ou o modelo ADM fornecido pela Microsoft. O cliente da área de trabalho App-V tem permissões que você pode definir para restringir o acesso de usuários não administrativos a todos os recursos do cliente da área de trabalho. Para obter uma lista completa de permissões, consulte o arquivo de ajuda do App-V Client ou o App-V Operations Guide.

**Importante**  Considere cuidadosamente as conseqüências da alteração dos direitos de acesso, especialmente em sistemas que são compartilhados por vários usuários, como servidores de terminal.

 

**Observação**  Se os usuários no ambiente tiverem privilégios de administrador local para seus computadores, as permissões serão ignoradas.

 

### Modelo ADM

O Microsoft Application Virtualization (App-V) introduz um modelo ADM que você pode usar para definir as configurações de cliente mais comuns por meio de políticas de grupo. Este modelo permite que os administradores implementem e alterem muitas das configurações do cliente por meio de um modelo de administração centralizado. Algumas das configurações disponíveis no modelo ADM são configurações de segurança.

**Importante**  Ao usar o modelo ADM, lembre-se de que as configurações são configurações de preferência de política de grupo e não diretivas de grupo totalmente gerenciadas.

 

Para obter uma descrição completa do modelo ADM, as configurações específicas e a orientação para implantar clientes com êxito em seu ambiente, consulte o White Paper App-V ADM template at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .

## Removendo associações de tipo de arquivo OSD


Se a sua organização não exigir que os usuários abram aplicativos diretamente de um arquivo OSD, você pode melhorar a segurança removendo associações de tipo de arquivo no cliente. Remova as `HKEY_CURRENT_USERS` chaves para OSD e `Softgird.osd.file` use o editor de registro. Você pode colocar esse processo em um script de logon ou em um script de pós-instalação para automatizar essas alterações.

 

 





