---
title: Planejamento para a implantação do sequenciador e do cliente do App-V 5.1
description: Planejamento para a implantação do sequenciador e do cliente do App-V 5.1
author: dansimp
ms.assetid: d92f8773-fa7d-4926-978a-433978f91202
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 31a0296814b16ba1c776dca522423fc7b6b6ed96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796255"
---
# Planejamento para a implantação do sequenciador e do cliente do App-V 5.1


Antes de começar a usar o Microsoft Application Virtualization (App-V) 5,1, você deve instalar o App-V 5,1 Sequencer, o cliente App-V 5,1 e, opcionalmente, o repositório de conteúdo compartilhado do App-V 5,1. As seções a seguir abordam o planejamento para essas instalações.

## Planejando a implantação do sequenciador do App-V 5,1


O App-V 5,1 usa um processo chamado sequenciamento para criar aplicativos virtualizados e pacotes de aplicativos. O sequenciamento requer o uso de um computador que executa o sequenciador do App-V 5,1.

**Observação**  Para obter informações sobre a nova funcionalidade do App-V 5,1 Sequencer, consulte a seção **melhorias do sequenciador** em [sobre o app-v 5,1](about-app-v-51.md).

 

O computador que executa o sequenciador do App-V 5,1 deve atender aos requisitos mínimos do sistema. Para obter uma lista desses requisitos, consulte [configurações compatíveis do App-V 5,1](app-v-51-supported-configurations.md).

O ideal é que você instale o sequenciador em um computador executado como máquina virtual. Isso permite que você reverta mais facilmente o computador executando o sequenciador para um estado "limpo" antes de sequenciar outro aplicativo. Ao instalar o sequenciador usando uma máquina virtual, você deve executar as seguintes etapas:

1.  Instale todos os pré-requisitos associados do sequenciador.

2.  Instale o sequenciador.

3.  Faça um "instantâneo" do ambiente.

**Importante**  Você deve ter sua equipe de segurança corporativa para revisar e aprovar o plano de processo de sequenciamento. Por motivos de segurança, você deve manter as operações do sequenciador em um laboratório separadas do ambiente de produção. A organização de separação pode ser tão simples ou tão abrangente quanto necessário, de acordo com suas necessidades de negócios. Os computadores de sequenciamento devem ser capazes de se conectar à rede corporativa para copiar pacotes concluídos para os servidores de produção. No entanto, como os computadores de sequenciamento são geralmente operados sem proteção antivírus, eles não devem estar desprotegidos da rede corporativa. Por exemplo, você pode ser capaz de operar atrás de um firewall ou de um segmento de rede isolado. Também é possível usar máquinas virtuais configuradas para compartilhar uma rede virtual isolada. Siga as políticas de segurança da sua empresa para solucionar esses problemas com segurança.

 

## Planejando a implantação do cliente do App-V 5,1


Para executar pacotes virtualizados em computadores de destino, você deve instalar o cliente App-V 5,1 nos computadores de destino. O cliente App-V 5,1 é o componente que executa um aplicativo virtualizado em um computador de destino. O cliente permite que os usuários interajam com ícones e tipos de arquivo específicos para iniciar aplicativos virtualizados. O cliente também ajuda a obter o conteúdo do aplicativo do servidor de gerenciamento e armazena o conteúdo em cache antes de o cliente iniciar o aplicativo. Há dois tipos de cliente diferentes: o cliente para serviços de área de trabalho remota, que é usado em sistemas de servidor host de sessão de área de trabalho remota (host de sessão de área de trabalho remota) e no cliente App-V 5,1, que é usado para todos os outros computadores.

O cliente App-V 5,1 deve ser configurado usando a linha de comando do instalador ou usando um script do PowerShell após a conclusão da instalação.

As configurações devem ser definidas cuidadosamente com antecedência para agilizar a implantação do software cliente App-V 5,1. Isso é especialmente importante quando você tem computadores em escritórios diferentes em que os clientes devem ser configurados para usar locais de origem diferentes.

