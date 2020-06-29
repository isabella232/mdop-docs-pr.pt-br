---
title: Considerações de segurança do UE-V 1.0
description: Considerações de segurança do UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799384"
---
# <span data-ttu-id="a1dc2-103">Considerações de segurança do UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="a1dc2-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="a1dc2-104">Este tópico contém uma breve visão geral de contas e grupos, arquivos de log e outras considerações relacionadas à segurança para o Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="a1dc2-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="a1dc2-105">Para obter mais informações, siga os links que são fornecidos aqui.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="a1dc2-106">Considerações de segurança para a configuração de UE-V</span><span class="sxs-lookup"><span data-stu-id="a1dc2-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="a1dc2-107">Ao criar o compartilhamento de armazenamento configurações, limite o acesso de compartilhamento aos usuários que precisam de acesso.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="a1dc2-108">Como os pacotes de configurações podem conter informações pessoais, você deve ter cuidado para protegê-los assim que possível.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="a1dc2-109">Em geral, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-109">In general, do the following:</span></span>

-   <span data-ttu-id="a1dc2-110">Restrinja o compartilhamento apenas aos usuários que precisam de acesso.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="a1dc2-111">Crie um grupo de segurança para usuários que tenham pastas redirecionadas em um determinado compartilhamento e limite o acesso somente a esses usuários.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="a1dc2-112">Ao criar o compartilhamento, oculte o compartilhamento colocando $ após o nome do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="a1dc2-113">Isso ocultará o compartilhamento de navegadores casuais, e o compartilhamento não será visível em meus locais de rede.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="a1dc2-114">Forneça aos usuários a quantidade mínima de permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="a1dc2-115">As permissões necessárias são mostradas nas tabelas abaixo.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="a1dc2-116">Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta de local de armazenamento de configuração:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="a1dc2-117">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="a1dc2-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="a1dc2-118">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="a1dc2-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="a1dc2-119">Todos</span><span class="sxs-lookup"><span data-stu-id="a1dc2-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a1dc2-120">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="a1dc2-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="a1dc2-121">Grupo de segurança da UE-V</span><span class="sxs-lookup"><span data-stu-id="a1dc2-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="a1dc2-122">Controle total</span><span class="sxs-lookup"><span data-stu-id="a1dc2-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="a1dc2-123">Usar servidores Windows Server 2003 ou posteriores para hospedar compartilhamentos de arquivos redirecionados</span><span class="sxs-lookup"><span data-stu-id="a1dc2-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="a1dc2-124">Os arquivos de pacote de configurações do usuário contêm informações pessoais que são transferidas entre o computador cliente e o servidor que armazena os pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="a1dc2-125">Por isso, você deve garantir que os dados sejam protegidos enquanto trafegam pela rede.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="a1dc2-126">Os dados das configurações do usuário são vulneráveis a essas possíveis ameaças: a interceptação dos dados durante a transmissão pela rede; adulteração dos dados durante a transmissão pela rede; e falsificação do servidor que hospeda os dados.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="a1dc2-127">Vários recursos do Windows Server 2003 e versões mais recentes podem ajudar a proteger os dados do usuário:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="a1dc2-128">**Kerberos** -Kerberos é padrão em todas as versões do Windows 2000 e windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="a1dc2-129">O Kerberos garante o mais alto nível de segurança aos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="a1dc2-130">O NTLM autentica somente o cliente; O Kerberos autentica o servidor e o cliente.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="a1dc2-131">Quando o NTLM for usado, o cliente não saberá se o servidor é válido.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="a1dc2-132">Isso é particularmente importante se o cliente estiver trocando arquivos pessoais com o servidor, como é o caso dos perfis de roaming.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="a1dc2-133">O Kerberos oferece melhor segurança do que o NTLM.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="a1dc2-134">O Kerberos não está disponível no Windows NT versão 4,0 ou sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="a1dc2-135">**IPSec** – o IP Security Protocol (IPSec) oferece autenticação, integridade e criptografia de dados no nível da rede.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="a1dc2-136">O IPsec garante o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="a1dc2-137">Os dados em roaming são seguros da modificação de dados durante a rota.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="a1dc2-138">Os dados em roaming estão protegidos contra interceptação, visualização ou cópia.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="a1dc2-139">Os dados em roaming são seguros de serem acessados por partes não autenticadas.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="a1dc2-140">**Assinatura SMB** – o protocolo de autenticação SMB (Server Message Block) dá suporte à autenticação de mensagens que impede ataques de mensagem ativa e "Man-in-the-middle".</span><span class="sxs-lookup"><span data-stu-id="a1dc2-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="a1dc2-141">A assinatura SMB fornece essa autenticação colocando uma assinatura digital em cada SMB.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="a1dc2-142">A assinatura digital é então verificada pelo cliente e pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="a1dc2-143">Para usar a assinatura SMB, primeiro você deve habilitá-la ou exigi-la no cliente SMB e no servidor SMB.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="a1dc2-144">Observe que a assinatura SMB impõe uma penalidade de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="a1dc2-145">Ele não consome mais largura de banda de rede, mas usa mais ciclos de CPU no lado do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="a1dc2-146">Sempre usar o sistema de arquivos NTFS para volumes que contêm dados de usuários</span><span class="sxs-lookup"><span data-stu-id="a1dc2-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="a1dc2-147">Para a configuração mais segura, configure os servidores que hospedam os arquivos de configurações do UE-V para usar o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="a1dc2-148">Diferentemente do FAT, o NTFS dá suporte a listas de controle de acesso discricional (DACLs) e listas de controle de acesso do sistema (SACLs).</span><span class="sxs-lookup"><span data-stu-id="a1dc2-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="a1dc2-149">As DACLs e SACLs controlam quem pode realizar operações em um arquivo e quais eventos dispararão o log de ações executadas em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="a1dc2-150">Não confie no EFS para criptografar os arquivos dos usuários quando transmitidos pela rede</span><span class="sxs-lookup"><span data-stu-id="a1dc2-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="a1dc2-151">Quando você usa o sistema de arquivos com criptografia (EFS) para criptografar arquivos em um servidor remoto, os dados criptografados não são criptografados durante o trânsito pela rede; Ele só se torna criptografado quando armazenado em disco.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="a1dc2-152">As exceções a isso são quando o sistema inclui segurança de protocolo Internet (IPsec) ou criação e controle de versão distribuídas (WebDAV).</span><span class="sxs-lookup"><span data-stu-id="a1dc2-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="a1dc2-153">O IPsec criptografa dados enquanto eles são transportados por uma rede TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="a1dc2-154">Se o arquivo for criptografado antes de ser copiado ou movido para uma pasta WebDAV em um servidor, ele permanecerá criptografado durante a transmissão e enquanto estiver armazenado no servidor.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="a1dc2-155">Criptografar o cache de arquivos offline</span><span class="sxs-lookup"><span data-stu-id="a1dc2-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="a1dc2-156">Por padrão, o cache de arquivos offline é protegido em partições NTFS por ACLs, mas a criptografia do cache melhora ainda mais a segurança em um computador local.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="a1dc2-157">Por padrão, o cache no computador local não é criptografado, portanto, os arquivos criptografados armazenados em cache da rede não serão criptografados no computador local.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="a1dc2-158">Isso pode representar um risco de segurança em alguns ambientes.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="a1dc2-159">Quando a criptografia está habilitada, todos os arquivos no cache de arquivos offline são criptografados.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="a1dc2-160">Isso inclui a criptografia de arquivos existentes, bem como os arquivos que são adicionados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="a1dc2-161">A cópia em cache no computador local é afetada, mas a cópia de rede associada não está.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="a1dc2-162">O cache pode ser criptografado de uma destas duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="a1dc2-163">Por meio da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-163">Via Group Policy.</span></span> <span data-ttu-id="a1dc2-164">-Habilite a configuração **criptografar o cache de arquivos offline** , localizada em arquivos do computador Configuration\\Administrative Templates\\Network\\Offline, no editor de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="a1dc2-165">Manualmente.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-165">Manually.</span></span> <span data-ttu-id="a1dc2-166">-Selecione Ferramentas e, em seguida, clique em opções de pasta no menu de comando do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="a1dc2-167">Selecione a guia arquivos offline e, em seguida, marque a caixa de seleção **criptografar arquivos offline para proteger os dados** .</span><span class="sxs-lookup"><span data-stu-id="a1dc2-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="a1dc2-168">Permitir que o UE-V Agent Crie pastas para cada usuário</span><span class="sxs-lookup"><span data-stu-id="a1dc2-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="a1dc2-169">Para garantir que o UE-V funcione de maneira ideal, crie somente o compartilhamento de raiz no servidor e deixe que o UE-V Agent crie as pastas para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="a1dc2-170">O UE-V criará essas pastas de usuário com a segurança adequada.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="a1dc2-171">Esta configuração de permissão permite que os usuários criem pastas para armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="a1dc2-172">O UE-V Agent cria e protege uma pasta settingspackage durante a execução no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="a1dc2-173">O usuário recebe controle total para a pasta settingspackage.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="a1dc2-174">Outros usuários não herdam o acesso a essa pasta.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="a1dc2-175">Você não precisa criar e proteger diretórios de usuário individuais.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="a1dc2-176">Isso será feito automaticamente pelo agente que é executado no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="a1dc2-177">Observação</span><span class="sxs-lookup"><span data-stu-id="a1dc2-177">Note</span></span>**  
<span data-ttu-id="a1dc2-178">É possível configurar mais segurança quando um Windows Server é utilizado para o compartilhamento de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="a1dc2-179">O UE-V pode ser configurado para verificar se o grupo do administrador local ou o usuário atual é o proprietário da pasta na qual os pacotes de configurações são armazenados.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="a1dc2-180">Para habilitar a segurança adicional, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a1dc2-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="a1dc2-181">Adicione uma chave do registro REG \ _DWORD chamada "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="a1dc2-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="a1dc2-182">Defina o valor da chave do registro como 1.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-182">Set registry key value to 1.</span></span>

<span data-ttu-id="a1dc2-183">Quando essa configuração está implementada, o UE-V Agent verifica se o grupo do administrador local ou o usuário atual é o proprietário da pasta settingspackage.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="a1dc2-184">Se não for, o UE-V Agent não permitirá acesso à pasta.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="a1dc2-185">Se você deve criar pastas para os usuários e garantir que você tenha as permissões corretas definidas.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="a1dc2-186">É altamente recomendável que você não crie pastas e, em vez disso, permita que o UE-V Agent crie a pasta para o usuário.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="a1dc2-187">Garantir que as permissões corretas sejam definidas ao armazenar as configurações de UE-V no diretório base de um usuário</span><span class="sxs-lookup"><span data-stu-id="a1dc2-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="a1dc2-188">Se você redirecionar as configurações do UE-V para o diretório base de um usuário, certifique-se de que as permissões no diretório base do usuário sejam definidas apropriadamente para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="a1dc2-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="a1dc2-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1dc2-189">Related topics</span></span>


[<span data-ttu-id="a1dc2-190">Segurança e privacidade do UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="a1dc2-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









