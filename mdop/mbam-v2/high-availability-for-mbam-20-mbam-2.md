---
title: Alta disponibilidade para o MBAM 2.0
description: Alta disponibilidade para o MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799530"
---
# Alta disponibilidade para o MBAM 2.0


Este tópico fornece informações básicas sobre uma instalação altamente disponível do Microsoft BitLocker Administration and Monitoring (MBAM). Não há suporte total para cenários de alta disponibilidade nesta versão do MBAM para que eles não sejam descritos aqui. É recomendável Pesquisar Blogs e fóruns relacionados, onde os usuários descrevem como eles configuraram com êxito a alta disponibilidade para o MBAM em seus ambientes.

## Cenários de alta disponibilidade para MBAM


A administração e o monitoramento do Microsoft BitLocker são projetados para serem tolerantes a falhas. Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente. Por exemplo, se o agente do MBAM não puder se conectar ao servidor Web do MBAM, os usuários não devem ser solicitados a confirmar a ação.

Ao planejar a instalação do MBAM, considere os seguintes itens, que podem afetar a disponibilidade do serviço MBAM:

-   Criptografia de unidade e senha de recuperação – se não for possível a caução de uma senha de recuperação, a criptografia não será iniciada no computador cliente.

-   Upload de dados de status de conformidade – se o servidor que hospeda o serviço de relatório de status de conformidade não estiver disponível, os dados de conformidade não permanecerão atualizados.

-   Acesso à chave de recuperação do suporte técnico-se o suporte técnico não conseguir acessar as informações do banco de dados do MBAM, o suporte técnico não poderá fornecer chaves de recuperação para os usuários.

-   Disponibilidade de relatórios – se o servidor que hospeda os relatórios de conformidade e auditoria não estiver disponível, os relatórios não estarão disponíveis.

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a>Como o MBAM backup usa o VSS (Volume Shadow Copy Service)


O MBAM 2.0 oferece um gravador VSS (Volume Shadow Copy Service), chamado de Microsoft BitLocker Administration and Management Writer, que facilita o backup do banco de dados de conformidade e auditoria e do banco de dados de recuperação.

O instalador do Windows Server do MBAM registra o gravador VSS do MBAM. Qualquer falha durante o registro do gravador VSS faz com que a instalação do servidor do MBAM seja revertida. Em uma topologia em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação são instalados em servidores diferentes, uma instância separada do gravador VSS do MBAM está registrada em cada servidor. O gravador VSS do MBAM depende do gravador VSS do SQL Server. O gravador VSS do SQL Server está registrado como parte da instalação do Microsoft SQL Server. Qualquer tecnologia de backup que usa gravadores VSS para executar o backup pode descobrir o gravador VSS do MBAM.

## Tópicos relacionados


[Manutenção do MBAM 2.0](maintaining-mbam-20-mbam-2.md)

 

 





