---
title: Introdução ao App-V 5.0
description: Introdução ao App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796528"
---
# <span data-ttu-id="89282-103">Introdução ao App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-103">Getting Started with App-V 5.0</span></span>


<span data-ttu-id="89282-104">O App-V 5,0 permite aos administradores implantar, atualizar e dar suporte a aplicativos como serviços em tempo real, de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="89282-104">App-V 5.0 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="89282-105">Os aplicativos individuais são transformados de produtos instalados localmente em serviços de gerenciamento centralizado e estão disponíveis onde você precisar, sem a necessidade de pré-configurar computadores ou alterar as configurações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="89282-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="89282-106">O App-V consiste nos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="89282-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="89282-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="89282-107">Element</span></span></th>
<th align="left"><span data-ttu-id="89282-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="89282-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89282-109">Servidor de gerenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="89282-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="89282-110">Fornece um local central para o gerenciamento da infraestrutura do App-V, que fornece aplicativos virtuais para o cliente da área de trabalho do App-V e para os serviços de área de trabalho remota (antigo Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="89282-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="89282-111">Usa o Microsoft SQL Server® para seu armazenamento de dados, em que um ou mais servidores de gerenciamento do App-V podem compartilhar um único repositório de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="89282-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="89282-112">Autentica solicitações e fornece segurança, medição, monitoramento e coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="89282-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="89282-113">O servidor usa o Active Directory e ferramentas de suporte para gerenciar usuários e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="89282-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="89282-114">Tem um site de gerenciamento baseado em® do Silverlight, que permite que você configure a infraestrutura do App-V em qualquer computador.</span><span class="sxs-lookup"><span data-stu-id="89282-114">Has a Silverlight®-based management site, which enables you to configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="89282-115">Você pode adicionar e remover aplicativos, manipular atalhos, atribuir permissões de acesso a usuários e grupos e criar grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="89282-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="89282-116">Permite a comunicação entre o console de gerenciamento da Web do App-V e o repositório de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="89282-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="89282-117">Esses componentes podem ser instalados em um único computador servidor ou em um ou mais computadores separados, dependendo da arquitetura do sistema necessária.</span><span class="sxs-lookup"><span data-stu-id="89282-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89282-118">Servidor de publicação do App-V</span><span class="sxs-lookup"><span data-stu-id="89282-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="89282-119">Fornece clientes App-V com aplicativos qualificados para o usuário específico</span><span class="sxs-lookup"><span data-stu-id="89282-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="89282-120">Hospeda o pacote de aplicativo virtual para streaming.</span><span class="sxs-lookup"><span data-stu-id="89282-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89282-121">Cliente de Desktop App-V</span><span class="sxs-lookup"><span data-stu-id="89282-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="89282-122">Recupera aplicativos virtuais</span><span class="sxs-lookup"><span data-stu-id="89282-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="89282-123">Publica os aplicativos nos clientes</span><span class="sxs-lookup"><span data-stu-id="89282-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="89282-124">Configura e gerencia automaticamente ambientes virtuais em tempo de extremidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="89282-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="89282-125">Armazena configurações de aplicativo virtual específicas do usuário, como alterações de registro e arquivo, em cada perfil de usuário&#39;s.</span><span class="sxs-lookup"><span data-stu-id="89282-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="89282-126">Cliente de serviços de área de trabalho remota do App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="89282-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="89282-127">Permite que servidores host da sessão da área de trabalho remota usem os recursos do cliente da área de trabalho do App-V para sessões de área de trabalho compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="89282-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="89282-128">Sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="89282-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="89282-129">É uma ferramenta baseada em assistente que você usa para transformar aplicativos tradicionais em aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="89282-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="89282-130">Produz o aplicativo "pacote", que consiste em:</span><span class="sxs-lookup"><span data-stu-id="89282-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="89282-131">um arquivo do aplicativo sequenciado (APPV)</span><span class="sxs-lookup"><span data-stu-id="89282-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="89282-132">um arquivo do Windows Installer (MSI) que pode ser implantado para clientes configurados para operação autônoma</span><span class="sxs-lookup"><span data-stu-id="89282-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="89282-133">Vários arquivos XML, incluindo Report.XML, PackageName_DeploymentConfig.XML e PackageName_UserConfig.XML.</span><span class="sxs-lookup"><span data-stu-id="89282-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="89282-134">Os arquivos userconfig e DeploymentConfig XML são usados para configurar as alterações personalizadas no comportamento padrão do pacote.</span><span class="sxs-lookup"><span data-stu-id="89282-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="89282-135">Para obter mais informações sobre esses elementos, consulte [arquitetura de alto nível para o App-V 5,0](high-level-architecture-for-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="89282-135">For more information about these elements, see [High Level Architecture for App-V 5.0](high-level-architecture-for-app-v-50.md).</span></span>

<span data-ttu-id="89282-136">Se você for novo para este produto, recomendamos que leia a documentação completamente.</span><span class="sxs-lookup"><span data-stu-id="89282-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="89282-137">Antes de implantá-lo em um ambiente de produção, também recomendamos que você valide seu plano de implantação em um ambiente de rede de teste.</span><span class="sxs-lookup"><span data-stu-id="89282-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="89282-138">Você também pode considerar a criação de uma classe sobre tecnologias pertinentes.</span><span class="sxs-lookup"><span data-stu-id="89282-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="89282-139">Para obter mais informações sobre oportunidades de treinamento da Microsoft, consulte a visão geral de treinamento da Microsoft em <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="89282-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="89282-140">**Observação**  Uma versão que pode ser baixada do guia deste administrador não está disponível.</span><span class="sxs-lookup"><span data-stu-id="89282-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="89282-141">No entanto, você pode aprender sobre um modo especial da biblioteca do TechNet que permite a você selecionar artigos, agrupá-los em uma coleção e imprimi-los ou exportá-los para um arquivo em <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="89282-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="89282-142">Esta seção do guia do administrador do App-V 5,0 inclui informações de alto nível sobre o App-V 5,0 para fornecer a você uma compreensão básica do produto antes de iniciar o planejamento de implantação.</span><span class="sxs-lookup"><span data-stu-id="89282-142">This section of the App-V 5.0 Administrator’s Guide includes high-level information about App-V 5.0 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="89282-143">Introdução ao App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="89282-143">Getting started with App-V 5.0</span></span>


-   [<span data-ttu-id="89282-144">Sobre o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-144">About App-V 5.0</span></span>](about-app-v-50.md)

    <span data-ttu-id="89282-145">Fornece uma visão geral de alto nível do App-V 5,0 e como ele pode ser usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="89282-145">Provides a high-level overview of App-V 5.0 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="89282-146">Sobre o App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="89282-146">About App-V 5.0 SP1</span></span>](about-app-v-50-sp1.md)

    <span data-ttu-id="89282-147">Fornece uma visão geral de alto nível do App-V 5.0 SP1 e como ele pode ser usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="89282-147">Provides a high-level overview of App-V 5.0SP1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="89282-148">Sobre o App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="89282-148">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

    <span data-ttu-id="89282-149">Fornece uma visão geral de alto nível do App-V 5.0 SP2 e como ele pode ser usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="89282-149">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="89282-150">Sobre o App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="89282-150">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

    <span data-ttu-id="89282-151">Fornece uma visão geral de alto nível do App-V 5.0 SP2 e como ele pode ser usado em sua organização.</span><span class="sxs-lookup"><span data-stu-id="89282-151">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="89282-152">Avaliação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-152">Evaluating App-V 5.0</span></span>](evaluating-app-v-50.md)

    <span data-ttu-id="89282-153">Fornece informações sobre como você pode avaliar melhor o App-V 5,0 para uso em sua organização.</span><span class="sxs-lookup"><span data-stu-id="89282-153">Provides information about how you can best evaluate App-V 5.0 for use in your organization.</span></span>

-   [<span data-ttu-id="89282-154">Arquitetura de alto nível para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-154">High Level Architecture for App-V 5.0</span></span>](high-level-architecture-for-app-v-50.md)

    <span data-ttu-id="89282-155">Fornece uma descrição dos recursos do App-V 5,0 e como eles funcionam juntos.</span><span class="sxs-lookup"><span data-stu-id="89282-155">Provides a description of the App-V 5.0 features and how they work together.</span></span>

-   [<span data-ttu-id="89282-156">Acessibilidade para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-156">Accessibility for App-V 5.0</span></span>](accessibility-for-app-v-50.md)

    <span data-ttu-id="89282-157">Fornece informações sobre recursos e serviços que tornam esse produto e sua documentação correspondente mais acessível para pessoas com deficiências.</span><span class="sxs-lookup"><span data-stu-id="89282-157">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="89282-158">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="89282-158">Other resources for this product</span></span>


-   [<span data-ttu-id="89282-159">Guia do administrador do Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="89282-159">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="89282-160">Planejamento para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-160">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

-   [<span data-ttu-id="89282-161">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-161">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

-   [<span data-ttu-id="89282-162">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-162">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

-   [<span data-ttu-id="89282-163">Solução de problemas do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="89282-163">Troubleshooting App-V 5.0</span></span>](troubleshooting-app-v-50.md)






 

 





