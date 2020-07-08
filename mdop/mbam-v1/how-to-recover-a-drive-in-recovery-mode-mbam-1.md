---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796128"
---
# Como recuperar uma unidade no modo de recuperação


O monitoramento e a administração do Microsoft BitLocker (MBAM) incluem recursos de recuperação de unidade criptografada. Esses recursos garantem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o BitLocker coloca esse volume em modo de recuperação. Um volume protegido pelo BitLocker entra no modo de recuperação quando um PIN ou uma senha é perdido ou esquecido ou quando o chip TPM detecta uma alteração na BIOS ou arquivos de inicialização do computador.

Use este procedimento para acessar o sistema de dados de recuperação de chave centralizada que pode fornecer uma senha de recuperação quando for fornecida uma ID de senha de recuperação e um identificador de usuário associado.

**Importante**  MBAM gera chaves de recuperação de uso único. Sob essa limitação, uma chave de recuperação pode ser usada apenas uma vez e, em seguida, não é mais válida. O uso único de uma senha de recuperação é aplicado automaticamente a unidades de sistema operacional e unidades fixas. Em unidades removíveis, o uso único é aplicado quando a unidade é removida e, em seguida, reinserida e desbloqueada em um computador com as configurações de política de grupo ativadas para gerenciar unidades removíveis.

 

**Para recuperar uma unidade no modo de recuperação**

1.  Abra o site do MBAM.

2.  No painel de navegação, clique em **recuperação de unidade**. A página da Web de **recuperação de acesso a uma unidade criptografada** é aberta.

3.  Insira o domínio de logon do Windows do usuário e o nome de usuário e os primeiros oito dígitos da ID da chave de recuperação para receber uma lista de possíveis chaves de recuperação correspondentes. Você também pode inserir a ID da chave de recuperação inteira para receber a chave de recuperação exata. Selecione uma das opções predefinidas na lista suspensa **razão para desbloquear unidade** e, em seguida, clique em **Enviar**.

    **Observação**  Se você for um usuário de helpdesk avançado do MBAM, as entradas de domínio de usuário e identificação de usuário não serão obrigatórias.

     

4.  MBAM retornará o seguinte:

    1.  Uma mensagem de erro se nenhuma senha de recuperação correspondente for encontrada

    2.  Várias correspondências possíveis se o usuário tiver várias senhas de recuperação correspondentes

    3.  A senha de recuperação e o pacote de recuperação para o usuário enviado

        **Observação**  Se você estiver recuperando uma unidade danificada, a opção pacote de recuperação fornece o BitLocker com as informações críticas necessárias para tentar a recuperação.

         

5.  Depois que a senha de recuperação e o pacote de recuperação forem recuperados, a senha de recuperação será exibida. Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em um email ou em outro arquivo de texto para armazenamento temporário. Ou, para salvar a senha de recuperação em um arquivo, clique em **salvar**.

6.  Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam.md)

 

 





