---
title: Sobre a configuração dinâmica do App-V 5.0
description: Sobre a configuração dinâmica do App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796644"
---
# <span data-ttu-id="44ada-103">Sobre a configuração dinâmica do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="44ada-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="44ada-104">Você pode usar a configuração dinâmica para personalizar um pacote App-V 5,0 para um usuário.</span><span class="sxs-lookup"><span data-stu-id="44ada-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="44ada-105">Use as informações a seguir para criar ou editar um arquivo de configuração dinâmica existente.</span><span class="sxs-lookup"><span data-stu-id="44ada-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="44ada-106">Quando você edita o arquivo de configuração dinâmica, ele personaliza como um pacote do App-V 5,0 será executado para um usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="44ada-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="44ada-107">Isso ajuda a fornecer um método mais conveniente para a personalização do pacote, removendo a necessidade de resequenciar os pacotes usando as configurações desejadas e fornece uma maneira de manter o conteúdo do pacote e as configurações personalizadas de forma independente.</span><span class="sxs-lookup"><span data-stu-id="44ada-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="44ada-108">Avançado: configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="44ada-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="44ada-109">Os pacotes de aplicativos virtuais contêm um manifesto que fornece todas as informações básicas do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="44ada-110">Essas informações incluem os padrões para as configurações do pacote e determina as configurações na forma mais básica (sem personalização adicional).</span><span class="sxs-lookup"><span data-stu-id="44ada-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="44ada-111">Se desejar ajustar esses padrões para um usuário ou grupo específico, você pode criar e editar os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="44ada-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="44ada-112">Arquivo de configuração do usuário</span><span class="sxs-lookup"><span data-stu-id="44ada-112">User Configuration file</span></span>

-   <span data-ttu-id="44ada-113">Arquivo de configuração de implantação</span><span class="sxs-lookup"><span data-stu-id="44ada-113">Deployment configuration file</span></span>

