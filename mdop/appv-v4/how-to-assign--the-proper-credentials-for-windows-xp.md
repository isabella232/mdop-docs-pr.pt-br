---
title: Como atribuir as credenciais adequadas para o Windows XP
description: Como atribuir as credenciais adequadas para o Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797502"
---
# Como atribuir as credenciais adequadas para o Windows XP


Use o procedimento a seguir para configurar o cliente da área de trabalho do App-V para credenciais corretas do WindowsXP.

**Observação**  Depois de concluir esse procedimento, o cliente que não ingressou no domínio pode executar uma atualização de publicação sem ingressar em um domínio.

 

**Para atribuir as credenciais adequadas para clientes App-V que executam o WindowsXP**

1.  Com privilégios de administrador no aplicativo App-V executando WindowsXP, abra o painel de controle de **contas de usuário** (painel de controle clássico).

2.  Clique na **guia Avançado**e selecione **gerenciar senhas**.

3.  Na tela **nomes de usuário e senhas armazenados** , clique em **Adicionar**.

4.  Na tela **Propriedades de informações de logon** , preencha os seguintes campos com informações da infraestrutura do App-V:

    1.  **Servidor:** Nome externo do servidor de publicação.

    2.  **Nome de usuário:** Nome de usuário para usuário externo na forma Domain\\username.

    3.  **Senha:** Senha da conta de usuário inserida no campo **nome de usuário** .

5.  Clique em **OK**. As credenciais serão armazenadas no cliente.

## Tópicos relacionados


[Clientes ingressados no domínio e não ingressados no domínio](domain-joined-and-non-domain-joined-clients.md)

[Como atribuir as credenciais adequadas para o Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





