---
title: Como implantar o cliente do App-V
description: Como implantar o cliente do App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796421"
---
# <span data-ttu-id="496cf-103">Como implantar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="496cf-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="496cf-104">Use o procedimento a seguir para instalar o cliente do Microsoft Application Virtualization (App-V) 5,1 e o cliente de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="496cf-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="496cf-105">Você deve instalar a versão do cliente que corresponde ao sistema operacional do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="496cf-106">O que fazer antes de começar</span><span class="sxs-lookup"><span data-stu-id="496cf-106">What to do before you start</span></span>**

1. <span data-ttu-id="496cf-107">Revise e instale os pré-requisitos do software:</span><span class="sxs-lookup"><span data-stu-id="496cf-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="496cf-108">Instale o software obrigatório que corresponde à versão do App-V que você está instalando:</span><span class="sxs-lookup"><span data-stu-id="496cf-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="496cf-109">Sobre o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="496cf-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="496cf-110">Pré-requisitos do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="496cf-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="496cf-111">Revise os cenários de coexistência e sem suporte do cliente, conforme aplicável à sua instalação:</span><span class="sxs-lookup"><span data-stu-id="496cf-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-112">Implantando clientes App-V coexistentes</span><span class="sxs-lookup"><span data-stu-id="496cf-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="496cf-113">Planejamento para a implantação do sequenciador e do cliente do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="496cf-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-114">Cenários de instalação sem suporte ou limitados</span><span class="sxs-lookup"><span data-stu-id="496cf-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-115">Consulte a seção cliente nas <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurações com suporte do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="496cf-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="496cf-116">Examine os locais do registro do cliente, log e informações de solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="496cf-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496cf-117">Informações do registro do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="496cf-118">Por padrão, depois de instalar o cliente App-V 5,1, as informações do cliente são armazenadas no registro na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="496cf-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="496cf-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE</span><span class="sxs-lookup"><span data-stu-id="496cf-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="496cf-120">Quando você implanta um pacote virtualizado em um computador que está executando o cliente App-V, os dados do pacote associado são armazenados no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="496cf-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="496cf-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="496cf-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="496cf-122">No entanto, você pode reconfigurar esse local com a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="496cf-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="496cf-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE \ STREAMING \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="496cf-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496cf-124">Arquivos de log do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="496cf-125">Para informações do arquivo de log associadas ao cliente App-V 5,1, pesquise no seguinte log:</span><span class="sxs-lookup"><span data-stu-id="496cf-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="496cf-126">Logs de eventos/aplicativos e serviços Logs/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="496cf-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="496cf-127">No App-V 5,0 SP3, alguns registros foram consolidados e movidos para o seguinte local:</span><span class="sxs-lookup"><span data-stu-id="496cf-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="496cf-128">Logs de eventos/aplicativos e serviços Logs/Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="496cf-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="496cf-129">Para obter uma lista dos logs movidos, consulte <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> sobre o App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="496cf-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="496cf-130">Os pacotes armazenados atualmente em computadores que executam o cliente App-V 5,1 são salvos no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="496cf-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="496cf-131">C:\ProgramData\App-V &amp; lt; ID do pacote &gt; &amp; lt; ID da versão&gt;</span><span class="sxs-lookup"><span data-stu-id="496cf-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496cf-132">Informações de solução de problemas de instalação do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="496cf-133">Consulte o log de erros na <strong> pasta% temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="496cf-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="496cf-134">Para examinar os arquivos de registro, clique em <strong> Iniciar </strong> , digite <strong> % temp% </strong> e procure o <strong> log de appv_ </strong> .</span><span class="sxs-lookup"><span data-stu-id="496cf-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="496cf-135">Para instalar o cliente do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="496cf-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="496cf-136">Copie o arquivo de instalação do cliente do App-V 5,1 para o computador em que ele será instalado.</span><span class="sxs-lookup"><span data-stu-id="496cf-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="496cf-137">Escolha um dos seguintes tipos de cliente:</span><span class="sxs-lookup"><span data-stu-id="496cf-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="496cf-138">Tipo de cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="496cf-139">Arquivo a ser usado</span><span class="sxs-lookup"><span data-stu-id="496cf-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="496cf-140">Versão padrão do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="496cf-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="496cf-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="496cf-142">Versão dos serviços de área de trabalho remota do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="496cf-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="496cf-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="496cf-144">Clique duas vezes no arquivo de instalação e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="496cf-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="496cf-145">Antes da instalação começar, o instalador verifica o computador em busca de [pré-requisitos do App-V 5,1](app-v-51-prerequisites.md)ausentes.</span><span class="sxs-lookup"><span data-stu-id="496cf-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="496cf-146">Revise e aceite os termos de licença para software, escolha se deseja usar o Microsoft Update e se quer participar do programa de aperfeiçoamento da experiência do usuário da Microsoft e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="496cf-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="496cf-147">Na página **configuração concluída com êxito** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="496cf-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="496cf-148">A instalação cria as seguintes entradas para o cliente App-V nos **programas**:</span><span class="sxs-lookup"><span data-stu-id="496cf-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="496cf-149">.exe</span><span class="sxs-lookup"><span data-stu-id="496cf-149">.exe</span></span>**

    -   **<span data-ttu-id="496cf-150">.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-150">.msi</span></span>**

    -   **<span data-ttu-id="496cf-151">pacote de idiomas</span><span class="sxs-lookup"><span data-stu-id="496cf-151">language pack</span></span>**

        **<span data-ttu-id="496cf-152">Observação</span><span class="sxs-lookup"><span data-stu-id="496cf-152">Note</span></span>**  
        <span data-ttu-id="496cf-153">Após a instalação, somente o arquivo. exe pode ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="496cf-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="496cf-154">Para instalar o cliente do App-V 5,1 usando um script</span><span class="sxs-lookup"><span data-stu-id="496cf-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="496cf-155">Instale todo o software de pré-requisito obrigatório nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="496cf-156">Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="496cf-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="496cf-157">Se você instalar o cliente usando um arquivo. msi, a instalação falhará se algum pré-requisito estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="496cf-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="496cf-158">Para usar um script para instalar o cliente App-V 5,1, use os parâmetros a seguir com **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="496cf-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="496cf-159">Observação</span><span class="sxs-lookup"><span data-stu-id="496cf-159">Note</span></span>**  
   <span data-ttu-id="496cf-160">O Windows Installer (. msi) do cliente oferece suporte ao mesmo conjunto de opções, exceto para o parâmetro **/log** .</span><span class="sxs-lookup"><span data-stu-id="496cf-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="496cf-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-162">Especifica o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="496cf-162">Specifies the installation directory.</span></span> <span data-ttu-id="496cf-163">Exemplo de uso: <strong> /installdir = C:\Program Files\AppV Client</span><span class="sxs-lookup"><span data-stu-id="496cf-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="496cf-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-165">Habilita a participação no programa de aperfeiçoamento da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="496cf-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="496cf-166">Exemplo de uso: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="496cf-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-168">Habilita o Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="496cf-168">Enables Microsoft Update.</span></span> <span data-ttu-id="496cf-169">Exemplo de uso: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="496cf-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-171">Especifica o diretório no qual instalará todos os novos aplicativos e atualizações.</span><span class="sxs-lookup"><span data-stu-id="496cf-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="496cf-172">Exemplo de uso: <strong> /PACKAGEINSTALLATIONROOT = pacotes C:\App-V de&#39;&#39;</span><span class="sxs-lookup"><span data-stu-id="496cf-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="496cf-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-174">Substitui o local de origem para baixar o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="496cf-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="496cf-175">Exemplo de uso: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="496cf-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="496cf-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-177">Especifica como novos pacotes serão carregados pelo App-V 5,1 em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="496cf-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="496cf-178">As opções a seguir estão habilitadas: [1]; carregar automaticamente todos os pacotes [2]; ou carregar automaticamente nenhum pacote [0]. <strong> Exemplo de uso:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="496cf-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="496cf-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-180">Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="496cf-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="496cf-181">Exemplo de uso: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="496cf-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-183">Permite que o cliente do App-V 5,1 modifique os atalhos e FTAs associados aos pacotes criados com uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="496cf-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="496cf-184">Exemplo de uso: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="496cf-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-186">Habilita os scripts definidos no arquivo de manifesto do pacote ou arquivos de configuração que devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="496cf-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="496cf-187">Exemplo de uso: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="496cf-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-189">Especifica os caminhos do registro que não serão movidos para um perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="496cf-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="496cf-190">Exemplo de uso: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="496cf-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="496cf-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-192">Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário&#39;s.</span><span class="sxs-lookup"><span data-stu-id="496cf-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="496cf-193">Exemplo de uso: <strong> /ROAMINGFILEEXCLUSIONS área de trabalho do &#39;; minhas imagens&#39;</span><span class="sxs-lookup"><span data-stu-id="496cf-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="496cf-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-195">Exibe o nome do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="496cf-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="496cf-196">Exemplo de uso: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="496cf-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="496cf-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-198">Exibe a URL do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="496cf-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="496cf-199">Exemplo de uso: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="496cf-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="496cf-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-201">Habilita uma atualização de publicação global.</span><span class="sxs-lookup"><span data-stu-id="496cf-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="496cf-202">Exemplo de uso: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="496cf-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-204">Inicia uma atualização de publicação global quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="496cf-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="496cf-205">Exemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="496cf-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-207">Especifica o intervalo de atualização de publicação, em que <strong> 0 indica que a </strong> atualização não é periódica.</span><span class="sxs-lookup"><span data-stu-id="496cf-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="496cf-208">Exemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="496cf-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="496cf-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-210">Especifica a unidade de intervalo (horas [0], dias [1]).</span><span class="sxs-lookup"><span data-stu-id="496cf-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="496cf-211">Exemplo de uso: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="496cf-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-213">Permite a atualização da publicação do usuário.</span><span class="sxs-lookup"><span data-stu-id="496cf-213">Enables user publishing refresh.</span></span> <span data-ttu-id="496cf-214">Exemplo de uso: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="496cf-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-216">Inicia uma atualização de publicação do usuário quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="496cf-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="496cf-217">Exemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="496cf-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-219">Especifica o intervalo de atualização de publicação, em que <strong> 0 indica que a </strong> atualização não é periódica.</span><span class="sxs-lookup"><span data-stu-id="496cf-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="496cf-220">Exemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="496cf-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="496cf-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-222">Especifica a unidade de intervalo (horas [0], dias [1]).</span><span class="sxs-lookup"><span data-stu-id="496cf-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="496cf-223">Exemplo de uso: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="496cf-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-224">/Log</span><span class="sxs-lookup"><span data-stu-id="496cf-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-225">Especifica um local onde as informações do log são salvas.</span><span class="sxs-lookup"><span data-stu-id="496cf-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="496cf-226">O local padrão é% Temp%.</span><span class="sxs-lookup"><span data-stu-id="496cf-226">The default location is %Temp%.</span></span> <span data-ttu-id="496cf-227">Exemplo de uso: <strong> /log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="496cf-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-228">/q</span><span class="sxs-lookup"><span data-stu-id="496cf-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-229">Especifica uma instalação autônoma.</span><span class="sxs-lookup"><span data-stu-id="496cf-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-230">/REPAIR</span><span class="sxs-lookup"><span data-stu-id="496cf-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-231">Repara uma instalação anterior do cliente.</span><span class="sxs-lookup"><span data-stu-id="496cf-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="496cf-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-233">Impede que o computador reinicie após a instalação do cliente.</span><span class="sxs-lookup"><span data-stu-id="496cf-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="496cf-234">O parâmetro impede que o computador do usuário final reinicie a reinicialização após a instalação de cada atualização e permite que você agende a reinicialização da sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="496cf-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="496cf-235">Por exemplo, você pode instalar o App-V 5,1 e, em seguida, instalar o pacote de hotfix Y sem reinicialização após a instalação do Service Pack.</span><span class="sxs-lookup"><span data-stu-id="496cf-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="496cf-236">Após a instalação, você deve reinicializar antes de começar a usar o App-V.</span><span class="sxs-lookup"><span data-stu-id="496cf-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="496cf-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-238">Desinstala o cliente.</span><span class="sxs-lookup"><span data-stu-id="496cf-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="496cf-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-240">Aceita o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="496cf-240">Accepts the license agreement.</span></span> <span data-ttu-id="496cf-241">Isso é necessário para uma instalação automática.</span><span class="sxs-lookup"><span data-stu-id="496cf-241">This is required for an unattended installation.</span></span> <span data-ttu-id="496cf-242">Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="496cf-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="496cf-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-244">Especifica a ação de layout associado.</span><span class="sxs-lookup"><span data-stu-id="496cf-244">Specifies the associated layout action.</span></span> <span data-ttu-id="496cf-245">Ele também extrai o Windows Installer (. msi) e arquivos de script para uma pasta sem instalar o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="496cf-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="496cf-246">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="496cf-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="496cf-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="496cf-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-248">Especifica o diretório de layout.</span><span class="sxs-lookup"><span data-stu-id="496cf-248">Specifies the layout directory.</span></span> <span data-ttu-id="496cf-249">Requer um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="496cf-249">Requires a string value.</span></span> <span data-ttu-id="496cf-250">Exemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualização C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="496cf-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="496cf-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="496cf-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="496cf-252">Solicita ajuda sobre os parâmetros de instalação anteriores.</span><span class="sxs-lookup"><span data-stu-id="496cf-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="496cf-253">Para instalar o cliente do App-V 5,1 usando o arquivo do Windows Installer (. msi)</span><span class="sxs-lookup"><span data-stu-id="496cf-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="496cf-254">Instale os pré-requisitos obrigatórios nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="496cf-255">Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="496cf-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="496cf-256">Se algum pré-requisito não for atendido, a instalação irá falhar.</span><span class="sxs-lookup"><span data-stu-id="496cf-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="496cf-257">Certifique-se de que os computadores de destino não tenham reinícios pendentes antes de instalar o cliente usando os arquivos do Windows Installer (. msi) do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="496cf-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="496cf-258">Os arquivos do Windows Installer não sinalizam uma reinicialização pendente.</span><span class="sxs-lookup"><span data-stu-id="496cf-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="496cf-259">Implante um dos seguintes arquivos do Windows Installer para o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="496cf-260">O arquivo especificado deve corresponder à configuração do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="496cf-261">Tipo de implantação</span><span class="sxs-lookup"><span data-stu-id="496cf-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="496cf-262">Implantar este arquivo</span><span class="sxs-lookup"><span data-stu-id="496cf-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="496cf-263">O computador está executando um sistema operacional Microsoft Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="496cf-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="496cf-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="496cf-265">O computador está executando um sistema operacional Microsoft Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="496cf-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="496cf-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="496cf-267">Você está implantando o cliente dos serviços de área de trabalho remota do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="496cf-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="496cf-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="496cf-269">Usando as informações da tabela a seguir, selecione o pacote de idiomas apropriado para instalar, com base no idioma **desejado para o** computador de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="496cf-270">O **xxxx** na tabela refere-se à localidade de destino do pacote de idiomas.</span><span class="sxs-lookup"><span data-stu-id="496cf-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="496cf-271">O que saber antes de começar:</span><span class="sxs-lookup"><span data-stu-id="496cf-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="496cf-272">Os pacotes de idiomas são comuns ao cliente padrão do App-V 5,1 e à versão dos serviços de área de trabalho remota do App-V 5,1 Client.</span><span class="sxs-lookup"><span data-stu-id="496cf-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="496cf-273">Se você instalar o cliente do App-V 5,1 usando o **. exe**, o instalador implantará apenas o pacote de idiomas que corresponde ao sistema operacional em execução no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="496cf-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="496cf-274">Para implantar pacotes de idiomas adicionais em um computador de destino, use o procedimento **para instalar o cliente do App-V 5,1 usando o arquivo do Windows Installer (. msi)**.</span><span class="sxs-lookup"><span data-stu-id="496cf-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="496cf-275">Tipo de implantação</span><span class="sxs-lookup"><span data-stu-id="496cf-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="496cf-276">Implantar este arquivo</span><span class="sxs-lookup"><span data-stu-id="496cf-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="496cf-277">O computador está executando um sistema operacional Microsoft Windows de 32 bits</span><span class="sxs-lookup"><span data-stu-id="496cf-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="496cf-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="496cf-279">O computador está executando um sistema operacional Microsoft Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="496cf-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="496cf-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="496cf-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="496cf-281">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="496cf-281">Related topics</span></span>


[<span data-ttu-id="496cf-282">Implantação do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="496cf-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="496cf-283">Sobre as configurações do cliente</span><span class="sxs-lookup"><span data-stu-id="496cf-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="496cf-284">Como desinstalar o cliente do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="496cf-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









