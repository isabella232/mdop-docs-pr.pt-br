---
title: Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro
description: Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797112"
---
# Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro


A instalação padrão do console de gerenciamento do App-V inclui suporte para comunicações seguras. Cada console de gerenciamento é configurado em uma base por conexão quando o console é iniciado pela primeira vez ou quando se conecta a um serviço de gerenciamento da Web do App-V adicional. A configuração padrão usa SSL na porta TCP 443. Você pode alterar o número da porta se o número da porta for modificado no servidor. Você pode usar o procedimento a seguir para se conectar a um serviço de gerenciamento da Web do App-V usando uma conexão segura.

**Como se conectar a um serviço de gerenciamento do App-V usando uma conexão SSL**

1.  Inicie o console de gerenciamento do Application Virtualization.

2.  Clique em **Configurar conexão** no painel Ações do console.

3.  Digite o **nome do host do serviço Web**e certifique-se de que **usar conexão segura** esteja selecionado.

    **Importante**  O nome fornecido no nome do host do serviço Web deve coincidir com o nome comum no certificado ou a conexão falhará.

     

4.  Selecione as credenciais de logon apropriadas e clique em **OK**.

## Tópicos relacionados


[Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





