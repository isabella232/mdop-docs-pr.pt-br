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
# <span data-ttu-id="aaa6a-103">Como criar uma imagem de recuperação por tempo limitado</span><span class="sxs-lookup"><span data-stu-id="aaa6a-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="aaa6a-104">Você pode criar uma imagem de recuperação do DaRT que só pode ser usada por um determinado número de dias após a geração.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="aaa6a-105">Para fazer isso, você deve executar o **Assistente de imagem de recuperação do DART** em um prompt de comando e especificar o número de dias.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="aaa6a-106">Para criar uma imagem de recuperação com um limite de tempo</span><span class="sxs-lookup"><span data-stu-id="aaa6a-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="aaa6a-107">Abra um prompt de comando com as credenciais de administrador.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="aaa6a-108">Altere o diretório para o local do programa ERDC.exe.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="aaa6a-109">Usando a sintaxe a seguir, execute o **Assistente de recuperação de imagem DART**.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="aaa6a-110">*NumberOfDays* é um inteiro positivo que representa o número de dias durante os quais a imagem de recuperação do DART será utilizável.</span><span class="sxs-lookup"><span data-stu-id="aaa6a-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="aaa6a-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aaa6a-111">Related topics</span></span>


[<span data-ttu-id="aaa6a-112">Criação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="aaa6a-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





