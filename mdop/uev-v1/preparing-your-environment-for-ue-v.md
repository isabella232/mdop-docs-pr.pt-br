---
title: Como preparar seu ambiente para a UE-V
description: Como preparar seu ambiente para a UE-V
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799514"
---
# Como preparar seu ambiente para a UE-V


As configurações de roaming do Microsoft User Experience Virtualization (UE-V) entre computadores pelo uso de um local de armazenamento de configurações. O local de armazenamento de configurações é um compartilhamento de arquivos e deve ser configurado durante a implantação do agente do UE-V. Ele deve ser definido como um local de armazenamento de configurações ou como um diretório base do Active Directory. Além disso, o administrador deve configurar um servidor de horário para dar suporte à sincronização consistente. Para preparar seu ambiente para UE-V, considere o seguinte:

-   [Armazenamento de configurações do UE-V](#bkmk-uevsettingsstorage):

    -   [Definindo um local de armazenamento de configurações](#bkmk-definingsettingsstoragelocation)

    -   [Usando o diretório inicial do Active Directory com UE-V](#bkmk-usingactivedirectoryhomedirectory)

-   [Sincronizar os relógios do computador para a sincronização de configurações do UE-V](#bkmk-synchronizecomputerclocks)

-   [Desempenho e planejamento de capacidade](#bkmk-performancecapacityplanning)

Para obter mais informações sobre os requisitos do sistema operacional e do computador, consulte [configurações com suporte para o UE-V 1,0](supported-configurations-for-ue-v-10.md).

## <a href="" id="bkmk-uevsettingsstorage"></a>Armazenamento de configurações do UE-V


Você pode definir o armazenamento de configurações de virtualização da experiência do usuário em uma das duas configurações: um local de armazenamento de configurações ou um diretório base do Active Directory.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>Definir um local de armazenamento de configurações

O local de armazenamento de configurações do UE-V é um compartilhamento de rede padrão acessível a usuários do UE-V. Antes de definir o local de armazenamento de configurações, você deve criar um diretório raiz. Os usuários que armazenam configurações no compartilhamento devem ter permissões de leitura/gravação para o local de armazenamento. O UE-V Agent criará pastas específicas do usuário neste diretório raiz. O local de armazenamento de configurações é definido definindo a opção de configuração **SettingsStoragePath** . Essa opção pode ser configurada das seguintes maneiras:

-   Durante a instalação do UE-V Agent por meio de um parâmetro de linha de comando ou em um script em lote.

-   Usando a política de grupo.

-   Após a instalação, usando o PowerShell ou WMI.

O caminho deve estar em um caminho UNC (Convenção Universal de nomenclatura) do servidor e do compartilhamento. Por exemplo, **\\\\server\\settingsshare\\**. Essa opção de configuração oferece suporte ao uso de variáveis para habilitar cenários de roaming específicos.

Você pode usar a `%username%` variável com o caminho UNC do servidor e do compartilhamento. Isso fornecerá a mesma experiência de configurações em todos os computadores ou sessões nos quais um usuário faz logon. Considere essa configuração para os seguintes cenários:

1.  Os usuários da empresa têm vários computadores físicos configurados de maneira semelhante e as configurações de cada usuário devem ser iguais em todos os computadores.

2.  Os usuários da empresa usam pools da VDI (Virtual Desktop Infrastructure) onde as configurações devem ser mantidas nas sessões de VDI de cada usuário.

3.  Os usuários da empresa têm um computador físico e também usam uma VDI. A experiência das configurações de cada usuário deve ser a mesma se estiver usando o computador físico ou a sessão de VDI.

4.  Vários computadores empresariais são usados por vários usuários. A experiência das configurações de cada usuário deve ser a mesma em todos os computadores.

Você pode usar as variáveis **%username%\\%ComputerName%** com o caminho UNC do servidor e do compartilhamento. Isso irá preservar a experiência de configurações para cada computador. Considere essa configuração para os seguintes cenários:

1.  Os usuários da empresa têm vários computadores físicos e você deseja preservar a experiência de configurações para cada computador.

2.  Os computadores da empresa são usados por vários usuários. A experiência das configurações deve ser preservada para cada computador no qual o usuário faz logon.

O UE-V Agent cria dinamicamente o caminho de armazenamento de configurações específicas do usuário com base em uma configuração de UE-V `SettingsStoragePath` e nas variáveis definidas.

O UE-V Agent cria dinamicamente uma pasta de sistema oculta `SettingsPackages` com o nome de cada local de armazenamento específico do usuário. O UE-V Agent lê e grava as configurações para este local, conforme definido pelos modelos de localização de configurações de UE-V registrados.

Se o local de armazenamento de configurações for o mesmo para um conjunto de computadores gerenciados de um usuário, as configurações de UE-V aplicáveis são determinadas por uma regra "última gravação de WINS". O agente executado em um computador lê e grava no local de configurações independentemente dos agentes executados em outros computadores. As últimas configurações e valores gravados são as configurações aplicadas quando o próximo agente lê do local de armazenamento de configurações. Para obter mais informações, consulte [implantando o local de armazenamento de configurações para UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md).

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>Usar diretório inicial do Active Directory com UE-V

Se nenhuma localização de armazenamento de configurações estiver configurada para UE-V quando o agente for implantado, o diretório base do Active Directory (AD) do usuário será usado para armazenar os pacotes de local de configurações. O UE-V Agent cria dinamicamente a pasta de armazenamento de configurações abaixo da raiz do diretório base do AD de cada usuário. O agente usará somente o diretório base do Active Directory se um local de armazenamento de configurações (SettingsStoragePath) não for definido de outra forma.

## <a href="" id="bkmk-synchronizecomputerclocks"></a>Sincronizar os relógios do computador para a sincronização de configurações do UE-V


Os computadores que executam o UE-V Agent para sincronizar as configurações devem usar um servidor de tempo. Carimbos de data/hora são usados para determinar se as configurações precisam ser sincronizadas do local de armazenamento de configurações. Se o relógio do computador não for exato, as configurações mais antigas podem substituir as configurações mais recentes, ou as novas configurações podem não ser salvas no local de armazenamento de configurações. O uso de um servidor de tempo permite que o UE-V mantenha uma experiência de configuração consistente.

## <a href="" id="bkmk-performancecapacityplanning"></a>Desempenho e planejamento de capacidade


Os requisitos de capacidade para UE-V podem ser determinados pelo uso da capacidade de disco padrão e do monitoramento da integridade da rede. O UE-V usa um compartilhamento SMB (Server Message Block) para o armazenamento de pacotes de configurações. O tamanho dos pacotes de configurações varia de acordo com as informações de configuração de um aplicativo específico. Embora a maioria dos pacotes de configurações seja pequena, a sincronização de arquivos potencialmente grandes, como imagens da área de trabalho, pode resultar em desempenho ruim, principalmente em redes mais lentas. Para minimizar problemas de latência da rede, você deve criar locais de armazenamento de configurações nas mesmas redes locais em que os computadores dos usuários residem.

Por padrão, a sincronização do UE-V irá expirar após 2 segundos se a rede estiver lenta ou o pacote de configurações for grande. Você pode configurar o tempo limite com a política de grupo. Para obter mais informações sobre como definir o tempo limite, consulte [Configurando o UE-V com objetos de política de grupo](configuring-ue-v-with-group-policy-objects.md).

## Tópicos relacionados


[Virtualização da Experiência do Usuário Microsoft (UE-V) 1.0](index.md)

[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Configurações com suporte para a UE-V 1.0](supported-configurations-for-ue-v-10.md)

 

 





