---
title: Autenticação de usuários finais da MED-V
description: Autenticação de usuários finais da MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799562"
---
# <span data-ttu-id="ec311-103">Autenticação de usuários finais da MED-V</span><span class="sxs-lookup"><span data-stu-id="ec311-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="ec311-104">A autenticação do Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 para usuários finais é um problema de segurança muito importante.</span><span class="sxs-lookup"><span data-stu-id="ec311-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="ec311-105">Nesse contexto, a autenticação se refere a verificar a identidade do usuário final do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ec311-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="ec311-106">A seção a seguir fornece informações e orientação sobre a autenticação do usuário final no MED-V.</span><span class="sxs-lookup"><span data-stu-id="ec311-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="ec311-107">Autenticação de usuário no MED-V</span><span class="sxs-lookup"><span data-stu-id="ec311-107">User Authentication in MED-V</span></span>


<span data-ttu-id="ec311-108">A autenticação no MED-V geralmente ocorre em dois níveis: quando um usuário acessa o MED-V pela primeira vez e sempre que eles alteram a senha.</span><span class="sxs-lookup"><span data-stu-id="ec311-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="ec311-109">Dependendo de como você configurou as configurações do MED-V para autenticação, o usuário final geralmente é solicitado em algum ponto para inserir a senha, seja na primeira vez em que o MED-V é iniciado ou na primeira vez que tentam abrir um aplicativo publicado.</span><span class="sxs-lookup"><span data-stu-id="ec311-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="ec311-110">Há vários aspectos da autenticação de usuários finais que você pode controlar, incluindo os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ec311-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="ec311-111">Se as credenciais que o usuário final insere são armazenadas no Gerenciador de credenciais</span><span class="sxs-lookup"><span data-stu-id="ec311-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="ec311-112">De que maneira o usuário final receberá a opção de inserir e salvar sua senha</span><span class="sxs-lookup"><span data-stu-id="ec311-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="ec311-113">Dependendo do processo preferido da sua empresa para gerenciar a autenticação do usuário final, você pode especificar se o cache de credenciais ocorre para um determinado espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ec311-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="ec311-114">O armazenamento em cache das credenciais de um usuário final é útil porque elas são solicitadas apenas uma vez por sua senha.</span><span class="sxs-lookup"><span data-stu-id="ec311-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="ec311-115">Se o usuário final não tiver permissão para salvar a senha ou se decidir não fazê-lo, todas as vezes que iniciarem uma nova sessão do MED-V, eles devem inseri-la novamente.</span><span class="sxs-lookup"><span data-stu-id="ec311-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="ec311-116">Por exemplo, se o MED-V estiver configurado para ser iniciado quando o usuário final fizer logon no host, mas a autenticação estiver desabilitada, o usuário final será solicitado apenas uma vez durante o logon.</span><span class="sxs-lookup"><span data-stu-id="ec311-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="ec311-117">Nesse caso, as credenciais são válidas até que o usuário final efetue logoff do host.</span><span class="sxs-lookup"><span data-stu-id="ec311-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="ec311-118">Se for necessário, você pode usar o Gerenciador de credenciais para remover todas as credenciais de usuário final armazenadas.</span><span class="sxs-lookup"><span data-stu-id="ec311-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="ec311-119">Por padrão, o armazenamento de credenciais está desabilitado, mas você pode alterar essa configuração por meio de um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="ec311-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="ec311-120">**Durante a criação do pacote do espaço de trabalho do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="ec311-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="ec311-121">Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="ec311-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="ec311-122">**Após a implantação do espaço de trabalho do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="ec311-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="ec311-123">Edite o parâmetro UxCredentialCacheEnabled do cmdlet do MED-V para definir a chave do registro dos serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="ec311-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="ec311-124">Para obter mais informações, consulte a ajuda do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ec311-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="ec311-125">Após a implantação do espaço de trabalho do MED-V, você pode definir sua preferência para a autenticação de usuário final modificando a política de serviços de terminal chamada DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="ec311-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="ec311-126">DisablePasswordSaving controla se a caixa de seleção Salvar senha é exibida na janela de diálogo do cliente RDP e se o prompt de credenciais do MED-V é exibido.</span><span class="sxs-lookup"><span data-stu-id="ec311-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="ec311-127">Veja a seguir o caminho da política da política de serviços de terminal chamada DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="ec311-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="ec311-128">Regedit</span><span class="sxs-lookup"><span data-stu-id="ec311-128">Regedit:</span></span>**

