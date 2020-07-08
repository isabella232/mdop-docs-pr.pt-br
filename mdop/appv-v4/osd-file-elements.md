---
title: Elementos de arquivo OSD
description: Elementos de arquivo OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796859"
---
# Elementos de arquivo OSD


O diretório de instalação do sequenciador contém um arquivo de esquema XML, **Softricity. xsd**, que define a estrutura válida de um arquivo de descritor de software aberto (OSD). Veja a seguir alguns dos elementos OSD usados com mais frequência.

<a href="" id="softpkg"></a>SOFTPKG  
O elemento raiz do arquivo OSD que contém todos os elementos que definem o pacote do software.

<a href="" id="codebase"></a>CÓDIGO  
Informações sobre o arquivo. SFT para este pacote, incluindo os atributos HREF, FILENAME e GUID. Você pode editar o atributo HREF se alterar o ponto de distribuição desse pacote específico.

<a href="" id="os"></a>SO  
Define em quais sistemas operacionais esse aplicativo pode ser executado com base em valores definidos inicialmente no assistente de sequenciamento. Esse valor pode conter apenas os valores definidos em **Softricity. xsd**.

<a href="" id="local-interaction-allowed"></a>LOCAL \ _INTERACTION \ _ALLOWED  
Definido como verdadeiro, permite a criação de objetos nomeados (eventos, exclusões mútuas, semáforos, mapeamentos de arquivos e processadores de aplicativos no namespace global, em vez de serem isolados dentro de um ambiente virtual específico, o que permite que os aplicativos virtuais interajam com os aplicativos do sistema operacional do host.

Exemplo: &lt; implementação do SOFTPKG &gt; &lt;&gt;

&lt;políticas de VIRTUALENV &gt; &lt;&gt;

&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; verdadeiro

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;

&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>RELAÇÃO  
Define a composição do pacote dinâmico (dependências em outros pacotes) usando uma marca CODEBASE de outro pacote.

Exemplo: &lt; dependências &gt; &lt; codebase href = "RTSPS://Server/Package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" Size = "6572748" Mandatory = "false"/ &gt; &lt; /Dependencies&gt;

<a href="" id="package-name"></a>NOME DO PACOTE  
Um nome comum para o pacote inserido na página **informações do pacote** do assistente de sequenciamento, que permite que você especifique um único nome usado para um aplicativo sequenciado contendo vários aplicativos.

<a href="" id="title"></a>LHE  
Nome descritivo opcional do aplicativo que você está sequenciando.

<a href="" id="abstract"></a>ABSTRAIR  
Descrição resumida do pacote de software inserido no campo **comentários** na página **informações do pacote** do assistente de sequenciamento. Uma prática recomendada é especificar informações como o sistema operacional e o nível de Service Pack da estação de trabalho do sequenciador, a versão do sequenciador e o nome do engenheiro de sequenciamento.

<a href="" id="script"></a>SOBRESCRITO  
Define eventos com script específicos para ocorrer durante a inicialização, o desligamento ou o streaming.

<a href="" id="mgmt-shortcutlist"></a>GERENCIAMENTO \ _SHORTCUTLIST  
Lista de todos os atalhos definidos no assistente.

<a href="" id="mgmt-fileassociations"></a>GERENCIAMENTO \ _FILEASSOCIATIONS  
Lista de tipos de arquivo especificados no assistente.

## Tópicos relacionados


[Sobre a guia OSD](about-the-osd-tab.md)

 

 





