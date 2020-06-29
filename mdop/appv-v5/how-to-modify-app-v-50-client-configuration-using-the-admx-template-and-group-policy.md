---
title: Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo
description: Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796350"
---
# Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo


Use o modelo ADMX do App-V 5,0 para definir as configurações do aplicativo cliente do App-V 5,0 usando o modelo ADMX e a política de grupo.

**Para modificar a configuração do cliente do App-V 5,0 usando a política de grupo**

1.  Para modificar a configuração do cliente do App-V 5,0, localize os arquivos **admxtemplate** disponíveis com o app-v 5,0.

    **Observação**  Use o link a seguir para baixar os **modelos do ADMX**do App-V 5,0: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  No computador em que você gerencia a política de grupo, normalmente o controlador de domínio, copie o arquivo template **. admx** para o seguinte diretório: ** &lt; unidade de instalação &gt; \ \ Windows \ \ policyDefinitions**.

    Em seguida, no mesmo computador, copie o arquivo **. adml** para o seguinte diretório: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  Depois de copiar os arquivos, abra o console de gerenciamento de política de grupo, para modificar as políticas associadas aos seus clientes do App-V 5,0 navegar para políticas de **configuração do computador**  /  **Policies**  /  sistema de**modelos administrativos**  /  **System**  /  **-V**.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.0](deploying-app-v-50.md)

[Sobre as configurações do cliente](about-client-configuration-settings.md)

 

 





