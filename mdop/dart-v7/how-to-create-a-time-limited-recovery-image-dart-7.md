---
title: Como criar uma imagem de recuperação por tempo limitado
description: Como criar uma imagem de recuperação por tempo limitado
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796048"
---
# Como criar uma imagem de recuperação por tempo limitado


Você pode criar uma imagem de recuperação do DaRT que só pode ser usada por um determinado número de dias após a geração. Para fazer isso, você deve executar o **Assistente de imagem de recuperação do DART** em um prompt de comando e especificar o número de dias.

**Para criar uma imagem de recuperação com um limite de tempo**

1.  Abra um prompt de comando com as credenciais de administrador.

2.  Altere o diretório para o local do programa ERDC.exe.

3.  Usando a sintaxe a seguir, execute o **Assistente de recuperação de imagem DART**. *NumberOfDays* é um inteiro positivo que representa o número de dias durante os quais a imagem de recuperação do DART será utilizável.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## Tópicos relacionados


[Criação da imagem de recuperação do DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





