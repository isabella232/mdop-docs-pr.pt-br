---
title: Planejamento da compatibilidade do sistema operacional para aplicativos
description: Planejamento da compatibilidade do sistema operacional para aplicativos
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799678"
---
# <span data-ttu-id="a7baf-103">Planejamento da compatibilidade do sistema operacional para aplicativos</span><span class="sxs-lookup"><span data-stu-id="a7baf-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="a7baf-104">Este tópico ajuda a determinar como resolver problemas de compatibilidade do sistema operacional do aplicativo e discute como a virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 funciona como uma solução para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="a7baf-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="a7baf-105">Este tópico discute os requisitos comerciais do MED-V e compara o MED-V ao modo Windows XP e ao Microsoft Application Virtualization (App-V):</span><span class="sxs-lookup"><span data-stu-id="a7baf-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="a7baf-106">Requisitos comerciais para o MED-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="a7baf-107">Benefícios do MED-V em relação ao modo Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7baf-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="a7baf-108">Benefícios do MED-V versus App-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="a7baf-109">Requisitos comerciais para o MED-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="a7baf-110">Quando o departamento de ti da sua empresa está determinando se deseja atualizar para o Windows 7, ele deve prestar atenção aos seus aplicativos de linha de negócios e aplicativos de linha de negócios baseados na Web para garantir que eles possam ser executados no novo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a7baf-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="a7baf-111">Geralmente, esses aplicativos e URLs foram criados para funcionar especificamente com uma versão mais antiga do Windows ou Internet Explorer, e podem ocorrer problemas quando você tenta usá-los no novo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a7baf-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="a7baf-112">A Microsoft oferece muitos métodos diferentes para manipular os vários problemas de compatibilidade que podem ocorrer quando você atualiza, como o Application Compatibility Toolkit (ACT) e o assistente de compatibilidade de programas do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7baf-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="a7baf-113">Mas mesmo depois que todos os aplicativos tiverem sido testados quanto à compatibilidade e correções forem determinados, alguns aplicativos ainda não funcionarão corretamente no Windows 7 ou são muito dispendiosos para serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="a7baf-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="a7baf-114">Ao usar o MED-V, você pode executar esses aplicativos herdados por meio de um ambiente de PC virtual do Windows executando o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7baf-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="a7baf-115">Como você não precisa mais testar e validar esses aplicativos de problemas no novo sistema operacional antes da atualização, a migração para o Windows 7 é muito mais fácil e rápida.</span><span class="sxs-lookup"><span data-stu-id="a7baf-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="a7baf-116">Usando a lista de verificação do MED-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-116">Using MED-V Checklist</span></span>

