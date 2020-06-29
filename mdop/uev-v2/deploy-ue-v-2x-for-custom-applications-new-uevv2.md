---
title: Implantar o UE-V 2. x para aplicativos personalizados
description: Implantar o UE-V 2. x para aplicativos personalizados
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799465"
---
# <span data-ttu-id="e8fe7-103">Implantar o UE-V 2. x para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="e8fe7-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="e8fe7-104">Microsoft User Experience Virtualization (UE-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="e8fe7-105">o 2,1 e o 2,1 SP1 usam arquivos XML denominados **modelos de localização de configurações** para monitorar e sincronizar as configurações do aplicativo da área de trabalho e as configurações da área de trabalho do Windows entre os computadores</span><span class="sxs-lookup"><span data-stu-id="e8fe7-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="e8fe7-106">Por padrão, alguns modelos de local das configurações estão incluídos no UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="e8fe7-107">Mas se você quiser sincronizar configurações para aplicativos da área de trabalho diferentes daqueles incluídos nos modelos padrão, poderá criar seus próprios modelos de local de configurações personalizadas usando o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="e8fe7-108">Depois de ler o material de planejamento em [preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) e decidir que você deseja sincronizar as configurações para aplicativos personalizados (terceiros, de linha de negócios, etc.), você vai implantar os recursos da UE-V conforme descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="e8fe7-109">Para começar, aqui estão as principais etapas necessárias para sincronizar as configurações para aplicativos personalizados:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="e8fe7-110">Instalar o gerador UEV</span><span class="sxs-lookup"><span data-stu-id="e8fe7-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="e8fe7-111">Use o gerador UEV para criar modelos de local de configurações XML personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="e8fe7-112">Configurar um catálogo de modelos de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="e8fe7-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="e8fe7-113">Você pode definir esse caminho onde modelos de localização de configurações personalizadas são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="e8fe7-114">Criar modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="e8fe7-115">Esses modelos personalizados permitem que os usuários sincronizem as configurações para aplicativos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="e8fe7-116">Implantar os modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="e8fe7-117">Depois de testar o modelo personalizado para garantir que as configurações sejam sincronizadas corretamente, você pode implantar esses modelos de uma destas maneiras:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="e8fe7-118">Por meio da infraestrutura de implantação existente, como o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e8fe7-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="e8fe7-119">Usando as preferências de política de grupo</span><span class="sxs-lookup"><span data-stu-id="e8fe7-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="e8fe7-120">Implantar um catálogo de modelos de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="e8fe7-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="e8fe7-121">**Observação**  Os modelos implantados usando ESD ou a política de grupo devem ser registrados com o WMI (Instrumentação de gerenciamento do Windows) do UE-V ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="e8fe7-122">Preparar-se para implantar o UE-V 2. x para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="e8fe7-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="e8fe7-123">Antes de começar a implantar os recursos do UE-V que manipulam aplicativos personalizados, há apenas algumas coisas a serem revisadas.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="e8fe7-124">O UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="e8fe7-124">The UE-V Generator</span></span>

<span data-ttu-id="e8fe7-125">O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="e8fe7-126">O aplicativo que é monitorado deve ser um aplicativo tradicional.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="e8fe7-127">Você usa o UE-V Generator para criar modelos de local de configurações, mas não pode criar um modelo de local de configurações a partir desses tipos de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="e8fe7-128">Aplicativos virtualizados</span><span class="sxs-lookup"><span data-stu-id="e8fe7-128">Virtualized applications</span></span>

-   <span data-ttu-id="e8fe7-129">Aplicativos oferecidos por meio dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="e8fe7-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="e8fe7-130">Aplicativos Java</span><span class="sxs-lookup"><span data-stu-id="e8fe7-130">Java applications</span></span>

-   <span data-ttu-id="e8fe7-131">Aplicativos do Windows  </span><span class="sxs-lookup"><span data-stu-id="e8fe7-131">Windows apps</span></span>

