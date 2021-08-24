---
title: Arquitetura de alto nível para a UE-V 1.0
description: Arquitetura de alto nível para a UE-V 1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b54a9a207f9b74ad3d028cf4ab1f9842d59b0b3a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910446"
---
# <a name="high-level-architecture-for-ue-v-10"></a>Arquitetura de alto nível para a UE-V 1.0


Este tópico descreve elementos arquitetônicos de alto nível da solução de roaming de Microsoft User Experience Virtualization (UE-V). Os elementos a seguir fazem parte de uma implantação UE-V padrão.

![Diagrama de arquitetura do agente ue-v.](images/ue-vagentarchitecturaldiagram.gif)

O UE-V monitora os aplicativos e os processos do sistema operacional conforme eles são identificados nos modelos de local de configurações UE-V configurações. Quando o aplicativo ou sistema operacional é iniciado, as configurações são lidas do pacote de configurações e aplicadas ao computador. Quando o aplicativo fecha ou quando o sistema operacional é bloqueado ou desligado, as configurações são salvas em um pacote de configurações UE-V no local de armazenamento de configurações.

## <a name="settings-storage-location"></a>Configurações local de armazenamento


O local de armazenamento de configurações é um compartilhamento de arquivos que o agente de Virtualização da Experiência do Usuário acessa para configurações de leitura e gravação. Esse local é o diretório residencial do Active Directory ou definido durante a UE-V instalação. Você pode definir o local durante a instalação do agente UE-V, ou pode defini-lo posteriormente com Política de Grupo, WMI ou PowerShell. O local pode estar em qualquer compartilhamento de arquivos comum que os usuários possam acessar. Se nenhum local de armazenamento de configuração for definido durante a instalação, UE-V usará o diretório home no Active Directory. O UE-V agente verifica o local e cria uma pasta do sistema que está oculta do usuário no qual armazenar e acessar as configurações do usuário. Para obter mais informações sobre o armazenamento de configurações, consulte [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).

## <a name="ue-v-agent"></a>UE-V Agente


O UE-V é instalado em cada computador com configurações sincronizadas pela Virtualização da Experiência do Usuário. O agente monitora os aplicativos registrados e o sistema operacional para quaisquer alterações feitas nas configurações e sincroniza essas configurações entre computadores. Configurações são aplicados do local de armazenamento de configurações ao aplicativo quando o aplicativo é iniciado. As configurações são salvas novamente no local de armazenamento de configurações quando o aplicativo é fechado. As configurações do sistema operacional são aplicadas quando o usuário faz o login, quando o computador é desbloqueado ou quando o usuário se conecta remotamente ao computador usando o protocolo de área de trabalho remota (RDP). O agente salva configurações quando o usuário faz o login, quando o computador está bloqueado ou quando uma conexão remota é desconectada. Para obter mais informações sobre o UE-V, consulte [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).

## <a name="settings-location-templates"></a><a href="" id="bkmk-settingslocationtemplate"></a>Configurações de localização


O modelo de local de configurações é um arquivo XML que define os locais de configurações a serem monitorados pela Virtualização da Experiência do Usuário. Somente os locais de configurações definidos nesses modelos de configuração são capturados ou aplicados em computadores que executam o UE-V Agent. O modelo de local de configurações não contém valores de configurações, apenas os locais onde os valores são armazenados no computador.

UE-V inclui um conjunto de modelos de localização de configurações que especificam locais de configurações para alguns aplicativos da Microsoft e Windows configurações. Um administrador pode criar modelos de local de configurações personalizadas usando o UE-V Generator.

[Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planejar a implantação de modelo personalizado para a UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <a name="settings-packages"></a>Configurações pacotes


As configurações de aplicativo e Windows são armazenadas em pacotes de configurações, que são criados pelo agente UE-V. Um pacote de configurações é uma coleção das configurações representadas nos modelos de local de configurações. Esses pacotes de configurações são construídos, armazenados localmente e copiados para o local de armazenamento de configurações. "Last write wins" determina quais configurações são preservadas quando um único usuário sincroniza o mais de um computador com um local de armazenamento. O agente que é executado em um computador lê e grava no local de configurações independente dos agentes que são executados em outros computadores. As configurações e valores gravados mais recentemente são aplicados quando o próximo agente lê do local de armazenamento de configurações.

![Processo do gerador ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-template-catalog"></a>Configurações catálogo de modelos


O catálogo de modelos de configurações é um caminho de pasta em computadores UE-V ou um compartilhamento de rede do SMB (Server Message Block) que armazena todos os modelos de local de configurações personalizadas. O UE-V agente recupera modelos novos ou atualizados desse local. O UE-V verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta. Os modelos que foram adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V agente. O UE-V desregula os modelos que foram removidos dessa pasta. Os modelos são registrados e não registrados uma vez por dia pelo agendador de tarefas. Se você usar apenas os modelos de local de configurações padrão incluídos no UE-V, um catálogo de modelos de configurações será desnecessário. Para obter mais informações sobre configurações de catálogos de implantação, consulte [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).

## <a name="user-experience-virtualization-generator"></a>Gerador de Virtualização da Experiência do Usuário


O Gerador de Virtualização da Experiência do Usuário permite que você crie modelos de local de configurações personalizadas que armazenarão os locais de configurações dos aplicativos usados na empresa e que você deseja incluir na solução de configurações móveis. O UE-V Generator procurará descobrir os locais dos valores do Registro e os arquivos de configurações para aplicativos e registrará esses locais em um arquivo XML de modelo de local de configurações. Em seguida, você pode distribuir esses modelos de localização de configurações para os computadores do usuário. O UE-V generator também permite que um administrador edite um modelo existente ou valide um modelo que foi criado com outro editor XML.

O UE-V Gerador monitora um aplicativo para descobrir e registrar onde armazena suas configurações. Para fazer isso, ele monitora onde o aplicativo lê ou grava no Registro HKEY\_CURRENT\_USER ou nas pastas de arquivo em **Usuários** \\ \[Nome do usuário\] \\ **AppData**  \\  **Roaming and Users** \\ \[Nome do usuário\] \\ **AppData**  \\  **Local**.

O processo de descoberta exclui chaves e arquivos do Registro nos quais o usuário conectado não pode gravar valores. Nenhum deles será incluído no arquivo XML. O processo de descoberta também exclui chaves e arquivos do Registro associados à funcionalidade principal do Windows operacional.

Para obter mais informações sobre o gerador UE-V, consulte [Installing the UE-V Generator](installing-the-ue-v-generator.md).

## <a name="related-topics"></a>Tópicos relacionados


[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Introdução à User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Sobre a User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





