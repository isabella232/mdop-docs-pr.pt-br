---
title: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
description: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797677"
---
# <span data-ttu-id="05fd2-103">Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="05fd2-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="05fd2-104">Este guia passo a passo demonstra técnicas avançadas para o gerenciamento de política de grupo que usam o console de gerenciamento de política de grupo (GPMC) e o gerenciamento avançado de política de grupo (AGPM) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="05fd2-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="05fd2-105">O AGPM aumenta a funcionalidade do GPMC, fornecendo:</span><span class="sxs-lookup"><span data-stu-id="05fd2-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="05fd2-106">Funções padrão para delegar permissões para gerenciar GPOs (objetos de política de grupo) para vários administradores de política de grupo, além da capacidade de delegar o acesso a GPOs no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="05fd2-107">Um arquivo morto para permitir que os administradores de política de grupo criem e modifiquem os GPOs offline antes de os GPOs serem implantados em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="05fd2-108">A capacidade de reverter para qualquer versão anterior de um GPO no arquivo morto e limitar o número de versões armazenadas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="05fd2-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="05fd2-109">Recurso de check-in e check-out de GPOs para garantir que os administradores de política de grupo não substituam acidentalmente uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="05fd2-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="05fd2-110">A capacidade de Pesquisar GPOs com atributos específicos e filtrar a lista de GPOs exibida.</span><span class="sxs-lookup"><span data-stu-id="05fd2-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="05fd2-111">Visão geral do cenário do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-111">AGPM scenario overview</span></span>


<span data-ttu-id="05fd2-112">Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a política de grupo pode ser gerenciada em um ambiente com vários administradores de política de grupo com diferentes níveis de permissões.</span><span class="sxs-lookup"><span data-stu-id="05fd2-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="05fd2-113">Especificamente, você vai executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="05fd2-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="05fd2-114">Usando uma conta que seja membro do grupo Domain admins, instale o servidor do AGPM e atribua a função de administrador do AGPM a uma conta ou grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="05fd2-115">Usando contas às quais você atribuirá funções do AGPM, instale o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="05fd2-116">Usar uma conta que tenha a função de administrador do AGPM, configurar o AGPM e o acesso de representante a GPOs atribuindo funções a outras contas.</span><span class="sxs-lookup"><span data-stu-id="05fd2-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="05fd2-117">Em uma conta que tem a função editor, solicite que um novo GPO seja criado e, em seguida, você aprove usando uma conta que tenha a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="05fd2-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="05fd2-118">Use a conta editor para fazer check-out do GPO, edite o GPO, verifique o GPO no arquivo e, em seguida, solicite implantação.</span><span class="sxs-lookup"><span data-stu-id="05fd2-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="05fd2-119">Usando uma conta que tenha a função Aprovador, examine o GPO e implante-o em seu ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="05fd2-120">Usando uma conta que tenha a função editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="05fd2-121">Usar uma conta que tenha a função de aprovador, excluir e restaurar um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![processo de desenvolvimento de objetos de política de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="05fd2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05fd2-123">Requirements</span></span>


<span data-ttu-id="05fd2-124">Os computadores em que você deseja instalar o AGPM devem atender aos seguintes requisitos, e você deve criar contas para uso nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="05fd2-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="05fd2-125">**Observação**  Se você tiver o AGPM 2,5 instalado e estiver atualizando do Windows Server® 2003 para o Windows Server2008R2 ou Windows Server2008 ou estiver atualizando do WindowsVista sem nenhum Service Pack instalado para o Windows7 ou o WindowsVista® com Service Pack1 (SP1), você deve atualizar o sistema operacional antes de poder atualizar para o AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="05fd2-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="05fd2-126">Se você tiver o AGPM 3,0 instalado, não será necessário atualizar o sistema operacional antes de atualizar para o AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="05fd2-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="05fd2-127">Em um ambiente misto que inclui sistemas operacionais mais recentes e mais antigos, há algumas limitações à funcionalidade, conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="05fd2-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05fd2-128">Sistema operacional no qual o servidor do AGPM 4,0 é executado</span><span class="sxs-lookup"><span data-stu-id="05fd2-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="05fd2-129">Sistema operacional no qual o cliente do AGPM 4,0 é executado</span><span class="sxs-lookup"><span data-stu-id="05fd2-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="05fd2-130">Status do suporte do AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="05fd2-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05fd2-131">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-132">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="05fd2-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05fd2-134">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-135">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="05fd2-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-136">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05fd2-137">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="05fd2-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-138">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-139">Sem Suporte</span><span class="sxs-lookup"><span data-stu-id="05fd2-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05fd2-140">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="05fd2-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-141">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="05fd2-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="05fd2-142">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="05fd2-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="05fd2-143">Requisitos do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-143">AGPM Server requirements</span></span>

