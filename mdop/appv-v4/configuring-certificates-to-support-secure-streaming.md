---
title: Configuração de certificados para dar suporte ao streaming seguro
description: Configuração de certificados para dar suporte ao streaming seguro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798016"
---
# Configuração de certificados para dar suporte ao streaming seguro


Por padrão, o serviço App-V é executado na conta de serviço de rede. No entanto, você pode criar uma conta de serviço nos serviços de domínio Active Directory e substituir a conta de serviço de rede pela conta de domínio do Active Directory.

O contexto de segurança no qual o serviço é executado é importante para configurar comunicações seguras aprimoradas. Esse contexto de segurança deve ter permissões de leitura para a chave privada do certificado. Quando um arquivo PKCS \ #10 *solicitação de assinatura de certificado* (CSR) é gerado para o servidor App-V, o provedor de serviços de *criptografia* do Windows é chamado e uma chave privada é gerada. A chave privada é protegida com permissões dadas apenas às contas de sistema e administrador.

Você deve modificar as listas de controle de acesso (ACLs) na chave privada para permitir que o gerenciamento do App-V ou o Streaming Server acessem a chave privada necessária para comunicações seguras protegidas de TLS.

## Obtendo e instalando um certificado


Os cenários para obter e instalar um certificado para o App-V são os seguintes:

-   Infraestrutura de chave pública interna (PKI).

-   Autoridade de certificação (CA) de emissão de certificados terceirizada.

    **Observação**  Se você precisar obter um certificado de uma autoridade de certificação terceirizada, siga a documentação disponível nesse site da Web da CA.

     

Se uma infraestrutura de PKI foi implantada, consulte os administradores de PKI para adquirir um certificado compatível com os requisitos descritos neste tópico. Se uma infraestrutura de PKI não estiver disponível, use uma CA de terceiros para obter um certificado válido.

Para obter orientação passo a passo para obter e instalar um certificado, consulte <https://go.microsoft.com/fwlink/?LinkId=151969> .

## Tópicos relacionados


Configurar certificados para dar suporte ao streaming seguro [como modificar as permissões de chave privada para o servidor de gerenciamento de suporte ou o Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





