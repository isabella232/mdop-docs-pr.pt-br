---
title: Publicação de aplicativos e interação com clientes
description: Publicação de aplicativos e interação com clientes
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796573"
---
# <span data-ttu-id="ad9bf-103">Publicação de aplicativos e interação com clientes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="ad9bf-104">Este artigo fornece informações técnicas sobre operações comuns do cliente App-V e sua integração com o sistema operacional local.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="ad9bf-105">Arquivos de pacote App-V criados pelo sequenciador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="ad9bf-106">O que há no arquivo do AppV?</span><span class="sxs-lookup"><span data-stu-id="ad9bf-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="ad9bf-107">Locais do armazenamento de dados do cliente App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="ad9bf-108">Registro do pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="ad9bf-109">Comportamento da loja de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="ad9bf-110">Registro e dados em roaming</span><span class="sxs-lookup"><span data-stu-id="ad9bf-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="ad9bf-111">Gerenciamento do ciclo de vida do aplicativo cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="ad9bf-112">Integração de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="ad9bf-113">Processamento dinâmico de configuração</span><span class="sxs-lookup"><span data-stu-id="ad9bf-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="ad9bf-114">Montagens lado a lado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="ad9bf-115">Registro em log do cliente</span><span class="sxs-lookup"><span data-stu-id="ad9bf-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="ad9bf-116">Para obter informações de referência adicionais, consulte a [página de download de recursos da documentação do Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="ad9bf-117">Arquivos de pacote App-V criados pelo sequenciador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="ad9bf-118">O sequenciador cria pacotes do App-V e produz um aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="ad9bf-119">O processo de sequenciamento cria os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-120">Arquivo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-120">File</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-122">. AppV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-123">O arquivo de pacote principal, que contém os ativos capturados e as informações de estado do processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-124">Arquitetura do arquivo de pacote, informações de publicação e registro em um formulário com token que pode ser reaplicado a um computador e a um usuário específico após a entrega.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-125">. MSI</span><span class="sxs-lookup"><span data-stu-id="ad9bf-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-126">Wrapper de implantação executável que você pode usar para implantar arquivos. AppV manualmente ou usando uma plataforma de implantação de terceiros.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-128">Arquivo usado para personalizar os parâmetros de publicação padrão para todos os aplicativos em um pacote que é implantado globalmente para todos os usuários em um computador que esteja executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-130">Arquivo usado para personalizar os parâmetros de publicação de todos os aplicativos em um pacote que é implantado para um usuário específico em um computador que esteja executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-132">Resumo das mensagens resultantes do processo de sequenciamento, incluindo drivers omitidos, arquivos e locais do registro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-133">. FICHEIRO</span><span class="sxs-lookup"><span data-stu-id="ad9bf-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="ad9bf-134">Opcional: </em> arquivo do acelerador de pacote usado para recriar automaticamente um pacote de aplicativo virtual sequenciado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="ad9bf-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="ad9bf-136">Opcional: </em> arquivo de modelo do sequenciador usado para manter as configurações do sequenciador reutilizadas comumente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-137">Para obter informações sobre o sequenciamento, consulte o [Guia de sequenciamento do Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=269810).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-137">For information about sequencing, see [Application Virtualization Sequencing Guide](https://go.microsoft.com/fwlink/?LinkID=269810).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="ad9bf-138">O que há no arquivo do AppV?</span><span class="sxs-lookup"><span data-stu-id="ad9bf-138">What’s in the appv file?</span></span>


<span data-ttu-id="ad9bf-139">O arquivo do AppV é um contêiner que armazena arquivos XML e não XML juntos em uma única entidade.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="ad9bf-140">Esse arquivo é criado a partir do formato AppX, que se baseia no padrão Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="ad9bf-141">Para exibir o conteúdo do arquivo do AppV, faça uma cópia do pacote e, em seguida, renomeie o arquivo copiado para uma extensão ZIP.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="ad9bf-142">O arquivo do AppV contém a seguinte pasta e arquivos, que são usados ao criar e publicar um aplicativo virtual:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-143">Nome</span><span class="sxs-lookup"><span data-stu-id="ad9bf-143">Name</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-144">Type</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-146">Root</span><span class="sxs-lookup"><span data-stu-id="ad9bf-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-147">Pasta de arquivos</span><span class="sxs-lookup"><span data-stu-id="ad9bf-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-148">Diretório que contém o sistema de arquivos para o aplicativo virtualizado que é capturado durante a sequenciagem.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-149">[Content_Types]. xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-150">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-151">Lista dos principais tipos de conteúdo no arquivo do AppV (por exemplo, DLL, EXE, BIN).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-153">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-154">Layout do arquivo do AppV, que usa elementos File, Block e BlockMap que habilitam o local e a validação dos arquivos no pacote App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-156">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-157">Metadados do pacote que contém as informações necessárias para adicionar, publicar e iniciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="ad9bf-158">Inclui pontos de extensão (associações de tipo de arquivo e atalhos) e os nomes e GUIDs associados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-160">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-161">Lista de arquivos capturados durante o sequenciamento, incluindo atributos (por exemplo, diretórios, arquivos, pastas opacas, pastas vazias e nomes longos e curtos).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-163">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-164">Informações sobre o computador de sequenciamento (versão do sistema operacional, versão do Internet Explorer, versão do .NET Framework) e processo (atualização, versão do pacote).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="ad9bf-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-166">Arquivo DAT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-167">Chaves do registro e valores capturados durante o processo de sequenciamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-169">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="ad9bf-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-170">Lista de arquivos para o bloco de recursos Primary e Publishing.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="ad9bf-171">O bloco de recursos de publicação contém os arquivos ICO e partes de arquivos (EXE e DLL) necessárias para publicar o pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="ad9bf-172">Quando presente, o bloco de recursos principal inclui arquivos que foram otimizados para streaming durante o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="ad9bf-173">Locais do armazenamento de dados do cliente App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-173">App-V client data storage locations</span></span>


<span data-ttu-id="ad9bf-174">O cliente App-V executa tarefas para garantir que os aplicativos virtuais sejam executados corretamente e funcionem como aplicativos instalados localmente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="ad9bf-175">O processo de abrir e executar aplicativos virtuais requer o mapeamento do sistema de arquivos virtual e do registro para garantir que o aplicativo tenha os componentes obrigatórios de um aplicativo tradicional esperado pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="ad9bf-176">Esta seção descreve os ativos necessários para executar aplicativos virtuais e lista o local onde o App-V armazena os ativos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-177">Nome</span><span class="sxs-lookup"><span data-stu-id="ad9bf-177">Name</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-178">Localização</span><span class="sxs-lookup"><span data-stu-id="ad9bf-178">Location</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-180">Repositório de pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-182">Local padrão para arquivos de pacote somente leitura</span><span class="sxs-lookup"><span data-stu-id="ad9bf-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-183">Catálogo da máquina</span><span class="sxs-lookup"><span data-stu-id="ad9bf-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="ad9bf-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-185">Contém documentos de configuração por máquina</span><span class="sxs-lookup"><span data-stu-id="ad9bf-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-186">Catálogo de usuários</span><span class="sxs-lookup"><span data-stu-id="ad9bf-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="ad9bf-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-188">Contém documentos de configuração por usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-189">Backups de atalho</span><span class="sxs-lookup"><span data-stu-id="ad9bf-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="ad9bf-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-191">Armazena os pontos de integração anteriores que habilitam a restauração em pacote cancelar publicação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-192">Roaming de cópia em gravação (vaca)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="ad9bf-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-194">Localização de roaming gravável para a modificação do pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-195">Copiar em gravação (vaca) local</span><span class="sxs-lookup"><span data-stu-id="ad9bf-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="ad9bf-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-197">Local não móvel gravável para a modificação do pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-198">Registro do computador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-200">Contém informações de estado do pacote, incluindo VReg para pacotes publicados de máquina ou globalmente (Hive da máquina)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-201">Registro de usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-203">Contém informações de estado do pacote do usuário, incluindo VReg</span><span class="sxs-lookup"><span data-stu-id="ad9bf-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-204">Classes de registro de usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-206">Contém informações adicionais do estado do pacote do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-207">Detalhes adicionais para a tabela são fornecidos na seção abaixo e em todo o documento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="ad9bf-208">Repositório de pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-208">Package store</span></span>

