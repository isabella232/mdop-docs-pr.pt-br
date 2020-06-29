---
title: Implantar os recursos necessários na UE-V 2.x
description: Implantar os recursos necessários na UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799518"
---
# <span data-ttu-id="c6616-103">Implantar os recursos necessários na UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c6616-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="c6616-104">Todas as implantações do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 exigem estes recursos</span><span class="sxs-lookup"><span data-stu-id="c6616-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="c6616-105">[Implante um local de armazenamento de configurações](#ssl) acessível para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="c6616-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="c6616-106">Esse é um compartilhamento de rede padrão que armazena e recupera configurações de usuário.</span><span class="sxs-lookup"><span data-stu-id="c6616-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="c6616-107">Escolher o método de configuração para UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="c6616-108">O UE-V pode ser implantado e configurado com ferramentas comuns de gerenciamento, como política de grupo, configuração do Configuration Manager ou infraestrutura de gerenciamento do Windows e PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c6616-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="c6616-109">[Implante um agente do UE-V](#agent) para ser instalado em cada computador que sincroniza as configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="c6616-110">Isso monitora os aplicativos registrados e o sistema operacional em busca de alterações de configurações e sincroniza essas configurações entre computadores.</span><span class="sxs-lookup"><span data-stu-id="c6616-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="c6616-111">Os tópicos desta seção descrevem como implantar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="c6616-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="c6616-112">Implantar um local de armazenamento de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="c6616-113">O UE-V exige um local no qual armazenar configurações de usuário em arquivos de pacote de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="c6616-114">Você pode definir esse local de armazenamento de configurações de uma destas maneiras:</span><span class="sxs-lookup"><span data-stu-id="c6616-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="c6616-115">Criar seu próprio local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="c6616-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="c6616-116">Usar o Active Directory existente para o local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="c6616-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="c6616-117">Se você não criar um local de armazenamento de configurações, o UE-V Agent usará o Active Directory (AD) por padrão.</span><span class="sxs-lookup"><span data-stu-id="c6616-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="c6616-118">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-118">Note</span></span>**  
<span data-ttu-id="c6616-119">Em questão de [desempenho e planejamento de capacidade](https://technet.microsoft.com/library/dn458932.aspx#capacity) e para reduzir problemas com a latência da rede, crie locais de armazenamento de configurações nas mesmas redes locais em que os computadores dos usuários residem.</span><span class="sxs-lookup"><span data-stu-id="c6616-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="c6616-120">Recomendamos 20 MB de espaço em disco por usuário para o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="c6616-121">Criar um local de armazenamento de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="c6616-122">Antes de definir o local de armazenamento de configurações, você deve criar um diretório raiz com permissões de leitura/gravação para usuários que armazenam configurações no compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c6616-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="c6616-123">O UE-V Agent cria pastas específicas do usuário neste diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="c6616-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="c6616-124">O local de armazenamento de configurações é definido definindo a opção de configuração SettingsStoragePath, que você pode configurar usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="c6616-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="c6616-125">Ao [implantar o UE-V Agent](#agent) por meio de um parâmetro de linha de comando ou em um script em lotes</span><span class="sxs-lookup"><span data-stu-id="c6616-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="c6616-126">Por meio das configurações de [política de grupo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6616-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="c6616-127">Com o [pacote de configuração do System Center](https://technet.microsoft.com/library/dn458917.aspx) para UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="c6616-128">Após a instalação do UE-V Agent, usando o [Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6616-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="c6616-129">O caminho deve estar em um caminho UNC (Convenção Universal de nomenclatura) do servidor e do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c6616-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="c6616-130">Por exemplo, **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="c6616-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="c6616-131">Essa opção de configuração oferece suporte ao uso de variáveis para habilitar cenários de sincronização específicos.</span><span class="sxs-lookup"><span data-stu-id="c6616-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="c6616-132">Por exemplo, você pode usar as `%username%\%computername%` variáveis para preservar a experiência das configurações do usuário final nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="c6616-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="c6616-133">Usuários finais que usam vários computadores físicos em sua empresa</span><span class="sxs-lookup"><span data-stu-id="c6616-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="c6616-134">Computadores corporativos que são usados por vários usuários finais</span><span class="sxs-lookup"><span data-stu-id="c6616-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="c6616-135">O UE-V Agent cria dinamicamente um caminho de armazenamento de configurações específico do usuário, com uma pasta de sistema oculta nomeada `SettingsPackages` , com base na configuração de configuração de **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="c6616-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="c6616-136">O agente lê e grava as configurações nesse local conforme definido pelos modelos de localização de configurações do UE-V registrados.</span><span class="sxs-lookup"><span data-stu-id="c6616-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="c6616-137">**As configurações de UE-V são determinadas por uma regra "última gravação de WINS":** Se o local de armazenamento de configurações for o mesmo para usuários com vários computadores gerenciados, um agente UE-V lê e grava no local de configurações independentemente dos agentes em execução em outros computadores.</span><span class="sxs-lookup"><span data-stu-id="c6616-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="c6616-138">As configurações e os valores gravados por último são aqueles aplicados quando o próximo agente lê do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="c6616-139">**Implantar o local de armazenamento de configurações:** Siga estas etapas para definir o local de armazenamento de configurações em vez de usar o serviço existente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6616-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="c6616-140">Você deve limitar o acesso ao compartilhamento de armazenamento de configurações a esses usuários que precisam dele, conforme mostrado nas tabelas abaixo.</span><span class="sxs-lookup"><span data-stu-id="c6616-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="c6616-141">Para implantar o compartilhamento de rede UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="c6616-142">Crie um novo grupo de segurança para usuários do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c6616-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="c6616-143">Crie uma nova pasta no computador centralizado que armazena os pacotes de configurações do UE-V e conceda aos usuários do UE-V acesso às permissões de grupo para a pasta.</span><span class="sxs-lookup"><span data-stu-id="c6616-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="c6616-144">O administrador que dá suporte a UE-V deve ter permissões para esta pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c6616-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="c6616-145">Defina as seguintes permissões de bloco de mensagens de servidor (SMB) de nível de compartilhamento para a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="c6616-146">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c6616-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="c6616-147">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="c6616-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c6616-148">Todos</span><span class="sxs-lookup"><span data-stu-id="c6616-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-149">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="c6616-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c6616-150">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-151">Controle total</span><span class="sxs-lookup"><span data-stu-id="c6616-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="c6616-152">Defina as seguintes permissões do sistema de arquivos NTFS para a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="c6616-153">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c6616-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="c6616-154">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="c6616-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="c6616-155">Pasta</span><span class="sxs-lookup"><span data-stu-id="c6616-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c6616-156">Criador/proprietário</span><span class="sxs-lookup"><span data-stu-id="c6616-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-157">Controle total</span><span class="sxs-lookup"><span data-stu-id="c6616-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-158">Somente subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="c6616-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c6616-159">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-160">Listar pasta/ler dados, criar pastas/acrescentar dados</span><span class="sxs-lookup"><span data-stu-id="c6616-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6616-161">Somente esta pasta</span><span class="sxs-lookup"><span data-stu-id="c6616-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="c6616-162">Com essa configuração, o UE-V Agent cria e protege uma pasta Settingspackage enquanto ele é executado no contexto do usuário e concede a cada usuário permissão para criar pastas para armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="c6616-163">Os usuários recebem controle total para a pasta Settingspackage enquanto outros usuários não podem acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="c6616-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="c6616-164">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-164">Note</span></span>**  
<span data-ttu-id="c6616-165">Se você criar o compartilhamento de armazenamento configurações em um computador que esteja executando um sistema operacional Windows Server, configure o UE-V para verificar se o grupo Administradores local ou o usuário atual é o proprietário da pasta em que os pacotes de configurações estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="c6616-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="c6616-166">Para habilitar essa segurança adicional, especifique essa configuração no editor do registro do Windows Server:</span><span class="sxs-lookup"><span data-stu-id="c6616-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="c6616-167">Adicione uma chave do registro **reg \ _DWORD** chamada **"RepositoryOwnerCheckEnabled"** ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="c6616-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="c6616-168">Defina o valor da chave do registro como *1*.</span><span class="sxs-lookup"><span data-stu-id="c6616-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="c6616-169">Usar o Active Directory com o UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c6616-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="c6616-170">Por padrão, o UE-V Agent usa o Active Directory (AD) se um local de armazenamento de configurações não for definido de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c6616-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="c6616-171">Nesses casos, o UE-V Agent cria dinamicamente a pasta de armazenamento de configurações na raiz do diretório base do AD de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="c6616-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="c6616-172">Mas, se uma configuração de diretório personalizada estiver configurada no AD, esse diretório será usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c6616-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="c6616-173">Escolha o método de configuração para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c6616-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="c6616-174">Você deseja descobrir qual método de configuração será usado para gerenciar o UE-V após a implantação, pois esse será o método de configuração usado para implantar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="c6616-175">Geralmente, esse é o método de configuração que você já usa em seu ambiente, como o Windows PowerShell ou o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c6616-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="c6616-176">Você pode configurar o UE-V antes, durante ou após a instalação do UE-V Agent, dependendo do método de configuração que você usa.</span><span class="sxs-lookup"><span data-stu-id="c6616-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="c6616-177">[Política de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** você pode usar sua infraestrutura de política de grupo existente para configurar o UE-v antes ou depois da implantação do agente do UE-v.</span><span class="sxs-lookup"><span data-stu-id="c6616-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="c6616-178">O modelo ADMX da política de grupo UE-V permite o gerenciamento centralizado das opções de configuração comuns do agente do UE-V e inclui configurações para configurar a sincronização de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c6616-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="c6616-179">**Instalando os modelos ADMX da política de grupo UE-V:** Modelos ADMX de política de grupo para UE-V defina as configurações de sincronização para o UE-V Agent e habilite o gerenciamento centralizado das configurações comuns de configuração do agente do UE-V usando uma infraestrutura de política de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c6616-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="c6616-180">Os sistemas operacionais com suporte para o controlador de domínio que implanta os objetos de política de grupo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6616-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="c6616-181">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6616-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="c6616-182">Windows Server 2012 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c6616-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="c6616-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** o pacote de configuração do UE-V permite que você use o recurso configurações de conformidade do System Center Configuration Manager 2012 SP1 ou posterior para aplicar configurações consistentes entre sites nos quais o UE-V e o Configuration Manager estão instalados.</span><span class="sxs-lookup"><span data-stu-id="c6616-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="c6616-184">[Windows PowerShell e WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** você pode usar comandos com script para Windows PowerShell e Windows Management Instrumentation (WMI) para modificar as configurações depois de instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="c6616-185">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-185">Note</span></span>**  
    <span data-ttu-id="c6616-186">A modificação do registro pode resultar em perda de dados ou o computador deixa de responder.</span><span class="sxs-lookup"><span data-stu-id="c6616-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="c6616-187">Recomendamos que você use outros métodos de configuração.</span><span class="sxs-lookup"><span data-stu-id="c6616-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="c6616-188">**Instalação de linha de comando ou de script em lotes:** Parâmetros que são usados quando você [implanta o UE-V Agent](#agent) define muitas configurações de UE-v.</span><span class="sxs-lookup"><span data-stu-id="c6616-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="c6616-189">Sistemas de distribuição de software eletrônico, como o System Center 2012 Configuration Manager, usam esses parâmetros para configurar seus clientes ao implantar e instalar o software do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="c6616-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="c6616-190">Implantar o agente UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c6616-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="c6616-191">O UE-V Agent é o núcleo de uma implantação do UE-V e deve ser executado em cada computador que usa o UE-V para sincronizar as configurações do aplicativo e do Windows.</span><span class="sxs-lookup"><span data-stu-id="c6616-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="c6616-192">**Arquivos de instalação do UE-V Agent:** Um único arquivo de instalação, AgentSetup.exe, instala o UE-V Agent nos sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c6616-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="c6616-193">Além disso, AgentSetupx86.msi ou arquivos do Windows Installer específicos da arquitetura do AgentSetupx64.msi são fornecidos e, como são menores, eles podem simplificar as implantações do agente.</span><span class="sxs-lookup"><span data-stu-id="c6616-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="c6616-194">Os [parâmetros de linha de comando para o instalador do AgentSetup.exe](#params) também têm suporte para a instalação do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c6616-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="c6616-195">Importante</span><span class="sxs-lookup"><span data-stu-id="c6616-195">Important</span></span>**  
<span data-ttu-id="c6616-196">Durante a instalação ou desinstalação do agente do UE-V, você pode usar o arquivo AgentSetup.exe ou o &lt; arquivo AgentSetup Arch &gt; . msi, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="c6616-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="c6616-197">O mesmo arquivo deve ser usado para desinstalar o UE-V Agent usado para instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="c6616-198">Para implantar o UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="c6616-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="c6616-199">Você pode usar os seguintes métodos para implantar o UE-V Agent:</span><span class="sxs-lookup"><span data-stu-id="c6616-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="c6616-200">Um sistema de solução ESD (Electronic Software Distribution), como o Configuration Manager, que pode instalar um arquivo Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="c6616-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="c6616-201">Um script de instalação que faz referência ao arquivo do Windows Installer (. msi) que está armazenado centralmente em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c6616-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="c6616-202">Um programa de instalação que você executa manualmente no computador.</span><span class="sxs-lookup"><span data-stu-id="c6616-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="c6616-203">Use o procedimento a seguir para implantar o UE-V Agent de um compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="c6616-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="c6616-204">Para instalar e configurar o UE-V Agent a partir de um compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="c6616-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="c6616-205">Testar o arquivo de instalação do agente do UE-V AgentSetup.exe em um compartilhamento de rede ao qual os usuários têm permissão de leitura.</span><span class="sxs-lookup"><span data-stu-id="c6616-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="c6616-206">Implante um script para os computadores dos usuários que instalam o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="c6616-207">O script deve especificar o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="c6616-208">**Opções de implantação:** Certifique-se de usar o formato de variável correto ao instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="c6616-209">A tabela a seguir fornece exemplos de opções de implantação para usar os arquivos AgentSetup.exe ou Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="c6616-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c6616-210">Tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="c6616-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c6616-211">Descrição da implantação</span><span class="sxs-lookup"><span data-stu-id="c6616-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c6616-212">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c6616-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-213">Prompt de comando</span><span class="sxs-lookup"><span data-stu-id="c6616-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-214">Ao instalar o UE-V Agent em um prompt de comando, use o <em> formato de variável% ^ username% </em> .</span><span class="sxs-lookup"><span data-stu-id="c6616-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="c6616-215">Se forem necessárias aspas por causa de espaços no caminho de armazenamento de configurações, use um arquivo de script em lotes para implantação.</span><span class="sxs-lookup"><span data-stu-id="c6616-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-216">Script em lotes</span><span class="sxs-lookup"><span data-stu-id="c6616-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-217">Ao instalar o UE-V Agent a partir de um arquivo de script em lotes, use o <em> formato de variável%% username%% </em> .</span><span class="sxs-lookup"><span data-stu-id="c6616-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="c6616-218">Se você usar esse método de instalação, deverá escapar a variável com os caracteres%%.</span><span class="sxs-lookup"><span data-stu-id="c6616-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="c6616-219">Sem esse caractere, o script expande a <em> </em> variável username no momento da instalação, em vez do tempo de execução, que faz com que o UE-V use um único local de armazenamento de configurações para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="c6616-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c6616-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-221">Ao instalar o UE-V Agent a partir de um prompt do Windows PowerShell ou de um script do Windows PowerShell, use o <em> formato de variável% username% </em> .</span><span class="sxs-lookup"><span data-stu-id="c6616-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-222">Distribuição de software eletrônico, como a implantação da implantação de software do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c6616-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-223">Ao instalar o UE-V Agent usando o Configuration Manager, use o <em> formato de variável ^% username ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="c6616-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c6616-224">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-224">Note</span></span>**  
<span data-ttu-id="c6616-225">A instalação do UE-V Agent exige direitos de administrador, e o computador requer uma reinicialização para que o UE-V Agent possa ser executado.</span><span class="sxs-lookup"><span data-stu-id="c6616-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="c6616-226">Parâmetros de linha de comando para implantação do agente UE-V</span><span class="sxs-lookup"><span data-stu-id="c6616-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="c6616-227">Os parâmetros de linha de comando do UE-V Agent são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="c6616-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c6616-228">Parâmetro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="c6616-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c6616-229">Definição</span><span class="sxs-lookup"><span data-stu-id="c6616-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c6616-230">Observações</span><span class="sxs-lookup"><span data-stu-id="c6616-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-231">/Help ou/h ou/?</span><span class="sxs-lookup"><span data-stu-id="c6616-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-232">Exibe a caixa de diálogo AgentSetup.exe uso.</span><span class="sxs-lookup"><span data-stu-id="c6616-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="c6616-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-234">Indica o caminho UNC (Convenção Universal de nomenclatura) que define onde as configurações são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c6616-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="c6616-235">Importante</span><span class="sxs-lookup"><span data-stu-id="c6616-235">Important</span></span></strong><br/><p><span data-ttu-id="c6616-236">Você deve especificar um SettingsStoragePath no UE-V 2,1 e no UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="c6616-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="c6616-237">Você pode definir a cadeia de caracteres AdHomePath para especificar que o caminho inicial do usuário&#39;s do Active Directory seja usado.</span><span class="sxs-lookup"><span data-stu-id="c6616-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="c6616-238">Por exemplo, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="c6616-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="c6616-239">No UE-V 2,0, você pode deixar o SettingsStoragePath em branco para usar o caminho inicial do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6616-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="c6616-240">as variáveis de ambiente% username% ou% computernamename% são aceitas.</span><span class="sxs-lookup"><span data-stu-id="c6616-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="c6616-241">O script pode exigir variáveis de escape.</span><span class="sxs-lookup"><span data-stu-id="c6616-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="c6616-242">Padrão </strong> : &lt; nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="c6616-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="c6616-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-244">Obtém o valor SettingsStoragePath do registro durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c6616-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-245">No prompt de comando, digite o exemplo a seguir para forçar o UE-V a usar o caminho inicial do Active Directory em vez de um UNC específico.</span><span class="sxs-lookup"><span data-stu-id="c6616-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="c6616-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-247">Indica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-248">Só é necessário para modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c6616-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="c6616-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-250">Especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c6616-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-251">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="c6616-251">True | False</span></span></p>
<p><strong><span data-ttu-id="c6616-252">Padrão </strong> : verdadeiro</span><span class="sxs-lookup"><span data-stu-id="c6616-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-253">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="c6616-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-254">Especifica qual método de sincronização deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="c6616-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-255">SyncProvider | Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c6616-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="c6616-256">Padrão </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="c6616-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="c6616-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-258">Especifica o número de milissegundos que o computador aguarda antes do tempo limite quando ele recupera as configurações de usuário do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c6616-259">Padrão </strong> : 2000 milissegundos</span><span class="sxs-lookup"><span data-stu-id="c6616-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="c6616-260">(Aguarde até 2 segundos)</span><span class="sxs-lookup"><span data-stu-id="c6616-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="c6616-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-262">Especifica se a sincronização de UE-V está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="c6616-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-263">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="c6616-263">True | False</span></span></p>
<p><strong><span data-ttu-id="c6616-264">Padrão </strong> : verdadeiro</span><span class="sxs-lookup"><span data-stu-id="c6616-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="c6616-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-266">Especifica um tamanho de arquivo de pacote de configurações em bytes quando o UE-V Agent informa que os arquivos excedem o limite.</span><span class="sxs-lookup"><span data-stu-id="c6616-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-267">&lt;tamanho&gt;</span><span class="sxs-lookup"><span data-stu-id="c6616-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="c6616-268">Padrão </strong> : nenhum (sem limite de aviso)</span><span class="sxs-lookup"><span data-stu-id="c6616-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="c6616-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-270">Especifica a configuração de participação no programa de aperfeiçoamento da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="c6616-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="c6616-271">Se definido como <strong> true </strong> , as informações do instalador serão carregadas no site do programa de aperfeiçoamento da experiência do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6616-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="c6616-272">Se definido como <strong> false </strong> , nenhuma informação será carregada.</span><span class="sxs-lookup"><span data-stu-id="c6616-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-273">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="c6616-273">True | False</span></span></p>
<p><strong><span data-ttu-id="c6616-274">Padrão </strong> : falso</span><span class="sxs-lookup"><span data-stu-id="c6616-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-275">Restart</span><span class="sxs-lookup"><span data-stu-id="c6616-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-276">Suporta o adiamento do computador após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="c6616-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-278">Permite que uma pasta de instalação diferente seja definida para o UE-V Agent ou o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="c6616-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="c6616-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-280">Permite que a instalação aceite a opção a ser incluída no programa Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="c6616-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c6616-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="c6616-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-282">Permite que o UE-V seja instalado silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="c6616-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="c6616-283">Isso deve ser definido como <strong> true </strong> para instalar o UE-V silenciosamente e ignorar a necessidade de que o usuário aceite os termos de licença do UE-v.</span><span class="sxs-lookup"><span data-stu-id="c6616-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="c6616-284">Se definido como <strong> falso </strong> ou deixado vazio, o usuário recebe uma mensagem de erro e UE-V não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6616-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="c6616-285">Importante</span><span class="sxs-lookup"><span data-stu-id="c6616-285">Important</span></span></strong><br/><p><span data-ttu-id="c6616-286">Este parâmetro é necessário para instalar o UE-V silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="c6616-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c6616-287">Restart</span><span class="sxs-lookup"><span data-stu-id="c6616-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="c6616-288">Impede uma reinicialização obrigatória após a instalação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c6616-289">Atualize o UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="c6616-289">Update the UE-V Agent</span></span>

<span data-ttu-id="c6616-290">As atualizações para o software do agente do UE-V são fornecidas por meio do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="c6616-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="c6616-291">Você pode implantar as atualizações do UE-V Agent usando sistemas de infraestrutura ESD (Enterprise Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="c6616-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="c6616-292">Durante uma atualização do UE-V Agent, o grupo padrão de modelos de localização de configurações para aplicativos e configurações do Windows comuns podem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="c6616-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="c6616-293">Atualize o agente do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c6616-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="c6616-294">O agente UE-V 2. x introduz muitos recursos novos e modifica como e quando o agente carrega o conteúdo para o compartilhamento de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="c6616-295">O processo de atualização automatiza essas alterações.</span><span class="sxs-lookup"><span data-stu-id="c6616-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="c6616-296">Para atualizar o UE-V Agent, execute o pacote de instalação do UE-V Agent (AgentSetup.exe, AgentSetupx86.msi ou AgentSetupx64.msi) nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="c6616-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="c6616-297">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-297">Note</span></span>**  
<span data-ttu-id="c6616-298">Ao atualizar o UE-V Agent, você deve usar o mesmo tipo de instalador (arquivo. exe ou pacote MSI) que instalou o UE-V Agent anterior.</span><span class="sxs-lookup"><span data-stu-id="c6616-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="c6616-299">Por exemplo, use o AgentSetup.exe do UE-V 2 para atualizar os agentes do UE-V 1,0 que foram instalados usando o AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="c6616-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="c6616-300">As configurações a seguir são preservadas quando o programa de configuração do agente é executado:</span><span class="sxs-lookup"><span data-stu-id="c6616-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="c6616-301">Caminho de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="c6616-301">Settings storage path</span></span>

-   <span data-ttu-id="c6616-302">Configurações do registro</span><span class="sxs-lookup"><span data-stu-id="c6616-302">Registry settings</span></span>

-   <span data-ttu-id="c6616-303">Tarefas agendadas (as configurações de intervalo são redefinidas para seus padrões)</span><span class="sxs-lookup"><span data-stu-id="c6616-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="c6616-304">Observação</span><span class="sxs-lookup"><span data-stu-id="c6616-304">Note</span></span>**  
<span data-ttu-id="c6616-305">Um computador com os modelos de localização de configurações do UE-V 2. x que são registrados no UE-V 1,0 Agent registra erros no log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c6616-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="c6616-306">Você pode usar o Gerenciador de configuração do Microsoft System Center 2012 ou outra ferramenta de distribuição de software corporativo para automatizar e distribuir a atualização do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="c6616-307">**Recomendações:** Recomendamos que você atualize todos os agentes do UE-V 1,0 em um ambiente de computação, mas isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="c6616-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="c6616-308">Os modelos de localização de configurações do UE-V 2. x podem interagir com um agente do UE-V 1,0, pois eles só compartilham as configurações do caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="c6616-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="c6616-309">No entanto, recomendamos que você mova as implantações para uma única versão do agente para simplificar o gerenciamento e para dar suporte a UE-V.</span><span class="sxs-lookup"><span data-stu-id="c6616-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="c6616-310">Reparar o UE-V Agent após uma atualização malsucedida</span><span class="sxs-lookup"><span data-stu-id="c6616-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="c6616-311">Você pode enfrentar erros após tentar uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="c6616-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="c6616-312">Atualização do UE-V 1,0 para o UE-V 2</span><span class="sxs-lookup"><span data-stu-id="c6616-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="c6616-313">Atualize para uma versão mais recente do Windows, por exemplo, do Windows 7 para o Windows 8 ou do Windows 8 para o Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="c6616-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="c6616-314">Desinstalar o agente após a atualização do UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="c6616-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="c6616-315">Para resolver problemas, tente reparar o UE-V Agent inserindo esse comando em um prompt de comando no computador em que o agente está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6616-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="c6616-316">Em seguida, você pode repetir o processo de desinstalação ou atualizar instalando a versão mais recente do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c6616-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="c6616-317">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6616-317">Related topics</span></span>


[<span data-ttu-id="c6616-318">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c6616-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="c6616-319">Implantar o UE-V 2. x para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="c6616-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









