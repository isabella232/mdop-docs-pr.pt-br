---
title: Sobre o Application Virtualization Sequencer
description: Sobre o Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797637"
---
# Sobre o Application Virtualization Sequencer


O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra todos os processos de instalação e configuração de um aplicativo e cria os seguintes arquivos: **ico**, **OSD**, **SFT**e **SPRJ**. Esses arquivos contêm todas as informações necessárias sobre um aplicativo para que o aplicativo possa ser executado em um ambiente virtual em computadores de destino. Você pode usar o sequenciador do Microsoft Application Virtualization (App-V) para criar aplicativos virtuais. Depois de sequenciar um aplicativo, ele pode ser transmitido para computadores de destino ou os computadores de destino podem executar o aplicativo virtual baixando o conteúdo do pacote de aplicativo virtual e executando o aplicativo localmente.

**Importante**  Para executar um pacote de aplicativo virtual, o computador de destino deve estar executando a versão adequada do cliente App-V.

 

Os pacotes de aplicativos virtuais são executados em computadores de destino sem interagir com o sistema operacional subjacente no computador de destino porque cada aplicativo é executado em um ambiente virtual e é isolado de outros aplicativos instalados ou em execução no computador de destino. Esse isolamento pode reduzir conflitos de aplicativos e pode ajudar a diminuir a quantidade necessária de testes de pré-implantação de aplicativos.

## Terminologia do sequenciador


<a href="" id="application-virtualization-drive"></a>Unidade de virtualização do aplicativo  
A unidade virtualização de aplicativo é a unidade padrão (Q:\) no computador de destino a partir do qual os aplicativos sequenciados são executados.

<a href="" id="ico-file"></a>Arquivo ICO  
O arquivo de ícone na área de trabalho do cliente que é usado para iniciar um aplicativo sequenciado.

<a href="" id="installation-directory"></a>Diretório de instalação  
O diretório usado pelo sequenciador para colocar os arquivos de instalação durante a instalação.

<a href="" id="open-software-descriptor--osd--file"></a>Abrir arquivo descritor de software (OSD)  
Um arquivo baseado em XML que instrui o cliente App-V a recuperar o aplicativo sequenciado do servidor de streaming App-V e como executar o aplicativo sequenciado no ambiente virtual.

<a href="" id="package-root-directory"></a>Diretório raiz do pacote  
O diretório no computador de sequenciamento em que os arquivos do pacote do aplicativo sequenciado são instalados. Esse diretório também existe virtualmente no computador para o qual um aplicativo sequenciado será transmitido.

<a href="" id="sequenced-application"></a>Aplicativo sequenciado  
Um aplicativo que foi monitorado pelo sequenciador, dividido em blocos de recursos primário e secundário, transmitido para um computador de destino que executa o cliente App-V t e executa um ambiente virtual.

<a href="" id="sequenced-application-package"></a>Pacote de aplicativo sequenciado  
Os arquivos que compõem um aplicativo virtual e permitem que um aplicativo virtual seja executado. Esses arquivos são criados após o sequenciamento e incluirão os arquivos. **OSD**, **. sft**, **. sprj**e **. ico** de maneira específica.

<a href="" id="sequencing"></a>Sequenciamento  
O processo de criação de um pacote de aplicativo usando o sequenciador App-V. Nesse processo, um aplicativo é monitorado, seus atalhos são configurados e um pacote de aplicativo sequenciado é criado.

<a href="" id="sequencing-computer"></a>Sequenciando computador  
O computador usado para sequenciar um aplicativo.

<a href="" id="virtual-application"></a>Aplicativo virtual  
Um aplicativo empacotado pelo sequenciador para ser executado em um ambiente virtual autônomo. O ambiente virtual contém as informações necessárias para executar o aplicativo no cliente sem instalar o aplicativo localmente.

<a href="" id="primary-feature-block"></a>Bloco de recursos primário  
O conteúdo mínimo em um pacote de aplicativo virtual que é necessário para que um aplicativo seja executado em um computador de destino. O conteúdo no bloco de recursos principal é identificado durante a fase de aplicação do sequenciamento e normalmente consiste no conteúdo dos recursos de aplicativo mais usados.

## <a href="" id="sequencing-applications-"></a>Sequenciando aplicativos


Há dois métodos para criar e modificar pacotes de aplicativos virtuais em seu ambiente. O primeiro método é usar o assistente de **sequenciamento** . O assistente de **sequenciamento** permite que você crie novos ou modifique pacotes de aplicativos virtuais existentes. Para obter mais informações sobre como usar o assistente de **sequenciamento** , consulte [como sequenciar um novo aplicativo](how-to-sequence-a-new-application.md). O segundo método é usando a linha de comando. A linha de comando permite que você crie novos ou modifique pacotes de aplicativos virtuais existentes usando o prompt de comando. Para obter mais informações sobre como usar a linha de comando, consulte [como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-using-the-command-line.md).

O assistente de **sequenciamento** fornece as seguintes funções para a criação de pacotes de aplicativos virtuais:

1.  **Configuração do pacote**: o assistente de **sequenciamento** solicita informações de configuração do pacote necessárias para concluir o arquivo do descritor de software aberto (OSD), que é um arquivo obrigatório para iniciar um pacote de aplicativo sequenciado.

2.  **Instalação do aplicativo**: o assistente de **sequenciamento** coleta informações sobre as configurações de instalação e inicialização de um aplicativo. Ele monitora e registra as informações de instalação e inicialização associadas ao aplicativo para criar os arquivos necessários para um pacote de aplicativo virtual.

3.  **Inicialização do aplicativo**: o assistente de **sequenciamento** coleta informações para compilar e ordenar os blocos de código necessários para executar a inicialização inicial do pacote do aplicativo sequenciado no computador de destino. A compilação do bloco de código é referida como o bloco de recursos principal.

## Considerações de segurança do sequenciador do Application Virtualization


O sequenciador App-V executa todos os serviços detectados no tempo de sequenciamento usando a conta do sistema local e não aplica os descritores de segurança nas solicitações de controle de serviço. Se o serviço foi instalado usando uma conta de usuário diferente ou se os descritores de segurança destinam-se a conceder permissões de serviço específicas a grupos de usuários diferentes, considere cuidadosamente se o serviço deve ser virtualizado. Em alguns casos, você deve instalar o serviço localmente para garantir que a segurança do serviço pretendida seja preservada.

**Importante**  Você deve sempre salvar pacotes de aplicativos virtuais em um local seguro.

 

## Tópicos relacionados


[Visão geral do Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





