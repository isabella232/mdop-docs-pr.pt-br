---
title: Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo
description: Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796346"
---
# Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo


Use o modelo ADMX do Microsoft Application Virtualization (App-V) 5,1 para configurar as definições do aplicativo cliente do App-V 5,1 usando o modelo ADMX e a política de grupo.

**Para modificar a configuração do cliente do App-V 5,1 usando a política de grupo**

1.  Para modificar a configuração do cliente do App-V 5,1, localize os arquivos **admxtemplate** disponíveis com o app-v 5,1.

    **Observação**  Use o link a seguir para baixar os **modelos do ADMX**do App-V 5,1: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  No computador em que você gerencia a política de grupo, normalmente o controlador de domínio, copie o arquivo template **. admx** para o seguinte diretório: ** &lt; unidade de instalação &gt; \ \ Windows \ \ policyDefinitions**.

    Em seguida, no mesmo computador, copie o arquivo **. adml** para o seguinte diretório: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  Depois de copiar os arquivos, abra o console de gerenciamento de política de grupo, para modificar as políticas associadas aos seus clientes do App-V 5,1 navegar para políticas de **configuração do computador**  /  **Policies**  /  sistema de**modelos administrativos**  /  **System**  /  **-V**.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.1](deploying-app-v-51.md)

[Sobre as configurações do cliente](about-client-configuration-settings51.md)

 

 





