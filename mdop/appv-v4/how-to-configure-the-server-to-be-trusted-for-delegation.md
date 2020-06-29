---
title: Como configurar o servidor para ser confiável para delegação
description: Como configurar o servidor para ser confiável para delegação
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797187"
---
# <span data-ttu-id="ca13c-103">Como configurar o servidor para ser confiável para delegação</span><span class="sxs-lookup"><span data-stu-id="ca13c-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="ca13c-104">Ao instalar o software do servidor de gerenciamento do Microsoft Application Virtualization (App-V), você pode optar por instalá-lo usando uma arquitetura de sistema distribuído.</span><span class="sxs-lookup"><span data-stu-id="ca13c-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="ca13c-105">Se você instalar o console, o serviço de gerenciamento da Web e o banco de dados em computadores diferentes, será necessário configurar o servidor de serviços de informações da Internet (IIS) para ser confiável para delegação.</span><span class="sxs-lookup"><span data-stu-id="ca13c-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="ca13c-106">Isso é necessário porque o serviço Web de gerenciamento tentará se conectar ao repositório de dados do App-V usando as credenciais do administrador do App-V que está usando o console.</span><span class="sxs-lookup"><span data-stu-id="ca13c-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="ca13c-107">O servidor de banco de dados no qual o repositório de dados está instalado não aceitará as credenciais do administrador do servidor IIS, a menos que o servidor IIS esteja configurado para ser confiável para delegação e, portanto, o serviço Web de gerenciamento não poderá se conectar ao repositório de dados do App-V.</span><span class="sxs-lookup"><span data-stu-id="ca13c-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="ca13c-108">**Observação**  Se você instalar o software do App-V Management Server em um único servidor e colocar o repositório de dados em um servidor separado, há uma situação em que você ainda deve configurar o servidor para ser confiável para delegação, embora o serviço Web de gerenciamento e o console de gerenciamento estejam no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="ca13c-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="ca13c-109">Essa situação ocorre se você precisar se conectar ao serviço Web de gerenciamento no console usando a opção **usar credenciais alternativas** .</span><span class="sxs-lookup"><span data-stu-id="ca13c-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="ca13c-110">O tipo de delegação que você pode usar depende do nível funcional do domínio que você configurou na infraestrutura dos serviços de domínio Active Directory (ADDS).</span><span class="sxs-lookup"><span data-stu-id="ca13c-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="ca13c-111">A tabela a seguir lista os tipos de delegação que podem ser configurados para cada nível funcional de domínio do App-V.</span><span class="sxs-lookup"><span data-stu-id="ca13c-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="ca13c-112">Instruções detalhadas seguem a tabela.</span><span class="sxs-lookup"><span data-stu-id="ca13c-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca13c-113">Nível funcional do domínio</span><span class="sxs-lookup"><span data-stu-id="ca13c-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="ca13c-114">Níveis de delegação disponíveis</span><span class="sxs-lookup"><span data-stu-id="ca13c-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca13c-115">Windows 2000 nativo</span><span class="sxs-lookup"><span data-stu-id="ca13c-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ca13c-116">Sem delegação (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca13c-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="ca13c-117">Delegação irrestrita</span><span class="sxs-lookup"><span data-stu-id="ca13c-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca13c-118">Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca13c-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ca13c-119">Sem delegação (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca13c-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="ca13c-120">¹ de delegação irrestrito</span><span class="sxs-lookup"><span data-stu-id="ca13c-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="ca13c-121">Delegação restrita (usar protocolos somente Kerberos)</span><span class="sxs-lookup"><span data-stu-id="ca13c-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="ca13c-122">Delegação restrita (usar qualquer protocolo de autenticação) ¹</span><span class="sxs-lookup"><span data-stu-id="ca13c-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ca13c-123">¹ não recomendado.</span><span class="sxs-lookup"><span data-stu-id="ca13c-123">¹ Not recommended.</span></span>

