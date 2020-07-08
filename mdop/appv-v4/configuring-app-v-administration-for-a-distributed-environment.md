---
title: Configuração da administração do App-V para um ambiente distribuído
description: Configuração da administração do App-V para um ambiente distribuído
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798020"
---
# Configuração da administração do App-V para um ambiente distribuído


Ao projetar a infraestrutura de sua organização específica, você pode instalar o serviço Web de gerenciamento do App-V em um computador diferente do computador em que você instala o servidor de gerenciamento do App-V. Os motivos comuns para separar esses componentes do App-V incluem o seguinte:

-   Desempenho

-   Confiabilidade

-   Disponibilidade

-   Escalabilidade

Separar o servidor de gerenciamento e o serviço Web de gerenciamento exige configuração adicional para que a infraestrutura opere corretamente. Quando você separa esses dois recursos, mas não conclua os procedimentos descritos neste tópico, o console de gerenciamento se conectará ao serviço Web de gerenciamento, mas não poderá ser autenticado corretamente com o repositório de dados. O console de gerenciamento não será carregado corretamente, e o administrador não será capaz de concluir tarefas administrativas.

Esse comportamento ocorre porque o serviço Web de gerenciamento não pode usar as credenciais, transmitidas a ele pelo console de gerenciamento, para acessar o repositório de dados. A solução é configurar o servidor de serviços Web de gerenciamento como "confiável para delegação".

## Configurar os serviços de domínio do Active Directory


Também é necessário configurar adequadamente os serviços de domínio do Active Directory para que funcionem em um ambiente distribuído. Esta seção inclui as informações de que você precisa para configurar os serviços de domínio Active Directory.

### Quando o SQL Service usa a conta do sistema local

Para configurar o ambiente em que o serviço SQL usa a conta do sistema local, altere as propriedades da conta do computador do serviço Web de gerenciamento para serem confiáveis para delegação. Para obter procedimentos detalhados sobre como fazer isso, consulte [como configurar o servidor para ser confiável para delegação](how-to-configure-the-server-to-be-trusted-for-delegation.md)

### Quando o serviço SQL usa uma conta baseada em domínio

Para configurar o ambiente em que os servidores SQL usam contas de serviço baseadas em domínio, você precisa considerar se uma série de fatores se aplica, incluindo o seguinte:

-   Clustering do SQL Server

-   Replicação

-   Tarefas automatizadas

-   Servidores vinculados

Para obter informações sobre como configurar os serviços de domínio Active Directory quando o serviço SQL usa uma conta baseada em domínio, consulte <https://go.microsoft.com/fwlink/?LinkId=151968> .

 

 





