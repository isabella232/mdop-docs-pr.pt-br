---
title: Classe WMI de aplicativo do App-V
description: Classe WMI de aplicativo do App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799049"
---
# Classe WMI de aplicativo do App-V


No cliente do Application Virtualization (App-V), a classe **Application** é uma classe WMI (Instrumentação de gerenciamento do Windows) que representa todos os aplicativos virtuais do cliente.

A sintaxe a seguir é simplificada do código MOF (formato de objeto gerenciado). O código inclui todas as propriedades herdadas.

## Sintaxe


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Requisitos


## Propriedades


<a href="" id="name"></a>**Nome**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: chave

O nome de exibição do aplicativo virtual.

<a href="" id="version"></a>**Versão**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: chave

A versão do aplicativo virtual.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O GUID do pacote ao qual o aplicativo virtual está associado.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Tipo de dados: **DateTime**

Tipo de acesso: somente leitura

Qualificadores: nenhum

A última data e hora em que o aplicativo virtual foi iniciado.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Tipo de dados: **UInt32**

Tipo de acesso: somente leitura

Qualificadores: nenhum

Uma contagem das instâncias em execução do aplicativo virtual que foram iniciadas diretamente.

<a href="" id="loading"></a>**Carregando**  
Tipo de dados: **booliano**

Tipo de acesso: somente leitura

Qualificadores: nenhum

**verdadeiro** se o aplicativo virtual estiver sendo iniciado; caso contrário, **false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O caminho de arquivo original do arquivo OSD que foi registrado com o cliente App-V.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O caminho do arquivo OSD se o cliente App-V tiver armazenado em cache o arquivo OSD localmente.

 

 





