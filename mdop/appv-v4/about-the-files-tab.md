---
title: Sobre a guia Arquivos
description: Sobre a guia Arquivos
author: dansimp
ms.assetid: 3c20e720-4b0f-465b-b7c4-3013dae1c815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e71cd0b60f9722da9736fc6987100f5c7bf53ab
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797623"
---
# Sobre a guia Arquivos


A guia **arquivos** exibe a lista completa de arquivos que estão incluídos em um pacote de aplicativo sequenciado. O painel esquerdo é exibido em um formato de pesquisa de arquivo padrão, a lista completa de arquivos no pacote que foi criada durante o sequenciamento do aplicativo. Esses arquivos incluem o diretório raiz do pacote (o diretório especificado durante a fase de instalação do aplicativo), a pasta sistema de arquivos virtual (VFS) e os arquivos de ambiente virtual. O painel à direita exibe o nome do arquivo, os atributos do arquivo e os atributos do sequenciador.

## Nome do arquivo e nome curto


<a href="" id="file-name"></a>**Nome do arquivo**  
O nome do arquivo está no painel esquerdo. Os arquivos exibidos no painel esquerdo são criados durante o sequenciamento.

<a href="" id="short-name"></a>**Nome Curto**  
Esse é o nome de um arquivo selecionado no painel esquerdo, escrito na Convenção de nomenclatura de formato 8,3.

## Atributos de arquivo


<a href="" id="file-size"></a>**Tamanho do arquivo**  
O tamanho do arquivo em bytes.

<a href="" id="file-version"></a>**Versão do arquivo**  
A versão do arquivo selecionado.

<a href="" id="date-created"></a>**Data de Criação**  
A data e a hora em que o arquivo selecionado foi criado.

<a href="" id="date-modified"></a>**Data da modificação**  
A data e a hora em que o arquivo selecionado foi modificado pela última vez.

<a href="" id="file-id"></a>**ID de Arquivo**  
O GUID do arquivo.

## Atributos do sequenciador


<a href="" id="user-data"></a>**Dados do usuário**  
Selecione esse atributo para especificar que um aplicativo deve reter as informações de um usuário individual.

<a href="" id="application-data"></a>**Dados do aplicativo**  
Selecione este atributo para especificar que um aplicativo deve reter as informações gerais de um grupo de usuários.

<a href="" id="override"></a>**Substituição**  
Quando selecionado, o cliente da área de trabalho do Application Virtualization substitui o arquivo correspondente quando o pacote do aplicativo sequenciado é atualizado e transmitido para o cliente. Se essa caixa de seleção não estiver marcada, o cliente determina se o arquivo selecionado deve ou não ser substituído.

## Tópicos relacionados


[Como modificar os arquivos incluídos em um pacote](how-to-modify-the-files-included-in-a-package.md)

[Console do Sequencer](sequencer-console.md)

 

 





