---
title: Como verificar as configurações da primeira instalação
description: Como verificar as configurações da primeira instalação
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796146"
---
# Como verificar as configurações da primeira instalação


Enquanto o teste da configuração inicial estiver em execução ou após a conclusão, você pode verificar as configurações que configurou em seu espaço de trabalho do MED-V executando as seguintes tarefas.

**Observação**  Para obter informações sobre como monitorar a conclusão bem-sucedida da primeira configuração da sua empresa após a implantação, consulte [monitoramento de implantações de espaço de trabalho do MED-V](monitoring-med-v-workspace-deployments.md).

 

**Para verificar as configurações durante a configuração da primeira vez**

1.  Enquanto a configuração estiver em execução pela primeira vez, verifique o seguinte:

    Se você especificou o modo **autônomo** , verifique se a máquina virtual não é exibida na primeira vez em que a configuração está em execução.

    Se você especificou o modo assistido, verifique se a máquina virtual é exibida e se todos os campos que exigem entrada do usuário são exibidos.

2.  Você também pode monitorar o processo de configuração completo da primeira vez, exibindo a máquina virtual na primeira vez em que a configuração estiver em execução. Para fazer isso, execute estas etapas:

    1.  Abra o console do Windows Virtual PC.

        Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.

    2.  Inicie o MED-V se ele ainda não estiver em execução.

        Se ainda não estiver presente, em curto período, uma máquina virtual com o nome do espaço de trabalho do MED-V implantado aparecerá na lista de máquinas virtuais.

    3.  Clique duas vezes na máquina virtual do MED-V para abri-la.

        Você pode observar a máquina virtual do MED-V quando ela está sendo configurada, e você pode solucionar problemas com o procedimento de mini-configuração. Verifique as informações nas diferentes telas à medida que elas entram, como a configuração de configurações de rede, informações sobre o domínio do computador, configuração do agente convidado, configuração de configurações pessoais e desligamento.

    4.  A máquina virtual é fechada automaticamente quando a instalação for concluída pela primeira vez.

        **Observação**  Você pode fechar a janela da máquina virtual a qualquer momento e a configuração da primeira vez continuar.

         

**Para verificar as configurações após a conclusão da instalação do programa pela primeira vez**

1.  Verifique se a configuração da primeira vez foi concluída com êxito.

2.  Verifique se o espaço de trabalho do MED-V está configurado corretamente.

    1.  Abra o console do Windows Virtual PC.

        Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.

    2.  Clique duas vezes no seu espaço de trabalho do MED-V instalado.

        Se o espaço de trabalho do MED-V já estiver executando um aplicativo virtual, talvez você seja solicitado a fechar o aplicativo antes de poder abrir a máquina virtual.

    3.  No espaço de trabalho do MED-V, clique com o botão direito do mouse em **meu computador**e, em seguida, clique em **Propriedades**.

    4.  Verifique se o espaço de trabalho do MED-V ingressou no domínio correto. Se aplicável à sua organização, teste o ingresso no domínio especificando dois domínios diferentes para verificar se o domínio de convidado é substituído pelo domínio host.

    5.  Verifique se o espaço de trabalho do MED-V ingressou na unidade organizacional do domínio que você especificou.

    6.  Se você especificou a máscara de nome do computador, verifique se o novo nome do computador corresponde ao que foi especificado.

3.  Verifique se as configurações de localidade especificadas estão corretas.

    1.  No espaço de trabalho do MED-V, clique em **Iniciar** e em **painel de controle**.

    2.  Verifique as configurações especificadas, por exemplo, **data e hora** e **regionais e idioma**.

**Observação**  Se você tiver problemas ao verificar as configurações de configuração da primeira vez, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).

 

Depois de verificar se as configurações de configuração da primeira vez estão corretas, você pode testar outras configurações do espaço de trabalho do MED-V para verificar se elas funcionam conforme o esperado, como a publicação de aplicativos e o redirecionamento de URL.

Depois de concluir o teste do pacote do espaço de trabalho do MED-V e verificar se ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.

## Tópicos relacionados


[Como testar a publicação de aplicativos](how-to-test-application-publishing.md)

[Como testar o redirecionamento da URL](how-to-test-url-redirection.md)

[Como implantar o pacote de espaço de trabalho da MED-V](deploying-the-med-v-workspace-package.md)

[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)

 

 





