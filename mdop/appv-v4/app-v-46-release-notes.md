---
title: Notas de versão do App-V 4.6
description: Notas de versão do App-V 4.6
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799058"
---
# Notas de versão do App-V 4.6


Para pesquisar essas notas de versão, pressione CTRL + F.

**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization (App-V). Estas notas da versão contêm informações de que você precisa para instalar com êxito o Application Virtualization (App-V) 4.6. Este documento contém informações que não estão disponíveis na documentação do produto. Se houver uma discrepância entre essas notas de versão e outras documentações do App-V, a alteração mais recente deve ser considerada autorizada.

 

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte o [site de segurança da Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conhecidos com o Application Virtualization 4.6


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.6. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Sempre que possível, esses problemas serão resolvidos em versões posteriores.

### Erro de carregamento/instalação ao executar um arquivo do Windows Installer gerado pelo App-V 4.5 Sequencer

A execução de um arquivo do Windows Installer gerado pelo sequenciador App-V 4.5 produz um erro de carga/instalação ao tentar executá-lo em um cliente App-V 4,6. Você verá a seguinte mensagem: "Este pacote requer o cliente 4.5 do Microsoft Application Virtualization ou posterior". Use a solução alternativa a seguir.

WORKAROUNDOpen o pacote antigo com o sequenciador do App-V 4,5 SP1 ou o sequenciador do App-V 4,6 e gere um novo arquivo. msi para o pacote.

**Observação**  Como alternativa, no prompt de comando, o sequenciador App-V pode gerar o novo arquivo. msi usando os parâmetros */Open* e */MSI* , por exemplo, `SFTSequencer /Open:”package.sprj” /MSI` . Para obter mais informações, consulte [como atualizar um aplicativo virtual usando a linha de comando](how-to-upgrade-a-virtual-application-by-using-the-command-line.md).

 

### Informações de direitos autorais da versão

Este documento é fornecido "como está". As informações e visualizações apresentadas neste documento, incluindo URL e outras referências a sites, estão sujeitas a alterações sem prévio aviso. Você assume o risco de usá-lo.

Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios.Nenhuma associação ou conexão real é intencional ou deve ser inferida.

Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft. Você pode copiar e usar este documento para fins de referência interna. Você pode modificar esse documento para suas finalidades de referência internas.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.

Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.

 

 





