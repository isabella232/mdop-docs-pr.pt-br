---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799596"
---
# Como recuperar uma unidade no modo de recuperação


Os recursos de recuperação de unidade criptografada do Microsoft BitLocker Administration and Monitoring (MBAM) garantem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o BitLocker entra no modo de recuperação. Um volume protegido pelo BitLocker entra no modo de recuperação quando um PIN ou uma senha é perdido ou esquecido, ou quando o chip TPM (plataforma de módulo confiável) detecta alterações nos arquivos do BIOS ou da inicialização de um computador.

Use este procedimento para acessar o sistema de dados de recuperação de chave centralizada, que pode fornecer uma senha de recuperação se uma ID de senha de recuperação e um identificador de usuário associado forem fornecidos.

**Importante**  
A administração e o monitoramento do Microsoft BitLocker usam chaves de recuperação de uso único que expiram em uso. O uso único de uma senha de recuperação é aplicado automaticamente a unidades de sistema operacional e unidades fixas. Em unidades removíveis, ele é aplicado quando a unidade é removida e, em seguida, reinserida em um computador com configurações de política de grupo ativadas para gerenciar unidades removíveis.



**Para recuperar uma unidade no modo de recuperação**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento.

2.  No painel de navegação, clique em **recuperação de unidade**. A página da Web "recuperação do acesso a uma unidade criptografada" é aberta.

3.  Insira o domínio de logon do Windows e o nome de usuário do usuário para exibir informações de recuperação e os primeiros oito dígitos da ID da chave de recuperação para receber uma lista de chaves de recuperação correspondentes ou a ID da chave de recuperação inteira para receber a chave de recuperação exata.

4.  Selecione uma das opções predefinidas da lista **motivo da desbloqueio de unidade** e clique em **Enviar**.

    **Observação**  
    Se você for um usuário de helpdesk avançado do MBAM, as entradas de domínio de usuário e identificação de usuário não serão obrigatórias.



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em uma mensagem de email. Ou, se preferir, clique em **salvar** para salvar a senha de recuperação em um arquivo.

   Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









