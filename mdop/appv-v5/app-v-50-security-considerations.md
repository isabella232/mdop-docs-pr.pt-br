---
title: Considerações de segurança do App-V 5.0
description: Considerações de segurança do App-V 5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796592"
---
# <span data-ttu-id="ac93f-103">Considerações de segurança do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ac93f-103">App-V 5.0 Security Considerations</span></span>


<span data-ttu-id="ac93f-104">Este tópico contém uma breve visão geral das contas e dos grupos, dos arquivos de log e outras considerações relacionadas à segurança do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for App-V 5.0.</span></span>

**<span data-ttu-id="ac93f-105">Importante</span><span class="sxs-lookup"><span data-stu-id="ac93f-105">Important</span></span>**  
<span data-ttu-id="ac93f-106">O App-V 5,0 não é um produto de segurança e não fornece garantias para um ambiente seguro.</span><span class="sxs-lookup"><span data-stu-id="ac93f-106">App-V 5.0 is not a security product and does not provide any guarantees for a secure environment.</span></span>



## <span data-ttu-id="ac93f-107">O recurso PackageStoreAccessControl (PSAC) foi preterido</span><span class="sxs-lookup"><span data-stu-id="ac93f-107">PackageStoreAccessControl (PSAC) feature has been deprecated</span></span>


<span data-ttu-id="ac93f-108">Em vigor a partir de junho de 2014, o PackageStoreAccessControl (PSAC) que foi introduzido no Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) foi preterido em ambientes com um único usuário e vários usuários.</span><span class="sxs-lookup"><span data-stu-id="ac93f-108">Effective as of June, 2014, the PackageStoreAccessControl (PSAC) feature that was introduced in Microsoft Application Virtualization (App-V) 5.0 Service Pack 2 (SP2) has been deprecated in both single-user and multi-user environments.</span></span>

## <span data-ttu-id="ac93f-109">Considerações gerais sobre segurança</span><span class="sxs-lookup"><span data-stu-id="ac93f-109">General security considerations</span></span>


**<span data-ttu-id="ac93f-110">Compreender os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="ac93f-110">Understand the security risks.</span></span>** <span data-ttu-id="ac93f-111">O risco mais sério para o App-V 5,0 é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia então reconfigurar dados de chave nos clientes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-111">The most serious risk to App-V 5.0 is that its functionality could be hijacked by an unauthorized user who could then reconfigure key data on App-V 5.0 clients.</span></span> <span data-ttu-id="ac93f-112">A perda da funcionalidade do App-V 5,0 por um curto período de tempo devido a um ataque de negação de serviço geralmente não teria um impacto catastrófico.</span><span class="sxs-lookup"><span data-stu-id="ac93f-112">The loss of App-V 5.0 functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="ac93f-113">**Proteja seus computadores fisicamente**.</span><span class="sxs-lookup"><span data-stu-id="ac93f-113">**Physically secure your computers**.</span></span> <span data-ttu-id="ac93f-114">A segurança está incompleta sem segurança física.</span><span class="sxs-lookup"><span data-stu-id="ac93f-114">Security is incomplete without physical security.</span></span> <span data-ttu-id="ac93f-115">Qualquer pessoa com acesso físico a um servidor do App-V 5,0 pode atacar potencialmente toda a base de clientes.</span><span class="sxs-lookup"><span data-stu-id="ac93f-115">Anyone with physical access to an App-V 5.0 server could potentially attack the entire client base.</span></span> <span data-ttu-id="ac93f-116">Qualquer ataque físico potencial deve ser considerado de alto risco e diminuído apropriadamente.</span><span class="sxs-lookup"><span data-stu-id="ac93f-116">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="ac93f-117">Os servidores do App-V 5,0 devem ser armazenados em uma sala de servidor fisicamente seguro com acesso controlado.</span><span class="sxs-lookup"><span data-stu-id="ac93f-117">App-V 5.0 servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="ac93f-118">Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.</span><span class="sxs-lookup"><span data-stu-id="ac93f-118">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="ac93f-119">**Aplicar as atualizações de segurança mais recentes a todos os computadores**.</span><span class="sxs-lookup"><span data-stu-id="ac93f-119">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="ac93f-120">Para se manter informado sobre as atualizações mais recentes dos sistemas operacionais, do Microsoft SQL Server e do App-V 5,0, assine o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="ac93f-120">To stay informed about the latest updates for operating systems, Microsoft SQL Server, and App-V 5.0, subscribe to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="ac93f-121">**Use senhas fortes ou frases secretas**.</span><span class="sxs-lookup"><span data-stu-id="ac93f-121">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="ac93f-122">Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do App-V 5,0 e do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-122">Always use strong passwords with 15 or more characters for all App-V 5.0 and App-V 5.0 administrator accounts.</span></span> <span data-ttu-id="ac93f-123">Nunca use senhas em branco.</span><span class="sxs-lookup"><span data-stu-id="ac93f-123">Never use blank passwords.</span></span> <span data-ttu-id="ac93f-124">Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="ac93f-124">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="ac93f-125">Contas e grupos no App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ac93f-125">Accounts and groups in App-V 5.0</span></span>


