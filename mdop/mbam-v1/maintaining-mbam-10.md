---
title: Manutenção do MBAM 1.0
description: Manutenção do MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799739"
---
# Manutenção do MBAM 1.0


Depois de concluir todos os planejamentos necessários e, em seguida, implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurar o MBAM para ser executado de forma altamente disponível ao usá-lo para gerenciar operações de criptografia do BitLocker da empresa. As informações nesta seção descrevem opções de alta disponibilidade para o MBAM, além de como mover recursos de servidor do MBAM, se necessário.

## Pacote de gerenciamento MBAM


O pacote de gerenciamento do MicrosoftSystemCenterOperationsManager para MBAM está disponível para download no centro de download da Microsoft.

Esse pacote de gerenciamento monitora as interações críticas na infraestrutura do lado do servidor, como as conexões entre os serviços Web e bancos de dados e as chamadas operacionais entre sites e seu serviço Web de apoio. Ele também carrega as solicitações entre os clientes da área de trabalho e seus respectivos pontos de extremidade do serviço Web de recebimento.

[Pacote de gerenciamento de administração e monitoramento do Microsoft BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## Garantir alta disponibilidade para o MBAM 1,0


O MBAM foi projetado para ser tolerante a falhas. Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente. As informações nesta seção podem ser usadas para configurar uma instalação do MBAM altamente disponível.

[Alta disponibilidade para o MBAM 1.0](high-availability-for-mbam-10.md)

## Mover os recursos do MBAM 1,0 para outro servidor


Quando você precisa mover um recurso de servidor MBAM de um computador servidor para outro, há um pedido específico e as etapas necessárias que devem ser seguidas para evitar perda de produtividade ou dados. Esta seção descreve as etapas que você deve seguir para mover um ou mais recursos de servidor do MBAM para um computador diferente.

[Como Mover os Recursos do MBAM 1.0 para Outro Computador](how-to-move-mbam-10-features-to-another-computer.md)

## Outros recursos para manter o MBAM


[Operações do MBAM 1.0](operations-for-mbam-10.md)

 

 





