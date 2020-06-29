---
title: Como instalar o sequenciador
description: Como instalar o sequenciador
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796378"
---
# <span data-ttu-id="b56fa-103">Como instalar o sequenciador</span><span class="sxs-lookup"><span data-stu-id="b56fa-103">How to Install the Sequencer</span></span>


<span data-ttu-id="b56fa-104">Use o procedimento a seguir para instalar o sequenciador do Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="b56fa-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="b56fa-105">O computador que executará o sequenciador não deve estar executando qualquer versão do cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b56fa-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="b56fa-106">Não há suporte para a atualização de uma instalação anterior do sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="b56fa-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="b56fa-107">**Importante**  Para obter uma lista completa dos requisitos do sequenciador, consulte as seções do sequenciador de [pré-requisitos do App-v 5,0](app-v-50-prerequisites.md) e do [app-v 5,0 com suporte](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="b56fa-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="b56fa-108">Você também pode usar a linha de comando para instalar o App-V 5,0 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b56fa-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="b56fa-109">A lista a seguir exibe informações sobre as opções para instalar o sequenciador usando a linha de comando e **appv\_sequencer\_setup.exe**:</span><span class="sxs-lookup"><span data-stu-id="b56fa-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b56fa-110">Comando</span><span class="sxs-lookup"><span data-stu-id="b56fa-110">Command</span></span></th>
<th align="left"><span data-ttu-id="b56fa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b56fa-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56fa-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="b56fa-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-113">Especifica o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="b56fa-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b56fa-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b56fa-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-115">Habilita a participação no programa de aperfeiçoamento da experiência do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b56fa-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56fa-116">/Log</span><span class="sxs-lookup"><span data-stu-id="b56fa-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-117">Especifica onde o log de instalação será salvo, o local padrão é <strong> % temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="b56fa-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="b56fa-118">Por exemplo, <strong> C:\ Logs \ log. log </strong> .</span><span class="sxs-lookup"><span data-stu-id="b56fa-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b56fa-119">/q</span><span class="sxs-lookup"><span data-stu-id="b56fa-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-120">Especifica uma instalação silenciosa ou silenciosa.</span><span class="sxs-lookup"><span data-stu-id="b56fa-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56fa-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="b56fa-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-122">Especifica a remoção do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="b56fa-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b56fa-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="b56fa-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-124">Aceita o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="b56fa-124">Accepts the license agreement.</span></span> <span data-ttu-id="b56fa-125">Isso é necessário para uma instalação automática.</span><span class="sxs-lookup"><span data-stu-id="b56fa-125">This is required for an unattended installation.</span></span> <span data-ttu-id="b56fa-126">Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="b56fa-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56fa-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="b56fa-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-128">Especifica a ação de layout associado.</span><span class="sxs-lookup"><span data-stu-id="b56fa-128">Specifies the associated layout action.</span></span> <span data-ttu-id="b56fa-129">Ele também extrai o Windows Installer (. msi) e arquivos de script para uma pasta sem instalar o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b56fa-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="b56fa-130">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="b56fa-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b56fa-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="b56fa-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-132">Especifica o diretório de layout.</span><span class="sxs-lookup"><span data-stu-id="b56fa-132">Specifies the layout directory.</span></span> <span data-ttu-id="b56fa-133">Requer um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b56fa-133">Requires a string value.</span></span> <span data-ttu-id="b56fa-134">Exemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualização C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="b56fa-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56fa-135">/?</span><span class="sxs-lookup"><span data-stu-id="b56fa-135">/?</span></span> <span data-ttu-id="b56fa-136">Ou/h ou/Help</span><span class="sxs-lookup"><span data-stu-id="b56fa-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56fa-137">Exibe a ajuda associada.</span><span class="sxs-lookup"><span data-stu-id="b56fa-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b56fa-138">Para instalar o sequenciador do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b56fa-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="b56fa-139">Copie os arquivos de instalação do sequenciador do App-V 5,0 para o computador em que ele será instalado.</span><span class="sxs-lookup"><span data-stu-id="b56fa-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="b56fa-140">Clique duas vezes **appv\_sequencer\_setup.exe** e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="b56fa-141">Na página **termos de licença para software** , você deve revisar os termos de licença.</span><span class="sxs-lookup"><span data-stu-id="b56fa-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="b56fa-142">Para aceitar os termos de licença **, selecione aceito os termos de licença.**</span><span class="sxs-lookup"><span data-stu-id="b56fa-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="b56fa-143">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-143">Click **Next**.</span></span>

3.  <span data-ttu-id="b56fa-144">Na página **usar o Microsoft Update para ajudar a manter o seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="b56fa-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="b56fa-145">Para desabilitar a execução de atualizações da Microsoft **, selecione não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="b56fa-146">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-146">Click **Next**.</span></span>

4.  <span data-ttu-id="b56fa-147">Na página do **programa de aperfeiçoamento da experiência do usuário** , para participar do programa, selecione **ingressar no programa de aperfeiçoamento da experiência do usuário**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="b56fa-148">Isso permitirá que as informações sejam coletadas sobre como você está usando o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b56fa-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="b56fa-149">Se não quiser participar do programa, selecione **não quero participar do programa no momento**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="b56fa-150">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-150">Click **Install**.</span></span>

5.  <span data-ttu-id="b56fa-151">Para abrir o sequenciador, clique em **Iniciar** e em **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="b56fa-152">Para solucionar problemas de instalação do sequenciador do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b56fa-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="b56fa-153">Para obter mais informações sobre a instalação do sequenciador, você pode exibir o log de erros na pasta **% Temp%** .</span><span class="sxs-lookup"><span data-stu-id="b56fa-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="b56fa-154">Para examinar os arquivos de log, clique em **Iniciar**, digite **% Temp%** e procure o **log appv\_**.</span><span class="sxs-lookup"><span data-stu-id="b56fa-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="b56fa-155">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="b56fa-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b56fa-156">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="b56fa-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b56fa-157">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="b56fa-157">Got an App-V issue?</span></span>** <span data-ttu-id="b56fa-158">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b56fa-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b56fa-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b56fa-159">Related topics</span></span>


[<span data-ttu-id="b56fa-160">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="b56fa-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