<span data-ttu-id="ac93f-126">Uma prática recomendada para o gerenciamento de contas de usuários é criar grupos globais de domínio e adicionar contas de usuário a eles.</span><span class="sxs-lookup"><span data-stu-id="ac93f-126">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="ac93f-127">Em seguida, adicione as contas globais do domínio aos grupos locais do App-V 5,0 nos servidores App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-127">Then, add the domain global accounts to the necessary App-V 5.0 local groups on the App-V 5.0 servers.</span></span>

**<span data-ttu-id="ac93f-128">Observação</span><span class="sxs-lookup"><span data-stu-id="ac93f-128">Note</span></span>**  
<span data-ttu-id="ac93f-129">As contas de computador cliente App-V que precisam se conectar ao servidor de publicação devem fazer parte do grupo local de **usuários** do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="ac93f-129">App-V client computer accounts that need to connect to the publishing server must be part of the publishing server’s **Users** local group.</span></span> <span data-ttu-id="ac93f-130">Por padrão, todos os computadores no domínio fazem parte do grupo **usuários autorizados** , que faz parte do grupo local **usuários** .</span><span class="sxs-lookup"><span data-stu-id="ac93f-130">By default, all computers in the domain are part of the **Authorized Users** group, which is part of the **Users** local group.</span></span>



### <a href="" id="-------------app-v-5-0-server-security"></a> <span data-ttu-id="ac93f-131">Segurança do App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="ac93f-131">App-V 5.0 server security</span></span>

<span data-ttu-id="ac93f-132">Nenhum grupo é criado automaticamente durante a configuração do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-132">No groups are created automatically during App-V 5.0 Setup.</span></span> <span data-ttu-id="ac93f-133">Você deve criar os seguintes grupos globais dos serviços de domínio Active Directory para gerenciar operações do servidor do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-133">You should create the following Active Directory Domain Services global groups to manage App-V 5.0 server operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ac93f-134">Nome do grupo</span><span class="sxs-lookup"><span data-stu-id="ac93f-134">Group name</span></span></th>
<th align="left"><span data-ttu-id="ac93f-135">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ac93f-135">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac93f-136">Grupo de administração do App-V Management</span><span class="sxs-lookup"><span data-stu-id="ac93f-136">App-V Management Admin group</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac93f-137">Usado para gerenciar o servidor de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-137">Used to manage the App-V 5.0 management server.</span></span> <span data-ttu-id="ac93f-138">Esse grupo é criado durante a instalação do servidor de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-138">This group is created during the App-V 5.0 Management Server installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ac93f-139">Importante</span><span class="sxs-lookup"><span data-stu-id="ac93f-139">Important</span></span></strong><br/><p><span data-ttu-id="ac93f-140">Não há nenhum método para criar o grupo usando o console de gerenciamento após concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="ac93f-140">There is no method to create the group using the management console after you have completed the installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac93f-141">Leitura/gravação de banco de dados para conta de serviço de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ac93f-141">Database read/write for Management Service account</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac93f-142">Fornece acesso de leitura/gravação ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac93f-142">Provides read/write access to the management database.</span></span> <span data-ttu-id="ac93f-143">Essa conta deve ser criada durante a instalação do banco de dados de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-143">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac93f-144">Conta de administrador de instalação do App-V Management Service</span><span class="sxs-lookup"><span data-stu-id="ac93f-144">App-V Management Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ac93f-145">Observação</span><span class="sxs-lookup"><span data-stu-id="ac93f-145">Note</span></span></strong><br/><p><span data-ttu-id="ac93f-146">Isso só será necessário se o banco de dados de gerenciamento estiver sendo instalado separadamente do serviço.</span><span class="sxs-lookup"><span data-stu-id="ac93f-146">This is only required if management database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ac93f-147">Fornece acesso público à tabela de versão de esquema no banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac93f-147">Provides public access to schema-version table in management database.</span></span> <span data-ttu-id="ac93f-148">Essa conta deve ser criada durante a instalação do banco de dados de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-148">This account should be created during the App-V 5.0 management database installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac93f-149">Conta de administrador de instalação do App-V Reporting Service</span><span class="sxs-lookup"><span data-stu-id="ac93f-149">App-V Reporting Service install admin account</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ac93f-150">Observação</span><span class="sxs-lookup"><span data-stu-id="ac93f-150">Note</span></span></strong><br/><p><span data-ttu-id="ac93f-151">Isso só é necessário se o banco de dados de relatórios estiver sendo instalado separadamente do serviço.</span><span class="sxs-lookup"><span data-stu-id="ac93f-151">This is only required if reporting database is being installed separately from the service.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ac93f-152">Acesso público à tabela de versão de esquema em banco de dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="ac93f-152">Public access to schema-version table in reporting database.</span></span> <span data-ttu-id="ac93f-153">Essa conta deve ser criada durante a instalação do banco de dados de relatórios do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac93f-153">This account should be created during the App-V 5.0 reporting database installation.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ac93f-154">Considere as seguintes informações adicionais:</span><span class="sxs-lookup"><span data-stu-id="ac93f-154">Consider the following additional information:</span></span>

