---
title: Planejamento da implantação do Application Virtualization Client
description: Planejamento da implantação do Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796828"
---
# Planejamento da implantação do Application Virtualization Client


Depois de decidir como publicar e implantar pacotes de aplicativos virtuais em seus computadores de usuário final, você deve planejar a implantação do software cliente do Application Virtualization.

O cliente Application Virtualization é o componente que realmente executa os aplicativos virtuais. O cliente de virtualização de aplicativos permite que os usuários interajam com ícones e clique duas vezes em tipos de arquivo para iniciar um aplicativo virtual. Ele também manipula o streaming do conteúdo do aplicativo a partir de um servidor de streaming e o armazena em cache antes de iniciar o aplicativo. O conteúdo do aplicativo é estruturado de forma que todo o conteúdo necessário para iniciar o aplicativo e manipular a interação inicial do usuário é transmitido primeiro para o computador do usuário final. Há dois tipos diferentes de software cliente de virtualização de aplicativo: o cliente de virtualização de aplicativos para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal), que é usado em sistemas de servidor host de sessão de área de trabalho remota (host RDSession) e no cliente da área de trabalho de virtualização, que é usado para todos os outros computadores.

O cliente do Application Virtualization deve ser configurado no momento da instalação, seja no console de gerenciamento do Application Virtualization ou por meio da linha de comando do instalador, com várias configurações importantes, incluindo o seguinte:

-   Locais dos ícones de todos os aplicativos.

-   O local do arquivo OSD que contém as informações de definição do pacote.

-   A fonte de conteúdo do aplicativo.

-   O protocolo de comunicação a ser usado durante a recuperação dos itens anteriores.

-   O tamanho do cache e o método de gerenciamento do tamanho do cache a serem usados.

Para agilizar a implantação do software cliente do Application Virtualization ao usar uma solução ESD (distribuição de software eletrônico), as configurações anteriores devem ser definidas cuidadosamente com antecedência. Isso é especialmente importante quando você tem computadores em escritórios diferentes, em que seus clientes precisam ser configurados para usar locais de origem diferentes.

**Observação**  
-   O local do ícone e os valores do arquivo OSD são um fator importante a ser considerado ao escolher o método de publicação, seja usando o Windows Installer ou o SFTMIME. A configuração da fonte de conteúdo do aplicativo é definida pela sua escolha de método de streaming.

-   Para garantir que o cache tem espaço suficiente alocado para todos os pacotes que podem ser implantados, use a configuração **usar o limite de espaço em disco livre** ao configurar o cliente para que o cache possa crescer conforme necessário. Ou, se preferir, determine com antecedência quanto espaço em disco será necessário para o cache do App-V e, no momento da instalação, defina o tamanho do cache de acordo. Para obter mais informações sobre o recurso de gerenciamento de espaço de cache, consulte **como usar o recurso de gerenciamento de espaço em cache** no guia de operações do Microsoft Application Virtualization (App-V).

-   Durante as operações de streaming e de transmissão HTTP (S), os clientes do App-V 4,5 SP1 usam as configurações de servidor proxy configuradas no Internet Explorer no computador do usuário.

Para obter mais informações sobre como configurar os parâmetros de instalação do cliente, consulte [parâmetros da linha de comando do instalador do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).

 

Por fim, você precisa determinar como implantar o software cliente da área de trabalho do Application Virtualization para os clientes da área de trabalho. Embora seja possível implantar o cliente da área de trabalho do Application Virtualization manualmente em cada computador, a maioria das organizações precisaria fazer isso por meio de um processo automatizado. Uma organização média ou grande pode ter um sistema ESD em operação, e essa seria uma maneira ideal de implantar o cliente. Se não houver um sistema ESD, você pode usar o método padrão de instalação do software em sua organização. As opções incluem política de grupo ou várias técnicas de script. Dependendo do número e do tamanho dos escritórios que você tem, esse processo de implantação pode ser complexo, e é essencial que você tenha uma abordagem estruturada para garantir que todos os computadores tenham um cliente instalado com a configuração correta.

## Tópicos relacionados


[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)

[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Como fazer upgrade do Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Como desinstalar o cliente do App-V](how-to-uninstall-the-app-v-client.md)

 

 





