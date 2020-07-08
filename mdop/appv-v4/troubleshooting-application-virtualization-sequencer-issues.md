---
title: Solução de problemas do Application Virtualization Sequencer
description: Solução de problemas do Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796686"
---
# Solução de problemas do Application Virtualization Sequencer


Este tópico inclui informações que você pode usar para ajudar a solucionar problemas gerais no sequenciador do Application Virtualization (App-V).

## A criação de um arquivo SFTD usando o sequenciador App-V aumenta o número da versão inesperadamente


Use a linha de comando para gerar um novo arquivo. SFT. Para criar o arquivo. sft usando a linha de comando, digite o seguinte em um prompt de comando:

**&lt;Nome do arquivo SFT base mkdiffpkg.exe nome do arquivo &gt; &lt; SFT do SFT&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>O nome do arquivo no arquivo OSD não está correto após a atualização do pacote


Ao abrir um pacote para atualização, você deve especificar a unidade Q:\\ raiz como o local de saída do pacote. Não especifique um nome de arquivo associado com o local de saída.

## A instalação padrão do Microsoft Word2003 resulta em um erro quando transmitido para um cliente


Quando você transmite o Microsoft Word2003 para um cliente, um erro é retornado, mas o Microsoft Word continua a ser executado.

**Solução**

Resequenciar o pacote de aplicativo virtual e selecionar **instalação completa**.

## A atualização ativa não funciona quando você cria um pacote dependente


Quando você cria um pacote dependente usando a atualização ativa e adiciona novas entradas do registro, parece funcionar corretamente, mas as entradas do registro atualizadas não estão disponíveis.

**Solução**

As configurações do registro são sempre armazenadas com a versão original do pacote, portanto, as atualizações para o pacote não parecerão estar disponíveis, a menos que você repare o pacote original.

## Informações detalhadas não estão visíveis para documentos do Microsoft Office2007 usando a página Propriedades


Quando você tenta exibir informações detalhadas associadas a um documento do Microsoft Office2007 usando a página Propriedades, as informações detalhadas não ficam visíveis.

**Solução**

O App-V não oferece suporte às extensões Shell necessárias para essas páginas de propriedades.

## Algumas chaves do registro não são capturadas quando você sequencia aplicativos de 16 bits


No App-V 4,5, o gancho do registro foi movido do modo kernel para o modo de usuário. Se quiser sequenciar um aplicativo de 16 bits ou um aplicativo que usa um instalador de 16 bits, você deve primeiro configurar o computador do sequenciador para que o processo seja executado em sua própria cópia do computador de DOS virtual do Windows NT (NTVDM).

**Solução**

Antes de sequenciar o aplicativo, defina o seguinte valor da chave do registro global REGSZ como "Sim" no computador de sequenciamento:

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

Você deve reiniciar o computador para que ele tenha efeito.

## Tópicos relacionados


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





