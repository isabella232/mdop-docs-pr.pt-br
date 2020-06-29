---
title: Noções básicas sobre relatórios do MBAM
description: Noções básicas sobre relatórios do MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799158"
---
# <span data-ttu-id="fc8d8-103">Noções básicas sobre relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="fc8d8-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) geram vários relatórios para monitorar o uso e a conformidade do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="fc8d8-105">Este tópico descreve os relatórios do MBAM para conformidade empresarial, computadores individuais, compatibilidade de hardware e atividade de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="fc8d8-106">Noções básicas sobre relatórios</span><span class="sxs-lookup"><span data-stu-id="fc8d8-106">Understanding Reports</span></span>


<span data-ttu-id="fc8d8-107">Para acessar o recurso relatórios do MBAM, abra o site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="fc8d8-108">Selecione **relatórios** no painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="fc8d8-109">Em seguida, no painel de conteúdo principal, clique na guia do tipo de relatório: **relatório de conformidade empresarial**, **relatório de conformidade do computador**, relatório de auditoria de **hardware**ou relatório de **auditoria de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="fc8d8-110">Relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="fc8d8-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="fc8d8-111">Um relatório de conformidade empresarial fornece informações sobre a conformidade geral do BitLocker em sua organização.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="fc8d8-112">Os filtros disponíveis para este relatório permitem restringir os resultados da pesquisa de acordo com o estado de conformidade e o status do erro.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="fc8d8-113">Este relatório é executado a cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-113">This report runs every six hours.</span></span>

**<span data-ttu-id="fc8d8-114">Campos relatório de conformidade para empresas</span><span class="sxs-lookup"><span data-stu-id="fc8d8-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-115">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="fc8d8-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-117">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-118">O nome DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-119">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="fc8d8-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-120">O nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-121">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-122">O estado de conformidade do computador, de acordo com a política especificada para o computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="fc8d8-123">Os Estados possíveis são incompatíveis e em conformidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="fc8d8-124">Para obter mais informações, consulte Estados de conformidade do relatório de conformidade empresarial neste tópico.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-125">Isenção</span><span class="sxs-lookup"><span data-stu-id="fc8d8-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-126">O estado do hardware do computador para determinar a identificação do tipo de hardware e se o computador está isento da política.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="fc8d8-127">Há três estados possíveis: hardware desconhecido (o tipo de hardware não foi identificado pela MBAM), isenta de hardware (o tipo de hardware foi identificado e foi marcado como isento da política de MBAM) e não está isento (o hardware foi identificado e não está isento da política).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-128">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fc8d8-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-129">Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-130">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-131">Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-132">Último contato</span><span class="sxs-lookup"><span data-stu-id="fc8d8-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-133">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="fc8d8-134">Esse horário é configurável.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-134">This time is configurable.</span></span> <span data-ttu-id="fc8d8-135">Consulte Configurações de política de MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="fc8d8-136">Estados de conformidade para relatórios de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="fc8d8-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-137">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-138">Isenção</span><span class="sxs-lookup"><span data-stu-id="fc8d8-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-139">Description</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-140">Ação do usuário</span><span class="sxs-lookup"><span data-stu-id="fc8d8-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-141">Não compatível</span><span class="sxs-lookup"><span data-stu-id="fc8d8-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-142">Não isento</span><span class="sxs-lookup"><span data-stu-id="fc8d8-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-143">O computador não é compatível, de acordo com a política especificada, e o tipo de hardware não foi indicado como isento da política.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-144">Clique em <strong> nome </strong> do computador para expandir o relatório de conformidade do computador e determinar se o estado de cada unidade está em conformidade com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="fc8d8-145">Se o estado de criptografia indicar que o computador não está criptografado, talvez a criptografia ainda esteja em andamento ou talvez haja um erro no computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="fc8d8-146">Se não houver nenhum erro, a causa provável é que o computador ainda está em processo de conexão ou estabelecimento do status de criptografia.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="fc8d8-147">Verifique novamente mais tarde para determinar se o estado muda.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-148">CLS</span><span class="sxs-lookup"><span data-stu-id="fc8d8-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-149">Não isento</span><span class="sxs-lookup"><span data-stu-id="fc8d8-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-150">O computador é compatível de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-151">Nenhuma ação necessária.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-151">No Action needed.</span></span> <span data-ttu-id="fc8d8-152">Opcionalmente, você pode exibir o relatório de conformidade do computador para confirmar o estado do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-153">CLS</span><span class="sxs-lookup"><span data-stu-id="fc8d8-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-154">Isento de hardware</span><span class="sxs-lookup"><span data-stu-id="fc8d8-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-155">Se o tipo de hardware estiver isento.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="fc8d8-156">Independentemente de como a política é definida ou o status individual de cada unidade de disco rígido, o estado geral é considerado compatível.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-157">Nenhuma ação necessária.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-158">CLS</span><span class="sxs-lookup"><span data-stu-id="fc8d8-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-159">Hardware desconhecido</span><span class="sxs-lookup"><span data-stu-id="fc8d8-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-160">O MBAM reconhece o tipo de hardware, mas o MBAM não sabe se está isento ou isento de isenção.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="fc8d8-161">Isso ocorrerá se o administrador não tiver definido o status de compatibilidade do hardware.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="fc8d8-162">Portanto, o MBAM é revertido para o status compatível por padrão.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-163">Esse é o estado inicial de um cliente MBAM recém implantado.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="fc8d8-164">Geralmente, é apenas um estado transitório.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-164">It is typically only a transient state.</span></span> <span data-ttu-id="fc8d8-165">Mesmo que o administrador tenha marcado o hardware como compatível, pode haver um atraso significativo ou tempo de espera configurável antes de o computador cliente retornar a relatórios.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="fc8d8-166">Anote a hora do último contato e faça check-in novamente após o intervalo especificado para ver se o estado mudou.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="fc8d8-167">Se o estado não mudar, pode haver um erro para este computador ou tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fc8d8-168">Relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-168">Computer Compliance Report</span></span>