-   <span data-ttu-id="ac93f-155">Acesso aos compartilhamentos de pacote-se houver um compartilhamento no mesmo computador que o servidor de gerenciamento, o serviço de **rede** requer acesso de leitura ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ac93f-155">Access to the package shares - If a share exists on the same computer as the management Server, the **Network** service requires read access to the share.</span></span> <span data-ttu-id="ac93f-156">Além disso, cada computador cliente App-V deve ter acesso de leitura ao compartilhamento de pacote.</span><span class="sxs-lookup"><span data-stu-id="ac93f-156">In addition, each App-V client computer must have read access to the package share.</span></span>

    **<span data-ttu-id="ac93f-157">Observação</span><span class="sxs-lookup"><span data-stu-id="ac93f-157">Note</span></span>**  
    <span data-ttu-id="ac93f-158">Em versões anteriores do App-V, o compartilhamento de pacote era chamado de compartilhamento de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ac93f-158">In previous versions of App-V, package share was referred to as content share.</span></span>



-   <span data-ttu-id="ac93f-159">Registrar servidores de publicação com o servidor de gerenciamento-um servidor de publicação deve ser registrado com o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac93f-159">Registering publishing servers with Management Server - A publishing server must be registered with the Management server.</span></span> <span data-ttu-id="ac93f-160">Por exemplo, ele deve ser adicionado ao banco de dados para que as contas do computador do servidor de publicação possam chamar a API do serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac93f-160">For example, it must be added to the database, so that the Publishing server machine accounts are able to call into the Management service API.</span></span>

### <a href="" id="-------------app-v-5-0-package-security"></a> <span data-ttu-id="ac93f-161">Segurança do pacote do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ac93f-161">App-V 5.0 package security</span></span>

<span data-ttu-id="ac93f-162">Os itens a seguir o ajudarão a planejar a segurança para garantir que os pacotes virtualizados sejam seguros.</span><span class="sxs-lookup"><span data-stu-id="ac93f-162">The following will help you plan how to ensure that virtualized packages are secure.</span></span>

-   <span data-ttu-id="ac93f-163">Se um instalador do aplicativo aplicar uma ACL (lista de controle de acesso) a um arquivo ou diretório, essa ACL não será mantida no pacote.</span><span class="sxs-lookup"><span data-stu-id="ac93f-163">If an application installer applies an access control list (ACL) to a file or directory, then that ACL is not persisted in the package.</span></span> <span data-ttu-id="ac93f-164">Quando o pacote é implantado, se o arquivo ou diretório for modificado por um usuário, ele herdará a ACL no **% USERPROFILE%** ou herdará a ACL do diretório do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ac93f-164">When the package is deployed, if the file or directory is modified by a user it will either inherit the ACL in the **%userprofile%** or inherit the ACL of the target computer’s directory.</span></span> <span data-ttu-id="ac93f-165">O primeiro caso ocorre se o arquivo ou diretório não existir em um local do sistema de arquivos virtual; o último caso ocorre se o arquivo ou diretório existir em um local do sistema de arquivos virtual, por exemplo, **% windir%**.</span><span class="sxs-lookup"><span data-stu-id="ac93f-165">The former case occurs if the file or directory does not exist in a virtual file system location; the latter case occurs if the file or directory exists in a virtual file system location, for example **%windir%**.</span></span>

## <a href="" id="---------app-v-5-0-log-files"></a> <span data-ttu-id="ac93f-166">Arquivos de log do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ac93f-166">App-V 5.0 log files</span></span>


<span data-ttu-id="ac93f-167">Durante a instalação do App-V 5,0, os arquivos de log de instalação são criados na pasta **% Temp%** do usuário da instalação.</span><span class="sxs-lookup"><span data-stu-id="ac93f-167">During App-V 5.0 Setup, setup log files are created in the **%temp%** folder of the installing user.</span></span>
