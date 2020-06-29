---
title: Atualização do MBAM 2,5 para o MBAM 2,5 SP1 atualização da versão de manutenção
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796082"
---
# Atualização do MBAM 2,5 para o MBAM 2,5 SP1 atualização da versão de manutenção

Este artigo fornece instruções passo a passo para fazer a atualização do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para MBAM 2,5 Service Pack 1 (SP1) junto com o [Microsoft Desktop Optimization Pack (MDOP) pode 2019 atualização de serviço](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) em uma configuração autônoma.

Neste guia, usaremos uma configuração de dois servidores. Um servidor será um servidor de banco de dados que está executando o Microsoft SQL Server 2016. Este servidor hospedará os bancos de dados e relatórios do MBAM. O outro servidor será um servidor Web do Windows Server 2012 R2. Este servidor irá hospedar "administração e monitoramento" e "portal de autoatendimento".

## Preparar-se para atualizar o MBAM 2,5 SP1

### Conheça os servidores do MBAM em seu ambiente

1. Mecanismo de banco de dados do SQL Server: Server que hospeda os bancos de dados do MBAM.
2. SQL Server Reporting Services: Server que hospeda os relatórios do MBAM.
3. Servidores Web dos serviços de informações da Internet (IIS): servidor que hospeda aplicativos Web do MBAM e serviços do MBAM.
4. Adicionais Servidor de site primário do Microsoft System Center Configuration Manager: o aplicativo de configuração do MBAM é executado neste servidor para integrar relatórios do MBAM com o Configuration Manager. Esses relatórios são mesclados com os relatórios do Configuration Manager existentes na instância do SQL Server Reporting Services (SSRS) do Configuration Manager.

### Identificar contas de serviço, grupos, nome do servidor e URL de relatórios

1. Identifique a conta de serviço do pool de aplicativos do MBAM que é usada pelos servidores Web do IIS para ler e gravar dados em bancos de dados do MBAM.
2. Identifique os grupos que são usados durante a configuração de recursos da Web do MBAM e a URL do serviço Web relatórios.
3. Identifique o nome do SQL Server e o nome da instância. Assista a este vídeo para saber mais.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identifique a conta do SQL Server Reporting Services que é usada para ler dados de conformidade do banco de dados de conformidade e auditoria. Assista a este vídeo para saber mais.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Atualize a infraestrutura do MBAM para a versão mais recente disponível

A instalação ou atualização da infraestrutura do servidor MBAM é sempre executada na ordem listada abaixo:

- Mecanismo de banco de dados do SQL Server: bancos de dados
- SQL Server Reporting Services: relatórios
- Servidor Web: aplicativos Web
- Servidor SCCM: relatórios integrados do SCCM, se aplicável
- Clientes: agente do MBAM ou atualização do cliente
- Modelos de política de Grupo: atualizar a política de grupo existente com novos modelos e habilitar novas configurações em uma política de grupo MBAM existente

> [!NOTE]
> Recomendamos que você crie um backup completo do banco de dados dos bancos de dados do MBAM antes de executar as atualizações.

### Atualizar o MBAM SQL Server

Assista a este vídeo para saber como atualizar o MBAM SQL Server:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Atualizar o servidor Web do MBAM

Assista a este vídeo para saber como atualizar o servidor Web do MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Mais informações

Para obter mais informações sobre problemas conhecidos no MBAM 2,5 SP1, consulte [notas de versão para MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
