---
title: Ajudando os usuários finais a gerenciar o BitLocker
description: Ajudando os usuários finais a gerenciar o BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799540"
---
# Ajudando os usuários finais a gerenciar o BitLocker


O conteúdo em um computador perdido ou roubado é vulnerável a acesso não autorizado, que pode representar um risco de segurança para pessoas e empresas. O monitoramento e administração do Microsoft BitLocker (MBAM) usa o BitLocker para ajudar a evitar o acesso não autorizado, bloqueando o computador para ajudar a proteger dados confidenciais de usuários mal-intencionados.

## O que é BitLocker?


A criptografia de unidade de disco BitLocker pode oferecer proteção para unidades de sistema operacionais, unidades de dados e unidades removíveis (como uma unidade USB Thumb) criptografando as unidades. Dependendo de como o BitLocker estiver configurado, os usuários podem precisar fornecer uma chave (uma senha ou PIN) para desbloquear as informações armazenadas nas unidades criptografadas.

Quando você adiciona novos arquivos a uma unidade criptografada com o BitLocker, o BitLocker os criptografa automaticamente. Os arquivos permanecem criptografados somente enquanto são armazenados na unidade criptografada. Os arquivos copiados para outra unidade ou computador são descriptografados. Se você compartilhar arquivos com outros usuários, por exemplo, por meio de uma rede, esses arquivos serão criptografados enquanto estiverem armazenados na unidade criptografada, mas poderão ser acessados normalmente por usuários autorizados.

Se você criptografar a unidade do sistema operacional, o BitLocker verifica o computador durante a inicialização em busca de condições que possam representar um risco de segurança (por exemplo, uma alteração no BIOS ou muda para qualquer arquivo de inicialização). Se um possível risco de segurança for detectado, o BitLocker bloqueará a unidade do sistema operacional e será necessária uma chave de recuperação do BitLocker especial para desbloqueá-la. Certifique-se de criar essa chave de recuperação ao ativar o BitLocker pela primeira vez. Caso contrário, você pode perder permanentemente o acesso aos seus arquivos.

Se você criptografar unidades de dados (fixas ou removíveis), poderá desbloquear uma unidade criptografada com uma senha ou um cartão inteligente ou definir a unidade para desbloquear automaticamente quando você fizer logon no computador.

Além de senhas e PINs, o BitLocker pode usar o chip Trusted Platform Module (TPM) fornecido em muitos computadores mais novos. O chip TPM é usado para garantir que seu computador não tenha sido adulterado antes de o BitLocker desbloqueie a unidade do sistema operacional. Durante o processo de criptografia, talvez seja necessário habilitar o chip TPM. Quando você inicia o computador, o BitLocker pede que o TPM entre as chaves para a unidade e a desbloqueie. Para habilitar o chip TPM, será preciso reiniciar o computador e alterar uma configuração no BIOS, em uma camada anterior ao Windows do software do computador. Para obter mais informações sobre o TPM, consulte [sobre o chip TPM do computador](about-the-computer-tpm-chip.md).

Depois que seu computador estiver protegido pelo BitLocker, talvez seja necessário digitar um PIN ou uma senha sempre que o computador ativar ou iniciar a hibernação. O suporte técnico para sua empresa ou organização pode ajudá-lo a se esquecer do seu PIN ou senha.

Você pode desativar o BitLocker temporariamente, temporariamente, suspendendo-o, ou permanentemente, descriptografando a unidade.

**Observação**  Como o BitLocker criptografa toda a unidade e não apenas os próprios arquivos individuais, tenha cuidado ao mover dados confidenciais entre unidades. Se você mover um arquivo de uma unidade de disco protegida pelo BitLocker para uma unidade não criptografada, o arquivo não será mais criptografado.

 

## Sobre o aplicativo opções de criptografia do BitLocker


Para desbloquear as unidades de disco rígido do seu computador e gerenciar seu PIN e senhas, use o aplicativo opções de criptografia do BitLocker no painel de controle do Windows seguindo o procedimento descrito aqui. Você pode inserir senhas para desbloquear unidades protegidas e verificar o status do BitLocker das unidades conectadas usando este aplicativo.

**Para abrir o aplicativo opções de criptografia do BitLocker**

1.  Clique em **Iniciar**e selecione **painel de controle**. O painel de controle é aberto em uma nova janela.

2.  No **painel de controle**, selecione **sistema e segurança**.

3.  Selecione **Opções de criptografia do BitLocker** para abrir o aplicativo opções de criptografia do BitLocker.

    Para obter uma descrição das opções disponíveis, consulte a seção a seguir.

## Opções no aplicativo opções de criptografia do BitLocker


O aplicativo opções de criptografia do BitLocker no painel de controle permite que você gerencie seu PIN e senhas, que o BitLocker usa para proteger seu computador.

**Criptografia de unidade de disco BitLocker – drives de disco fixos:**

Nesta seção, você pode exibir informações sobre unidades de disco rígido conectadas ao seu computador e o status atual de criptografia do BitLocker.

-   **Gerenciar seu PIN** -altera o PIN usado pelo BitLocker para desbloquear a unidade do sistema operacional.

-   **Gerenciar sua senha** – altera a senha que é usada pelo BitLocker para desbloquear suas outras unidades internas.

**Criptografia de unidade de disco BitLocker-unidades externas:**

Nesta seção, você pode exibir informações sobre unidades externas (como um pen drive) conectados ao seu computador e o status atual de criptografia do BitLocker.

-   **Gerenciar sua senha** – altera a senha que é usada pelo BitLocker para desbloquear suas outras unidades internas.

**Antecipa**

-   **Administração do TPM** -abre a ferramenta de administração do TPM em uma janela separada. Aqui você pode configurar tarefas comuns do TPM e obter informações sobre o chipset TPM. Você deve ter permissões administrativas no seu computador para acessar essa ferramenta.

-   **Gerenciamento de disco** : abrir a ferramenta de gerenciamento de disco. Aqui você pode ver as informações de todos os discos rígidos conectados ao computador e configurar partições e opções de unidade. Você deve ter direitos administrativos em seu computador para acessar essa ferramenta.

 

 





