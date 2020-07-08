---
title: Guia de planejamento e implantação para o sistema de virtualização de aplicativos
description: Guia de planejamento e implantação para o sistema de virtualização de aplicativos
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796829"
---
# Guia de planejamento e implantação para o sistema de virtualização de aplicativos


O gerenciamento de virtualização de aplicativos da Microsoft oferece a funcionalidade de disponibilizar aplicativos para os computadores dos usuários finais sem precisar instalar os aplicativos diretamente nesses computadores. Isso se tornou possível por meio de um processo conhecido como *sequenciamento do aplicativo, o*que permite que cada aplicativo seja executado em seu próprio ambiente virtual autocontido no computador cliente. Os aplicativos sequenciados são isolados uns dos outros, eliminando conflitos de aplicativo e ainda podem interagir com o computador cliente.

O cliente de virtualização de aplicativos é o componente de sistema do Application Virtualization que permite que o usuário final interaja com os aplicativos após eles terem sido publicados no computador. O cliente gerencia o ambiente virtual no qual os aplicativos virtualizados são executados em cada computador. Após a instalação do cliente em um computador, os aplicativos devem ser disponibilizados para o computador por meio de um processo conhecido como *publicação*, o que permite que o usuário final execute os aplicativos virtuais. O processo de publicação coloca os ícones e atalhos do aplicativo virtual no computador, geralmente na área de trabalho do Windows ou no menu **Iniciar** , e também coloca as informações de definição do pacote e Associação de tipo de arquivo no computador. A publicação também torna o conteúdo do pacote do aplicativo disponível para o computador do usuário final.

O conteúdo do pacote do aplicativo virtual pode ser colocado em um ou mais servidores de virtualização de aplicativos para que ele possa ser transmitido para os clientes por demanda e armazenado localmente em cache. Servidores de arquivos e servidores Web também podem ser usados como servidores de streaming ou o conteúdo pode ser colocado diretamente no computador do usuário final, por exemplo, se você estiver usando um sistema de distribuição de software eletrônico, como o Microsoft Endpoint Configuration Manager. Em uma implementação de vários servidores, manter o conteúdo do pacote e mantê-lo atualizado em todos os servidores de streaming requer uma solução de gerenciamento de pacotes abrangente. Dependendo do tamanho da sua organização, talvez seja necessário ter muitos aplicativos virtuais acessíveis para os usuários finais localizados em todo o mundo. Gerenciar os pacotes para garantir que os aplicativos certos estejam disponíveis para todos os usuários onde e quando precisarem acessá-los é, portanto, um requisito essencial.

O guia de planejamento e implantação do Application Virtualization fornece informações para ajudá-lo a entender melhor e a implantar o aplicativo Microsoft Application Virtualization e seus componentes. Ele também fornece procedimentos passo a passo para implementar os principais cenários de implantação.

## Nesta seção


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Planejamento da implantação do Application Virtualization System](planning-for-application-virtualization-system-deployment.md)  
Fornece as diretrizes necessárias para planejar a implementação e a implantação do sistema de virtualização de aplicativos.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Considerações de atualização e implantação do Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)  
Fornece informações sobre os requisitos de hardware e software para instalar os vários componentes da virtualização de aplicativos, bem como informações de atualização.

<a href="" id="electronic-software-distribution-based-scenario"></a>[Cenário baseado em Distribuição Eletrônica de Software](electronic-software-distribution-based-scenario.md)  
Fornece informações sobre a implantação da virtualização de aplicativos usando um sistema ESD (distribuição de software eletrônico).

<a href="" id="application-virtualization-server-based-scenario"></a>[Cenário baseado no Application Virtualization Server](application-virtualization-server-based-scenario.md)  
Fornece informações sobre a implantação da virtualização de aplicativos usando o servidor de gerenciamento do Application Virtualization.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Cenário de Entrega Autônoma Application Virtualization Clients](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
Descreve como implantar a virtualização do aplicativo em um modo autônomo, sem o uso de recursos ESD ou baseados em servidor.

<a href="" id="application-virtualization-reference"></a>[Referência do Application Virtualization](application-virtualization-reference.md)  
Contém material de referência técnica detalhado relacionado à instalação e ao gerenciamento de componentes do sistema.

 

 





