---
title: Introdução ao Guia de Segurança de Virtualização de Aplicativos
description: Introdução ao Guia de Segurança de Virtualização de Aplicativos
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
ms.openlocfilehash: 82914de48a5a5777f6ce4b50fe3e8af34dd82494
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910776"
---
# <a name="introduction-to-the-application-virtualization-security-guide"></a>Introdução ao Guia de Segurança de Virtualização de Aplicativos


Este guia de segurança do Microsoft Application Virtualization (App-V) fornece instruções para administradores responsáveis pela configuração dos recursos de segurança selecionados para a implantação do App-V.

**Observação**  
Esta documentação não fornece orientações para escolher as opções de segurança específicas. Essas informações são fornecidas no white paper práticas recomendadas de segurança do App-V disponíveis em <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Como administrador do App-V usando este guia, você deve estar familiarizado com as seguintes tecnologias relacionadas à segurança:

-   Active Directory Domain Services

-   Infraestrutura de chave pública (PKI)

-   Internet Protocol Security (IPsec)

-   Políticas de Grupo

-   Serviços de Informações da Internet (IIS)

## <a name="app-v-infrastructure-components"></a>Componentes de infraestrutura do APP-V


Ao planejar um ambiente app-V de segurança aprimorado, você pode considerar vários modelos de infraestrutura diferentes.

**Observação**  
Para obter mais informações sobre modelos de infraestrutura do App-V, consulte a seguinte documentação:

-   [Guia de Planejamento e Implantação do App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Série de Guias de Planejamento e Design de Infraestrutura](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Esses modelos utilizam alguns, mas possivelmente, nem todos os componentes do App-V representados na ilustração a seguir.

![diagrama de filial do app-v.](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Servidor de Gerenciamento de Virtualização de Aplicativos (App-V)  
O Servidor de Gerenciamento do App-V transmite o conteúdo do pacote e publica os atalhos e associações de tipo de arquivo ao Cliente App-V. O Servidor de Gerenciamento do App-V também oferece suporte a atualização ativa, gerenciamento de licenças e um banco de dados que pode ser usado para relatórios.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Servidor de Streaming de Virtualização de Aplicativos (App-V)  
O Servidor de Streaming do App-V hospeda os pacotes para streaming para Clientes do App-V em ambientes como filiais, onde a largura de banda da conexão com o Servidor de Gerenciamento do App-V é insuficiente para streaming de conteúdo de pacote para clientes. O Servidor de Streaming contém apenas a funcionalidade de streaming e não fornece o Console de Gerenciamento do App-V ou o Serviço Web de Gerenciamento do App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Armazenamento de dados de Virtualização de Aplicativos (App-V)  
O armazenamento de dados do App-V, no banco de dados SQL, mantém informações relacionadas à infraestrutura do App-V. As informações no armazenamento de dados do App-V incluem todos os registros de aplicativos, atribuições de aplicativos e quais grupos gerenciam o ambiente de Virtualização de Aplicativos.

<a href="" id="application-virtualization--app-v--management-service"></a>Serviço de Gerenciamento de Virtualização de Aplicativos (App-V)  
O Serviço de Gerenciamento do App-V comunica solicitações de leitura/gravação ao armazenamento de dados de Virtualização de Aplicativos. Esse componente pode ser instalado no mesmo computador que o Servidor de Gerenciamento do App-V ou em um computador separado com o IIS instalado.

<a href="" id="application-virtualization--app-v--management-console"></a>Console de Gerenciamento de Virtualização de Aplicativos (App-V)  
O Console de Gerenciamento do App-V é um utilitário de gerenciamento de snap-in para a administração do App-V Server. Esse componente pode ser instalado no mesmo computador que o Servidor app-V ou em uma estação de trabalho separada que tenha o MMC 3.0 e o .NET 2.0 instalados.

<a href="" id="application-virtualization--app-v--sequencer"></a>Sequenciador de Virtualização de Aplicativo (App-V)  
O App-V Sequencer monitora e captura a instalação de aplicativos e cria pacotes de aplicativos virtuais. A saída do Sequencer consiste no ícone do aplicativo, no arquivo OSD que contém informações de definição do aplicativo, em um arquivo de manifesto de pacote e em um arquivo SFT que contém os arquivos de conteúdo do aplicativo. Opcionalmente, um arquivo Windows Instalador pode ser criado para instalar o pacote sem usar a infraestrutura do App-V.

<a href="" id="application-virtualization--app-v--client"></a>Cliente de Virtualização de Aplicativos (App-V)  
O Cliente App-V está instalado no computador cliente da Área de Trabalho do App-V ou no computador Cliente de Serviços de Terminal do App-V. Ele fornece o ambiente virtual para os pacotes de aplicativo virtual. O Cliente app-V gerencia o streaming de pacote para o cache, atualização de publicação de aplicativo virtual e interação com os Servidores de Virtualização de Aplicativos.

 

 





