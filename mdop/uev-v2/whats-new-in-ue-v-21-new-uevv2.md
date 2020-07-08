---
title: Novidades da UE-V 2.1
description: Novidades da UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799837"
---
# Novidades da UE-V 2.1


O User Experience Virtualization 2,1 oferece esses novos recursos e funcionalidades em comparação com o UE-V 2,0. As [notas de versão do Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) fornecem mais informações sobre o lançamento do UE-v 2,1.

## Modelo de local de configurações do Office 2013


O UE-V 2,1 inclui o modelo de local de configurações do Microsoft Office 2013 com suporte de assinatura do Outlook aprimorado. No UE-V 2,1, os dados de assinatura são sincronizados entre os dispositivos do usuário. Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados. Os clientes não precisam mais escolher as configurações de assinatura padrão.

**Observação**  Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook. Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.

 

Anteriormente, o UE-V incluía modelos de local de configurações do Microsoft Office 2010 que foram automaticamente distribuídos e registrados com o UE-V Agent. O UE-V 2,1 funciona com o Office 365 para determinar se as configurações do Office 2013 estão em roaming pelo Office 365. Se as configurações estiverem em roaming pelo Office 365, elas não serão em roaming pela UE-V. [Visão geral sobre as configurações de usuário e roaming do Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fornecem mais informações.

Para habilitar a sincronização de configurações usando o UE-V 2,1, siga um destes procedimentos:

-   Usar a política de grupo para desabilitar a sincronização do Office 365

-   Não habilite a experiência de sincronização do Office 365 durante a instalação do Office 2013

O UE-V 2,1 envia os [modelos do office 2013 e do office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Esta versão remove os modelos do Office 2007. Os usuários ainda podem usar os modelos do Office 2007 do UE-V 2,0 ou versões anteriores e ainda podem obter os modelos da Galeria de modelos do UE-V localizada [aqui](https://go.microsoft.com/fwlink/p/?LinkID=246589).

## Correção para usuários de namespace do sistema de arquivos distribuídos


O UE-V aprimorou o suporte do Distributed File System namespace (DFSN), adicionando uma configuração de UE-V chamada SyncProviderPingEnabled. Desabilitar essa configuração usando o PowerShell ou o WMI permite que os usuários desabilitem o ping do UE-V. O ping do UE-V causa um erro ao usar os servidores DFSN porque esses servidores não respondem aos pings. A não resposta impede que o UE-V sincronize as configurações. Desabilitar o ping do UE-V permite que a sincronização do UE-V funcione normalmente.

Para desativar o UE-V ping, use este cmdlet do PowerShell:

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## Sincronização de credenciais


O UE-V 2,1 oferece aos clientes a capacidade de sincronizar credenciais e certificados armazenados no Gerenciador de credenciais do Windows. Esse componente é desabilitado por padrão. Habilitar esse componente permite que os usuários mantenham suas credenciais de domínio e certificados em sincronia. Os usuários podem entrar uma vez em um dispositivo, e essas credenciais serão transferidas para aquele usuário em todos os dispositivos habilitados da UE-V. [Gerenciar credenciais com o UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) fornece mais informações.

**Observação**  No Windows 8 e posteriores, o Gerenciador de credenciais contém credenciais da Web. Essas credenciais não são sincronizadas entre os dispositivos dos usuários.

 

## Sincronização da conta do UE-V e da Microsoft


O UE-V detecta se as "configurações de sincronização com o OneDrive", também conhecidas como sincronização da conta da Microsoft, está ativada. Se a conta da Microsoft não estiver configurada para sincronizar as configurações, o UE-V sincronizará aplicativos do Windows, pacotes AppX e configurações da área de trabalho do Windows entre dispositivos. Isso permite que os usuários acessem seus aplicativos da loja, música, imagens e outros aplicativos habilitados para contas da Microsoft sem sincronização fora do firewall da empresa. O UE-V Verifica se a política de grupo vai parar de sincronizar as configurações com o OneDrive ou se o usuário desabilitar a **sincronização de suas configurações neste computador** nos controles de usuário.

## Suporte para o SyncMethod external


Uma nova [configuração de SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) chamada **external** especifica que, se as configurações de UE-V forem gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o onedrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.

## Suporte aprimorado para o modo VDI


O UE-V 2,1 inclui [suporte a sessões do VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) compartilhadas entre os usuários finais. Como administrador, você pode registrar e configurar um modelo VDI especial, o que garante que o UE-V mantém toda a funcionalidade intacta em sessões de VDI não persistentes.

**Observação**  Se você não habilitar o modo VDI para sessões de VDI não persistentes, alguns recursos não funcionarão, como backup/restauração e LKG.

 

## Backup e restauração administrativos


Você pode restaurar configurações adicionais quando um usuário adotar um novo dispositivo colocando um modelo de local de configurações no perfil **backup** ou **roaming (padrão)** usando o cmdlet Set-UevTemplateProfile do PowerShell. Isso permite que as configurações do computador sejam sincronizadas com o novo computador, além das configurações do usuário. Os modelos atribuídos ao perfil de backup são incluídos em backup para esse dispositivo e configurados em cada dispositivo. [Gerenciar o backup e a restauração administrativos no UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) fornece mais informações.

## Sincronização para configurações adicionais do Windows


O UE-V agora sincroniza a personalização do teclado virtual, o dicionário ortográfico e permite que o aplicativo alterne para aplicativos recentes e configurações de borda da tela para sincronizar entre os dispositivos Windows 8 e Windows 8,1.






## Tópicos relacionados


[Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