<span data-ttu-id="fc8d8-169">O relatório de conformidade do computador exibe informações específicas para um computador ou usuário.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="fc8d8-170">O relatório de conformidade do computador fornece informações de criptografia detalhadas e políticas aplicáveis para cada unidade em um computador, incluindo unidades do sistema operacional e unidades de dados fixos.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="fc8d8-171">Para exibir esse tipo de relatório, clique no nome do computador no relatório de conformidade empresarial ou digite o nome do computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="fc8d8-172">Para ver os detalhes de cada unidade, expanda a entrada nome do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="fc8d8-173">**Observação**  Esse relatório não fornece o status de criptografia para volumes de dados removíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="fc8d8-174">Campos de relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-175">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="fc8d8-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-177">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-178">O nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-179">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="fc8d8-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-180">O nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-181">Tipo de computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-182">O tipo de portabilidade do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-182">The portability type of computer.</span></span> <span data-ttu-id="fc8d8-183">Tipos válidos são não portáteis e portáteis.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-184">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="fc8d8-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-185">Tipo de sistema operacional instalado no computador cliente gerenciado MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-186">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-187">O status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="fc8d8-188">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="fc8d8-189">Embora seja possível ter unidades de conformidade e de não conformidade no mesmo computador, esse campo indica a conformidade geral do computador por política especificada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-190">Força da política de Cypher</span><span class="sxs-lookup"><span data-stu-id="fc8d8-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-191">A intensidade de codificação selecionada pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="fc8d8-192">Por exemplo, 128-bit com difusor</span><span class="sxs-lookup"><span data-stu-id="fc8d8-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-193">Unidade de sistema operacional da política</span><span class="sxs-lookup"><span data-stu-id="fc8d8-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-194">Indica se a criptografia é necessária para o o/S e o tipo de protetor conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-195">Unidade de dados fixos da política</span><span class="sxs-lookup"><span data-stu-id="fc8d8-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-196">Indica se a criptografia é necessária para a unidade fixa.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-197">Unidade de dados removível de política</span><span class="sxs-lookup"><span data-stu-id="fc8d8-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-198">Indica se a criptografia é necessária para a unidade removível.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-199">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fc8d8-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-200">Fornece a identidade de usuários conhecidos no computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-201">Isenção</span><span class="sxs-lookup"><span data-stu-id="fc8d8-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-202">Indica se o tipo de hardware do computador é reconhecido pela MBAM e, se for conhecido, se o computador foi indicado como isento da política.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="fc8d8-203">Há três Estados: hardware desconhecido (o tipo de hardware não foi identificado pela MBAM); Isento de hardware (o tipo de hardware foi identificado e foi marcado como isento da política MBAM); e não isento (o hardware foi identificado e não está isento da política).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-204">Fabricante</span><span class="sxs-lookup"><span data-stu-id="fc8d8-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-205">O nome do fabricante do computador exibido no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-206">Modelo</span><span class="sxs-lookup"><span data-stu-id="fc8d8-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-207">O nome do modelo do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-208">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-209">Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-210">Último contato</span><span class="sxs-lookup"><span data-stu-id="fc8d8-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-211">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="fc8d8-212">T</span><span class="sxs-lookup"><span data-stu-id="fc8d8-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="fc8d8-213">Campos da unidade do relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="fc8d8-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-214">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="fc8d8-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-216">Letra da unidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-217">Letra da unidade de computador que foi atribuída a essa determinada unidade pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-218">Tipo de unidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-219">Tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-219">Type of drive.</span></span> <span data-ttu-id="fc8d8-220">Os valores válidos são unidade do sistema operacional e unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="fc8d8-221">Esses são drives físicos, em vez de volumes lógicos.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-222">Força Cypher</span><span class="sxs-lookup"><span data-stu-id="fc8d8-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-223">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-224">Tipo de protetor</span><span class="sxs-lookup"><span data-stu-id="fc8d8-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-225">Tipo de protetor selecionado pela política usada para criptografar um sistema operacional ou volume fixo.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="fc8d8-226">Os tipos de protetor válidos em uma unidade de sistema operacional são TPM ou TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="fc8d8-227">O único tipo de protetor válido para um volume de dados fixo é a senha.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-228">Estado do protetor</span><span class="sxs-lookup"><span data-stu-id="fc8d8-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-229">Este campo indica se o computador ativou o tipo de protetor especificado na política.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="fc8d8-230">Os Estados válidos estão ATIVAdos ou desativados.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-231">Estado de criptografia</span><span class="sxs-lookup"><span data-stu-id="fc8d8-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-232">Esse é o estado atual de criptografia da unidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="fc8d8-233">Os Estados válidos são criptografados, não criptografados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-234">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-235">Indica se a unidade está de acordo com a política.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="fc8d8-236">Os Estados são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-237">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="fc8d8-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-238">Contém mensagens de erro e status sobre o estado de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fc8d8-239">Relatório de auditoria de hardware</span><span class="sxs-lookup"><span data-stu-id="fc8d8-239">Hardware Audit Report</span></span>

