---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799597"
---
# Como recuperar uma unidade movida


Quando você move uma unidade de sistema operacional criptografada usando o Microsoft BitLocker Administration and Monitoring (MBAM), a unidade não aceita o PIN que foi usado em um computador anterior devido à mudança para o chip TPM (Trusted Platform Module). Para usar a unidade movida, você precisará de uma maneira de obter a ID da chave de recuperação para recuperar a senha de recuperação. Use o procedimento a seguir para recuperar uma unidade que foi movida.

**Para recuperar uma unidade movida**

1.  No computador que contém a unidade movida, inicie o computador no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft.

2.  Depois que o computador for iniciado com o WinRE ou o DaRT, a administração e o monitoramento do Microsoft BitLocker tratarão a unidade do sistema operacional movida como uma unidade de dados. O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.

    **Observação**  Em alguns casos, você poderá clicar em **esqueci o PIN** durante o processo de inicialização e, em seguida, inserir o modo de recuperação para exibir a ID da chave de recuperação.

     

3.  Use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade no site de administração e monitoramento.

4.  Se a unidade movida foi configurada para usar um chip TPM no computador original, você deve executar etapas adicionais após desbloquear a unidade e concluir o processo de inicialização. No modo WinRE, abra um prompt de comando e use a ferramenta **Manage-bde** para descriptografar a unidade. Usar essa ferramenta é a única maneira de remover o TPM e o protetor de pino sem o chip TPM original.

5.  Quando a remoção for concluída, inicie o computador normalmente. O agente do MBAM agora irá impor a política para criptografar a unidade com o novo PIN do computador e o PIN do novo computador.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





