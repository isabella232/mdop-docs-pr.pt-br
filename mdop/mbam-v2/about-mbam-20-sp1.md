---
title: Sobre o MBAM 2.0 SP1
description: Sobre o MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799295"
---
# <span data-ttu-id="76dcc-103">Sobre o MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="76dcc-104">Este tópico descreve as alterações no Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="76dcc-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="76dcc-105">Para obter uma descrição geral do MBAM, consulte [introdução ao MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="76dcc-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="76dcc-106">O que há de novo no MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="76dcc-107">Esta versão do MBAM fornece os novos recursos e funcionalidades a seguir.</span><span class="sxs-lookup"><span data-stu-id="76dcc-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="76dcc-108">Suporte para o Gerenciador de configuração do Windows 8,1, Windows Server 2012 R2 e System Center 2012 R2</span><span class="sxs-lookup"><span data-stu-id="76dcc-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="76dcc-109">O Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) adiciona suporte para o Windows 8,1, o Windows Server 2012 R2 e o System Center 2012 R2 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="76dcc-110">Suporte para Microsoft SQL Server 2008 R2 SP2</span><span class="sxs-lookup"><span data-stu-id="76dcc-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="76dcc-111">O Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) adiciona suporte ao Microsoft SQL Server 2008 R2 SP2.</span><span class="sxs-lookup"><span data-stu-id="76dcc-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="76dcc-112">Você deve usar o Microsoft SQL Server 2008 R2 ou superior se estiver executando o Microsoft System Center Configuration Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="76dcc-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="76dcc-113">Acúmulo de comentários do cliente</span><span class="sxs-lookup"><span data-stu-id="76dcc-113">Customer feedback rollup</span></span>

