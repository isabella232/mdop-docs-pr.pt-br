---
title: Informações para solução de problemas do Application Virtualization Server
description: Informações para solução de problemas do Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796675"
---
# Informações para solução de problemas do Application Virtualization Server


Este tópico inclui informações que você pode usar para solucionar vários problemas nos servidores do Application Virtualization (App-V).

## Mensagem de aviso 25017 no log de instalação após a instalação do servidor


Você pode encontrar a seguinte mensagem no log de instalação do servidor após a instalação.

*Aviso 25017. O programa de instalação não pôde criar o objeto do marcador do Active Directory para o servidor. A conta usada para instalar não tinha os direitos suficientes para gravar no Active Directory ou o Active Directory estava indisponível.*

O instalador do App-V ou o instalador do Stream Server cria uma entrada de ponto de conexão de serviço no objeto de computador nos serviços de domínio Active Directory (ADDS) que corresponde ao computador no qual o servidor está instalado se a conta usada para executar o instalador tem os direitos apropriados. Não criar essa entrada não fará com que a instalação falhe, e isso não afetará o funcionamento do produto. A causa mais provável de qualquer falha é que a conta de usuário usada para executar a instalação não tinha direitos suficientes para gravar em adições. Embora o registro do App-V Server no ADDS seja opcional, um benefício disso permite que as ferramentas de gerenciamento centralizado localizem o servidor App-V para fins de inventário e gerenciamento.

## Tópicos relacionados


[Application Virtualization Server](application-virtualization-server.md)

 

 