<span data-ttu-id="44ada-114">Os arquivos. XML anteriores especificam as configurações do pacote e permitem que os pacotes sejam personalizados sem afetar diretamente os pacotes.</span><span class="sxs-lookup"><span data-stu-id="44ada-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="44ada-115">Quando um pacote é criado, o sequenciador gera automaticamente a implantação padrão e os arquivos user. xml usando os dados do manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="44ada-116">Portanto, esses arquivos de configuração gerados simplesmente refletem as configurações padrão que o pacote innateu de como as coisas foram configuradas durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="44ada-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="44ada-117">Se você aplicar esses arquivos de configuração a um pacote no formato gerado pelo sequenciador, os pacotes terão as mesmas configurações padrão que vieram do manifesto.</span><span class="sxs-lookup"><span data-stu-id="44ada-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="44ada-118">Isso fornece um modelo específico do pacote para começar se qualquer um dos padrões deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="44ada-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="44ada-119">**Observação**  As informações a seguir só podem ser usadas para modificar arquivos de configuração gerados do sequenciador para personalizar pacotes para atender a requisitos específicos de um usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="44ada-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="44ada-120">Conteúdo do arquivo de configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="44ada-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="44ada-121">Todas as adições, exclusões e atualizações nos arquivos de configuração precisam ser feitas em relação aos valores padrão especificados pelas informações de manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="44ada-122">Revise a seguinte tabela:</span><span class="sxs-lookup"><span data-stu-id="44ada-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-123">Arquivo de configuração do usuário. xml</span><span class="sxs-lookup"><span data-stu-id="44ada-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44ada-124">Arquivo de implantação de configuração. xml</span><span class="sxs-lookup"><span data-stu-id="44ada-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-125">Manifesto do pacote</span><span class="sxs-lookup"><span data-stu-id="44ada-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="44ada-126">A tabela anterior representa como os arquivos serão lidos.</span><span class="sxs-lookup"><span data-stu-id="44ada-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="44ada-127">A primeira entrada representa o que será lido por último, portanto, o conteúdo terá precedência.</span><span class="sxs-lookup"><span data-stu-id="44ada-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="44ada-128">Portanto, todos os pacotes contêm inerentemente e fornecem configurações padrão do manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="44ada-129">Se um arquivo Configuration. XML de implantação com configurações personalizadas for aplicado, ele substituirá os padrões de manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="44ada-130">Se um arquivo de configuração de usuário. XML com configurações personalizadas for aplicado antes disso, ele substituirá a configuração de implantação e os padrões de manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="44ada-131">A lista a seguir exibe mais informações sobre os dois tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="44ada-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="44ada-132">**Arquivo de configuração do usuário (userconfig)** – permite que você especifique ou modifique configurações personalizadas para um pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="44ada-133">Essas configurações serão aplicadas para um usuário específico quando o pacote for implantado em um computador que esteja executando o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="44ada-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="44ada-134">**Arquivo de configuração de implantação (deploymentconfig)** – permite que você especifique ou modifique as configurações padrão para um pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="44ada-135">Essas configurações serão aplicadas a todos os usuários quando um pacote for implantado em um computador que esteja executando o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="44ada-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="44ada-136">Para personalizar as configurações de um pacote para um conjunto específico de usuários em um computador ou para fazer alterações que serão aplicadas a locais de usuários locais, como o HKCU, o arquivo userconfig deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="44ada-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="44ada-137">Para modificar as configurações padrão de um pacote para todos os usuários em um computador ou para fazer alterações que serão aplicadas a locais globais, como HKEY \ _LOCAL \ _MACHINE e a pasta All Users, o arquivo DeploymentConfig deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="44ada-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="44ada-138">O arquivo userconfig fornece configurações que podem ser aplicadas a um único usuário sem afetar outros usuários em um cliente:</span><span class="sxs-lookup"><span data-stu-id="44ada-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="44ada-139">Extensões que serão integradas ao sistema nativo por usuário:-atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM</span><span class="sxs-lookup"><span data-stu-id="44ada-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="44ada-140">Subsistemas virtuais:-objetos do aplicativo, variáveis de ambiente, modificações do registro, serviços e fontes</span><span class="sxs-lookup"><span data-stu-id="44ada-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="44ada-141">Scripts (somente contexto do usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="44ada-142">Gerenciando autoridade (para controlar a coexistência do pacote com o App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="44ada-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="44ada-143">O arquivo DeploymentConfig fornece configurações em duas seções, uma em relação ao contexto da máquina e uma em relação ao contexto do usuário fornecendo as mesmas funcionalidades listadas na lista userconfig acima:</span><span class="sxs-lookup"><span data-stu-id="44ada-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="44ada-144">Todas as configurações de userconfig acima</span><span class="sxs-lookup"><span data-stu-id="44ada-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="44ada-145">Extensões que só podem ser aplicadas globalmente para todos os usuários</span><span class="sxs-lookup"><span data-stu-id="44ada-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="44ada-146">Subsistemas virtuais que podem ser configurados para locais de máquinas globais, por exemplo, registro</span><span class="sxs-lookup"><span data-stu-id="44ada-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="44ada-147">URL da fonte do produto</span><span class="sxs-lookup"><span data-stu-id="44ada-147">Product Source URL</span></span>

-   <span data-ttu-id="44ada-148">Scripts (somente contexto da máquina)</span><span class="sxs-lookup"><span data-stu-id="44ada-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="44ada-149">Controles para encerrar processos filho</span><span class="sxs-lookup"><span data-stu-id="44ada-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="44ada-150">Estrutura de arquivos</span><span class="sxs-lookup"><span data-stu-id="44ada-150">File structure</span></span>

