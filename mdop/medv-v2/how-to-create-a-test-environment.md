---
title: Como criar um ambiente de teste
description: Como criar um ambiente de teste
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800042"
---
# Como criar um ambiente de teste


Veja a seguir algumas etapas e instruções para ajudá-lo a criar um ambiente de teste que você pode usar para testar o pacote do espaço de trabalho do MED-V localmente antes de implantá-lo em toda a empresa. Esta seção fornece orientação sobre como criar um ambiente de teste, seja manualmente ou usando um sistema de distribuição de software eletrônico.

**Para criar um ambiente de teste usando um ESD**

1.  Use o método de implantação de software na empresa em toda a empresa para implantar os seguintes componentes necessários em um computador de teste. Instale-os na seguinte ordem:

    -   **PC virtual do Windows** – se ainda não estiver instalado. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    -   **Inclusões e atualizações do Windows Virtual PC**– se ainda não estiverem instaladas. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    -   **Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação). Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).

    -   **Instalador do espaço de trabalho do MED-v, VHD e executável de configuração** – criado no **pacote do espaço de trabalho do MED-v**. Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).

        **Importante**  O programa executável de configuração e VHD deve estar na mesma pasta que o instalador do espaço de trabalho do MED-V. Em seguida, instale o instalador do espaço de trabalho do MED-V executando setup.exe.

         

2.  Depois que todos os componentes estiverem instalados no computador de teste, execute o MED-V Host Agent para iniciar a configuração da primeira vez.

    Clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.

    **Observação**  Se você não puder executar fisicamente o agente de host do MED-V no computador de teste, a configuração iniciará automaticamente na próxima vez em que o computador for reiniciado.

     

Primeira vez que o programa de instalação é iniciado, pode levar dez minutos ou mais para concluir.

Para obter informações sobre como testar suas configurações na primeira vez em que a configuração estiver em execução, consulte [como verificar as configurações de configuração da primeira vez](how-to-verify-first-time-setup-settings.md).

**Para criar um ambiente de teste manualmente**

1.  Instale o agente de host do MED-V em um ambiente de teste local que inclua pré-requisitos do MED-V, como o Windows Virtual PC com adições e atualizações. Para obter informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).

2.  Copie os arquivos do espaço de trabalho do MED-V para o seu ambiente de teste. Os arquivos do espaço de trabalho do MED-V estão localizados na pasta de destino que você especificou no **pacote do espaço de trabalho do MED-v**.

    **Importante**  O programa executável de configuração e VHD deve estar na mesma pasta em seu ambiente de teste como o instalador do espaço de trabalho do MED-V.

     

3.  Instale o espaço de trabalho do MED-V executando setup.exe.

4.  Iniciar a configuração da primeira vez executando o agente de host MED-V.

    Clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.

Início da primeira vez em que a configuração é iniciada e pode demorar vários minutos para ser concluída, dependendo do tamanho do VHD especificado.

Agora você está pronto para testar as diferentes configurações de configuração, publicação de aplicativos e redirecionamento de URL que você especificou para seu espaço de trabalho do MED-V.

**Observação**  Por padrão, o MED-V substitui a política de bloqueio de tela no convidado. No entanto, isso não representa um problema de segurança porque o computador host ainda honra a política de bloqueio de tela.

 

## Tópicos relacionados


[Como verificar as configurações da primeira instalação](how-to-verify-first-time-setup-settings.md)

[Como testar a publicação de aplicativos](how-to-test-application-publishing.md)

[Como testar o redirecionamento da URL](how-to-test-url-redirection.md)

 

 





