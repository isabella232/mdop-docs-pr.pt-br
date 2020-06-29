---
title: Implantação da Atualização da Versão de Idioma do MBAM 1.0
description: Implantação da Atualização da Versão de Idioma do MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796096"
---
# Implantação da Atualização da Versão de Idioma do MBAM 1.0


O lançamento do idioma do Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 é uma atualização do MBAM e inclui o suporte de novos idiomas. Os novos idiomas são:

-   Inglês (en-US)

-   Francês (FR)

-   Italiano (TI)

-   Alemão (de)

-   Espanhol (es)

-   Coreano (KO)

-   Japonês (ja)

-   Português (Brasil) Português (Portugal-br)

-   Russo (ru)

-   Chinês tradicional (zh-TW)

-   Chinês simplificado (ZH-CN)

A atualização de idioma do MBAM 1.0 alterará o número de versão de MBAM 1.0.1237.1 para MBAM 1.0.2001.

Você não precisa reinstalar todos os recursos MBAM para adicionar esses idiomas adicionais. Este tópico define as etapas necessárias para adicionar os idiomas recentemente aceitos.

## Implantar o MBAM International Release to MBAM Server Features


Para começar, você deve atualizar os seguintes recursos do MBAM Server:

-   Relatório de conformidade e auditoria

-   Servidor de administração e monitoramento

-   Modelos de política

Em seguida, você deve executar o **MbamSetup.exe** para atualizar os recursos do MBAM que são executados no mesmo servidor ao mesmo tempo.

[Como instalar a atualização de idiomas do MBAM em um servidor único](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[Como instalar a atualização de idioma do MBAM em servidores distribuídos](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## Instalar a atualização de idioma do MBAM para políticas de grupo


Os modelos de política de grupo do MBAM podem ser instalados em cada estação de trabalho de gerenciamento ou podem ser copiados para o repositório central de política de grupo, a fim de disponibilizar os modelos para todos os administradores de política de grupo. Os modelos de política não podem ser instalados diretamente em um controlador de domínio. Se você não usar um repositório central de políticas de grupo, deverá copiar as políticas manualmente para cada controlador de domínio que gerencia a política de grupo do MBAM.

Para adicionar os modelos de diretivas de idioma do MBAM, copie os arquivos de idioma da política de grupo do%SystemRoot%\\PolicyDefinitions no computador em que a função "modelos de política" foi instalada no mesmo local no computador da estação de trabalho. Veja alguns exemplos de arquivos de política de Grupo:

-   BitLockerManagement. admx

-   BitLockerUserManagement. admx

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   fr-fr\\ BitLockerManagement. adml

-   fr-fr\\ BitLockerUserManagement. adml

-   (e, da mesma forma, para cada idioma com suporte)

## Problemas conhecidos do lançamento do MBAM International


Este tópico contém problemas conhecidos para a atualização do Microsoft BitLocker Administration and Monitoring International.

[Problemas Conhecidos na Versão Internacional do MBAM](known-issues-in-the-mbam-international-release-mbam-1.md)

## Outros recursos para implantar a atualização de idioma do MBAM 1,0


[Implantando o MBAM 1.0](deploying-mbam-10.md)

 

 





