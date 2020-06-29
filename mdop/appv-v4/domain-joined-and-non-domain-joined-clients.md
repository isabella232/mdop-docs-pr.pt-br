---
title: Clientes ingressados no domínio e não ingressados no domínio
description: Clientes ingressados no domínio e não ingressados no domínio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797964"
---
# Clientes ingressados no domínio e não ingressados no domínio


O cliente da área de trabalho App-V pode ser configurado para permitir a conexão a uma rede independentemente de o cliente ter ingressado no domínio ou não no domínio.

## Clientes associados a um domínio


Os clientes que fazem parte do domínio, mas fora da rede interna, podem se comunicar com a infraestrutura do App-V usando uma conexão VPN. Quando quiser fornecer aos usuários a capacidade de sair da rede interna, mas continuar a se comunicar em uma infraestrutura do App-V, seu ambiente requer muito pouca configuração. Como os usuários já fazem parte do domínio, você só precisa garantir que as credenciais armazenadas em cache sejam compatíveis com o cliente. Essa é a configuração padrão, e todas as alterações feitas a essa configuração podem ser realizadas em políticas de grupo.

Conforme mencionado no guia de práticas recomendadas de segurança do App-V, o usuário tentará enviar sua permissão de usuário para a infraestrutura do App-V para autenticação. Se a permissão estiver vencida, ela será revertida para usar NTLM e as credenciais armazenadas em cache no computador. Para permitir o roaming, os administradores devem garantir que o servidor de publicação que está sendo acessado internamente está disponível no mesmo nome externamente para que os nomes sejam resolvidos corretamente.

## Clientes que não fazem parte do domínio


Os clientes que não ingressaram no domínio, mas precisam se comunicar na infraestrutura do App-V devem ser configurados para garantir que a autenticação para a infraestrutura do App-V seja bem-sucedida. O cliente da área de trabalho do App-V não permite solicitação para o processo de atualização de publicação, portanto, o cliente deve ser configurado para apresentar as credenciais adequadas para o servidor de gerenciamento do App-V.

O servidor de publicação, que é configurado para publicação de atualização do cliente que não ingressou no domínio, requer que o nome externo que o acesso aos clientes esteja configurado como o nome comum ou um nome alternativo de assunto (SAN) no certificado do servidor de publicação.

## Tópicos relacionados


[Como atribuir as credenciais adequadas para o Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

[Como atribuir as credenciais adequadas para o Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





