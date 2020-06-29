---
title: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP3
description: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP3
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797342"
---
# <span data-ttu-id="d1bd5-103">Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="d1bd5-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>


<span data-ttu-id="d1bd5-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d1bd5-105">Leia estas notas de versão cuidadosamente antes de instalar o serviço de gerenciamento de política de grupo (AGPM) Pack3 (SP3) 4.0 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="d1bd5-106">Estas notas da versão contêm informações que são necessárias para instalar com êxito o AGPM 4.0 SP3 e contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-106">These release notes contain information that is required to successfully install AGPM4.0 SP3 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="d1bd5-107">Se houver uma diferença entre essas notas de versão e outra documentação do AGPM, considere as alterações mais recentes autorizadas.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="d1bd5-108">Estas notas de versão substituem o conteúdo incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="d1bd5-109">Problemas conhecidos do AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="d1bd5-109">AGPM4.0 SP3 known issues</span></span>


<span data-ttu-id="d1bd5-110">Esta seção descreve os problemas conhecidos do AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-110">This section describes the known issues for AGPM 4.0 SP3.</span></span>

### <span data-ttu-id="d1bd5-111">A instalação do AGPM falha no Windows 10</span><span class="sxs-lookup"><span data-stu-id="d1bd5-111">AGPM installation fails in Windows 10</span></span>

<span data-ttu-id="d1bd5-112">O AGPM habilita internamente o recurso Windows Communication Foundation (WCF)-ativação de não HTTP durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-112">AGPM internally enables the Windows Communication Foundation (WCF)-NonHTTP-Activation feature during installation.</span></span> <span data-ttu-id="d1bd5-113">No Windows 10, o WCF agora inclui um requisito para reiniciar o Windows após habilitar o recurso WCF NonHTTP-Activation.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-113">In Windows 10, WCF now includes a requirement to restart Windows after enabling the WCF NonHTTP-Activation feature.</span></span> <span data-ttu-id="d1bd5-114">No entanto, o código do programa de instalação do AGPM atual não manipula esse requisito de reinício e pára de responder enquanto aguarda o serviço ser ativado.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-114">However, the current AGPM installer code does not handle this restart requirement and stops responding while it waits for the service to be activated.</span></span>

<span data-ttu-id="d1bd5-115">**Solução alternativa:** Antes de executar o instalador do AGPM, habilite o recurso ativação do WCF non-HTTP e reinicie o Windows.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-115">**Workaround:** Before you run the AGPM installer, enable the WCF Non-HTTP Activation feature and then restart Windows.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="d1bd5-116">A ferramenta "Desinstalar" do painel de controle pode não funcionar quando você tenta alterar as configurações do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="d1bd5-116">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="d1bd5-117">A ferramenta no painel de controle que você usa para desinstalar ou alterar um programa pode não funcionar quando você tenta alterar as configurações do servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-117">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="d1bd5-118">**Solução alternativa:** Antes de tentar alterar as configurações do servidor de AGPM usando o painel de controle, faça uma cópia da pasta de arquivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-118">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="d1bd5-119">Em seguida, você pode usar Setup.exe para reinstalar o servidor do AGPM e escolher os parâmetros de configuração desejados.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-119">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="d1bd5-120">Os relatórios não exibem os links que foram adicionados a um objeto de política de grupo</span><span class="sxs-lookup"><span data-stu-id="d1bd5-120">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="d1bd5-121">As configurações do AGPM e os relatórios de diferença não exibem os links que foram adicionados a um objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="d1bd5-121">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="d1bd5-122">**Solução alternativa:** Para exibir os links nos relatórios, selecione o GPO no console de gerenciamento de política de grupo (GPMC) e, em seguida, clique na guia **configurações** no painel direito.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-122">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="d1bd5-123">Relatórios não exibe todas as opções configurações de propriedades de opção</span><span class="sxs-lookup"><span data-stu-id="d1bd5-123">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="d1bd5-124">As configurações do AGPM e os relatórios de diferença não exibem todas as configurações selecionadas na janela **Propriedades de opções de escolha** no editor de objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-124">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="d1bd5-125">**Solução alternativa:** Use o GPMC para exibir as configurações de **Opções de opções de escolha** selecionadas nos relatórios.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-125">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="d1bd5-126">Os relatórios podem não exibir as guias mostrar e ocultar em determinados navegadores</span><span class="sxs-lookup"><span data-stu-id="d1bd5-126">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="d1bd5-127">As guias **Mostrar** e **ocultar** , no lado direito das configurações do AGPM e relatórios de diferença, podem não aparecer quando você vê os relatórios no Google Chrome ou no Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-127">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="d1bd5-128">**Solução alternativa:** Exiba os relatórios usando o navegador Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-128">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="d1bd5-129">As configurações do AGPM e os relatórios de diferença podem mostrar conteúdo diferente dos relatórios do GPMC</span><span class="sxs-lookup"><span data-stu-id="d1bd5-129">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="d1bd5-130">As configurações do AGPM e os relatórios de diferença podem não mostrar o mesmo conteúdo que os relatórios no GPMC.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-130">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="d1bd5-131">**Solução alternativa:** Use o GPMC para ver os relatórios do AGPM.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-131">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="d1bd5-132">O serviço do AGPM não iniciará se o controlador de domínio estiver offline</span><span class="sxs-lookup"><span data-stu-id="d1bd5-132">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="d1bd5-133">Quando o serviço do AGPM estiver instalado em um controlador de domínio nos sistemas operacionais Windows® 8 ou sistemas operacionais posteriores, o serviço não iniciará se o controlador de domínio estiver offline.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-133">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="d1bd5-134">**Solução alternativa:** Inicie manualmente o serviço do AGPM após o controlador de domínio estar online.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-134">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="d1bd5-135">A atualização do servidor do AGPM para o AGPM 4.0 SP2 é bloqueada quando você atualiza da versão do AGPM 4.0 mais Hotfix1</span><span class="sxs-lookup"><span data-stu-id="d1bd5-135">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="d1bd5-136">Se você tentar atualizar o servidor do AGPM para o AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-136">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="d1bd5-137">SP2 depois de instalar o AGPM 4,0 Server e instalar o hotfix do AGPM chamado AGPM 4,0 relata diferenças incorretas no relatório HTML (consulte o artigo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)da base de dados de conhecimento), a atualização falha e não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-137">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="d1bd5-138">**Solução alternativa:** Desinstale o servidor do AGPM 4,0 e instale o AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-138">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="d1bd5-139">Relatórios não exibem links de unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="d1bd5-139">Reports do not display organizational unit links</span></span>

