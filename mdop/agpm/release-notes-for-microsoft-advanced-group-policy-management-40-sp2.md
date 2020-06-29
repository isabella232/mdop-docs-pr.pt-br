---
title: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2
description: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797715"
---
# <span data-ttu-id="43aba-103">Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="43aba-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="43aba-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="43aba-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="43aba-105">Leia estas notas de versão cuidadosamente antes de instalar o serviço de gerenciamento de política de grupo (AGPM) Pack2 (SP2) 4.0 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="43aba-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="43aba-106">Estas notas da versão contêm informações que são necessárias para instalar com êxito o AGPM 4.0 SP2 e contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="43aba-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="43aba-107">Se houver uma diferença entre essas notas de versão e outra documentação do AGPM, considere as alterações mais recentes autorizadas.</span><span class="sxs-lookup"><span data-stu-id="43aba-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="43aba-108">Estas notas de versão substituem o conteúdo incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="43aba-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="43aba-109">Problemas conhecidos do AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="43aba-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="43aba-110">Esta seção descreve os problemas conhecidos do AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="43aba-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="43aba-111">A ferramenta "Desinstalar" do painel de controle pode não funcionar quando você tenta alterar as configurações do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="43aba-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="43aba-112">A ferramenta no painel de controle que você usa para desinstalar ou alterar um programa pode não funcionar quando você tenta alterar as configurações do servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="43aba-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="43aba-113">**Solução alternativa:** Antes de tentar alterar as configurações do servidor de AGPM usando o painel de controle, faça uma cópia da pasta de arquivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="43aba-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="43aba-114">Em seguida, você pode usar Setup.exe para reinstalar o servidor do AGPM e escolher os parâmetros de configuração desejados.</span><span class="sxs-lookup"><span data-stu-id="43aba-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="43aba-115">Os relatórios não exibem os links que foram adicionados a um objeto de política de grupo</span><span class="sxs-lookup"><span data-stu-id="43aba-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="43aba-116">As configurações do AGPM e os relatórios de diferença não exibem os links que foram adicionados a um objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="43aba-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="43aba-117">**Solução alternativa:** Para exibir os links nos relatórios, selecione o GPO no console de gerenciamento de política de grupo (GPMC) e, em seguida, clique na guia **configurações** no painel direito.</span><span class="sxs-lookup"><span data-stu-id="43aba-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="43aba-118">Relatórios não exibe todas as opções configurações de propriedades de opção</span><span class="sxs-lookup"><span data-stu-id="43aba-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="43aba-119">As configurações do AGPM e os relatórios de diferença não exibem todas as configurações selecionadas na janela **Propriedades de opções de escolha** no editor de objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="43aba-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="43aba-120">**Solução alternativa:** Use o GPMC para exibir as configurações de **Opções de opções de escolha** selecionadas nos relatórios.</span><span class="sxs-lookup"><span data-stu-id="43aba-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="43aba-121">Os relatórios podem não exibir as guias mostrar e ocultar em determinados navegadores</span><span class="sxs-lookup"><span data-stu-id="43aba-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="43aba-122">As guias **Mostrar** e **ocultar** , no lado direito das configurações do AGPM e relatórios de diferença, podem não aparecer quando você vê os relatórios no Google Chrome ou no Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="43aba-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="43aba-123">**Solução alternativa:** Exiba os relatórios usando o navegador Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="43aba-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="43aba-124">As configurações do AGPM e os relatórios de diferença podem mostrar conteúdo diferente dos relatórios do GPMC</span><span class="sxs-lookup"><span data-stu-id="43aba-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="43aba-125">As configurações do AGPM e os relatórios de diferença podem não mostrar o mesmo conteúdo que os relatórios no GPMC.</span><span class="sxs-lookup"><span data-stu-id="43aba-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="43aba-126">**Solução alternativa:** Use o GPMC para ver os relatórios do AGPM.</span><span class="sxs-lookup"><span data-stu-id="43aba-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="43aba-127">O serviço do AGPM não iniciará se o controlador de domínio estiver offline</span><span class="sxs-lookup"><span data-stu-id="43aba-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="43aba-128">Quando o serviço do AGPM estiver instalado em um controlador de domínio nos sistemas operacionais Windows® 8 ou sistemas operacionais posteriores, o serviço não iniciará se o controlador de domínio estiver offline.</span><span class="sxs-lookup"><span data-stu-id="43aba-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="43aba-129">**Solução alternativa:** Inicie manualmente o serviço do AGPM após o controlador de domínio estar online.</span><span class="sxs-lookup"><span data-stu-id="43aba-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="43aba-130">A atualização do servidor do AGPM para o AGPM 4.0 SP2 é bloqueada quando você atualiza da versão do AGPM 4.0 mais Hotfix1</span><span class="sxs-lookup"><span data-stu-id="43aba-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="43aba-131">Se você tentar atualizar o servidor do AGPM para o AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="43aba-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="43aba-132">SP2 depois de instalar o AGPM 4,0 Server e instalar o hotfix do AGPM chamado AGPM 4,0 relata diferenças incorretas no relatório HTML (consulte o artigo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)da base de dados de conhecimento), a atualização falha e não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="43aba-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="43aba-133">**Solução alternativa:** Desinstale o servidor do AGPM 4,0 e instale o AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="43aba-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="43aba-134">Relatórios não exibem links de unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="43aba-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="43aba-135">Se você vincular um GPO não controlado a uma unidade organizacional e controlar esse GPO usando o AGPM, as configurações do AGPM e os relatórios de diferença não exibirão os links de unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="43aba-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="43aba-136">**Solução alternativa:** Na guia **controlado** do nó **alterar configurações** , clique com o botão direito do mouse no GPO, clique em **configurações**e, em seguida, clique em **links de GPO** para ver os links organizacionais.</span><span class="sxs-lookup"><span data-stu-id="43aba-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="43aba-137">Você também pode usar o GPMC para ver os links para um GPO na guia **escopo** .</span><span class="sxs-lookup"><span data-stu-id="43aba-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="43aba-138">O AGPM exibirá um erro se você clicar no botão retornar na caixa de diálogo Alterar, reparar ou remover cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="43aba-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="43aba-139">Se você navegar até **programas e recursos** no painel de controle e, em seguida, selecionar **gerenciamento avançado de política de grupo da Microsoft – cliente**, o AGPM exibirá um erro se você clicar em **Modificar** e, em seguida, clicar no botão **retornar** na caixa de diálogo **alterar, reparar ou remover cliente do AGPM** .</span><span class="sxs-lookup"><span data-stu-id="43aba-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="43aba-140">**Solução alternativa:** Clique em **Cancelar** para limpar o erro e inicie o processo novamente.</span><span class="sxs-lookup"><span data-stu-id="43aba-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="43aba-141">Não clique no botão **retornar** depois de clicar em **Modificar** .</span><span class="sxs-lookup"><span data-stu-id="43aba-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="43aba-142">O comentário não aparecerá na janela do histórico quando o aprovador implantar um GPO e inserir um comentário</span><span class="sxs-lookup"><span data-stu-id="43aba-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="43aba-143">Se um usuário com a função de editor enviar uma solicitação para implantar um GPO e o usuário que tiver a função de aprovador implantar o GPO e inserir um comentário, o comentário não aparecerá na janela do **histórico** .</span><span class="sxs-lookup"><span data-stu-id="43aba-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="43aba-144">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="43aba-144">**Workaround:** None.</span></span>

## <span data-ttu-id="43aba-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43aba-145">Related topics</span></span>


[<span data-ttu-id="43aba-146">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="43aba-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="43aba-147">Novidades do AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="43aba-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 





