---
title: Como configurar um cache somente leitura no cliente do App-V (RDS)
description: Como configurar um cache somente leitura no cliente do App-V (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797227"
---
# <span data-ttu-id="bf9ca-103">Como configurar um cache somente leitura no cliente do App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="bf9ca-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="bf9ca-104">**Importante**  Você deve estar executando o App-V 4,6, SP1 para usar este procedimento.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="bf9ca-105">Você pode implantar o cliente App-V usando um cache compartilhado que é preenchido com todos os aplicativos necessários para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="bf9ca-106">Em seguida, você configura os clientes dos serviços de área de trabalho remota do App-V (RDS) para usar o mesmo arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="bf9ca-107">Os usuários recebem acesso a aplicativos específicos usando o processo de publicação do App-V.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="bf9ca-108">Como o cache já está pré-carregado com todos os aplicativos, não ocorrerá nenhum streaming quando um usuário iniciar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="bf9ca-109">No entanto, os pacotes usados para pré-popular o cache devem ser colocados em um servidor App-V que suporte a transmissão de protocolo RTSP (Real Time Streaming Protocol) e que conceda permissões de acesso aos clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="bf9ca-110">Se você publicar os aplicativos usando um servidor de gerenciamento App-V, poderá usá-lo para fornecer essa função de streaming.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="bf9ca-111">**Observação**  Os detalhes descritos nesses procedimentos destinam-se apenas a exemplos.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="bf9ca-112">Você pode usar métodos diferentes para concluir o processo geral.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="bf9ca-113">Implantando o cliente App-V em um cenário RDS</span><span class="sxs-lookup"><span data-stu-id="bf9ca-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="bf9ca-114">O processo de implantação consiste em quatro tarefas principais:</span><span class="sxs-lookup"><span data-stu-id="bf9ca-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="bf9ca-115">Criar e preencher o arquivo de cache compartilhado mestre</span><span class="sxs-lookup"><span data-stu-id="bf9ca-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="bf9ca-116">Copiando o arquivo de cache compartilhado para o armazenamento do servidor</span><span class="sxs-lookup"><span data-stu-id="bf9ca-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="bf9ca-117">Configurando o software do aplicativo cliente App-V</span><span class="sxs-lookup"><span data-stu-id="bf9ca-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="bf9ca-118">Gerenciando o ciclo de implantação de atualização para o arquivo de cache compartilhado após a implantação inicial</span><span class="sxs-lookup"><span data-stu-id="bf9ca-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="bf9ca-119">Essas tarefas exigem um planejamento cuidadoso.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-119">These tasks require careful planning.</span></span> <span data-ttu-id="bf9ca-120">Recomendamos que você prepare e documente um processo unificado e reproduzível para sua organização acompanhar.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="bf9ca-121">Isso é especialmente importante para a preparação e a implantação do arquivo de cache compartilhado mestre e para o gerenciamento contínuo de atualizações de aplicativos, cada um que exija uma atualização para o cache compartilhado mestre.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="bf9ca-122">Use os procedimentos a seguir para concluir essas tarefas principais.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="bf9ca-123">**Observação**  Embora você possa publicar os aplicativos usando vários métodos diferentes, os procedimentos a seguir se baseiam no uso de um servidor de gerenciamento App-V para publicação.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="bf9ca-124">Para configurar o cache somente leitura para a implantação inicial</span><span class="sxs-lookup"><span data-stu-id="bf9ca-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="bf9ca-125">Configure e configure um servidor de gerenciamento App-V para fornecer suporte à autenticação e publicação de usuários.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="bf9ca-126">Preencha a pasta de conteúdo deste servidor de gerenciamento com todos os pacotes de aplicativos necessários para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="bf9ca-127">Configure um computador temporário que tenha o cliente App-V instalado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="bf9ca-128">Faça logon no computador de teste usando uma conta que tenha acesso a todos os aplicativos para que o conjunto completo de aplicativos seja publicado no computador e, em seguida, transmita os aplicativos para o cache para que eles sejam totalmente carregados.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="bf9ca-129">Importante</span><span class="sxs-lookup"><span data-stu-id="bf9ca-129">Important</span></span>**  
   <span data-ttu-id="bf9ca-130">O computador de preparação deve usar o mesmo tipo de sistema operacional e arquitetura do sistema que os usados pelas VMs nas quais o cliente App-V será executado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="bf9ca-131">Reinicie o computador de preparação no modo de segurança para garantir que os drivers não sejam iniciados, pois isso bloquearia o arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="bf9ca-132">Observação</span><span class="sxs-lookup"><span data-stu-id="bf9ca-132">Note</span></span>**  
   <span data-ttu-id="bf9ca-133">Ou, você pode parar e desabilitar o serviço Application Virtualization e reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="bf9ca-134">Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="bf9ca-135">Copie o arquivo de cache Sftfs. FSD para uma SAN em que todos os servidores RDS possam acessá-lo, por exemplo, em uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="bf9ca-136">Defina as permissões de acesso de pasta como somente leitura para o grupo todos e para controle total para administradores que gerenciarão as atualizações de arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="bf9ca-137">O local do arquivo de cache pode ser obtido a partir da chave do registro AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="bf9ca-138">Importante</span><span class="sxs-lookup"><span data-stu-id="bf9ca-138">Important</span></span>**  
   <span data-ttu-id="bf9ca-139">Você deve colocar o arquivo FSD em um local que tenha a capacidade de resposta e a confiabilidade iguais ao desempenho de armazenamento conectado localmente, por exemplo, uma SAN.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="bf9ca-140">Instale o cliente App-V RDS em cada servidor RDS e, em seguida, configure-o para usar o cache somente leitura adicionando os seguintes valores de chave do registro para a chave AppFS no cliente.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="bf9ca-141">A chave AppFS está localizada em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS para computadores de 32 bits e em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS para computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="bf9ca-142">Chave</span><span class="sxs-lookup"><span data-stu-id="bf9ca-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="bf9ca-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf9ca-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="bf9ca-144">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9ca-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="bf9ca-145">Finalidade</span><span class="sxs-lookup"><span data-stu-id="bf9ca-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bf9ca-146">FileName</span><span class="sxs-lookup"><span data-stu-id="bf9ca-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-147">String</span><span class="sxs-lookup"><span data-stu-id="bf9ca-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-148">caminho do FSD</span><span class="sxs-lookup"><span data-stu-id="bf9ca-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-149">Especifica o caminho do arquivo de cache compartilhado, por exemplo, \RDSServername\Sharefolder\SFTFS. FSD (obrigatório).</span><span class="sxs-lookup"><span data-stu-id="bf9ca-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bf9ca-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="bf9ca-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="bf9ca-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-152">um</span><span class="sxs-lookup"><span data-stu-id="bf9ca-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-153">Configura o cliente para operar no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="bf9ca-154">Isso garante que o cliente não tentará transmitir atualizações para o cache do pacote.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="bf9ca-155">(Obrigatório)</span><span class="sxs-lookup"><span data-stu-id="bf9ca-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bf9ca-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="bf9ca-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-157">String</span><span class="sxs-lookup"><span data-stu-id="bf9ca-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-158">caminho do arquivo log de erros (. ETL)</span><span class="sxs-lookup"><span data-stu-id="bf9ca-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bf9ca-159">Entrada usada para especificar o caminho do log de erros.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="bf9ca-160">Usar.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-160">(Recommended.</span></span> <span data-ttu-id="bf9ca-161">Use um caminho local como C:\Logs\Sftfs.etl.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="bf9ca-162">Configure cada servidor RDS no farm para usar o servidor de publicação e para usar a atualização de publicação quando os usuários fizerem logon.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="bf9ca-163">Conforme os usuários fazem logon nos servidores RDS, um ciclo de atualização de publicação ocorre e publica todos os aplicativos para os quais sua conta está autorizada.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="bf9ca-164">Esses aplicativos são executados do cache compartilhado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="bf9ca-165">Para configurar a atualização do cliente RDS para pacote</span><span class="sxs-lookup"><span data-stu-id="bf9ca-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="bf9ca-166">Conclua a atualização e o teste do pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="bf9ca-167">Atualize o pacote no App-V Server.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="bf9ca-168">Em seguida, publique e transmita a nova versão dos aplicativos para o cliente no computador temporário para que eles sejam totalmente carregados no cache.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="bf9ca-169">Reinicie o computador de teste no modo de segurança para garantir que os drivers não sejam iniciados.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="bf9ca-170">**Observação**  Ou, primeiro, você pode parar e, em seguida, desabilitar o serviço Application Virtualization no Services. msc e reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="bf9ca-171">Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="bf9ca-172">Copie o arquivo de cache Sftfs. FSD para uma SAN em que todos os servidores RDS possam acessá-lo, por exemplo, em uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="bf9ca-173">Você pode usar um nome de arquivo diferente, por exemplo, SFTFS \ _V2. FSD, para distinguir a nova versão.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="bf9ca-174">Para configurar o cliente App-V RDS em cada servidor RDS no farm para usar o arquivo de cache compartilhado atualizado, altere o valor do nome de arquivo da chave do registro AppFS para apontar para o local do arquivo atualizado, por exemplo, \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="bf9ca-175">Isso garante que cada servidor RDS receba a cópia atualizada do cache quando os drivers do aplicativo-Vclient forem reiniciados.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="bf9ca-176">**Importante**  Você deve reiniciar os servidores RDS para usar o arquivo de cache compartilhado atualizado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="bf9ca-177">Como usar links simbólicos ao atualizar o cache</span><span class="sxs-lookup"><span data-stu-id="bf9ca-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="bf9ca-178">Em vez de alterar o valor do nome de arquivo da chave AppFS sempre que um novo arquivo de cache for implantado contendo pacotes novos ou atualizados, você poderá usar um link simbólico nos seguintes sistemas operacionais: Windows Vista, Windows 7 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="bf9ca-179">Para obter mais informações sobre links simbólicos, consulte [links simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="bf9ca-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="bf9ca-180">Em contraste, o Windows XP não oferece suporte ao uso de links simbólicos, e você deve usar pontos de junção em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="bf9ca-181">Para obter mais informações sobre junções, consulte o [artigo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) na base de dados de conhecimento Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) e também a junção de ferramenta [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="bf9ca-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="bf9ca-182">Para configurar um link simbólico para fazer referência ao cache</span><span class="sxs-lookup"><span data-stu-id="bf9ca-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="bf9ca-183">Durante o estágio de implantação inicial, abra uma janela do prompt de comando como administrador local no sistema operacional do host do servidor RDS.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="bf9ca-184">Crie um link simbólico usando o comando MKLINK e, em seguida, configure-o para apontar para o arquivo Sftfs. FSD.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="bf9ca-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="bf9ca-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="bf9ca-186">Na imagem da VM do VDI Master, abra uma janela do prompt de comando usando a opção **Executar como administrador** e conceder permissões de link remoto para que a VM possa acessar o link simbólico no sistema operacional do host VDI.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="bf9ca-187">Por padrão, as permissões de link remoto são desativadas.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="bf9ca-188">fsutil Behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="bf9ca-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="bf9ca-189">**Observação**  No servidor de armazenamento, as permissões de link adequadas devem estar habilitadas.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="bf9ca-190">Dependendo da localização do link e do arquivo Sftfs. FSD, as permissões são **L2L: 1** ou **l2r: 1** ou **R2L: 1** ou **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="bf9ca-191">Ao configurar o cliente App-V RDS, defina o valor do nome de arquivo do AppFS da chave igual ao caminho UNC do arquivo FSD que está usando o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="bf9ca-192">Por exemplo, defina o nome do arquivo como \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="bf9ca-193">Quando o cliente App-V acessa o cache pela primeira vez, o link simbólico passa para o identificador do cliente a para o arquivo de cache.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="bf9ca-194">O cliente continua a usar essa manipulação enquanto o cliente estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="bf9ca-195">O valor do link simbólico pode ser atualizado com segurança, mesmo se os clientes existentes tiverem o antigo cache compartilhado aberto.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="bf9ca-196">Quando você deve atualizar um pacote ou adicionar um novo pacote ao cache, siga as etapas de 1 a 4 do procedimento de atualização.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="bf9ca-197">Em seguida, exclua o link simbólico e crie-o novamente para apontar para a nova versão do arquivo de cache compartilhado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="bf9ca-198">Isso garante que cada servidor RDS receba a cópia atualizada do cache quando os drivers do cliente App-V forem reiniciados.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="bf9ca-199">Quando o servidor RDS é reiniciado, o cliente App-V recebe um identificador para a cópia atualizada do cache porque o cliente usa o caminho que contém o link simbólico atualizado.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="bf9ca-200">Em seguida, os usuários têm acesso aos aplicativos novos e atualizados.</span><span class="sxs-lookup"><span data-stu-id="bf9ca-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="bf9ca-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf9ca-201">Related topics</span></span>


[<span data-ttu-id="bf9ca-202">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="bf9ca-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="bf9ca-203">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="bf9ca-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="bf9ca-204">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="bf9ca-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