## <span data-ttu-id="ca13c-124">Para configurar a delegação irrestrita quando o nível funcional do domínio for Windows 2000 nativo</span><span class="sxs-lookup"><span data-stu-id="ca13c-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="ca13c-125">No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca13c-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="ca13c-126">Clique em **Iniciar**, **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="ca13c-127">Expanda domínio e, em seguida, expanda a pasta computadores.</span><span class="sxs-lookup"><span data-stu-id="ca13c-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="ca13c-128">No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="ca13c-129">Na guia **geral** , verifique se a caixa de seleção **confiar no computador para delegação** está marcada.</span><span class="sxs-lookup"><span data-stu-id="ca13c-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="ca13c-130">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-130">Click **OK**.</span></span>

## <span data-ttu-id="ca13c-131">Para configurar a delegação irrestrita quando o nível funcional do domínio for Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca13c-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="ca13c-132">No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca13c-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="ca13c-133">Clique em **Iniciar**, em **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="ca13c-134">Expanda domínio e expanda a pasta computadores.</span><span class="sxs-lookup"><span data-stu-id="ca13c-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="ca13c-135">No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web, selecione **Propriedades**e, em seguida, clique na guia **delegação** .</span><span class="sxs-lookup"><span data-stu-id="ca13c-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="ca13c-136">Clique para selecionar **confiar neste computador para delegação a qualquer serviço (somente Kerberos)**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="ca13c-137">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-137">Click **OK**.</span></span>

## <span data-ttu-id="ca13c-138">Para configurar a delegação restrita quando o nível funcional do domínio for Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca13c-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="ca13c-139">No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca13c-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="ca13c-140">Clique em **Iniciar**, em **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="ca13c-141">Expanda domínio e, em seguida, expanda a pasta computadores.</span><span class="sxs-lookup"><span data-stu-id="ca13c-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="ca13c-142">No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web, selecione **Propriedades**e, em seguida, clique na guia **delegação** .</span><span class="sxs-lookup"><span data-stu-id="ca13c-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="ca13c-143">Clique para selecionar **confiar neste computador para delegação apenas a serviços especificados**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="ca13c-144">Verifique se a **somente usar Kerberos** está selecionada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="ca13c-145">Clique no botão **Adicionar** .</span><span class="sxs-lookup"><span data-stu-id="ca13c-145">Click the **Add** button.</span></span> <span data-ttu-id="ca13c-146">Na caixa de diálogo **Adicionar serviços** , clique em **usuários ou computadores**e, em seguida, navegue até ou digite o nome do Microsoft SQL Server que tem o repositório de dados App-V e é receber as credenciais de usuários do IIS.</span><span class="sxs-lookup"><span data-stu-id="ca13c-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="ca13c-147">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-147">Click **OK**.</span></span>

7.  <span data-ttu-id="ca13c-148">Na lista **serviços disponíveis** , selecione o serviço MSSQLSvc que lista o número da porta na qual o Microsoft SQL Server está aceitando conexões para o banco de dados do App-V (a porta padrão é 1433).</span><span class="sxs-lookup"><span data-stu-id="ca13c-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="ca13c-149">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-149">Click **OK**.</span></span>

### <span data-ttu-id="ca13c-150">Etapas adicionais para configurar o IIS 7 para delegação restrita</span><span class="sxs-lookup"><span data-stu-id="ca13c-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="ca13c-151">Se você estiver executando o serviço Web de gerenciamento em um servidor do IIS 7, deve completar as etapas a seguir para definir a variável *useAppPoolCredentials* do IIS 7 como true.</span><span class="sxs-lookup"><span data-stu-id="ca13c-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="ca13c-152">Abra uma janela de prompt de comando com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="ca13c-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="ca13c-153">Para abrir uma janela de prompt de comando elevado, clique em **Iniciar**, clique em **todos os programas**, clique em **acessórios**, clique com o botão direito do mouse em **prompt de comando**e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="ca13c-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="ca13c-154">Navegue até%windir%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="ca13c-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="ca13c-155">Digite **appcmd.exe set config-section: System. WebServer/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="ca13c-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





