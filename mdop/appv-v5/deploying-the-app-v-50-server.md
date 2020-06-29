---
title: Implantação do servidor App-V 5.0
description: Implantação do servidor App-V 5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796533"
---
# <span data-ttu-id="be4a3-103">Implantação do servidor App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="be4a3-103">Deploying the App-V 5.0 Server</span></span>


<span data-ttu-id="be4a3-104">Você pode instalar os recursos do servidor do App-V 5,0 usando diferentes configurações de implantação, descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="be4a3-104">You can install the App-V 5.0 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="be4a3-105">Antes de instalar os recursos do servidor, examine a seção do servidor das [considerações de segurança do App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="be4a3-105">Before you install the server features, review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

<span data-ttu-id="be4a3-106">Para obter informações sobre a implantação do servidor do App-V 5,0 SP3, consulte [sobre o app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="be4a3-106">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

<span data-ttu-id="be4a3-107">**Importante**  Antes de instalar e configurar os servidores do App-V 5,0, você deve especificar uma porta onde cada componente será hospedado.</span><span class="sxs-lookup"><span data-stu-id="be4a3-107">**Important** Before you install and configure the App-V 5.0 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="be4a3-108">Você também deve adicionar as regras de firewall associadas para permitir que as solicitações de entrada acessem as portas especificadas.</span><span class="sxs-lookup"><span data-stu-id="be4a3-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="be4a3-109">O instalador não modifica as configurações de firewall.</span><span class="sxs-lookup"><span data-stu-id="be4a3-109">The installer does not modify firewall settings.</span></span>

 

## <a href="" id="---------app-v-5-0-server-overview"></a> <span data-ttu-id="be4a3-110">Visão geral do App-V Server 5,0</span><span class="sxs-lookup"><span data-stu-id="be4a3-110">App-V 5.0 Server overview</span></span>


<span data-ttu-id="be4a3-111">O servidor do App-V 5,0 é composto de cinco componentes.</span><span class="sxs-lookup"><span data-stu-id="be4a3-111">The App-V 5.0 Server is made up of five components.</span></span> <span data-ttu-id="be4a3-112">Cada componente serve a uma finalidade diferente no ambiente do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-112">Each component serves a different purpose within the App-V 5.0 environment.</span></span> <span data-ttu-id="be4a3-113">Cada um dos cinco componentes é brevemente descrito aqui:</span><span class="sxs-lookup"><span data-stu-id="be4a3-113">Each of the five components is briefly described here:</span></span>

-   <span data-ttu-id="be4a3-114">Servidor de gerenciamento – oferece funcionalidade de gerenciamento geral para a infraestrutura do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-114">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="be4a3-115">Banco de dados de gerenciamento – facilita as implantações de banco de dados do gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-115">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="be4a3-116">Publishing Server – fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="be4a3-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="be4a3-117">Servidor de relatórios – fornece o App-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="be4a3-117">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="be4a3-118">Banco de dados de relatórios – facilita a implantação de bancos de dados para relatórios do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-118">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> <span data-ttu-id="be4a3-119">Implantação autônoma do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="be4a3-119">App-V 5.0 stand-alone deployment</span></span>


<span data-ttu-id="be4a3-120">A implantação autônoma do App-V 5,0 fornece uma boa topologia para uma implantação pequena ou um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="be4a3-120">The App-V 5.0 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="be4a3-121">Quando você usa esse tipo de implementação, todos os componentes do servidor são implantados em um único computador.</span><span class="sxs-lookup"><span data-stu-id="be4a3-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="be4a3-122">Os serviços e bancos de dados associados serão concorrentes para os recursos do computador que executam os componentes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.0 components.</span></span> <span data-ttu-id="be4a3-123">Portanto, você não deve usar essa topologia para implantações maiores.</span><span class="sxs-lookup"><span data-stu-id="be4a3-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="be4a3-124">Como implantar o servidor do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="be4a3-124">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)

[<span data-ttu-id="be4a3-125">Como implantar o servidor App-V 5.0 usando um script</span><span class="sxs-lookup"><span data-stu-id="be4a3-125">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> <span data-ttu-id="be4a3-126">Implantação distribuída do App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="be4a3-126">App-V 5.0 Server distributed deployment</span></span>


<span data-ttu-id="be4a3-127">A topologia de implantação distribuída pode dar suporte a uma grande base de cliente do App-V 5,0 e permite que você gerencie e dimensione com mais facilidade seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="be4a3-127">The distributed deployment topology can support a large App-V 5.0 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="be4a3-128">Quando você usa esse tipo de implantação, os componentes do servidor do App-V 5,0 são implantados em vários computadores, com base na estrutura e nos requisitos da organização.</span><span class="sxs-lookup"><span data-stu-id="be4a3-128">When you use this type of deployment, the App-V 5.0 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="be4a3-129">Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios</span><span class="sxs-lookup"><span data-stu-id="be4a3-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="be4a3-130">Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="be4a3-130">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[<span data-ttu-id="be4a3-131">Como implantar o servidor App-V 5.0 usando um script</span><span class="sxs-lookup"><span data-stu-id="be4a3-131">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="be4a3-132">Como instalar o servidor de publicação em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="be4a3-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="be4a3-133">Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="be4a3-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## <span data-ttu-id="be4a3-134">Usando uma solução ESD (Enterprise Software Distribution) e o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="be4a3-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.0</span></span>


<span data-ttu-id="be4a3-135">Você também pode implantar os clientes e pacotes do App-V 5,0 usando um ESD sem ter que implantar o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-135">You can also deploy the App-V 5.0 clients and packages by using an ESD without having to deploy App-V 5.0.</span></span> <span data-ttu-id="be4a3-136">Os recursos completos para a integração variam de acordo com o ESD que você usa.</span><span class="sxs-lookup"><span data-stu-id="be4a3-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

<span data-ttu-id="be4a3-137">**Observação**  O servidor de relatórios do App-V 5,0 e o banco de dados de relatórios ainda podem ser implantados junto com o ESD para coletar os dados de relatório dos clientes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-137">**Note** The App-V 5.0 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.0 clients.</span></span> <span data-ttu-id="be4a3-138">No entanto, os outros três componentes do servidor não devem ser implantados, pois eles entrarão em conflito com a funcionalidade ESD.</span><span class="sxs-lookup"><span data-stu-id="be4a3-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

 

[<span data-ttu-id="be4a3-139">Implantação dos pacotes do App-V 5.0 usando a Distribuição eletrônica de software (ESD)</span><span class="sxs-lookup"><span data-stu-id="be4a3-139">Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> <span data-ttu-id="be4a3-140">Logs do servidor do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="be4a3-140">App-V 5.0 Server logs</span></span>


<span data-ttu-id="be4a3-141">Você pode usar as informações de log do App-V 5,0 Server para ajudar a solucionar problemas de instalação do servidor e eventos operacionais durante o uso do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-141">You can use App-V 5.0 server log information to help troubleshoot the server installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="be4a3-142">As informações de log relacionadas ao servidor podem ser analisadas com o **Visualizador de eventos**.</span><span class="sxs-lookup"><span data-stu-id="be4a3-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="be4a3-143">A linha a seguir exibe o caminho específico para eventos relacionados ao servidor:</span><span class="sxs-lookup"><span data-stu-id="be4a3-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="be4a3-144">Visualizador de eventos \ \ logs de aplicativos e serviços \ \ Microsoft \ \ App V</span><span class="sxs-lookup"><span data-stu-id="be4a3-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="be4a3-145">Os logs de instalação associados são salvos no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="be4a3-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="be4a3-146">Temp</span><span class="sxs-lookup"><span data-stu-id="be4a3-146">%temp%</span></span>**

<span data-ttu-id="be4a3-147">No App-V 5,0 SP3, alguns registros foram consolidados e movidos.</span><span class="sxs-lookup"><span data-stu-id="be4a3-147">In App-V 5.0 SP3, some logs have been consolidated and moved.</span></span> <span data-ttu-id="be4a3-148">Consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="be4a3-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-0-reporting"></a> <span data-ttu-id="be4a3-149">Relatórios do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="be4a3-149">App-V 5.0 reporting</span></span>


<span data-ttu-id="be4a3-150">Os relatórios do App-V 5,0 permitem que os clientes do App-V 5,0 coletem dados e os enviem de volta para serem armazenados em um repositório central.</span><span class="sxs-lookup"><span data-stu-id="be4a3-150">App-V 5.0 reporting allows App-V 5.0 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="be4a3-151">Você pode usar essas informações para obter uma visão melhor do uso do aplicativo virtual dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="be4a3-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="be4a3-152">A lista a seguir mostra alguns dos tipos de informação que o cliente do App-V 5,0 coleta:</span><span class="sxs-lookup"><span data-stu-id="be4a3-152">The following list displays some of the types of information the App-V 5.0 client collects:</span></span>

-   <span data-ttu-id="be4a3-153">Informações sobre o computador que executa o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-153">Information about the computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="be4a3-154">Informações sobre pacotes virtualizados em um computador específico que executa o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="be4a3-154">Information about virtualized packages on a specific computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="be4a3-155">Informações sobre abertura e desligamento de pacotes para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="be4a3-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="be4a3-156">As informações de relatório serão mantidas até que sejam enviadas com êxito para o banco de dados do servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="be4a3-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="be4a3-157">Depois que os dados estiverem no banco de dados, você poderá usar o Microsoft SQL Server Reporting Services para gerar os relatórios necessários.</span><span class="sxs-lookup"><span data-stu-id="be4a3-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="be4a3-158">Se quiser recuperar informações de relatório, você deve usar o Microsoft SQL Server Reporting Services (SSRS) que está disponível com o Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="be4a3-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="be4a3-159">O SSRS não é instalado quando você instala o servidor de relatórios do App-V 5,0 e deve ser implantado separadamente para gerar os relatórios associados.</span><span class="sxs-lookup"><span data-stu-id="be4a3-159">SSRS is not installed when you install the App-V 5.0 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="be4a3-160">Use o link a seguir para obter mais informações [sobre relatórios do App-V 5,0](about-app-v-50-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="be4a3-160">Use the following link for more information [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>

[<span data-ttu-id="be4a3-161">Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="be4a3-161">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## <span data-ttu-id="be4a3-162">Outros recursos para o App-V Server</span><span class="sxs-lookup"><span data-stu-id="be4a3-162">Other resources for the App-V server</span></span>


[<span data-ttu-id="be4a3-163">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="be4a3-163">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)






 

 





