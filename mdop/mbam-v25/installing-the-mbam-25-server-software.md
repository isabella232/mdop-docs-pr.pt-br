---
title: Instalando o software de servidor do MBAM 2.5
description: Instalando o software de servidor do MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799263"
---
# <span data-ttu-id="4aa4e-103">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="4aa4e-104">Este tópico descreve como instalar o software de servidor Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando o assistente de configuração de administração e administração do Microsoft BitLocker ou usando parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="4aa4e-105">Repita o processo de instalação do servidor para cada servidor no qual você está configurando os recursos do MBAM 2,5 Server.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="4aa4e-106">Após concluir a instalação, consulte [Configurando os recursos do servidor do MBAM 2,5](configuring-the-mbam-25-server-features.md) para ver as etapas sobre como configurar os recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4aa4e-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="4aa4e-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="4aa4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aa4e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa4e-109">Examinar as informações de planejamento do MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="4aa4e-110">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="4aa4e-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="4aa4e-111">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="4aa4e-112">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4aa4e-113">Leia como obter arquivos de log</span><span class="sxs-lookup"><span data-stu-id="4aa4e-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-114">Por padrão, os arquivos de log são criados na pasta% Temp% do computador local.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="4aa4e-115">Para gravar os arquivos de log em um local específico, em vez de na <strong> pasta% temp </strong> %, use o <strong> </strong> &lt; <em> argumento/log Location </em> &gt; .</span><span class="sxs-lookup"><span data-stu-id="4aa4e-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="4aa4e-116">Outros eventos podem ser registrados em Visualizador de eventos nos <strong> nós MBAM, Setup </strong> ou <strong> MBAM-Web </strong> em <strong> aplicativos e serviços registra o &gt; Microsoft &gt; Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="4aa4e-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="4aa4e-117">Por exemplo, se você desinstalar o MBAM, o desinstalador também desinstalará os logs da MBAM-instalação e MBAM-no EventViewer.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4aa4e-118">Instalar o software de servidor do MBAM 2,5 usando o assistente de configuração de monitoramento e administração do Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="4aa4e-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="4aa4e-119">Use estas etapas para instalar o software MBAM Server usando o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="4aa4e-120">Para instalar o software de servidor MBAM 2,5 usando o assistente</span><span class="sxs-lookup"><span data-stu-id="4aa4e-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="4aa4e-121">No servidor em que você deseja instalar o MBAM, execute **MBAMserversetup.exe** para iniciar o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="4aa4e-122">Na página de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="4aa4e-123">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="4aa4e-124">Escolha se deseja usar o Microsoft Update ao verificar se há atualizações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="4aa4e-125">Escolha se deseja participar do programa de aperfeiçoamento da experiência do usuário e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="4aa4e-126">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="4aa4e-127">Para configurar os recursos de servidor após a instalação do software do servidor MBAM, marque a caixa de seleção **executar configuração do servidor do MBAM após o assistente se fechar** .</span><span class="sxs-lookup"><span data-stu-id="4aa4e-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="4aa4e-128">Você também pode configurar o MBAM mais tarde usando o atalho de **configuração do servidor do MBAM** que a instalação do servidor cria no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="4aa4e-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="4aa4e-129">Clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-129">Click **Finish**.</span></span>

## <span data-ttu-id="4aa4e-130">Instalar o software de servidor MBAM 2,5 usando uma janela do prompt de comando</span><span class="sxs-lookup"><span data-stu-id="4aa4e-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="4aa4e-131">Em um prompt de comando, digite um comando semelhante ao seguinte comando para instalar o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="4aa4e-132">A tabela a seguir descreve os parâmetros de linha de comando para a instalação do software de servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4aa4e-133">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aa4e-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4aa4e-134">Valor do parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aa4e-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="4aa4e-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aa4e-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa4e-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="4aa4e-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-137">Verdadeiro falso</span><span class="sxs-lookup"><span data-stu-id="4aa4e-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-138">Verdadeiro – participe do programa experiência de aprimoramento do cliente, que ajuda a Microsoft a identificar quais recursos de MBAM para melhorar.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="4aa4e-139">False – não participa do programa experiência de aprimoramento do cliente.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4aa4e-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="4aa4e-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-141">Verdadeiro falso</span><span class="sxs-lookup"><span data-stu-id="4aa4e-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-142">True – use o Microsoft Update para manter seu computador seguro e atualizado para Windows e outros produtos da Microsoft, incluindo o MBAM.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="4aa4e-143">Falso – não usar o Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="4aa4e-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa4e-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="4aa4e-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-145">&lt;Caminho&gt;</span><span class="sxs-lookup"><span data-stu-id="4aa4e-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-146">Local onde você deseja instalar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="4aa4e-147">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="4aa4e-147">Example:</span></span></p>
<p><span data-ttu-id="4aa4e-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="4aa4e-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4aa4e-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="4aa4e-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-150">Verdadeiro falso</span><span class="sxs-lookup"><span data-stu-id="4aa4e-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa4e-151">True – continuar o processo de desinstalação do MBAM, mesmo se houver falha na remoção de qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="4aa4e-152">Falso (padrão) se a ação personalizada de desinstalação não conseguir remover um recurso do servidor MBAM adicionado, a desinstalação falha e o MBAM permanecerá instalado.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="4aa4e-153">Em ambos os casos, todos os recursos que foram removidos com sucesso durante a tentativa de desinstalar o MBAM permanecem removidos.</span><span class="sxs-lookup"><span data-stu-id="4aa4e-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="4aa4e-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aa4e-154">Related topics</span></span>


[<span data-ttu-id="4aa4e-155">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="4aa4e-156">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4aa4e-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="4aa4e-157">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="4aa4e-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4aa4e-158">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4aa4e-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4aa4e-159">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4aa4e-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