<span data-ttu-id="76dcc-114">O MBAM 2,0 SP1 inclui um pacote cumulativo de correções para solucionar problemas que foram encontrados desde a versão do Microsoft BitLocker Administration and Monitoring (MBAM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="76dcc-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="76dcc-115">Como parte dessas alterações, o campo nome do computador agora aparece nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker, quando você executa o MBAM com o Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="76dcc-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="76dcc-116">A exceção do firewall deve ser definida em portas para o portal de autoatendimento e o site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="76dcc-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="76dcc-117">Ao configurar o portal de autoatendimento e o site de administração e monitoramento, você deve definir uma exceção de firewall para permitir a comunicação por meio das portas especificadas.</span><span class="sxs-lookup"><span data-stu-id="76dcc-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="76dcc-118">Anteriormente, a instalação do servidor do MBAM abriu as portas automaticamente no firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="76dcc-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="76dcc-119">O local dos relatórios do MBAM foi alterado no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76dcc-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="76dcc-120">Os relatórios do MBAM para a topologia integrada do Configuration Manager agora estão disponíveis em subpastas dentro do nó MBAM.</span><span class="sxs-lookup"><span data-stu-id="76dcc-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="76dcc-121">Os nomes de subpastas representam o idioma dos relatórios dentro da subpasta.</span><span class="sxs-lookup"><span data-stu-id="76dcc-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="76dcc-122">Capacidade de instalar o MBAM em um servidor de site primário quando você instala o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76dcc-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="76dcc-123">Você pode instalar o MBAM em um servidor de site primário ou um servidor de site de administração central quando instalar o MBAM com a topologia integrada do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="76dcc-124">Antes, era necessário instalar o MBAM em um servidor de site de administração central.</span><span class="sxs-lookup"><span data-stu-id="76dcc-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="76dcc-125">Importante</span><span class="sxs-lookup"><span data-stu-id="76dcc-125">Important</span></span>**  
<span data-ttu-id="76dcc-126">O servidor no qual você instala o MBAM deve ser o servidor de nível superior na sua hierarquia.</span><span class="sxs-lookup"><span data-stu-id="76dcc-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="76dcc-127">A instalação do MBAM funciona de maneira diferente para o Microsoft System Center Configuration Manager 2007 e o Microsoft System Center 2012 Configuration Manager da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="76dcc-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="76dcc-128">**Configuration manager 2007** : se você instalar o MBAM em um servidor de site primário que faz parte de uma hierarquia do Configuration Manager maior e tiver um servidor pai do site central, o MBAM resolverá o servidor pai do site central e executará todas as ações de instalação nesse servidor pai.</span><span class="sxs-lookup"><span data-stu-id="76dcc-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="76dcc-129">As ações de instalação incluem verificação de pré-requisitos e instalação dos objetos e relatórios do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="76dcc-130">Por exemplo, se você instalar o MBAM em um servidor de site primário que seja filho de um servidor pai de site central, o MBAM instalará todos os objetos e relatórios do Configuration Manager no servidor pai.</span><span class="sxs-lookup"><span data-stu-id="76dcc-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="76dcc-131">Se você instalar o MBAM no servidor pai, o MBAM executará todas as ações de instalação nesse servidor pai.</span><span class="sxs-lookup"><span data-stu-id="76dcc-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="76dcc-132">**Gerenciador de configuração do System Center 2012** : se você instalar o MBAM em um servidor de site primário ou em um servidor de administração central, o MBAM executará todas as ações de instalação nesse servidor de site.</span><span class="sxs-lookup"><span data-stu-id="76dcc-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="76dcc-133">O console do Configuration Manager deve estar instalado no computador no qual você instala o servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="76dcc-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="76dcc-134">Ao instalar o MBAM com a topologia integrada do Configuration Manager, você deve instalar o console do Configuration Manager no mesmo computador em que o MBAM será instalado.</span><span class="sxs-lookup"><span data-stu-id="76dcc-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="76dcc-135">Se você usar a arquitetura recomendada, que é descrita em [introdução-usando MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), você instalaria o MBAM no servidor de site primário do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="76dcc-136">Novos parâmetros de linha de comando de configuração para a topologia integrada do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76dcc-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="76dcc-137">Parâmetro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="76dcc-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="76dcc-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="76dcc-138">Description</span></span></th>
<th align="left"><span data-ttu-id="76dcc-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76dcc-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="76dcc-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="76dcc-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-141">Permite que você instale os relatórios do Configuration Manager em um servidor remoto do SQL Server Reporting Services (SSRS) que faz parte do mesmo site do Configuration Manager para o qual o MBAM está instalado.</span><span class="sxs-lookup"><span data-stu-id="76dcc-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="76dcc-142">Você pode definir o valor para o nome de domínio totalmente qualificado do servidor de função do ponto do SSRS remoto.</span><span class="sxs-lookup"><span data-stu-id="76dcc-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</span><span class="sxs-lookup"><span data-stu-id="76dcc-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="76dcc-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="76dcc-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-145">Permite que você instale somente os relatórios do Configuration Manager, sem outros objetos do Configuration Manager, como a linha de base, a coleção e os itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="76dcc-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="76dcc-146">Observação</span><span class="sxs-lookup"><span data-stu-id="76dcc-146">Note</span></span></strong><br/><p><span data-ttu-id="76dcc-147">Você deve combinar esse parâmetro com o parâmetro CM_REPORTS_COLLECTION_ID.</span><span class="sxs-lookup"><span data-stu-id="76dcc-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="76dcc-148">Valores de parâmetros válidos:</span><span class="sxs-lookup"><span data-stu-id="76dcc-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="76dcc-149">True</span><span class="sxs-lookup"><span data-stu-id="76dcc-149">True</span></span></p></li>
<li><p><span data-ttu-id="76dcc-150">False</span><span class="sxs-lookup"><span data-stu-id="76dcc-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="76dcc-151">Você pode combinar esse parâmetro com o parâmetro CM_SSRS_REMOTE_SERVER_NAME se quiser instalar os relatórios apenas em um servidor remoto de função do ponto do SSRS.</span><span class="sxs-lookup"><span data-stu-id="76dcc-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="76dcc-152">Se você não definir o parâmetro ou se defini-lo como false, a instalação do MBAM instalará todos os objetos do Configuration Manager, incluindo os relatórios.</span><span class="sxs-lookup"><span data-stu-id="76dcc-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-153">MbamSetup.exe CM_REPORTS_ONLY = verdadeiro</span><span class="sxs-lookup"><span data-stu-id="76dcc-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="76dcc-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="76dcc-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="76dcc-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="76dcc-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-156">Uma ID de coleção existente que identifica a coleção para a qual os dados de conformidade de relatório serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="76dcc-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="76dcc-157">Você pode especificar qualquer ID de coleção.</span><span class="sxs-lookup"><span data-stu-id="76dcc-157">You can specify any collection ID.</span></span> <span data-ttu-id="76dcc-158">Você não precisa usar a ID da coleção "computadores com suporte MBAM".</span><span class="sxs-lookup"><span data-stu-id="76dcc-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="76dcc-159">MbamSetup.exe CM_REPORTS_ONLY = verdadeiro</span><span class="sxs-lookup"><span data-stu-id="76dcc-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="76dcc-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="76dcc-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="76dcc-161">Capacidade de ativar ou desativar o texto do aviso do portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="76dcc-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="76dcc-162">O MBAM 2,0 SP1 permite que você desative o texto de aviso no portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="76dcc-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="76dcc-163">Anteriormente, o texto do aviso é exibido por padrão e você não pôde desativá-lo.</span><span class="sxs-lookup"><span data-stu-id="76dcc-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="76dcc-164">Para desativar o texto de aviso</span><span class="sxs-lookup"><span data-stu-id="76dcc-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="76dcc-165">No servidor em que você instalou o portal de autoatendimento, abra serviços de informações da Internet (IIS) e navegue até **sites &gt; Administração e monitoramento do Microsoft BitLocker &gt; SelfService &gt; configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="76dcc-166">Na coluna **Name** , selecione **DisplayNotice**e defina o valor como **false**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="76dcc-167">Capacidade de localizar a instrução HelpdeskText que aponta os usuários para obter informações mais Autoatendimento do portal</span><span class="sxs-lookup"><span data-stu-id="76dcc-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="76dcc-168">Você pode configurar uma versão localizada da instrução "HelpdeskText" do portal de autoatendimento, que informa aos usuários finais como obter ajuda adicional quando estiverem usando o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="76dcc-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="76dcc-169">Se você configurar o texto localizado para a instrução, conforme descrito nas instruções a seguir, o MBAM exibirá a versão localizada.</span><span class="sxs-lookup"><span data-stu-id="76dcc-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="76dcc-170">Se MBAM não encontrar a versão localizada, ele exibirá o valor que está no parâmetro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="76dcc-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="76dcc-171">Para exibir uma versão localizada da instrução HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="76dcc-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="76dcc-172">No servidor em que você instalou o portal de autoatendimento, abra o IIS e navegue para **sites &gt; Administração e administração do Microsoft BitLocker &gt; SelfService configurações do &gt; aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="76dcc-173">No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="76dcc-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="76dcc-174">No campo **nome** , digite **HelpdeskText**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para o texto.</span><span class="sxs-lookup"><span data-stu-id="76dcc-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="76dcc-175">Por exemplo, para criar uma instrução HelpdeskText localizada em espanhol, você deve nomear o parâmetro HelpdeskText \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="76dcc-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="76dcc-176">Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="76dcc-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="76dcc-177">No campo **valor** , digite o texto localizado que você deseja exibir para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="76dcc-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="76dcc-178">Capacidade de localizar o portal de autoatendimento HelpdeskURL</span><span class="sxs-lookup"><span data-stu-id="76dcc-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="76dcc-179">Você pode configurar uma versão localizada do portal de autoatendimento HelpdeskURL para exibir aos usuários finais por padrão.</span><span class="sxs-lookup"><span data-stu-id="76dcc-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="76dcc-180">Se você criar uma versão localizada, conforme descrito nas instruções a seguir, o MBAM encontrará e exibirá a versão localizada.</span><span class="sxs-lookup"><span data-stu-id="76dcc-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="76dcc-181">Se o MBAM não encontrar uma versão localizada, ele exibirá a URL que está configurada para o parâmetro HelpDeskURL.</span><span class="sxs-lookup"><span data-stu-id="76dcc-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="76dcc-182">Para exibir um HelpdeskURL localizado</span><span class="sxs-lookup"><span data-stu-id="76dcc-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="76dcc-183">No servidor em que você instalou o portal de autoatendimento, abra o IIS e navegue para **sites &gt; Administração e administração do Microsoft BitLocker &gt; SelfService configurações do &gt; aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="76dcc-184">No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="76dcc-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="76dcc-185">No campo **nome** , digite **HelpdeskURL**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para a URL.</span><span class="sxs-lookup"><span data-stu-id="76dcc-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="76dcc-186">Por exemplo, para criar um HelpdeskURL localizado em espanhol, você deve nomear o parâmetro HelpdeskURL \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="76dcc-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="76dcc-187">Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="76dcc-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="76dcc-188">No campo **valor** , digite o HelpdeskURL localizado que você deseja exibir para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="76dcc-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="76dcc-189">Capacidade de localizar o texto de aviso do portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="76dcc-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="76dcc-190">Você pode configurar o texto de aviso localizado para exibir aos usuários finais por padrão no portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="76dcc-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="76dcc-191">O arquivo notice.txt, que exibe o texto do aviso, está localizado no seguinte diretório raiz:</span><span class="sxs-lookup"><span data-stu-id="76dcc-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="76dcc-192">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="76dcc-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="76dcc-193">Para exibir o texto de aviso localizado, crie um arquivo notice.txt localizado e salve-o em uma pasta de idioma específico no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="76dcc-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="76dcc-194">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="76dcc-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="76dcc-195">O MBAM exibe o texto do aviso com base nas seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="76dcc-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="76dcc-196">Se você criar um arquivo notice.txt localizado na pasta de idiomas apropriada, o MBAM exibirá o texto de aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="76dcc-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="76dcc-197">Se o MBAM não encontrar uma versão localizada do arquivo notice.txt, ele exibirá o texto no arquivo de notice.txt padrão.</span><span class="sxs-lookup"><span data-stu-id="76dcc-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="76dcc-198">Se o MBAM não encontrar um arquivo de notice.txt padrão, ele exibirá o texto padrão no portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="76dcc-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="76dcc-199">Observação</span><span class="sxs-lookup"><span data-stu-id="76dcc-199">Note</span></span>**  
<span data-ttu-id="76dcc-200">Se o navegador de um usuário final estiver definido como um idioma que não tenha uma subpasta ou notice.txt de idioma correspondente, o texto que estiver no arquivo notice.txt do diretório raiz a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="76dcc-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="76dcc-201">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="76dcc-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>



**<span data-ttu-id="76dcc-202">Para criar um arquivo notice.txt localizado</span><span class="sxs-lookup"><span data-stu-id="76dcc-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="76dcc-203">No servidor em que você instalou o portal de autoatendimento, crie uma &lt; *language* &gt; pasta de idiomas no seguinte diretório, onde &lt; *idioma* &gt; representa o nome do idioma localizado:</span><span class="sxs-lookup"><span data-stu-id="76dcc-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="76dcc-204">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="76dcc-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    **<span data-ttu-id="76dcc-205">Observação</span><span class="sxs-lookup"><span data-stu-id="76dcc-205">Note</span></span>**  
    <span data-ttu-id="76dcc-206">Algumas pastas de idioma já existem, portanto, talvez você não precise criar uma.</span><span class="sxs-lookup"><span data-stu-id="76dcc-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="76dcc-207">Se você precisar criar uma pasta de idiomas, consulte [referência da API do NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947) para obter uma lista dos nomes válidos que você pode usar para a pasta de &lt; *idiomas* &gt; .</span><span class="sxs-lookup"><span data-stu-id="76dcc-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="76dcc-208">Crie um arquivo notice.txt que contenha o texto de aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="76dcc-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="76dcc-209">Salve o arquivo notice.txt na pasta de &lt; *idiomas* &gt; .</span><span class="sxs-lookup"><span data-stu-id="76dcc-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="76dcc-210">Por exemplo, para criar um arquivo notice.txt localizado em espanhol, salve o arquivo notice.txt localizado na seguinte pasta:</span><span class="sxs-lookup"><span data-stu-id="76dcc-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="76dcc-211">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\es-es do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="76dcc-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="76dcc-212">Atualizando para o MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="76dcc-213">Você pode atualizar para o MBAM 2,0 SP1 a partir de qualquer versão anterior do MBAM.</span><span class="sxs-lookup"><span data-stu-id="76dcc-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="76dcc-214">Atualizando a infraestrutura do MBAM</span><span class="sxs-lookup"><span data-stu-id="76dcc-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="76dcc-215">Você pode atualizar a infraestrutura do MBAM Server para o MBAM 2,0 SP1 da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="76dcc-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="76dcc-216">**Substituição manual do servidor in-loco**: você deve desinstalar manualmente a infraestrutura do servidor do MBAM existente e instalar a infraestrutura de servidor do MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="76dcc-217">Você não precisa remover os bancos de dados para fazer a atualização.</span><span class="sxs-lookup"><span data-stu-id="76dcc-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="76dcc-218">Em vez disso, selecione os bancos de dados existentes, que a versão anterior do MBAM criou.</span><span class="sxs-lookup"><span data-stu-id="76dcc-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="76dcc-219">A instalação da atualização do MBAM 2,0 SP1 migra os bancos de dados existentes para o MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="76dcc-220">**Atualização do cliente distribuído**: se você estiver usando a topologia MBAM autônoma, poderá atualizar os clientes do MBAM gradualmente após a instalação da infraestrutura de servidor MBAM do 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="76dcc-221">Depois de atualizar a infraestrutura do MBAM Server, os clientes do MBAM 1,0 ou do 2,0 serão reportados para o servidor do MBAM 2,0 SP1 e armazenarão os dados de recuperação, mas a conformidade será baseada nas políticas disponíveis para a versão do MBAM cliente que está instalada atualmente.</span><span class="sxs-lookup"><span data-stu-id="76dcc-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="76dcc-222">Para habilitar o relatório de políticas do MBAM 2,0 SP1, você deve atualizar os computadores cliente para o MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="76dcc-223">Você pode atualizar os computadores cliente para o cliente do MBAM 2,0 SP1 sem desinstalar o cliente anterior, e o cliente começará a se aplicar e gerar relatórios com base nas políticas do MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="76dcc-224">Para obter mais informações sobre como atualizar os servidores do MBAM, consulte [atualizando de versões anteriores do MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="76dcc-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="76dcc-225">Atualizando o cliente do MBAM para o MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="76dcc-226">Para atualizar os computadores de usuários finais para o cliente do MBAM 2,0 SP1, execute **MbamClientSetup.exe** em cada computador cliente.</span><span class="sxs-lookup"><span data-stu-id="76dcc-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="76dcc-227">O instalador atualiza automaticamente o cliente para o cliente do MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="76dcc-228">Após a instalação, os computadores cliente não precisam ser reinicializados, e o cliente do MBAM 2,0 SP1 começa a se aplicar e se comunicar com as políticas do MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="76dcc-229">Se estiver usando o MBAM com o Configuration Manager, você deve atualizar os computadores cliente MBAM para o MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="76dcc-230">Para obter mais informações sobre como atualizar os computadores cliente do MBAM, confira o guia [de atualização de versões anteriores do MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="76dcc-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="76dcc-231">Instalar ou atualizar para o MBAM 2,0 SP1 com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76dcc-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="76dcc-232">Esta seção descreve os requisitos durante a instalação do MBAM 2,0 SP1 como uma nova instalação ou atualização para uma instalação anterior do MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="76dcc-233">Arquivos necessários para instalar o MBAM 2,0 SP1 se você estiver usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76dcc-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="76dcc-234">Se você estiver instalando o MBAM pela primeira vez e estiver usando o MBAM 2,0 SP1 com o System Center Configuration Manager, será necessário criar ou editar arquivos MOF para permitir que o MBAM funcione corretamente com o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="76dcc-235">arquivo de configuração. mof</span><span class="sxs-lookup"><span data-stu-id="76dcc-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="76dcc-236">Se você estiver usando o Configuration Manager 2007, será necessário editar o arquivo Configuration. mof completando a etapa 3 do item **atualizar o arquivo Configuration. mof se você atualizar para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007**, que segue este item.</span><span class="sxs-lookup"><span data-stu-id="76dcc-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="76dcc-237">Se você estiver usando o Gerenciador de configuração do System Center 2012, edite o arquivo Configuration. mof seguindo as instruções em [Editar o arquivo Configuration. mof](edit-the-configurationmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="76dcc-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="76dcc-238">**arquivo SMS \ _def. mof** – siga as instruções em [criar ou editar o arquivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="76dcc-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="76dcc-239">Atualize o arquivo Configuration. mof se você atualizar para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="76dcc-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="76dcc-240">Se estiver atualizando para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007, você deve atualizar o arquivo Configuration. MOF para garantir que o MBAM 2,0 SP1 funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="76dcc-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="76dcc-241">Para atualizar o arquivo Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="76dcc-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="76dcc-242">No servidor do Configuration Manager, navegue até o local do arquivo de configuração. mof:</span><span class="sxs-lookup"><span data-stu-id="76dcc-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="76dcc-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="76dcc-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="76dcc-244">Em uma instalação padrão, o local de instalação é%systemdrive%\\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="76dcc-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="76dcc-245">Examine o bloco de código que você acrescentou ao arquivo Configuration. mof e exclua-o.</span><span class="sxs-lookup"><span data-stu-id="76dcc-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="76dcc-246">O bloco de código será semelhante ao mostrado na etapa a seguir.</span><span class="sxs-lookup"><span data-stu-id="76dcc-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="76dcc-247">Copie o bloco de código a seguir e, em seguida, adicione-o ao arquivo Configuration. MOF para adicionar as seguintes classes MBAM necessárias ao arquivo:</span><span class="sxs-lookup"><span data-stu-id="76dcc-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="76dcc-248">Tradução do MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="76dcc-249">O MBAM 2,0 SP1 agora está disponível nos seguintes idiomas:</span><span class="sxs-lookup"><span data-stu-id="76dcc-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="76dcc-250">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="76dcc-250">English (United States) en-US</span></span>
-   <span data-ttu-id="76dcc-251">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="76dcc-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="76dcc-252">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="76dcc-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="76dcc-253">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="76dcc-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="76dcc-254">Espanhol, classificação internacional (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="76dcc-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="76dcc-255">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="76dcc-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="76dcc-256">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="76dcc-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="76dcc-257">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="76dcc-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="76dcc-258">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="76dcc-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="76dcc-259">Chinês tradicional zh-TW</span><span class="sxs-lookup"><span data-stu-id="76dcc-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="76dcc-260">Chinês simplificado zh-CN</span><span class="sxs-lookup"><span data-stu-id="76dcc-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="76dcc-261">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="76dcc-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="76dcc-262">O MBAM 2,0 SP1 faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="76dcc-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="76dcc-263">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="76dcc-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="76dcc-264">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="76dcc-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="76dcc-265">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76dcc-265">Related topics</span></span>

[<span data-ttu-id="76dcc-266">Notas de versão do MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="76dcc-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)









