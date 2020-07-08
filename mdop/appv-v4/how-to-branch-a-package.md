---
title: Como ramificar um pacote
description: Como ramificar um pacote
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797263"
---
# Como ramificar um pacote


Use este procedimento para modificar um pacote de aplicativo sequenciado existente para que você possa executá-lo lado a lado com o pacote de aplicativo sequenciado original. Esse processo é chamado de ramificação. Ao ramificar um pacote de aplicativo virtual, você pode executar duas versões do mesmo pacote. Por exemplo, você pode aplicar um Service Pack a um pacote existente e executá-lo lado a lado com o pacote de aplicativo virtual sequenciado original.

Use o procedimento a seguir para ramificar um pacote de aplicativo virtual sequenciado.

**Para ramificar um pacote de aplicativo virtual sequenciado**

1.  Abra o sequenciador do Microsoft Application Virtualization (App-V). Para especificar o diretório de destino que contém o pacote (. sprj) que você deseja ramificar selecionar **arquivo**, **abra**.

2.  Navegue até o diretório que contém o aplicativo sequenciado que você planeja ramificar e clique em **abrir**.

3.  Para salvar uma cópia do pacote, na sequência App-V, selecione **arquivo**, **salvar como**. Especifique um novo nome exclusivo e especifique um novo diretório raiz exclusivo do pacote para a cópia do pacote. Clique em **Salvar**.

    **Importante**  
    Você deve especificar um novo nome de pacote ou substituirá a versão existente do pacote.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. Depois de salvar a nova versão, você pode aplicar as alterações de configuração necessárias e salvar os arquivos ICO, OSD, SFT e SPRJ associados para corrigir o local no servidor do Application Virtualization (App-V).

## Tópicos relacionados


[Tarefas para o Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









