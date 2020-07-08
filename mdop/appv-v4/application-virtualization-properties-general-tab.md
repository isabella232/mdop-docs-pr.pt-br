---
title: Guia geral de propriedades da virtualização de aplicativos
description: Guia geral de propriedades da virtualização de aplicativos
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797575"
---
# Propriedades do Application Virtualization: guia Geral


Use a guia **geral** da caixa de diálogo **Propriedades do Application Virtualization** para modificar as configurações de log e locais de dados.

Esta guia contém os elementos a seguir.

<a href="" id="log-level"></a>**Nível de log**  
Selecione o nível na lista suspensa. O nível padrão é **informações**.

<a href="" id="reset-log"></a>**Redefinir log**  
Clique neste botão para fazer backup do arquivo de log atual e iniciar imediatamente um novo arquivo de log.

<a href="" id="location"></a>**Localização**  
Digite ou navegue até o local onde você deseja salvar o arquivo de log sftlog.txt. Os locais padrão são os seguintes:

-   Para WindowsXP, Windows Server2003-*C:\\Documents e Settings\\All Users\\Application cliente de virtualização do Data\\Microsoft\\Application*

-   Para Windows Vista, Windows 7, Windows Server2008 —*cliente de virtualização C:\\ProgramData\\Microsoft\\Application*

<a href="" id="system-log-level"></a>**Nível de log do sistema**  
Selecione o nível na lista suspensa. O nível padrão é **aviso**.

**Observação**  A configuração de **nível de log do sistema** controla o nível de mensagens enviadas ao log de eventos do sistema. As mensagens registradas são idênticas às mensagens que são registradas no log de eventos do cliente, mas elas são armazenadas em um local diferente, que não tem as limitações de espaço do log de eventos do cliente. Como o log de eventos do sistema não tem limitações de espaço, ele é ideal para situações em que o registro em log detalhado é necessário.

 

<a href="" id="global-data-directory"></a>**Diretório de dados globais**  
Digite ou navegue até o local do diretório do arquivo de log. Os locais padrão são os seguintes:

-   Para WindowsXP, Windows Server2003-*C:\\Documents e Settings\\All Users\\Application cliente de virtualização do Data\\Microsoft\\Application*

-   Para Windows Vista, Windows 7, Windows Server2008 —*cliente de virtualização C:\\ProgramData\\Microsoft\\Application*

<a href="" id="user-data-directory"></a>**Diretório de dados do usuário**  
Digite ou navegue até o local do diretório onde os dados específicos do usuário estão armazenados. O padrão é% APPDATA%. Esse caminho deve ser uma variável de ambiente válida no computador cliente.

## Tópicos relacionados


[Client Management Console: propriedades do Application Virtualization](client-management-console-application-virtualization-properties.md)

 

 





