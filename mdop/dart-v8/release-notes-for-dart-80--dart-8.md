---
title: Notas de versão do DaRT 8.0
description: Notas de versão do DaRT 8.0
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799542"
---
# Notas de versão do DaRT 8.0


**Para pesquisar essas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

Estas notas da versão contêm informações necessárias para instalar o DaRT 8,0 com êxito. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outra documentação do DaRT, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

Para obter o software DaRT, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).

## Sobre a documentação do produto


Para obter informações sobre a documentação do DaRT, consulte a [Home Page do DART](https://go.microsoft.com/fwlink/?LinkID=252096) no Microsoft TechNet.

Para obter uma cópia disponível para download da documentação DaRT, consulte <https://go.microsoft.com/fwlink/?LinkID=267420> o centro de download da Microsoft.

## Fornecendo comentários


Estamos interessados em seus comentários sobre o DaRT 8,0. Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .

**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar mudanças futuras para nossa documentação e versões de produtos.

 

Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conhecidos com o DaRT 8,0


### A restauração do sistema falha quando você executa o locksmith ou o editor do registro

Se você executar o locksmith, o editor do registro e possivelmente outras ferramentas, a restauração do sistema falhará.

**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie a restauração do sistema.

### A verificação do SFC falha ao ser executada após iniciar e fechar o locksmith ou o gerenciamento do computador

Se você iniciar e fechar as ferramentas de gerenciamento de locksmith ou computador, verificador de arquivos do sistema falha ao executar.

**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie o SFC.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> O instalador do DaRT não falha quando o ADK não foi instalado

Se você instalar o DaRT 8,0 usando a linha de comando para executar o MSI, e o ADK não tiver sido instalado, a instalação do DaRT não será bem-sucedida. Atualmente, o instalador do DaRT 8,0 instala todos os componentes, exceto a imagem de recuperação do DaRT 8,0.

**Solução alternativa:** Nenhuma.

### Não é possível iniciar o defender após a inicialização do locksmith, do RegEdit, do Crash Analyzer e do gerenciamento do computador

O defender não será iniciado se você já tiver iniciado o locksmith, o RegEdit, o Crash Analyzer e o gerenciamento do computador.

**Solução alternativa:** Feche e reinicie o DaRT e inicie o defender.

### O defender pode estar lento para iniciar

O defender às vezes leva alguns minutos para ser iniciado. A barra de progresso indica o status atual de carregamento.

**Solução alternativa:** Nenhuma.

## Informações de direitos autorais da versão


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft. Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.



## Tópicos relacionados


[Sobre o DaRT 8.0](about-dart-80-dart-8.md)

 

 





