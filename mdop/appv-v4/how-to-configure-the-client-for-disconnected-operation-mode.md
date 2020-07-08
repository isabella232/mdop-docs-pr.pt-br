---
title: Como configurar o cliente para o Modo de Operação Desconectada
description: Como configurar o cliente para o Modo de Operação Desconectada
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797201"
---
# Como configurar o cliente para o Modo de Operação Desconectada


O modo de operação desconectado habilita o cliente de desktop do Application Virtualization (App-V) ou o cliente do Application Virtualization (App-V) para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal) para executar aplicativos armazenados no cache do sistema de arquivos do cliente quando o cliente não consegue se conectar ao servidor de gerenciamento do App-V.

**Importante**  Em uma organização de grande porte em que vários servidores de host de sessão de área de trabalho remota (host de Sessão RD °) (anteriormente chamado de Terminal Server) são vinculados a um farm para dar suporte a muitos usuários, usar um servidor de gerenciamento do App-V único para dar suporte ao farm representa um único ponto de falha. Para fornecer alta disponibilidade para dar suporte ao farm de hosts do RDSession, considere vincular dois ou mais servidores de gerenciamento do App-V para usar o mesmo banco de dados.

 

**Para habilitar o modo de operação desconectado**

-   Defina o seguinte valor da chave do registro igual a 1 para habilitar o modo de operação desconectada:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**Para definir um limite de tempo no modo de operação desconectado, use**

1.  Defina o seguinte valor da chave do registro como 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  Defina o seguinte valor da chave do registro como o número de minutos que você deseja limitar o modo de operação desconectado. O intervalo válido de valores é 1 – 999999. O valor padrão é 90 dias ou 129.600 minutos.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**Configurar o modo de operação cliente para serviços de área de trabalho remota para desconexão**

1.  Defina o seguinte valor da chave do registro como 1 para habilitar o modo de operação desconectada:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  Defina o seguinte valor da chave do registro como 0 (zero) para permitir o uso ilimitado do modo de operação desconectado:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  Certifique-se de que todos os pacotes sejam pré-carregados no cache para melhorar o desempenho.

## Tópicos relacionados


[Modo de Operação Desconectada](disconnected-operation-mode.md)

[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





