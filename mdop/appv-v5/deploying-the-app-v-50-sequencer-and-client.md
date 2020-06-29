---
title: Implantação do sequenciador e do cliente App-V 5.0
description: Implantação do sequenciador e do cliente App-V 5.0
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796539"
---
# Implantação do sequenciador e do cliente App-V 5.0


O sequenciador e o cliente do App-V 5,0 permitem aos administradores virtualizar e executar aplicativos virtualizados.

## Implantar o cliente


O cliente App-V 5,0 é o componente que executa um aplicativo virtualizado em um computador de destino. O cliente permite que os usuários interajam com ícones e clique duas vezes em tipos de arquivo, para que eles possam iniciar um aplicativo virtualizado. O cliente também pode obter o conteúdo do aplicativo virtual do servidor de gerenciamento.

[Como implantar o cliente do App-V](how-to-deploy-the-app-v-client-gb18030.md)

[Como desinstalar o cliente do App-V 5.0](how-to-uninstall-the-app-v-50-client.md)

[Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## Definições de configuração do cliente


O cliente App-V 5,0 armazena sua configuração no registro. Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro. Você também pode configurar várias ações do cliente alterando as entradas do registro.

[Sobre as configurações do cliente](about-client-configuration-settings.md)

## Configurar o cliente usando o modelo ADMX e a política de grupo


Você pode usar o modelo ADMX da Microsoft para definir as configurações do cliente para o cliente do App-V 5,0 e o cliente de serviços de área de trabalho remota. O modelo ADMX gerencia configurações comuns do cliente usando uma infraestrutura de política de grupo existente e inclui configurações para a configuração do cliente do App-V 5,0.

**Importante**  Você pode obter o modelo ADMX do App-V 5,0 a partir do centro de download da Microsoft.

 

Depois de baixar e instalar o modelo ADMX, execute as seguintes etapas no computador que você usará para gerenciar a política de grupo. Geralmente, esse é o controlador de domínio.

1.  Salve o arquivo **. admx** no seguinte diretório: **Windows \ \ policyDefinitions**

2.  Salve o arquivo **. adml** no seguinte diretório: **Windows \ \ policyDefinitions \ \ &lt; diretório &gt; de idioma**

Depois de concluir as etapas anteriores, você pode gerenciar as configurações de cliente do App-V 5,0 com o console de **Gerenciamento de política de grupo** .

O cliente App-V 5,0 também armazena sua configuração no registro. Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro. Você também pode configurar várias ações do cliente alterando as entradas do registro.

[Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## Implantar o cliente usando o modo de repositório de conteúdo compartilhado


O modo SCS (Shared Content Store) do App-V 5,0 permite que os clientes do SCS App-V 5,0 executem aplicativos virtualizados sem salvar qualquer um dos dados de pacote associados localmente. Todos os dados obrigatórios de pacotes virtualizados são transmitidos na rede; Portanto, você deve usar somente o modo SCS em ambientes com conexão rápida. Os serviços de área de trabalho remota (RDS) e a versão padrão do cliente App-V 5,0 são compatíveis com o modo SCS.

**Importante**  Se o cliente do App-V 5,0 estiver configurado para ser executado no modo SCS, o local em que os pacotes do App-V 5,0 são transmitidos deve estar disponível, caso contrário, o pacote virtualizado falhará. Além disso, não recomendamos a implantação de aplicativos virtualizados em computadores que executam o cliente App-V 5,0 no modo SCS na Internet.

 

Além disso, o SCS não é um local físico que contém pacotes virtualizados. É um modo que permite que o cliente App-V 5,0 transmita os dados de pacote virtualizados necessários na rede.

O modo SCS é útil nos seguintes cenários:

-   Implantações de infraestrutura de área de trabalho virtual (VDI)

-   Implantações de serviços de área de trabalho remota (RDS)

Para usar o SCS em seu ambiente, você deve habilitar o cliente App-V 5,0 para ser executado no modo SCS. Essa configuração deve ser especificada durante a instalação. Por padrão, o cliente não está configurado para usar o modo SCS. Você deve instalar o cliente usando o procedimento sugerido se planeja usar o SCS. No entanto, você pode configurar um cliente App-V 5,0 existente para ser executado no modo SCS inserindo o seguinte comando do PowerShell no computador que executa o cliente App-V 5,0:

**Set-AppvClientConfiguration-SharedContentStoreMode 1**

Pode haver casos em que o administrador pré-carrega alguns aplicativos virtuais no computador que executa o cliente App-V 5,0 no modo SCS. Isso pode ser feito com comandos do PowerShell para adicionar, publicar e montar o pacote. Por exemplo, se um pacote é pré-carregado em todos os computadores, o administrador pode adicionar, publicar e montar o pacote usando comandos do PowerShell. O pacote não transmitiria pela rede porque seria armazenado localmente.

[Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## Implantar o sequenciador


O sequenciador é uma ferramenta usada para converter aplicativos padrão em pacotes virtuais para implantação em computadores que executam o cliente App-V 5,0. O sequenciador ajuda a fornecer um processo de conversão simples e previsível com alterações mínimas nos fluxos de trabalho de sequenciamento anteriores. Além disso, o sequenciador permite aos usuários configurar aplicativos com mais facilidade para permitir conexões de aplicativos virtualizados.

Para obter uma lista de alterações no sequenciador do App-V 5,0, confira [novidades no app-v 5,0](whats-new-in-app-v-50.md).

[Como instalar o sequenciador](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> Logs do cliente e do sequenciador do App-V 5,0


Você pode usar as informações do log do sequenciador do App-V 5,0 para ajudar a solucionar problemas de instalação e eventos operacionais do sequenciador ao usar o App-V 5,0. As informações do log relacionadas ao sequenciador podem ser analisadas com o **Visualizador de eventos**. A linha a seguir exibe o caminho específico para eventos relacionados ao sequenciador:

**Visualizador de eventos \ \ aplicativos e logs de serviços \ \ Microsoft \ \ App V**. Os eventos relacionados ao sequenciador são anexados ao **AppV \ _Sequencer**. Os eventos relacionados ao cliente são anexados ao **AppV \ _Client**.

No App-V 5,0 SP3, alguns registros foram consolidados. Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## Outros recursos para a implantação do sequenciador e do cliente


[Implantação do App-V 5.0](deploying-app-v-50.md)

[Planejamento para o App-V 5.0](planning-for-app-v-50-rc.md)






 

 