<span data-ttu-id="44ada-151">A estrutura do arquivo de configuração dinâmica do App-V 5,0 é explicada na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="44ada-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="44ada-152">Arquivo de configuração de usuário dinâmico</span><span class="sxs-lookup"><span data-stu-id="44ada-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="44ada-153">**Header** -o cabeçalho de um arquivo de configuração de usuário dinâmico é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44ada-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="44ada-154">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="44ada-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="44ada-155">O **PackageID** é o mesmo valor que existe no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="44ada-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="44ada-156">**Corpo** -o corpo do arquivo de configuração de usuário dinâmico pode incluir todos os pontos de extensão do aplicativo definidos no arquivo de manifesto, bem como informações para configurar aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="44ada-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="44ada-157">Há quatro subseções permitidas no corpo:</span><span class="sxs-lookup"><span data-stu-id="44ada-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="44ada-158">**Aplicativos** – todas as extensões de aplicativo que estão contidas no arquivo de manifesto dentro de um pacote são atribuídas com uma ID de aplicativo, que também é definida no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="44ada-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="44ada-159">Isso permite que você habilite ou desabilite todas as extensões para um determinado aplicativo em um pacote.</span><span class="sxs-lookup"><span data-stu-id="44ada-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="44ada-160">A **ID do aplicativo** deve existir no arquivo de manifesto ou será ignorada.</span><span class="sxs-lookup"><span data-stu-id="44ada-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="44ada-161">&lt;Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="44ada-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="44ada-162">&lt;Aplicativos&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="44ada-163">&lt;!--Nenhum novo aplicativo pode ser definido na política.</span><span class="sxs-lookup"><span data-stu-id="44ada-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="44ada-164">O cliente AppV ignorará qualquer ID de aplicativo que não esteja também no arquivo de manifesto--&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="44ada-165">&lt;ID do aplicativo = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="44ada-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="44ada-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="44ada-168">…</span><span class="sxs-lookup"><span data-stu-id="44ada-168">…</span></span>

   <span data-ttu-id="44ada-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="44ada-170">**Subsistemas** -AppExtensions e outros subsistemas são organizados como subnós nos &lt; subsistemas &gt; :</span><span class="sxs-lookup"><span data-stu-id="44ada-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="44ada-171">&lt;Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="44ada-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="44ada-172">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="44ada-173">..</span><span class="sxs-lookup"><span data-stu-id="44ada-173">..</span></span>

   <span data-ttu-id="44ada-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="44ada-175">..</span><span class="sxs-lookup"><span data-stu-id="44ada-175">..</span></span>

   <span data-ttu-id="44ada-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="44ada-177">Cada subsistema pode ser habilitado/desabilitado usando o atributo "**Enabled**".</span><span class="sxs-lookup"><span data-stu-id="44ada-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="44ada-178">Veja a seguir vários subsistemas e exemplos de uso.</span><span class="sxs-lookup"><span data-stu-id="44ada-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="44ada-179">Extensions</span><span class="sxs-lookup"><span data-stu-id="44ada-179">Extensions:</span></span>**

   <span data-ttu-id="44ada-180">Alguns subsistemas (subsistemas de extensão) extensões de controle.</span><span class="sxs-lookup"><span data-stu-id="44ada-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="44ada-181">Esses subsistemas são:-atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM</span><span class="sxs-lookup"><span data-stu-id="44ada-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="44ada-182">Subsistemas de extensão podem ser habilitados e desabilitados independentemente do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="44ada-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="44ada-183">Portanto, se os atalhos estiverem habilitados, o cliente usará os atalhos contidos no manifesto por padrão.</span><span class="sxs-lookup"><span data-stu-id="44ada-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="44ada-184">Cada subsistema de extensão pode conter &lt; um &gt; nó de extensões.</span><span class="sxs-lookup"><span data-stu-id="44ada-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="44ada-185">Se esse elemento filho estiver presente, o cliente ignorará o conteúdo do arquivo de manifesto desse subsistema e somente usará o conteúdo do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="44ada-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="44ada-186">Exemplo usando o subsistema de atalhos:</span><span class="sxs-lookup"><span data-stu-id="44ada-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="44ada-187">Se o usuário definiu isso no arquivo de configuração dinâmica ou de implantação:</span><span class="sxs-lookup"><span data-stu-id="44ada-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="44ada-188">Se o usuário tiver definido somente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44ada-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="44ada-189">Se o usuário definir o seguinte</span><span class="sxs-lookup"><span data-stu-id="44ada-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="44ada-190">Então, todos os atalhos dentro do manifesto ainda serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="44ada-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="44ada-191">Não haverá nenhum atalho integrado.</span><span class="sxs-lookup"><span data-stu-id="44ada-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="44ada-192">Os subsistemas de extensão suportados são:</span><span class="sxs-lookup"><span data-stu-id="44ada-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="44ada-193">**Atalhos:** Isso controla atalhos que serão integrados ao sistema local.</span><span class="sxs-lookup"><span data-stu-id="44ada-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="44ada-194">Veja a seguir um exemplo com 2 atalhos:</span><span class="sxs-lookup"><span data-stu-id="44ada-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="44ada-195">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="44ada-196">&lt;Atalhos habilitados = "verdadeiro"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="44ada-197">&lt;Extensões&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="44ada-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="44ada-199">&lt;Categoria de extensão = "AppV. Shortcut"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="44ada-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="44ada-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="44ada-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="44ada-203">**Associações de tipo de arquivo:** Associa tipos de arquivos aos programas para abrir por padrão, bem como configurar o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="44ada-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="44ada-204">(Os tipos MIME também podem ser configurados usando essa susbsystem).</span><span class="sxs-lookup"><span data-stu-id="44ada-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="44ada-205">Exemplo de associação de tipo de arquivo está abaixo:</span><span class="sxs-lookup"><span data-stu-id="44ada-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="44ada-206">&lt;FileTypeAssociations Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="44ada-207">&lt;Extensões&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="44ada-208">&lt;Extension category = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="44ada-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="44ada-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="44ada-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="44ada-212">**Protocolos de URL**: controla os protocolos de URL que são integrados ao registro local da máquina do cliente, por exemplo, "mailto:".</span><span class="sxs-lookup"><span data-stu-id="44ada-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="44ada-213">&lt;URLProtocols Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="44ada-214">&lt;Extensões&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="44ada-215">&lt;Extension category = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="44ada-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="44ada-217">&lt;Nome &gt; mailto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="44ada-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="44ada-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="44ada-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="44ada-221">&lt;Descritivo&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="44ada-222">&lt;AppUserModelId&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="44ada-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="44ada-224">&lt;InfoTip&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="44ada-225">&lt;SourceFilter /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="44ada-226">&lt;ShellFolder /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="44ada-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="44ada-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="44ada-229">&lt;CLSID&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="44ada-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="44ada-231">&lt;Netcommand &gt; Open &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="44ada-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="44ada-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="44ada-234">&lt;Nome &gt; aberto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="44ada-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Observação/m "%1" &lt; /CommandLine&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="44ada-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="44ada-237">&lt;FriendlyName&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="44ada-238">&lt;/Extended estendido &gt; 0 &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="44ada-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="44ada-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="44ada-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="44ada-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="44ada-243">&lt;Aplicativos &gt; ContosoMail &lt; /Application&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="44ada-244">&lt;Tópico &gt; ShellSystem &lt; /topic&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="44ada-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="44ada-246">&lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="44ada-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="44ada-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="44ada-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="44ada-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="44ada-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="44ada-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="44ada-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="44ada-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="44ada-255">**Clientes de software**: permite que o aplicativo se registre como um cliente de email, leitor de notícias, Media Player e torna o aplicativo visível na interface do usuário definir acesso do programa e padrões do computador.</span><span class="sxs-lookup"><span data-stu-id="44ada-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="44ada-256">Na maioria dos casos, você só precisa habilitá-lo e desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="44ada-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="44ada-257">Também há um controle para habilitar e desabilitar o cliente de email especificamente se você quiser que os outros clientes ainda estejam habilitados, exceto para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="44ada-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="44ada-258">&lt;SoftwareClients Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="44ada-259">&lt;ClientConfiguration EmailEnabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="44ada-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="44ada-261">AppPaths:-se um aplicativo por exemplo contoso.exe for registrado com um nome AppPath de "MyApp", ele permitirá que você digite "MyApp" no menu executar e ele será aberto contoso.exe.</span><span class="sxs-lookup"><span data-stu-id="44ada-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="44ada-262">&lt;AppPaths Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="44ada-263">&lt;Extensões&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="44ada-264">&lt;Extension category = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="44ada-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="44ada-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="44ada-267">&lt;Nome &gt;contosomail.exe&lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="44ada-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="44ada-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="44ada-270">&lt;CanAcceptUrl &gt; falsa &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="44ada-271">&lt;SaveUrl /&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="44ada-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="44ada-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="44ada-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="44ada-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="44ada-276">**Com**: permite que um aplicativo registre servidores com locais.</span><span class="sxs-lookup"><span data-stu-id="44ada-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="44ada-277">O Mode pode ser integração, isolado ou desligado.</span><span class="sxs-lookup"><span data-stu-id="44ada-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="44ada-278">Quando ISOL.</span><span class="sxs-lookup"><span data-stu-id="44ada-278">When Isol.</span></span>

   <span data-ttu-id="44ada-279">&lt;Modo COM = "isolado"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="44ada-280">**Outras configurações**:</span><span class="sxs-lookup"><span data-stu-id="44ada-280">**Other Settings**:</span></span>

   <span data-ttu-id="44ada-281">Além das extensões, outros subsistemas podem ser habilitados/desabilitados e editados:</span><span class="sxs-lookup"><span data-stu-id="44ada-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="44ada-282">**Objetos de núcleo virtual**:</span><span class="sxs-lookup"><span data-stu-id="44ada-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="44ada-283">&lt;Objetos habilitados = "falso"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="44ada-284">**Registro virtual**: usado se você deseja definir um registro no registro virtual dentro de HKCU</span><span class="sxs-lookup"><span data-stu-id="44ada-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="44ada-285">&lt;Registro Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="44ada-286">&lt;Conter&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="44ada-287">&lt;Caminho da chave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="44ada-288">&lt;Tipo de valor = "REG \ _SZ" Name = "bar" data = "NewValue"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="44ada-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="44ada-290">&lt;Caminho da chave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="44ada-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="44ada-292">&lt;Remover&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="44ada-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="44ada-294">Sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="44ada-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="44ada-295">Fontes virtuais</span><span class="sxs-lookup"><span data-stu-id="44ada-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="44ada-296">Variáveis de ambiente virtual</span><span class="sxs-lookup"><span data-stu-id="44ada-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="44ada-297">&lt;EnvironmentVariables Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="44ada-298">&lt;Conter&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="44ada-299">Serviços virtuais</span><span class="sxs-lookup"><span data-stu-id="44ada-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="44ada-300">**Userscript** – os scripts podem ser usados para configurar ou alterar o ambiente virtual, bem como executar scripts no momento da implantação ou remoção, antes do aplicativo ser executado ou podem ser usados para "limpar" o ambiente após o encerramento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44ada-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="44ada-301">Faça referência a um arquivo de configuração de usuário de exemplo que é exibido pelo sequenciador para ver um exemplo de script.</span><span class="sxs-lookup"><span data-stu-id="44ada-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="44ada-302">A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="44ada-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="44ada-303">**ManagingAuthority** – pode ser usado quando duas versões do pacote são coexistentes na mesma máquina, uma implantada no app-v 4,6 e outras implantadas no app-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="44ada-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="44ada-304">Para permitir que o App-V vNext assuma os pontos de extensão do App-V 4,6 para o pacote nomeado, digite o seguinte no arquivo userconfig (em que PackageName é o GUID do pacote no App-V 4,6:</span><span class="sxs-lookup"><span data-stu-id="44ada-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="44ada-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="44ada-306">Arquivo de configuração de implantação dinâmica</span><span class="sxs-lookup"><span data-stu-id="44ada-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="44ada-307">**Header** -o cabeçalho de um arquivo de configuração de implantação é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="44ada-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="44ada-308">&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="44ada-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="44ada-309">O **PackageID** é o mesmo valor que existe no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="44ada-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="44ada-310">**Corpo** -o corpo do arquivo de configuração de implantação inclui duas seções:</span><span class="sxs-lookup"><span data-stu-id="44ada-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="44ada-311">Seção de configuração do usuário – permite o mesmo conteúdo que o arquivo de configuração do usuário descrito na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="44ada-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="44ada-312">Quando o pacote for publicado para um usuário, as configurações de configuração do appextensions nesta seção substituirão as configurações correspondentes no manifesto dentro do pacote, a menos que um arquivo de configuração do usuário também seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="44ada-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="44ada-313">Se um arquivo userconfig também for fornecido, ele será usado em vez das configurações de usuário no arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="44ada-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="44ada-314">Se o pacote for publicado globalmente, somente o conteúdo do arquivo de configuração de implantação será usado em combinação com o manifesto.</span><span class="sxs-lookup"><span data-stu-id="44ada-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="44ada-315">Seção de configuração da máquina – contém informações que podem ser configuradas somente para uma máquina inteira, não para um usuário específico na máquina.</span><span class="sxs-lookup"><span data-stu-id="44ada-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="44ada-316">Por exemplo, HKEY \ _LOCAL \ _MACHINE chaves do registro no VFS.</span><span class="sxs-lookup"><span data-stu-id="44ada-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="44ada-317">&lt;DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="44ada-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="44ada-318">&lt;Userconfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="44ada-319">..</span><span class="sxs-lookup"><span data-stu-id="44ada-319">..</span></span>

