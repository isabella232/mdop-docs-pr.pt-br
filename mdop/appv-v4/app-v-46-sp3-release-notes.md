---
title: Notas de versão do App-V 4.6 SP3
description: Notas de versão do App-V 4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797596"
---
# Notas de versão do App-V 4.6 SP3


Para pesquisar essas notas de versão, pressione CTRL + F.

Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization (App-V). Estas notas da versão contêm informações que ajudam você a instalar com êxito o Application Virtualization (App-V) 4.6 SP3. Este documento contém informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do App-V, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte o [site de segurança da Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conhecidos com o Application Virtualization 4.6 SP3


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.6 SP3. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Quando isso for possível, esses problemas serão resolvidos em versões posteriores.

### Não é possível abrir hiperlinks usando o Internet Explorer11 no Microsoft Windows 8,1 no ambiente virtual

A tentativa de abrir hiperlinks dentro de um ambiente virtual falhará no Windows 8,1 usando o Internet Explorer 11. Isso ocorre porque o Internet Explorer 11 agora vem com o modo de proteção avançada (EPM) habilitado por padrão, e isso faz com que o App-V seja incapaz de acessar as chaves de registro, arquivos e objetos de porta de comunicação necessários.

SOLUÇÃO alternativa: desabilite o EPM no Internet Explorer11 antes de abrir um pacote do App-V. Isso permitirá que você abra o Internet Explorer dentro do ambiente virtual.

## Tópicos relacionados


[Sobre o Microsoft Application Virtualization 4.6 SP3](about-microsoft-application-virtualization-46-sp3.md)

 

 





