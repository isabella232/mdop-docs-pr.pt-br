---
title: Como configurar um cache somente leitura no cliente do App-V (VDI)
description: Como configurar um cache somente leitura no cliente do App-V (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797226"
---
# <span data-ttu-id="931eb-103">Como configurar um cache somente leitura no cliente do App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="931eb-103">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>


<span data-ttu-id="931eb-104">No Microsoft Application Virtualization (App-V) 4,6, o cliente dá suporte ao uso de um cache somente leitura compartilhado.</span><span class="sxs-lookup"><span data-stu-id="931eb-104">In Microsoft Application Virtualization (App-V) 4.6 the Client supports using a shared read-only cache.</span></span> <span data-ttu-id="931eb-105">O cache somente leitura compartilhado permite que o cliente use o espaço em disco de forma eficiente em um sistema da Virtual Desktop Infrastructure (VDI), em que os usuários executam aplicativos em máquinas virtuais (VM) hospedadas em um ambiente de servidor de data center e compartilham armazenamento de rede em uma rede de área de armazenamento (SAN).</span><span class="sxs-lookup"><span data-stu-id="931eb-105">The shared read-only cache enables the Client to use disk space efficiently in a Virtual Desktop Infrastructure (VDI) system, where users run applications on Virtual Machines (VM) that are hosted in a data center server environment and share network storage on a Storage Area Network (SAN).</span></span> <span data-ttu-id="931eb-106">Os procedimentos a seguir fornecem uma visão geral do processo necessário para implementar o cliente App-V em qualquer uma das arquiteturas de VDI primárias, conhecida como "VM em pool" ou "VM estática".</span><span class="sxs-lookup"><span data-stu-id="931eb-106">The following procedures provide an overview of the process that is required to implement the App-V Client in either of the primary VDI architectures, known as “Pooled VM” or “Static VM”.</span></span> <span data-ttu-id="931eb-107">Presume-se que você esteja familiarizado com o planejamento, a implantação e a operação do sistema App-V e seus componentes e também a operação e o gerenciamento do servidor VDI.</span><span class="sxs-lookup"><span data-stu-id="931eb-107">It is assumed that you are familiar with the planning, deployment, and operation of the App-V system and its components, and also the operation and management of the VDI server.</span></span> <span data-ttu-id="931eb-108">Para obter mais informações sobre o App-V, consulte [virtualização de aplicativo](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)</span><span class="sxs-lookup"><span data-stu-id="931eb-108">For more information about App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)</span></span>

<span data-ttu-id="931eb-109">**Observação**  Os detalhes descritos nesses procedimentos destinam-se apenas a exemplos.</span><span class="sxs-lookup"><span data-stu-id="931eb-109">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="931eb-110">Você pode usar métodos diferentes para concluir o processo geral.</span><span class="sxs-lookup"><span data-stu-id="931eb-110">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="931eb-111">Implantando o cliente App-V em um cenário VDI</span><span class="sxs-lookup"><span data-stu-id="931eb-111">Deploying the App-V Client in a VDI Scenario</span></span>


