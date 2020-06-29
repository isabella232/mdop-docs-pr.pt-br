---
title: Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação
description: Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798013"
---
# Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação


Se o certificado correto não era provisionado antes da instalação do servidor de gerenciamento do App-V ou do App-V Streaming Server, o App-V pode ser configurado para melhorar a segurança após a instalação inicial. Você pode configurar o servidor de gerenciamento do App-V por meio do console de gerenciamento do App-V. No entanto, o servidor de streaming App-V é gerenciado por meio do registro. Em ambos os casos, o certificado deve incluir o *uso de chave estendida* (EKU) adequado para autenticação do servidor e o serviço de rede deve ter acesso de leitura à chave privada.

## Nesta seção


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[Como configurar a segurança do servidor de gerenciamento após a instalação](how-to-configure-management-server-security-post-installation.md)  
Fornece um procedimento que pode ser executado após a instalação, usando o console de gerenciamento do App-V, para adicionar o certificado e configurar o servidor de gerenciamento do App-V para segurança aprimorada.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[Como configurar a segurança do servidor de streaming após a instalação](how-to-configure-streaming-server-security-post-installation.md)  
Fornece um procedimento que pode ser executado após a instalação, para adicionar o certificado e configurar o servidor de streaming App-V para segurança aprimorada.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[Solução de problemas de permissão de certificado](troubleshooting-certificate-permission-issues.md)  
Fornece orientação de solução de problemas para quando a chave privada não tiver sido configurada com a ACL apropriada para o serviço de rede.

 

 





