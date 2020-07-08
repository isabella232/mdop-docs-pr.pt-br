---
title: Como usar seu PIN ou sua senha
description: Como usar seu PIN ou sua senha
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799343"
---
# Como usar seu PIN ou sua senha


O BitLocker ajuda a proteger seu computador exigindo um PIN (número de identificação pessoal) ou uma senha para desbloquear as informações armazenadas no seu computador. Os requisitos de PIN ou senha são definidos por sua organização e dependem do tipo de unidade sendo criptografada. Os dados nas unidades criptografadas não podem ser exibidos sem a inserção do PIN ou da senha. Se o hardware do seu computador incluir um Trusted Platform Module (TPM) compatível, o chip TPM solicitará o seu PIN antes de iniciar o Windows em seu computador.

## Sobre seu PIN e senhas do BitLocker


Sua empresa especifica a complexidade necessária para seu PIN ou senha. Esses requisitos para seu PIN ou senha são explicados durante o processo de configuração do BitLocker.

A senha é usada para desbloquear unidades no computador que não contêm o sistema operacional. O BitLocker solicitará sua senha após o PIN ser solicitado durante a inicialização. Cada disco rígido protegido pelo BitLocker em seu computador tem sua própria senha exclusiva. Você não pode desbloquear uma unidade de disco protegida pelo BitLocker até fornecer a senha.

**Observação**  Seu suporte técnico pode definir unidades para desbloquear automaticamente. Isso elimina a necessidade de fornecer um PIN ou uma senha para exibir as informações nas unidades.

 

## Desbloqueando o computador se você esquecer seu PIN ou senha


Se você esquecer seu PIN ou senha, o suporte técnico poderá ajudá-lo a desbloquear unidades protegidas pelo BitLocker. Para desbloquear uma unidade protegida pelo BitLocker, entre em contato com o suporte técnico se precisar de ajuda.

**Como desbloquear seu computador se você esquecer seu PIN ou senha**

1.  Ao entrar em contato com o suporte técnico, você precisará fornecê-los com as seguintes informações:

    -   Seu nome de usuário

    -   Seu domínio

    -   Os primeiros oito dígitos da ID da chave de recuperação. Esse será um código de 32 dígitos que o BitLocker exibirá se você esquecer seu PIN ou senha.

        -   Se você esquecer seu PIN, precisará inserir os primeiros oito dígitos da ID da chave de recuperação, que aparecerá no console de recuperação do BitLocker. O console de recuperação do BitLocker é uma tela anterior ao Windows que será exibida se você não inserir o PIN correto.

        -   Se você esquecer sua senha, procure a ID da chave de recuperação no aplicativo painel de controle de opções de criptografia do BitLocker. Selecione **desbloquear unidade** e, em seguida, clique em **não consigo me lembrar da minha senha**. O aplicativo opções de criptografia do BitLocker exibirá uma ID de chave de recuperação que você fornecerá ao Help Desk.

2.  Quando o suporte técnico receber as informações necessárias, será fornecida uma chave de recuperação pelo telefone ou por email.

    -   Se você esqueceu seu PIN, insira a chave de recuperação no console de recuperação do BitLocker para desbloquear seu computador.

    -   Se você esqueceu sua senha, insira a chave de recuperação no aplicativo painel de controle de opções de criptografia BitLocker, no mesmo local em que você encontrou a ID da chave de recuperação anteriormente. Isso destravará o disco rígido protegido.

## Alterar seu PIN ou senha


Antes de poder alterar a senha em um disco protegido pelo BitLocker, você deve desbloquear a unidade. Se a unidade não for desbloqueada, selecione **desbloquear unidade**e digite sua senha atual. Assim que a unidade for desbloqueada, você poderá selecionar **gerenciar sua senha** para alterar sua senha atual.

**Como alterar seu PIN ou senha**

1.  Clique em **Iniciar**e, em seguida, selecione **painel de controle**. O painel de controle é aberto em uma nova janela.

2.  Selecione **sistema e segurança**e, em seguida, selecione **Opções de criptografia BitLocker**.

    -   Para alterar seu PIN, selecione **gerenciar seu PIN**. Digite seu novo PIN nos dois campos e selecione **Redefinir PIN**.

    -   Para alterar sua senha, selecione **gerenciar sua senha**. Digite sua nova senha nos dois campos e selecione **Redefinir senha**.

 

 