<span data-ttu-id="931eb-112">Você pode implantar o cliente App-V em um cenário VDI usando um cache somente leitura compartilhado que foi preenchido com todos os aplicativos necessários para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="931eb-112">You can deploy the App-V Client in a VDI scenario by using a shared read-only cache that has been populated with all the applications required for all users.</span></span> <span data-ttu-id="931eb-113">Em seguida, você configura a imagem da VM mestre do VDI para que todos os clientes do App-V usem o mesmo arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-113">You then configure the VDI Master VM Image so that all the App-V Clients use the same cache file.</span></span> <span data-ttu-id="931eb-114">Os usuários recebem acesso a aplicativos específicos usando o processo de publicação do App-V.</span><span class="sxs-lookup"><span data-stu-id="931eb-114">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="931eb-115">Já que o cache já está pré-carregado com todos os aplicativos, nenhum streaming ocorre quando um usuário inicia um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="931eb-115">Since the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="931eb-116">No entanto, os pacotes usados para pré-popular o cache devem ser colocados em um servidor App-V que suporte a transmissão de protocolo RTSP (Real Time Streaming Protocol) e que conceda permissões de acesso aos clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="931eb-116">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="931eb-117">Se você publicar os aplicativos usando um servidor de gerenciamento App-V, poderá usá-lo para fornecer essa função de streaming.</span><span class="sxs-lookup"><span data-stu-id="931eb-117">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="931eb-118">O processo de implantação consiste em quatro tarefas principais:</span><span class="sxs-lookup"><span data-stu-id="931eb-118">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="931eb-119">Criar e preencher o arquivo de cache compartilhado mestre</span><span class="sxs-lookup"><span data-stu-id="931eb-119">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="931eb-120">Copiando o arquivo de cache compartilhado para o armazenamento do servidor VDI</span><span class="sxs-lookup"><span data-stu-id="931eb-120">Copying the shared cache file to the VDI server storage</span></span>

-   <span data-ttu-id="931eb-121">Configurando o software cliente App-V na imagem mestra do VDI</span><span class="sxs-lookup"><span data-stu-id="931eb-121">Configuring the App-V client software on the VDI Master Image</span></span>

-   <span data-ttu-id="931eb-122">Gerenciando o ciclo de implantação de atualização para o arquivo de cache compartilhado após a implantação inicial</span><span class="sxs-lookup"><span data-stu-id="931eb-122">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="931eb-123">Essas tarefas exigem um planejamento cuidadoso.</span><span class="sxs-lookup"><span data-stu-id="931eb-123">These tasks require careful planning.</span></span> <span data-ttu-id="931eb-124">Recomendamos que você prepare e documente um processo unificado e reproduzível para sua organização acompanhar.</span><span class="sxs-lookup"><span data-stu-id="931eb-124">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="931eb-125">Isso é especialmente importante para a preparação e implantação iniciais do arquivo de cache principal compartilhado e para o gerenciamento contínuo de atualizações de aplicativos, cada uma delas requer uma atualização do cache compartilhado mestre.</span><span class="sxs-lookup"><span data-stu-id="931eb-125">This is especially important for the initial preparation and deployment of the master shared cache file, and for the on-going management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="931eb-126">Use os procedimentos a seguir para concluir essas tarefas principais.</span><span class="sxs-lookup"><span data-stu-id="931eb-126">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="931eb-127">**Observação**  Embora você possa publicar os aplicativos usando vários métodos diferentes, os procedimentos a seguir se baseiam no uso de um servidor de gerenciamento App-V para publicação.</span><span class="sxs-lookup"><span data-stu-id="931eb-127">**Note** Although you can publish the applications by using several different methods, the following procedures are based on the use of an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="931eb-128">Para configurar o cache somente leitura para implantação inicial em uma VDI de VM em pool ou em um cenário de VDI de VM estática</span><span class="sxs-lookup"><span data-stu-id="931eb-128">To configure the read-only cache for initial deployment in a Pooled VM VDI or Static VM VDI scenario</span></span>**

