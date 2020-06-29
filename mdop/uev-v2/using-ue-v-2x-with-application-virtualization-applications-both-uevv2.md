---
title: Usar o UE-V 2. x com aplicativos do Application Virtualization
description: Usar o UE-V 2. x com aplicativos do Application Virtualization
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800039"
---
# Usar o UE-V 2. x com aplicativos do Application Virtualization


O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 dão suporte a aplicativos Microsoft Application Virtualization (App-V) sem modificações obrigatórias no pacote do App-V ou no modelo UE-V. No entanto, uma etapa adicional é necessária porque não é possível executar o gerador do UE-V diretamente em um aplicativo virtualizado do V App-V. Em vez disso, você deve instalar o aplicativo localmente, gerar o modelo e, em seguida, aplicar o modelo ao aplicativo virtualizado. O UE-V é compatível com pacotes do App-v 4,5, App-V 4,6 e App-V 5,0.

## Sincronização de configurações do UE-V para aplicativos App-V


O UE-V monitora quando um aplicativo é aberto pelo nome do programa e, opcionalmente, por números de versão do arquivo e números de versão do produto, se o aplicativo é instalado localmente ou virtualmente usando o App-V. Quando o aplicativo é iniciado, o UE-V monitora o processo App-V, aplica todas as configurações armazenadas no caminho de armazenamento de configurações do usuário e, em seguida, permite que o aplicativo inicie normalmente. O UE-V monitora aplicativos do App-V e traduz automaticamente o arquivo relevante e os caminhos do registro para o local virtualizado, em oposição ao local físico fora do ambiente de computação do App-V.

 **Para implementar a sincronização de configurações para um aplicativo virtualizado**

1.  Execute o UE-V Generator para coletar as configurações do aplicativo instalado localmente cujas configurações você deseja sincronizar entre computadores. Esse processo cria um modelo de local de configurações. Se você usar um modelo interno, como o modelo do Microsoft Office 2010, pule esta etapa. Para obter mais informações sobre como executar o UE-V Generator, consulte [implantar o UE-v 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).

2.  Instale o pacote do aplicativo App-V se ainda não tiver feito isso.

3.  Publique o modelo no local do catálogo de modelos de configurações ou instale manualmente o modelo usando o `Register-UEVTemplate` cmdlet do Windows PowerShell.

    **Observação**  Se você publicar o modelo recém-criado no catálogo de modelos de configurações, o cliente não receberá o modelo até que o provedor de sincronização atualize as configurações. Para iniciar manualmente esse processo, abra o **Agendador de tarefas**, expanda **biblioteca do Agendador de tarefas**, expanda **Microsoft**e expanda **UE-V**. No painel de resultados, clique com o botão direito do mouse em **atualização automática de modelo**e clique em **executar**.

     

4.  Inicie o pacote App-V.






## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





