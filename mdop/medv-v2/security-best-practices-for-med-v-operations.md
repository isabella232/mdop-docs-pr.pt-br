---
title: Práticas recomendadas de segurança para operações da MED-V
description: Práticas recomendadas de segurança para operações da MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799664"
---
# <span data-ttu-id="08eae-103">Práticas recomendadas de segurança para operações da MED-V</span><span class="sxs-lookup"><span data-stu-id="08eae-103">Security Best Practices for MED-V Operations</span></span>


<span data-ttu-id="08eae-104">Como um administrador autorizado, você é responsável por proteger as informações dos usuários e manter a segurança da sua organização durante e após a implantação de espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="08eae-104">As an authorized administrator, you are responsible to protect the information of the users and maintain security of your organization during and after the deployment of MED-V workspaces.</span></span> <span data-ttu-id="08eae-105">Em particular, considere os seguintes problemas.</span><span class="sxs-lookup"><span data-stu-id="08eae-105">In particular, consider the following issues.</span></span>

<span data-ttu-id="08eae-106">**Personalizando o Internet Explorer no espaço de trabalho do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="08eae-106">**Customizing Internet Explorer in the MED-V workspace**.</span></span> <span data-ttu-id="08eae-107">Versões anteriores do sistema operacional Windows e do Internet Explorer não são tão seguras quanto as versões atuais.</span><span class="sxs-lookup"><span data-stu-id="08eae-107">Earlier versions of the Windows operating system and of Internet Explorer are not as secure as current versions.</span></span> <span data-ttu-id="08eae-108">Portanto, o Internet Explorer no espaço de trabalho do MED-V está configurado para impedir a navegação e outras atividades que possam representar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="08eae-108">Therefore, Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span> <span data-ttu-id="08eae-109">Além disso, a configuração de zona de segurança da Internet para o Internet Explorer no espaço de trabalho do MED-V é definida como o nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="08eae-109">In addition, the Internet security zone setting for Internet Explorer in the MED-V workspace is set to the highest level.</span></span> <span data-ttu-id="08eae-110">Por padrão, ambas as configurações são definidas no pacote do espaço de trabalho do MED-V quando você cria seu pacote de espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="08eae-110">By default, both of these configurations are set in the MED-V Workspace Packager when you create your MED-V workspace package.</span></span>

<span data-ttu-id="08eae-111">Usando o kit de administração do Internet Explorer (IEAK) ou alterando os padrões no pacote de espaço de trabalho do MED-V, você pode personalizar o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="08eae-111">By using Internet Explorer Administration Kit (IEAK) or by changing the defaults in the MED-V Workspace Packager, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="08eae-112">No entanto, observe que, se você personalizar o Internet Explorer no espaço de trabalho do MED-V de forma a torná-lo menos seguro, você poderá expor sua organização a esses riscos de segurança que estão presentes em versões mais antigas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="08eae-112">However, realize that if you customize Internet Explorer in the MED-V workspace in such a way as to make it less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span>

<span data-ttu-id="08eae-113">De uma perspectiva de segurança, as práticas recomendadas para o gerenciamento do Internet Explorer no espaço de trabalho do MED-V são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="08eae-113">From a security perspective, best practices for managing Internet Explorer in the MED-V workspace are as follows:</span></span>

-   <span data-ttu-id="08eae-114">Ao criar seu pacote de espaço de trabalho do MED-V, deixe os padrões definidos para que o Internet Explorer no espaço de trabalho do MED-V seja configurado para impedir a navegação e outras atividades que possam representar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="08eae-114">When creating your MED-V workspace package, leave the defaults set so that Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span>

-   <span data-ttu-id="08eae-115">Ao criar seu pacote de espaço de trabalho do MED-V, deixe os padrões definidos para que a configuração de segurança da zona de segurança da Internet permaneça no nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="08eae-115">When creating your MED-V workspace package, leave the defaults set so that the security setting for the Internet security zone remains at the highest level.</span></span>

-   <span data-ttu-id="08eae-116">Configure seu proxy corporativo ou o supervisor de conteúdo do Internet Explorer para bloquear domínios fora da intranet da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="08eae-116">Configure your enterprise proxy or Internet Explorer Content Advisor to block domains that are outside your company’s intranet.</span></span>

**<span data-ttu-id="08eae-117">Configurar um espaço de trabalho do MED-V para todos os usuários em um computador compartilhado.</span><span class="sxs-lookup"><span data-stu-id="08eae-117">Configuring a MED-V workspace for all users on a shared computer.</span></span>** <span data-ttu-id="08eae-118">Ao configurar um espaço de trabalho do MED-V para que ele possa ser acessado por todos os usuários em um computador compartilhado, perceba que a máquina virtual convidada (VHD) é inserida em um local que concede acesso de leitura e gravação a todos os usuários desse sistema.</span><span class="sxs-lookup"><span data-stu-id="08eae-118">When configuring a MED-V workspace so that it can be accessed by all users on a shared computer, realize that the guest virtual machine (VHD) is put in a location that gives Read and Write access to all users on that system.</span></span>

