---
title: Quais são as novidades no App-V 5.0 SP1
description: Quais são as novidades no App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796194"
---
# Quais são as novidades no App-V 5.0 SP1


Esta seção é para os usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,0 SP1. Se você ainda não estiver familiarizado com o App-V, comece lendo planejando o [app-v 5,0](planning-for-app-v-50-rc.md).

## Alterações na funcionalidade padrão


As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5,0 SP1.

### Alterações em idiomas com suporte

Para obter mais informações, consulte [sobre o App-V 5,0 SP1](about-app-v-50-sp1.md).

A lista a seguir contém mais informações sobre os novos pacotes de idiomas:

-   Os pacotes de idiomas do App-V 5.0 SP1 são incluídos no instalador **appv\_xxx\_setup.exe** para todos os componentes do App-v 5,0.

-   Quando você executar o instalador, ele instalará automaticamente o pacote de idiomas mais apropriado com base na localidade do sistema operacional associado em execução no computador de destino.

-   Se forem necessários pacotes de idiomas adicionais, você deverá extrair esses pacotes de idiomas do instalador executando o seguinte `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` comando: Depois que isso tiver sido executado, o conteúdo do instalador será extraído para o local especificado.

-   Você deve instalar o pacote de idiomas desejado aplicando o arquivo de instalação do pacote de idiomas apropriado. Por exemplo, **appv\_hib\_LP\_jmmb\_x86.msi** ou **appv\_hib\_LP\_jmmb\_x64.msi**, onde **Hib** refere-se ao componente e **jmmb** refere-se à localidade.

## Suporte aprimorado para o Microsoft office2010


**O kit de sequenciamento do Microsoft Office 2010 para o Application Virtualization 5,0** – ajuda a oferecer aos usuários uma experiência consistente ao usar uma versão virtualizada do Microsoft office2010. O **Kit de sequenciamento do Microsoft office 2010 para o Application Virtualization 5,0** é usado em conjunto com o **Kit de implantação do Microsoft Office 2010 para o App-V** e também fornece o serviço de licenciamento do Microsoft office2010 necessário.






## Tópicos relacionados


[Sobre o App-V 5.0](about-app-v-50.md)

 

 





