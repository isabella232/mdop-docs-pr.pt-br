---
title: Projetar os repositórios de imagens do MED-V
description: Projetar os repositórios de imagens do MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799307"
---
# Projetar os repositórios de imagens do MED-V


Após a criação e a compactação de imagens do MED-V, elas podem ser armazenadas em um servidor de arquivos em qualquer local. Os arquivos podem ser enviados por HTTP ou HTTPS por um ou mais servidores IIS. O repositório de imagens pode ser compartilhado por várias instâncias do MED-V.

Para projetar os repositórios de imagens, primeiro você deve decidir como as imagens serão implantadas em cada cliente e, se o cliente exigir um repositório de imagens local. Em seguida, cada repositório é projetado e colocado, juntamente com seu servidor IIS correspondente.

## Determinar como as imagens serão implantadas


Para cada espaço de trabalho do MED-V, decida como você planeja implantar imagens do MED-V no cliente. Isso é importante na determinação de quantos repositórios são necessários para armazenar as imagens compactadas, onde esses repositórios serão colocados e, em seguida, projetar esses repositórios.

Imagens compactadas podem ser implantadas das seguintes maneiras:

-   Baixado pela rede a partir de um servidor de distribuição de imagens, que inclui um servidor de arquivos e um servidor IIS.

-   Em mídia removível, como uma unidade USB ou DVD.

-   Pré-preparado para um diretório de repositório de imagens no computador cliente usando um centro de distribuição de software corporativo.

Decida qual método, ou métodos, será usado para implantar imagens do MED-V em cada um dos clientes e se o local exigirá um repositório de imagens.

## Determinar o número de repositórios de imagens


Agora que você determinou o número mínimo de repositórios necessários, adicione mais se qualquer um dos seguintes critérios se aplicar:

-   Razões organizacionais ou normativas para separar as imagens do MED-V – algumas imagens do MED-V podem não ser capazes de coexistir no mesmo repositório. Por exemplo, dados pessoais confidenciais podem exigir armazenamento em um servidor que só esteja disponível para um conjunto limitado de funcionários que precisem de acesso aos dados.

-   Clientes em redes isoladas — se as imagens forem implantadas na rede, determine se qualquer rede está isolada e exija um repositório separado. Por exemplo, as organizações muitas vezes isolam redes de laboratório de redes de produção.

-   Clientes em redes remotas — se as imagens forem implantadas na rede, algumas máquinas cliente poderão ser separadas do repositório por links de rede com largura de banda insuficiente para fornecer uma experiência adequada quando um cliente carregar um espaço de trabalho do MED-V. Se necessário, crie instâncias do MED-V adicionais para atender a essa necessidade.

Adicione esses repositórios ao design. Escolha um nome para cada repositório e o motivo para criá-lo. Decida quais imagens do MED-V serão mantidas pelos repositórios e quais clientes do MED-V carregará os espaços de trabalho do MED-V com imagens do repositório.

## Criar e colocar os repositórios de imagens


Quando uma nova imagem está disponível para clientes, os clientes começam a baixar a imagem, possivelmente simultaneamente. Isso cria uma demanda alta no repositório e deve ser levado em conta durante a criação do repositório de imagens.

Para cada repositório, determine a quantidade de dados que será armazenada. Somar os tamanhos das imagens que serão armazenadas no repositório. Esse é o valor do espaço em disco necessário no servidor de arquivos.

Em seguida, adicione o número de clientes que podem baixar imagens do MED-V do repositório. Este é o número máximo de downloads simultâneos que podem ocorrer quando uma nova imagem do MED-V é carregada no repositório. O servidor de arquivos deve ser projetado com um subsistema de disco que pode atender às demandas de e/s que isso criará.

O repositório de imagens pode residir no mesmo sistema do servidor MED-V e do servidor que executa o SQL Server, ou em um compartilhamento de arquivos remoto. Você também pode executá-lo em uma VM do Windows Server2008 Hyper-V. Verifique o local de rede dos clientes que o repositório de imagens vai atender e coloque o repositório em um local de rede onde ele terá largura de banda suficiente para atender às expectativas de nível de serviço desses clientes.

### Tolerância a falhas

Se o repositório de imagens não estiver disponível, os clientes não poderão baixar imagens do MED-V novas ou atualizadas. Para criar opções de tolerância a falhas para o servidor de arquivos e discos tolerantes a falhas, consulte o guia [planejamento e design de infraestrutura Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .

## Projetar e colocar os servidores IIS


Esta seção só será relevante se os clientes baixarem arquivos de imagem pela rede usando HTTP ou HTTPS.

O servidor IIS pode coexistir no mesmo sistema que o servidor MED-V e o servidor que executa o SQL Server. Ele também pode ser executado em uma VM do Windows Server2008 Hyper-V. A infraestrutura do servidor IIS deve ter throughput suficiente para fornecer imagens aos clientes nas expectativas do nível de serviço da organização. Ele deve ser projetado com um subsistema de disco que possa atender às demandas de e/s que isso cria.

Para cada repositório de imagens, some o número de clientes que podem baixar imagens do MED-V usando o IIS. Este é o número máximo de downloads simultâneos que podem ocorrer quando uma imagem é carregada no repositório. Use a soma da taxa de serviço e as expectativas de nível de serviço determinadas em [definir o escopo do projeto](define-the-project-scope.md) para planejar o design da infraestrutura do servidor IIS e para determinar a quantidade apropriada de largura de banda a ser alocada para o repositório.

Para projetar a infraestrutura do IIS, consulte o guia [planejamento de infraestrutura e design do Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

### Tolerância a falhas

Se a infraestrutura do servidor IIS não estiver disponível, os clientes não poderão baixar imagens novas ou atualizadas. Para configurar a tolerância a falhas, o servidor IIS baseado no Windows Server2008 pode ser colocado em um cluster de failover. Para projetar a tolerância a falhas para a infraestrutura do servidor IIS, consulte o guia [planejamento de infraestrutura e design do Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

## Tópicos relacionados


[Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[Implantando um espaço de trabalho do MED-V usando um pacote de implantação](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





