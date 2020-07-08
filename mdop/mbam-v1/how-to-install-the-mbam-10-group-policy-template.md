---
title: Como instalar o Modelo de Política de Grupo do MBAM 1.0
description: Como instalar o Modelo de Política de Grupo do MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799652"
---
# Como instalar o Modelo de Política de Grupo do MBAM 1.0


Além dos recursos relacionados ao servidor do Microsoft BitLocker Administration and Monitoring (MBAM), o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM. Você pode instalar esse modelo em qualquer computador que seja capaz de executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).

As etapas a seguir descrevem como instalar o modelo de política de grupo do MBAM.

**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.

 

**Para instalar o modelo de política de grupo do MBAM**

1.  Iniciar o assistente de instalação do MBAM; em seguida, clique em **instalar** na página de boas-vindas.

2.  Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

3.  Por padrão, todos os recursos do MBAM são selecionados para instalação. Desmarque todas as opções de recursos, exceto o **modelo de política**, e clique em **Avançar** para continuar a instalação.

    **Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você deve resolver o pré-requisito ausente e clicar **novamente em verificar pré-requisitos**. Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.

     

4.  Depois que o assistente de configuração do MBAM exibir as páginas de instalação dos recursos selecionados, clique em **concluir** para fechar a instalação do MBAM.

## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





