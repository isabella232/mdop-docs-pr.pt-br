---
title: Sobre como usar a linha de comando do Sequencer
description: Sobre como usar a linha de comando do Sequencer
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797618"
---
# Sobre como usar a linha de comando do Sequencer


Você pode usar a linha de comando para criar pacotes de aplicativos sequenciados. Usar a linha de comando para criar aplicativos virtuais é útil nos seguintes cenários:

-   Você precisa criar um grande número de pacotes de aplicativos sequenciados.

-   Você precisa criar um pacote de aplicativo sequenciado em uma base recorrente.

**Importante**  O sequenciamento no prompt de comando permite somente o sequenciamento padrão. Se precisar alterar os parâmetros de sequenciamento padrão, você deve modificar manualmente um pacote de aplicativo sequenciado ou resequenciar o aplicativo.

 

Todas as modificações subsequentes em pacotes de aplicativos sequenciados existentes devem ser feitas usando o assistente de sequenciamento.

## Pré-requisitos


Para sequenciar um aplicativo usando o prompt de comando, as seguintes condições devem ser atendidas:

-   O aplicativo que está prestes a ser sequenciado não deve exigir alterações ou soluções alternativas feitas a ele fora do instalador ou do pacote do Windows Installer.

-   Antes de sequenciamento, você deve preparar uma lista de arquivos em lotes para criar pacotes de aplicativos sequenciados.

-   Revise para obter mais informações sobre os parâmetros de linha de comando, consulte [parâmetros de linha de comando](command-line-parameters.md).

-   Revise os erros que podem ser exibidos ao criar um pacote de aplicativo sequenciado usando a linha de comando. Para obter mais informações, consulte esses erros, consulte [erros de linha de comando](command-line-errors.md).

## Tópicos relacionados


[Como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





