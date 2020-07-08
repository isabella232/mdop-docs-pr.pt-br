---
title: Como atribuir as credenciais adequadas para o Windows Vista
description: Como atribuir as credenciais adequadas para o Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797911"
---
# Como atribuir as credenciais adequadas para o Windows Vista


Use o procedimento a seguir para configurar o cliente da área de trabalho App-V para credenciais WindowsVista adequadas.

**Observação**  Este procedimento deve ser concluído em cada computador não associado ao domínio. Dependendo do número de computadores não associados ao domínio em seu ambiente, isso pode ser uma operação muito tediosa. Você pode usar scripts e a interface de linha de comando para o Gerenciador de credenciais para ajudar os administradores a automatizar esse processo.

 

**Para atribuir as credenciais adequadas para os clientes App-V que executam o Windows Vista**

1.  Com privilégios de administrador no cliente da área de trabalho App-V executando o Windows Vista, abra o painel de controle de **contas de usuário** (painel de controle clássico).

2.  Selecione **gerenciar suas senhas de rede** em **contas de usuário** no painel de tarefas à esquerda.

3.  Selecione **Adicionar** na tela **nomes de usuário e senhas armazenados** .

4.  Na tela **Propriedades de credenciais armazenadas** , forneça as informações para a infraestrutura do App-V:

    1.  **Faça logon em:** Nome externo do servidor de publicação.

    2.  **Nome de usuário:** Nome de usuário do usuário externo na forma Domain\\Username.

    3.  **Senha:** Senha da conta de usuário inserida no campo **nome de usuário** .

    4.  Deixe o **tipo de credencial** selecionado e clique em **OK**.

5.  Clique em **Fechar**. As credenciais são armazenadas no repositório de credenciais para autenticação adequada à infraestrutura do App-V.

## Tópicos relacionados


[Clientes ingressados no domínio e não ingressados no domínio](domain-joined-and-non-domain-joined-clients.md)

[Como atribuir as credenciais adequadas para o Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





