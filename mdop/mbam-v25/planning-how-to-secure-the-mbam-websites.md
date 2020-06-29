---
title: Planejamento de formas para proteger os sites do MBAM
description: Planejamento de formas para proteger os sites do MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799589"
---
# <span data-ttu-id="6daf3-103">Planejamento de formas para proteger os sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="6daf3-104">Este tópico descreve os métodos a seguir para proteger o site de administração e monitoramento do Microsoft BitLocker (MBAM) 2,5 para o site de administração e o portal de autoatendimento:</span><span class="sxs-lookup"><span data-stu-id="6daf3-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-105">Método</span><span class="sxs-lookup"><span data-stu-id="6daf3-105">Method</span></span></th>
<th align="left"><span data-ttu-id="6daf3-106">Obrigatório ou opcional?</span><span class="sxs-lookup"><span data-stu-id="6daf3-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-107">Usar certificados para proteger sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-108">Opcional, mas altamente recomendado</span><span class="sxs-lookup"><span data-stu-id="6daf3-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-109">Registrando o SPN (nomes de entidade de serviço) para a conta do pool de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6daf3-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6daf3-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6daf3-111">Para obter mais informações sobre como proteger sua implantação do MBAM, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="6daf3-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="6daf3-112">Usar certificados para proteger sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="6daf3-113">Recomendamos que você use um certificado para proteger a comunicação entre:</span><span class="sxs-lookup"><span data-stu-id="6daf3-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="6daf3-114">Cliente MBAM e os serviços Web</span><span class="sxs-lookup"><span data-stu-id="6daf3-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="6daf3-115">Navegador e o site de administração e monitoramento e sites de portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="6daf3-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="6daf3-116">Para saber mais sobre como solicitar e instalar um certificado, consulte [Configurando certificados do servidor de Internet](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="6daf3-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="6daf3-117">Observação</span><span class="sxs-lookup"><span data-stu-id="6daf3-117">Note</span></span>**  
<span data-ttu-id="6daf3-118">Você pode configurar os sites e serviços Web em servidores diferentes somente se você estiver usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6daf3-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="6daf3-119">Se você usar o assistente de configuração do servidor do MBAM para configurar os sites, você deve configurar os sites e os serviços Web no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="6daf3-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="6daf3-120">Para proteger a comunicação entre os serviços Web e os bancos de dados, também recomendamos que você force a criptografia no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6daf3-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="6daf3-121">Para obter informações sobre como proteger todas as conexões com o SQL Server, incluindo a comunicação entre os serviços Web e o SQL Server, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="6daf3-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="6daf3-122">Registrando SPNs para a conta do pool de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6daf3-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="6daf3-123">Para habilitar os servidores MBAM para autenticar a comunicação a partir do site de administração e monitoramento e do portal de autoatendimento, você deve registrar um SPN (nome da entidade de serviço) para o nome do host na conta de domínio que você está usando para o pool de aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="6daf3-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="6daf3-124">Este tópico contém instruções sobre como registrar SPNs para os seguintes tipos de nomes de host:</span><span class="sxs-lookup"><span data-stu-id="6daf3-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="6daf3-125">Nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="6daf3-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="6daf3-126">Nome NetBIOS</span><span class="sxs-lookup"><span data-stu-id="6daf3-126">NetBIOS name</span></span>

-   <span data-ttu-id="6daf3-127">Nome virtual</span><span class="sxs-lookup"><span data-stu-id="6daf3-127">Virtual name</span></span>

### <span data-ttu-id="6daf3-128">Antes de criar SPNs para uma instalação inicial do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="6daf3-129">Revise as informações na tabela a seguir antes de começar a criar SPNs.</span><span class="sxs-lookup"><span data-stu-id="6daf3-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-130">Tarefa ou item</span><span class="sxs-lookup"><span data-stu-id="6daf3-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="6daf3-131">Mais informações</span><span class="sxs-lookup"><span data-stu-id="6daf3-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-132">Crie uma conta de serviço nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="6daf3-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-133">A conta de serviço é uma conta de usuário que você cria no AD DS para fornecer segurança para os sites do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6daf3-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="6daf3-134">Os sites do MBAM são executados em um pool de aplicativos cuja identidade é o nome da conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="6daf3-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="6daf3-135">Em seguida, os SPNs são registrados na conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6daf3-136">Observação</span><span class="sxs-lookup"><span data-stu-id="6daf3-136">Note</span></span></strong><br/><p><span data-ttu-id="6daf3-137">Você deve usar a mesma conta de pool de aplicativos para todos os servidores Web.</span><span class="sxs-lookup"><span data-stu-id="6daf3-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-138">Verifique se a conta de grupo IIS-IUSRS ou a conta de pool de aplicativos recebeu os direitos necessários.</span><span class="sxs-lookup"><span data-stu-id="6daf3-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-139">Para verificar isso, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="6daf3-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="6daf3-140">Abra o <strong> Editor de política de segurança local </strong> e expanda o <strong> nó Diretivas locais </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="6daf3-141">Selecione o <strong> nó atribuição de direitos de usuário </strong> e, em seguida, clique duas vezes no painel direito, clique em <strong> representar um cliente após autenticação </strong> e <strong> logon como um trabalho em lotes </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-142">Se você configurar os sites do MBAM usando uma conta de administrador de domínio, o MBAM criará os SPNs para você.</span><span class="sxs-lookup"><span data-stu-id="6daf3-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-143">Se você configurar os sites do MBAM usando uma conta de administrador de domínio, siga as etapas neste tópico para registrar os SPNs manualmente para o tipo de nome de host que você está usando.</span><span class="sxs-lookup"><span data-stu-id="6daf3-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="6daf3-144">Registrando SPNs quando você usa um nome de host de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="6daf3-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="6daf3-145">Se você usar um nome de host de domínio totalmente qualificado ao configurar o MBAM, será necessário registrar apenas um SPN, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="6daf3-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-146">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="6daf3-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="6daf3-147">Exemplos e mais informações</span><span class="sxs-lookup"><span data-stu-id="6daf3-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-148">Registre um SPN para o nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6daf3-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-149">O nome totalmente qualificado do host é <strong> mybitlockerrecovery.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-150">Configure a delegação restrita para o SPN que você está registrando para a conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="6daf3-151">Configuração da delegação restrita</span><span class="sxs-lookup"><span data-stu-id="6daf3-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="6daf3-152">Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="6daf3-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="6daf3-153">Registrando SPNs quando você usa um nome de host NetBIOS</span><span class="sxs-lookup"><span data-stu-id="6daf3-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="6daf3-154">Se você usar um nome de host NetBIOS ao configurar o MBAM, registre um SPN para o nome NetBIOS e outro SPN para o nome de domínio totalmente qualificado, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6daf3-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-155">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="6daf3-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="6daf3-156">Exemplos e mais informações</span><span class="sxs-lookup"><span data-stu-id="6daf3-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-157">Registre um SPN para o nome do host NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="6daf3-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-158">O nome do host NetBIOS é <strong> nbname01 </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-159">Registre um SPN para o nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6daf3-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-160">O nome de domínio totalmente qualificado é <strong> nbname01.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-161">Configure a delegação restrita para os SPNs que você está registrando para a conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="6daf3-162">Configuração da delegação restrita</span><span class="sxs-lookup"><span data-stu-id="6daf3-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="6daf3-163">Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="6daf3-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="6daf3-164">Registrando SPNs quando você usa um nome de host virtual</span><span class="sxs-lookup"><span data-stu-id="6daf3-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="6daf3-165">Se você configurar o MBAM com um nome de host virtual que é um nome de domínio totalmente qualificado, registre apenas um SPN para o nome do host virtual.</span><span class="sxs-lookup"><span data-stu-id="6daf3-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="6daf3-166">Se o nome do host virtual que você configurar não for um nome de domínio totalmente qualificado, você deve criar um segundo SPN que especifica o nome de domínio totalmente qualificado, conforme descrito nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6daf3-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-167">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="6daf3-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="6daf3-168">Exemplos e mais informações</span><span class="sxs-lookup"><span data-stu-id="6daf3-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-169">Se o seu nome de host virtual for um nome de domínio totalmente qualificado, como neste exemplo, registre apenas um SPN.</span><span class="sxs-lookup"><span data-stu-id="6daf3-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-170">No exemplo, o nome do host virtual é <strong> mbamvirtual.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-171">Registre esse SPN adicional se seu nome de host virtual não for um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6daf3-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-172">No exemplo, o nome do host virtual é <strong> mbamvirtual </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-173">Registre esse SPN adicional se seu nome de host virtual não for um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6daf3-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="6daf3-174">No exemplo, o nome do host virtual é <strong> mbamvirtual.contoso.com </strong> e a conta de domínio usada para o pool de aplicativos Web é <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-175">No servidor DNS (servidor de nomes de domínio), crie um "registro A" para o nome de host personalizado e o aponte para um servidor Web ou um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="6daf3-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-176">Consulte a seção "Configurar registros de um host DNS" em <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> Configurar registros de host DNS </a> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="6daf3-177">Recomendamos que você use registros em vez de CNAMEs.</span><span class="sxs-lookup"><span data-stu-id="6daf3-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="6daf3-178">Se você usar CNAMEs para apontar para o endereço de domínio, também deverá registrar os SPNs para o nome do servidor Web na conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-179">Configure a delegação restrita para os SPNs que você está registrando para a conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="6daf3-180">Configuração da delegação restrita</span><span class="sxs-lookup"><span data-stu-id="6daf3-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="6daf3-181">Este requisito aplica-se somente ao MBAM 2,5; Não é necessário no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="6daf3-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="6daf3-182">Registrando um SPN durante a atualização de versões anteriores do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="6daf3-183">Conclua as etapas nesta seção apenas se desejar:</span><span class="sxs-lookup"><span data-stu-id="6daf3-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="6daf3-184">Atualize a partir de uma versão anterior do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6daf3-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="6daf3-185">Execute os sites no MBAM 2,5 em uma configuração de carga balanceada ou distribuída e, no momento, você está executando em uma configuração que não está equilibrada para a carga.</span><span class="sxs-lookup"><span data-stu-id="6daf3-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="6daf3-186">Se você já registrou SPNs na conta do computador, em vez de em uma conta de pool de aplicativos, o MBAM usa os SPNs existentes, e você não pode configurar os websites em uma configuração de carga balanceada ou distribuída.</span><span class="sxs-lookup"><span data-stu-id="6daf3-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-187">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="6daf3-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="6daf3-188">Exemplos e mais informações</span><span class="sxs-lookup"><span data-stu-id="6daf3-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-189">Criar uma conta de pool de aplicativos nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="6daf3-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-190">Remova os sites e serviços Web instalados no momento.</span><span class="sxs-lookup"><span data-stu-id="6daf3-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="6daf3-191">Removendo os recursos de servidor ou o software do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-192">Remova os SPNs da conta do computador.</span><span class="sxs-lookup"><span data-stu-id="6daf3-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-193">Registre os SPNs na conta do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-194">Siga as etapas para <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrar os SPNs quando você usar um nome de host virtual </a> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6daf3-195">Reconfigure os aplicativos Web e serviços Web.</span><span class="sxs-lookup"><span data-stu-id="6daf3-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="6daf3-196">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6daf3-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6daf3-197">Siga um destes procedimentos, dependendo do método usado para a configuração:</span><span class="sxs-lookup"><span data-stu-id="6daf3-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6daf3-198">Método</span><span class="sxs-lookup"><span data-stu-id="6daf3-198">Method</span></span></th>
<th align="left"><span data-ttu-id="6daf3-199">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6daf3-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6daf3-200">Assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="6daf3-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6daf3-201">Digite a conta do pool de aplicativos no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="6daf3-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="6daf3-202">Cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6daf3-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="6daf3-203">Digite a conta no <code>WebServiceApplicationPoolCredential</code> parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6daf3-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="6daf3-204">Importante</span><span class="sxs-lookup"><span data-stu-id="6daf3-204">Important</span></span></strong><br/><p><span data-ttu-id="6daf3-205">O nome do host inserido deve ser o mesmo nome que o nome do host virtual para o qual você está criando os SPNs.</span><span class="sxs-lookup"><span data-stu-id="6daf3-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="6daf3-206">Além disso, no seu farm da Web, os nomes de host e as credenciais do pool de aplicativos devem ser iguais em todos os servidores que você está configurando.</span><span class="sxs-lookup"><span data-stu-id="6daf3-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="6daf3-207">Quando o MBAM configura os aplicativos da Web, ele tenta registrar os SPNs para você, mas ele só pode fazer isso se você tiver direitos de administrador de domínio no servidor no qual você está instalando o MBAM.</span><span class="sxs-lookup"><span data-stu-id="6daf3-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="6daf3-208">Se você não tiver esses direitos, você pode concluir a configuração, mas será necessário definir os SPNs antes ou depois de configurar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="6daf3-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="6daf3-209">Configurações de filtragem de solicitações necessárias</span><span class="sxs-lookup"><span data-stu-id="6daf3-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="6daf3-210">' Permitir extensões de nome de arquivo não listadas ' é necessário para que o aplicativo opere conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="6daf3-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="6daf3-211">Isso pode ser encontrado ao navegar para o ' Microsoft BitLocker Administration and Monitoring '-> solicitação de filtragem-> editar configurações de recursos.</span><span class="sxs-lookup"><span data-stu-id="6daf3-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="6daf3-212">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6daf3-212">Related topics</span></span>


[<span data-ttu-id="6daf3-213">Preparando seu ambiente para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6daf3-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="6daf3-214">Pré-requisitos para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6daf3-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="6daf3-215">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="6daf3-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6daf3-216">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="6daf3-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="6daf3-217">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6daf3-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



