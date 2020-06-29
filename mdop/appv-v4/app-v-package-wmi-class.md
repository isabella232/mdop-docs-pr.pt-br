---
title: Classe WMI de pacote do App-V
description: Classe WMI de pacote do App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797597"
---
# Classe WMI de pacote do App-V


No cliente do Application Virtualization (App-V), a classe **Package** é uma classe WMI (Instrumentação de gerenciamento do Windows) que representa todos os pacotes virtuais no cliente. Os pacotes virtuais podem conter muitos aplicativos virtuais.

## Sintaxe


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Propriedades


<a href="" id="name"></a>**Nome**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O nome de usuário amigável do pacote virtual.

<a href="" id="version"></a>**Versão**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

A versão do pacote virtual.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: chave

O identificador de GUID dos arquivos de origem e de configuração do pacote.

<a href="" id="sftpath"></a>**SftPath**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O caminho do arquivo SFT.

<a href="" id="totalsize"></a>**TotalSize**  
Tipo de dados: **UInt64**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O tamanho total do pacote virtual, em quilobytes.

<a href="" id="cachedsize"></a>**CachedSize**  
Tipo de dados: **UInt64**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O tamanho total do cache do pacote virtual, em quilobytes.

<a href="" id="launchsize"></a>**LaunchSize**  
Tipo de dados: **UInt64**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O tamanho total do bloco de recursos principal do pacote virtual, em quilobytes.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Tipo de dados: **UInt64**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O tamanho total do bloco de recursos primário do pacote virtual que foi armazenado em cache, em kilobytes.

<a href="" id="inuse"></a>**InUse**  
Tipo de dados: **booliano**

Tipo de acesso: somente leitura

Qualificadores: nenhum

**true** se algum aplicativo virtual do pacote virtual estiver em execução; caso contrário, **false**.

<a href="" id="locked"></a>**Bloqueado**  
Tipo de dados: **booliano**

Tipo de acesso: somente leitura

Qualificadores: nenhum

**verdadeiro** se o pacote virtual estiver bloqueado; caso contrário, **false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Tipo de dados: **UInt16**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O percentual dos arquivos de cache. Com base na fórmula a seguir: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Tipo de dados: **cadeia de caracteres**

Tipo de acesso: somente leitura

Qualificadores: nenhum

O identificador de GUID da versão do pacote.

 

 





