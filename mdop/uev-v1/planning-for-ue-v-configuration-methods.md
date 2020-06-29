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
# <span data-ttu-id="2cfed-103">Planejamento para os métodos de configuração da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cfed-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="2cfed-104">As configurações da Microsoft User Experience Virtualization (UE-V Virtualization) determinam como as configurações são sincronizadas em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="2cfed-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="2cfed-105">Este tópico descreve como as configurações do UE-V são criadas para ajudá-lo a formular um plano de configuração que melhor atenda às suas necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="2cfed-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="2cfed-106">Métodos de configuração para UE-V</span><span class="sxs-lookup"><span data-stu-id="2cfed-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="2cfed-107">Você pode configurar o UE-V antes, durante ou após a instalação do agente, dependendo do método de configuração que você usa.</span><span class="sxs-lookup"><span data-stu-id="2cfed-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="2cfed-108">**Política de Grupo:** a infraestrutura de política de grupo existente pode ser usada para configurar o UE-v antes ou depois da implantação do agente do UE-v.</span><span class="sxs-lookup"><span data-stu-id="2cfed-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="2cfed-109">O modelo UE-V ADMX permite o gerenciamento centralizado das opções de configuração comuns do agente do UE-V e inclui configurações para configurar a sincronização de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cfed-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="2cfed-110">Os ambientes de rede que usam a política de grupo podem pré-configurar o UE-V na previsão da implantação do agente.</span><span class="sxs-lookup"><span data-stu-id="2cfed-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="2cfed-111">Configurando o UE-V com objetos de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="2cfed-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="2cfed-112">Instalação dos modelos ADMX da Política de Grupo da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cfed-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="2cfed-113">**Instalação de linha de comando ou de script em lotes:** os parâmetros que são usados com a implantação do UE-v Agent permitem a configuração de muitas configurações de UE-v.</span><span class="sxs-lookup"><span data-stu-id="2cfed-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="2cfed-114">Sistemas de distribuição de software eletrônico, como o System Center Configuration Manager, usam esses parâmetros para configurar seus clientes ao implantar e instalar o software do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cfed-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="2cfed-115">Para obter uma lista de parâmetros de instalação e exemplos de scripts de instalação, consulte [implantando o UE-V Agent](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="2cfed-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="2cfed-116">**PowerShell e WMI:** comandos com script que usam PowerShell ou WMI podem ser usados para modificar as configurações após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2cfed-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="2cfed-117">Para obter uma lista de comandos do PowerShell e WMI, consulte [Gerenciando o agente do UE-V 1,0 e pacotes com o PowerShell e o WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2cfed-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="2cfed-118">**Editar configurações do registro:** As configurações de UE-V são armazenadas no registro e podem ser modificadas usando qualquer ferramenta que possa modificar as configurações do registro, como o RegEdit.</span><span class="sxs-lookup"><span data-stu-id="2cfed-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="2cfed-119">**Observação**  A modificação do registro pode resultar em perda de dados ou o computador não responderá.</span><span class="sxs-lookup"><span data-stu-id="2cfed-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="2cfed-120">Recomendamos que você use outros métodos de configuração.</span><span class="sxs-lookup"><span data-stu-id="2cfed-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="2cfed-121">Definições de configuração de UE-V</span><span class="sxs-lookup"><span data-stu-id="2cfed-121">UE-V configuration settings</span></span>

<span data-ttu-id="2cfed-122">Veja a seguir exemplos de definições de configuração de UE-V:</span><span class="sxs-lookup"><span data-stu-id="2cfed-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="2cfed-123">**Definindo o caminho de armazenamento:** especifica o local do compartilhamento de arquivos que armazena as configurações de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2cfed-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="2cfed-124">**Caminho do catálogo de modelos de configurações:** especifica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="2cfed-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="2cfed-125">**Registrar modelos da Microsoft:** especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="2cfed-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="2cfed-126">**Método de sincronização:** especifica se o recurso arquivos offline do Windows é usado para suporte offline.</span><span class="sxs-lookup"><span data-stu-id="2cfed-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="2cfed-127">**Tempo limite de sincronização:** especifica o número de milissegundos que o computador aguarda antes do tempo limite ao recuperar as configurações de usuário do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="2cfed-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="2cfed-128">**Habilitar Sincronização:** especifica se a sincronização das configurações do UE-V está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2cfed-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="2cfed-129">**Tamanho máximo do pacote:** especifica um tamanho do limiar do arquivo de pacote de configurações em bytes em que o UE-V Agent informa um aviso.</span><span class="sxs-lookup"><span data-stu-id="2cfed-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="2cfed-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cfed-130">Related topics</span></span>


[<span data-ttu-id="2cfed-131">Planejamento para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cfed-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="2cfed-132">Planejamento para a configuração da UE-V</span><span class="sxs-lookup"><span data-stu-id="2cfed-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