<span data-ttu-id="05fd2-144">O AGPM Server 4.0 requer o Windows Server2008R2, o Windows Server2008, o Windows Vista e o GPMC do RSAT (Remote Server Administration Tools) ou o Windows Vista com SP1 e o GPMC do RSAT instalados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="05fd2-145">Há suporte para as duas versões de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05fd2-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="05fd2-146">Antes de instalar o servidor do AGPM, você deve ser membro do grupo Domain admins e os seguintes recursos do Windows devem estar presentes, a menos que indicado de outra forma:</span><span class="sxs-lookup"><span data-stu-id="05fd2-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="05fd2-147">GPMC</span><span class="sxs-lookup"><span data-stu-id="05fd2-147">GPMC</span></span>

    -   <span data-ttu-id="05fd2-148">Windows Server2008R2 ou Windows Server2008: se o GPMC não estiver presente, ele será instalado automaticamente pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="05fd2-149">Windows7: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="05fd2-150">Para obter mais informações, consulte [ferramentas de administração de servidor remoto para Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="05fd2-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="05fd2-151">Windows Vista com SP1: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="05fd2-152">Para obter mais informações, consulte [ferramentas de administração de servidor remoto para Windows Vista com Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="05fd2-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="05fd2-153">O .NET Framework 3,5 ou versões posteriores</span><span class="sxs-lookup"><span data-stu-id="05fd2-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="05fd2-154">Windows Server2008R2 ou Windows7: se o .NET Framework 3,5 ou versão posterior não estiver presente, o .NET Framework 3,5 será automaticamente instalado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="05fd2-155">Windows Server2008 ou Windows Vista com SP1: você deve instalar o .NET Framework 3,5 ou uma versão posterior antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="05fd2-156">Os seguintes recursos do Windows são exigidos pelo servidor do AGPM e serão instalados automaticamente se não estiverem presentes:</span><span class="sxs-lookup"><span data-stu-id="05fd2-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="05fd2-157">Ativação do WCF; Ativação não HTTP</span><span class="sxs-lookup"><span data-stu-id="05fd2-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="05fd2-158">Serviço de Ativação de Processos do Windows</span><span class="sxs-lookup"><span data-stu-id="05fd2-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="05fd2-159">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="05fd2-159">Process Model</span></span>

    -   <span data-ttu-id="05fd2-160">O ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="05fd2-160">The .NET Environment</span></span>

    -   <span data-ttu-id="05fd2-161">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="05fd2-161">Configuration APIs</span></span>

### <span data-ttu-id="05fd2-162">Requisitos do cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-162">AGPM Client requirements</span></span>

<span data-ttu-id="05fd2-163">O cliente do AGPM 4.0 requer o Windows Server2008R2, o Windows Server2008, o Windows7 e o GPMC do RSAT ou o Windows Vista com SP1 e o GPMC do RSAT instalados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="05fd2-164">Há suporte para as duas versões de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="05fd2-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="05fd2-165">O cliente do AGPM pode ser instalado em um computador que esteja executando o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="05fd2-166">Os seguintes recursos do Windows são necessários para o cliente do AGPM e, a menos que indicado de outra forma, será automaticamente instalado se não estiverem presentes:</span><span class="sxs-lookup"><span data-stu-id="05fd2-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="05fd2-167">GPMC</span><span class="sxs-lookup"><span data-stu-id="05fd2-167">GPMC</span></span>

    -   <span data-ttu-id="05fd2-168">Windows Server2008R2 ou Windows Server2008: se o GPMC não estiver presente, ele será instalado automaticamente pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="05fd2-169">Windows7: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="05fd2-170">Para obter mais informações, consulte [ferramentas de administração de servidor remoto para Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="05fd2-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="05fd2-171">Windows Vista com SP1: você deve instalar o GPMC a partir do RSAT antes de instalar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="05fd2-172">Para obter mais informações, consulte [ferramentas de administração de servidor remoto para Windows Vista com Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="05fd2-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="05fd2-173">O .NET Framework 3,0 ou versão posterior</span><span class="sxs-lookup"><span data-stu-id="05fd2-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="05fd2-174">Windows Server2008R2 ou Windows7: se o .NET Framework 3,0 ou versão posterior não estiver presente, o .NET Framework 3,5 será automaticamente instalado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="05fd2-175">Windows Server2008 ou Windows Vista com SP1: se o .NET Framework 3,0 ou versão posterior não estiver presente, o .NET Framework 3,0 será automaticamente instalado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="05fd2-176">Requisitos do cenário</span><span class="sxs-lookup"><span data-stu-id="05fd2-176">Scenario requirements</span></span>

<span data-ttu-id="05fd2-177">Antes de iniciar esse cenário, crie quatro contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="05fd2-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="05fd2-178">Durante o cenário, você atribuirá uma das seguintes funções do AGPM a cada uma dessas contas: administrador do AGPM (controle total), Aprovador, editor e revisor.</span><span class="sxs-lookup"><span data-stu-id="05fd2-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="05fd2-179">Essas contas devem ser capazes de enviar e receber mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="05fd2-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="05fd2-180">Atribua a permissão de **vincular GPOs** às contas que têm as funções de editor do administrador do AGPM, Aprovador e (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="05fd2-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="05fd2-181">**Observação** 
 A permissão **vincular GPOs** é atribuída a membros de administradores de domínio e administradores corporativos por padrão.</span><span class="sxs-lookup"><span data-stu-id="05fd2-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="05fd2-182">Para atribuir a permissão de **vincular GPOs** a usuários ou grupos adicionais (como contas que têm as funções de administrador do AGPM ou aprovador), clique no nó do domínio e clique na guia **delegação** , selecione **vincular GPOs**, clique em **Adicionar**e selecione os usuários ou grupos aos quais você deseja atribuir a permissão.</span><span class="sxs-lookup"><span data-stu-id="05fd2-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="05fd2-183">Etapas para instalar e configurar o AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="05fd2-184">Você deve completar as etapas a seguir para instalar e configurar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="05fd2-185">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="05fd2-186">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="05fd2-187">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="05fd2-188">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="05fd2-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="05fd2-189">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="05fd2-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="05fd2-190">Etapa 1: instalar o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="05fd2-191">Nesta etapa, você instala o servidor do AGPM no servidor membro ou controlador de domínio que executará o serviço do AGPM e você poderá configurar o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="05fd2-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="05fd2-192">Todas as operações do AGPM são gerenciadas por meio desse serviço do Windows e são executadas com as credenciais do serviço.</span><span class="sxs-lookup"><span data-stu-id="05fd2-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="05fd2-193">O arquivo gerenciado por um servidor do AGPM pode ser hospedado nesse servidor ou em outro servidor na mesma floresta.</span><span class="sxs-lookup"><span data-stu-id="05fd2-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="05fd2-194">Para instalar o servidor do AGPM no computador que irá hospedar o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="05fd2-195">Faça logon com uma conta que seja membro do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="05fd2-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="05fd2-196">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **Advanced Group Policy Management-Server**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="05fd2-197">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="05fd2-198">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="05fd2-199">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="05fd2-200">O computador no qual o servidor do AGPM está instalado hospedará o serviço do AGPM e gerenciará o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="05fd2-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="05fd2-201">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-201">Click **Next**.</span></span>

6.  <span data-ttu-id="05fd2-202">Na caixa de diálogo **caminho do arquivo morto** , selecione um local para o arquivo morto em relação ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="05fd2-203">O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="05fd2-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="05fd2-204">No entanto, você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="05fd2-205">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-205">Click **Next**.</span></span>

7.  <span data-ttu-id="05fd2-206">Na caixa de diálogo **conta de serviço do AGPM** , selecione uma conta de serviço na qual o serviço do AGPM será executado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="05fd2-207">Essa conta deve ser membro do grupo Domain admins ou, para uma configuração de menos privilégios, os seguintes grupos em cada domínio gerenciados pelo servidor do AGPM:</span><span class="sxs-lookup"><span data-stu-id="05fd2-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="05fd2-208">Proprietários criadores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="05fd2-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="05fd2-209">Operadores de backup</span><span class="sxs-lookup"><span data-stu-id="05fd2-209">Backup Operators</span></span>

    <span data-ttu-id="05fd2-210">Além disso, essa conta exige permissão de controle total para as seguintes pastas:</span><span class="sxs-lookup"><span data-stu-id="05fd2-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="05fd2-211">A pasta de arquivo de AGPM, para a qual essa permissão é concedida automaticamente durante a instalação do servidor do AGPM se ela estiver instalada em uma unidade local.</span><span class="sxs-lookup"><span data-stu-id="05fd2-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="05fd2-212">A pasta temporária do sistema local, geralmente%WINDIR%\\temp.</span><span class="sxs-lookup"><span data-stu-id="05fd2-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="05fd2-213">Na caixa de diálogo **proprietário do arquivo** , selecione uma conta ou grupo à qual você atribui a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="05fd2-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="05fd2-214">Os administradores do AGPM podem atribuir funções do AGPM e permissões a outros administradores de política de grupo para que, posteriormente, você possa atribuir a função de administrador do AGPM a administradores adicionais de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="05fd2-215">Para esse cenário, selecione a conta a ser usada na função de administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="05fd2-216">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-216">Click **Next**.</span></span>

9.  <span data-ttu-id="05fd2-217">Na caixa de diálogo **configuração de portabilidade** , digite uma porta na qual o serviço do AGPM deve escutar.</span><span class="sxs-lookup"><span data-stu-id="05fd2-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="05fd2-218">Não desmarque a caixa de seleção **Adicionar exceção de porta ao firewall** , a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta.</span><span class="sxs-lookup"><span data-stu-id="05fd2-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="05fd2-219">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-219">Click **Next**.</span></span>

10. <span data-ttu-id="05fd2-220">Na caixa de diálogo **idiomas** , selecione um ou mais idiomas de exibição para instalar no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="05fd2-221">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="05fd2-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="05fd2-222">**Cuidado**  Não altere as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="05fd2-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="05fd2-223">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="05fd2-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="05fd2-224">Para obter informações sobre como alterar as configurações do serviço, consulte a ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="05fd2-225">Etapa 2: instalar o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="05fd2-226">Cada administrador da política de grupo — qualquer pessoa que cria, edita, implanta, revisa ou exclui GPOs — deve ter o cliente do AGPM instalado em computadores que eles usam para gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="05fd2-227">O nó de controle de alterações, que você usa para executar muitas das tarefas de gerenciamento de GPO, aparecerá no console de gerenciamento de política de grupo somente se você instalar o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="05fd2-228">Para esse cenário, instale o cliente do AGPM em pelo menos um computador.</span><span class="sxs-lookup"><span data-stu-id="05fd2-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="05fd2-229">Você não precisa instalar o cliente do AGPM nos computadores dos usuários finais que não executam a administração da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="05fd2-230">Para instalar o cliente do AGPM no computador de um administrador de política de grupo</span><span class="sxs-lookup"><span data-stu-id="05fd2-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="05fd2-231">Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **gerenciamento avançado de política de grupo-cliente**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="05fd2-232">Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="05fd2-233">Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="05fd2-234">Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="05fd2-235">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-235">Click **Next**.</span></span>

5.  <span data-ttu-id="05fd2-236">Na caixa de diálogo **servidor de AGPM** , digite o nome DNS ou o endereço IP do servidor do AGPM e a porta à qual você deseja se conectar.</span><span class="sxs-lookup"><span data-stu-id="05fd2-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="05fd2-237">A porta padrão do serviço do AGPM é 4600.</span><span class="sxs-lookup"><span data-stu-id="05fd2-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="05fd2-238">Não desmarque a caixa de seleção **permitir o console de gerenciamento da Microsoft por meio do firewall** , a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta.</span><span class="sxs-lookup"><span data-stu-id="05fd2-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="05fd2-239">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-239">Click **Next**.</span></span>

6.  <span data-ttu-id="05fd2-240">Na caixa de diálogo **idiomas** , selecione um ou mais idiomas de exibição para instalar para o cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="05fd2-241">Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="05fd2-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="05fd2-242">Etapa 3: configurar uma conexão com o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="05fd2-243">O AGPM armazena todas as versões de cada objeto de política de grupo (GPO) controlado, ou seja, cada GPO para o qual o AGPM fornece controle de alterações, em um arquivo morto central.</span><span class="sxs-lookup"><span data-stu-id="05fd2-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="05fd2-244">Isso permite que os administradores de política de grupo exibam e alterem os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="05fd2-245">Nesta etapa, você configura uma conexão do servidor do AGPM e garante que todos os administradores de política de grupo se conectam ao mesmo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="05fd2-246">(Para obter informações sobre como configurar vários servidores do AGPM, consulte a ajuda para gerenciamento avançado de política de grupo.)</span><span class="sxs-lookup"><span data-stu-id="05fd2-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="05fd2-247">Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo</span><span class="sxs-lookup"><span data-stu-id="05fd2-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="05fd2-248">Em um computador no qual você instalou o cliente do AGPM, faça logon com a conta de usuário selecionada como o proprietário do arquivo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="05fd2-249">Esse usuário tem a função de administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="05fd2-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="05fd2-250">Clique em **Iniciar**, aponte para **Ferramentas administrativas**e clique em **Gerenciamento de política de grupo** para abrir o GPMC.</span><span class="sxs-lookup"><span data-stu-id="05fd2-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="05fd2-251">Editar um GPO aplicado a todos os administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="05fd2-252">Na janela **Editor de gerenciamento de política de grupo** , clique duas vezes em **configuração do usuário**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="05fd2-253">No painel detalhes, clique duas vezes em **AGPM: especifique o servidor do AGPM padrão (todos os domínios)**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="05fd2-254">Na janela **Propriedades** , selecione **habilitado** e digite o nome DNS ou o endereço IP e a portabilidade (por exemplo, **Server.contoso.com:4600**) para o servidor que hospeda o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="05fd2-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="05fd2-255">Por padrão, o serviço do AGPM usa a porta 4600.</span><span class="sxs-lookup"><span data-stu-id="05fd2-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="05fd2-256">Clique em **OK**e feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="05fd2-257">Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="05fd2-258">Etapa 4: configurar a notificação por email</span><span class="sxs-lookup"><span data-stu-id="05fd2-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="05fd2-259">Como administrador do AGPM (controle total), você designa os endereços de email de aprovadores e administradores do AGPM para quem uma mensagem de email contendo uma solicitação é enviada quando um editor tenta criar, implantar ou excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="05fd2-260">Você também pode determinar o alias do qual essas mensagens são enviadas.</span><span class="sxs-lookup"><span data-stu-id="05fd2-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="05fd2-261">Para configurar a notificação por email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="05fd2-262">No **Editor de gerenciamento de política de grupo** , navegue até a pasta **alterar controle**</span><span class="sxs-lookup"><span data-stu-id="05fd2-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="05fd2-263">No painel de detalhes, clique na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="05fd2-264">No campo **do endereço de email** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="05fd2-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="05fd2-265">No campo **endereço de email para** , digite o endereço de email da conta de usuário à qual você pretende atribuir a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="05fd2-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="05fd2-266">No campo **servidor SMTP** , digite um servidor de email SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="05fd2-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="05fd2-267">Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário que tenha acesso ao serviço SMTP.</span><span class="sxs-lookup"><span data-stu-id="05fd2-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="05fd2-268">Clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="05fd2-269">Etapa 5: delegar acesso</span><span class="sxs-lookup"><span data-stu-id="05fd2-269">Step 5: Delegate access</span></span>

<span data-ttu-id="05fd2-270">Como administrador do AGPM (controle total), você delega o acesso no nível do domínio aos GPOs, atribuindo funções à conta de cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="05fd2-271">**Observação**  Você também pode delegar o acesso no nível do GPO em vez do nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="05fd2-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="05fd2-272">Para obter mais informações, consulte ajuda para gerenciamento avançado de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="05fd2-273">**Importante**  Você deve restringir a participação no grupo proprietários criadores de política de grupo para que ela não possa ser usada para burlar o gerenciamento de AGPM do acesso a GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="05fd2-274">(No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)</span><span class="sxs-lookup"><span data-stu-id="05fd2-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="05fd2-275">Para delegar o acesso a todos os GPOs em um domínio</span><span class="sxs-lookup"><span data-stu-id="05fd2-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="05fd2-276">Na guia **delegação de domínio** , clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como Aprovador e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="05fd2-277">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função **Aprovador** para atribuir a função à conta e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="05fd2-278">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="05fd2-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="05fd2-279">Clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como editor e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="05fd2-280">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função de **Editor** para atribuir a função à conta e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="05fd2-281">(Essa função inclui a função de revisor.)</span><span class="sxs-lookup"><span data-stu-id="05fd2-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="05fd2-282">Clique no botão **Adicionar** , selecione a conta de usuário do administrador de política de grupo para atuar como revisor e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="05fd2-283">Na caixa de diálogo **Adicionar grupo ou usuário** , selecione a função **revisor** para atribuir apenas essa função à conta.</span><span class="sxs-lookup"><span data-stu-id="05fd2-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="05fd2-284">Etapas para gerenciar GPOs</span><span class="sxs-lookup"><span data-stu-id="05fd2-284">Steps for managing GPOs</span></span>


<span data-ttu-id="05fd2-285">Você deve completar as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="05fd2-286">Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.</span><span class="sxs-lookup"><span data-stu-id="05fd2-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="05fd2-287">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="05fd2-288">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="05fd2-289">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="05fd2-290">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="05fd2-291">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="05fd2-292">Etapa 1: criar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="05fd2-293">Em um ambiente com vários administradores de política de grupo, aqueles com a função editor podem solicitar que novos GPOs sejam criados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="05fd2-294">No entanto, essa solicitação deve ser aprovada por alguém com a função de aprovador.</span><span class="sxs-lookup"><span data-stu-id="05fd2-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="05fd2-295">Nesta etapa, você usa uma conta que tem a função de editor para solicitar que um novo GPO seja criado.</span><span class="sxs-lookup"><span data-stu-id="05fd2-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="05fd2-296">Usando uma conta que tenha a função Aprovador, você aprova essa solicitação para criar o GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="05fd2-297">Para solicitar que um novo GPO seja criado e gerenciado pelo AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="05fd2-298">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário à qual a função de editor foi atribuída no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="05fd2-299">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="05fd2-300">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="05fd2-301">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="05fd2-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="05fd2-302">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="05fd2-303">Digite **MyGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="05fd2-304">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="05fd2-305">Clique em **criar ao vivo** de modo que o novo GPO seja implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="05fd2-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="05fd2-306">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="05fd2-307">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-308">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="05fd2-309">Para aprovar a solicitação pendente para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="05fd2-310">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha a função de aprovador no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="05fd2-311">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com a solicitação do editor para criar um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="05fd2-312">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="05fd2-313">Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.</span><span class="sxs-lookup"><span data-stu-id="05fd2-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="05fd2-314">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="05fd2-315">Clique em **Sim** para confirmar a aprovação e mover o GPO para a guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="05fd2-316">Etapa 2: editar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="05fd2-317">Você pode usar GPOs para configurar o computador ou o usuário e implantá-los em muitos computadores ou usuários.</span><span class="sxs-lookup"><span data-stu-id="05fd2-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="05fd2-318">Nesta etapa, você usa uma conta que tem a função de editor para fazer check-out de um GPO do arquivo, editar o GPO offline, verificar o GPO editado no arquivo e solicitar a implantação do GPO ao ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="05fd2-319">Nesse cenário, você define uma configuração no GPO para exigir que a senha tenha pelo menos oito caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="05fd2-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="05fd2-320">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="05fd2-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="05fd2-321">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha a função de editor no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="05fd2-322">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="05fd2-323">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="05fd2-324">Clique com o botão direito do mouse em **MyGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="05fd2-325">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="05fd2-326">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-327">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="05fd2-328">Para editar o GPO offline e configurar o tamanho mínimo da senha</span><span class="sxs-lookup"><span data-stu-id="05fd2-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="05fd2-329">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de gerenciamento de política de grupo** e alterar uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="05fd2-330">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="05fd2-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="05fd2-331">Em **configuração do computador**, clique duas vezes em **políticas**, **configurações do Windows**, configurações de **segurança**, **políticas de conta**e **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="05fd2-332">No painel de detalhes, clique duas vezes em **tamanho mínimo da senha**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="05fd2-333">Na janela Propriedades, marque a caixa de seleção **definir esta configuração de política** , defina o número de caracteres para **8**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="05fd2-334">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="05fd2-335">Para verificar o GPO no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="05fd2-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="05fd2-336">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **check-in**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="05fd2-337">Digite um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="05fd2-338">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-339">Na guia **controlado** , o estado do GPO é identificado como **checked-in**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="05fd2-340">Para solicitar a implantação do GPO ao ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="05fd2-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="05fd2-341">Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **implantar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="05fd2-342">Como essa conta não é um Aprovador ou administrador do AGPM, você deve enviar uma solicitação de implantação.</span><span class="sxs-lookup"><span data-stu-id="05fd2-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="05fd2-343">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="05fd2-344">Digite um comentário a ser exibido no histórico do GPO e, em seguida, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="05fd2-345">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-346">**MyGPO** é exibido na lista de GPOs na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="05fd2-347">Etapa 3: revisar e implantar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="05fd2-348">Nesta etapa, você atua como Aprovador, criando relatórios e analisando as configurações e alterando as configurações no GPO para determinar se devem ser aprovadas.</span><span class="sxs-lookup"><span data-stu-id="05fd2-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="05fd2-349">Depois de avaliar o GPO, implante-o no ambiente de produção e vincule o GPO a um domínio ou a uma unidade organizacional (OU).</span><span class="sxs-lookup"><span data-stu-id="05fd2-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="05fd2-350">O GPO entra em vigor quando a política de grupo é atualizada para computadores nesse domínio ou unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="05fd2-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="05fd2-351">Para revisar as configurações no GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="05fd2-352">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário à qual a função de aprovador está atribuída no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="05fd2-353">Qualquer administrador da política de grupo com a função revisor, que está incluída em todas as outras funções, pode revisar as configurações em um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="05fd2-354">Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com uma solicitação de editor para implantar um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="05fd2-355">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="05fd2-356">Na guia **conteúdo** do painel detalhes, clique na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="05fd2-357">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="05fd2-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="05fd2-358">Examine as configurações na versão mais recente do MyGPO:</span><span class="sxs-lookup"><span data-stu-id="05fd2-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="05fd2-359">Na janela do **histórico** , clique com o botão direito do mouse na versão do GPO com o carimbo de data/hora mais recente, clique em **configurações**e, em seguida, clique em **relatório HTML** para exibir um resumo das configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="05fd2-360">No navegador da Web, clique em **Mostrar tudo** para exibir todas as configurações no GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="05fd2-361">Feche a janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="05fd2-361">Close the browser.</span></span>

7. <span data-ttu-id="05fd2-362">Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:</span><span class="sxs-lookup"><span data-stu-id="05fd2-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="05fd2-363">Na janela do **histórico** , clique na versão do GPO com o carimbo de data/hora mais recente.</span><span class="sxs-lookup"><span data-stu-id="05fd2-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="05fd2-364">Pressione CTRL e clique na versão do GPO mais antiga para a qual a **versão do computador** não é \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="05fd2-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="05fd2-365">Clique no botão **diferenças** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-365">Click the **Differences** button.</span></span> <span data-ttu-id="05fd2-366">A seção **políticas de conta/política de senha** é realçada em verde e precedida por **\ [+ \]**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="05fd2-367">Isso indica que a configuração é configurada somente na última versão do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="05fd2-368">Clique em **políticas de conta/política de senha**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="05fd2-369">A configuração **comprimento mínimo da senha** também é realçada em verde e precedida por **\ [+ \]**, indicando que ela está configurada somente na última versão do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="05fd2-370">Fechar o navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="05fd2-370">Close the Web browser.</span></span>

**<span data-ttu-id="05fd2-371">Para implantar o GPO no ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="05fd2-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="05fd2-372">Na guia **pendente** , clique com o botão direito do mouse em **MyGPO** e, em seguida, clique em **aprovar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="05fd2-373">Digite um comentário para incluir no histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="05fd2-374">Clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-374">Click **Yes**.</span></span> <span data-ttu-id="05fd2-375">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-376">O GPO é implantado no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="05fd2-377">Para vincular o GPO a um domínio ou unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="05fd2-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="05fd2-378">No GPMC, clique com o botão direito do mouse no domínio ou em uma UO (unidade organizacional) à qual você deseja aplicar o GPO que você configurou e clique em **vincular um GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="05fd2-379">Na caixa de diálogo **selecionar GPO** , clique em **MyGPO**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="05fd2-380">Etapa 4: usar um modelo para criar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="05fd2-381">Nesta etapa, você usa uma conta que tem a função de editor para criar e usar um modelo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="05fd2-382">Esse modelo é uma versão estática de um GPO para uso como um ponto de partida para a criação de novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="05fd2-383">Embora não seja possível editar um modelo, você pode criar um novo GPO com base em um modelo.</span><span class="sxs-lookup"><span data-stu-id="05fd2-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="05fd2-384">Os modelos são úteis para criar rapidamente vários GPOs que incluam muitas das mesmas configurações de política.</span><span class="sxs-lookup"><span data-stu-id="05fd2-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="05fd2-385">Para criar um modelo com base em um GPO existente</span><span class="sxs-lookup"><span data-stu-id="05fd2-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="05fd2-386">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário à qual a função do editor seja atribuída no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="05fd2-387">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="05fd2-388">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="05fd2-389">Clique com o botão direito do mouse em **MyGPO**e clique em **salvar como modelo** para criar um modelo que incorpora todas as configurações no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="05fd2-390">Digite **MyTemplate** como o nome do modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="05fd2-391">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-392">O novo modelo aparece na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="05fd2-393">Para solicitar que um novo GPO seja criado e gerenciado pelo AGPM</span><span class="sxs-lookup"><span data-stu-id="05fd2-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="05fd2-394">Clique na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="05fd2-395">Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="05fd2-396">Na caixa de diálogo **novo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="05fd2-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="05fd2-397">Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="05fd2-398">Digite **MyOtherGPO** como o nome do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="05fd2-399">Digite um comentário para o novo GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="05fd2-400">Clique em **criar ao vivo** de modo que o novo GPO seja implantado para o ambiente de produção imediatamente após a aprovação.</span><span class="sxs-lookup"><span data-stu-id="05fd2-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="05fd2-401">Em **modelo de GPO**, selecione **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="05fd2-402">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="05fd2-403">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-404">O novo GPO será exibido na guia **pendente** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="05fd2-405">Use uma conta que é atribuída à função de aprovador para aprovar a solicitação pendente para criar o GPO da mesma forma que você fez na [etapa 1: criar um GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="05fd2-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="05fd2-406">MyTemplate incorpora todas as configurações que você configurou no MyGPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="05fd2-407">Como o MyOtherGPO foi criado usando MyTemplate, ele primeiro contém todas as configurações que MyGPO no momento em que MyTemplate foi criado.</span><span class="sxs-lookup"><span data-stu-id="05fd2-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="05fd2-408">Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO ao MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="05fd2-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="05fd2-409">Para fazer check-out do GPO do arquivo para edição</span><span class="sxs-lookup"><span data-stu-id="05fd2-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="05fd2-410">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário à qual a função do editor seja atribuída no AGPM.</span><span class="sxs-lookup"><span data-stu-id="05fd2-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="05fd2-411">Clique com o botão direito do mouse em **MyOtherGPO**e clique em **check-out**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="05fd2-412">Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="05fd2-413">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-414">Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="05fd2-415">Para editar o GPO offline e configurar a duração do bloqueio de conta</span><span class="sxs-lookup"><span data-stu-id="05fd2-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="05fd2-416">Na guia **controlado** , clique com o botão direito do mouse em **MyOtherGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de gerenciamento de política de grupo** e alterar uma cópia offline do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="05fd2-417">Para esse cenário, configure o tamanho mínimo da senha:</span><span class="sxs-lookup"><span data-stu-id="05fd2-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="05fd2-418">Em **configuração do computador**, clique duas vezes em **políticas**, **configurações do Windows**, **configurações de segurança**, políticas de **conta**e política de **bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="05fd2-419">No painel de detalhes, clique duas vezes em **duração do bloqueio de conta**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="05fd2-420">Na janela Propriedades, marque **definir esta configuração de política**, defina a duração como **30** minutos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="05fd2-421">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="05fd2-422">Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [etapa 2: editar um GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="05fd2-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="05fd2-423">Você pode comparar o MyOtherGPO ao MyGPO ou ao MyTemplate usando relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="05fd2-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="05fd2-424">Qualquer conta que inclua a função de Revisor (administrador do AGPM \ [controle total \], Aprovador, editor ou revisor) pode gerar relatórios.</span><span class="sxs-lookup"><span data-stu-id="05fd2-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="05fd2-425">Para comparar um GPO a outro GPO e a um modelo</span><span class="sxs-lookup"><span data-stu-id="05fd2-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="05fd2-426">Para comparar o MyGPO e o MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="05fd2-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="05fd2-427">Na guia **controlado** , clique em **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="05fd2-428">Pressione CTRL e clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="05fd2-429">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **relatório HTML**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="05fd2-430">Para comparar MyOtherGPO e MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="05fd2-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="05fd2-431">Na guia **controlado** , clique em **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="05fd2-432">Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **modelo**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="05fd2-433">Selecione meu **modelo** e **relatório HTML**e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="05fd2-434">Etapa 5: excluir e restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="05fd2-435">Nesta etapa, você atua como um Aprovador para excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="05fd2-436">Para excluir um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="05fd2-437">Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário à qual a função de aprovador está atribuída.</span><span class="sxs-lookup"><span data-stu-id="05fd2-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="05fd2-438">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="05fd2-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="05fd2-439">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="05fd2-440">Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="05fd2-441">Clique em **excluir GPO do arquivo morto e da produção** para excluir a versão no arquivo morto e a versão implantada do GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="05fd2-442">Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="05fd2-443">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-444">O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído.</span><span class="sxs-lookup"><span data-stu-id="05fd2-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="05fd2-445">Às vezes, você pode descobrir depois de excluir um GPO que ainda é necessário.</span><span class="sxs-lookup"><span data-stu-id="05fd2-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="05fd2-446">Nesta etapa, você atua como um Aprovador para restaurar um GPO que foi excluído.</span><span class="sxs-lookup"><span data-stu-id="05fd2-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="05fd2-447">Para restaurar um GPO excluído</span><span class="sxs-lookup"><span data-stu-id="05fd2-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="05fd2-448">Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.</span><span class="sxs-lookup"><span data-stu-id="05fd2-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="05fd2-449">Clique com o botão direito do mouse em **MyGPO**e clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="05fd2-450">Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="05fd2-451">Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-452">O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .</span><span class="sxs-lookup"><span data-stu-id="05fd2-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="05fd2-453">**Observação**  Restaurar um GPO para o arquivo não o reimplanta automaticamente no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="05fd2-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="05fd2-454">Para retornar o GPO ao ambiente de produção, implante o GPO da [etapa 3: revise e implante um GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="05fd2-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="05fd2-455">Depois de editar e implantar um GPO, você pode descobrir que alterações recentes no GPO estão causando um problema.</span><span class="sxs-lookup"><span data-stu-id="05fd2-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="05fd2-456">Nesta etapa, você atua como um Aprovador para reverter para uma versão anterior do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="05fd2-457">Você pode reverter para qualquer versão do histórico do GPO.</span><span class="sxs-lookup"><span data-stu-id="05fd2-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="05fd2-458">Você pode usar comentários e rótulos para identificar versões válidas conhecidas e quando foram feitas alterações específicas.</span><span class="sxs-lookup"><span data-stu-id="05fd2-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="05fd2-459">Para reverter para uma versão anterior de um GPO</span><span class="sxs-lookup"><span data-stu-id="05fd2-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="05fd2-460">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="05fd2-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="05fd2-461">Clique duas vezes em **MyGPO** para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="05fd2-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="05fd2-462">Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="05fd2-463">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="05fd2-464">Na janela do **histórico** , clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="05fd2-465">**Observação**  Para verificar se a versão que foi reimplementada é a versão pretendida, examine um relatório de diferença para as duas versões.</span><span class="sxs-lookup"><span data-stu-id="05fd2-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="05fd2-466">Na janela do **histórico** do GPO, selecione as duas versões, clique com o botão direito do mouse nelas, aponte para **diferença**e clique em **relatório HTML** ou **relatório XML**.</span><span class="sxs-lookup"><span data-stu-id="05fd2-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