1. <span data-ttu-id="931eb-129">Configure e configure um servidor de gerenciamento App-V em uma VM no servidor VDI para fornecer suporte à autenticação e publicação de usuários.</span><span class="sxs-lookup"><span data-stu-id="931eb-129">Set up and configure an App-V Management Server in a VM on the VDI server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="931eb-130">Preencha a pasta de conteúdo deste servidor de gerenciamento com todos os pacotes de aplicativos necessários para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="931eb-130">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="931eb-131">Configure um computador temporário que tenha o cliente App-V instalado.</span><span class="sxs-lookup"><span data-stu-id="931eb-131">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="931eb-132">Faça logon no computador de teste com uma conta que tenha acesso a todos os aplicativos para que o conjunto completo de aplicativos sejam publicados no computador e, em seguida, transmita os aplicativos para o cache, para que eles sejam totalmente carregados.</span><span class="sxs-lookup"><span data-stu-id="931eb-132">Log on to the staging computer with an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="931eb-133">Importante</span><span class="sxs-lookup"><span data-stu-id="931eb-133">Important</span></span>**  
   <span data-ttu-id="931eb-134">O computador de preparação deve usar o mesmo tipo de sistema operacional e arquitetura do sistema que os usados pelas VMs nas quais o cliente App-V será executado.</span><span class="sxs-lookup"><span data-stu-id="931eb-134">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="931eb-135">Reinicie o computador de preparação no modo de segurança para garantir que os drivers não sejam iniciados, o que bloquearia o arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-135">Restart the staging computer in Safe Mode to ensure the drivers are not started, which would lock the cache file.</span></span>

   **<span data-ttu-id="931eb-136">Observação</span><span class="sxs-lookup"><span data-stu-id="931eb-136">Note</span></span>**  
   <span data-ttu-id="931eb-137">Você também pode parar e desabilitar o serviço Application Virtualization e reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="931eb-137">Alternatively, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="931eb-138">Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.</span><span class="sxs-lookup"><span data-stu-id="931eb-138">After the file has been copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="931eb-139">Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="931eb-139">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="931eb-140">Defina as permissões de acesso de pasta como somente leitura para o grupo todos e para controle total para administradores que gerenciarão as atualizações de arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-140">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="931eb-141">O local do arquivo de cache pode ser obtido a partir da chave do registro AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="931eb-141">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="931eb-142">Importante</span><span class="sxs-lookup"><span data-stu-id="931eb-142">Important</span></span>**  
   <span data-ttu-id="931eb-143">Você deve colocar o arquivo FSD em um local com a capacidade de resposta e a confiabilidade equivalente ao desempenho de armazenamento conectado localmente, por exemplo, uma SAN.</span><span class="sxs-lookup"><span data-stu-id="931eb-143">You must put the FSD file in a location that has the responsiveness and reliability equivalent to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="931eb-144">Instale o cliente da área de trabalho do App-V na imagem da VM principal do VDI e, em seguida, configure-o para usar o cache somente leitura adicionando os seguintes valores de chave do registro para a chave AppFS no cliente.</span><span class="sxs-lookup"><span data-stu-id="931eb-144">Install the App-V Desktop Client on the VDI Master VM Image, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="931eb-145">A chave AppFS está localizada em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.</span><span class="sxs-lookup"><span data-stu-id="931eb-145">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="931eb-146">Chave</span><span class="sxs-lookup"><span data-stu-id="931eb-146">Key</span></span></th>
   <th align="left"><span data-ttu-id="931eb-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="931eb-147">Type</span></span></th>
   <th align="left"><span data-ttu-id="931eb-148">Valor</span><span class="sxs-lookup"><span data-stu-id="931eb-148">Value</span></span></th>
   <th align="left"><span data-ttu-id="931eb-149">Finalidade</span><span class="sxs-lookup"><span data-stu-id="931eb-149">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="931eb-150">FileName</span><span class="sxs-lookup"><span data-stu-id="931eb-150">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-151">String</span><span class="sxs-lookup"><span data-stu-id="931eb-151">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-152">caminho para FSD</span><span class="sxs-lookup"><span data-stu-id="931eb-152">path to FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-153">Especifica o caminho para o arquivo de cache compartilhado, por exemplo, \VDIServername\Sharefolder\SFTFS. FSD (obrigatório).</span><span class="sxs-lookup"><span data-stu-id="931eb-153">Specifies the path to the shared cache file, for example, \VDIServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="931eb-154">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="931eb-154">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="931eb-155">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-156">um</span><span class="sxs-lookup"><span data-stu-id="931eb-156">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-157">Configura o cliente para operar no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="931eb-157">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="931eb-158">Isso garante que o cliente não tentará transmitir atualizações para o cache do pacote.</span><span class="sxs-lookup"><span data-stu-id="931eb-158">This ensures that the client will not attempt to stream updates to the package cache.</span></span> <span data-ttu-id="931eb-159">(Obrigatório)</span><span class="sxs-lookup"><span data-stu-id="931eb-159">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="931eb-160">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="931eb-160">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-161">String</span><span class="sxs-lookup"><span data-stu-id="931eb-161">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-162">caminho para o arquivo log de erros (. ETL)</span><span class="sxs-lookup"><span data-stu-id="931eb-162">path to error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="931eb-163">Entrada usada para especificar o caminho para o log de erros.</span><span class="sxs-lookup"><span data-stu-id="931eb-163">Entry used to specify the path to the error log.</span></span> <span data-ttu-id="931eb-164">Usar.</span><span class="sxs-lookup"><span data-stu-id="931eb-164">(Recommended.</span></span> <span data-ttu-id="931eb-165">Use um caminho local como C:\Logs\Sftfs.etl.</span><span class="sxs-lookup"><span data-stu-id="931eb-165">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="931eb-166">Configurar o cliente de imagem principal da VM para usar o servidor de publicação e usar a atualização de publicação durante o logon.</span><span class="sxs-lookup"><span data-stu-id="931eb-166">Configure the Master VM Image client to use the publishing server and to use publishing refresh at logon.</span></span> <span data-ttu-id="931eb-167">À medida que os usuários fazem logon no sistema VDI e sua VM é criada a partir da imagem mestra da VM, um ciclo de atualização de publicação ocorre e publica todos os aplicativos para os quais sua conta está autorizada.</span><span class="sxs-lookup"><span data-stu-id="931eb-167">As users log on to the VDI system and their VM is built from the Master VM Image, a publishing refresh cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="931eb-168">Esses aplicativos são executados do cache compartilhado.</span><span class="sxs-lookup"><span data-stu-id="931eb-168">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="931eb-169">Para configurar o cliente para a atualização do pacote em um cenário de VM em pool</span><span class="sxs-lookup"><span data-stu-id="931eb-169">To configure the client for package upgrade in a Pooled VM scenario</span></span>**