<span data-ttu-id="d1bd5-140">Se você vincular um GPO não controlado a uma unidade organizacional e controlar esse GPO usando o AGPM, as configurações do AGPM e os relatórios de diferença não exibirão os links de unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-140">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="d1bd5-141">**Solução alternativa:** Na guia **controlado** do nó **alterar configurações** , clique com o botão direito do mouse no GPO, clique em **configurações**e, em seguida, clique em **links de GPO** para ver os links organizacionais.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-141">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="d1bd5-142">Você também pode usar o GPMC para ver os links para um GPO na guia **escopo** .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-142">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="d1bd5-143">O AGPM exibirá um erro se você clicar no botão retornar na caixa de diálogo Alterar, reparar ou remover cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="d1bd5-143">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="d1bd5-144">Se você navegar até **programas e recursos** no painel de controle e, em seguida, selecionar **gerenciamento avançado de política de grupo da Microsoft – cliente**, o AGPM exibirá um erro se você clicar em **Modificar** e, em seguida, clicar no botão **retornar** na caixa de diálogo **alterar, reparar ou remover cliente do AGPM** .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-144">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="d1bd5-145">**Solução alternativa:** Clique em **Cancelar** para limpar o erro e inicie o processo novamente.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-145">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="d1bd5-146">Não clique no botão **retornar** depois de clicar em **Modificar** .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-146">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="d1bd5-147">O comentário não aparecerá na janela do histórico quando o aprovador implantar um GPO e inserir um comentário</span><span class="sxs-lookup"><span data-stu-id="d1bd5-147">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="d1bd5-148">Se um usuário com a função de editor enviar uma solicitação para implantar um GPO e o usuário que tiver a função de aprovador implantar o GPO e inserir um comentário, o comentário não aparecerá na janela do **histórico** .</span><span class="sxs-lookup"><span data-stu-id="d1bd5-148">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="d1bd5-149">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-149">**Workaround:** None.</span></span>

### <span data-ttu-id="d1bd5-150">Mecanismo adicionado para substituir o comportamento padrão do AGPM de remover alterações de permissão do GPO</span><span class="sxs-lookup"><span data-stu-id="d1bd5-150">Added mechanism to override AGPM default behavior of removing GPO permission changes</span></span>

<span data-ttu-id="d1bd5-151">A partir de HF02, o AGPM adicionou uma chave do registro para habilitar a substituição do comportamento padrão de permissão do GPO do AGPM.</span><span class="sxs-lookup"><span data-stu-id="d1bd5-151">As of HF02, AGPM has added a registry key to enable overriding the default AGPM GPO permission behavior.</span></span> <span data-ttu-id="d1bd5-152">Para obter mais informações, confira [as alterações nas permissões do objeto de política de grupo por meio do AGPM são ignoradas](https://support.microsoft.com/kb/3174540)</span><span class="sxs-lookup"><span data-stu-id="d1bd5-152">For more information, please see [Changes to Group Policy object permissions through AGPM are ignored](https://support.microsoft.com/kb/3174540)</span></span>

## <span data-ttu-id="d1bd5-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1bd5-153">Related topics</span></span>


[<span data-ttu-id="d1bd5-154">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="d1bd5-154">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="d1bd5-155">Novidades do AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="d1bd5-155">What's New in AGPM 4.0 SP3</span></span>](whats-new-in-agpm-40-sp3.md)

 

 