**<span data-ttu-id="08eae-119">Configurando uma conta proxy para ingressar no domínio.</span><span class="sxs-lookup"><span data-stu-id="08eae-119">Configuring a proxy account for domain joining.</span></span>** <span data-ttu-id="08eae-120">Ao configurar uma conta proxy para ingressar em máquinas virtuais no domínio, você deve saber que é possível que um usuário final obtenha as credenciais da conta proxy.</span><span class="sxs-lookup"><span data-stu-id="08eae-120">When configuring a proxy account for joining virtual machines to the domain, you must know that it is possible for an end user to obtain the proxy account credentials.</span></span> <span data-ttu-id="08eae-121">Portanto, devem ser tomadas precauções necessárias, como a limitação de direitos de usuário da conta, para impedir que um usuário final use as credenciais para causar danos.</span><span class="sxs-lookup"><span data-stu-id="08eae-121">Thus, necessary precautions must be taken, such as limiting account user rights, to prevent an end user from using the credentials for causing harm.</span></span>

**<span data-ttu-id="08eae-122">Configuração de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="08eae-122">Sysprep Configuration.</span></span>** <span data-ttu-id="08eae-123">Embora o arquivo Sysprep. inf seja criptografado por padrão, seu conteúdo pode ser descriptografado e lido por qualquer usuário final determinado que pode fazer logon com êxito na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08eae-123">Although the Sysprep.inf file is encrypted by default, its contents can be decrypted and read by any determined end user who can successfully log on to the virtual machine.</span></span> <span data-ttu-id="08eae-124">Isso gera problemas de segurança porque o arquivo Sysprep. inf pode conter credenciais, além de uma chave de produto do Windows.</span><span class="sxs-lookup"><span data-stu-id="08eae-124">This raises security concerns because the Sysprep.inf file can contain credentials in addition to a Windows product key.</span></span>

<span data-ttu-id="08eae-125">Você pode diminuir esse risco Configurando uma conta limitada para ingressar em máquinas virtuais no domínio e especificando as credenciais dessa conta ao configurar o Sysprep.</span><span class="sxs-lookup"><span data-stu-id="08eae-125">You can lessen this risk by setting up a limited account for joining virtual machines to the domain and specifying the credentials for that account when configuring Sysprep.</span></span> <span data-ttu-id="08eae-126">Como alternativa, você também pode configurar o Sysprep e a primeira vez que o programa de instalação seja executado no modo **assistido** e exigir que os usuários finais forneçam suas credenciais para ingressar na máquina virtual no domínio.</span><span class="sxs-lookup"><span data-stu-id="08eae-126">Alternately, you can also configure Sysprep and first time setup to run in **Attended** mode and require end users to provide their credentials for joining the virtual machine to the domain.</span></span>

<span data-ttu-id="08eae-127">Uma prática recomendada do MED-V é especificar que o FtsCompletion.exe seja executado em uma conta que conceda aos direitos de usuário final para se conectar ao convidado por meio do cliente de conexão de área de trabalho remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="08eae-127">A MED-V best practice is to specify that FtsCompletion.exe is run under an account that gives the end user rights to connect to the guest through the Remote Desktop Connection (RDC) Client.</span></span>

**<span data-ttu-id="08eae-128">Autenticação de usuário final.</span><span class="sxs-lookup"><span data-stu-id="08eae-128">End-user authentication.</span></span>** <span data-ttu-id="08eae-129">Habilitar o armazenamento em cache de credenciais de usuário final proporciona a melhor experiência do usuário do MED-V, mas cria o potencial que alguém pode ter acesso às credenciais do usuário final.</span><span class="sxs-lookup"><span data-stu-id="08eae-129">Enabling the caching of end-user credentials provides the best user experience of MED-V, but creates the potential that someone could gain access to the end user’s credentials.</span></span> <span data-ttu-id="08eae-130">A única maneira de diminuir esse risco é especificando no pacote do **espaço de trabalho do MED-V** que as credenciais do usuário final não são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="08eae-130">The only way to lessen this risk is by specifying on the **MED-V Workspace Packager** that end-user credentials are not stored.</span></span> <span data-ttu-id="08eae-131">Para obter mais informações sobre autenticação de usuários finais, confira [autenticação de usuários finais do MED-V](authentication-of-med-v-end-users.md).</span><span class="sxs-lookup"><span data-stu-id="08eae-131">For more information about authentication of end users, see [Authentication of MED-V End Users](authentication-of-med-v-end-users.md).</span></span>

## <span data-ttu-id="08eae-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08eae-132">Related topics</span></span>


[<span data-ttu-id="08eae-133">Solução de problemas de operações</span><span class="sxs-lookup"><span data-stu-id="08eae-133">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

[<span data-ttu-id="08eae-134">Microsoft Enterprise Desktop Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="08eae-134">Microsoft Enterprise Desktop Virtualization 2.0</span></span>](index.md)

 

 





