---
title: Solução de problemas do Application Virtualization Sequencer
description: Solução de problemas do Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796674"
---
# Solução de problemas do Application Virtualization Sequencer


Este tópico inclui informações que você pode usar para ajudar a solucionar problemas gerais no sequenciador do Application Virtualization (App-V).

## A criação de um arquivo SFTD usando o sequenciador App-V aumenta o número da versão inesperadamente


O número de versão associado a um arquivo SFTD aumenta inesperadamente.

**Solução**

Use a linha de comando para gerar um novo arquivo. SFT. Para criar o arquivo. sft usando a linha de comando, digite o seguinte em um prompt de comando:

**&lt;Nome do arquivo SFT base mkdiffpkg.exe nome do arquivo &gt; &lt; SFT do SFT&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>O nome do arquivo no arquivo OSD não está correto após a atualização do pacote


Depois de atualizar um pacote existente, o nome do arquivo não está correto.

**Solução**

Ao abrir um pacote para atualização, você deve especificar a unidade Q:\\ raiz como o local de saída do pacote. Não especifique um nome de arquivo associado com o local de saída.

## A instalação padrão do Microsoft Word2003 resulta em um erro quando transmitido para um cliente


Quando você transmite o Microsoft Word2003 para um cliente, um erro é retornado, mas o Microsoft Word continua a ser executado.

**Solução**

Resequenciar o pacote de aplicativo virtual e selecionar **instalação completa**.

## A atualização do pacote não funciona quando você cria um pacote dependente


Quando você cria um pacote dependente usando a atualização de pacote e adiciona novas entradas do registro, parece funcionar corretamente, mas as entradas do registro atualizadas não estão disponíveis.

**Solução**

As configurações do registro são sempre armazenadas com a versão original do pacote, portanto, as atualizações para o pacote não parecerão estar disponíveis, a menos que você repare o pacote original.

## Erro ao tentar sequenciar. NET 2.0


Quando você sequenciar um pacote que exija. NET 2.0, você recebe um erro.

**Solução**

Sequenciando pacotes que exigem. Não há suporte para NET 2.0.

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





