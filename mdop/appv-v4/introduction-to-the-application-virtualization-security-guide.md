---
title: Introdução ao guia de segurança do Application Virtualization
description: Introdução ao guia de segurança do Application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796891"
---
# Introdução ao guia de segurança do Application Virtualization


Este guia de segurança do Microsoft Application Virtualization (App-V) fornece instruções para administradores que são responsáveis por configurar os recursos de segurança que foram selecionados para a implantação do App-V.

**Observação**  Esta documentação não fornece orientação para escolher as opções de segurança específicas. Essas informações são fornecidas no White paper sobre as práticas recomendadas de segurança do App-V disponíveis em <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Como administrador do App-V usando este guia, você deve estar familiarizado com as seguintes tecnologias relacionadas à segurança:

-   Active Directory Domain Services

-   Infraestrutura de chave pública (PKI)

-   Segurança do protocolo Internet (IPsec)

-   Políticas de grupo

-   Serviços de informações da Internet (IIS)

## Componentes da infraestrutura do APP-V


Ao planejar um ambiente Security App-V aprimorado, você pode considerar vários modelos de infraestrutura diferentes.

**Observação**  Para obter mais informações sobre modelos de infraestrutura do App-V, consulte a seguinte documentação:

-   [Guia de planejamento e implantação do App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Planejamento de infraestrutura e série de guias de design](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Esses modelos utilizam alguns, mas possivelmente não todos os componentes do App-V descritos na ilustração a seguir.

![diagrama de filial do App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Servidor de gerenciamento do Application Virtualization (App-V)  
O servidor de gerenciamento do App-V transmite o conteúdo do pacote e publica os atalhos e associações de tipo de arquivo para o cliente App-V. O App-V Management Server também dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Servidor de streaming do Application Virtualization (App-V)  
O servidor de streaming App-V hospeda os pacotes para clientes de streaming para aplicativos do App-V em ambientes como filiais, onde a largura de banda da conexão com o servidor de gerenciamento do App-V é insuficiente para transmitir o conteúdo do pacote para os clientes. O servidor de streaming contém apenas a funcionalidade de streaming e não fornece o console de gerenciamento do App-V ou o serviço Web de gerenciamento do App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Repositório de dados do Application Virtualization (App-V)  
O repositório de dados App-V, no banco de dados SQL, retém as informações relacionadas à infraestrutura do App-V. As informações no repositório de dados App-V incluem todos os registros de aplicativos, atribuições de aplicativo e quais grupos gerenciam o ambiente de virtualização de aplicativos.

<a href="" id="application-virtualization--app-v--management-service"></a>Serviço de gerenciamento do Application Virtualization (App-V)  
O serviço de gerenciamento do App-V comunica solicitações de leitura/gravação ao repositório de dados do Application Virtualization. Esse componente pode ser instalado no mesmo computador que o servidor de gerenciamento do App-V ou em um computador separado com o IIS instalado.

<a href="" id="application-virtualization--app-v--management-console"></a>Console de gerenciamento do Application Virtualization (App-V)  
O console de gerenciamento do App-V é um utilitário de gerenciamento de snap-in para administração do App-V Server. Esse componente pode ser instalado no mesmo computador que o servidor do App-V ou em uma estação de trabalho separada que tenha o MMC 3.0 e o. .NET 2.0 instalado.

<a href="" id="application-virtualization--app-v--sequencer"></a>Sequenciador do Application Virtualization (App-V)  
O sequenciador do App-V monitora e captura a instalação de aplicativos e cria pacotes de aplicativos virtuais. A saída do sequenciador consiste no ícone do aplicativo, o arquivo OSD contendo informações de definição do aplicativo, um arquivo de manifesto do pacote e um arquivo SFT que contém os arquivos de conteúdo do aplicativo. Opcionalmente, um arquivo do Windows Installer pode ser criado para instalar o pacote sem usar a infraestrutura do App-V.

<a href="" id="application-virtualization--app-v--client"></a>Cliente do Application Virtualization (App-V)  
O cliente App-V está instalado no computador cliente da área de trabalho do App-V ou no computador cliente dos serviços de terminal do App-V. Ele fornece o ambiente virtual para os pacotes de aplicativos virtuais. O cliente App-V gerencia o pacote de streaming para o cache, a atualização de publicação de aplicativo virtual e a interação com os servidores de virtualização de aplicativos.

 

 