<span data-ttu-id="e8fe7-132">**Observação**  Os modelos de local das configurações do UE-V não podem ser criados em aplicativos virtualizados ou aplicativos de serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="e8fe7-133">No entanto, as configurações sincronizadas usando os modelos podem ser aplicadas a esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="e8fe7-134">Para criar modelos compatíveis com o VDI (Virtual Desktop Infrastructure) e aplicativos de serviços de terminal, abra uma versão do pacote do Windows Installer (. msi) do aplicativo usando o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="e8fe7-135">Para obter mais informações sobre a sincronização de configurações para aplicativos virtuais, consulte [usando o UE-V 2. x com aplicativos de virtualização de aplicativo](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e8fe7-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="e8fe7-136">**Locais excluídos:** O processo de descoberta exclui locais que normalmente armazenam arquivos de software do aplicativo que não sincronizam configurações bem entre computadores de usuário ou ambientes de computação.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="e8fe7-137">Por padrão, eles são excluídos:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="e8fe7-138">HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores</span><span class="sxs-lookup"><span data-stu-id="e8fe7-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="e8fe7-139">HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows</span><span class="sxs-lookup"><span data-stu-id="e8fe7-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="e8fe7-140">Todas as chaves do registro localizadas na seção HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="e8fe7-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="e8fe7-141">Arquivos localizados em diretórios de arquivos de programas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="e8fe7-142">Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="e8fe7-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="e8fe7-143">Arquivos do sistema operacional do Windows localizados em% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="e8fe7-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="e8fe7-144">Se as chaves do registro e os arquivos armazenados em locais excluídos forem necessários para sincronizar as configurações do aplicativo, você pode adicionar manualmente os locais ao modelo de local de configurações durante o processo de criação de modelos.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="e8fe7-145">No entanto, somente as alterações feitas em HKEY \ _CURRENT \ _USER Hive serão Sync-Ed.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="e8fe7-146">Substituir os modelos padrão da Microsoft</span><span class="sxs-lookup"><span data-stu-id="e8fe7-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="e8fe7-147">O UE-V Agent instala um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft e configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="e8fe7-148">Se você personalizar esses modelos ou criar modelos de local de configurações para sincronizar as configurações de aplicativos personalizados, o UE-V Agent pode ser configurado para usar um catálogo de modelos de configurações para armazenar os modelos.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="e8fe7-149">Nesse caso, será necessário incluir os modelos padrão juntamente com os modelos personalizados no catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="e8fe7-150">Ao [implantar um agente do UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), você pode usar o parâmetro de linha de comando `RegisterMSTemplates` para desabilitar o registro dos modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="e8fe7-151">Ao usar a política de grupo para definir o caminho do catálogo de modelos de configurações, você pode optar por substituir os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="e8fe7-152">Se você definir as configurações de política para substituir os modelos padrão da Microsoft, todos os modelos padrão da Microsoft instalados pelo UE-V Agent serão excluídos e somente os modelos localizados no catálogo de modelos de configurações serão usados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="e8fe7-153">O parâmetro de configuração do UE-V Agent `RegisterMSTemplates` deve ser definido como *true* para substituir o modelo padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="e8fe7-154">**Observação**  Se você desabilitar essa configuração de política após a habilitação, o UE-V Agent não restaurará os modelos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="e8fe7-155">Se houver modelos personalizados no catálogo de modelos de configurações que usam a mesma ID que os modelos padrão da Microsoft, e o UE-V Agent não estiver configurado para substituir os modelos padrão da Microsoft, os modelos da Microsoft serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="e8fe7-156">Você também pode substituir os modelos padrão usando os recursos do Windows PowerShell do UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="e8fe7-157">Para substituir o modelo padrão da Microsoft pelo Windows PowerShell, cancele o registro de todos os modelos padrão da Microsoft e registre os modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="e8fe7-158">**Observação**  Os pacotes de configurações antigas permanecerão no local de armazenamento configurações, mesmo se você implantar novos modelos de local de configurações para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="e8fe7-159">Esses pacotes não são lidos pelo agente, mas nenhum deles é excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="e8fe7-160">Instalar o UEV 2. x Generator</span><span class="sxs-lookup"><span data-stu-id="e8fe7-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="e8fe7-161">Instale o gerador do 2,0 do Microsoft User Experience Virtualization (UE-V) em um computador que você pode usar para criar um modelo de local de configurações personalizado.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="e8fe7-162">Esse computador deve ter os aplicativos instalados para os quais modelos de localização de configurações personalizadas serão gerados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="e8fe7-163">Para instalar o UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="e8fe7-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="e8fe7-164">Como usuário com direitos de administrador local, localize o arquivo de instalação do gerador do UE-V **ToolSetup.exe** fornecido com o software UE-v.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="e8fe7-165">Ou, se você souber a arquitetura do computador, poderá executar o arquivo apropriado do Windows Installer (. msi), **ToolsSetupx64.msi** ou **ToolsSetupx86.msi**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="e8fe7-166">Clique duas vezes no arquivo de instalação.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-166">Double-click the installation file.</span></span> <span data-ttu-id="e8fe7-167">O assistente de configuração do gerador do User Experience Virtualization é aberto.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="e8fe7-168">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="e8fe7-169">Aceite os termos de licença para software Microsoft e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="e8fe7-170">Clique nas opções do programa de aperfeiçoamento da experiência do usuário e opções do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="e8fe7-171">Selecione a pasta de destino na qual instalar o UE-V Generator e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="e8fe7-172">Clique em **instalar** para começar a instalação.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="e8fe7-173">**Observação**  Uma solicitação de **controle de conta de usuário** é exibida antes de o aplicativo ser instalado.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="e8fe7-174">É necessário ter permissão para instalar o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="e8fe7-175">Clique em **concluir** para fechar o assistente após a conclusão da instalação.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="e8fe7-176">Você deve reiniciar o computador para poder executar o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="e8fe7-177">Para verificar se a instalação foi bem-sucedida, clique em **Iniciar**, clique em **todos os programas**, clique em **virtualização da experiência do usuário da Microsoft**e, em seguida, clique em **gerador do Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="e8fe7-178">**Observação**  O gerador UE-V 2 somente pode ser usado para criar modelos para agentes UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="e8fe7-179">Em uma implantação mista dos agentes do UE-V 1,0 e do UE-V 2, você deve continuar a usar o gerador do UE-V 1,0 até ter atualizado todos os agentes do UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="e8fe7-180">Implantar um catálogo de modelos de configurações</span><span class="sxs-lookup"><span data-stu-id="e8fe7-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="e8fe7-181">O catálogo de modelos de configurações de experiência de usuário da experiência do usuário é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens (SMB) que armazena todos os modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="e8fe7-182">Uma tarefa agendada no UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização, com base nos modelos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="e8fe7-183">O UE-V Agent registra os modelos que foram adicionados ou atualizados nesta pasta após a última vez que a pasta foi verificada e cancela o registro de modelos que são removidos.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="e8fe7-184">Por padrão, os modelos são registrados e não registrados uma vez por dia em 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="e8fe7-185">Hora local pelo Agendador de tarefas e na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="e8fe7-186">Para personalizar a frequência desta tarefa agendada, consulte [alterando a frequência das tarefas agendadas de UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="e8fe7-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="e8fe7-187">Você pode definir o caminho do catálogo de modelos de configurações usando as opções de linha de comando de instalação, a política de grupo, a WMI ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="e8fe7-188">Os modelos armazenados no caminho do catálogo de modelos de configurações são automaticamente registrados e não são registrados por uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="e8fe7-189">Para configurar o catálogo de modelos de configurações para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e8fe7-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="e8fe7-190">Crie uma nova pasta no computador que armazena o catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="e8fe7-191">Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="e8fe7-192">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="e8fe7-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="e8fe7-193">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8fe7-194">Todos</span><span class="sxs-lookup"><span data-stu-id="e8fe7-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-195">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="e8fe7-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e8fe7-196">Computadores do domínio</span><span class="sxs-lookup"><span data-stu-id="e8fe7-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-197">Ler níveis de permissão</span><span class="sxs-lookup"><span data-stu-id="e8fe7-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8fe7-198">Administradores</span><span class="sxs-lookup"><span data-stu-id="e8fe7-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-199">Níveis de permissão de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e8fe7-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="e8fe7-200">Defina as seguintes permissões do sistema de arquivos NTFS para a pasta catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="e8fe7-201">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="e8fe7-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="e8fe7-202">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="e8fe7-203">Aplicar a</span><span class="sxs-lookup"><span data-stu-id="e8fe7-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8fe7-204">Criador/proprietário</span><span class="sxs-lookup"><span data-stu-id="e8fe7-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-205">Controle total</span><span class="sxs-lookup"><span data-stu-id="e8fe7-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-206">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="e8fe7-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e8fe7-207">Computadores do domínio</span><span class="sxs-lookup"><span data-stu-id="e8fe7-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-208">Listar conteúdo da pasta e ler</span><span class="sxs-lookup"><span data-stu-id="e8fe7-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-209">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="e8fe7-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="e8fe7-210">Todos</span><span class="sxs-lookup"><span data-stu-id="e8fe7-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-211">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="e8fe7-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-212">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="e8fe7-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="e8fe7-213">Administradores</span><span class="sxs-lookup"><span data-stu-id="e8fe7-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-214">Controle total</span><span class="sxs-lookup"><span data-stu-id="e8fe7-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="e8fe7-215">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="e8fe7-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="e8fe7-216">Clique em **OK** para fechar as caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="e8fe7-217">No mínimo, o compartilhamento de rede deve conceder permissões para o grupo computadores do domínio.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="e8fe7-218">Além disso, conceda permissões de acesso à pasta de compartilhamento de rede para administradores que devem gerenciar os modelos armazenados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="e8fe7-219">Criar modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="e8fe7-220">Use o UE-V Generator para criar modelos de local de configurações para aplicativos de linha de negócios ou outros aplicativos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="e8fe7-221">Depois que o modelo de um aplicativo for criado, você poderá implantá-lo nos computadores para que as configurações sejam sincronizadas para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="e8fe7-222">Para criar um modelo de local de configurações de UE-V com o UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="e8fe7-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="e8fe7-223">Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="e8fe7-224">Clique em **criar um modelo de local de configurações**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="e8fe7-225">Especifique o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-225">Specify the application.</span></span> <span data-ttu-id="e8fe7-226">Navegue até o caminho do arquivo do aplicativo (. exe) ou o atalho do aplicativo (. lnk) para o qual você deseja criar um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="e8fe7-227">Especifique os argumentos de linha de comando, se houver e diretório de trabalho, se houver.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="e8fe7-228">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="e8fe7-229">**Observação**  Antes de o aplicativo ser iniciado, o sistema exibe uma solicitação de **controle de conta de usuário**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="e8fe7-230">É necessário ter permissão para monitorar o registro e os locais de arquivo que o aplicativo usa para armazenar as configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="e8fe7-231">Depois que o aplicativo for iniciado, feche o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-231">After the application starts, close the application.</span></span> <span data-ttu-id="e8fe7-232">O gerador do UE-V registra os locais onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="e8fe7-233">Após a conclusão do processo, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="e8fe7-234">Revise e marque as caixas de seleção que estão próximas às configurações locais do registro e locais dos arquivos de configurações a serem sincronizados para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="e8fe7-235">A lista inclui as duas categorias a seguir para locais de configurações:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="e8fe7-236">**Padrão**: configurações de aplicativo que são armazenadas no registro nas chaves hKey \ _CURRENT \ _USER ou nas pastas de arquivo em \ \ **Users** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="e8fe7-237">O gerador do UE-V inclui essas configurações por padrão.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="e8fe7-238">Não **padrão**: as configurações do aplicativo armazenadas fora dos locais são especificadas nas práticas recomendadas para armazenamento de dados de configurações (opcional).</span><span class="sxs-lookup"><span data-stu-id="e8fe7-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="e8fe7-239">Isso inclui arquivos e pastas em **usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="e8fe7-240">Revise esses locais para determinar se devem ser incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="e8fe7-241">Marque as caixas de seleção de locais para incluí-las.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="e8fe7-242">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="e8fe7-243">Revise e edite quaisquer **Propriedades**, locais **do registro** e locais de **arquivos** para o modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="e8fe7-244">Edite as seguintes propriedades na guia **Propriedades** :</span><span class="sxs-lookup"><span data-stu-id="e8fe7-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="e8fe7-245">**Nome do aplicativo**: o nome do aplicativo que está escrito na descrição das propriedades dos arquivos de programa.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="e8fe7-246">**Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="e8fe7-247">Esse nome geralmente tem a extensão de nome de arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="e8fe7-248">**Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="e8fe7-249">Essa propriedade, em conjunto com a **versão do arquivo**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="e8fe7-250">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-250">This property accepts a major version number.</span></span> <span data-ttu-id="e8fe7-251">Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do produto.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="e8fe7-252">**Versão do arquivo**: o número da versão do arquivo. exe do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="e8fe7-253">Essa propriedade, em conjunto com a **versão do produto**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="e8fe7-254">Essa propriedade aceita um número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-254">This property accepts a major version number.</span></span> <span data-ttu-id="e8fe7-255">Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do programa.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="e8fe7-256">**Nome do autor do modelo** (opcional): o nome do autor do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="e8fe7-257">**Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="e8fe7-258">A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="e8fe7-259">Edite os locais do registro usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="e8fe7-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="e8fe7-260">As tarefas permitem que você adicione novas chaves, edite o nome ou o escopo das chaves existentes, exclua as chaves e procure o registro no qual as chaves estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="e8fe7-261">Use o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="e8fe7-262">Use **todas as configurações e subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="e8fe7-263">A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais de arquivos que estão incluídos no modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="e8fe7-264">Edite os locais de arquivos usando o menu suspenso **tarefas** .</span><span class="sxs-lookup"><span data-stu-id="e8fe7-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="e8fe7-265">Tarefas para locais de arquivos permitem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="e8fe7-266">Deixe a máscara de arquivo vazia para incluir todos os arquivos na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="e8fe7-267">Clique em **criar**e, em seguida, clique em **salvar** para salvar o modelo de local de configurações no computador.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="e8fe7-268">Clique em **fechar** para fechar o assistente de modelo de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="e8fe7-269">Saia do aplicativo do gerador do UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="e8fe7-270">Depois de criar o modelo de local de configurações para um aplicativo, você deve testar o modelo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="e8fe7-271">Implante o modelo em um ambiente de laboratório antes de colocá-lo em produção na empresa.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="e8fe7-272">[Referência de esquema de modelo de aplicativo para UE-V](https://technet.microsoft.com/library/dn763947.aspx) detalha a estrutura XML do modelo de local de configurações do UE-v e fornece orientação para a edição desses arquivos.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="e8fe7-273">Implantar os modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="e8fe7-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="e8fe7-274">Depois de criar um modelo de local de configurações com o UE-V Generator, você deve testá-lo para garantir que as configurações do aplicativo sejam sincronizadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="e8fe7-275">Em seguida, você pode implantar com segurança o modelo de local de configurações em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="e8fe7-276">Os modelos de local de configurações podem ser implantados usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="e8fe7-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="e8fe7-277">Um sistema ESD (Enterprise Software Distribution), como o System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e8fe7-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="e8fe7-278">Preferências da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="e8fe7-278">Group Policy preferences</span></span>

-   <span data-ttu-id="e8fe7-279">Um catálogo de modelos de configurações de UE-V</span><span class="sxs-lookup"><span data-stu-id="e8fe7-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="e8fe7-280">Os modelos implantados usando um sistema ESD ou objetos de política de grupo devem ser registrados por meio da WMI (Instrumentação de gerenciamento do Windows) do UE-V ou do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="e8fe7-281">Os modelos armazenados na localização do catálogo de modelos de configurações são automaticamente registrados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="e8fe7-282">Para usar o caminho do catálogo de modelos de configurações para implantar os modelos de local das configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="e8fe7-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="e8fe7-283">Navegue até a pasta de compartilhamento de rede que é definida como o catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="e8fe7-284">Adicione, remova ou atualize os modelos de local de configurações no catálogo de modelos de configurações para refletir a configuração de modelo de agente do UE-V que você deseja para computadores UE-V.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="e8fe7-285">**Observação**  Os modelos em computadores são atualizados diariamente.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="e8fe7-286">A atualização é baseada em alterações no catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="e8fe7-287">Para atualizar manualmente os modelos em um computador que executa o UE-V Agent, abra um prompt de comando elevado e navegue até \*\*% Program Files%\\Microsoft Virtualization Experience User Experience \ \ Agent \ \ &lt; x86 ou x64 &gt; \*\*e execute **ApplySettingsTemplateCatalog.exe**.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="e8fe7-288">**Observação**  Este programa é executado automaticamente durante a inicialização do computador e o diário em 3:30 A. M.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="e8fe7-289">para coletar novos modelos que foram adicionados recentemente ao catálogo.</span><span class="sxs-lookup"><span data-stu-id="e8fe7-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="e8fe7-290">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8fe7-290">Related topics</span></span>


[<span data-ttu-id="e8fe7-291">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e8fe7-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="e8fe7-292">Implantar os recursos necessários na UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="e8fe7-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





