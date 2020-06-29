---
title: Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V
description: Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798015"
---
# Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V


O serviço de gerenciamento da Web App-V deve ser configurado para dar suporte a conexões baseadas em SSL para ajudar a proteger a comunicação. Esse processo requer que o servidor Web ou computador no qual o serviço de gerenciamento está instalado tenha um certificado emitido para o serviço ou computador.

Os cenários a seguir ilustram como obter um certificado para essa finalidade:

1.  A infraestrutura da empresa já tem uma infraestrutura de chave pública (PKI) que emite certificados automaticamente para computadores.

2.  A infraestrutura da empresa já tem uma PKI in-loco, embora não emita certificados automaticamente para computadores.

3.  A infraestrutura da empresa não tem PKI in-loco.

Em cada um dos cenários anteriores, o método para obter um certificado é diferente, mas o resultado final é o mesmo. O administrador deve atribuir um certificado ao site padrão do IIS e configurar o serviço de gerenciamento da Web do App-V para exigir comunicações seguras.

**Importante**  O nome do certificado deve corresponder ao nome do servidor. É uma prática recomendada usar nomes de domínio totalmente qualificados (FQDNs) para o nome comum do certificado.

 

O App-V pode usar os servidores IIS para dar suporte a diferentes configurações de infraestrutura. Para obter mais informações sobre a configuração de servidores IIS para suporte a HTTPS, consulte <https://go.microsoft.com/fwlink/?LinkId=151972> .

## Tópicos relacionados


[Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