Você também deve determinar como vai implantar o software cliente. Embora seja possível implantar o cliente manualmente em cada computador, a maioria das organizações prefere implantar o cliente por meio de um processo automatizado. Uma organização maior pode ter um sistema ESD (Electronic Software Distribution) operacional, que é um sistema de implantação de cliente ideal. Se não houver um sistema ESD, você pode usar o método padrão de instalação do software da sua organização. Os métodos possíveis incluem política de grupo ou várias técnicas de script. Dependendo da quantidade e dos locais diferentes dos computadores cliente, esse processo de implantação pode ser complexo. Você deve usar uma abordagem estruturada para garantir que todos os computadores tenham o cliente instalado com a configuração correta.

Para obter uma lista dos requisitos mínimos do cliente [, consulte pré-requisitos do App-V 5,1](app-v-51-prerequisites.md).

## <a href="" id="bkmk-client-coexist"></a>Planejamento para a coexistência do cliente App-V


Você pode implantar o cliente do App-V 5,1 lado a lado com o cliente App-V 4,6. A coexistência de cliente requer que você adicione ou publique aplicativos virtualizados usando um arquivo de configuração de implantação ou um arquivo de configuração do usuário, pois há certas configurações nesses arquivos de configuração que devem ser configuradas para que o App-V 5,1 funcione com os clientes do App-V 4.6. Quando um pacote é atualizado usando o cliente ou o servidor, o pacote deve reenviar o arquivo de configuração. Isso é verdadeiro para qualquer pacote que tenha um arquivo de configuração correspondente, para que ele não seja específico da coexistência do cliente. No entanto, se você não enviar o arquivo de configuração durante a atualização do pacote, o estado do pacote não funcionará como esperado nos cenários de coexistência.

Arquivos de configuração dinâmica do App-V 5,1 personalizam um pacote para um usuário específico. Você deve criar o arquivo de configuração dinâmica do usuário (. xml) ou o arquivo de configuração de implantação dinâmica antes de poder usá-los. Para criar o arquivo, ele exige uma operação manual avançada.

Quando um arquivo de configuração de usuário dinâmico é usado, nenhuma das informações do App-V 5,1 para a extensão no arquivo de manifesto é usada. Isso significa que o arquivo de configuração de usuário dinâmico deve incluir tudo para a extensão específica do App-V 5,1 no arquivo de manifesto, bem como as alterações que você deseja fazer, como exclusões e atualizações. Para obter mais informações sobre como criar um arquivo de configuração personalizado, consulte [como criar um arquivo de configuração personalizado usando o console de gerenciamento do App-V 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

## <a href="" id="bkmk-plan-for-scs"></a>Planejando a App-V 5,1 Shared Content Store (SCS)


O modo de repositório de conteúdo compartilhado do App-V 5,1 permite que o computador executando o cliente App-V 5,1 para executar aplicativos virtualizados e nenhum dos conteúdos do pacote seja salvo no computador que está executando o cliente App-V 5,1. Os aplicativos virtuais são transmitidos para computadores de destino somente quando solicitados pelo cliente.

A lista a seguir mostra alguns dos benefícios de usar o repositório de conteúdo compartilhado do App-V 5,1:

-   Redução de conflitos de aplicativos de aplicativos para aplicativos e vários usuários e, portanto, uma necessidade reduzida de teste de regressão

-   Implantação de aplicativos acelerada por meio da redução do risco da implantação

-   Gerenciamento simplificado de perfis






## <a href="" id="other-resources-for-the-app-v-5-1-deployment-"></a>Outros recursos para a implantação do App-V 5,1


[Planejando a implantação do App-V](planning-to-deploy-app-v51.md)

## Tópicos relacionados


[Como instalar o sequenciador](how-to-install-the-sequencer-51beta-gb18030.md)

[Como implantar o cliente do App-V](how-to-deploy-the-app-v-client-51gb18030.md)

[Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

[Como instalar o cliente App-V 5.1 para o modo de repositório de conteúdo compartilhado](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

 

 





