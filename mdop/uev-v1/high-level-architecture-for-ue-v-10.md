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
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800004"
---
# Arquitetura de alto nível para a UE-V 1.0


Este tópico descreve os elementos arquitetônicos de alto nível da solução de roaming de configurações do Microsoft User Experience Virtualization (UE-V). Os elementos a seguir fazem parte de uma implantação padrão do UE-V.

![diagrama arquitetônico do agente do UE-v](images/ue-vagentarchitecturaldiagram.gif)

O UE-V Agent monitora os aplicativos e os processos do sistema operacional conforme eles são identificados nos modelos de local das configurações do UE-V. Quando o aplicativo ou sistema operacional é iniciado, as configurações são lidas do pacote de configurações e aplicadas ao computador. Quando o aplicativo é fechado ou quando o sistema operacional está bloqueado ou desligado, as configurações são salvas em um pacote de configurações de UE-V no local de armazenamento configurações.

## Local de armazenamento de configurações


O local de armazenamento de configurações é um compartilhamento de arquivos que o agente de virtualização da experiência do usuário acessa para as configurações de leitura e gravação. Este local é o diretório base do Active Directory ou definido durante a instalação do UE-V. Você pode definir o local durante a instalação do UE-V Agent ou pode configurá-lo mais tarde com política de grupo, WMI ou PowerShell. O local pode estar em qualquer compartilhamento de arquivo comum que os usuários possam acessar. Se nenhuma configuração de local de armazenamento for definida durante a instalação, o UE-V usará o diretório base no Active Directory. O UE-V Agent verifica o local e cria uma pasta do sistema que está oculta do usuário para armazenar e acessar as configurações do usuário. Para obter mais informações sobre o armazenamento de configurações, consulte [preparando seu ambiente para UE-V](preparing-your-environment-for-ue-v.md).

## UE-V Agent


O UE-V Agent está instalado em cada computador com configurações sincronizadas pela virtualização da experiência do usuário. O agente monitora os aplicativos registrados e o sistema operacional em busca de alterações feitas nas configurações e sincroniza essas configurações entre computadores. As configurações são aplicadas do local de armazenamento de configurações ao aplicativo quando o aplicativo é iniciado. As configurações serão salvas novamente no local de armazenamento de configurações quando o aplicativo for fechado. As configurações do sistema operacional são aplicadas quando o usuário faz logon, quando o computador é desbloqueado ou quando o usuário se conecta remotamente ao computador usando o RDP (protocolo de área de trabalho remota). O agente salva as configurações quando o usuário faz logoff, quando o computador está bloqueado ou quando uma conexão remota é desconectada. Para obter mais informações sobre o UE-V Agent, consulte [preparando seu ambiente para UE-v](preparing-your-environment-for-ue-v.md).

## <a href="" id="bkmk-settingslocationtemplate"></a>Modelos de local de configurações


O modelo de local de configurações é um arquivo XML que define os locais de configurações a serem monitorados pela virtualização da experiência do usuário. Somente as configurações locais definidas nesses modelos de configurações são capturadas ou aplicadas em computadores que executam o UE-V Agent. O modelo de local de configurações não contém valores de configurações, somente os locais onde os valores são armazenados no computador.

O UE-V inclui um conjunto de modelos de local de configurações que especificam locais de configurações para alguns aplicativos e configurações do Windows. Um administrador pode criar modelos de local de configurações personalizadas usando o UE-V Generator.

[Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planejar a implantação de modelo personalizado para a UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## Pacotes de configurações


As configurações do aplicativo e as configurações do Windows são armazenadas em pacotes de configurações, que são criados pelo UE-V Agent. Um pacote de configurações é uma coleção das configurações que são representadas nos modelos de local de configurações. Esses pacotes de configurações são compilados, armazenados localmente e, em seguida, copiados para o local de armazenamento de configurações. "Última gravação de WINS" determina quais configurações serão preservadas quando um único usuário sincronizar o mais de um computador com um local de armazenamento. O agente executado em um computador lê e grava no local de configurações independentemente dos agentes executados em outros computadores. As configurações e valores gravados mais recentemente são aplicados quando o próximo agente lê do local de armazenamento de configurações.

![processo de gerador de UE-v](images/ue-vgeneratorprocess.gif)

## Catálogo de modelos de configurações


O catálogo de modelos de configurações é um caminho de pasta em computadores de UE-V ou um compartilhamento de rede de servidor de mensagens (SMB) que armazena todos os modelos de local de configurações personalizadas. O UE-V Agent recupera modelos novos ou atualizados deste local. O UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta. Os modelos que foram adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V Agent. O UE-V Agent cancela o registro dos modelos que foram removidos desta pasta. Os modelos são registrados e não registrados uma vez por dia pelo Agendador de tarefas. Se você usar somente os modelos de local de configurações padrão que estão incluídos no UE-V, um catálogo de modelos de configurações é desnecessário. Para obter mais informações sobre os catálogos de implantação de configurações, consulte [planejando a implantação de modelos personalizados para o UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Gerador de virtualização da experiência do usuário


O gerador de virtualização da experiência do usuário permite criar modelos de local de configurações personalizadas que armazenarão os locais de configurações dos aplicativos que são usados na empresa e que você deseja incluir na solução de configurações de roaming. O gerador do UE-V buscará descobrir os locais dos valores do registro e os arquivos de configurações para os aplicativos e, em seguida, gravará esses locais em um arquivo XML de modelo de local de configurações. Em seguida, você pode distribuir esses modelos de locais de configurações para os computadores dos usuários. O gerador UE-V também permite que um administrador edite um modelo existente ou valide um modelo que foi criado com outro editor de XML.

O gerador do UE-V monitora um aplicativo para descobrir e gravar onde ele armazena suas configurações. Para fazer isso, ele monitora onde o aplicativo lê ou grava na hKey \ _CURRENT \ _USER registro ou nas pastas de arquivo em **usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **roaming e usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **local**.

O processo de descoberta exclui os arquivos e as chaves do registro aos quais o usuário conectado não pode gravar valores. Nenhum deles será incluído no arquivo XML. O processo de descoberta também exclui as chaves do registro e os arquivos associados à funcionalidade central do sistema operacional Windows.

Para obter mais informações sobre o UE-V Generator, consulte [instalando o UE-v Generator](installing-the-ue-v-generator.md).

## Tópicos relacionados


[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Introdução à User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Sobre a User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