<span data-ttu-id="ec311-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="ec311-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="ec311-130">Observação</span><span class="sxs-lookup"><span data-stu-id="ec311-130">Note</span></span>**  
<span data-ttu-id="ec311-131">As alterações feitas no DisablePasswordSaving só afetam o prompt RDP para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ec311-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="ec311-132">A tabela a seguir lista as maneiras diferentes pelas quais você pode definir suas configurações para o armazenamento de credenciais e os efeitos das diferentes configurações:</span><span class="sxs-lookup"><span data-stu-id="ec311-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ec311-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ec311-133">Value</span></span></th>
<th align="left"><span data-ttu-id="ec311-134">Configuração</span><span class="sxs-lookup"><span data-stu-id="ec311-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="ec311-135">Resultado</span><span class="sxs-lookup"><span data-stu-id="ec311-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec311-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="ec311-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="ec311-137">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="ec311-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ec311-138">O prompt do MED-V é apresentado e uma caixa de seleção para aceitar está disponível e desmarcada.</span><span class="sxs-lookup"><span data-stu-id="ec311-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="ec311-139">Se o usuário final marcar a caixa de seleção, as credenciais serão armazenadas em cache para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="ec311-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="ec311-140">O usuário final também tem a vantagem de ser avisado apenas quando a senha expira.</span><span class="sxs-lookup"><span data-stu-id="ec311-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ec311-141">Se o usuário final não marcar a caixa de seleção, o prompt do cliente de conexão de área de trabalho remota (RDC) será apresentado em vez do prompt do MED-V, e a caixa de seleção a ser aceita será desmarcada.</span><span class="sxs-lookup"><span data-stu-id="ec311-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="ec311-142">Se o usuário final marcar a caixa de seleção, a credencial do cliente RDC será armazenada para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="ec311-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ec311-143">Importante</span><span class="sxs-lookup"><span data-stu-id="ec311-143">Important</span></span></strong><br/><p><span data-ttu-id="ec311-144">A RDC não valida as credenciais quando o usuário termina de inseri-las.</span><span class="sxs-lookup"><span data-stu-id="ec311-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="ec311-145">Se o usuário final armazenar as credenciais em cache por meio do prompt de RDC, há um risco de que credenciais incorretas possam ser armazenadas.</span><span class="sxs-lookup"><span data-stu-id="ec311-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="ec311-146">Nesse caso, as credenciais incorretas devem ser excluídas no Gerenciador de credenciais do Windows.</span><span class="sxs-lookup"><span data-stu-id="ec311-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ec311-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="ec311-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="ec311-148">Habilitado</span><span class="sxs-lookup"><span data-stu-id="ec311-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="ec311-149">Observação</span><span class="sxs-lookup"><span data-stu-id="ec311-149">Note</span></span></strong><br/><p><span data-ttu-id="ec311-150">Essa configuração é mais segura porque não permite que as credenciais do usuário final sejam armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="ec311-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ec311-151">Por padrão, a instalação do MED-V define uma chave do registro no convidado para suprimir o prompt "senha sobre para expirar".</span><span class="sxs-lookup"><span data-stu-id="ec311-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="ec311-152">O usuário final é solicitado apenas por uma alteração de senha no host.</span><span class="sxs-lookup"><span data-stu-id="ec311-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="ec311-153">As credenciais que são atualizadas no host são passadas para o convidado.</span><span class="sxs-lookup"><span data-stu-id="ec311-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="ec311-154">Tenha</span><span class="sxs-lookup"><span data-stu-id="ec311-154">Caution</span></span>**  
<span data-ttu-id="ec311-155">Se você usar a política de grupo em seu ambiente, saiba que ela pode substituir a chave do registro que faz com que os prompts de senha do convidado reapareçam.</span><span class="sxs-lookup"><span data-stu-id="ec311-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="ec311-156">Questões de segurança com a autenticação</span><span class="sxs-lookup"><span data-stu-id="ec311-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="ec311-157">Embora o armazenamento em cache das credenciais do usuário final forneça a melhor experiência do usuário, você deve estar ciente dos riscos envolvidos.</span><span class="sxs-lookup"><span data-stu-id="ec311-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="ec311-158">Quando o cache de credenciais está habilitado, a credencial do domínio do usuário final é armazenada em um formato reversível dentro do Gerenciador de credenciais do Windows.</span><span class="sxs-lookup"><span data-stu-id="ec311-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="ec311-159">Como resultado, um invasor pode gravar uma ferramenta que é executada como um processo no nível do sistema ou um processo do usuário final e recupera as credenciais do usuário final.</span><span class="sxs-lookup"><span data-stu-id="ec311-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="ec311-160">Você só pode diminuir esse risco Configurando DisablePasswordSaving como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="ec311-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="ec311-161">Essa mesma preocupação existe quando a autenticação do MED-V está desabilitada, mas a configuração de política dos serviços de terminal está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ec311-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="ec311-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec311-162">Related topics</span></span>


[<span data-ttu-id="ec311-163">Práticas recomendadas de segurança para operações da MED-V</span><span class="sxs-lookup"><span data-stu-id="ec311-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









