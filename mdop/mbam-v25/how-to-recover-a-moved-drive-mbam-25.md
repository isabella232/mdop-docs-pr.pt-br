---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799253"
---
# Como recuperar uma unidade movida
Este tópico explica como usar o site de administração e monitoramento (também chamado de suporte técnico) para recuperar uma unidade do sistema operacional que foi movida após ser criptografada pelo Microsoft BitLocker Administration and Monitoring (MBAM). Quando uma unidade é movida, ela não aceita mais o PIN usado no computador anterior porque o chip TPM (Trusted Platform Module) foi alterado. Para recuperar a unidade movida, você deve obter a ID da chave de recuperação para recuperar a senha de recuperação.

Para recuperar uma unidade movida, você deve usar a área de **recuperação de unidade** do site de administração e monitoramento. Para acessar a área de **recuperação da unidade** , você deve ser atribuído à função usuários da assistência técnica do MBAM ou à função usuários avançados da assistência técnica do MBAM. Para obter mais informações sobre essas funções, confira [planejamento para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Para recuperar uma unidade movida**
1.  No computador que contém a unidade movida, inicie o computador no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft.

2.  Depois que o computador for iniciado com o WinRE ou o DaRT, o MBAM tratará a unidade do sistema operacional movida como uma unidade de dados fixa. O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.

    **Observação**  Em alguns casos, você poderá clicar em **esqueci o PIN** durante o processo de inicialização e, em seguida, inserir o modo de recuperação para exibir a ID da chave de recuperação.

     

3.  Use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade no site de administração e monitoramento. Para obter instruções, consulte [como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).

    Se a unidade movida tiver sido configurada para usar um chip TPM no computador original, conclua as etapas adicionais a seguir. Caso contrário, o processo de recuperação é concluído.

4.  Após desbloquear a unidade e concluir o processo de inicialização, abra um prompt de comando no modo WinRE e use o `manage-bde` comando para descriptografar a unidade. Usar essa ferramenta é a única maneira de remover o TPM mais o protetor de PIN sem o chip TPM original. Para obter informações sobre o `manage-bde` comando, consulte [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).

5.  Quando a remoção for concluída, inicie o computador normalmente. O agente MBAM irá impor a política para criptografar a unidade com o TPM do novo computador mais o PIN.



## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





