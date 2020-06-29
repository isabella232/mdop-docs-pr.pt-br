---
title: Visão geral técnica do AGPM
description: Visão geral técnica do AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797297"
---
# <span data-ttu-id="31ae1-103">Visão geral técnica do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="31ae1-104">O gerenciamento avançado de política de grupo (AGPM) da Microsoft é um aplicativo cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="31ae1-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="31ae1-105">O servidor do AGPM armazena objetos de política de grupo (GPOs) offline no arquivo morto que o AGPM cria no sistema de arquivos do servidor.</span><span class="sxs-lookup"><span data-stu-id="31ae1-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="31ae1-106">Os administradores de política de grupo usam o snap-in do AGPM para o console de gerenciamento de política de grupo (GPMC) para trabalhar com GPOs no servidor que hospeda o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="31ae1-107">Compreender as partes do AGPM e dos itens relacionados, como eles armazenam os GPOs no sistema de arquivos e como as permissões controlam as ações disponíveis para cada função de usuário podem melhorar a eficácia dos administradores de política de grupo com o AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="31ae1-108">Terminologia</span><span class="sxs-lookup"><span data-stu-id="31ae1-108">Terminology</span></span>


<span data-ttu-id="31ae1-109">A seguir está a explicação dos termos básicos do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="31ae1-110">**Cliente do AGPM:** Um computador que executa o snap-in do AGPM para o console de gerenciamento de política de grupo (GPMC) e de quais administradores de política de grupo gerenciam GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="31ae1-111">**Snap-in do AGPM:** O componente de software do AGPM instalado em clientes do AGPM para que eles possam gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="31ae1-112">**Servidor do AGPM:** Um servidor que executa o serviço do AGPM e gerencia um arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="31ae1-113">Cada servidor do AGPM pode gerenciar apenas um arquivo, mas um servidor do AGPM pode gerenciar dados de arquivo para vários domínios em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="31ae1-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="31ae1-114">Um arquivo pode ser hospedado em um computador que não seja um servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="31ae1-115">**Serviço do AGPM:** O componente de software do AGPM que é executado em um servidor do AGPM como um serviço.</span><span class="sxs-lookup"><span data-stu-id="31ae1-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="31ae1-116">O serviço gerencia GPOs no arquivo morto e no ambiente de produção dessa floresta.</span><span class="sxs-lookup"><span data-stu-id="31ae1-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="31ae1-117">**Arquivo morto:** No AGPM, um repositório central que contém os GPOs controlados que o servidor do AGPM associado gerencia, além do histórico de cada um desses GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="31ae1-118">Isso inclui todas as versões controladas anteriores de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="31ae1-119">Um arquivo consiste em um arquivo de índice de arquivo morto e dados de arquivo morto associados que podem incluir dados para GPOs em vários domínios.</span><span class="sxs-lookup"><span data-stu-id="31ae1-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="31ae1-120">Um arquivo pode ser hospedado em um computador que não seja um servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="31ae1-121">**GPO controlado:** Um GPO que está sendo gerenciado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="31ae1-122">O AGPM gerencia o histórico e as permissões dos GPOs controlados, que são armazenados no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="31ae1-123">**GPO não controlado:** Um GPO no ambiente de produção para um domínio e não é gerenciado pelo AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="31ae1-124">O que o AGPM instala, cria e afeta</span><span class="sxs-lookup"><span data-stu-id="31ae1-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="31ae1-125">Em um servidor do AGPM, o programa de instalação do AGPM instala o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="31ae1-126">O AGPM não altera o serviço de diretório® do Active Directory ou o esquema.</span><span class="sxs-lookup"><span data-stu-id="31ae1-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="31ae1-127">Por padrão, os arquivos de programa do servidor do AGPM são instalados no%ProgramFiles%\\Microsoft\\AGPM\\Server.</span><span class="sxs-lookup"><span data-stu-id="31ae1-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="31ae1-128">Você pode instalar o serviço do AGPM em um controlador de domínio se precisar; no entanto, recomendamos que você instale o serviço do AGPM em um servidor membro.</span><span class="sxs-lookup"><span data-stu-id="31ae1-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="31ae1-129">Em um cliente do AGPM, o programa de instalação do AGPM instala o snap-in do AGPM, adicionando uma pasta de **controle de alterações** a cada domínio exibido no GPMC.</span><span class="sxs-lookup"><span data-stu-id="31ae1-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="31ae1-130">Por padrão, os arquivos do programa cliente do AGPM são instalados no%ProgramFiles%\\Microsoft\\AGPM\\Client.</span><span class="sxs-lookup"><span data-stu-id="31ae1-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="31ae1-131">A tabela 1 descreve os itens que o AGPM instala ou cria e as partes do sistema operacional que afetam a operação do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="31ae1-132">Tabela 1: itens instalados, criados ou afetados pelo AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="31ae1-133">Item</span><span class="sxs-lookup"><span data-stu-id="31ae1-133">Item</span></span></th>
<th align="left"><span data-ttu-id="31ae1-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="31ae1-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ae1-135">Serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-136">O serviço do AGPM é executado no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="31ae1-137">O serviço gerencia o arquivo morto, que contém GPOs offline e GPOs controlados no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="31ae1-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="31ae1-138">A configuração padrão do serviço do AGPM é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="31ae1-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="31ae1-139">Nome do serviço: </strong> serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-140">Nome para exibição: </strong> serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-141">Caminho para executável: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="31ae1-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-142">Inicialização: </strong> automática</span><span class="sxs-lookup"><span data-stu-id="31ae1-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-143">Faça logon como: </strong> conta de serviço do AGPM especificada durante a instalação do servidor do AGPM, que pode ser alterada usando <strong> programas e recursos </strong> no <strong> painel de controle </strong> .</span><span class="sxs-lookup"><span data-stu-id="31ae1-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ae1-144">Arquivo do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-145">Por padrão, o AGPM cria o arquivo morto no%ProgramData%\Microsoft\AGPM no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="31ae1-146">O arquivo fornece armazenamento para GPOs offline e pode armazenar várias versões de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="31ae1-147">As alterações que o AGPM faz nos GPOs no arquivo não afetam o ambiente de produção até que um administrador do AGPM ou o aprovador implante o GPO no ambiente de produção e vincule o GPO a uma unidade organizacional (OU).</span><span class="sxs-lookup"><span data-stu-id="31ae1-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ae1-148">Firewall do Windows</span><span class="sxs-lookup"><span data-stu-id="31ae1-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-149">Durante a instalação, o AGPM permite uma regra de firewall de entrada do Windows que permite que o cliente do AGPM se comunique com o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="31ae1-150">A regra padrão do firewall do Windows é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="31ae1-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="31ae1-151">Nome: </strong> serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-152">Ação: </strong> permitir a conexão</span><span class="sxs-lookup"><span data-stu-id="31ae1-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-153">Programas: </strong> todos os programas que atendem às condições especificadas</span><span class="sxs-lookup"><span data-stu-id="31ae1-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-154">Tipo de protocolo: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="31ae1-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-155">Porta local: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="31ae1-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-156">Porta remota: </strong> todas as portas</span><span class="sxs-lookup"><span data-stu-id="31ae1-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-157">Endereço IP local: </strong> qualquer</span><span class="sxs-lookup"><span data-stu-id="31ae1-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="31ae1-158">Endereço IP remoto: </strong> qualquer</span><span class="sxs-lookup"><span data-stu-id="31ae1-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31ae1-159">Servidor de email</span><span class="sxs-lookup"><span data-stu-id="31ae1-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-160">O AGPM usa SMTP (Simple Mail Transfer Protocol) para enviar solicitações de email para os endereços configurados na <strong> Guia de delegação de domínio </strong> . Por exemplo, quando um editor solicita que um novo GPO seja criado, o AGPM notifica cada endereço de email especificado na <strong> Guia de delegação de domínio </strong> .</span><span class="sxs-lookup"><span data-stu-id="31ae1-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31ae1-161">Snap-in do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-162">O snap-in do AGPM para o GPMC é executado em clientes do AGPM e é usado por administradores de política de grupo para gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="31ae1-163">O snap-in é exibido no GPMC como uma <strong> pasta controle de alterações </strong> em cada domínio.</span><span class="sxs-lookup"><span data-stu-id="31ae1-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="31ae1-164">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="31ae1-164">Additional references</span></span>

