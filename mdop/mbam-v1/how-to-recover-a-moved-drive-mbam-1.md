---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796122"
---
# Como recuperar uma unidade movida


Ao mover uma unidade de sistema operacional anteriormente criptografada usando o Microsoft BitLocker Administration and Monitoring (MBAM), você deve resolver certos problemas. Depois que um PIN é anexado ao novo computador, a unidade não aceita o PIN de inicialização que foi usado no computador anterior. O sistema considera o PIN como inválido devido à mudança para o chip TPM (Trusted Platform Module). Você deve obter uma ID da chave de recuperação para recuperar a senha de recuperação a fim de usar a unidade movida. Para fazer isso, use o procedimento a seguir.

**Para recuperar uma unidade movida**

1.  No computador que contém a unidade movida, inicie no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o diagnóstico e o conjunto de ferramentas de recuperação (DaRT) da Microsoft.

2.  Depois que o computador for iniciado com o WinRE ou o DaRT, o MBAM tratará a unidade do sistema operacional movida como uma unidade de dados. O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.

    **Observação**  Em alguns casos, você poderá clicar em **eu esquecer o PIN** durante o processo de inicialização para entrar no modo de recuperação. Isso também exibe a ID da chave de recuperação.

     

3.  No site de administração do MBAM, use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade.

4.  Se a unidade movida foi configurada para usar um chip TPM no computador original, você deve executar etapas adicionais após desbloquear a unidade e concluir o processo de inicialização. No modo WinRE, abra um prompt de comando e use a ferramenta **Manage-bde** para descriptografar a unidade. O uso dessa ferramenta é a única maneira de remover a proteção TPM-mais-PIN sem o chip TPM original.

5.  Após a conclusão da remoção, inicie o sistema normalmente. O agente do MBAM continuará importando a política para criptografar a unidade com o novo PIN do computador e o PIN.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam.md)

 

 





