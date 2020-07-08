---
title: Como alterar o tamanho do cache e a designação da letra da unidade
description: Como alterar o tamanho do cache e a designação da letra da unidade
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797245"
---
# Como alterar o tamanho do cache e a designação da letra da unidade


Você pode alterar o tamanho do cache e a designação da letra da unidade diretamente do nó do **Application Virtualization** no console de gerenciamento do cliente do Application Virtualization.

**Observação**  
Após o tamanho do cache ter sido definido, ele não pode ser menor.



**Para alterar o tamanho do cache**

1.  Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.

2.  Selecione a guia **sistema de arquivos** na caixa de diálogo **Propriedades** . Na seção **configurações de configuração de cache do cliente** , clique em um dos seguintes botões de opção para escolher como gerenciar o espaço do cache:

    **Importante**  
    Se você selecionar a configuração de **limite de espaço livre em disco** , o valor inserido definirá o tamanho do cache para o tamanho total do disco menos o limite de espaço livre em disco que você inseriu. Se, em seguida, você quiser reverter usando a configuração de **tamanho máximo do cache** , especifique um número maior do que o tamanho do cache existente. Caso contrário, o erro "novo tamanho deve ser maior do que o tamanho do cache existente" será exibido.



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Clique em **OK** ou **aplicar** para alterar a configuração.

**Para alterar a designação da letra da unidade**

1.  Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.

2.  Na guia **sistema de arquivos** na caixa de diálogo **Propriedades** , no campo **unidade a ser usado** , selecione a letra da unidade desejada na lista suspensa de letras de unidade disponíveis. Essa configuração torna-se efetiva quando o computador é reinicializado.

3.  Clique em **OK** ou **aplicar** para alterar a configuração.

## Tópicos relacionados


[Como configurar o Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









