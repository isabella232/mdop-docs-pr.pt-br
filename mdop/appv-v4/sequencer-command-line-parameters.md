---
title: Parâmetros de linha de comando do Sequencer
description: Parâmetros de linha de comando do Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796748"
---
# Parâmetros de linha de comando do Sequencer


Você pode usar os seguintes parâmetros do sequenciador do Application Virtualization (App-V) para sequenciar um aplicativo e atualizar um aplicativo virtual existente usando uma linha de comando. Para obter mais informações sobre como sequenciar um aplicativo usando uma linha de comando, consulte [como sequenciar um novo aplicativo usando a linha de comando](how-to-sequence-a-new-application-by-using-the-command-line.md).

## Parâmetros de linha de comando do Sequencer


<a href="" id="-help-or---"></a>**/HELP ou/?**  
Exibe informações sobre os parâmetros que estão disponíveis para usar uma linha de comando para sequenciar aplicativos.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE ou/I**  
Especifica o Windows Installer ou um arquivo em lotes que será usado para instalar um aplicativo para que ele possa ser sequenciado.

<a href="" id="-installpath-or--p"></a>**/INSTALLPATH ou/P**  
Especifica o diretório raiz do pacote para um aplicativo.

<a href="" id="-outputfile-or--o"></a>**/OUTPUTFILE ou/O**  
Especifica o caminho e o nome do arquivo SPRJ que será gerado.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD ou/F**  
Especifica se todos os arquivos estarão contidos no bloco de recursos principal. Se o parâmetro **/FULLLOAD** for especificado na linha de comando, todos os dados de aplicativo associados serão adicionados ao bloco de recursos principal. Se o parâmetro **/FULLLOAD** não for especificado na linha de comando, nenhum dos dados do aplicativo associado será adicionado ao bloco de recursos principal.

<a href="" id="-packagename-or--k"></a>**/PACKAGENAME ou/K**  
Especifica o nome do pacote que será atribuído ao aplicativo sequenciado.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
Especifica o tamanho do bloco de arquivos SFT que será usado para transmitir o pacote para os computadores cliente. Você pode selecionar um dos seguintes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Você deve considerar o tamanho do arquivo SFT ao especificar o tamanho do bloco. Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda. Arquivos com tamanhos de blocos maiores usam mais largura de banda de rede.

<a href="" id="-compression"></a>**/COMPRESSION**  
Especifica o método para compactar o arquivo SFT que será transmitido ao cliente.

<a href="" id="-msi-or--m"></a>**/MSI ou/M**  
Especifica se um instalador do Windows para o aplicativo sequenciado deve ser criado.

<a href="" id="-default"></a>**/DEFAULT**  
Especifica o arquivo SPRJ padrão que será usado ao criar um pacote de aplicativo virtual. Esse arquivo é usado como o modelo. sprj quando o aplicativo é sequenciado pela primeira vez.

<a href="" id="-upgrade"></a>**/UPGRADE**  
Especifica o caminho e o nome do arquivo SPRJ que será atualizado.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
Especifica o diretório no computador de sequenciamento em que os arquivos associados ao pacote de aplicativo sequenciado são instalados. Use um dos seguintes formatos ao especificar o diretório:

-   /DECODEPATH: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /DECODEPATH: "p:"

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Códigos de erro de linha de comando do Sequencer](sequencer-command-line-error-codes.md)

 

 





