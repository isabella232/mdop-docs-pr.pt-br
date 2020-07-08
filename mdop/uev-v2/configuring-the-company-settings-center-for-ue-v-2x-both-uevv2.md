---
title: Configurando o centro de configurações de empresa para UE-V 2. x
description: Configurando o centro de configurações de empresa para UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799243"
---
# Configurando o centro de configurações de empresa para UE-V 2. x


O Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 incluem um novo aplicativo, o centro de configurações da empresa, que ajuda os usuários a gerenciar as configurações para sincronizar. O centro de configurações de empresa é instalado usando o UE-V Agent. Os usuários acessam o centro de configurações da empresa no painel de controle, no menu **Iniciar** ou na tela **inicial** , e por meio do ícone da área de notificação do UE-V. O centro de configurações de empresa mostra quais configurações são sincronizadas e ajuda os usuários a ver o status de sincronização da UE-V. Os usuários podem usar o centro de configurações da empresa para selecionar quais aplicativos ou recursos do Windows sincronizam suas configurações entre computadores. Eles também podem clicar no botão **sincronizar agora** para sincronizar todas as configurações imediatamente. O administrador também pode incluir um link para suporte no centro de configurações da empresa.

## Sobre o centro de configurações da empresa


O aplicativo da área de trabalho do centro de configurações da empresa fornece aos usuários informações sobre a sincronização das configurações do UE-V. O centro de configurações de empresa pode ser acessado de várias maneiras diferentes:

-   Ícone da área de notificação – com o **ícone da bandeja** configuração da política de grupo ou configuração do Windows PowerShell habilitada, o ícone do UE-V aparece na área de notificação. Clique no ícone do UE-V para abrir o centro de configurações da empresa.

    **Observação**  O ícone da área de notificação pode ser desabilitado usando as seguintes configurações:

    -   Configuração da política de Grupo: `Policy Tray Icon`

    -   Cmdlet do Windows PowerShell: `TrayIconEnabled`

    -   Item de configuração no pacote de configuração do UE-V para SystemCenter2012 ConfigurationManager: `Tray icon enabled`

     

-   Aplicativo painel de controle – no painel de controle, navegue até **aparência e personalização**e clique em **central de configurações da empresa**.

-   Notificação de primeira utilização – a não ser que seja desabilitado, o UE-V Agent alertará o usuário de que as configurações agora são sincronizadas quando o UE-V Agent é executado pela primeira vez em um computador. Clique na caixa de diálogo de notificação para abrir o centro de configurações da empresa.

-   A tela **inicial** ou o menu **Iniciar** inclui um link para o centro de configurações da empresa. Uma pesquisa pela central de configurações da empresa localiza o aplicativo.

## Configurando o link de suporte no centro de configurações da empresa


O centro de configurações da empresa pode incluir um hiperlink no qual os usuários podem clicar para obter suporte com problemas de sincronização das configurações do UE-V. Esse link pode abrir qualquer protocolo de URL válido, como http://para uma página da Web ou mailto://para um email. O link suporte pode ser configurado usando a política de grupo, o Windows PowerShell ou o pacote de configuração do UE-V do Gerenciador de configuração do 2012 do System Center.

**Como configurar o link de suporte do centro de configurações da empresa**

1.  Abra sua ferramenta de gerenciamento preferencial:

    -   **Política de grupo** -se você ainda não tiver feito isso, baixe o modelo ADMX para UE-V 2 de [modelos administrativos do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).

    -   **Windows PowerShell** – em um computador com o UE-V Agent instalado, abra o **Windows PowerShell**. Para obter mais informações sobre como administrar o UE-V usando o Windows PowerShell, consulte [administrando o UE-v 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).

    -   **Pacote de configuração do System Center 2012 para Microsoft User Experience Virtualization (UE-v)** – importe o pacote de configuração do UE-v e siga a documentação do pacote de configuração para criar itens de configuração. Para obter mais informações sobre o pacote de configuração do UE-V, consulte [Configurando o UE-v 2. x com o System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

2.  Edite as configurações das seguintes políticas:

    -   **Texto do link de ti de contato** -essa configuração especifica o texto do hiperlink da URL do contato no centro de configurações da empresa. Se você habilitar essa configuração, o centro de configurações da empresa exibirá o texto especificado no link para a URL do contato.

        -   Configurações da política de Grupo: `Contact IT Link Text`

        -   Cmdlet do Windows PowerShell: `ContactITDescription`

        -   Item de configuração do pacote de configuração: `IT contact descriptive text`

    -   **Entre em contato com a URL** -essa configuração especifica a URL do link para o seu contato no centro de configurações da empresa em um protocolo de URL válido, como http://para uma página da web ou mailto://para um email.

        -   Configurações da política de Grupo: `Contact IT URL`

        -   Cmdlet do Windows PowerShell: `ContactITUrl`

        -   Item de configuração do pacote de configuração: `IT contact URL`

3.  Implantar configurações nos computadores dos usuários usando a ferramenta de gerenciamento.






 

 