1.  <span data-ttu-id="931eb-170">Conclua a atualização e o teste do pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="931eb-170">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="931eb-171">Atualize o pacote no App-V Server.</span><span class="sxs-lookup"><span data-stu-id="931eb-171">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="931eb-172">Em seguida, publique e transmita a nova versão dos aplicativos para o cliente no computador temporário para que eles sejam totalmente carregados no cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-172">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="931eb-173">Reinicie o computador de teste no modo de segurança para garantir que os drivers não sejam iniciados.</span><span class="sxs-lookup"><span data-stu-id="931eb-173">Restart the staging computer in Safe Mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="931eb-174">**Observação**  Você também pode parar e desabilitar o serviço Application Virtualization no Services. msc e reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="931eb-174">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="931eb-175">Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.</span><span class="sxs-lookup"><span data-stu-id="931eb-175">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="931eb-176">Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="931eb-176">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="931eb-177">Você pode usar um nome de arquivo diferente, por exemplo, SFTFS \ _V2. FSD, para distinguir a nova versão.</span><span class="sxs-lookup"><span data-stu-id="931eb-177">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="931eb-178">Para configurar o cliente da área de trabalho do App-V na imagem da VM principal do VDI para usar o arquivo de cache compartilhado atualizado, altere o valor do nome de arquivo da chave do registro AppFS para apontar para o local do arquivo atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="931eb-178">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="931eb-179">Quando os usuários fazem logoff e, em seguida, fazem logon novamente, uma nova VM é criada para ele usando a imagem mestra atualizada.</span><span class="sxs-lookup"><span data-stu-id="931eb-179">When users log off and then log on again, a new VM is created for them by using the updated Master Image.</span></span> <span data-ttu-id="931eb-180">Todas as configurações do usuário serão mantidas e aplicadas à nova VM.</span><span class="sxs-lookup"><span data-stu-id="931eb-180">All their user settings will be retained and applied to the new VM.</span></span> <span data-ttu-id="931eb-181">Em seguida, eles têm acesso aos aplicativos atualizados.</span><span class="sxs-lookup"><span data-stu-id="931eb-181">Then they have access to the updated applications.</span></span>

