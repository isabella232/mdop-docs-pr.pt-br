---
title: Sobre as configurações do cliente
description: Sobre as configurações do cliente
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796625"
---
# <span data-ttu-id="b843b-103">Sobre as configurações do cliente</span><span class="sxs-lookup"><span data-stu-id="b843b-103">About Client Configuration Settings</span></span>


<span data-ttu-id="b843b-104">O cliente Microsoft Application Virtualization (App-V) 5,0 armazena sua configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="b843b-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="b843b-105">Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro.</span><span class="sxs-lookup"><span data-stu-id="b843b-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="b843b-106">Você também pode configurar várias ações do cliente alterando as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="b843b-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="b843b-107">Este tópico lista as configurações de cliente do App-V 5,0 e explica seus usos.</span><span class="sxs-lookup"><span data-stu-id="b843b-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="b843b-108">Você pode usar o PowerShell para modificar as configurações de configuração do cliente.</span><span class="sxs-lookup"><span data-stu-id="b843b-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="b843b-109">Para obter mais informações sobre como usar o PowerShell e o App-V 5,0 [, consulte Administrando o app-v usando o PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="b843b-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="b843b-110">Configurações de cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b843b-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="b843b-111">A tabela a seguir exibe informações sobre as definições de configuração do cliente do App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="b843b-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

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
<th align="left"><span data-ttu-id="b843b-112">Nome da configuração</span><span class="sxs-lookup"><span data-stu-id="b843b-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="b843b-113">Sinalizador de configuração</span><span class="sxs-lookup"><span data-stu-id="b843b-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="b843b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b843b-114">Description</span></span></th>
<th align="left"><span data-ttu-id="b843b-115">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="b843b-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="b843b-116">Valor da chave do registro</span><span class="sxs-lookup"><span data-stu-id="b843b-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="b843b-117">Chaves e valores de estado de política desabilitados</span><span class="sxs-lookup"><span data-stu-id="b843b-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b843b-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="b843b-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-120">Especifica o diretório onde todos os novos aplicativos e atualizações serão instalados.</span><span class="sxs-lookup"><span data-stu-id="b843b-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-121">String</span><span class="sxs-lookup"><span data-stu-id="b843b-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b843b-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-123">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b843b-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="b843b-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-126">Substitui o local de origem para baixar o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="b843b-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-127">String</span><span class="sxs-lookup"><span data-stu-id="b843b-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b843b-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-129">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b843b-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-131">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-132">Esta configuração controla se os aplicativos virtualizados são iniciados em máquinas Windows 8 conectadas por meio de uma conexão de rede limitada (por exemplo, 4G).</span><span class="sxs-lookup"><span data-stu-id="b843b-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-133">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b843b-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-135">0</span><span class="sxs-lookup"><span data-stu-id="b843b-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b843b-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-137">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-138">Especifica o número de vezes para tentar uma sessão descartada novamente.</span><span class="sxs-lookup"><span data-stu-id="b843b-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-139">Inteiro (0-99)</span><span class="sxs-lookup"><span data-stu-id="b843b-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b843b-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-141">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-143">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-144">Especifica o número de segundos entre tentativas para restabelecer uma sessão interrompida.</span><span class="sxs-lookup"><span data-stu-id="b843b-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-145">Inteiro (0-3600)</span><span class="sxs-lookup"><span data-stu-id="b843b-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-147">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-148">Carregar</span><span class="sxs-lookup"><span data-stu-id="b843b-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-149">CARREGAR</span><span class="sxs-lookup"><span data-stu-id="b843b-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-150">Especifica como novos pacotes devem ser carregados automaticamente pelo App-V em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="b843b-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-151">(0x0) nenhum; (0x1) usado anteriormente; (0x2) todos</span><span class="sxs-lookup"><span data-stu-id="b843b-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="b843b-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-153">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-154">LocalProvider</span><span class="sxs-lookup"><span data-stu-id="b843b-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-155">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-156">Especifica o CLSID para uma implementação compatível da interface IAppvPackageLocationProvider.</span><span class="sxs-lookup"><span data-stu-id="b843b-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-157">String</span><span class="sxs-lookup"><span data-stu-id="b843b-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="b843b-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-159">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b843b-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-161">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-162">Especifica o caminho para um certificado válido no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="b843b-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-163">String</span><span class="sxs-lookup"><span data-stu-id="b843b-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b843b-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-165">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b843b-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-167">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-168">Verifica o status da revogação do certificado do servidor antes do fluxo usando HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b843b-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-169">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b843b-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-171">0</span><span class="sxs-lookup"><span data-stu-id="b843b-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b843b-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="b843b-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-174">Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="b843b-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-175">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b843b-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-177">0</span><span class="sxs-lookup"><span data-stu-id="b843b-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-178">Nome</span><span class="sxs-lookup"><span data-stu-id="b843b-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-179">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-179">Note</span></span></strong><br/><p><span data-ttu-id="b843b-180">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-181">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="b843b-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-183">Exibe o nome do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="b843b-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-184">String</span><span class="sxs-lookup"><span data-stu-id="b843b-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-185">Publishing\Servers {serverID} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b843b-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-186">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-187">URL</span><span class="sxs-lookup"><span data-stu-id="b843b-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-188">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-188">Note</span></span></strong><br/><p><span data-ttu-id="b843b-189">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-190">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="b843b-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-192">Exibe a URL do Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="b843b-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-193">String</span><span class="sxs-lookup"><span data-stu-id="b843b-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-194">Publishing\Servers {serverID} \ URL</span><span class="sxs-lookup"><span data-stu-id="b843b-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-195">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b843b-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-197">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-197">Note</span></span></strong><br/><p><span data-ttu-id="b843b-198">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-199">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b843b-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-201">Habilita a atualização de publicação global (booliano)</span><span class="sxs-lookup"><span data-stu-id="b843b-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-202">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-203">Publishing\Servers {serverID} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="b843b-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-204">False</span><span class="sxs-lookup"><span data-stu-id="b843b-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b843b-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-206">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-206">Note</span></span></strong><br/><p><span data-ttu-id="b843b-207">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-208">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b843b-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-210">Dispara uma atualização de publicação global ao fazer logon.</span><span class="sxs-lookup"><span data-stu-id="b843b-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="b843b-211">Booliana</span><span class="sxs-lookup"><span data-stu-id="b843b-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-212">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-213">Publishing\Servers {serverID} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b843b-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-214">False</span><span class="sxs-lookup"><span data-stu-id="b843b-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-216">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-216">Note</span></span></strong><br/><p><span data-ttu-id="b843b-217">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-218">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b843b-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b843b-220">Especifica o intervalo de atualização de publicação usando GlobalRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="b843b-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="b843b-221">Para desabilitar a atualização do pacote, selecione 0.</span><span class="sxs-lookup"><span data-stu-id="b843b-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-222">Inteiro (0-744</span><span class="sxs-lookup"><span data-stu-id="b843b-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-223">Publishing\Servers {serverID} \ GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-224">0</span><span class="sxs-lookup"><span data-stu-id="b843b-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b843b-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-226">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-226">Note</span></span></strong><br/><p><span data-ttu-id="b843b-227">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-228">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="b843b-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-230">Especifica a unidade de intervalo (hora 0-23, dia 0-31).</span><span class="sxs-lookup"><span data-stu-id="b843b-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b843b-231">0 para hora, 1 para dia</span><span class="sxs-lookup"><span data-stu-id="b843b-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-232">Publishing\Servers {serverID} \ GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b843b-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-233">um</span><span class="sxs-lookup"><span data-stu-id="b843b-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b843b-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-235">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-235">Note</span></span></strong><br/><p><span data-ttu-id="b843b-236">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-237">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b843b-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b843b-239">Habilita a atualização da publicação do usuário (booliano)</span><span class="sxs-lookup"><span data-stu-id="b843b-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-240">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-241">Publishing\Servers {serverID} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b843b-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-242">False</span><span class="sxs-lookup"><span data-stu-id="b843b-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b843b-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-244">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-244">Note</span></span></strong><br/><p><span data-ttu-id="b843b-245">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-246">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b843b-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-248">Dispara uma atualização de publicação do usuário ONLOGON.</span><span class="sxs-lookup"><span data-stu-id="b843b-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="b843b-249">Booliana</span><span class="sxs-lookup"><span data-stu-id="b843b-249">( Boolean)</span></span></p>
<p><span data-ttu-id="b843b-250">Contagem de palavras (com espaços): 60</span><span class="sxs-lookup"><span data-stu-id="b843b-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-251">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-252">Publishing\Servers {serverID} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b843b-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-253">False</span><span class="sxs-lookup"><span data-stu-id="b843b-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-255">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-255">Note</span></span></strong><br/><p><span data-ttu-id="b843b-256">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-257">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b843b-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="b843b-259">Especifica o intervalo de atualização de publicação usando UserRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="b843b-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="b843b-260">Para desabilitar a atualização do pacote, selecione 0.</span><span class="sxs-lookup"><span data-stu-id="b843b-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="b843b-261">Contagem de palavras (com espaços): 85</span><span class="sxs-lookup"><span data-stu-id="b843b-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-262">Integer (0-744 horas)</span><span class="sxs-lookup"><span data-stu-id="b843b-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-263">Publishing\Servers {serverID} \ UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-264">0</span><span class="sxs-lookup"><span data-stu-id="b843b-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b843b-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-266">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-266">Note</span></span></strong><br/><p><span data-ttu-id="b843b-267">Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b843b-268">Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b843b-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="b843b-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b843b-270">Especifica a unidade de intervalo (hora 0-23, dia 0-31).</span><span class="sxs-lookup"><span data-stu-id="b843b-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b843b-271">0 para hora, 1 para dia</span><span class="sxs-lookup"><span data-stu-id="b843b-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-272">Publishing\Servers {serverID} \ UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b843b-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-273">um</span><span class="sxs-lookup"><span data-stu-id="b843b-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-274">Migrationmode</span><span class="sxs-lookup"><span data-stu-id="b843b-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-275">MIGRATIONmode</span><span class="sxs-lookup"><span data-stu-id="b843b-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-276">O modo de migração permite que o cliente App-V modifique atalhos e FTA de pacotes criados usando uma versão anterior do App-V.</span><span class="sxs-lookup"><span data-stu-id="b843b-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-277">Verdadeiro (estado habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="b843b-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b843b-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b843b-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-281">Permite que o computador executando o cliente App-V 5,0 colete e retorne determinadas informações de uso para que possamos melhorar ainda mais o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b843b-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-282">0 para desabilitado; 1 para habilitado</span><span class="sxs-lookup"><span data-stu-id="b843b-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="b843b-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-284">0</span><span class="sxs-lookup"><span data-stu-id="b843b-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b843b-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="b843b-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-287">Habilita scripts definidos no manifesto do pacote de arquivos de configuração que devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="b843b-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-288">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b843b-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="b843b-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b843b-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-292">Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário&#39;s.</span><span class="sxs-lookup"><span data-stu-id="b843b-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="b843b-293">Exemplo de uso:/ROAMINGFILEEXCLUSIONS =&#39;área de trabalho; minhas imagens&#39;</span><span class="sxs-lookup"><span data-stu-id="b843b-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b843b-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b843b-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-296">Especifica os caminhos do registro que não fazem roaming com um perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="b843b-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="b843b-297">Exemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="b843b-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-298">String</span><span class="sxs-lookup"><span data-stu-id="b843b-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b843b-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-300">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b843b-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-302">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-303">Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado por usuário.</span><span class="sxs-lookup"><span data-stu-id="b843b-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="b843b-304">todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho.</span><span class="sxs-lookup"><span data-stu-id="b843b-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b843b-305">Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote.</span><span class="sxs-lookup"><span data-stu-id="b843b-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b843b-306">Por exemplo:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="b843b-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-307">String</span><span class="sxs-lookup"><span data-stu-id="b843b-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b843b-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-309">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b843b-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-311">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-312">Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="b843b-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="b843b-313">todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho.</span><span class="sxs-lookup"><span data-stu-id="b843b-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b843b-314">Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote.</span><span class="sxs-lookup"><span data-stu-id="b843b-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b843b-315">Por exemplo:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="b843b-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-316">String</span><span class="sxs-lookup"><span data-stu-id="b843b-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b843b-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-318">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b843b-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-320">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-321">Uma lista delineada por vírgulas de extensões de nome de arquivo que podem ser usadas para determinar se um aplicativo instalado localmente pode ser executado no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="b843b-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="b843b-322">Quando os atalhos, FTAs e outros pontos de extensão forem criados durante a publicação, o App-V irá comparar a extensão de nome de arquivo com a lista se o aplicativo associado ao ponto de extensão for instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="b843b-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="b843b-323">Se a extensão for localizada, o <strong> </strong> parâmetro de linha de comando RunVirtual será adicionado, e o aplicativo será executado virtualmente.</span><span class="sxs-lookup"><span data-stu-id="b843b-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="b843b-324">Para obter mais informações sobre <strong> o </strong> parâmetro RunVirtual, consulte <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> executando um aplicativo instalado localmente dentro de um ambiente virtual com aplicativos virtualizados </a> .</span><span class="sxs-lookup"><span data-stu-id="b843b-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-325">String</span><span class="sxs-lookup"><span data-stu-id="b843b-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b843b-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-327">Valor da política não escrito</span><span class="sxs-lookup"><span data-stu-id="b843b-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="b843b-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-329">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-330">Permite que o cliente retorne informações para um servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="b843b-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-331">Verdadeiro (habilitado); Falso (estado desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="b843b-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-333">False</span><span class="sxs-lookup"><span data-stu-id="b843b-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="b843b-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-335">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-336">Especifica o local no servidor de relatório onde as informações do cliente são salvas.</span><span class="sxs-lookup"><span data-stu-id="b843b-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-337">String</span><span class="sxs-lookup"><span data-stu-id="b843b-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="b843b-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-339">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b843b-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-341">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-342">Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="b843b-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="b843b-343">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="b843b-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="b843b-344">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="b843b-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="b843b-345">Definido entre 0 e 1024.</span><span class="sxs-lookup"><span data-stu-id="b843b-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-346">Inteiro [0-1024]</span><span class="sxs-lookup"><span data-stu-id="b843b-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b843b-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-348">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b843b-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-350">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-351">Especifica o tamanho máximo em bytes a ser transmitido para o servidor para relatar solicitações de carregamento.</span><span class="sxs-lookup"><span data-stu-id="b843b-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="b843b-352">Isso pode ajudar a evitar falhas de transmissão permanente quando o log atingir um tamanho significativo.</span><span class="sxs-lookup"><span data-stu-id="b843b-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="b843b-353">Definido entre 1024 e ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b843b-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-354">Inteiro [1024-ilimitado]</span><span class="sxs-lookup"><span data-stu-id="b843b-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b843b-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-356">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="b843b-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-358">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-359">Especifica o tempo de início do cliente para enviar dados ao servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="b843b-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="b843b-360">Você deve especificar um inteiro válido entre 0-23 correspondente à hora do dia.</span><span class="sxs-lookup"><span data-stu-id="b843b-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="b843b-361">Por padrão, o <strong> ReportingStartTime </strong> começará no dia atual em 10 P. M ou 22.</span><span class="sxs-lookup"><span data-stu-id="b843b-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-362">Observação</span><span class="sxs-lookup"><span data-stu-id="b843b-362">Note</span></span></strong><br/><p><span data-ttu-id="b843b-363">Você deve definir essa configuração para um horário em que os computadores que executam o cliente App-V 5,0 têm menos probabilidade de ficar offline.</span><span class="sxs-lookup"><span data-stu-id="b843b-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-364">Inteiro (0 – 23)</span><span class="sxs-lookup"><span data-stu-id="b843b-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-365">Relatórios \ StartTime</span><span class="sxs-lookup"><span data-stu-id="b843b-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-366">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-368">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-369">Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="b843b-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-370">Inteiro</span><span class="sxs-lookup"><span data-stu-id="b843b-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="b843b-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-372">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="b843b-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-374">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-375">Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="b843b-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="b843b-376">Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e <strong> ReportingRandomDelay </strong> e esperará a duração especificada antes de enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="b843b-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="b843b-377">Isso pode ajudar a evitar colisões no servidor.</span><span class="sxs-lookup"><span data-stu-id="b843b-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-378">Inteiro [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="b843b-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="b843b-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-380">Valor da política não gravado (igual a não configurado)</span><span class="sxs-lookup"><span data-stu-id="b843b-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="b843b-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-382">Importante</span><span class="sxs-lookup"><span data-stu-id="b843b-382">Important</span></span></strong><br/><p><span data-ttu-id="b843b-383">Essa configuração está disponível somente com o App-V 5,0 SP2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b843b-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-384">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-385">Habilita as extensões do shell com suporte, os objetos auxiliares do navegador e os controles ActiveX para serem virtualizados e executados com aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="b843b-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-386">1 (habilitado), 0 (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="b843b-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="b843b-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-389">Importante</span><span class="sxs-lookup"><span data-stu-id="b843b-389">Important</span></span></strong><br/><p><span data-ttu-id="b843b-390">Essa configuração está disponível somente com o App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b843b-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-391">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-392">Habilita a barra de progresso de atualização de publicação do computador que executa o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b843b-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-393">1 (habilitado), 0 (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="b843b-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b843b-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="b843b-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b843b-396">Importante</span><span class="sxs-lookup"><span data-stu-id="b843b-396">Important</span></span></strong><br/><p><span data-ttu-id="b843b-397">Essa configuração está disponível somente com o App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b843b-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b843b-398">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-399">Oculta a barra de progresso de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="b843b-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-400">1 (habilitado), 0 (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="b843b-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b843b-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b843b-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-402">Não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b843b-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-403">Especifica uma lista de caminhos de processo (que podem conter caracteres curinga), que são candidatos ao uso de virtualização dinâmica (extensões do shell com suporte, objetos auxiliares do navegador e controles ActiveX).</span><span class="sxs-lookup"><span data-stu-id="b843b-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="b843b-404">Somente os processos cujo caminho completo corresponde a um desses itens podem usar a virtualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b843b-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-405">String</span><span class="sxs-lookup"><span data-stu-id="b843b-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b843b-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b843b-407">Cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="b843b-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="b843b-408">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b843b-408">Related topics</span></span>


[<span data-ttu-id="b843b-409">Implantação do sequenciador e do cliente App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b843b-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="b843b-410">Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="b843b-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="b843b-411">Como implantar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="b843b-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









