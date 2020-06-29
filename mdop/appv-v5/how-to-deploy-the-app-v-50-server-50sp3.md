---
title: Como implantar o servidor do App-V 5.0
description: Como implantar o servidor do App-V 5.0
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796434"
---
# <span data-ttu-id="fc4ab-103">Como implantar o servidor do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fc4ab-103">How to Deploy the App-V 5.0 Server</span></span>


<span data-ttu-id="fc4ab-104">Use o procedimento a seguir para instalar o servidor do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-104">Use the following procedure to install the App-V 5.0 server.</span></span> <span data-ttu-id="fc4ab-105">Para obter informações sobre a implantação do servidor do App-V 5,0 SP3, consulte [sobre o app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-105">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

**<span data-ttu-id="fc4ab-106">Antes de começar:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-106">Before you start:</span></span>**

-   <span data-ttu-id="fc4ab-107">Verifique se você instalou o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="fc4ab-108">Consulte [pré-requisitos do App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-108">See [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

-   <span data-ttu-id="fc4ab-109">Examine a seção de servidor das [considerações de segurança do App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-109">Review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

-   <span data-ttu-id="fc4ab-110">Especifique uma porta onde cada componente será hospedado.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="fc4ab-111">Adicione regras de firewall para permitir que as solicitações de entrada acessem as portas especificadas.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="fc4ab-112">Se você usar scripts SQL, em vez do Windows Installer, para configurar o banco de dados de gerenciamento ou banco de dados de relatórios, será necessário executar os scripts SQL antes de instalar o servidor de gerenciamento ou o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="fc4ab-113">Veja [como implantar os bancos de dados do App-V usando scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

**<span data-ttu-id="fc4ab-114">Para instalar o servidor do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="fc4ab-114">To install the App-V 5.0 server</span></span>**

1. <span data-ttu-id="fc4ab-115">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-115">Copy the App-V 5.0 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="fc4ab-116">Inicie a instalação do servidor do App-V 5,0 clicando com o botão direito do mouse e executando **appv\_server\_setup.exe** como administrador e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-116">Start the App-V 5.0 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="fc4ab-117">Revise e aceite os termos de licença e escolha se deseja habilitar as atualizações da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="fc4ab-118">Na página **seleção de recursos** , selecione todos os componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fc4ab-119">Componente</span><span class="sxs-lookup"><span data-stu-id="fc4ab-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="fc4ab-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc4ab-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fc4ab-121">Servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc4ab-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-122">Fornece funcionalidade de gerenciamento geral para a infraestrutura do App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="fc4ab-123">Banco de dados de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc4ab-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-124">Facilita a implantação de bancos de dados para gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fc4ab-125">Publishing Server</span><span class="sxs-lookup"><span data-stu-id="fc4ab-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-126">Fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="fc4ab-127">Servidor de relatórios</span><span class="sxs-lookup"><span data-stu-id="fc4ab-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-128">Oferece o App-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-128">Provides App-V 5.0 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fc4ab-129">Banco de dados de relatórios</span><span class="sxs-lookup"><span data-stu-id="fc4ab-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-130">Facilita a implantação de bancos de dados para relatórios do App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="fc4ab-131">Na página **local de instalação** , aceite o local padrão onde os componentes selecionados serão instalados ou altere o local digitando um novo caminho na linha local de **instalação** .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="fc4ab-132">Na página **criar novo banco de dados de gerenciamento** inicial, configure a instância do **Microsoft SQL Server** e o **banco de dados do servidor de gerenciamento** selecionando a opção apropriada abaixo.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fc4ab-133">Método</span><span class="sxs-lookup"><span data-stu-id="fc4ab-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="fc4ab-134">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="fc4ab-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fc4ab-135">Você está usando uma instância personalizada do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-136">Selecione <strong> usar a instância personalizada </strong> e digite o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="fc4ab-137">Use o formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="fc4ab-138">O local de instalação presumido é o computador local.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="fc4ab-139">Sem suporte: um nome de servidor usando a <strong> instância forte de Format ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="fc4ab-140">Você está usando um nome de banco de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-141">Selecione <strong> configuração personalizada </strong> e digite o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="fc4ab-142">O nome do banco de dados deve ser exclusivo ou haverá falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="fc4ab-143">Na página **Configurar** , aceite o valor padrão **usar este computador local**.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="fc4ab-144">Observação</span><span class="sxs-lookup"><span data-stu-id="fc4ab-144">Note</span></span>**  
   <span data-ttu-id="fc4ab-145">Se você estiver instalando o servidor de gerenciamento e o banco de dados de gerenciamento lado a lado, algumas opções nessa página não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="fc4ab-146">Nesse caso, as opções apropriadas são selecionadas por padrão e não podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="fc4ab-147">Na página inicial do **banco de dados criar novo relatório** , configure a **instância do Microsoft SQL Server** e o **banco de dados do servidor de relatórios** selecionando a opção apropriada abaixo.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fc4ab-148">Método</span><span class="sxs-lookup"><span data-stu-id="fc4ab-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="fc4ab-149">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="fc4ab-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fc4ab-150">Você está usando uma instância personalizada do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-151">Selecione <strong> usar a instância personalizada </strong> e digite o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="fc4ab-152">Use o formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="fc4ab-153">O local de instalação presumido é o computador local.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="fc4ab-154">Sem suporte: um nome de servidor usando a <strong> instância forte de Format ServerName </strong> &lt; &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="fc4ab-155">Você está usando um nome de banco de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="fc4ab-156">Selecione <strong> configuração personalizada </strong> e digite o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="fc4ab-157">O nome do banco de dados deve ser exclusivo ou haverá falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="fc4ab-158">Na página **Configurar** , aceite o valor padrão: **Use este computador local**.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="fc4ab-159">Observação</span><span class="sxs-lookup"><span data-stu-id="fc4ab-159">Note</span></span>**  
   <span data-ttu-id="fc4ab-160">Se você estiver instalando o servidor de gerenciamento e o banco de dados de gerenciamento lado a lado, algumas opções nessa página não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="fc4ab-161">Nesse caso, as opções apropriadas são selecionadas por padrão e não podem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="fc4ab-162">Na página **Configurar** (configuração do servidor de gerenciamento), especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fc4ab-163">Item para configurar</span><span class="sxs-lookup"><span data-stu-id="fc4ab-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="fc4ab-164">Descrição e exemplos</span><span class="sxs-lookup"><span data-stu-id="fc4ab-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fc4ab-165">Digite o grupo de anúncios com permissões suficientes para gerenciar o ambiente do App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-166">Exemplo: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="fc4ab-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="fc4ab-167">Após a instalação, você pode adicionar mais usuários ou grupos usando o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="fc4ab-168">Entretanto, não há suporte para grupos de segurança global e grupos de distribuição dos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="fc4ab-169">Você deve usar <strong> o domínio local </strong> ou <strong> grupos universais </strong> são necessários para executar essa ação.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-170">Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-171">Se você não tiver um nome personalizado, não faça alterações.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-172">Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-173">Exemplo: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="fc4ab-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="fc4ab-174">Certifique-se de que a porta especificada não está sendo usada por outro site.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="fc4ab-175">Na página **Configurar** o **Publishing Server Configuration** , especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fc4ab-176">Item para configurar</span><span class="sxs-lookup"><span data-stu-id="fc4ab-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="fc4ab-177">Descrição e exemplos</span><span class="sxs-lookup"><span data-stu-id="fc4ab-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fc4ab-178">Especifique a URL para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-179">Exemplo<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="fc4ab-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-180">Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-181">Se você não tiver um nome personalizado, não faça alterações.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-182">Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-183">Exemplo: 54321</span><span class="sxs-lookup"><span data-stu-id="fc4ab-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="fc4ab-184">Certifique-se de que a porta especificada não está sendo usada por outro site.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="fc4ab-185">Na página **servidor de relatórios** , especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fc4ab-186">Item para configurar</span><span class="sxs-lookup"><span data-stu-id="fc4ab-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="fc4ab-187">Descrição e exemplos</span><span class="sxs-lookup"><span data-stu-id="fc4ab-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-188">Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de relatório.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-189">Se você não tiver um nome personalizado, não faça alterações.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="fc4ab-190">Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fc4ab-191">Exemplo: 55555</span><span class="sxs-lookup"><span data-stu-id="fc4ab-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="fc4ab-192">Certifique-se de que a porta especificada não está sendo usada por outro site.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="fc4ab-193">Para iniciar a instalação, clique em **instalar** na página **pronto** e, em seguida, clique em **Fechar** na página **concluída** .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="fc4ab-194">Para verificar se a configuração foi concluída com êxito, abra um navegador da Web e digite a seguinte URL:</span><span class="sxs-lookup"><span data-stu-id="fc4ab-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="fc4ab-195">**http:// &lt; Nome do computador do servidor de gerenciamento &gt; : &lt; número da porta do serviço de gerenciamento &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="fc4ab-196">Exemplo: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="fc4ab-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="fc4ab-197">Se a instalação for bem-sucedida, o console de gerenciamento do App-V será exibido sem erros.</span><span class="sxs-lookup"><span data-stu-id="fc4ab-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="fc4ab-198">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="fc4ab-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fc4ab-199">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fc4ab-200">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="fc4ab-200">Got an App-V issue?</span></span>** <span data-ttu-id="fc4ab-201">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fc4ab-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="fc4ab-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc4ab-202">Related topics</span></span>


[<span data-ttu-id="fc4ab-203">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fc4ab-203">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="fc4ab-204">Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios</span><span class="sxs-lookup"><span data-stu-id="fc4ab-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="fc4ab-205">Como instalar o servidor de publicação em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="fc4ab-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="fc4ab-206">Como implantar o servidor App-V 5.0 usando um script</span><span class="sxs-lookup"><span data-stu-id="fc4ab-206">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="fc4ab-207">Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc4ab-207">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