**<span data-ttu-id="931eb-182">Para configurar o cliente para a atualização do pacote em um cenário de VM estática</span><span class="sxs-lookup"><span data-stu-id="931eb-182">To configure the client for package upgrade in a Static VM scenario</span></span>**

1.  <span data-ttu-id="931eb-183">Conclua a atualização e o teste do pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="931eb-183">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="931eb-184">Atualize o pacote no App-V Server.</span><span class="sxs-lookup"><span data-stu-id="931eb-184">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="931eb-185">Em seguida, publique e transmita a nova versão dos aplicativos para o cliente no computador temporário para que os aplicativos sejam totalmente carregados no cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-185">Then, publish and stream the new version of the applications to the client on the staging computer so that the applications are fully loaded into cache.</span></span>

3.  <span data-ttu-id="931eb-186">Reinicie o computador de preparação no modo de segurança para garantir que os drivers não sejam iniciados.</span><span class="sxs-lookup"><span data-stu-id="931eb-186">Restart the staging computer in Safe Mode to ensure that the drivers are not started.</span></span>

    <span data-ttu-id="931eb-187">**Observação**  Você também pode parar e desabilitar o serviço Application Virtualization no Services. msc e reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="931eb-187">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="931eb-188">Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.</span><span class="sxs-lookup"><span data-stu-id="931eb-188">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="931eb-189">Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="931eb-189">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="931eb-190">Você pode usar um nome de arquivo diferente, por exemplo, SFTFS \ _V2. FSD, para distinguir a nova versão.</span><span class="sxs-lookup"><span data-stu-id="931eb-190">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="931eb-191">Para configurar o cliente da área de trabalho do App-V na imagem da VM principal do VDI para usar o arquivo de cache compartilhado atualizado, altere o valor do nome de arquivo da chave do registro AppFS para apontar para o local do arquivo atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="931eb-191">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="931eb-192">Isso garante que novos usuários obtenham a nova versão.</span><span class="sxs-lookup"><span data-stu-id="931eb-192">This ensures that new users get the new version.</span></span>

6.  <span data-ttu-id="931eb-193">Crie um script que edite o valor de nome de arquivo da chave AppFS para defini-lo como o local do cache atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="931eb-193">Create a script that edits the AppFS key FILENAME value to set it to the location of the updated cache, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="931eb-194">Configure esse script para ser executado quando o usuário fizer logoff ou logon para que ele seja executado antes do início dos drivers do cliente App-V, por exemplo, usando as configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="931eb-194">Configure this script to run when the user logs off or logs on so that it runs before the App-V client drivers start, for example, by using Group Policy settings.</span></span> <span data-ttu-id="931eb-195">Quando os usuários fazem logoff e se reconectam novamente, a VM existente é atualizada e ele usará a cópia atualizada do cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-195">When users log off and log on again, their existing VM is updated, and they will use the updated copy of the cache.</span></span> <span data-ttu-id="931eb-196">Em seguida, eles têm acesso aos aplicativos atualizados.</span><span class="sxs-lookup"><span data-stu-id="931eb-196">Then, they have access to the updated applications.</span></span>

## <span data-ttu-id="931eb-197">Como usar links simbólicos ao atualizar o cache</span><span class="sxs-lookup"><span data-stu-id="931eb-197">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="931eb-198">Em vez de modificar o valor do nome de arquivo da chave AppFS sempre que um novo arquivo de cache for implantado contendo pacotes novos ou atualizados, você pode usar um link simbólico nos seguintes sistemas operacionais: Windows Vista, Windows 7 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="931eb-198">Instead of modifying the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="931eb-199">Para obter mais informações sobre links simbólicos, consulte [links simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="931eb-199">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="931eb-200">Em contraste, o Windows XP não oferece suporte ao uso de links simbólicos, e você deve usar pontos de junção em vez disso.</span><span class="sxs-lookup"><span data-stu-id="931eb-200">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="931eb-201">Para obter mais informações sobre junções, consulte o [artigo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) na base de dados de conhecimento Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) e também a junção de ferramenta [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="931eb-201">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="931eb-202">Para configurar um link simbólico para fazer referência ao cache</span><span class="sxs-lookup"><span data-stu-id="931eb-202">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="931eb-203">Durante o estágio de implantação inicial, abra uma janela do prompt de comando como administrador local no sistema operacional do host do servidor VDI.</span><span class="sxs-lookup"><span data-stu-id="931eb-203">During the initial deployment stage, open a Command Prompt window as a local administrator on the VDI server host operating system.</span></span>

