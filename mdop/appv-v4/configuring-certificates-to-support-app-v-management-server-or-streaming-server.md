---
title: Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V
description: Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798017"
---
# Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V


Depois de concluir o processo de provisionamento de certificado e alterar as permissões da chave privada para dar suporte à instalação do App-V, você pode iniciar a configuração do servidor de gerenciamento ou do servidor de transmissão. Durante a configuração, se um certificado for provisionado antes de executar o programa de instalação, o assistente exibirá o certificado na tela **modo de segurança de conexão** e, por padrão, a caixa de seleção **usar segurança aprimorada** estará marcada.

**Observação**  Selecione o certificado que foi configurado para o App-V se houver mais de um certificado provisionado para este servidor.

 

**Importante**  Durante a atualização da versão 4,2 para a versão 4,5, a configuração tem uma opção para **usar a segurança aprimorada**; no entanto, a seleção dessa opção não desabilitará o streaming em RTSP. Você deve usar o console de gerenciamento para desabilitar o RTSP após a instalação.

 

Selecione a porta TCP que o serviço vai usar para comunicações de cliente. A porta padrão é TCP 322; no entanto, você pode mudar a porta para uma porta personalizada do seu ambiente.

As etapas restantes do assistente são as mesmas que se você estivesse implantando um servidor de gerenciamento ou de streaming do App-V sem usar o recurso de **segurança aprimorado** .

## Configurar certificados para ambientes NLB


Para dar suporte a grandes empresas, muitas vezes o servidor de gerenciamento é colocado em um cluster de balanceamento de carga de rede (NLB) para dar suporte ao grande número de conexões. Isso requer pelo menos dois servidores de gerenciamento que parecem ser um único servidor de gerenciamento. Quando o ambiente usa um cluster NLB com vários servidores de gerenciamento, você precisa de uma configuração avançada do certificado usado para o cluster NLB.

O certificado App-V é enviado a uma autoridade de certificação (CA) configurada em um computador com o Windows Server2003. A SAN permite que você se conecte a um nome de host de cluster NLB específico do servidor de gerenciamento usando um nome de sistema de nomes de domínio (DNS) que pode ser diferente dos nomes de computador reais, porque pode haver até 32 servidores que compõem o cluster NLB.

Essa configuração é necessária somente ao usar um cluster NLB. Quando o cliente se conecta ao servidor, ele se conecta usando o nome de domínio totalmente qualificado (FQDN) do cluster NLB e não o FQDN de um servidor individual. Se você não adicionar a propriedade SAN com o FQDN dos nós do servidor no cluster, todas as conexões do cliente serão recusadas porque o nome comum do certificado não corresponderá ao nome do servidor.

Para obter informações mais detalhadas sobre a configuração de certificados com o atributo SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .

## Tópicos relacionados


[Configuração de certificados para dar suporte ao streaming seguro](configuring-certificates-to-support-secure-streaming.md)

[Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





