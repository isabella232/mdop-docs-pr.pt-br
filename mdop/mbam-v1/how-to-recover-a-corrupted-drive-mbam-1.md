---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796126"
---
# Como recuperar uma unidade corrompida


Para recuperar uma unidade corrompida que foi protegida pelo BitLocker, um usuário de suporte técnico de administração e monitoramento do Microsoft BitLocker (MBAM) deve criar um arquivo de pacote de chave de recuperação. Este arquivo de pacote pode ser copiado para o computador que contém a unidade corrompida e, em seguida, usado para recuperar a unidade. Para fazer isso, use o procedimento a seguir.

**Para recuperar uma unidade corrompida**

1.  Abra o site de administração do MBAM.

2.  Selecione **recuperação de unidade** no painel de navegação. Digite o nome de domínio e o nome de usuário do usuário, o motivo para desbloquear a unidade e a ID da senha de recuperação do usuário.

    **Observação**  Se você for membro da função Administradores de suporte técnico, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.

     

3.  Clique em **Enviar**. A chave de recuperação será exibida.

4.  Clique em **salvar**e selecione **pacote de chave de recuperação**. O pacote da chave de recuperação será criado em seu computador.

5.  Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.

6.  Abra um prompt de comando com privilégios elevados. Para fazer isso, clique em **Iniciar** e digite `cmd` na caixa **Pesquisar programas e arquivos** . Na lista de resultados da pesquisa, clique com o botão direito do mouse em **cmd.exe** e selecione **Executar como administrador**.

7.  No prompt de comando, digite o seguinte:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Observação**  Para a &lt; unidade fixa &gt; no comando, especifique um dispositivo de armazenamento disponível com espaço livre igual ou maior que os dados na unidade corrompida. Os dados na unidade corrompida são recuperados e movidos para a unidade fixa especificada.

     

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam.md)

 

 





