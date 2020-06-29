---
title: Configurando o UE-V 2. x com o System Center Configuration Manager 2012
description: Configurando o UE-V 2. x com o System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799466"
---
# <span data-ttu-id="71686-103">Configurando o UE-V 2. x com o System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="71686-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="71686-104">Depois de instalar o Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 ou o 2,1 SP1 e seus recursos obrigatórios, a UE-V deve estar configurada.</span><span class="sxs-lookup"><span data-stu-id="71686-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="71686-105">O pacote de configuração do UE-V fornece uma maneira para os administradores usarem o recurso configurações de conformidade do System Center Configuration Manager 2012 SP1 ou posterior para aplicar configurações consistentes entre sites nos quais o UE-V e o Configuration Manager estão instalados.</span><span class="sxs-lookup"><span data-stu-id="71686-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="71686-106">Recursos compatíveis com o UE-V Configuration Pack</span><span class="sxs-lookup"><span data-stu-id="71686-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="71686-107">O pacote de configuração do UE-V inclui ferramentas para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="71686-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="71686-108">Criar ou atualizar as linhas de base de distribuição do modelo de local de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="71686-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="71686-109">Definir modelos UE-V a serem registrados ou não registrados</span><span class="sxs-lookup"><span data-stu-id="71686-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="71686-110">Atualizar itens de configuração do modelo UE-V e linhas de base como modelos são adicionados ou atualizados</span><span class="sxs-lookup"><span data-stu-id="71686-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="71686-111">Distribuir e registrar modelos do UE-V usando a correção padrão de item de configuração</span><span class="sxs-lookup"><span data-stu-id="71686-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="71686-112">Crie ou atualize um item de configuração de política do UE-V Agent para definir ou limpar essas configurações.</span><span class="sxs-lookup"><span data-stu-id="71686-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="71686-113">Tamanho máximo do pacote</span><span class="sxs-lookup"><span data-stu-id="71686-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-114">Habilitar/desabilitar a sincronização de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="71686-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-115">Aguarde a sincronização durante o início do aplicativo</span><span class="sxs-lookup"><span data-stu-id="71686-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="71686-116">Definindo o atraso de importação</span><span class="sxs-lookup"><span data-stu-id="71686-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-117">Sincronizar aplicativos do Windows não listados</span><span class="sxs-lookup"><span data-stu-id="71686-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-118">Aguarde a sincronização durante o logon</span><span class="sxs-lookup"><span data-stu-id="71686-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="71686-119">Notificação de importação de configurações</span><span class="sxs-lookup"><span data-stu-id="71686-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-120">URL do contato de ti</span><span class="sxs-lookup"><span data-stu-id="71686-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-121">Aguarde o tempo limite de sincronização</span><span class="sxs-lookup"><span data-stu-id="71686-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="71686-122">Caminho de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="71686-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-123">Texto descritivo do contato do contato</span><span class="sxs-lookup"><span data-stu-id="71686-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-124">Caminho do catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="71686-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="71686-125">Ativação de sincronização</span><span class="sxs-lookup"><span data-stu-id="71686-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-126">Ícone de bandeja habilitado</span><span class="sxs-lookup"><span data-stu-id="71686-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-127">Iniciar/parar o serviço de agente do UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="71686-128">Método de sincronização</span><span class="sxs-lookup"><span data-stu-id="71686-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-129">Notificação de primeira utilização</span><span class="sxs-lookup"><span data-stu-id="71686-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="71686-130">Definir quais aplicativos do Windows serão as configurações de roaming</span><span class="sxs-lookup"><span data-stu-id="71686-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="71686-131">Tempo limite de sincronização</span><span class="sxs-lookup"><span data-stu-id="71686-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="71686-132">Verifique a conformidade confirmando que o UE-V está em execução.</span><span class="sxs-lookup"><span data-stu-id="71686-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="71686-133">Gerar um item de configuração de política do UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="71686-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="71686-134">Todas as políticas e políticas do UE-V Agent são distribuídas por meio de um único item de configuração que é gerado usando a ferramenta de UevAgentPolicyGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="71686-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="71686-135">Essa ferramenta lê a configuração desejada de um arquivo de configuração XML e cria um CI contendo as configurações de descoberta e correção necessárias para colocar a máquina em conformidade.</span><span class="sxs-lookup"><span data-stu-id="71686-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="71686-136">O arquivo CAB do item de configuração da política do UE-V Agent é criado usando a ferramenta de linha de comando UevTemplateBaselineGenerator.exe, que tem os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="71686-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="71686-137">Código do site do site &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="71686-138">PolicyName &lt; nome &gt; opcional: padrão para "política de agente do UE-V", se não estiver presente</span><span class="sxs-lookup"><span data-stu-id="71686-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="71686-139">Descrição do PolicyDescription &lt; &gt; opcional: uma descrição será fornecida se não estiver presente</span><span class="sxs-lookup"><span data-stu-id="71686-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="71686-140">CabFilePath &lt; caminho completo para o item de configuração. Arquivo CAB&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="71686-141">ConfigurationFile &lt; caminho completo para arquivo XML de configuração do agente&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="71686-142">**Observação**  Pode ser necessário alterar a política de execução do PowerShell para permitir que esses scripts sejam executados em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="71686-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="71686-143">Execute estas etapas no console do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="71686-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="71686-144">Selecionar \*\* &gt; &gt; Propriedades de configurações do cliente de administração\*\*</span><span class="sxs-lookup"><span data-stu-id="71686-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="71686-145">Na guia **agente do usuário** , defina a **política de execução do PowerShell** como **ignorar**</span><span class="sxs-lookup"><span data-stu-id="71686-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="71686-146">Criar o primeiro item de configuração da política do UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="71686-147">Copie o arquivo de configuração de configurações padrão do diretório de instalação do UE-V config Pack para um local visível para o seu console de administração do ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="71686-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="71686-148">O arquivo de configuração padrão contém cinco seções:</span><span class="sxs-lookup"><span data-stu-id="71686-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="71686-149">Política de computador</span><span class="sxs-lookup"><span data-stu-id="71686-149">Computer Policy</span></span>**  
    <span data-ttu-id="71686-150">Todas as configurações no nível da máquina UE-V.</span><span class="sxs-lookup"><span data-stu-id="71686-150">All UE-V machine level settings.</span></span> <span data-ttu-id="71686-151">O atributo desirestate pode ser</span><span class="sxs-lookup"><span data-stu-id="71686-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="71686-152">**Definido** para ter o valor atribuído no registro</span><span class="sxs-lookup"><span data-stu-id="71686-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="71686-153">**Desmarque** para remover a configuração</span><span class="sxs-lookup"><span data-stu-id="71686-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="71686-154">**Não gerenciado** para que o item de configuração seja deixado em seu estado atual</span><span class="sxs-lookup"><span data-stu-id="71686-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="71686-155">Não remova as linhas desta seção.</span><span class="sxs-lookup"><span data-stu-id="71686-155">Do not remove lines from this section.</span></span> <span data-ttu-id="71686-156">Em vez disso, defina ostate desejado como ' não gerenciado ' se você não quiser que o Configuration Manager altere os valores atuais ou padrão.</span><span class="sxs-lookup"><span data-stu-id="71686-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="71686-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="71686-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="71686-158">Todas as configurações de nível de usuário do UE-V.</span><span class="sxs-lookup"><span data-stu-id="71686-158">All UE-V user level settings.</span></span> <span data-ttu-id="71686-159">Essas entradas substituem as configurações da máquina para um usuário.</span><span class="sxs-lookup"><span data-stu-id="71686-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="71686-160">O atributo desirestate pode ser</span><span class="sxs-lookup"><span data-stu-id="71686-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="71686-161">**Definido** para ter o valor atribuído no registro</span><span class="sxs-lookup"><span data-stu-id="71686-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="71686-162">**Desmarque** para remover a configuração</span><span class="sxs-lookup"><span data-stu-id="71686-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="71686-163">**Não gerenciado** para que o item de configuração seja deixado em seu estado atual</span><span class="sxs-lookup"><span data-stu-id="71686-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="71686-164">Não remova as linhas desta seção.</span><span class="sxs-lookup"><span data-stu-id="71686-164">Do not remove lines from this section.</span></span> <span data-ttu-id="71686-165">Em vez disso, defina ostate desejado como ' não gerenciado ' se você não quiser que o Configuration Manager altere os valores atuais ou padrão.</span><span class="sxs-lookup"><span data-stu-id="71686-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="71686-166">Serviços</span><span class="sxs-lookup"><span data-stu-id="71686-166">Services</span></span>**  
    <span data-ttu-id="71686-167">As entradas nesta seção controlam a operação do serviço.</span><span class="sxs-lookup"><span data-stu-id="71686-167">Entries in this section control service operation.</span></span> <span data-ttu-id="71686-168">O arquivo de configuração padrão contém uma única entrada para o UevAgentService.</span><span class="sxs-lookup"><span data-stu-id="71686-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="71686-169">O atributo desirestate pode ser definido como **running** ou **Stopped**.</span><span class="sxs-lookup"><span data-stu-id="71686-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="71686-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="71686-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="71686-171">Todas as configurações de sincronização do aplicativo Windows em nível de máquina.</span><span class="sxs-lookup"><span data-stu-id="71686-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="71686-172">Cada PackageFamilyName listado nesta seção pode ser atribuído umstate desejado de</span><span class="sxs-lookup"><span data-stu-id="71686-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="71686-173">**Habilitado** para ter configurações de roaming</span><span class="sxs-lookup"><span data-stu-id="71686-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="71686-174">**Desabilitado** para impedir que as configurações sejam móveis</span><span class="sxs-lookup"><span data-stu-id="71686-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="71686-175">**Desmarcada** para que a entrada seja removida do controle UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="71686-176">Linhas adicionais podem ser adicionadas a esta seção com base na lista de aplicativos do Windows instalados que podem ser visualizados usando o cmdlet do PowerShell GetAppxPackage.</span><span class="sxs-lookup"><span data-stu-id="71686-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="71686-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="71686-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="71686-178">É idêntico ao Windows8AppsComputerPolicy com configurações que substituem as configurações do computador para um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="71686-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="71686-179">Edite o arquivo de configuração alterando os campos estado e valor desejados.</span><span class="sxs-lookup"><span data-stu-id="71686-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="71686-180">Execute este comando em um computador que executa o console de administração do ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="71686-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="71686-181">Importar o arquivo CAB usando o console do ConfigMgr ou o PowerShell Import-CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="71686-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="71686-182">Atualizar um item de configuração de política do UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="71686-183">Edite o arquivo de configuração alterando os campos estado e valor desejados.</span><span class="sxs-lookup"><span data-stu-id="71686-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="71686-184">Execute o comando da etapa 3 em [criar o primeiro item de configuração da política do UE-V](#create).</span><span class="sxs-lookup"><span data-stu-id="71686-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="71686-185">Se você alterou o nome com o parâmetro PolicyName, certifique-se de inserir o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="71686-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="71686-186">Reimportar o arquivo CAB.</span><span class="sxs-lookup"><span data-stu-id="71686-186">Reimport the CAB file.</span></span> <span data-ttu-id="71686-187">A versão no ConfigMgr será atualizada.</span><span class="sxs-lookup"><span data-stu-id="71686-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="71686-188">Gerar uma linha de base de modelo UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="71686-189">Os modelos do UE-V são distribuídos usando uma linha de base contendo vários itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="71686-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="71686-190">Cada item de configuração contém os scripts de descoberta e correção necessários para instalar um modelo de UE-V.</span><span class="sxs-lookup"><span data-stu-id="71686-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="71686-191">O modelo real UE-V é inserido no script de correção para distribuição usando a funcionalidade padrão de item de configuração.</span><span class="sxs-lookup"><span data-stu-id="71686-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="71686-192">A linha de base do modelo UE-V é criada usando a ferramenta de linha de comando UevTemplateBaselineGenerator.exe, que tem os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="71686-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="71686-193">Código do site do site &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="71686-194">Nome da linha de basename &lt; &gt; (opcional: padrões para "linha de base de distribuição do modelo do UE-V", se não estiverem presentes)</span><span class="sxs-lookup"><span data-stu-id="71686-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="71686-195">&lt;Descrição &gt; do BaselineDescription (opcional: uma descrição será fornecida se não estiver presente)</span><span class="sxs-lookup"><span data-stu-id="71686-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="71686-196">&lt;Pasta de modelos do TemplateFolder UE-V&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="71686-197">Registrar a &lt; lista de arquivos de modelo separados por vírgula&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="71686-198">Remover registro da &lt; lista de modelos separados por vírgula&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="71686-199">CabFilePath &lt; caminho completo para o arquivo CAB da linha de base a ser gerado&gt;</span><span class="sxs-lookup"><span data-stu-id="71686-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="71686-200">O resultado é um arquivo CAB de linha de base que está pronto para ser importado para o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71686-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="71686-201">Se, em uma data futura, você atualizar ou adicionar um modelo, poderá executar novamente o comando usando o mesmo nome de linha de base.</span><span class="sxs-lookup"><span data-stu-id="71686-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="71686-202">Importar os resultados do CAB em atualizações de versão do CI nos modelos alterados.</span><span class="sxs-lookup"><span data-stu-id="71686-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="71686-203">Criar a primeira linha de base de modelo UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="71686-204">Crie um conjunto "mestre" de modelos do UE-V em um local de pasta estável visível para a máquina que está executando o console de administração do ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="71686-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="71686-205">À medida que os modelos são adicionados ou atualizados, essa pasta é onde elas são puxadas para distribuição.</span><span class="sxs-lookup"><span data-stu-id="71686-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="71686-206">A lista inicial de modelos pode ser copiada de um computador com a UE-V instalada.</span><span class="sxs-lookup"><span data-stu-id="71686-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="71686-207">O local padrão do modelo é C:\\Arquivos de experiência do usuário do Files\\Microsoft Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="71686-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="71686-208">Crie um arquivo text.bat onde você possa adicionar o comando gerador de modelos.</span><span class="sxs-lookup"><span data-stu-id="71686-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="71686-209">Isso é opcional, mas tornará a regeneração mais simples se você salvar os parâmetros do comando.</span><span class="sxs-lookup"><span data-stu-id="71686-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="71686-210">Adicione o comando e os parâmetros ao arquivo. bat que irá gerar a linha de base.</span><span class="sxs-lookup"><span data-stu-id="71686-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="71686-211">O exemplo a seguir cria uma linha de base que distribui o bloco de notas e a calculadora:</span><span class="sxs-lookup"><span data-stu-id="71686-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="71686-212">Execute o arquivo. bat para criar UevTemplateBaseline.cab pronto para importação no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71686-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="71686-213">Atualizar uma linha de base de modelo UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="71686-214">O gerador de modelos usa a versão do modelo para determinar se um modelo deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="71686-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="71686-215">Se você fizer uma alteração no modelo e atualizar a versão, o gerador da linha de base comparará o modelo em sua pasta mestra com o modelo contido no IC no servidor do ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="71686-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="71686-216">Se for encontrada uma diferença, a linha de base e as versões de IC modificadas serão atualizadas.</span><span class="sxs-lookup"><span data-stu-id="71686-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="71686-217">Para distribuir um novo modelo do bloco de notas, execute estas etapas:</span><span class="sxs-lookup"><span data-stu-id="71686-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="71686-218">Atualize o modelo e a versão do modelo localizada &lt; no &gt; elemento Version do modelo.</span><span class="sxs-lookup"><span data-stu-id="71686-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="71686-219">Copie o modelo para seu diretório de modelo mestre.</span><span class="sxs-lookup"><span data-stu-id="71686-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="71686-220">Execute o comando no arquivo. bat que você criou na etapa 3 em [criar a primeira linha de base de modelo UE-V](#create2).</span><span class="sxs-lookup"><span data-stu-id="71686-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="71686-221">Importe o arquivo CAB gerado para o ConfigMgr usando o console ou o CMBaseline de importação do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71686-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="71686-222">Obter o pacote de configuração do UE-V</span><span class="sxs-lookup"><span data-stu-id="71686-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="71686-223">É possível baixar o pacote de configuração do UE-V para o Configuration Manager 2012 SP1 ou posterior [aqui](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="71686-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="71686-224">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71686-224">Related topics</span></span>


[<span data-ttu-id="71686-225">Gerenciar as configurações da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="71686-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





