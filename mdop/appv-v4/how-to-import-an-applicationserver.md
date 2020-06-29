---
title: Como importar um aplicativo
description: Como importar um aplicativo
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797118"
---
# <span data-ttu-id="272cf-103">Como importar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="272cf-103">How to Import an Application</span></span>


<span data-ttu-id="272cf-104">Normalmente, você importa aplicativos para disponibilizá-los para o fluxo de um servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="272cf-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="272cf-105">Você também pode adicionar um aplicativo manualmente, mas deve fornecer informações precisas e detalhadas sobre o aplicativo para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="272cf-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="272cf-106">Para obter mais informações, consulte [como adicionar um aplicativo manualmente](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="272cf-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="272cf-107">**Observação**  Para importar um aplicativo, você deve ter o arquivo Open Software Descriptor (OSD) em seqüência ou o arquivo de projeto do sequenciador (SPRJ) disponível no servidor.</span><span class="sxs-lookup"><span data-stu-id="272cf-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="272cf-108">Ao importar um aplicativo, você deve certificar-se de que o servidor está configurado com um valor no campo **caminho de conteúdo padrão** na guia **geral** da caixa de diálogo **Opções do sistema** (acessível, clicando com o botão direito do mouse no nó do **sistema** App-V do App-V Server).</span><span class="sxs-lookup"><span data-stu-id="272cf-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="272cf-109">O valor padrão de caminho de conteúdo define onde os aplicativos serão importados e durante o processo de importação, esse valor é usado para modificar os caminhos definidos no arquivo OSD para o arquivo SFT e para os atalhos de ícone.</span><span class="sxs-lookup"><span data-stu-id="272cf-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="272cf-110">No arquivo OSD, o caminho para o arquivo SFT é especificado na entrada HREF de CODEBASE e o caminho para os ícones é especificado na entrada atalhos.</span><span class="sxs-lookup"><span data-stu-id="272cf-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="272cf-111">Durante o processo de importação, o protocolo, o servidor e, se estiverem presentes, a porta especificada nesses dois caminhos no arquivo OSD serão substituídas pelo valor do caminho de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="272cf-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="272cf-112">A tabela a seguir fornece um exemplo de como o caminho de importação será afetado.</span><span class="sxs-lookup"><span data-stu-id="272cf-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="272cf-113">Caminho de conteúdo padrão</span><span class="sxs-lookup"><span data-stu-id="272cf-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="272cf-114">BASE de código do arquivo OSD HREF</span><span class="sxs-lookup"><span data-stu-id="272cf-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="272cf-115">Valor resultante</span><span class="sxs-lookup"><span data-stu-id="272cf-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="272cf-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="272cf-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="272cf-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="272cf-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="272cf-118">Para importar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="272cf-118">To import an application</span></span>**

1.  <span data-ttu-id="272cf-119">Clique com o botão direito do mouse no nó **aplicativos** no painel esquerdo e escolha **importar aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="272cf-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="272cf-120">Na caixa de diálogo **abrir** , navegue até o arquivo SPRJ ou OSD do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="272cf-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="272cf-121">Realce o arquivo e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="272cf-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="272cf-122">No **Assistente para novo aplicativo**, certifique-se de que a caixa **habilitado** esteja selecionada para os aplicativos que você deseja transmitir.</span><span class="sxs-lookup"><span data-stu-id="272cf-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="272cf-123">Você também pode inserir uma descrição e verificar os caminhos do servidor e do arquivo.</span><span class="sxs-lookup"><span data-stu-id="272cf-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="272cf-124">Além disso, se você tiver configurado licenças e grupos de servidores, poderá selecionar esses grupos.</span><span class="sxs-lookup"><span data-stu-id="272cf-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="272cf-125">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="272cf-125">Click **Next**.</span></span>

5.  <span data-ttu-id="272cf-126">Na tela **atalhos publicados** , marque as caixas dos locais onde você gostaria que os atalhos do aplicativo aparecessem nos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="272cf-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="272cf-127">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="272cf-127">Click **Next**.</span></span>

7.  <span data-ttu-id="272cf-128">Na tela **associações de arquivo** , você pode adicionar novas associações de arquivo a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="272cf-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="272cf-129">Para fazer isso, clique em **Adicionar**, insira a extensão (sem um ponto precedente), insira uma descrição e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="272cf-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="272cf-130">**Observação**  Aplicativos sequenciados com o sequenciador 4,0 preencha a caixa de diálogo **associações de arquivos** ao importar ou criá-las por meio do console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="272cf-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="272cf-131">Aplicativos com pacotes de versão do sequenciador anteriores não.</span><span class="sxs-lookup"><span data-stu-id="272cf-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="272cf-132">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="272cf-132">Click **Next**.</span></span>

9.  <span data-ttu-id="272cf-133">Na tela **permissões de acesso** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="272cf-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="272cf-134">Preencha a caixa de diálogo **Selecionar grupos** .</span><span class="sxs-lookup"><span data-stu-id="272cf-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="272cf-135">Quando terminar, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="272cf-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="272cf-136">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="272cf-136">Click **Next**.</span></span>

12. <span data-ttu-id="272cf-137">Na tela **Resumo** , você pode revisar as configurações de importação.</span><span class="sxs-lookup"><span data-stu-id="272cf-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="272cf-138">Clique em **concluir**ou em **retornar** para alterar a importação ou clique em **Cancelar** para cancelar a importação.</span><span class="sxs-lookup"><span data-stu-id="272cf-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="272cf-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="272cf-139">Related topics</span></span>


[<span data-ttu-id="272cf-140">Como gerenciar grupos de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="272cf-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="272cf-141">Como gerenciar aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="272cf-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="272cf-142">Como adicionar um aplicativo manualmente</span><span class="sxs-lookup"><span data-stu-id="272cf-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





