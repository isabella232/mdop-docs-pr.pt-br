---
title: Pré-requisitos de instalação do MED-V
description: Pré-requisitos de instalação do MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799578"
---
# <span data-ttu-id="cfde1-103">Pré-requisitos de instalação do MED-V</span><span class="sxs-lookup"><span data-stu-id="cfde1-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="cfde1-104">Estes são pré-requisitos para a instalação do MED-V:</span><span class="sxs-lookup"><span data-stu-id="cfde1-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="cfde1-105">Requisitos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="cfde1-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="cfde1-106">Banco de dados de relatório</span><span class="sxs-lookup"><span data-stu-id="cfde1-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="cfde1-107">Antivirus/configuração do software de backup</span><span class="sxs-lookup"><span data-stu-id="cfde1-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="cfde1-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="cfde1-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="cfde1-109">Requisitos do Active Directory</span><span class="sxs-lookup"><span data-stu-id="cfde1-109">Active Directory Requirements</span></span>


<span data-ttu-id="cfde1-110">Ao configurar o servidor MED-V, se os usuários não fizerem parte do mesmo domínio ao qual o servidor pertence, uma relação de confiança deve ser definida entre os domínios.</span><span class="sxs-lookup"><span data-stu-id="cfde1-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="cfde1-111">Como instalar o banco de dados de relatórios</span><span class="sxs-lookup"><span data-stu-id="cfde1-111">How to Install the Report Database</span></span>


<span data-ttu-id="cfde1-112">O banco de dados de relatórios é necessário para armazenar todos os logs do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="cfde1-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="cfde1-113">O banco de dados de log é usado para gerar relatórios do MED-V.</span><span class="sxs-lookup"><span data-stu-id="cfde1-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="cfde1-114">Para obter informações sobre relatórios, consulte [relatórios do MED-V](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="cfde1-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="cfde1-115">O SQL Server pode ser instalado no mesmo servidor do servidor MED-V ou em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="cfde1-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="cfde1-116">Se estiver instalando em um servidor remoto, consulte [instalando o SQL Server em um servidor remoto](#bkmk-installingsqlserveronaremoteserver).</span><span class="sxs-lookup"><span data-stu-id="cfde1-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="cfde1-117">Instalando o SQL Server em um servidor remoto</span><span class="sxs-lookup"><span data-stu-id="cfde1-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="cfde1-118">Para instalar o SQL Server em um servidor remoto</span><span class="sxs-lookup"><span data-stu-id="cfde1-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="cfde1-119">Configure o seguinte no servidor remoto:</span><span class="sxs-lookup"><span data-stu-id="cfde1-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="cfde1-120">Nome da instância — instância padrão</span><span class="sxs-lookup"><span data-stu-id="cfde1-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="cfde1-121">Modo de autenticação – modo misto</span><span class="sxs-lookup"><span data-stu-id="cfde1-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="cfde1-122">Usuário – o usuário padrão criado é "SA"</span><span class="sxs-lookup"><span data-stu-id="cfde1-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="cfde1-123">Senha — senha desejada</span><span class="sxs-lookup"><span data-stu-id="cfde1-123">Password—Desired password</span></span>

    -   <span data-ttu-id="cfde1-124">Configurações de agrupamento — padrão</span><span class="sxs-lookup"><span data-stu-id="cfde1-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="cfde1-125">Erro nas configurações do relatório de uso — padrão</span><span class="sxs-lookup"><span data-stu-id="cfde1-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="cfde1-126">Instale os seguintes arquivos no servidor MED-V:</span><span class="sxs-lookup"><span data-stu-id="cfde1-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="cfde1-127">Para instalar os pré-requisitos para a coleção de objetos do pacote de gerenciamento do Microsoft SQL Server2008, baixe o [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) a partir do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="cfde1-128">Para instalar os pré-requisitos para a coleção de objetos do pacote de gerenciamento do Microsoft SQL Server2005, baixe o [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) a partir do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="cfde1-129">Para instalar os arquivos dll necessários para o Microsoft SQL Server2008, baixe a [coleção de objetos de gerenciamento do Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) a partir do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="cfde1-130">Para instalar os arquivos dll necessários para o Microsoft SQL Server2005, baixe os [objetos de gerenciamento do Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) no centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="cfde1-131">Para instalar os pacotes de instalação autônomos que fornecem valor adicional para SQL Server2008, baixe o [pacote de recursos do Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="cfde1-132">Para instalar os pacotes de instalação autônomos que fornecem valor adicional para SQL Server2005, baixe o [Feature Pack para Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) do centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfde1-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="cfde1-133">Para obter mais informações sobre esses arquivos, consulte [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) ou [pacote de recursos para Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="cfde1-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="cfde1-134">Antivirus/configuração do software de backup</span><span class="sxs-lookup"><span data-stu-id="cfde1-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="cfde1-135">Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, é recomendável que seja possível excluir os seguintes tipos de arquivo de máquina virtual de qualquer Antivirus ou processamento de backup em execução no host:</span><span class="sxs-lookup"><span data-stu-id="cfde1-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="cfde1-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="cfde1-136">\*.VMC</span></span>

-   <span data-ttu-id="cfde1-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="cfde1-137">\*.VUD</span></span>

-   <span data-ttu-id="cfde1-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="cfde1-138">\*.VSV</span></span>

-   <span data-ttu-id="cfde1-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="cfde1-139">\*.CKM</span></span>

-   <span data-ttu-id="cfde1-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="cfde1-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="cfde1-141">Como instalar e configurar o Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="cfde1-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="cfde1-142">**Importante**  Se o Virtual PC para Windows existir no computador host, desinstale-o antes de instalar o virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="cfde1-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="cfde1-143">Para instalar o Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="cfde1-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="cfde1-144">Baixe o virtual PC2007 SP1 do centro de download da Microsoft para o [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span><span class="sxs-lookup"><span data-stu-id="cfde1-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="cfde1-145">Execute o arquivo de instalação no computador host e siga o assistente.</span><span class="sxs-lookup"><span data-stu-id="cfde1-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="cfde1-146">Instale a atualização do PC2007 SP1 do virtual no computador host no modo elevado.</span><span class="sxs-lookup"><span data-stu-id="cfde1-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="cfde1-147">Para obter mais informações, consulte [a descrição do pacote de hotfix do Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="cfde1-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="cfde1-148">**Observação**  A atualização do PC2007 SP1 virtual é necessária para executar o PC2007 virtual SP1.</span><span class="sxs-lookup"><span data-stu-id="cfde1-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="cfde1-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cfde1-149">Related topics</span></span>


[<span data-ttu-id="cfde1-150">Configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="cfde1-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





