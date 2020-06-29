---
title: Solução de problemas de permissão de certificado
description: Solução de problemas de permissão de certificado
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796679"
---
# Solução de problemas de permissão de certificado


Após a instalação do App-V 4.5, se a chave privada não tiver sido configurada com a ACL apropriada para o serviço de rede, um evento será registrado no log de eventos do NT e uma entrada será colocada no `Sft-server.log` arquivo.

## Mensagens de erro


### Windows Server2003

ID do evento 36870 — ocorreu um erro fatal ao tentar acessar a chave privada da credencial do servidor SSL. O código de erro retornado do módulo criptográfico é 0x80090016.

### Windows Server2008

ID do evento 36870 — ocorreu um erro fatal ao tentar acessar a chave privada da credencial do servidor SSL. O código de erro retornado do módulo criptográfico é 0x8009030d.

## SFT-Server. log


O erro a seguir é colocado no `sft-server.log` arquivo localizado no `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` diretório:

Não foi possível carregar o certificado. Código de erro \ [-2146893043 \]. Verifique se a conta de serviço de rede tem acesso adequado ao certificado e seu arquivo de chave particular correspondente.

 

 





