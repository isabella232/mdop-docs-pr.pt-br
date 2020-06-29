---
title: Identificar o número de instâncias do MED-V
description: Identificar o número de instâncias do MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799436"
---
# Identificar o número de instâncias do MED-V


Você precisa determinar o número de instâncias do MED-V, além de definir o escopo para cada instância para que você possa projetar a infraestrutura do servidor. Uma instância do MED-V inclui o seguinte:

-   O servidor MED-V e os espaços de trabalho do MED-V armazenados no servidor, incluindo permissões do Active Directory.

-   Um banco de dados do SQL Server que armazena eventos do cliente. O banco de dados pode ser compartilhado por várias instâncias do MED-V.

-   O repositório de imagens para as imagens do MED-V empacotadas. O repositório pode ser compartilhado por várias instâncias do MED-V.

-   O console de gerenciamento usado para criar e compactar imagens e criar espaços de trabalho do MED-V. O console não pode ser usado simultaneamente por várias instâncias do MED-V, mas pode ser desconectado de um servidor MED-V e, em seguida, conectado a um servidor MED-V diferente.

-   Os clientes do MED-V que recebem os espaços de trabalho do MED-V e a autorização para usá-los do servidor.

Instâncias do MED-V separadas não podem ser integradas ou compartilhar espaços de trabalho do MED-V. Portanto, cada instância adicional descentraliza o gerenciamento de virtualização.

## Determine o número de instâncias do MED-V necessárias


Comece pressupondo que você esteja usando uma instância do MED-V. Em seguida, considere as seguintes condições e adicione mais instâncias para cada condição que se aplica à sua infraestrutura.

-   Número de usuários com suporte — cada instância do MED-V pode oferecer suporte a até 5.000 clientes ativos simultaneamente. Simultaneamente ativo significa que o cliente está online com o servidor MED-V e envia Polls para o servidor para obter atualizações de políticas e imagens, bem como eventos. Se sua infraestrutura incluir mais de 5.000 usuários ativos, adicione uma instância para cada 5.000 usuários.

-   Usuários em domínios não confiáveis – as permissões do espaço de trabalho do MED-v Server associa o espaço de trabalho do MED-V do Active Directory com usuários e/ou grupos do Active Directory. Isso exige que os usuários do MED-V existam dentro do limite de confiança do servidor MED-V. Adicione uma instância do MED-V para cada grupo de usuários do MED-V que está em um domínio separado e não confiável.

-   Clientes em redes isoladas — determine se todos os clientes residem em redes isoladas e, portanto, exigem uma instância do MED-V separada. Por exemplo, as organizações muitas vezes isolam redes de laboratório de redes de produção. Adicione uma instância do MED-V a cada rede isolada que conterá clientes MED-V.

-   Requisitos organizacionais — a organização pode exigir que um grupo de clientes seja gerenciado por uma instância do MED-V separada por motivos de segurança, como quando aplicativos confidenciais são entregues somente a um conjunto restrito de usuários em um domínio. Por exemplo, o departamento de folha de pagamento pode negar aos usuários de outros departamentos acesso à instância do MED-V que armazena a política para processamento de folha de pagamento. Além disso, se a organização usa um modelo de gerenciamento distribuído, uma instância do MED-V separada pode ser necessária para cada grupo de negócios com clientes MED-V a fim de permitir que o grupo Gerencie seu próprio ambiente virtualizado. Adicione uma instância do MED-V para cada requisito organizacional individual.

-   Considerações legais: problemas nacionais de segurança ou privacidade e leis fiduciárias podem exigir a separação de certos dados ou impedir que outros dados ultrapassem as bordas nacionais. Se necessário, adicione mais instâncias do MED-V para atender a essa necessidade.

Depois de determinar o número de instâncias do MED-V necessárias para sua infraestrutura, bem como o raciocínio para cada uma, forneça um nome para cada instância.

 

 





