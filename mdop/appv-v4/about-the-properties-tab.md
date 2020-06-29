---
title: Sobre a guia Propriedades
description: Sobre a guia Propriedades
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797622"
---
# Sobre a guia Propriedades


Use a guia **Propriedades** para exibir informações estatísticas básicas sobre um pacote de aplicativo sequenciado. As informações são geradas automaticamente, a menos que indicado de outra forma. Esta guia contém os elementos a seguir.

## Informações do pacote


<a href="" id="package-name"></a>**Nome do pacote**  
O nome único usado para um pacote de aplicativo sequenciado que pode conter um ou mais aplicativos — por exemplo, o Microsoft Office pode ser usado para rotular um pacote de aplicativo sequenciado que contém aplicativos Microsoft Word e Microsoft Excel que são executados no mesmo ambiente virtual.

<a href="" id="comments"></a>**Comentários**  
Exibe uma breve descrição do pacote de software que será exibido no elemento ABSTRACT do arquivo OSD (Open Software Descriptor). Este item é opcional.

<a href="" id="package-version"></a>**Versão do pacote**  
A versão do pacote do aplicativo sequenciado.

<a href="" id="package-guid"></a>**GUID do pacote**  
O identificador global exclusivo (GUID) atribuído automaticamente ao pacote do aplicativo sequenciado para distingui-lo de outros pacotes de aplicativo sequenciados que podem estar em execução no computador para o qual um pacote de aplicativo sequenciado é transmitido.

<a href="" id="package-version-guid"></a>**GUID de versão do pacote**  
O GUID da versão do pacote do aplicativo sequenciado.

<a href="" id="root-directory"></a>**Diretório raiz**  
O diretório no computador de sequenciamento em que os arquivos do pacote do aplicativo sequenciado são instalados. Esse diretório também é criado no computador para o qual um pacote de aplicativo sequenciado será transmitido. É recomendado para compatibilidade com versões anteriores, que é um nome de diretório de formato do 8,3 na raiz da unidade Q, como Q:\\MyApp.1\\.

<a href="" id="created"></a>**Criado**  
A data e a hora em que o pacote do aplicativo sequenciado foi criado.

<a href="" id="modified"></a>**Modificação em**  
A data e a hora em que o pacote do aplicativo sequenciado foi modificado pela última vez.

<a href="" id="package-size"></a>**Tamanho do pacote**  
O tamanho do pacote em megabytes.

<a href="" id="launch-size"></a>**Tamanho do lançamento**  
O tamanho em megabytes da parte do arquivo SFT que é necessário para iniciar o aplicativo.

## Parâmetros de sequenciamento


<a href="" id="block-size"></a>**Tamanho do bloco**  
Especifica o tamanho dos blocos de recursos primário e secundário para os quais o arquivo SFT é dividido para streaming em uma rede. Todos os blocos são iguais ao tamanho especificado; no entanto, o último bloco pode ser menor do que o especificado. Você verá um dos seguintes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

**Observação**  Após a criação do pacote inicial, o valor do tamanho do bloco não é alterado.

 

## Tópicos relacionados


[Como alterar as propriedades do pacote](how-to-change-package-properties.md)

[Console do Sequencer](sequencer-console.md)

 

 