2.  <span data-ttu-id="931eb-204">Crie um link simbólico usando o comando MKLINK e, em seguida, configure-o para apontar para o arquivo Sftfs. FSD.</span><span class="sxs-lookup"><span data-stu-id="931eb-204">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="931eb-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="931eb-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="931eb-206">Na imagem da VM do VDI Master, abra uma janela do prompt de comando usando a opção **Executar como administrador** e conceder permissões de link remoto para que a VM possa acessar o link simbólico no sistema operacional do host VDI.</span><span class="sxs-lookup"><span data-stu-id="931eb-206">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="931eb-207">Por padrão, as permissões de link remoto são desativadas.</span><span class="sxs-lookup"><span data-stu-id="931eb-207">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="931eb-208">fsutil Behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="931eb-208">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="931eb-209">**Observação**  No servidor de armazenamento, as permissões de link adequadas devem estar habilitadas.</span><span class="sxs-lookup"><span data-stu-id="931eb-209">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="931eb-210">Dependendo da localização do link e do arquivo Sftfs. FSD, as permissões são **L2L: 1** ou **l2r: 1** ou **R2L: 1** ou **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="931eb-210">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="931eb-211">Quando você configura o cliente da área de trabalho do App-V na imagem da VM principal do VDI, defina o valor do nome de arquivo do AppFS da chave igual ao caminho UNC do arquivo FSD que está usando o link simbólico; por exemplo, defina-o como \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="931eb-211">When you configure the App-V Desktop Client on the VDI Master VM Image, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link; for example, set it to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="931eb-212">Quando o cliente App-V acessa o cache pela primeira vez, o link simbólico passa para o identificador do cliente a para o arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="931eb-212">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="931eb-213">O cliente continua a usar essa manipulação enquanto o cliente estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="931eb-213">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="931eb-214">O valor do link simbólico pode ser atualizado com segurança, mesmo se os clientes existentes tiverem o antigo cache compartilhado aberto.</span><span class="sxs-lookup"><span data-stu-id="931eb-214">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="931eb-215">Quando você deve atualizar um pacote ou adicionar um novo pacote ao cache, siga as etapas de 1 a 5 do procedimento de atualização para a VM estática ou o cenário da máquina virtual em pool.</span><span class="sxs-lookup"><span data-stu-id="931eb-215">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 5 of the upgrade procedure for either the Static VM or Pooled VM scenario.</span></span> <span data-ttu-id="931eb-216">Em seguida, exclua o link simbólico e crie-o novamente para apontar para a nova versão do arquivo de cache compartilhado.</span><span class="sxs-lookup"><span data-stu-id="931eb-216">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="931eb-217">Quando a VM é reiniciada, o cliente recebe um identificador para a cópia atualizada do cache porque a VM usa o caminho que contém o link simbólico atualizado.</span><span class="sxs-lookup"><span data-stu-id="931eb-217">When the VM is restarted, the client receives a handle to the updated copy of the cache because the VM uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="931eb-218">Em seguida, os usuários têm acesso aos aplicativos novos e atualizados.</span><span class="sxs-lookup"><span data-stu-id="931eb-218">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="931eb-219">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="931eb-219">Related topics</span></span>


[<span data-ttu-id="931eb-220">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="931eb-220">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="931eb-221">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="931eb-221">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="931eb-222">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="931eb-222">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





