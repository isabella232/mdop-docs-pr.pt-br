---
title: Interoperabilidade do App-V com o Windows AppLocker
description: Interoperabilidade do App-V com o Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799047"
---
# Interoperabilidade do App-V com o Windows AppLocker


A versão 4,5 SP1 do cliente do Microsoft Application Virtualization (App-V) oferece suporte ao recurso AppLocker do Windows 7. O recurso AppLocker permite que os administradores de ti especifiquem quais aplicativos estão impedidos de serem executados em computadores. Este documento descreve como configurar as regras do AppLocker para trabalhar com o ambiente virtual do App-V e aplicativos virtualizados.

**Observação**  O Windows AppLocker deve ser habilitado primeiro antes da configuração de regras do Windows AppLocker para aplicativos virtuais. Para obter mais informações sobre como habilitar o Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Configurando regras do Windows AppLocker para aplicativos virtuais


Os administradores locais podem criar regras do Windows AppLocker que restringem a execução de executáveis de programa (arquivos. exe), arquivos do Windows Installer (arquivos. msi e. msp) e scripts (arquivos. PS,. bat,. cmd,. vbs e. js). O administrador faz isso usando um computador de referência que tenha o cliente App-V instalado e que tenha todos os aplicativos virtuais relevantes transmitidos para o cache do cliente. Em seguida, o administrador usa a seção Windows AppLocker do snap-in console de gerenciamento da Microsoft (MMC) da política de segurança local no computador de referência para criar as regras.

Ao navegar para localizar um caminho de diretório ou arquivo específico para o qual você deseja criar uma regra, você pode acessar a unidade App-V usando o caminho para o compartilhamento oculto. Por exemplo, você pode navegar até \\\\localhost\\Q $, onde a unidade App-V é a unidade Q. No entanto, para criar a regra, você deve editar o caminho para remover a referência a \\\\localhost\\Q $ e usar Q:\\ em vez disso. Você deve iniciar cada aplicativo no computador de referência para acessar os arquivos do aplicativo, e os direitos administrativos são necessários para navegar até \\\\localhost\\Q $.

 

 





