---
title: Componentes adicionais do pacote de aplicativo virtual
description: Componentes adicionais do pacote de aplicativo virtual
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796653"
---
# Componentes adicionais do pacote de aplicativo virtual


O sequenciador App-V detectou um diretório que contém arquivos executáveis de 64 bits e 32 bits e/ou biblioteca de vínculo dinâmico (. dll) que dependem do mesmo assembly lado a lado. Geralmente, o sequenciador cria assemblies lado a lado privados para todos os assemblies públicos que são usados pelo pacote; no entanto, não é possível criar versões de 32 bits e de 64 bits dos assemblies particulares no mesmo diretório.

Se o sequenciador detectar um único conflito, ele irá executar as seguintes ações:

-   Remova todos os assemblies particulares de 64 bits existentes em todo o pacote, independentemente de o diretório ter ou não conflito.

-   Crie somente versões de 32 bits dos conjuntos lado a lado privados.

Você deve instalar nativamente as versões públicas de todos os assemblies de 64 bits necessários no computador que executa o sequenciador e em todos os computadores cliente do App-V.

Para localizar os assemblies públicos existentes necessários, abra o diretório onde o pacote foi salvo e procure na pasta **VFS** . Por exemplo, se a raiz do pacote for **Q:\\MyApp**, quando você sequenciar o aplicativo, procure em **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** e localize todos os assemblies públicos existentes. As versões de 64 bits desses arquivos sempre serão iniciadas com o seguinte texto no início do nome do manifesto: **AMD64...**. O nome exato e a versão do assembly podem ser encontrados no arquivo de manifesto associado.

Use qualquer um dos links a seguir para baixar e instalar a versão correta dos pré-requisitos obrigatórios:

-   [Pacote redistribuível do Microsoft Visual C++ 2005 (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Pacote redistribuível do Microsoft Visual C++ 2005 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Pacote redistribuível do Microsoft Visual C++ 2008 (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Pacote redistribuível do Microsoft Visual C++ 2008 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





