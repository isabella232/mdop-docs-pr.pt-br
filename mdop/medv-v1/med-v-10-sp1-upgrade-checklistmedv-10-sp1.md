---
title: Lista de verificação para atualização do MED-V 1.0 SP1
description: Lista de verificação para atualização do MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800038"
---
# Lista de verificação para atualização do MED-V 1.0 SP1


Para atualizar o Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 para o MED-V 1.0 Service Pack1 (SP1), o cliente deve ser atualizado. Opcionalmente, o servidor pode ser atualizado.

## Atualização do servidor


**Para atualizar o servidor MED-V 1.0 para o MED-V 1.0 SP1**

1.  Faça backup dos seguintes arquivos localizados no diretório * &lt; installdir &gt; /Servers/ConfigurationServer* :

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Faça backup do arquivo * &lt; installdir &gt; /servers/ServerSettings.xml* .

3.  Desinstale o servidor do MED-V 1.0.

4.  Instale o servidor MED-V 1.0 SP1.

5.  Restaure os arquivos de backup para os diretórios apropriados.

6.  Reinicie o serviço do servidor MED-V.

**Observação**  Se a configuração do servidor tiver sido alterada do padrão, os arquivos poderão estar armazenados em um local diferente.

 

## Atualização do cliente


Para atualizar o cliente do MED-V 1.0 para o MED-V 1.0 SP1, instale o arquivo. msp em um cliente MED-V 1.0. O cliente e o MED-V são atualizados automaticamente.

 

 