<span data-ttu-id="fc8d8-240">Este relatório pode ajudá-lo a auditar alterações no status de compatibilidade de hardware de modelos e modelos de computador específicos.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="fc8d8-241">Para ajudá-lo a restringir os resultados da pesquisa, esse relatório inclui a filtragem de critérios, como tipo de alteração e hora de ocorrência.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="fc8d8-242">Cada alteração de estado é controlada por usuário e data e hora.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="fc8d8-243">O tipo de hardware é automaticamente preenchido pelo agente do MBAM que é executado no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="fc8d8-244">Esse relatório controla as alterações do usuário nas informações coletadas diretamente do computador gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="fc8d8-245">Uma alteração administrativa típica está mudando de compatível para incompatível.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="fc8d8-246">No entanto, o administrador também pode revisar qualquer campo.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="fc8d8-247">Campos de relatório de auditoria de hardware</span><span class="sxs-lookup"><span data-stu-id="fc8d8-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-248">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="fc8d8-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-249">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-250">Data e hora</span><span class="sxs-lookup"><span data-stu-id="fc8d8-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-251">Data e hora em que uma alteração foi feita para o tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="fc8d8-252">Observe que cada tipo de hardware exclusivo é atribuído a pelo menos uma entrada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-253">Usuário</span><span class="sxs-lookup"><span data-stu-id="fc8d8-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-254">Usuário administrativo que fez a alteração para a entrada específica.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-255">Tipo de alteração</span><span class="sxs-lookup"><span data-stu-id="fc8d8-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-256">Tipo de alteração feita nas informações de tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="fc8d8-257">Os valores válidos são soma (nova entrada), atualizar (alterar entrada existente) ou exclusão (remover entrada existente).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-258">Valor original</span><span class="sxs-lookup"><span data-stu-id="fc8d8-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-259">Valor da especificação do tipo de hardware antes da alteração ser feita.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-260">Valor atual</span><span class="sxs-lookup"><span data-stu-id="fc8d8-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-261">Valor da especificação do tipo de hardware após a alteração ter sido feita.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fc8d8-262">Relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="fc8d8-262">Recovery Audit Report</span></span>

