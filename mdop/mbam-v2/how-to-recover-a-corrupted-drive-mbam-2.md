---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799159"
---
# Como recuperar uma unidade corrompida


Para recuperar uma unidade corrompida protegida pelo BitLocker, um usuário de suporte técnico do Microsoft BitLocker Administration and Monitoring (MBAM) precisará criar um arquivo de pacote de chave de recuperação. Esse arquivo de pacote pode ser copiado para o computador que contém a unidade corrompida e, em seguida, usado para recuperar a unidade. Use o procedimento a seguir para as etapas necessárias para fazer isso.

**Importante**  Para evitar uma possível perda de dados, é altamente recomendável que você leia a ajuda "reparar-bde" e entenda claramente como usar o comando antes de concluir as instruções a seguir.

 

**Para recuperar uma unidade corrompida**

1.  Para criar o pacote de chave de recuperação necessário para recuperar uma unidade corrompida, inicie um navegador da Web e abra o site de administração e monitoramento do MBAM.

2.  Selecione **recuperação de unidade** no painel de navegação à esquerda. Digite o nome de domínio do usuário, o nome de usuário, motivo para desbloquear a unidade e a ID da senha de recuperação do usuário.

    **Observação**  Se você for membro da função Administradores de suporte técnico, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.

     

3.  Clique em **Enviar**. A chave de recuperação será exibida.

4.  Clique em **salvar**e selecione **pacote de chave de recuperação**. O pacote da chave de recuperação será criado em seu computador.

5.  Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.

6.  Abra um prompt de comando com privilégios elevados. Para fazer isso, clique em **Iniciar** e digite `cmd` na **caixa Pesquisar programas e arquivos**. Clique com o botão direito do mouse **cmd.exe** e selecione **Executar como administrador**.

7.  No prompt de comando, digite o seguinte:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Observação**  Substitua &lt; unidade fixa &gt; por uma unidade de disco rígido disponível com espaço livre igual ou maior que os dados na unidade corrompida. Os dados na unidade corrompida são recuperados e movidos para a unidade de disco rígido especificada.

     

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





