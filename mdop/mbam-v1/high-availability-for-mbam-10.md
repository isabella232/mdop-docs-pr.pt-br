---
title: Alta disponibilidade para o MBAM 1.0
description: Alta disponibilidade para o MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799657"
---
# Alta disponibilidade para o MBAM 1.0


Este tópico descreve como configurar uma instalação altamente disponível do Microsoft BitLocker Administration and Monitoring (MBAM).

## Cenários de alta disponibilidade para MBAM


O Microsoft BitLocker Administration and Monitoring (MBAM) foi projetado para ser tolerante a falhas. Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente. Por exemplo, se o agente do MBAM não puder se conectar ao servidor Web do MBAM, os usuários não devem ser solicitados a confirmar a ação.

Ao planejar a instalação do MBAM, considere as seguintes preocupações que podem afetar a disponibilidade do serviço MBAM:

-   Criptografia de unidade e senha de recuperação – se uma senha de recuperação não puder ser subprecisada, a criptografia não será iniciada no computador cliente.

-   Upload de dados de status de conformidade – se o servidor que hospeda o serviço de relatório de status de conformidade não estiver disponível, os dados de conformidade não permanecerão atuais.

-   Acesso à chave de recuperação do suporte técnico-se o suporte técnico não conseguir acessar as informações do banco de dados do MBAM, não será possível fornecer chaves de recuperação para os usuários.

-   Disponibilidade de relatórios – os relatórios não estarão disponíveis se o servidor que hospeda os relatórios de conformidade e auditoria não estiver disponível.

A principal preocupação para o MBAM High Availability é a disponibilidade da chave de recuperação do BitLocker. Se o suporte técnico não puder fornecer chaves de recuperação, os usuários bloqueados não poderão desbloquear seus computadores. Para evitar esse problema, considere a implementação de servidores da Web redundantes e bancos de dados para garantir alta disponibilidade.

Para obter mais informações sobre a escalabilidade de MBAM e alta disponibilidade, consulte o [White Paper de redimensionamento de MBAM](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Para obter orientação geral sobre a alta disponibilidade do Microsoft SQL Server, consulte [alta disponibilidade](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .

Para obter orientação geral sobre a disponibilidade e a escalabilidade para servidores Web, consulte [disponibilidade e escalabilidade](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## Tópicos relacionados


[Manutenção do MBAM 1.0](maintaining-mbam-10.md)

 

 





