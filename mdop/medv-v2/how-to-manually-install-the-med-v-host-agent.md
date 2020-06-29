---
title: Como instalar manualmente o agente de host da MED-V
description: Como instalar manualmente o agente de host da MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796114"
---
# Como instalar manualmente o agente de host da MED-V


Há dois componentes separados, mas relacionados à solução de virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0: o agente de host e o agente de convidado do MED-V. O agente do host reside no computador host (um computador do usuário que está executando o Windows 7) e fornece um canal para se comunicar com o convidado do MED-V (a máquina virtual do MED-V em execução no computador host). Ele também fornece certas funcionalidades relacionadas ao MED-V, como a publicação de aplicativos.

Geralmente, você implanta e instala o agente de host do MED-V usando o método preferencial de provisionamento da sua empresa. No entanto, antes de implantar o MED-V em toda a sua empresa, talvez você prefira instalar o agente do host localmente para fins de teste. Esta seção fornece instruções passo a passo para instalar manualmente o agente de host MED-V.

**Observação**  O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.

 

**Importante**  Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL. Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.

 

**Para instalar o agente de host do MED-V**

1.  Localize os arquivos de instalação do MED-V recebidos como parte do download do software.

2.  Clique duas vezes no arquivo de instalação do MED-V \ _HostAgent \ _Setup.

    O assistente de **configuração do agente de host do Microsoft Enterprise Desktop Virtualization (MED-V)** é aberto. Clique em **Avançar** para continuar.

3.  Aceite os termos de licença para software Microsoft e clique em **Avançar**.

4.  Selecione a pasta de destino para instalar o agente de host MED-V. Clique em **Avançar**.

5.  Para começar a instalação do Host Agent, clique em **instalar**.

6.  Depois que a instalação for concluída com êxito, clique em **concluir** para fechar o assistente.

    Para verificar se a instalação do agente do host foi bem-sucedida, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.

**Observação**  Até que um espaço de trabalho do MED-V seja instalado, o agente de host do MED-V pode ser iniciado e executado, mas não oferece funcionalidades.

 

## Tópicos relacionados


[Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[Como instalar o empacotador de espaço de trabalho da MED-V](how-to-install-the-med-v-workspace-packager.md)

[Como desinstalar os componentes da MED-V](how-to-uninstall-the-med-v-components.md)

 

 





