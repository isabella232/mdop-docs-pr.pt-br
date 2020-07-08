---
title: Parâmetros de linha de comando
description: Parâmetros de linha de comando
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797518"
---
# Parâmetros de linha de comando


Use os seguintes parâmetros do sequenciador do Application Virtualization para sequenciar um aplicativo e para atualizar um pacote de aplicativo sequenciado no prompt de comando. No diretório Microsoft Application Virtualization Sequencer, você digitaria **SFTSequencer**, seguido do parâmetro apropriado.

<a href="" id="-help-or---"></a>*/Help* ou */?*  
Use para exibir a lista de parâmetros disponíveis para o sequenciamento de linha de comando.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* ou */i*  
Use para especificar o instalador ou um arquivo em lotes para o aplicativo ser sequenciado.

<a href="" id="-installpath-or--p"></a>*/InstallPath* ou */p*  
Use para especificar o diretório raiz do pacote.

<a href="" id="-outputfile-or--o"></a>*/OutputFile* ou */o*  
Use para especificar o caminho e o nome do arquivo SPRJ que será gerado.

**Importante**  O parâmetro */OutputFile* não está disponível ao abrir um pacote que você não pretende atualizar.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* ou */f*  
Use para especificar se deseja colocar tudo no bloco de recursos principal.

<a href="" id="-packagename-or--k"></a>*/PackageName* ou */k*  
Use para especificar o nome do pacote do aplicativo sequenciado.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Especifica o tamanho do bloco de arquivos SFT que será usado para transmitir o pacote para os computadores cliente. Você pode selecionar um dos seguintes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Você deve considerar o tamanho do arquivo SFT ao especificar o tamanho do bloco. Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda. Arquivos com tamanhos de blocos maiores usam mais largura de banda de rede.

<a href="" id="-compression"></a>*/COMPRESSION*  
Use para especificar o método para compactar o arquivo SFT conforme ele é transmitido para o cliente.

<a href="" id="-msi-or--m"></a>*/MSI* ou */m*  
Use para especificar a geração de um pacote do Microsoft Windows Installer para o aplicativo sequenciado.

<a href="" id="-default"></a>*/DEFAULT*  
Especifica o arquivo SPRJ padrão que será usado ao criar um pacote de aplicativo virtual. Esse arquivo é usado como o modelo. sprj quando o aplicativo é sequenciado pela primeira vez.

<a href="" id="-upgrade"></a>*/UPGRADE*  
Especifica o caminho e o nome do arquivo SPRJ que será atualizado.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Especifica o diretório no computador de sequenciamento em que os arquivos associados ao pacote de aplicativo sequenciado são instalados. Use um dos seguintes formatos ao especificar o diretório:

-   /DECODEPATH: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /DECODEPATH: "p:"

## Tópicos relacionados


[Sobre como usar a linha de comando do Sequencer](about-using-the-sequencer-command-line.md)

[Como abrir um aplicativo sequenciado usando a linha de comando](how-to-open-a-sequenced-application-using-the-command-line.md)

[Como fazer upgrade de um pacote usando o comando Abrir Pacote](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





