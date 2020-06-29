---
title: Aplicação de hotfixes no MBAM 2.5 SP1
description: Aplicação de hotfixes no MBAM 2.5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799422"
---
# Aplicação de hotfixes no MBAM 2.5 SP1
Este tópico descreve o processo para aplicar os hotfixes do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) Server 2,5 SP1

### Antes de começar, baixe o hotfix mais recente do Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1
[Desktop Optimization Pack](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> Para obter mais informações sobre as versões de hotfix, consulte o [gráfico de versão do MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).

#### Etapas para atualizar o servidor MBAM para o ambiente MBAM existente 
1. Remova o recurso do servidor do MBAM (faça isso abrindo a ferramenta de configuração do servidor do MBAM e selecionando remover recursos).
2. Remover o MBAM do MDOP do painel de controle | Programas e recursos.
3. Instale os componentes do servidor do MBAM 2,5 SP1 RTM.
4. Instalar o pacote cumulativo de hotfix do MBAM 2,5 SP1 mais recente.
5. Configure os recursos do MBAM usando o configurador do MBAM Server.

#### Etapas para instalar o novo hotfix do servidor do MBAM 2,5 SP1
Consulte o documento para [instalação do novo servidor](deploying-the-mbam-25-server-infrastructure.md).
