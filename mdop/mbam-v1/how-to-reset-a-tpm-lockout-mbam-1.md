---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796120"
---
# Como redefinir um bloqueio de TPM


O recurso de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) abrange tanto a captura quanto o armazenamento de dados quanto a disponibilidade para ferramentas necessárias para gerenciar o TPM (Trusted Platform Module). Este tópico aborda como acessar o sistema de dados de recuperação de chave centralizada no site de administração do bit \ _admmon \ _tlanextref. O sistema de dados de recuperação de chave pode fornecer um arquivo de senha de proprietário do TPM quando a identidade do computador e o identificador de usuário associado são fornecidos.

Um bloqueio de TPM pode ocorrer se um usuário inserir um PIN incorreto muitas vezes. O número de vezes que um usuário pode inserir um PIN incorreto antes de o bloqueio do TPM se basear na especificação do fabricante do computador.

**Para redefinir um bloqueio de TPM**

1.  Abra o site de administração do MBAM.

2.  No painel de navegação, selecione **gerenciar TPM**. Isso abre a página **gerenciar TPM** .

3.  Digite o nome de domínio totalmente qualificado (FQDN) para o computador e o nome do computador. Insira o domínio de logon do Windows do usuário e o nome de usuário do usuário. Selecione uma das opções predefinidas no menu suspenso o **arquivo de senha de proprietário do TPM** . Clique em **Enviar**.

4.  MBAM retornará um dos seguintes:

    -   Uma mensagem de erro se não for encontrado um arquivo de senha de proprietário do TPM correspondente

    -   O arquivo de senha de proprietário do TPM para o computador enviado

    **Observação**  Se você for um usuário avançado da assistência técnica, os campos de usuário e ID de usuário do usuário não são necessários.

     

5.  Após a recuperação, a senha do proprietário será exibida. Para salvar esta senha em um arquivo. TPM, clique no botão **salvar** .

6.  O usuário executará o console de gerenciamento do TPM e selecionará a opção **Redefinir bloqueio do TPM** e fornecerá o arquivo de senha de proprietário do TPM para redefinir o bloqueio do TPM.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam.md)

 

 





