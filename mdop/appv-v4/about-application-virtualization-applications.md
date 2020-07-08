---
title: Sobre aplicativos do Application Virtualization
description: Sobre aplicativos do Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797655"
---
# Sobre aplicativos do Application Virtualization


Na virtualização do aplicativo, um *aplicativo* é um programa executável, como o Microsoft Visio, que é transmitido para o cliente ou cliente da área de trabalho do Application Virtualization para serviços de área de trabalho remota (anteriormente serviços de terminal) de um servidor de gerenciamento do Application Virtualization. Para que um aplicativo possa ser transmitido para um cliente, o aplicativo deve estar preparado para streaming ao processá-lo com o sequenciador do Application Virtualization.

## Gerenciando aplicativos


Você deve adicionar aplicativos ao sistema para poder disponibilizá-los aos usuários. O método mais comum para adicionar aplicativos ao sistema é importá-los. Para acessar esse recurso, clique com o botão direito do mouse no nó **aplicativos** no console de gerenciamento do servidor do Application Virtualization e escolha **importar aplicativos**.

Você pode importar mais de um arquivo OSD (Open Software Descriptor) ao mesmo tempo, ou pode importar um arquivo de projeto do sequenciador (SPRJ) que pode conter vários arquivos OSD. Essa funcionalidade permite configurar aplicativos relacionados da mesma forma.

Você também pode usar os seguintes recursos para ajudá-lo a gerenciar seus aplicativos:

-   **Grupos de aplicativos**— permite criar grupos lógicos de aplicativos para gerenciamento simplificado. Quando são feitas alterações em um grupo (por exemplo, permissões de acesso), as alterações são aplicadas a todos os aplicativos do grupo. Os aplicativos em um grupo podem vir de diferentes pacotes.

-   Seleção **múltipla**— permite que você selecione vários aplicativos ao mesmo tempo mantendo a tecla Ctrl pressionada ao clicar em um aplicativo para modificar as propriedades do aplicativo. No entanto, se quiser manter uma relação entre os aplicativos, você deve criar um grupo de aplicativos para armazenar os aplicativos.

-   **Cópia cruzada do sistema**— permite copiar aplicativos de um ambiente para outro que esteja executando a mesma versão do App-V em uma etapa. Por exemplo, você pode ter um ambiente de teste de aceitação do usuário no qual você inicialmente implanta e configura aplicativos. Depois de concluir a fase de teste, talvez você queira replicar o mesmo conjunto de aplicativos (incluindo permissões) para o ambiente de produção.

## Tópicos relacionados


[Sobre pacotes do Application Virtualization](about-application-virtualization-packages.md)

[Sobre o Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Como gerenciar grupos de aplicativos no Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Como gerenciar aplicativos no Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