<span data-ttu-id="44ada-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="44ada-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="44ada-322">..</span><span class="sxs-lookup"><span data-stu-id="44ada-322">..</span></span>

<span data-ttu-id="44ada-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="44ada-324">..</span><span class="sxs-lookup"><span data-stu-id="44ada-324">..</span></span>

<span data-ttu-id="44ada-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="44ada-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="44ada-327">**Configuração do usuário** – use a seção **arquivo de configuração do usuário dinâmico** anterior para obter informações sobre as configurações fornecidas na seção configuração do usuário do arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="44ada-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="44ada-328">Configuração da máquina – a seção configuração da máquina do arquivo de configuração de implantação é usada para configurar informações que podem ser definidas somente para uma máquina inteira, não para um usuário específico no computador.</span><span class="sxs-lookup"><span data-stu-id="44ada-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="44ada-329">Por exemplo, HKEY \ _LOCAL \ _MACHINE chaves do registro no registro virtual.</span><span class="sxs-lookup"><span data-stu-id="44ada-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="44ada-330">Há quatro subseções permitidas nesse elemento</span><span class="sxs-lookup"><span data-stu-id="44ada-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="44ada-331">**Subsistemas** -AppExtensions e outros subsistemas são organizados como subnós em &lt; subsistemas &gt; :</span><span class="sxs-lookup"><span data-stu-id="44ada-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="44ada-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="44ada-333">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="44ada-334">..</span><span class="sxs-lookup"><span data-stu-id="44ada-334">..</span></span>

      <span data-ttu-id="44ada-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="44ada-336">..</span><span class="sxs-lookup"><span data-stu-id="44ada-336">..</span></span>

    <span data-ttu-id="44ada-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="44ada-338">A seção a seguir exibe os vários subsistemas e exemplos de uso.</span><span class="sxs-lookup"><span data-stu-id="44ada-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="44ada-339">**Extensões**:</span><span class="sxs-lookup"><span data-stu-id="44ada-339">**Extensions**:</span></span>

    <span data-ttu-id="44ada-340">Alguns subsistemas (subsistemas de extensão) extensões de controle que só podem se aplicar a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="44ada-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="44ada-341">O subsistema é recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44ada-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="44ada-342">Como isso só pode se aplicar a todos os usuários, o pacote deve ser publicado globalmente para que esse tipo de extensão seja integrado ao sistema local.</span><span class="sxs-lookup"><span data-stu-id="44ada-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="44ada-343">As mesmas regras para controles e configurações que se aplicam às extensões na configuração do usuário também se aplicam aos usuários na seção MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="44ada-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="44ada-344">**Recursos do aplicativo**: usado por programas padrão na interface do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="44ada-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="44ada-345">Permite que um aplicativo se registre como capaz de abrir determinadas extensões de arquivo, como um Contender para o menu iniciar slot do navegador da Internet, como capaz de abrir certos tipos MIME do Windows.</span><span class="sxs-lookup"><span data-stu-id="44ada-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="44ada-346">Essa extensão também torna o aplicativo virtual visível na interface do usuário definir programas padrão.:</span><span class="sxs-lookup"><span data-stu-id="44ada-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="44ada-347">&lt;ApplicationCapabilities Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="44ada-348">&lt;Extensões&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="44ada-349">&lt;Extension category = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="44ada-350">&lt;Recurso&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="44ada-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="44ada-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="44ada-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="44ada-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="44ada-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="44ada-356">**Outras configurações**:</span><span class="sxs-lookup"><span data-stu-id="44ada-356">**Other Settings**:</span></span>

    <span data-ttu-id="44ada-357">Além das extensões, outros subsistemas podem ser editados:</span><span class="sxs-lookup"><span data-stu-id="44ada-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="44ada-358">**Registro virtual em toda a máquina**: usado quando você deseja definir uma chave do registro no registro virtual em HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="44ada-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="44ada-359">&lt;Registro&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="44ada-360">&lt;Conter&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="44ada-361">&lt;Caminho da chave = "\\REGISTRY\\Machine\\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="44ada-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="44ada-363">&lt;Caminho da chave = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="44ada-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="44ada-365">&lt;Remover&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="44ada-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="44ada-367">Objetos de núcleo virtual em toda a máquina</span><span class="sxs-lookup"><span data-stu-id="44ada-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="44ada-368">&lt;Eles&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="44ada-369">&lt;Não isolar&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="44ada-370">&lt;Nome do objeto = "TestObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="44ada-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="44ada-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="44ada-373">**ProductSourceURLOptOut**: indica se a URL do pacote pode ser modificada globalmente por meio do PackageSourceRoot (para dar suporte a cenários de filial do escritório).</span><span class="sxs-lookup"><span data-stu-id="44ada-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="44ada-374">O padrão é falso e a alteração da configuração entra em vigor na próxima inicialização.</span><span class="sxs-lookup"><span data-stu-id="44ada-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="44ada-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="44ada-376">..</span><span class="sxs-lookup"><span data-stu-id="44ada-376">..</span></span> 

      <span data-ttu-id="44ada-377">&lt;ProductSourceURLOptOut Enabled = "true"/&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="44ada-378">..</span><span class="sxs-lookup"><span data-stu-id="44ada-378">..</span></span>

    <span data-ttu-id="44ada-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="44ada-380">**MachineScripts** – o pacote pode ser configurado para executar scripts no momento da implantação, publicação ou remoção.</span><span class="sxs-lookup"><span data-stu-id="44ada-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="44ada-381">Faça referência a um arquivo de configuração de implantação de exemplo gerado pelo sequenciador para ver um exemplo de script.</span><span class="sxs-lookup"><span data-stu-id="44ada-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="44ada-382">A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados</span><span class="sxs-lookup"><span data-stu-id="44ada-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="44ada-383">**TerminateChildProcess**:-um executável do aplicativo pode ser especificado, cujos processos filho serão encerrados quando o processo exe do aplicativo for finalizado.</span><span class="sxs-lookup"><span data-stu-id="44ada-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="44ada-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="44ada-385">..</span><span class="sxs-lookup"><span data-stu-id="44ada-385">..</span></span>   

      <span data-ttu-id="44ada-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="44ada-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="44ada-388">..</span><span class="sxs-lookup"><span data-stu-id="44ada-388">..</span></span>

    <span data-ttu-id="44ada-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="44ada-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="44ada-390">Scripts</span><span class="sxs-lookup"><span data-stu-id="44ada-390">Scripts</span></span>

