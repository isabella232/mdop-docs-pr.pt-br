---
title: Detecções de alterações na rede que afetam a MED-V
description: Detecções de alterações na rede que afetam a MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799259"
---
# Detecções de alterações na rede que afetam a MED-V


A solução Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 permite que você configure seu ambiente para detectar determinadas alterações de rede que podem ocorrer após a implantação do espaço de trabalho do MED-V, e isso pode afetar o MED-V.

O recurso inclui um componente em execução no sistema operacional convidado que é notificado sobre alterações de configuração de rede no computador host. Ele permite que um ESD ou outro aplicativo que não seja da Microsoft seja executado no convidado resolva os mesmos pontos de extremidade de rede que o host ESD ou o aplicativo resolve.

**Observação**  Esse recurso só estará disponível se a máquina virtual estiver configurada para o modo NAT (conversão de endereços de rede). Se a máquina virtual estiver configurada para o modo de ponte, nenhum indicações de alteração será gerado.

 

Esta seção fornece informações e instruções para ajudá-lo a monitorar as alterações de rede que podem afetar o MED-V.

## Para detectar as alterações de rede do MED-V


Depois de implantar seus espaços de trabalho do MED-V, você pode monitorar as alterações em determinadas configurações de rede, preformando as seguintes tarefas:

1. Crie um arquivo MOF (formato de objeto gerenciado) que irá procurar as alterações de configuração de rede que você deseja monitorar. O código a seguir mostra um exemplo do arquivo MOF que você pode criar.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Compile o arquivo MOF.

3. Instale o arquivo MOF no convidado.

Depois de instalar o arquivo MOF, você pode criar uma assinatura de evento que assine os eventos de criação, modificação ou exclusão da Windows Management Instrumentation (WMI) para a classe **CCM \ _NetworkAdapters** . Isso detecta as seguintes alterações no host:

Há alguma alteração de configuração na rede, como alterações no endereço IP ou adaptador de rede?

A rede está disponível ou não está disponível?

A configuração de rede foi alterada do modo de ponte para o modo NAT?

A configuração de rede foi alterada do modo NAT para o modo de ponte?

Um componente do MED-V no host monitora a rede em busca dessas alterações e, em seguida, sinaliza o convidado da alteração. Um componente no convidado cria uma instância do WMI para monitorar o espaço de trabalho do MED-V para essas alterações.

A assinatura de evento que você criou fornece uma notificação pelo sistema WMI quando uma ou mais dessas alterações de rede – ocorre a criação, modificação ou exclusão – ocorre.

## Tópicos relacionados


[Monitorar espaços de trabalho da MED-V](monitor-med-v-workspaces.md)

[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)

 

 