<span data-ttu-id="ad9bf-209">O cliente App-V gerencia os ativos de aplicativos montados no armazenamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="ad9bf-210">Esse local de armazenamento padrão é `%ProgramData%\App-V` , mas você pode configurá-lo durante ou após a instalação usando o `Set-AppVClientConfiguration` comando do PowerShell, que modifica o registro local ( `PackageInstallationRoot` valor na `HKLM\Software\Microsoft\AppV\Client\Streaming` chave).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="ad9bf-211">O repositório de pacotes deve estar localizado em um caminho local no sistema operacional do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="ad9bf-212">Os pacotes individuais são armazenados no repositório de pacotes em subdiretórios nomeados para o GUID do pacote e o GUID da versão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="ad9bf-213">Exemplo de um caminho para um aplicativo específico:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="ad9bf-214">Para alterar o local padrão do repositório de pacotes durante a instalação, consulte [como implantar o cliente App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

### <span data-ttu-id="ad9bf-215">Repositório de conteúdo compartilhado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-215">Shared Content Store</span></span>

<span data-ttu-id="ad9bf-216">Se o cliente App-V estiver configurado no modo de repositório de conteúdo compartilhado, nenhum dado será gravado em disco quando ocorrer uma falha de fluxo, o que significa que os pacotes exigem espaço em disco local mínimo (dados de publicação).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="ad9bf-217">O uso de menos espaço em disco é altamente desejável em ambientes VDI, em que o armazenamento local pode ser limitado e o fluxo de aplicativos de um local de rede de alto desempenho (como uma SAN) é preferível.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="ad9bf-218">Para obter mais informações sobre o modo de repositório de conteúdo compartilhado, consulte <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="ad9bf-219">**Observação**  O repositório do computador e do pacote devem estar localizados em uma unidade local, mesmo quando você estiver usando configurações compartilhadas de repositório de conteúdo para o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="ad9bf-220">Catálogos de pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-220">Package catalogs</span></span>

<span data-ttu-id="ad9bf-221">O cliente App-V gerencia os seguintes dois locais baseados em arquivos:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="ad9bf-222">Catálogos (usuário e computador).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="ad9bf-223">**Locais do registro** – depende de como o pacote é direcionado para publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="ad9bf-224">Há um catálogo (armazenamento de dados) para o computador e um catálogo para cada usuário individual.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="ad9bf-225">O catálogo do computador armazena informações globais aplicáveis a todos os usuários ou qualquer usuário, e o catálogo do usuário armazena as informações aplicáveis a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="ad9bf-226">O catálogo é um conjunto de configurações dinâmicas e arquivos de manifesto; Há dados discretos para o arquivo e o registro por versão do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="ad9bf-227">Catálogo da máquina</span><span class="sxs-lookup"><span data-stu-id="ad9bf-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-229">Armazena documentos do pacote que estão disponíveis para os usuários do computador, quando os pacotes são adicionados e publicados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="ad9bf-230">No entanto, se um pacote for "global" no momento da publicação, as integrações estarão disponíveis para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="ad9bf-231">Se um pacote for não global, as integrações serão publicadas somente para usuários específicos, mas ainda há recursos globais modificados e visíveis para qualquer pessoa no computador cliente (por exemplo, o diretório do pacote está em um local de disco compartilhado).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="ad9bf-232">Se um pacote estiver disponível para um usuário no computador (global ou não global), o manifesto será armazenado no catálogo da máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="ad9bf-233">Quando um pacote é publicado globalmente, há um arquivo de configuração dinâmico, armazenado no catálogo da máquina; Portanto, a determinação de se um pacote é global é definida de acordo com a existência de um arquivo de política (arquivo UserDeploymentConfiguration) no catálogo da máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-234">Local de armazenamento padrão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="ad9bf-235">Este local não é o mesmo que o local de armazenamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="ad9bf-236">O repositório de pacotes é a cópia dourada ou pristine dos arquivos do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-237">Arquivos no catálogo do computador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-240">UserManifest.xml (pacote publicado globalmente)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-241">UserDeploymentConfiguration.xml (pacote publicado globalmente)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-242">Localização adicional do catálogo do computador, usado quando o pacote faz parte de um grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="ad9bf-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-243">O local a seguir é além do local do pacote específico mencionado acima:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-244">Arquivos adicionais no catálogo do computador quando o pacote fizer parte de um grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="ad9bf-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-246">UserPackageGroupDescriptor.xml (grupo de conexão publicada globalmente)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ad9bf-247">Catálogo de usuários</span><span class="sxs-lookup"><span data-stu-id="ad9bf-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-249">Criado durante o processo de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-249">Created during the publishing process.</span></span> <span data-ttu-id="ad9bf-250">Contém informações usadas para publicar o pacote e também usado no lançamento para garantir que um pacote seja provisionado para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="ad9bf-251">Criado em um local de roaming e inclui informações de publicação específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="ad9bf-252">Quando um pacote é publicado para um usuário, o arquivo de política é armazenado no catálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="ad9bf-253">Ao mesmo tempo, uma cópia do manifesto também é armazenada no catálogo do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="ad9bf-254">Quando uma qualificação de pacote é removida para um usuário, os arquivos de pacote relevantes são removidos do catálogo de usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="ad9bf-255">Olhando para o catálogo do usuário, um administrador pode visualizar a presença de um arquivo de configuração dinâmico, que indica que o pacote tem direito para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="ad9bf-256">Para usuários de roaming, o catálogo do usuário precisa estar em um local de roaming ou compartilhado para preservar o comportamento herdado do App-V do direcionamento de usuários por padrão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="ad9bf-257">A qualificação e a política são vinculadas a um usuário, não um computador, para que eles possam fazer roaming com o usuário quando forem provisionados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-258">Local de armazenamento padrão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-259">Arquivos no catálogo do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-261">DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-262">Local de catálogo do usuário adicional, usado quando o pacote faz parte de um grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="ad9bf-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-263">O local a seguir é além do local do pacote específico mencionado acima:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-264">Arquivo adicional no catálogo do computador quando o pacote fizer parte de um grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="ad9bf-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ad9bf-265">Backups de atalho</span><span class="sxs-lookup"><span data-stu-id="ad9bf-265">Shortcut backups</span></span>

<span data-ttu-id="ad9bf-266">Durante o processo de publicação, o cliente App-V faz o backup de todos os atalhos e pontos de integração para `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` esse backup permite que a restauração desses pontos de integração para as versões anteriores sejam canceladas quando o pacote é cancelado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="ad9bf-267">Copiar em arquivos de gravação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-267">Copy on Write files</span></span>

<span data-ttu-id="ad9bf-268">O repositório de pacotes contém uma cópia pristine dos arquivos de pacote que foram retransmitidos do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="ad9bf-269">Durante a operação normal de um aplicativo App-V, o usuário ou serviço pode exigir alterações nos arquivos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="ad9bf-270">Essas alterações não são feitas no repositório de pacotes para preservar a capacidade de reparar o aplicativo, o que remove essas alterações.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="ad9bf-271">Esses locais, chamados de cópia na gravação (vaca), dão suporte a locais de roaming e não móveis.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="ad9bf-272">O local onde as modificações são armazenadas depende de onde o aplicativo foi programado para escrever alterações em uma experiência nativa.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="ad9bf-273">VACA roaming</span><span class="sxs-lookup"><span data-stu-id="ad9bf-273">COW roaming</span></span>

<span data-ttu-id="ad9bf-274">O local de roaming vaca descrito acima armazena alterações em arquivos e diretórios direcionados para o local típico% AppData% ou o local \\Users\\{username}\\AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="ad9bf-275">Esses diretórios e arquivos são então movidos de acordo com as configurações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="ad9bf-276">Local vaca</span><span class="sxs-lookup"><span data-stu-id="ad9bf-276">COW local</span></span>

<span data-ttu-id="ad9bf-277">O local vaca local é semelhante ao local de roaming, mas as pastas e os arquivos não são movidos para outros computadores, mesmo se o suporte a roaming tiver sido configurado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="ad9bf-278">O local vaca local descrito acima armazena alterações aplicáveis a janelas típicas e não ao local% AppData%.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="ad9bf-279">As pastas listadas irão variar, mas haverá dois locais para qualquer local típico do Windows (por exemplo, AppData comuns e AppDatas comuns).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="ad9bf-280">O **S** significa o local restrito quando o serviço virtual solicita a alteração como um usuário elevado diferente dos usuários conectados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="ad9bf-281">O local não-**S** armazena alterações baseadas em usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="ad9bf-282">Registro do pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-282">Package registry</span></span>


<span data-ttu-id="ad9bf-283">Antes de um aplicativo poder acessar os dados do registro do pacote, o cliente App-V deve disponibilizar os dados do registro do pacote para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="ad9bf-284">O cliente App-V usa o registro real como um repositório de backup para todos os dados do registro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="ad9bf-285">Quando um novo pacote é adicionado ao cliente App-V, uma cópia do registro. O arquivo DAT do pacote é criado em `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="ad9bf-286">O nome do arquivo é o GUID da versão com a extensão. Extensão DAT.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="ad9bf-287">O motivo pelo qual essa cópia é feita é garantir que o arquivo de Hive real do pacote nunca seja usado, o que impediria a remoção do pacote posteriormente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ad9bf-288">Registry. dat do repositório de pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ad9bf-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="ad9bf-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-290">Quando o primeiro aplicativo do pacote é iniciado no cliente, o cliente prepara ou copia o conteúdo do arquivo hive, recriando os dados do registro do pacote em um local alternativo `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="ad9bf-291">Os dados do registro em estágios têm dois tipos distintos de dados da máquina e dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="ad9bf-292">Os dados da máquina são compartilhados entre todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="ad9bf-293">Os dados do usuário são testados para cada usuário em um local específico do usuário `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="ad9bf-294">Os dados da máquina são removidos basicamente no momento da remoção do pacote e os dados do usuário são removidos em uma operação de cancelamento de usuário do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="ad9bf-295">Transferência do registro do pacote versus transferência do registro do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="ad9bf-296">Quando os grupos de conexão estão presentes, o processo anterior de preparação do registro é verdadeiro, mas em vez de ter um arquivo de Hive para processar, há mais de um.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="ad9bf-297">Os arquivos são processados na ordem em que aparecem no XML do grupo de conexão, com o primeiro autor vencedor de qualquer conflito.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="ad9bf-298">O registro em estágios persiste da mesma maneira que no caso do único pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="ad9bf-299">Os dados do registro do usuário em estágios permanecem para o grupo de conexão até que ele seja desativado; os dados do registro do computador em estágios são removidos na remoção do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="ad9bf-300">Registro virtual</span><span class="sxs-lookup"><span data-stu-id="ad9bf-300">Virtual registry</span></span>

<span data-ttu-id="ad9bf-301">A finalidade do registro virtual (VREG) é fornecer um único modo de exibição mesclado do registro do pacote e do registro nativo para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="ad9bf-302">Ele também fornece a funcionalidade Copy-on-Write (vaca), que é qualquer alteração feita no registro do contexto de um processo virtual é feita para um local vaca separado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="ad9bf-303">Isso significa que o VREG deve combinar até três locais de registro separados em um único modo de exibição com base nos locais preenchidos do registro vaca- &gt; Package- &gt; Native.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="ad9bf-304">Quando for feita uma solicitação para os dados do registro, ele será localizado na ordem até encontrar os dados que ele estava solicitando.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="ad9bf-305">Ou seja, se houver um valor armazenado em um local do vaca, ele não vai para outros locais, no entanto, se não houver dados no local vaca, ele passará para o pacote e, em seguida, a localização nativa até encontrar os dados apropriados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="ad9bf-306">Locais do registro</span><span class="sxs-lookup"><span data-stu-id="ad9bf-306">Registry locations</span></span>

<span data-ttu-id="ad9bf-307">Há dois locais do registro do pacote e dois locais de grupo de conexão onde o cliente App-V armazena as informações do registro, dependendo se o pacote é publicado individualmente ou como parte de um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="ad9bf-308">Há três locais vaca para pacotes e três para grupos de conexão, que são criados e gerenciados pelo VREG.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="ad9bf-309">As configurações de pacotes e grupos de conexão não são compartilhadas:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="ad9bf-310">Pacote único de VReg:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ad9bf-311">Localização</span><span class="sxs-lookup"><span data-stu-id="ad9bf-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ad9bf-312">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ad9bf-313">VACA</span><span class="sxs-lookup"><span data-stu-id="ad9bf-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (processo de elevação do computador somente pode gravar)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-315">Registry\Client\Packages\PkgGUID\REGISTRY do usuário (usuário móvel qualquer coisa escrita em HKCU, exceto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-316">Classes\Client\Packages\PkgGUID\REGISTRY do registro do usuário (HKCU\Software\Classes de gravação e HKLM para processo não elevado)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ad9bf-317">Pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="ad9bf-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-319">Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry do registro do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ad9bf-320">ISCSI</span><span class="sxs-lookup"><span data-stu-id="ad9bf-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-321">Local do registro do aplicativo nativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="ad9bf-322">VReg do grupo de conexão:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ad9bf-323">Localização</span><span class="sxs-lookup"><span data-stu-id="ad9bf-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="ad9bf-324">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ad9bf-325">VACA</span><span class="sxs-lookup"><span data-stu-id="ad9bf-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (processo de elevação do computador somente pode gravar)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-327">Registry\Client\PackageGroups\GrpGUID\REGISTRY do usuário (qualquer coisa escrita para HKCU, exceto Software\Classes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-328">Classes\Client\PackageGroups\GrpGUID\REGISTRY do registro do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ad9bf-329">Pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="ad9bf-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-331">Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY do registro do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ad9bf-332">ISCSI</span><span class="sxs-lookup"><span data-stu-id="ad9bf-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ad9bf-333">Local do registro do aplicativo nativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="ad9bf-334">Há dois locais do vaca para HKLM; processos elevados e não elevados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="ad9bf-335">Processos elevados sempre gravam as alterações de HKLM no vaca seguro em HKLM.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="ad9bf-336">Processos não elevados sempre gravam as alterações de HKLM nas vaca não seguras em HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="ad9bf-337">Quando um aplicativo lê alterações de HKLM, processos elevados lêem alterações do vaca seguro em HKLM.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="ad9bf-338">Leituras não elevadas de ambos, favorecendo as alterações feitas no vaca não seguro primeiro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="ad9bf-339">Teclas de passagem</span><span class="sxs-lookup"><span data-stu-id="ad9bf-339">Pass-through keys</span></span>

<span data-ttu-id="ad9bf-340">As teclas de passagem permitem que um administrador configure determinadas teclas para que elas só possam ser lidas do registro nativo, ignorando os locais do pacote e do vaca.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="ad9bf-341">Locais de passagem são globais para a máquina (não específico do pacote) e podem ser configurados adicionando o caminho à chave, que deve ser tratado como pass-through para o valor **reg \ _MULTI \ _SZ** chamado **PassThroughPaths** da chave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="ad9bf-342">Qualquer chave que aparece sob esse valor de cadeia de caracteres múltipla (e seus filhos) será tratada como pass-through.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="ad9bf-343">Os locais a seguir são configurados como locais de passagem por padrão:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="ad9bf-344">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="ad9bf-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="ad9bf-345">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="ad9bf-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="ad9bf-346">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="ad9bf-347">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="ad9bf-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="ad9bf-348">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="ad9bf-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="ad9bf-349">HKEY \ _CURRENT \ _USER configurações \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet</span><span class="sxs-lookup"><span data-stu-id="ad9bf-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="ad9bf-350">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="ad9bf-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="ad9bf-351">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="ad9bf-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="ad9bf-352">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="ad9bf-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="ad9bf-353">A finalidade das teclas de passagem é garantir que um aplicativo virtual não grave dados do registro no VReg que é necessário para aplicativos não virtuais para operação ou integração bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="ad9bf-354">A chave Policies garante que as configurações baseadas em políticas de grupo definidas pelo administrador sejam utilizadas e não por configurações de pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="ad9bf-355">A chave AppModel é necessária para integração com aplicativos baseados na interface do usuário moderna do Windows.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="ad9bf-356">Recomendamos que a administração não modifique nenhuma das teclas de passagem padrão, mas em alguns casos, com base no comportamento do aplicativo, talvez seja necessário adicionar teclas de passagem adicionais.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="ad9bf-357">Comportamento da loja de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-357">App-V package store behavior</span></span>


<span data-ttu-id="ad9bf-358">O App-V 5 gerencia o repositório de pacotes, que é o local onde os arquivos de ativos expandidos do arquivo do AppV são armazenados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="ad9bf-359">Por padrão, esse local está armazenado em%ProgramData%\\App-V e é limitado em termos de recursos de armazenamento apenas pelo espaço livre em disco.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="ad9bf-360">O repositório do pacote é organizado pelos GUIDs do pacote e da versão, conforme mencionado na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="ad9bf-361">Adicionar pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-361">Add packages</span></span>

<span data-ttu-id="ad9bf-362">Os pacotes do App-V são testados após a adição ao computador com o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="ad9bf-363">O cliente App-V fornece transferência sob demanda.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="ad9bf-364">Durante a publicação ou um Add-AppVClientPackage manual, a estrutura de dados é criada no repositório de pacotes (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="ad9bf-365">Os arquivos de pacote identificados no bloco de publicação definido no StreamMap.xml são adicionados ao sistema e as pastas de nível superior e os arquivos filho testados para garantir que os ativos de aplicativo apropriados existam na inicialização.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="ad9bf-366">Montando pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-366">Mounting packages</span></span>

<span data-ttu-id="ad9bf-367">Os pacotes podem ser carregados explicitamente usando o PowerShell `Mount-AppVClientPackage` ou usando a **interface do usuário do cliente App-V** para baixar um pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="ad9bf-368">Esta operação carrega completamente o pacote inteiro no repositório de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="ad9bf-369">Pacotes de streaming</span><span class="sxs-lookup"><span data-stu-id="ad9bf-369">Streaming packages</span></span>

<span data-ttu-id="ad9bf-370">O cliente App-V pode ser configurado para alterar o comportamento padrão do streaming.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="ad9bf-371">Todas as políticas de streaming são armazenadas na seguinte chave do `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` registro:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="ad9bf-372">As políticas são definidas usando o cmdlet do PowerShell `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="ad9bf-373">As políticas a seguir se aplicam ao streaming:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-374">Política</span><span class="sxs-lookup"><span data-stu-id="ad9bf-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-375">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="ad9bf-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-377">No Windows 8 e posterior, permite o streaming em redes 3G e celulares</span><span class="sxs-lookup"><span data-stu-id="ad9bf-377">On Windows 8 and later, it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-378">Carregar</span><span class="sxs-lookup"><span data-stu-id="ad9bf-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-379">Especifica a configuração de carga em segundo plano:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="ad9bf-380">0 </strong> - desativado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="ad9bf-381">1 </strong> – pacotes usados anteriormente</span><span class="sxs-lookup"><span data-stu-id="ad9bf-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="ad9bf-382">2 </strong> – todos os pacotes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="ad9bf-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-384">A pasta raiz do repositório de pacotes no computador local</span><span class="sxs-lookup"><span data-stu-id="ad9bf-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="ad9bf-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-386">A raiz substitui a do qual os pacotes devem ser transmitidos</span><span class="sxs-lookup"><span data-stu-id="ad9bf-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="ad9bf-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-388">Habilita o uso de repositório de conteúdo compartilhado para cenários de VDI</span><span class="sxs-lookup"><span data-stu-id="ad9bf-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="ad9bf-389">Essas configurações afetam o comportamento dos ativos do pacote do App-V de streaming para o cliente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="ad9bf-390">Por padrão, o App-V só baixa os ativos necessários após o download da publicação inicial e dos blocos de recursos primários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="ad9bf-391">Há três comportamentos específicos em relação aos pacotes de streaming que devem ser explicados:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="ad9bf-392">Streaming em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ad9bf-392">Background Streaming</span></span>

-   <span data-ttu-id="ad9bf-393">Streaming otimizado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-393">Optimized Streaming</span></span>

-   <span data-ttu-id="ad9bf-394">Falhas de fluxo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-394">Stream Faults</span></span>

### <span data-ttu-id="ad9bf-395">Streaming em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ad9bf-395">Background streaming</span></span>

<span data-ttu-id="ad9bf-396">O cmdlet do PowerShell `Get-AppvClientConfiguration` pode ser usado para determinar o modo atual para streaming em segundo plano com a configuração AutoLoad e modificada com o cmdlet Set-AppvClientConfiguration ou a partir do registro (chave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="ad9bf-397">Streaming em segundo plano é uma configuração padrão em que a configuração de AutoLoad está definida para baixar pacotes usados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="ad9bf-398">O comportamento com base na configuração padrão (valor = 1) baixa os blocos de dados do App-V em segundo plano após a inicialização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="ad9bf-399">Essa configuração pode ser desabilitada juntos (valor = 0) ou habilitado para todos os pacotes (valor = 2), se foram iniciados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="ad9bf-400">Streaming otimizado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-400">Optimized streaming</span></span>

<span data-ttu-id="ad9bf-401">Os pacotes do App-V podem ser configurados com um bloco de recursos principal durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="ad9bf-402">Essa configuração permite que o engenheiro de sequenciamento monitore arquivos de inicialização para um aplicativo específico, ou aplicativos, e marque os blocos de dados no pacote App-V para streaming na primeira inicialização de qualquer aplicativo no pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="ad9bf-403">Falhas de fluxo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-403">Stream faults</span></span>

<span data-ttu-id="ad9bf-404">Após o fluxo inicial de todos os dados de publicação e o bloco de recursos principal, as solicitações de arquivos adicionais executam falhas de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="ad9bf-405">Esses blocos de dados são baixados para o repositório de pacotes conforme o necessário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="ad9bf-406">Isso permite que um usuário Baixe apenas uma pequena parte do pacote, geralmente suficiente para iniciar o pacote e executar tarefas normais.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="ad9bf-407">Todos os outros blocos são baixados quando um usuário inicia uma operação que requer dados que não estão no repositório de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="ad9bf-408">Para obter mais informações sobre o compartilhamento de pacotes do App-V, acesse: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="ad9bf-409">O sequenciamento para otimização de transmissão está disponível em: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="ad9bf-410">Atualizações de pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-410">Package upgrades</span></span>

<span data-ttu-id="ad9bf-411">Os pacotes do App-V exigem atualização ao longo do ciclo de vida do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="ad9bf-412">As atualizações do pacote do App-V são semelhantes à operação de publicação do pacote, pois cada versão será criada em seu próprio local PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="ad9bf-413">A operação de atualização é otimizada pela criação de links rígidos para arquivos idênticos e transmitidos de outras versões do mesmo pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="ad9bf-414">Remoção de pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-414">Package removal</span></span>

<span data-ttu-id="ad9bf-415">O comportamento do cliente App-V quando os pacotes são removidos depende do método usado para remoção.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="ad9bf-416">Usando uma infraestrutura completa do App-V para cancelar a publicação do aplicativo, os arquivos de catálogo do usuário (catálogo de computadores para aplicativos publicados globalmente) são removidos, mas retém o local do repositório de pacotes e locais do vaca.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="ad9bf-417">Quando o cmdlet do PowerShell `Remove-AppVClientPackge` é usado para remover um pacote do App-V, o local do repositório de pacotes é limpo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="ad9bf-418">Lembre-se de que cancelar a publicação de um pacote do App-V a partir do servidor de gerenciamento não executa uma operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="ad9bf-419">Nenhuma operação removerá os arquivos de pacote do pacote de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="ad9bf-420">Registro e dados em roaming</span><span class="sxs-lookup"><span data-stu-id="ad9bf-420">Roaming registry and data</span></span>


<span data-ttu-id="ad9bf-421">O App-V 5 pode oferecer uma experiência quase nativa ao fazer roaming, dependendo de como o aplicativo sendo usado é gravado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="ad9bf-422">Por padrão, o App-V roams AppData que está armazenado no local de roaming, com base na configuração de roaming do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="ad9bf-423">Outros locais para armazenamento de dados baseados em arquivos não fazem roaming de um computador para outro, já que eles estão em locais que não estão em roaming.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="ad9bf-424">Requisitos de roaming e armazenamento de dados de catálogo do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="ad9bf-425">O App-V armazena dados, que representam o estado do catálogo do usuário, na forma de:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="ad9bf-426">Arquivos em%appdata%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="ad9bf-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="ad9bf-427">Configurações do registro em</span><span class="sxs-lookup"><span data-stu-id="ad9bf-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="ad9bf-428">Juntos, esses arquivos e configurações do registro representam o catálogo do usuário, portanto ambos devem ser movidos ou não devem ser movidos para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="ad9bf-429">O App-V não oferece suporte a roaming% AppData%, mas não ao roaming do perfil do usuário (registro) ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="ad9bf-430">**Observação**  O cmdlet **Repair-AppvClientPackage** não repara o estado de publicação de pacotes, onde o estado App-V do usuário em `HKEY_CURRENT_USER` está ausente ou incompatível com os dados em% AppData%.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="ad9bf-431">Dados baseados no registro</span><span class="sxs-lookup"><span data-stu-id="ad9bf-431">Registry-based data</span></span>

<span data-ttu-id="ad9bf-432">O roaming do registro do App-V se encaixa em dois cenários, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-433">Cenário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-434">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-435">Aplicativos que são executados como usuários padrão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-436">Quando um usuário padrão inicia um aplicativo App-V, os aplicativos HKLM e HKCU para aplicativos App-V são armazenados no hive HKCU do computador.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="ad9bf-437">Isso apresenta os dois caminhos distintos:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="ad9bf-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="ad9bf-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {userid} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="ad9bf-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="ad9bf-440">Os locais são habilitados para roaming com base nas configurações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-441">Aplicativos executados com elevação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-442">Quando um aplicativo é iniciado com elevação:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="ad9bf-443">Os dados HKLM são armazenados no hive HKLM no computador local</span><span class="sxs-lookup"><span data-stu-id="ad9bf-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-444">Dados HKCU são armazenados no local do registro do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="ad9bf-445">Nesse cenário, essas configurações não estão em roaming com configurações de roaming normal do sistema operacional, e os valores e as chaves do registro resultantes são armazenados no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="ad9bf-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {userid} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="ad9bf-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="ad9bf-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {Usuáriosid} \ SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="ad9bf-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ad9bf-448">App-V e redirecionamento de pastas</span><span class="sxs-lookup"><span data-stu-id="ad9bf-448">App-V and folder redirection</span></span>

<span data-ttu-id="ad9bf-449">O App-V 5,1 dá suporte ao redirecionamento de pastas da pasta Roaming AppData (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-449">App-V 5.1 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="ad9bf-450">Quando o ambiente virtual é iniciado, o estado roaming de AppData do diretório roaming do usuário é copiado para o cache local.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="ad9bf-451">Por outro lado, quando o ambiente virtual é desligado, o cache local que está associado a um usuário específico do roaming de um usuário é transferido para o local real do diretório de AppData do roaming do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="ad9bf-452">Um pacote típico tem vários locais mapeados no repositório de backup do usuário para configurações em AppData\\Local e AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="ad9bf-453">Esses locais são a cópia em locais de gravação que são armazenados por usuário no perfil do usuário, e que são usados para armazenar alterações feitas nos diretórios do pacote do VFS e para proteger o pacote VFS padrão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="ad9bf-454">A tabela a seguir mostra locais locais e de roaming, quando o redirecionamento de pastas não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-455">Diretório VFS no pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-456">Local mapeado do repositório de backup</span><span class="sxs-lookup"><span data-stu-id="ad9bf-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-458">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-460">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-461">Windows</span><span class="sxs-lookup"><span data-stu-id="ad9bf-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-462">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; \Windows do GUID &gt;</span><span class="sxs-lookup"><span data-stu-id="ad9bf-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-464">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-465">AppData</span><span class="sxs-lookup"><span data-stu-id="ad9bf-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-466">C:\users\jsmith\AppData &lt; forte &gt; </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID de &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="ad9bf-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="ad9bf-467">A tabela a seguir mostra locais locais e de roaming, quando o redirecionamento de pastas foi implementado para% AppData% e o local foi redirecionado (geralmente para um local de rede).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-468">Diretório VFS no pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-469">Local mapeado do repositório de backup</span><span class="sxs-lookup"><span data-stu-id="ad9bf-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-471">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-473">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="ad9bf-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-474">Windows</span><span class="sxs-lookup"><span data-stu-id="ad9bf-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-475">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; \Windows do GUID &gt;</span><span class="sxs-lookup"><span data-stu-id="ad9bf-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-477">C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="ad9bf-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-478">AppData</span><span class="sxs-lookup"><span data-stu-id="ad9bf-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="ad9bf-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID de &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="ad9bf-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="ad9bf-480">O driver VFS do cliente App-V atual não pode gravar em locais de rede, portanto, o cliente App-V detecta a presença do redirecionamento de pasta e copia os dados na unidade local durante a publicação e quando o ambiente virtual é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="ad9bf-481">Depois que o usuário fechar o aplicativo App-V e o cliente App-V fechar o ambiente virtual, o armazenamento local do VFS AppData será copiado novamente para a rede, permitindo o roaming para outras máquinas, onde o processo será repetido.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="ad9bf-482">As etapas detalhadas dos processos são:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="ad9bf-483">Durante a publicação ou a inicialização do ambiente virtual, o cliente App-V detecta a localização do diretório AppData.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="ad9bf-484">Se o caminho de AppData do roaming for local ou ino local AppData\\Roaming for mapeado, nada acontecerá.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="ad9bf-485">Se o caminho de AppData do roaming não for local, o diretório VFS AppData será mapeado para o diretório local AppData.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="ad9bf-486">Esse processo resolve o problema de um% AppData% não local que não é suportado pelo driver VFS do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="ad9bf-487">No entanto, os dados armazenados nesse novo local não são movidos com o redirecionamento de pastas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="ad9bf-488">Todas as alterações durante a execução do aplicativo acontecem para o local AppData local e devem ser copiadas para o local redirecionado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="ad9bf-489">As etapas detalhadas desse processo são:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="ad9bf-490">Aplicativo App-V está desligado, o que desliga o ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="ad9bf-491">O cache local do local de AppData do roaming é compactado e armazenado em um arquivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="ad9bf-492">Um carimbo de data/hora no final do processo de empacotamento ZIP é usado para nomear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="ad9bf-493">O carimbo de data/hora é registrado no registro: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime como o último carimbo de data/hora conhecido do AppData.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="ad9bf-494">O processo de redirecionamento de pastas é chamado para avaliar e iniciar o arquivo ZIP carregado no diretório roaming AppData.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="ad9bf-495">O carimbo de data/hora é usado para determinar um cenário "último gravador WINS" se houver um conflito e usado para otimizar o download dos dados quando o aplicativo App-V for publicado ou o ambiente virtual for iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="ad9bf-496">O redirecionamento de pastas disponibilizará os dados de qualquer outro cliente coberto pela política de suporte e iniciará o processo de armazenamento dos dados do AppData\\Roaming no local AppData local no cliente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="ad9bf-497">Os processos detalhados são:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="ad9bf-498">O usuário inicia o ambiente virtual iniciando um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="ad9bf-499">O ambiente virtual do aplicativo verifica o arquivo ZIP com carimbo de data/hora mais recente, se houver.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="ad9bf-500">O registro é verificado para o último carimbo de data/hora carregado conhecido, se houver.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="ad9bf-501">O arquivo ZIP mais recente é baixado, a menos que o último carimbo de data/hora de carregamento conhecido seja maior ou igual ao carimbo de data/hora do arquivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="ad9bf-502">Se o último carimbo de data/hora de carregamento conhecido local for anterior ao do arquivo ZIP mais recente no local roaming AppData, o arquivo ZIP será extraído para o diretório Temp local no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="ad9bf-503">Depois que o arquivo ZIP é extraído com êxito, o cache local do diretório roaming AppData é renomeado e os novos dados são movidos para o lugar.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="ad9bf-504">O diretório renomeado é excluído e o aplicativo é aberto com os dados de roaming salvos mais recentemente salvos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="ad9bf-505">Isso conclui o roaming bem-sucedido das configurações do aplicativo que estão presentes nos locais do AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="ad9bf-506">A única outra condição que deve ser abordada é uma operação de reparo do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="ad9bf-507">Os detalhes do processo são:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-507">The details of the process are:</span></span>

1.  <span data-ttu-id="ad9bf-508">Durante o reparo, detecte se o caminho do diretório de AppData do roaming do usuário não é local.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="ad9bf-509">Mapear os destinos de caminho do roaming de AppData não locais são recriados os locais esperados de sites de mesmo roaming e locais.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="ad9bf-510">Exclua o carimbo de data/hora armazenado no registro, se houver.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="ad9bf-511">Esse processo recriará os locais locais e de rede para AppData e removerá o registro do registro do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="ad9bf-512">Gerenciamento do ciclo de vida do aplicativo cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="ad9bf-513">Em uma infraestrutura completa do App-V, após os aplicativos serem sequenciados, eles são gerenciados e publicados em usuários ou computadores por meio dos servidores de gerenciamento e publicação do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="ad9bf-514">Esta seção detalha as operações que ocorrem durante as operações do ciclo de vida do aplicativo comum do App-V (adicionar, publicar, iniciar, atualizar e remover) e os locais de arquivo e registro que são alterados e modificados da perspectiva do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="ad9bf-515">As operações do cliente App-V são executadas como uma série de comandos do PowerShell iniciada no computador executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="ad9bf-516">Este documento enfoca as soluções de infraestrutura completa do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="ad9bf-517">Para obter informações específicas sobre a integração do App-V com o Configuration Manager 2012, acesse: <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="ad9bf-518">As tarefas do ciclo de vida do aplicativo App-V são disparadas no logon do usuário (padrão), na inicialização da máquina ou nas operações com tempo de tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="ad9bf-519">As configurações para as operações do cliente App-V, incluindo servidores de publicação, intervalos de atualização, habilitação de script de pacote e outros, são configuradas durante a configuração do cliente ou pós-instalação com comandos do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="ad9bf-520">Consulte a seção como implantar o cliente no TechNet em: [como implantar o cliente App-V](how-to-deploy-the-app-v-client-51gb18030.md) ou usar o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="ad9bf-521">Atualização de publicação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-521">Publishing refresh</span></span>

<span data-ttu-id="ad9bf-522">O processo de atualização de publicação é composto por várias operações menores que são executadas no cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="ad9bf-523">Como o App-V é uma tecnologia de virtualização de aplicativos e não uma tecnologia de agendamento de tarefas, o Agendador de tarefas do Windows é usado para habilitar o processo no logon do usuário, na inicialização da máquina e em intervalos agendados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="ad9bf-524">A configuração do cliente durante a configuração listada acima é o método preferencial ao distribuir o cliente para um grupo grande de computadores com as configurações corretas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="ad9bf-525">Essas configurações de cliente podem ser configuradas com os seguintes cmdlets do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="ad9bf-526">**Add-AppVPublishingServer:** Configura o cliente com um servidor de publicação App-V que fornece pacotes do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="ad9bf-527">**Set-AppVPublishingServer:** Modifica as configurações atuais para o servidor de publicação App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="ad9bf-528">**Set-AppVClientConfiguration:** Modifica as configurações atuais para o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="ad9bf-529">**Sync-AppVPublishingServer:** Inicia um processo de atualização de publicação do App-V manualmente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="ad9bf-530">Isso também é usado nas tarefas agendadas criadas durante a configuração do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="ad9bf-531">O foco das seções a seguir é detalhando as operações que ocorrem durante diferentes fases de uma atualização de publicação do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="ad9bf-532">Os tópicos incluem:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-532">The topics include:</span></span>

-   <span data-ttu-id="ad9bf-533">Adicionando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="ad9bf-534">Publicando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="ad9bf-535">Adicionando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-535">Adding an App-V package</span></span>

<span data-ttu-id="ad9bf-536">Adicionar um pacote do App-V ao cliente é a primeira etapa do processo de atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="ad9bf-537">O resultado final é o mesmo que o `Add-AppVClientPackage` cmdlet no PowerShell, exceto durante o processo de adição de atualização de publicação, o servidor de publicação configurado é contatado e passa uma lista de alto nível de aplicativos de volta para o cliente para obter informações mais detalhadas e não um único pacote Adicionar operação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="ad9bf-538">O processo continua Configurando adições ou atualizações do cliente para pacote ou grupo de conexão e, em seguida, acessa o arquivo do AppV.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="ad9bf-539">Em seguida, o conteúdo do arquivo do AppV é expandido e colocado no sistema operacional local nos locais apropriados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="ad9bf-540">Veja a seguir um fluxo de trabalho detalhado do processo, presumindo que o pacote esteja configurado para streaming de falhas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="ad9bf-541">Como adicionar um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="ad9bf-542">Início manual via PowerShell ou início de sequência de tarefas do processo de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="ad9bf-543">O cliente App-V faz uma conexão HTTP e solicita uma lista de aplicativos com base no destino.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="ad9bf-544">O processo de atualização de publicação dá suporte a máquinas ou usuários de destino.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="ad9bf-545">O servidor de publicação App-V usa a identidade do destino de inicialização, usuário ou computador e consulta o banco de dados para obter uma lista de aplicativos qualificados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="ad9bf-546">A lista de aplicativos é fornecida como uma resposta XML, que o cliente usa para enviar solicitações adicionais ao servidor para obter mais informações com base em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="ad9bf-547">O agente de publicação no cliente App-V executa todas as ações abaixo de serializadas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="ad9bf-548">Avalie todos os grupos de conexão que são cancelados ou desativados, pois as atualizações de versão de pacote que fazem parte do grupo de conexão não podem ser processadas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="ad9bf-549">Configure os pacotes identificando as operações de adição ou atualização.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="ad9bf-550">O cliente App-V usa a API AppX do Windows e acessa o arquivo do AppV a partir do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="ad9bf-551">O arquivo de pacote é aberto e o AppXManifest.xml e os StreamMap.xml são baixados para o armazenamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="ad9bf-552">Dados de bloco de publicação de fluxo completamente definidos no StreamMap.xml.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="ad9bf-553">Armazena os dados do bloco de publicação no pacote Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="ad9bf-554">Ícones: destinos de pontos de extensão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="ad9bf-555">Cabeçalhos executáveis portáteis (cabeçalhos PE): alvos de pontos de extensão que contêm as informações básicas sobre a imagem necessária em disco, acessados diretamente ou por meio de tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="ad9bf-556">Scripts: baixar o diretório de scripts para uso em todo o processo de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="ad9bf-557">Preencha o repositório de pacotes:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="ad9bf-558">Crie arquivos esparsos em disco que representem o pacote extraído para qualquer diretório listado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="ad9bf-559">Estágio arquivos e diretórios de nível superior em root.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="ad9bf-560">Todos os outros arquivos são criados quando o diretório é listado como esparso em disco e em fluxo por demanda.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="ad9bf-561">Criar as entradas do catálogo da máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-561">Create the machine catalog entries.</span></span> <span data-ttu-id="ad9bf-562">Crie o Manifest.xml e DeploymentConfiguration.xml a partir dos arquivos de pacote (se nenhum arquivo de DeploymentConfiguration.xml no pacote tiver sido criado um espaço reservado).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="ad9bf-563">Criar local do repositório de pacotes no registro HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span><span class="sxs-lookup"><span data-stu-id="ad9bf-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="ad9bf-564">Crie o arquivo Registry. dat do pacote de armazenamento para%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="ad9bf-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="ad9bf-565">Registrar o pacote com o driver do modo kernel do App-V HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="ad9bf-566">Invoque o script do arquivo AppxManifest.xml ou DeploymentConfig.xml para adicionar intervalo ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="ad9bf-567">Configurar grupos de conexão adicionando e habilitando ou desabilitando.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="ad9bf-568">Remover objetos que não são publicados no destino (usuário ou computador).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="ad9bf-569">**Observação**  Isso não executará uma exclusão de pacote, mas, em vez disso, removerá pontos de integração para o destino específico (usuário ou computador) e removerá arquivos de catálogo do usuário (arquivos de catálogo do computador para publicação global).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="ad9bf-570">Invocar a montagem da carga em segundo plano com base na configuração do cliente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="ad9bf-571">Os pacotes que já têm informações de publicação para a máquina ou usuário são restaurados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="ad9bf-572">**Observação**  Essa condição ocorre como um produto de remoção sem cancelar a publicação com a adição de plano de fundo do pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="ad9bf-573">Isso conclui um pacote App-V Add do processo de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="ad9bf-574">A próxima etapa é publicar o pacote para o destino específico (computador ou usuário).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![pacote adicionar dados de arquivo e registro](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="ad9bf-576">Publicando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-576">Publishing an App-V package</span></span>

<span data-ttu-id="ad9bf-577">Durante a operação de atualização de publicação, a operação de publicação específica (Publish-AppVClientPackage) adiciona entradas ao catálogo do usuário, mapeia a qualificação ao usuário, identifica o repositório local e termina ao completar qualquer etapa de integração.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="ad9bf-578">Veja a seguir as etapas detalhadas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="ad9bf-579">Como publicar e o pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="ad9bf-580">Entradas de pacote são adicionadas ao catálogo de usuários</span><span class="sxs-lookup"><span data-stu-id="ad9bf-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="ad9bf-581">Pacotes direcionados pelo usuário: o UserDeploymentConfiguration.xml e os UserManifest.xml são colocados na máquina no catálogo do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="ad9bf-582">Pacotes direcionados por máquina (global): o UserDeploymentConfiguration.xml é colocado no catálogo do computador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="ad9bf-583">Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="ad9bf-584">Executar tarefas de integração.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="ad9bf-585">Criar pontos de extensão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-585">Create extension points.</span></span>

    2.  <span data-ttu-id="ad9bf-586">Armazene informações de backup no registro do usuário e perfil móvel (backups de atalho).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="ad9bf-587">**Observação**  Isso permite que os pontos de extensão da restauração se o pacote seja cancelado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="ad9bf-588">Executar scripts destinados para a publicação do tempo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="ad9bf-589">Publicar um pacote do App-V que faz parte de um grupo de conexão é muito semelhante ao processo acima.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="ad9bf-590">Para grupos de conexão, o caminho que armazena as informações específicas do catálogo inclui PackageGroups como um filho do diretório de catálogo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="ad9bf-591">Examine as informações de catálogo do computador e dos usuários acima para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-591">Review the machine and users catalog information above for details.</span></span>

![pacote adicionar dados de arquivo e registro-global](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="ad9bf-593">Início do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-593">Application launch</span></span>

<span data-ttu-id="ad9bf-594">Após o processo de atualização de publicação, o usuário é iniciado e reinicia subseqüentemente um aplicativo App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="ad9bf-595">O processo é muito simples e otimizado para iniciar rapidamente com um mínimo de tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="ad9bf-596">O cliente App-V verifica o caminho para o catálogo do usuário em busca de arquivos criados durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="ad9bf-597">Depois que os direitos para iniciar o pacote são estabelecidos, o cliente App-V cria um ambiente virtual, começa a transmitir os dados necessários e aplica os arquivos de manifesto e de configuração de implantação apropriados durante a criação do ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="ad9bf-598">Com o ambiente virtual criado e configurado para o pacote e o aplicativo específico, o aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="ad9bf-599">Como iniciar aplicativos App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="ad9bf-600">O usuário inicia o aplicativo clicando em um atalho ou em uma chamada de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="ad9bf-601">O cliente App-V Verifica a existência no catálogo do usuário para os seguintes arquivos</span><span class="sxs-lookup"><span data-stu-id="ad9bf-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="ad9bf-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="ad9bf-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="ad9bf-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="ad9bf-604">Se os arquivos estiverem presentes, o aplicativo será qualificado para esse usuário específico, e o aplicativo iniciará o processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="ad9bf-605">Não há tráfego de rede neste ponto.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="ad9bf-606">Em seguida, o cliente App-V Verifica se o caminho do pacote registrado para o serviço do cliente App-V está localizado no registro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="ad9bf-607">Ao encontrar o caminho para o repositório de pacotes, o ambiente virtual é criado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="ad9bf-608">Se esta for a primeira inicialização, o bloco de recursos principal será baixado, se houver.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="ad9bf-609">Após o download, o serviço App-V cliente consome os arquivos de manifesto e de configuração de implantação para configurar o ambiente virtual e todos os subsistemas do App-V são carregados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="ad9bf-610">O aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-610">The Application launches.</span></span> <span data-ttu-id="ad9bf-611">Para todos os arquivos ausentes no repositório de pacotes (arquivos esparsos), o App-V transmitirá falhas nos arquivos de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![pacote Adicionar arquivo e dados do registro-Stream](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="ad9bf-613">Atualizando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-613">Upgrading an App-V package</span></span>

<span data-ttu-id="ad9bf-614">O processo de atualização do pacote do App-V 5 é diferente das versões mais antigas do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="ad9bf-615">O App-V oferece suporte a várias versões do mesmo pacote em um computador qualificado para usuários diferentes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="ad9bf-616">Versões de pacote podem ser adicionadas a qualquer momento, pois o repositório de pacotes e os catálogos são atualizados com os novos recursos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="ad9bf-617">O único processo específico para a adição de novos recursos de versão é a otimização do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="ad9bf-618">Durante uma atualização, somente os novos arquivos são adicionados ao novo local de armazenamento de versão, e os links físicos são criados para arquivos inalterados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="ad9bf-619">Isso reduz o armazenamento geral apenas apresentando o arquivo em um local de disco e projeta-o em todas as pastas com uma entrada de local de arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="ad9bf-620">Os detalhes específicos da atualização de um pacote do App-V são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="ad9bf-621">Como atualizar um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="ad9bf-622">O cliente App-V executa uma atualização de publicação e descobre uma versão mais recente de um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="ad9bf-623">Entradas de pacote são adicionadas ao catálogo apropriado para a nova versão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="ad9bf-624">Pacotes direcionados pelo usuário: o UserDeploymentConfiguration.xml e os UserManifest.xml são colocados na máquina no catálogo do usuário em appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="ad9bf-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="ad9bf-625">Pacotes direcionados pelo computador (global): o UserDeploymentConfiguration.xml é colocado no catálogo do computador em%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="ad9bf-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="ad9bf-626">Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="ad9bf-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="ad9bf-627">Executar tarefas de integração.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="ad9bf-628">Integre os pontos de extensão (EP) a partir dos arquivos de manifesto e de configuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="ad9bf-629">Os dados do EP baseados em arquivos são armazenados na pasta AppData usando pontos de junção do armazenamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="ad9bf-630">A versão 1 EPs já existe quando uma nova versão se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="ad9bf-631">Os pontos de extensão são alternados para o local da versão 2 no computador ou catálogos do usuário para qualquer ponto de extensão mais recente ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="ad9bf-632">Executar scripts destinados para a publicação do tempo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="ad9bf-633">Instale montagens lado a lado conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="ad9bf-634">Atualizando um pacote App-V em uso</span><span class="sxs-lookup"><span data-stu-id="ad9bf-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="ad9bf-635">A **partir do App-V 5 SP2**: se você tentar atualizar um pacote que está sendo usado por um usuário final, a tarefa de atualização será colocada em um estado pendente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="ad9bf-636">A atualização será executada mais tarde, de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-637">Tipo de tarefa</span><span class="sxs-lookup"><span data-stu-id="ad9bf-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-638">Regra aplicável</span><span class="sxs-lookup"><span data-stu-id="ad9bf-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-639">Tarefa baseada em usuário, por exemplo, publicar um pacote para um usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-640">A tarefa pendente será executada após o usuário fazer logoff e, em seguida, fazer logon novamente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-641">Tarefa com base global, por exemplo, habilitar um grupo de conexão globalmente</span><span class="sxs-lookup"><span data-stu-id="ad9bf-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-642">A tarefa pendente será executada quando o computador for desligado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-643">Quando uma tarefa é colocada em um estado pendente, o cliente App-V também gera uma chave do registro para a tarefa pendente, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-644">Tarefa baseada em usuário ou globalmente</span><span class="sxs-lookup"><span data-stu-id="ad9bf-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-645">Onde a chave do registro é gerada</span><span class="sxs-lookup"><span data-stu-id="ad9bf-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-646">Tarefas baseadas em usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="ad9bf-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-648">Tarefas com base global</span><span class="sxs-lookup"><span data-stu-id="ad9bf-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="ad9bf-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-650">As seguintes operações devem ser concluídas para que os usuários possam usar a versão mais recente do pacote:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-651">Tarefa</span><span class="sxs-lookup"><span data-stu-id="ad9bf-651">Task</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-652">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ad9bf-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-653">Adicionar o pacote ao computador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-654">Esta tarefa é específica do computador e você pode executá-la a qualquer momento, completando as etapas na seção Adicionar pacote acima.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-655">Publicar o pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-656">Consulte a seção publicação do pacote acima para ver as etapas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="ad9bf-657">Esse processo requer que você atualize os pontos de extensão no sistema.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="ad9bf-658">Os usuários finais não podem usar o aplicativo quando você concluir essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ad9bf-659">Use os cenários de exemplo a seguir como um guia para a atualização de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-660">Cenário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-661">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9bf-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-662">O pacote do App-V não está em uso quando você tenta atualizar</span><span class="sxs-lookup"><span data-stu-id="ad9bf-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-663">Nenhum dos seguintes componentes do pacote pode estar em uso: aplicativo virtual, servidor COM ou extensões Shell.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="ad9bf-664">O administrador publica uma versão mais recente do pacote e a atualização funciona da próxima vez que um componente ou aplicativo dentro do pacote for iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="ad9bf-665">A nova versão do pacote é transmitida e executada.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="ad9bf-666">Nada mudou nesse cenário no App-V 5 SP2 de versões anteriores do App-V 5.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-667">O pacote do App-V está em uso quando o administrador publica uma versão mais recente do pacote</span><span class="sxs-lookup"><span data-stu-id="ad9bf-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-668">A operação de atualização é definida como pendente pelo cliente App-V, o que significa que ele é enfileirado e executado mais tarde quando o pacote não está em uso.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="ad9bf-669">Se o aplicativo do pacote estiver em uso, o usuário desliga o aplicativo virtual, após o qual a atualização pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="ad9bf-670">Se o pacote tiver extensões Shell (Office 2013), que são carregadas permanentemente pelo Windows Explorer, o usuário não pode estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="ad9bf-671">Os usuários devem fazer logoff e fazer logon novamente para iniciar a atualização do pacote App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ad9bf-672">Publicação global versus usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-672">Global vs user publishing</span></span>

<span data-ttu-id="ad9bf-673">Os pacotes do App-V podem ser publicados de uma das duas maneiras: Usuário que entitula um pacote App-V para um usuário ou grupo de usuários específico que entitula o pacote App-V para o computador inteiro para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="ad9bf-674">Uma vez que a atualização do pacote está pendente, e o pacote do App-V não está em uso, considere os dois tipos de publicação:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="ad9bf-675">**Publicado globalmente**: o aplicativo é publicado em um computador; todos os usuários desse computador podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="ad9bf-676">A atualização ocorrerá quando o serviço do cliente App-V for iniciado, o que significa efetivamente uma reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="ad9bf-677">**Usuário publicado**: o aplicativo é publicado para um usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="ad9bf-678">Se houver vários usuários na máquina, o aplicativo poderá ser publicado em um subconjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="ad9bf-679">A atualização ocorrerá quando o usuário fizer logon ou quando for publicada novamente (periodicamente, atualização e avaliação de política do ConfigMgr, ou uma publicação/atualização periódica do App-V, ou explicitamente via comandos do PowerShell).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="ad9bf-680">Como remover um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-680">Removing an App-V package</span></span>

<span data-ttu-id="ad9bf-681">Remover aplicativos do App-V em uma infraestrutura completa é uma operação de cancelamento de publicação e não executa uma remoção de pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="ad9bf-682">O processo é o mesmo que o processo de publicação acima, mas em vez de adicionar o processo de remoção reverte as alterações que foram feitas para pacotes do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="ad9bf-683">Reparando um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-683">Repairing an App-V package</span></span>

<span data-ttu-id="ad9bf-684">A operação de reparo é muito simples, mas pode afetar muitos locais na máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="ad9bf-685">Os locais de cópia em gravação (vaca) mencionados anteriormente são removidos e os pontos de extensão são desintegrados e, em seguida, integrados novamente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="ad9bf-686">Revise os locais de posicionamento de dados do vaca revisando o local onde estão registrados no registro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="ad9bf-687">Esta operação é feita automaticamente e não há controle administrativo além de iniciar uma operação de reparo no console do cliente App-V ou via PowerShell (Repair-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="ad9bf-688">Integração de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="ad9bf-688">Integration of App-V packages</span></span>


<span data-ttu-id="ad9bf-689">A arquitetura do cliente App-V e do pacote fornece integração específica com o sistema operacional local durante a adição e a publicação de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="ad9bf-690">Três arquivos definem os pontos de integração ou de extensão para um pacote do App-V:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="ad9bf-691">AppXManifest.xml: armazenados dentro do pacote com cópias de fallback armazenadas no repositório de pacotes e no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="ad9bf-692">Contém as opções criadas durante o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="ad9bf-693">DeploymentConfig.xml: fornece informações de configuração de pontos de extensão de integração com base em computador e usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="ad9bf-694">UserConfig.xml: um subconjunto do Deploymentconfig.xml que fornece apenas configurações baseadas em usuário e direciona somente pontos de extensão baseados em usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="ad9bf-695">Regras de integração</span><span class="sxs-lookup"><span data-stu-id="ad9bf-695">Rules of integration</span></span>

<span data-ttu-id="ad9bf-696">Quando os aplicativos do App-V são publicados em um computador com o cliente App-V, algumas ações específicas são feitas conforme descrito na lista abaixo:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="ad9bf-697">Publicação global: os atalhos são armazenados no local do perfil todos os usuários e outros pontos de extensão são armazenados no registro no hive HKLM.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="ad9bf-698">Publicação do usuário: os atalhos são armazenados no perfil atual da conta do usuário e outros pontos de extensão são armazenados no registro no hive HKCU.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="ad9bf-699">Backup e restauração: os dados de aplicativos nativos existentes e o registro (como registros FTA) são incluídos durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="ad9bf-700">Os pacotes do App-V recebem Propriedade com base no último pacote integrado em que a propriedade é passada para o aplicativo App-V publicado mais recente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="ad9bf-701">As transferências de propriedade de um pacote App-V para outro quando o pacote App-V proprietário é cancelado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="ad9bf-702">Isso não irá iniciar uma restauração dos dados ou do registro.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="ad9bf-703">Restaure os dados de backup quando o último pacote for cancelado ou removido por cada ponto de extensão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="ad9bf-704">Pontos de extensão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-704">Extension points</span></span>

<span data-ttu-id="ad9bf-705">Os arquivos de publicação do App-V (manifesto e configuração dinâmica) fornecem vários pontos de extensão que permitem que o aplicativo se integre com o sistema operacional local.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="ad9bf-706">Esses pontos de extensão executam tarefas típicas de instalação do aplicativo, como o posicionamento de atalhos, a criação de associações de tipo de arquivo e o registro de componentes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="ad9bf-707">Como esses são aplicativos virtualizados que não são instalados da mesma maneira em um aplicativo tradicional, há algumas diferenças.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="ad9bf-708">Veja a seguir uma lista de pontos de extensão abordados nesta seção:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="ad9bf-709">Teclado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-709">Shortcuts</span></span>

-   <span data-ttu-id="ad9bf-710">Associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-710">File Type Associations</span></span>

-   <span data-ttu-id="ad9bf-711">Extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="ad9bf-711">Shell Extensions</span></span>

-   <span data-ttu-id="ad9bf-712">COM</span><span class="sxs-lookup"><span data-stu-id="ad9bf-712">COM</span></span>

-   <span data-ttu-id="ad9bf-713">Clientes de software</span><span class="sxs-lookup"><span data-stu-id="ad9bf-713">Software Clients</span></span>

-   <span data-ttu-id="ad9bf-714">Funcionalidades do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-714">Application capabilities</span></span>

-   <span data-ttu-id="ad9bf-715">Manipulador de protocolo de URL</span><span class="sxs-lookup"><span data-stu-id="ad9bf-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="ad9bf-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="ad9bf-716">AppPath</span></span>

-   <span data-ttu-id="ad9bf-717">Aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="ad9bf-717">Virtual Application</span></span>

### <span data-ttu-id="ad9bf-718">Teclado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-718">Shortcuts</span></span>

<span data-ttu-id="ad9bf-719">O corte curto é um dos elementos básicos da integração com o sistema operacional e é a interface para a inicialização direta do usuário de um aplicativo App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="ad9bf-720">Durante a publicação e a publicação de aplicativos App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="ad9bf-721">No manifesto do pacote e nos arquivos XML de configuração dinâmica, o caminho para um executável do aplicativo específico pode ser encontrado em uma seção semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="ad9bf-722">Conforme mencionado anteriormente, os atalhos do App-V são colocados por padrão no perfil do usuário com base na operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="ad9bf-723">Atualização global locais os atalhos no perfil todos os usuários e na atualização do usuário os armazena no perfil do usuário específico.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="ad9bf-724">O executável real é armazenado no repositório de pacotes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="ad9bf-725">O local do arquivo ICO é um local com token no pacote App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="ad9bf-726">Associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-726">File type associations</span></span>

<span data-ttu-id="ad9bf-727">O cliente App-V gerencia as associações de tipo de arquivo do sistema operacional local durante a publicação, o que permite que os usuários usem invocações de tipo de arquivo ou abram um arquivo com uma extensão especialmente registrada (. docx) para iniciar um aplicativo App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="ad9bf-728">As associações de tipo de arquivo estão presentes nos arquivos de configuração dinâmica e manifesto, conforme representado no exemplo abaixo:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="ad9bf-729">**Observação**  Neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="ad9bf-730">é a extensão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="ad9bf-731">é o valor ProgId (que aponta para o ProgId adjacente)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="ad9bf-732">é a linha de comando, que aponta para o executável do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="ad9bf-733">Extensões de shell</span><span class="sxs-lookup"><span data-stu-id="ad9bf-733">Shell extensions</span></span>

<span data-ttu-id="ad9bf-734">Extensões do shell são incorporadas ao pacote automaticamente durante o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="ad9bf-735">Quando o pacote é publicado globalmente, a extensão do shell oferece aos usuários a mesma funcionalidade que se o aplicativo fosse instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="ad9bf-736">O aplicativo não requer configuração adicional ou configuração no cliente para habilitar a funcionalidade de extensão do Shell.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="ad9bf-737">Requisitos para usar extensões do Shell:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="ad9bf-738">Os pacotes que contêm extensões de shell inseridas devem ser publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="ad9bf-739">O "" bits "do aplicativo, o Sequencer e o cliente App-V devem corresponder ou as extensões do shell não funcionarão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="ad9bf-740">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-740">For example:</span></span>

    -   <span data-ttu-id="ad9bf-741">A versão do aplicativo é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="ad9bf-742">O sequenciador está em execução em um computador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="ad9bf-743">O pacote está sendo entregue a um computador cliente do App-V do 64-bit.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="ad9bf-744">A tabela a seguir exibe as extensões do shell com suporte.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-745">Manipulação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-746">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad9bf-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-747">Manipulador de menu de contexto</span><span class="sxs-lookup"><span data-stu-id="ad9bf-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-748">Adiciona itens de menu ao menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="ad9bf-749">Ele é chamado antes de o menu de contexto ser exibido.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-750">Manipulador de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="ad9bf-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-751">Controla a ação ao clicar com o botão direito do mouse no recurso arrastar-e-soltar e modifica o menu de contexto exibido.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-752">Manipulador de destino soltar</span><span class="sxs-lookup"><span data-stu-id="ad9bf-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-753">Controla a ação após um objeto de dados ser arrastado e solto em um destino de soltura, como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-754">Manipulador de objeto de dados</span><span class="sxs-lookup"><span data-stu-id="ad9bf-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-755">Controla a ação após um arquivo ser copiado para a área de transferência ou arrastado e solto em um destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="ad9bf-756">Ele pode fornecer formatos de área de transferência adicionais para o destino de soltura.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-757">Manipulador de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="ad9bf-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-758">Substitui ou adiciona páginas à caixa de diálogo folha de propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-759">Manipulador InfoTip</span><span class="sxs-lookup"><span data-stu-id="ad9bf-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-760">Permite a recuperação de sinalizadores e informações de infotip de um item e a exibição dentro de uma dica de ferramenta pop-up ao focalizar o mouse.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-761">Manipulador de colunas</span><span class="sxs-lookup"><span data-stu-id="ad9bf-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-762">Permite criar e exibir colunas personalizadas no modo de exibição de detalhes do Windows Explorer <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="ad9bf-763">Ele pode ser usado para estender a classificação e o agrupamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-764">Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="ad9bf-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-765">Permite que uma visualização de um arquivo seja exibida no painel de visualização do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ad9bf-766">COM</span><span class="sxs-lookup"><span data-stu-id="ad9bf-766">COM</span></span>

<span data-ttu-id="ad9bf-767">O cliente App-V dá suporte a aplicativos de publicação com suporte para integração COM e virtualização.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="ad9bf-768">A integração COM permite que o cliente App-V Registre objetos COM no sistema operacional local e virtualização dos objetos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="ad9bf-769">Para os fins deste documento, a integração de objetos COM requer detalhe adicional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="ad9bf-770">O App-V oferece suporte ao registro de objetos COM do pacote para o sistema operacional local com dois tipos de processo: fora de processo e em processo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="ad9bf-771">O registro de objetos COM é realizado com uma ou uma combinação de vários modos de operação para um pacote App-V específico que inclui desativado, isolado e integrado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="ad9bf-772">O modo integrado é configurado para o tipo fora de processo ou no processo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="ad9bf-773">A configuração dos modos de COM e tipos é realizada com arquivos de configuração dinâmica (deploymentconfig.xml ou userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="ad9bf-774">Detalhes sobre a integração do App-V estão disponíveis em: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="ad9bf-775">Recursos de aplicativos e clientes de software</span><span class="sxs-lookup"><span data-stu-id="ad9bf-775">Software clients and application capabilities</span></span>

<span data-ttu-id="ad9bf-776">O App-V dá suporte a clientes de software e pontos de extensão de recursos de aplicativo específicos que permitem que aplicativos virtualizados sejam registrados com o cliente de software do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="ad9bf-777">Isso permite que os usuários selecionem programas padrão para operações como emails, mensagens instantâneas e Media Player.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="ad9bf-778">Essa operação é realizada no painel de controle com o botão Definir acesso do programa e padrões do computador e é configurado durante o sequenciamento nos arquivos de manifesto ou de configuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="ad9bf-779">Os recursos do aplicativo só têm suporte quando os aplicativos do App-V são publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="ad9bf-780">Exemplo de registro de cliente de software de um cliente de email baseado em App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="ad9bf-781">**Observação**  Neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="ad9bf-782">é a configuração geral dos clientes de software para integrar clientes de email</span><span class="sxs-lookup"><span data-stu-id="ad9bf-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="ad9bf-783">é o sinalizador para definir um cliente de email específico como o cliente de email padrão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="ad9bf-784">é o registro de dll MAPI</span><span class="sxs-lookup"><span data-stu-id="ad9bf-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="ad9bf-785">Manipulador de protocolo de URL</span><span class="sxs-lookup"><span data-stu-id="ad9bf-785">URL Protocol handler</span></span>

<span data-ttu-id="ad9bf-786">Os aplicativos nem sempre são chamados de aplicativos virtualizados usando invocação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="ad9bf-787">Por exemplo, em um aplicativo com suporte para inserir um link mailto: dentro de um documento ou página da Web, o usuário clica em um link mailto: e espera obter seu cliente de email registrado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="ad9bf-788">O App-V dá suporte a manipuladores de protocolo de URL que podem ser registrados em cada pacote com o sistema operacional local.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="ad9bf-789">Durante o sequenciamento, os manipuladores de protocolo de URL são adicionados automaticamente ao pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="ad9bf-790">Para situações em que há mais de um aplicativo que pode registrar o manipulador de protocolo de URL específico, os arquivos de configuração dinâmica podem ser utilizados para modificar o comportamento e suprimir ou desabilitar esse recurso para um aplicativo que não deve ser o aplicativo principal iniciado.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="ad9bf-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="ad9bf-791">AppPath</span></span>

<span data-ttu-id="ad9bf-792">O ponto de extensão AppPath permite chamar aplicativos App-V diretamente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="ad9bf-793">Isso normalmente é realizado na tela de execução ou início, dependendo do sistema operacional, que permite que os administradores forneçam acesso a aplicativos App-V de comandos do sistema operacional ou scripts sem chamar o caminho específico para o executável.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="ad9bf-794">Portanto, evita modificar a variável de ambiente de caminho do sistema em todos os sistemas, conforme é realizado durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="ad9bf-795">O ponto de extensão AppPath é configurado no manifesto ou nos arquivos de configuração dinâmico e é armazenado no registro do computador local durante a publicação para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="ad9bf-796">Para obter informações adicionais sobre a revisão do AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="ad9bf-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="ad9bf-797">Aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="ad9bf-797">Virtual application</span></span>

<span data-ttu-id="ad9bf-798">Esse subsistema fornece uma lista de aplicativos capturados durante o sequenciamento, que normalmente são consumidos por outros componentes do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="ad9bf-799">A integração de pontos de extensão que pertencem a um aplicativo específico pode ser desabilitada usando arquivos de configuração dinâmico.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="ad9bf-800">Por exemplo, se um pacote contém dois aplicativos, é possível desabilitar todos os pontos de extensão pertencentes a um aplicativo, para permitir somente a integração de pontos de extensão de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="ad9bf-801">Regras de ponto de extensão</span><span class="sxs-lookup"><span data-stu-id="ad9bf-801">Extension point rules</span></span>

<span data-ttu-id="ad9bf-802">Os pontos de extensão descritos acima são integrados ao sistema operacional com base na forma como os pacotes foram publicados.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="ad9bf-803">Locais de publicação global pontos de extensão em locais de máquinas públicas, onde a publicação do usuário coloca os pontos de extensão nos locais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="ad9bf-804">Por exemplo, um atalho criado na área de trabalho e publicado globalmente resultará nos dados de arquivo para o atalho (%Public%\\Desktop) e os dados do registro (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="ad9bf-805">O mesmo atalho teria dados de arquivo (%UserProfile%\\Desktop) e dados do registro (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="ad9bf-806">Os pontos de extensão não são todos publicados da mesma maneira, em que alguns pontos de extensão exigirão publicação global e outros exigem sequenciamento no sistema operacional específico e na arquitetura onde são entregues.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="ad9bf-807">Veja a seguir uma tabela que descreve essas duas principais regras.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ad9bf-808">Extensão virtual</span><span class="sxs-lookup"><span data-stu-id="ad9bf-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-809">Requer o sequenciamento de so de destino</span><span class="sxs-lookup"><span data-stu-id="ad9bf-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="ad9bf-810">Requer publicação global</span><span class="sxs-lookup"><span data-stu-id="ad9bf-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-811">Atalho</span><span class="sxs-lookup"><span data-stu-id="ad9bf-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-812">Associação de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-813">Protocolos de URL</span><span class="sxs-lookup"><span data-stu-id="ad9bf-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-814">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="ad9bf-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-816">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-817">Modo COM</span><span class="sxs-lookup"><span data-stu-id="ad9bf-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-818">Cliente de software</span><span class="sxs-lookup"><span data-stu-id="ad9bf-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-819">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-820">Funcionalidades do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ad9bf-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-821">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-822">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-823">Manipulador de menu de contexto</span><span class="sxs-lookup"><span data-stu-id="ad9bf-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-824">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-825">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-826">Manipulador de arrastar e soltar</span><span class="sxs-lookup"><span data-stu-id="ad9bf-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-827">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-828">Manipulador de objeto de dados</span><span class="sxs-lookup"><span data-stu-id="ad9bf-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-829">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-830">Manipulador de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="ad9bf-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-831">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-832">Manipulador InfoTip</span><span class="sxs-lookup"><span data-stu-id="ad9bf-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-833">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-834">Manipulador de colunas</span><span class="sxs-lookup"><span data-stu-id="ad9bf-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-835">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-836">Extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="ad9bf-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-837">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ad9bf-838">Objeto auxiliar do navegador</span><span class="sxs-lookup"><span data-stu-id="ad9bf-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-839">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-840">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ad9bf-841">Objeto ActiveX</span><span class="sxs-lookup"><span data-stu-id="ad9bf-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-842">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="ad9bf-843">X</span><span class="sxs-lookup"><span data-stu-id="ad9bf-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="ad9bf-844">Processamento dinâmico de configuração</span><span class="sxs-lookup"><span data-stu-id="ad9bf-844">Dynamic configuration processing</span></span>


<span data-ttu-id="ad9bf-845">Implantar pacotes do App-V em um computador ou usuário é muito simples.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="ad9bf-846">No entanto, como as organizações implantam aplicativos do AppV em linhas comerciais e limites geográficos e políticos, a capacidade de sequenciar um aplicativo uma vez com um conjunto de configurações se torna impossível.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="ad9bf-847">O App-V foi projetado para esse cenário, pois ele captura configurações e configurações específicas durante o sequenciamento no arquivo de manifesto, mas também dá suporte à modificação com arquivos de configuração dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="ad9bf-848">A configuração dinâmica do App-V permite especificar uma política para um pacote no nível do computador ou no nível do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="ad9bf-849">Os arquivos de configuração dinâmica permitem que os engenheiros de sequenciamento modifiquem a configuração de um pacote, seqüência de postagem, para atender às necessidades de grupos individuais de usuários ou máquinas.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="ad9bf-850">Em alguns casos, pode ser necessário fazer modificações no aplicativo para fornecer a funcionalidade adequada dentro do ambiente do App-V.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="ad9bf-851">Por exemplo, talvez seja necessário fazer modificações nos arquivos \ _ \ \* config.xml para permitir que determinadas ações sejam executadas em um tempo especificado durante a execução do aplicativo, como desabilitar uma extensão mailto para impedir que um aplicativo virtualizado Substitua essa extensão de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="ad9bf-852">Os pacotes do App-V contêm o arquivo de manifesto dentro do arquivo do pacote do AppV, que é o representativo de operações de sequenciamento e é a política escolhida, a menos que arquivos de configuração dinâmicos sejam atribuídos a um pacote específico.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="ad9bf-853">Pós-sequenciamento, os arquivos de configuração dinâmica podem ser modificados para permitir a publicação de um aplicativo para áreas de trabalho ou usuários diferentes com pontos de extensão diferentes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="ad9bf-854">Os dois arquivos de configuração dinâmica são os arquivos DDC (configuração de implantação dinâmica) e DUC (configuração dinâmica do usuário).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="ad9bf-855">Esta seção enfoca a combinação dos arquivos de manifesto e de configuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="ad9bf-856">Exemplo de arquivos de configuração dinâmicos</span><span class="sxs-lookup"><span data-stu-id="ad9bf-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="ad9bf-857">O exemplo a seguir mostra a combinação dos arquivos de manifesto, configuração de implantação e configuração do usuário após a publicação e durante a operação normal.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="ad9bf-858">Estes exemplos são exemplos abreviados de cada um dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="ad9bf-859">O objetivo é mostrar a combinação apenas dos arquivos e não ser uma descrição completa das categorias específicas disponíveis em cada um dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="ad9bf-860">Para obter mais informações, consulte o guia de sequenciamento do App-V 5 em:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="ad9bf-861">Manifesto</span><span class="sxs-lookup"><span data-stu-id="ad9bf-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="ad9bf-862">Configuração de implantação</span><span class="sxs-lookup"><span data-stu-id="ad9bf-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="ad9bf-863">Configuração do usuário</span><span class="sxs-lookup"><span data-stu-id="ad9bf-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="ad9bf-864">Montagens lado a lado</span><span class="sxs-lookup"><span data-stu-id="ad9bf-864">Side-by-side assemblies</span></span>


<span data-ttu-id="ad9bf-865">O App-V dá suporte ao empacotamento automático de assemblies lado a lado (SxS) durante o sequenciamento e a implantação no cliente durante a publicação do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="ad9bf-866">O App-V 5 SP2 dá suporte à captura de assemblies SxS durante o sequenciamento para assemblies que não estão presentes na máquina de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="ad9bf-867">E para assemblies que consistem em Visual C++ (versão 8 e mais recente) e/ou em tempo de execução do MSXML, o sequenciador detectará e capturará essas dependências automaticamente, mesmo que elas não tenham sido instaladas durante o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="ad9bf-868">O recurso de assemblies lado a lado remove as limitações das versões anteriores do App-V, em que o sequenciador do App-V não captura assemblies já presentes na estação de trabalho de sequenciamento e privatizing os assemblies que limitam-se a uma versão de bit por pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="ad9bf-869">Esse comportamento resultou em aplicativos do App-V implantados em clientes que não continham os assemblies SxS necessários, causando falhas de inicialização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="ad9bf-870">Isso forçou o processo de empacotamento para documentar e, em seguida, garantir que todos os assemblies necessários para pacotes foram instalados localmente no sistema operacional cliente do usuário para garantir o suporte para os aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="ad9bf-871">Com base no número de assemblies e na falta de documentação do aplicativo para as dependências necessárias, essa tarefa foi um desafio de gerenciamento e implementação.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="ad9bf-872">O suporte ao assembly lado a lado do App-V tem os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="ad9bf-873">Capturas automáticas do assembly SxS durante o sequenciamento, independentemente de o assembly já ter sido instalado na estação de trabalho de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="ad9bf-874">O cliente App-V instala automaticamente assemblies SxS necessários para o computador cliente no momento da publicação, quando eles não estão presentes.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="ad9bf-875">O sequenciador relata a dependência do tempo de execução do VC no mecanismo de relatório do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="ad9bf-876">O sequenciador permite optar por não empacotar os assemblies que já estão instalados no sequenciador, oferecendo suporte a cenários em que os assemblies foram instalados anteriormente nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="ad9bf-877">Publicação automática de assemblies SxS</span><span class="sxs-lookup"><span data-stu-id="ad9bf-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="ad9bf-878">Durante a publicação de um pacote App-V com assemblies SxS, o cliente App-V Verifica a presença do assembly na máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="ad9bf-879">Se o assembly não existir, o cliente vai implantar o assembly na máquina.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="ad9bf-880">Os pacotes que fazem parte dos grupos de conexão dependerão das instalações de assembly lado a lado que fazem parte dos pacotes base, pois o grupo de conexões não contém informações sobre a instalação do assembly.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="ad9bf-881">**Observação**  Cancelar a publicação ou a remoção de um pacote com um assembly não remove os assemblies desse pacote.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="ad9bf-882">Registro em log do cliente</span><span class="sxs-lookup"><span data-stu-id="ad9bf-882">Client logging</span></span>


<span data-ttu-id="ad9bf-883">O cliente App-V registra informações no log de eventos do Windows no formato ETW padrão.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="ad9bf-884">Os eventos específicos do App-V podem ser encontrados no Visualizador de eventos, em aplicativos e serviços Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="ad9bf-885">**Observação**  No App-V 5,0 SP3, alguns registros foram consolidados e movidos para o seguinte local:</span><span class="sxs-lookup"><span data-stu-id="ad9bf-885">**Note** In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="ad9bf-886">Para obter uma lista dos logs movidos, consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="ad9bf-887">Há três categorias específicas de eventos gravadas descritas abaixo.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="ad9bf-888">**Administrador**: registra eventos para configurações aplicadas ao cliente App-V e contém os principais avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="ad9bf-889">**Operacional**: registra a execução geral do App-v e o uso de componentes individuais criando um log de auditoria das operações do App-v que foram concluídas no cliente App-v.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="ad9bf-890">**Aplicativo virtual**: registra os lançamentos e o uso de subsistemas de virtualização do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