<span data-ttu-id="44ada-391">A tabela a seguir descreve os vários eventos de script e o contexto em que eles podem ser executados.</span><span class="sxs-lookup"><span data-stu-id="44ada-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44ada-392">Tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="44ada-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="44ada-393">Pode ser especificado na configuração de implantação</span><span class="sxs-lookup"><span data-stu-id="44ada-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="44ada-394">Pode ser especificado na configuração do usuário</span><span class="sxs-lookup"><span data-stu-id="44ada-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="44ada-395">Pode ser executado no ambiente virtual do pacote</span><span class="sxs-lookup"><span data-stu-id="44ada-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="44ada-396">Pode ser executado no contexto de um aplicativo específico</span><span class="sxs-lookup"><span data-stu-id="44ada-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="44ada-397">Executado no contexto do sistema/usuário: (configuração da implantação, configuração do usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="44ada-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-399">X</span><span class="sxs-lookup"><span data-stu-id="44ada-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-400">(SISTEMA, N/D)</span><span class="sxs-lookup"><span data-stu-id="44ada-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44ada-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="44ada-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-402">X</span><span class="sxs-lookup"><span data-stu-id="44ada-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-403">X</span><span class="sxs-lookup"><span data-stu-id="44ada-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-404">(Sistema, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="44ada-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-406">X</span><span class="sxs-lookup"><span data-stu-id="44ada-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-407">X</span><span class="sxs-lookup"><span data-stu-id="44ada-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-408">(Sistema, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44ada-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="44ada-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-410">X</span><span class="sxs-lookup"><span data-stu-id="44ada-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-411">(SISTEMA, N/D)</span><span class="sxs-lookup"><span data-stu-id="44ada-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-412">StartProcess</span><span class="sxs-lookup"><span data-stu-id="44ada-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-413">X</span><span class="sxs-lookup"><span data-stu-id="44ada-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-414">X</span><span class="sxs-lookup"><span data-stu-id="44ada-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-415">X</span><span class="sxs-lookup"><span data-stu-id="44ada-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-416">X</span><span class="sxs-lookup"><span data-stu-id="44ada-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-417">(Usuário, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44ada-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="44ada-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-419">X</span><span class="sxs-lookup"><span data-stu-id="44ada-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-420">X</span><span class="sxs-lookup"><span data-stu-id="44ada-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-421">X</span><span class="sxs-lookup"><span data-stu-id="44ada-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-422">(Usuário, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44ada-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="44ada-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-424">X</span><span class="sxs-lookup"><span data-stu-id="44ada-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-425">X</span><span class="sxs-lookup"><span data-stu-id="44ada-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-426">X</span><span class="sxs-lookup"><span data-stu-id="44ada-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-427">(Usuário, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44ada-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="44ada-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-429">X</span><span class="sxs-lookup"><span data-stu-id="44ada-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="44ada-430">X</span><span class="sxs-lookup"><span data-stu-id="44ada-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="44ada-431">(Usuário, usuário)</span><span class="sxs-lookup"><span data-stu-id="44ada-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="44ada-432">Criar um arquivo de configuração dinâmico usando um arquivo de manifesto do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="44ada-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="44ada-433">Você pode criar o arquivo de configuração dinâmica usando um dos três métodos: manualmente, usando o console de gerenciamento do App-V 5,0 ou sequenciando um pacote, que será gerado com dois arquivos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="44ada-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="44ada-434">Para obter mais informações sobre como criar o arquivo usando o console de gerenciamento do App-V 5,0, consulte [como criar um arquivo de configuração personalizado usando o console de gerenciamento do App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="44ada-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="44ada-435">Para criar o arquivo manualmente, as informações acima nas seções anteriores podem ser combinadas em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="44ada-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="44ada-436">Recomendamos que você use arquivos gerados pelo sequenciador.</span><span class="sxs-lookup"><span data-stu-id="44ada-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="44ada-437">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44ada-437">Related topics</span></span>


[<span data-ttu-id="44ada-438">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="44ada-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="44ada-439">Como aplicar o arquivo de configuração do usuário usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="44ada-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="44ada-440">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="44ada-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