<span data-ttu-id="31ae1-165">Para obter mais informações sobre os arquivos instalados pelo AGPM, consulte o [Guia de planejamento para o AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span><span class="sxs-lookup"><span data-stu-id="31ae1-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="31ae1-166">Archive</span><span class="sxs-lookup"><span data-stu-id="31ae1-166">Archive</span></span>


<span data-ttu-id="31ae1-167">Por padrão, o processo de instalação do servidor do AGPM cria o arquivo no disco rígido local do servidor do AGPM em%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="31ae1-168">No entanto, você pode alterar o caminho durante a instalação e até mesmo criar o arquivo morto em um servidor que não seja o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="31ae1-169">O arquivo contém uma subpasta para cada versão de cada GPO que o arquivo contém.</span><span class="sxs-lookup"><span data-stu-id="31ae1-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="31ae1-170">O nome de cada subpasta é um GUID que identifica uma versão do GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="31ae1-171">O arquivo gpostate.xml registra o estado de cada GPO no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="31ae1-172">O arquivo é um manifesto que descreve o conteúdo do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="31ae1-173">Por exemplo, um GPO pode ter várias versões, e cada versão está em sua própria subpasta no arquivo.</span><span class="sxs-lookup"><span data-stu-id="31ae1-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="31ae1-174">O arquivo gpostate.xml indica quais subpastas contêm versões diferentes de um único GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="31ae1-175">Além disso, os modelos de GPO têm subpastas no arquivo, mas gpostate.xml indicam que esses são modelos e não GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="31ae1-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="31ae1-176">Da mesma forma, quando os administradores de política de Grupo excluem GPOs, o AGPM altera seus Estados em gpostate.xml para indicar que eles estão na **Lixeira** , mas não remove as subpastas dos GPOs do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="31ae1-177">**Cuidado**  Não edite gpostate.xml manualmente ou os GPOs que o arquivo contém.</span><span class="sxs-lookup"><span data-stu-id="31ae1-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="31ae1-178">Essas informações são fornecidas apenas para melhorar a compreensão do arquivamento do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="31ae1-179">Em vez disso, use o snap-in do AGPM para alterar os GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="31ae1-180">Quando o AGPM cria o arquivo morto, ele dá controle total a sistema, administradores e conta de serviço do AGPM (especificado na configuração do servidor do AGPM).</span><span class="sxs-lookup"><span data-stu-id="31ae1-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="31ae1-181">Alterar permissões usando a interface do usuário do AGPM no snap-in do AGPM não altera permissões no arquivo morto, porque a conta do serviço do AGPM executa todas as operações em nome do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="31ae1-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="31ae1-182">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="31ae1-182">Additional references</span></span>

<span data-ttu-id="31ae1-183">Para obter informações sobre como fazer backup do arquivo morto, restaurar o arquivo de um backup ou mover o servidor do AGPM e o arquivo morto, consulte a seção "realizando tarefas do administrador do AGPM" no [Guia de operações do AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="31ae1-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="31ae1-184">Funções e permissões</span><span class="sxs-lookup"><span data-stu-id="31ae1-184">Roles and permissions</span></span>


<span data-ttu-id="31ae1-185">As funções simplificam a delegação.</span><span class="sxs-lookup"><span data-stu-id="31ae1-185">Roles simplify delegation.</span></span> <span data-ttu-id="31ae1-186">Em vez de atribuir permissões detalhadas a administradores de política de grupo, os administradores do AGPM podem atribuir uma das quatro funções aos administradores de política de grupo para que elas realizem o trabalho relacionado a essa função:</span><span class="sxs-lookup"><span data-stu-id="31ae1-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="31ae1-187">**Administrador do AGPM:** Administradores de política de grupo com a função de administrador do AGPM (controle total) atribuídas podem executar qualquer tarefa no AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="31ae1-188">Os administradores do AGPM podem configurar opções em todo o domínio e delegar permissões para outros administradores de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="31ae1-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="31ae1-189">**Aprovador:** Os administradores de política de grupo atribuíram a função de aprovador podem implantar GPOs no ambiente de produção para um domínio.</span><span class="sxs-lookup"><span data-stu-id="31ae1-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="31ae1-190">Os aprovadores também podem criar e excluir GPOs e aprovar ou rejeitar solicitações dos editores.</span><span class="sxs-lookup"><span data-stu-id="31ae1-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="31ae1-191">Os aprovadores podem exibir a lista de GPOs em um domínio, Visualizar as configurações de política em GPOs e criar e exibir relatórios das configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="31ae1-192">Não é possível editar as configurações de política nos GPOs, a menos que elas também sejam atribuídas à função de editor.</span><span class="sxs-lookup"><span data-stu-id="31ae1-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="31ae1-193">**Editor:** Administradores de política de grupo atribuídos a função de editor podem exibir a lista de GPOs em um domínio, Visualizar as configurações de política em GPOs, editar as configurações de política em GPOs e criar e exibir relatórios das configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="31ae1-194">A menos que também sejam atribuídas a função de aprovador, os editores não poderão criar, implantar ou excluir GPOs.</span><span class="sxs-lookup"><span data-stu-id="31ae1-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="31ae1-195">No entanto, eles podem solicitar que os GPOs sejam criados, implantados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="31ae1-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="31ae1-196">**Revisor:** Administradores de política de grupo atribuídos a função de revisor podem exibir a lista de GPOs em um domínio e criar e exibir relatórios das configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="31ae1-197">A menos que também sejam atribuídas a função de editor, eles não podem editar as configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="31ae1-198">O AGPM proporciona aos administradores do AGPM a flexibilidade de configurar permissões em um nível mais detalhado do que as funções usando o snap-in do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="31ae1-199">A tabela 2 descreve essas permissões e indica as permissões concedidas a cada função por padrão.</span><span class="sxs-lookup"><span data-stu-id="31ae1-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="31ae1-200">Permissão</span><span class="sxs-lookup"><span data-stu-id="31ae1-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="31ae1-201">Descrição</span><span class="sxs-lookup"><span data-stu-id="31ae1-201">Description</span></span></th>
<th align="left"><span data-ttu-id="31ae1-202">Administrador do AGPM</span><span class="sxs-lookup"><span data-stu-id="31ae1-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="31ae1-203">Aprovador</span><span class="sxs-lookup"><span data-stu-id="31ae1-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="31ae1-204">Editor</span><span class="sxs-lookup"><span data-stu-id="31ae1-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="31ae1-205">Revisor</span><span class="sxs-lookup"><span data-stu-id="31ae1-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-206">Controle total</span><span class="sxs-lookup"><span data-stu-id="31ae1-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-207">Ter todas as permissões.</span><span class="sxs-lookup"><span data-stu-id="31ae1-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-208">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-209">Criar GPO</span><span class="sxs-lookup"><span data-stu-id="31ae1-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-210">Criar GPOs em um domínio.</span><span class="sxs-lookup"><span data-stu-id="31ae1-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-211">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-212">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-213">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="31ae1-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-214">Listar os GPOs em um domínio.</span><span class="sxs-lookup"><span data-stu-id="31ae1-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-215">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-216">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-217">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-218">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-219">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="31ae1-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-220">Leia as configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-221">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-222">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-223">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-224">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-225">Editar configurações</span><span class="sxs-lookup"><span data-stu-id="31ae1-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-226">Altere as configurações de política em um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-227">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="31ae1-228">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-229">Excluir GPO</span><span class="sxs-lookup"><span data-stu-id="31ae1-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-230">Excluir um GPO.</span><span class="sxs-lookup"><span data-stu-id="31ae1-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-231">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-232">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-233">Modificar a segurança</span><span class="sxs-lookup"><span data-stu-id="31ae1-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-234">Delegar o acesso ao nível do domínio, acessar o acesso a um único GPO e delegar o acesso ao ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="31ae1-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-235">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-236">Implantar GPO</span><span class="sxs-lookup"><span data-stu-id="31ae1-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-237">Implante um GPO do arquivo morto para o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="31ae1-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-238">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-239">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-240">Criar modelo</span><span class="sxs-lookup"><span data-stu-id="31ae1-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-241">Crie um modelo de GPO no AGPM.</span><span class="sxs-lookup"><span data-stu-id="31ae1-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-242">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="31ae1-243">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-244">Opções de modificação</span><span class="sxs-lookup"><span data-stu-id="31ae1-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-245">Configurar a notificação de email do AGPM e limitar as versões do GPO armazenadas no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31ae1-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-246">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="31ae1-247">GPO de exportação</span><span class="sxs-lookup"><span data-stu-id="31ae1-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-248">Exportar um GPO para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="31ae1-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-249">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="31ae1-250">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="31ae1-251">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="31ae1-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="31ae1-252">Importar um GPO de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="31ae1-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="31ae1-253">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="31ae1-254">Sim</span><span class="sxs-lookup"><span data-stu-id="31ae1-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="31ae1-255">**Observação** 
 As permissões **Exportar GPO** e **importar GPO** não estão disponíveis no AGPM 3,0 ou 2,5.</span><span class="sxs-lookup"><span data-stu-id="31ae1-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="31ae1-256">A capacidade de delegar o acesso a GPOs no ambiente de produção para um domínio e a capacidade de limitar o número de versões de GPO armazenadas não está disponível no AGPM 2,5.</span><span class="sxs-lookup"><span data-stu-id="31ae1-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="31ae1-257">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="31ae1-257">Additional references</span></span>

<span data-ttu-id="31ae1-258">Para saber mais sobre quais tarefas podem ser executadas por administradores de política de grupo com uma função específica atribuídas ou sobre quais permissões são necessárias para executar uma tarefa específica, consulte o [Guia de operações para o AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="31ae1-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





