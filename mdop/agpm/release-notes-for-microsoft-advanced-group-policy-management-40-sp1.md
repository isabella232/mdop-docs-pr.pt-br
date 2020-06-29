---
title: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft
description: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797344"
---
# <span data-ttu-id="a7a9f-103">Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7a9f-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="a7a9f-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="a7a9f-105">Leia estas notas de versão cuidadosamente antes de instalar o gerenciamento avançado de política de grupo (AGPM) 4,0 SP1 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="a7a9f-106">Estas notas da versão contêm informações que são necessárias para instalar com êxito o AGPM 4,0 SP1 e contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="a7a9f-107">Se houver uma diferença entre essas notas de versão e outra documentação do AGPM, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="a7a9f-108">Estas notas de versão substituem o conteúdo incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="a7a9f-109">Problemas conhecidos do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="a7a9f-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="a7a9f-110">Esta seção contém notas de versão do AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="a7a9f-111">A ferramenta "Desinstalar" do painel de controle pode não funcionar quando você tenta alterar as configurações do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="a7a9f-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="a7a9f-112">A ferramenta no painel de controle que permite desinstalar ou alterar um programa pode não funcionar quando você tenta alterar as configurações do servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="a7a9f-113">SOLUÇÃO alternativa: antes de tentar alterar as configurações do servidor do AGPM usando o painel de controle, faça uma cópia da pasta de arquivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="a7a9f-114">Em seguida, você pode usar Setup.exe para reinstalar o servidor do AGPM e escolher os parâmetros de configuração desejados.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="a7a9f-115">Os relatórios não exibem os links que foram adicionados a um objeto de política de grupo</span><span class="sxs-lookup"><span data-stu-id="a7a9f-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="a7a9f-116">As configurações do AGPM e os relatórios de diferença não exibem os links que foram adicionados a um objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="a7a9f-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="a7a9f-117">SOLUÇÃO alternativa: para exibir os links nos relatórios, selecione o GPO no console de gerenciamento de política de grupo (GPMC) e clique na guia **configurações** no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="a7a9f-118">Os relatórios não exibem todas as configurações de "Propriedades de opções de opção"</span><span class="sxs-lookup"><span data-stu-id="a7a9f-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="a7a9f-119">As configurações do AGPM e os relatórios de diferença não exibem todas as configurações selecionadas na janela Propriedades de opções de escolha no editor de objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="a7a9f-120">SOLUÇÃO alternativa: Use o GPMC para exibir as configurações de opções de opções de escolha selecionadas nos relatórios.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="a7a9f-121">Os relatórios não mostram as guias mostrar e ocultar em determinados navegadores</span><span class="sxs-lookup"><span data-stu-id="a7a9f-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="a7a9f-122">As guias mostrar e ocultar, mostradas no lado direito das configurações do AGPM e relatórios de diferença, não são exibidas quando você vê os relatórios no Google Chrome ou no Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="a7a9f-123">SOLUÇÃO alternativa: visualize os relatórios usando o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="a7a9f-124">As configurações do AGPM e os relatórios de diferença podem mostrar conteúdo diferente dos relatórios do GPMC</span><span class="sxs-lookup"><span data-stu-id="a7a9f-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="a7a9f-125">As configurações do AGPM e os relatórios de diferença podem não mostrar o mesmo conteúdo que os relatórios no GPMC (console de gerenciamento de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="a7a9f-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="a7a9f-126">SOLUÇÃO alternativa: Use o GPMC para ver os relatórios do AGPM.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="a7a9f-127">O serviço do AGPM não iniciará se o controlador de domínio não estiver online</span><span class="sxs-lookup"><span data-stu-id="a7a9f-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="a7a9f-128">Quando o serviço do AGPM estiver instalado em um controlador de domínio no Windows 8, o serviço não iniciará se o controlador de domínio não estiver online.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="a7a9f-129">SOLUÇÃO alternativa: Inicie manualmente o serviço do AGPM após o controlador de domínio estar online.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="a7a9f-130">A atualização do servidor do AGPM para o AGPM 4,0 SP1 é bloqueada quando você atualiza a partir da versão do AGPM 4,0 mais o hotfix</span><span class="sxs-lookup"><span data-stu-id="a7a9f-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="a7a9f-131">Se você tentar atualizar o servidor do AGPM para o AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="a7a9f-132">SP1 depois de instalar o AGPM 4,0 e, em seguida, instalar o hotfix do AGPM (consulte o artigo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)da base de dados de conhecimento), a atualização falha e não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="a7a9f-133">SOLUÇÃO alternativa: desinstale o servidor do AGPM 4,0 e instale o AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="a7a9f-134">Relatórios não exibem links de unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="a7a9f-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="a7a9f-135">Se você vincular um GPO não controlado a uma unidade organizacional e controlar esse GPO usando o AGPM, as configurações do AGPM e os relatórios de diferença não exibirão os links de unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="a7a9f-136">SOLUÇÃO alternativa: na guia **controlado** do nó **alterar configurações** , clique com o botão direito do mouse no GPO e clique em **configurações** e, em seguida, clique em **links de GPO** para ver os links organizacionais.</span><span class="sxs-lookup"><span data-stu-id="a7a9f-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="a7a9f-137">Você também pode usar o GPMC para ver os links para um GPO na guia **escopo** .</span><span class="sxs-lookup"><span data-stu-id="a7a9f-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="a7a9f-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7a9f-138">Related topics</span></span>


[<span data-ttu-id="a7a9f-139">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="a7a9f-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="a7a9f-140">Novidades do AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="a7a9f-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 