<span data-ttu-id="fc8d8-263">O relatório de auditoria de recuperação pode ajudá-lo a auditar os usuários que solicitaram acesso às chaves de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="fc8d8-264">Os critérios de filtro deste relatório incluem o tipo de usuário que está realizando a solicitação, o tipo de chave solicitada, o tempo de ocorrência, êxito ou falha, hora de ocorrência e tipo de usuário solicitando (suporte técnico, usuário final).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="fc8d8-265">Esse relatório permite que os administradores produzam relatórios contextuais de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="fc8d8-266">Campos de relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="fc8d8-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc8d8-267">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="fc8d8-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="fc8d8-268">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8d8-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-269">Data e hora da solicitação</span><span class="sxs-lookup"><span data-stu-id="fc8d8-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-270">A data e a hora em que uma solicitação de recuperação de chave foi feita por um usuário final ou usuário de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-271">Status da solicitação</span><span class="sxs-lookup"><span data-stu-id="fc8d8-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-272">Status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-272">Status of the request.</span></span> <span data-ttu-id="fc8d8-273">Os status válidos são bem-sucedidos (a chave foi recuperada) ou falha (a tecla não foi recuperada).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-274">Usuário da assistência técnica</span><span class="sxs-lookup"><span data-stu-id="fc8d8-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-275">O usuário de suporte técnico que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="fc8d8-276">Se o usuário do suporte técnico recuperar a chave em nome de um usuário final, o campo usuário final estará em branco.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-277">Usuário</span><span class="sxs-lookup"><span data-stu-id="fc8d8-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-278">O usuário final que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc8d8-279">Tipo de chave</span><span class="sxs-lookup"><span data-stu-id="fc8d8-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-280">O tipo de chave que foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-280">The type of key that was requested.</span></span> <span data-ttu-id="fc8d8-281">O MBAM coleta três tipos de chave: senha da chave de recuperação (para a recuperação de um computador no modo de recuperação); ID da chave de recuperação (para recuperar um computador no modo de recuperação em nome de outro usuário); e hash de senha do Trusted Platform Module (TPM) (para recuperar um computador com um TPM bloqueado).</span><span class="sxs-lookup"><span data-stu-id="fc8d8-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc8d8-282">Descrição do motivo</span><span class="sxs-lookup"><span data-stu-id="fc8d8-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc8d8-283">O motivo pelo qual o tipo de chave especificado foi solicitado.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="fc8d8-284">Os motivos são especificados nos recursos de recuperação de unidade e gerenciamento de TPM do site administrativo.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="fc8d8-285">As entradas válidas incluem texto inserido pelo usuário ou um dos seguintes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="fc8d8-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="fc8d8-286">Ordem de inicialização do sistema operacional alterada</span><span class="sxs-lookup"><span data-stu-id="fc8d8-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-287">BIOS alterado</span><span class="sxs-lookup"><span data-stu-id="fc8d8-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-288">Arquivos do sistema operacional alterados</span><span class="sxs-lookup"><span data-stu-id="fc8d8-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-289">Chave de inicialização perdida</span><span class="sxs-lookup"><span data-stu-id="fc8d8-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-290">Perdeu o PIN</span><span class="sxs-lookup"><span data-stu-id="fc8d8-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-291">Redefinição de TPM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-292">Senha perdida</span><span class="sxs-lookup"><span data-stu-id="fc8d8-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-293">Cartão inteligente perdido</span><span class="sxs-lookup"><span data-stu-id="fc8d8-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-294">Redefinir o bloqueio de PIN</span><span class="sxs-lookup"><span data-stu-id="fc8d8-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-295">Ativar o TPM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-296">Desativar o TPM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-297">Alterar a senha do TPM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="fc8d8-298">Limpar TPM</span><span class="sxs-lookup"><span data-stu-id="fc8d8-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fc8d8-299">**Observação**  Para salvar os resultados do relatório em um arquivo, clique no botão **Exportar** na barra de menus relatórios.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="fc8d8-300">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc8d8-300">Related topics</span></span>


[<span data-ttu-id="fc8d8-301">Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="fc8d8-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





