---
title: Lista de verificação de upgrade do App-V
description: Lista de verificação de upgrade do App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797585"
---
# <span data-ttu-id="de4c2-103">Lista de verificação de upgrade do App-V</span><span class="sxs-lookup"><span data-stu-id="de4c2-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="de4c2-104">Antes de tentar atualizar para versões do Microsoft Application Virtualization (App-V) 4,5 ou posterior, qualquer versão anterior ao App-V 4,1 deve ser atualizada para o App-V 4,1.</span><span class="sxs-lookup"><span data-stu-id="de4c2-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="de4c2-105">Você deve planejar a atualização dos clientes primeiro e, em seguida, atualizar os componentes do servidor.</span><span class="sxs-lookup"><span data-stu-id="de4c2-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="de4c2-106">Os clientes do App-V que foram atualizados para o App-V 4,5 continuam a funcionar com servidores App-V que ainda não foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="de4c2-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="de4c2-107">Não há suporte para versões anteriores do cliente em servidores que foram atualizados para o App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de4c2-108">Etapa</span><span class="sxs-lookup"><span data-stu-id="de4c2-108">Step</span></span></th>
<th align="left"><span data-ttu-id="de4c2-109">Referência</span><span class="sxs-lookup"><span data-stu-id="de4c2-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-110">Atualize os clientes do App-V.</span><span class="sxs-lookup"><span data-stu-id="de4c2-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="de4c2-111">Como fazer upgrade do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="de4c2-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-112">Atualize o banco de dados e os servidores do App-V.</span><span class="sxs-lookup"><span data-stu-id="de4c2-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="de4c2-113">Importante</span><span class="sxs-lookup"><span data-stu-id="de4c2-113">Important</span></span></strong><br/><p><span data-ttu-id="de4c2-114">Se você tiver mais de um servidor com acesso de compartilhamento ao banco de dados do App-V, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="de4c2-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="de4c2-115">Você deve seguir as práticas comerciais regulares para a atualização do banco de dados, mas recomendamos testar a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste.</span><span class="sxs-lookup"><span data-stu-id="de4c2-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="de4c2-116">Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de4c2-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="de4c2-117">Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar o software App-V nos outros servidores.</span><span class="sxs-lookup"><span data-stu-id="de4c2-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="de4c2-118">Como fazer upgrade dos componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="de4c2-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-119">Atualize o serviço Web de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="de4c2-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="de4c2-120">Esta etapa se aplica apenas se o serviço Web de gerenciamento estiver em um servidor separado, o que exigirá que você execute o programa de instalação do servidor nesse servidor separado para atualizar o serviço Web de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="de4c2-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="de4c2-121">Caso contrário, a etapa anterior de atualização do servidor atualizará automaticamente o serviço Web de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="de4c2-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="de4c2-122">Como fazer upgrade dos componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="de4c2-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-123">Atualize o console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="de4c2-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="de4c2-124">Esta etapa se aplica apenas se o console de gerenciamento estiver em um computador separado, o que exigirá que você execute o programa de instalação do servidor nesse computador separado para atualizar o console.</span><span class="sxs-lookup"><span data-stu-id="de4c2-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="de4c2-125">Caso contrário, a etapa anterior de atualização do servidor atualizará o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="de4c2-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="de4c2-126">Como fazer upgrade dos componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="de4c2-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-127">Atualize o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="de4c2-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="de4c2-128">Como fazer upgrade do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="de4c2-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="de4c2-129">Considerações de atualização adicionais</span><span class="sxs-lookup"><span data-stu-id="de4c2-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="de4c2-130">Qualquer pacote de aplicativos virtual sequenciado na versão 4,2 não terá que ser sequenciado novamente para uso com a versão 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="de4c2-131">No entanto, você deve considerar a atualização dos pacotes virtuais para o formato 4,5 do Microsoft Application Virtualization se desejar aplicar ACLs (listas de controle de acesso) padrão ou gerar um arquivo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="de4c2-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="de4c2-132">Isso é um processo simples e requer que o pacote de aplicativo virtual existente seja aberto e salvo com o sequenciador do App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="de4c2-133">Isso pode ser automatizado usando a interface de linha de comando App-VSequencer.</span><span class="sxs-lookup"><span data-stu-id="de4c2-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="de4c2-134">Para obter mais informações, consulte [como criar ou atualizar aplicativos virtuais usando o sequenciador App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span><span class="sxs-lookup"><span data-stu-id="de4c2-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="de4c2-135">Um dos recursos do sequenciador 4,5 é a capacidade de criar arquivos do Windows Installer (. msi) como pontos de controle para interoperabilidade do pacote de aplicativos virtual com sistemas ESD (distribuição de software eletrônico), como o Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="de4c2-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="de4c2-136">Os arquivos anteriores do Windows Installer criados com a ferramenta MSI para a virtualização de aplicativos que foram instalados em um cliente App-V 4,1 ou 4,2 que, em seguida, foi atualizado para o App-V 4,5 continuarão funcionando, embora não possam ser instalados no cliente App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="de4c2-137">No entanto, eles não podem ser removidos ou atualizados, a menos que eles sejam atualizados no sequenciador do App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="de4c2-138">O pacote App-V original anterior a 4,5 precisa ser aberto no sequenciador App-V 4,5 e salvo como um arquivo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="de4c2-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="de4c2-139">Observação</span><span class="sxs-lookup"><span data-stu-id="de4c2-139">Note</span></span>**  
    <span data-ttu-id="de4c2-140">Se o cliente App-V 4,2 já tiver sido atualizado para o App-V 4,5, é possível criar um script de solução alternativa para preservar os pacotes da versão 4,2 nos clientes da versão 4,5 e permitir que eles sejam gerenciados.</span><span class="sxs-lookup"><span data-stu-id="de4c2-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="de4c2-141">Esse script deve copiar dois arquivos, msvcp71.dll e msvcr71.dll, para a pasta de instalação do App-V e definir os seguintes valores de chave do registro na chave do registro: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="de4c2-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="de4c2-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="de4c2-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="de4c2-143">"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (um local gravável globalmente)</span><span class="sxs-lookup"><span data-stu-id="de4c2-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="de4c2-144">Os arquivos do Windows Installer gerados pela App-V 4,5 Sequencer exibem a mensagem de erro "Este pacote requer o cliente do Microsoft Application Virtualization 4,5 ou posterior" ao tentar executá-los em um cliente do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="de4c2-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="de4c2-145">Abra o pacote antigo com o sequenciador do App-V 4,5 SP1 ou o sequenciador do App-V 4,6 e gere um novo arquivo. msi para o pacote.</span><span class="sxs-lookup"><span data-stu-id="de4c2-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="de4c2-146">Quaisquer relatórios da versão 4,2 que foram criados e salvos serão substituídos quando o servidor for atualizado para a versão 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="de4c2-147">Se precisar manter esses relatórios, você deve salvar uma cópia de backup do arquivo SftMMC. msc localizado na pasta do console de gerenciamento do SoftGrid no servidor e usar essa cópia para substituir o novo SftMMC. msc que é instalado durante a atualização.</span><span class="sxs-lookup"><span data-stu-id="de4c2-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="de4c2-148">Para obter informações adicionais sobre a atualização de versões anteriores, consulte [atualização para perguntas frequentes do Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="de4c2-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="de4c2-149">Suporte ao pacote cliente do App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="de4c2-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="de4c2-150">Você pode implantar pacotes criados em versões anteriores dos clientes do App-v para o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="de4c2-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="de4c2-151">No entanto, você deve modificar o arquivo. OSD associado para que ele inclua o sistema operacional apropriado e as informações sobre a arquitetura do chip.</span><span class="sxs-lookup"><span data-stu-id="de4c2-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="de4c2-152">Os seguintes valores podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="de4c2-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="de4c2-153">Valor do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="de4c2-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-154">&lt;VALOR do sistema operacional = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-155">&lt;VALOR do sistema operacional = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-156">&lt;VALOR do sistema operacional = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-157">&lt;VALOR do sistema operacional = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-158">&lt;VALOR do sistema operacional = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-159">&lt;VALOR do sistema operacional = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-160">&lt;VALOR do sistema operacional = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-161">&lt;VALOR do sistema operacional = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-162">&lt;VALOR do sistema operacional = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-163">&lt;VALOR do sistema operacional = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-164">&lt;VALOR do sistema operacional = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="de4c2-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="de4c2-165">Para executar um pacote de 32 bits recém-criado, você deve sequenciar o aplicativo em um computador que executa um sistema operacional de 32 bits com o sequenciador do App-V 4,6 instalado.</span><span class="sxs-lookup"><span data-stu-id="de4c2-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="de4c2-166">Depois de sequenciar o aplicativo, no console do sequenciador, clique na guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="de4c2-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="de4c2-167">Importante</span><span class="sxs-lookup"><span data-stu-id="de4c2-167">Important</span></span>**  
<span data-ttu-id="de4c2-168">Aplicativos sequenciados em um computador executando um sistema operacional de 64 bits devem ser implantados em computadores que executam um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="de4c2-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="de4c2-169">Os novos pacotes de 32 bits criados usando o sequenciador do App-V 4,6 não são executados em computadores que executam o cliente App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="de4c2-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="de4c2-170">Para executar novos pacotes de 64 bits no cliente do App-V 4,6, você deve sequenciar o aplicativo em um computador que executa o sequenciador do App-V 4,6 e que está executando um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="de4c2-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="de4c2-171">Depois de sequenciar o aplicativo, no console do sequenciador, clique na guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="de4c2-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="de4c2-172">A tabela a seguir lista quais versões do cliente executarão pacotes criados usando as várias versões do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="de4c2-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="de4c2-173">Sequenciado usando o sequenciador do App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="de4c2-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="de4c2-174">Sequenciado usando o sequenciador do App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="de4c2-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="de4c2-175">Sequenciado usando o sequenciador do App-V 4,6 de 32 bits</span><span class="sxs-lookup"><span data-stu-id="de4c2-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="de4c2-176">Sequenciado usando o sequenciador do App-V 4,6 de 64 bits</span><span class="sxs-lookup"><span data-stu-id="de4c2-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-177">cliente do 4,2</span><span class="sxs-lookup"><span data-stu-id="de4c2-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-178">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-179">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-180">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-181">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-182">¹ Client 4,5</span><span class="sxs-lookup"><span data-stu-id="de4c2-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-183">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-184">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-185">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-186">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="de4c2-187">cliente do 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="de4c2-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-188">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-189">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-190">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-191">Não</span><span class="sxs-lookup"><span data-stu-id="de4c2-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="de4c2-192">cliente do 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="de4c2-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-193">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-194">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-195">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="de4c2-196">Sim</span><span class="sxs-lookup"><span data-stu-id="de4c2-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="de4c2-197">o ¹ aplica-se a todas as versões do cliente App-V 4,5, incluindo o App-V 4,5, o App-V 4,5 CU1 e o App-V 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="de4c2-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