<span data-ttu-id="a7baf-117">Considere o MED-V se qualquer um dos seguintes cenários se aplicarem a você:</span><span class="sxs-lookup"><span data-stu-id="a7baf-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="a7baf-118">Você é uma organização de grande porte (por exemplo, 500 usuários e mais), ter um contrato empresarial com a Microsoft e planejar a atualização para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7baf-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="a7baf-119">Você testou seus aplicativos de linha de negócios e encontrou alguns que são incompatíveis com o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7baf-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="a7baf-120">Você resolveu os problemas de compatibilidade para alguns desses aplicativos problemáticos atualizando o aplicativo ou usando um Shim fornecido pela Microsoft, como o kit de ferramentas de compatibilidade de aplicativos (ACT), mas os problemas de compatibilidade permanecem para alguns aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a7baf-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="a7baf-121">Você considerou o App-V como uma opção para fornecer os aplicativos incompatíveis e concluiu que, mesmo depois de implementar o App-V, você ainda tem problemas de compatibilidade do sistema operacional do aplicativo que você deve resolver.</span><span class="sxs-lookup"><span data-stu-id="a7baf-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="a7baf-122">Você considerou o modo Windows XP como uma solução e determinou que essa não é uma opção eficiente porque:</span><span class="sxs-lookup"><span data-stu-id="a7baf-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="a7baf-123">Você deseja poder implantar imagens virtuais que contenham os aplicativos de problemas para todos os usuários finais ao mesmo tempo, em vez de individualmente e ter as imagens virtuais automaticamente associadas ao domínio.</span><span class="sxs-lookup"><span data-stu-id="a7baf-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="a7baf-124">Você decidiu que é muito mais econômico gerenciar esses aplicativos herdados (que são entregues virtualmente) e controlar as configurações do Windows Virtual PC de um local centralizado, em vez de cada área de trabalho do usuário final.</span><span class="sxs-lookup"><span data-stu-id="a7baf-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="a7baf-125">Você deseja poder atualizar e dar suporte a máquinas virtuais em escala em vez de por área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7baf-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="a7baf-126">Você deseja a capacidade de redirecionar URLs executadas melhor em uma versão mais antiga do Internet Explorer para as máquinas virtuais e gerenciar facilmente o redirecionamento de URL mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a7baf-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="a7baf-127">Você determinou que seria mais econômico e útil fazer a atualização para o Windows 7 o mais breve possível e decidiu adiar a solução de problemas de compatibilidade de aplicativos restantes até uma data posterior, sabendo que você tem uma solução disponível no MED-V.</span><span class="sxs-lookup"><span data-stu-id="a7baf-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="a7baf-128">Benefícios do MED-V em relação ao modo Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7baf-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="a7baf-129">O Windows Virtual PC para Windows 7 permite que você execute versões diferentes de um sistema operacional ao mesmo tempo em um único dispositivo e está incluído no Windows 7 Professional Edition e versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="a7baf-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="a7baf-130">A funcionalidade do modo do Windows XP aproveita o PC virtual do Windows fornecendo uma imagem pré-configurada do Windows XP que permite criar um ambiente virtual do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7baf-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="a7baf-131">Nesse ambiente virtual, você pode instalar manualmente os aplicativos que são incompatíveis com o Windows 7 e que sejam executados diretamente de sua área de trabalho por meio do PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7baf-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="a7baf-132">Usando o modo Windows XP, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a7baf-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="a7baf-133">Executar aplicativos compatíveis com o Windows XP dentro de uma máquina virtual que é executada no PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7baf-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="a7baf-134">Publicar esses aplicativos no menu da área de trabalho ou do programa do host.</span><span class="sxs-lookup"><span data-stu-id="a7baf-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="a7baf-135">Quando quiser fornecer essas máquinas virtuais em uma escala grande, como parte de uma migração empresarial para o Windows 7, você deve ser capaz de implantar as máquinas virtuais rapidamente, provisionar e personalizá-las com eficiência, controlar suas configurações e dar suporte a elas com facilidade.</span><span class="sxs-lookup"><span data-stu-id="a7baf-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="a7baf-136">O MED-V se baseia no modo Windows XP para oferecer compatibilidade de aplicativos em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="a7baf-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="a7baf-137">Enquanto o modo Windows XP está limitado a fornecer funcionalidade de aplicativo virtual para indivíduos e pequenas empresas, o MED-V permite implantações em larga escala de imagens pré-configuradas do Windows XP em toda a sua rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="a7baf-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="a7baf-138">Ele oferece uma solução de gerenciamento pronto para empresas para a configuração, a implantação e a manutenção desses espaços de trabalho virtuais do MED-V.</span><span class="sxs-lookup"><span data-stu-id="a7baf-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="a7baf-139">O MED-V também oferece ao enterpriseadministrators um conjunto de políticas para controlar o uso da imagem.</span><span class="sxs-lookup"><span data-stu-id="a7baf-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="a7baf-140">Isso inclui quais usuários terão acesso a quais aplicativos específicos nessas imagens.</span><span class="sxs-lookup"><span data-stu-id="a7baf-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="a7baf-141">Ao usar o MED-V, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a7baf-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="a7baf-142">Atualize para seu novo sistema operacional sem precisar testar e resolver cada aplicativo e URL incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="a7baf-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="a7baf-143">Implante imagens virtuais do Windows XP que sejam automaticamente integradas ao domínio e personalizadas por cada usuário.</span><span class="sxs-lookup"><span data-stu-id="a7baf-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="a7baf-144">Provisionar aplicativos e informações de redirecionamento de URL para os usuários.</span><span class="sxs-lookup"><span data-stu-id="a7baf-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="a7baf-145">Controlar as configurações do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a7baf-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="a7baf-146">Mantenha e dê suporte a pontos de extremidade por meio de monitoramento e solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="a7baf-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="a7baf-147">Certifique-se de que os computadores convidados sejam corrigidos, mesmo se estiverem em um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="a7baf-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="a7baf-148">Automatizar a criação de máquinas virtuais por usuário e a inicialização de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="a7baf-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="a7baf-149">Diagnostique problemas no host e nos computadores convidados facilmente.</span><span class="sxs-lookup"><span data-stu-id="a7baf-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="a7baf-150">Gerencie perfeitamente computadores convidados conectados por meio do modo NAT do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a7baf-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="a7baf-151">Benefícios do MED-V versus App-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="a7baf-152">O MED-V e o App-V são duas tecnologias muito diferentes que podem facilmente trabalhar em conjunto para resolver problemas de compatibilidade do sistema operacional do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7baf-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="a7baf-153">Ao usar o App-V, você cria um pacote individual para cada aplicativo, e cada um deles é mantido separadamente dos outros.</span><span class="sxs-lookup"><span data-stu-id="a7baf-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="a7baf-154">Cada aplicativo virtual pode ser entregue imediatamente ao usuário final, o que é muito útil para uma estratégia de implantação do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7baf-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="a7baf-155">O MED-V não manipula aplicativos individualmente.</span><span class="sxs-lookup"><span data-stu-id="a7baf-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="a7baf-156">Em vez disso, ele cria uma instância adicional do Windows XP na mesma área de trabalho que está executando o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7baf-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="a7baf-157">Você pode instalar quantos aplicativos forem necessários para esta imagem virtual e gerenciar a imagem da mesma forma que faria com qualquer outro computador da sua organização.</span><span class="sxs-lookup"><span data-stu-id="a7baf-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="a7baf-158">Além disso, você pode usar o MED-V em conjunto com o App-V para que os aplicativos virtuais que são sequenciados por meio do App-V sejam instalados, publicados e gerenciados usando o MED-V.</span><span class="sxs-lookup"><span data-stu-id="a7baf-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="a7baf-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7baf-159">Related topics</span></span>


[<span data-ttu-id="a7baf-160">Definir e planejar sua implantação da MED-V</span><span class="sxs-lookup"><span data-stu-id="a7baf-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





