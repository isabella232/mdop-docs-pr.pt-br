---
title: Como instalar o Modelo de Política de Grupo do MBAM 2.0
description: Como instalar o Modelo de Política de Grupo do MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799835"
---
# Como instalar o Modelo de Política de Grupo do MBAM 2.0


Além dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo de administração e monitoramento do Microsoft BitLocker. Este modelo pode ser instalado em qualquer computador capaz de executar o GPMC (console de gerenciamento de política de grupo) ou no AGPM (gerenciamento avançado de política de grupo).

As etapas a seguir descrevem como instalar o modelo de política de grupo do MBAM.

**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.

 

**Para instalar o modelo de política de grupo do MBAM**

1.  No servidor em que você deseja instalar o MBAM, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Por padrão, todos os recursos de administração e monitoramento do Microsoft BitLocker são selecionados para instalação. Desmarque todas as opções de recursos, exceto o **modelo de política**, e clique em **Avançar** para continuar a instalação.

    **Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.

     

5.  Para ver as etapas específicas sobre como e onde instalar os modelos, consulte [como baixar e implantar modelos de política de grupo do MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

6.  Depois que o assistente de configuração de administração e administração do Microsoft BitLocker exibir páginas de instalação dos recursos selecionados, clique em **concluir** para fechar a instalação do MBAM.

## Tópicos relacionados


[Implantar Objetos de Política de Grupo no MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





