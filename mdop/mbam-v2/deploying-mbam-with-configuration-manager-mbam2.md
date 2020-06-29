---
title: Como implantar o MBAM com o Configuration Manager
description: Como implantar o MBAM com o Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799275"
---
# <span data-ttu-id="6d656-103">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="6d656-104">Os procedimentos a seguir descrevem como implantar o Microsoft BitLocker Administration and Monitoring (MBAM) com o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager pela configuração recomendada do usingthe, descrito em [introdução-usando MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6d656-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="6d656-105">A configuração recomendada é instalar os recursos de administração e monitoramento em um ou mais servidores de administração e monitoramento do Microsoft BitLocker e instalar o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager em um servidor separado.</span><span class="sxs-lookup"><span data-stu-id="6d656-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="6d656-106">Antes de iniciar a instalação, verifique se você atendeu os pré-requisitos e requisitos de hardware e software para instalar o MBAM com o Configuration Manager analisando o [planejamento para implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="6d656-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="6d656-107">Se você precisar reinstalar o MBAM com a topologia do Configuration Manager, será necessário remover determinados objetos do Configuration Manager primeiro.</span><span class="sxs-lookup"><span data-stu-id="6d656-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="6d656-108">Leia o [artigo da base de dados de conhecimento](https://go.microsoft.com/fwlink/?LinkId=286306) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6d656-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="6d656-109">As etapas para instalar o MBAM com o Configuration Manager são agrupadas nas categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d656-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="6d656-110">Conclua as etapas para cada categoria para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="6d656-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="6d656-111">Como criar ou editar os arquivos mof</span><span class="sxs-lookup"><span data-stu-id="6d656-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="6d656-112">Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker através dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo **Configuration. mof** e editar ou criar o arquivo Sms \ _def. MOF, dependendo de qual versão do Configuration Manager você está usando.</span><span class="sxs-lookup"><span data-stu-id="6d656-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="6d656-113">Como criar ou editar os arquivos mof</span><span class="sxs-lookup"><span data-stu-id="6d656-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="6d656-114">Como instalar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="6d656-115">Esta seção fornece as etapas sobre como instalar o seguinte: MBAM no servidor do Configuration Manager; os bancos de dados de recuperação e auditoria no servidor de banco de dados; e os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="6d656-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="6d656-116">Como instalar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="6d656-117">Como validar a instalação de recursos do servidor MBAM no servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="6d656-118">Quando a instalação do Microsoft BitLocker Administration and Monitoring for concluída, valide se a instalação configurou com êxito todos os recursos MBAM necessários para o servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6d656-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="6d656-119">Como validar a instalação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="6d656-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d656-120">Related topics</span></span>


[<span data-ttu-id="6d656-121">Usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6d656-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





