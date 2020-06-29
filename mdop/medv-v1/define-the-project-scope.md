---
title: Definir o escopo do projeto
description: Definir o escopo do projeto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799313"
---
# Definir o escopo do projeto


Ao definir o escopo do projeto, determine o seguinte:

1.  Os usuários finais do MED-V – o local e o número de usuários finais são usados para determinar a localização das instalações do cliente MED-V e o número de instâncias do MED-V, bem como o número e o posicionamento de repositórios de imagens do MED-V.

2.  As imagens da máquina virtual (VM) a serem gerenciadas pelo MED-V – para determinar o método de distribuição de imagens e posicionamento de repositórios de imagens.

3.  As expectativas de nível de serviço da organização — para determinar os requisitos de desempenho e tolerância a falhas para o servidor e o banco de dados do MED-V, bem como o repositório de imagens.

4.  Valide-se com a empresa — Verifique se há uma compreensão completa de como a infraestrutura planejada afeta a empresa.

## Definir os usuários finais do MED-V


Primeiro, determine onde os usuários finais estão localizados, bem como o número de usuários em cada local. Em seguida, obtenha um diagrama de infraestrutura de rede que exiba os locais do usuário e a largura de banda disponível para esses locais. Terceiro, descubra se os usuários viajam entre locais. Se os usuários viajarem, talvez seja necessário capacidade adicional no design dos repositórios de infraestrutura e imagem do servidor.

## Determinar as imagens do MED-V a serem gerenciadas pelo MED-V


Depois que os usuários finais do MED-V tiverem sido definidos, determine quais VMs serão gerenciadas pelo MED-V para os usuários em cada local.

Se qualquer uma das VMs estiver armazenada em uma biblioteca centralizada, determine o local da biblioteca para que ela possa ser avaliada para uso como um repositório do MED-V.

## <a href="" id="determine-the-organization-s-service-level-expectations"></a>Determinar as expectativas de nível de serviço da organização


Para cada espaço de trabalho do MED-V, observe o tempo aceitável para uma nova imagem carregar e o período de tempo para atualizações críticas a serem implantadas.

Se aplicável, registre as expectativas de nível de serviço para relatórios do MED-V a serem usados no design da infraestrutura do servidor.

## Validar com o negócio


Pergunte aos stakeholders de negócios e aos proprietários de aplicativos as seguintes perguntas:

-   Há imagens existentes que possam ser combinadas? Por exemplo, se o aplicativo A em WindowsXP for uma imagem do VPC e o aplicativo B no WindowsXP for outra imagem do VPC, talvez uma única imagem possa conter ambos os aplicativos, reduzindo o espaço do repositório e a largura de banda necessária para o download da imagem.

-   Os aplicativos em escopo são licenciados e compatíveis, se entregues em uma VM pelo MED-V? Consulte o fornecedor do aplicativo para garantir que os termos de licenciamento e suporte não sejam violados ao entregar o aplicativo pelo MED-V.

 

 





