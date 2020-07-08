---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799595"
---
# Como redefinir um bloqueio de TPM


O recurso de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) abrange tanto a captura quanto o armazenamento de dados quanto a disponibilidade para ferramentas necessárias para gerenciar o TPM (Trusted Platform Module). Este tópico aborda como acessar o sistema de dados de recuperação de chave centralizada no site de administração e monitoramento, que pode fornecer um arquivo de senha de proprietário do TPM quando uma ID de computador e um identificador de usuário associado são fornecidos.

Um bloqueio de TPM pode ocorrer se um usuário inserir o PIN incorreto muitas vezes. O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.

Você só pode redefinir um bloqueio de TPM se MBAM for proprietário do TPM.

**Para redefinir um bloqueio de TPM**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento.

2.  No painel de navegação à esquerda, selecione **gerenciar TPM** para abrir a página **gerenciar TPM** .

3.  Digite o nome de domínio totalmente qualificado para o computador e o nome do computador e insira o domínio de logon do Windows do usuário e o nome de usuário do usuário para recuperar o arquivo de senha de proprietário do TPM.

4.  Na lista o motivo da solicitação **de arquivo de senha de proprietário do TPM** , selecione um motivo para a solicitação e clique em **Enviar**.

    MBAM retorna um dos seguintes:

    -   Uma mensagem de erro, se não for encontrado um arquivo de senha de proprietário do TPM correspondente

    -   O arquivo de senha de proprietário do TPM para o computador enviado

    **Observação**  
    Se você for um usuário avançado da assistência técnica, os campos de usuário e ID de usuário do usuário não são necessários.



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. Para salvar a senha em um arquivo. TPM, clique no botão **salvar** .

   O usuário executará o console de gerenciamento do TPM, selecionará a opção **Redefinir bloqueio do TPM** e fornecerá o arquivo de senha de proprietário do TPM para redefinir o bloqueio do TPM.

   **Importante**  
   Os administradores de suporte técnico não devem fornecer o valor de hash TPM ou o arquivo de senha de proprietário do TPM aos usuários finais. As informações do TPM não são alteradas, portanto, ele pode representar um risco de segurança se o arquivo for fornecido para os usuários finais.



## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









