---
title: Planejamento para os métodos de configuração da UE-V
description: Planejamento para os métodos de configuração da UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800003"
---
# Planejamento para os métodos de configuração da UE-V


As configurações da Microsoft User Experience Virtualization (UE-V Virtualization) determinam como as configurações são sincronizadas em toda a empresa. Este tópico descreve como as configurações do UE-V são criadas para ajudá-lo a formular um plano de configuração que melhor atenda às suas necessidades de negócios.

## Métodos de configuração para UE-V


Você pode configurar o UE-V antes, durante ou após a instalação do agente, dependendo do método de configuração que você usa.

**Política de Grupo:** a infraestrutura de política de grupo existente pode ser usada para configurar o UE-v antes ou depois da implantação do agente do UE-v. O modelo UE-V ADMX permite o gerenciamento centralizado das opções de configuração comuns do agente do UE-V e inclui configurações para configurar a sincronização de UE-V. Os ambientes de rede que usam a política de grupo podem pré-configurar o UE-V na previsão da implantação do agente.

[Configurando o UE-V com objetos de Política de Grupo](configuring-ue-v-with-group-policy-objects.md)

[Instalação dos modelos ADMX da Política de Grupo da UE-V](installing-the-ue-v-group-policy-admx-templates.md)

**Instalação de linha de comando ou de script em lotes:** os parâmetros que são usados com a implantação do UE-v Agent permitem a configuração de muitas configurações de UE-v. Sistemas de distribuição de software eletrônico, como o System Center Configuration Manager, usam esses parâmetros para configurar seus clientes ao implantar e instalar o software do agente do UE-V. Para obter uma lista de parâmetros de instalação e exemplos de scripts de instalação, consulte [implantando o UE-V Agent](deploying-the-ue-v-agent.md).

**PowerShell e WMI:** comandos com script que usam PowerShell ou WMI podem ser usados para modificar as configurações após a instalação do UE-V Agent. Para obter uma lista de comandos do PowerShell e WMI, consulte [Gerenciando o agente do UE-V 1,0 e pacotes com o PowerShell e o WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

**Editar configurações do registro:** As configurações de UE-V são armazenadas no registro e podem ser modificadas usando qualquer ferramenta que possa modificar as configurações do registro, como o RegEdit.

**Observação**  A modificação do registro pode resultar em perda de dados ou o computador não responderá. Recomendamos que você use outros métodos de configuração.

 

### Definições de configuração de UE-V

Veja a seguir exemplos de definições de configuração de UE-V:

-   **Definindo o caminho de armazenamento:** especifica o local do compartilhamento de arquivos que armazena as configurações de UE-V.

-   **Caminho do catálogo de modelos de configurações:** especifica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.

-   **Registrar modelos da Microsoft:** especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.

-   **Método de sincronização:** especifica se o recurso arquivos offline do Windows é usado para suporte offline.

-   **Tempo limite de sincronização:** especifica o número de milissegundos que o computador aguarda antes do tempo limite ao recuperar as configurações de usuário do local de armazenamento de configurações.

-   **Habilitar Sincronização:** especifica se a sincronização das configurações do UE-V está habilitada ou desabilitada.

-   **Tamanho máximo do pacote:** especifica um tamanho do limiar do arquivo de pacote de configurações em bytes em que o UE-V Agent informa um aviso.

## Tópicos relacionados


[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Planejamento para a configuração da UE-V](planning-for-ue-v-configuration.md)

 

 





