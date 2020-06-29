---
title: Sobre o Microsoft Application Virtualization 4.6 SP2
description: Sobre o Microsoft Application Virtualization 4.6 SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797641"
---
# <span data-ttu-id="5caa0-103">Sobre o Microsoft Application Virtualization 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="5caa0-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="5caa0-104">O Microsoft Application Virtualization (App-V) 4.6 SP2 oferece vários aprimoramentos e novos recursos, que estão descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5caa0-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="5caa0-105">**Cuidado**  Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="5caa0-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="5caa0-106">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="5caa0-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="5caa0-107">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="5caa0-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="5caa0-108">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="5caa0-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="5caa0-109">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="5caa0-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="5caa0-110">Suporte para Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5caa0-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="5caa0-111">O App-V 4.6 SP2 adiciona suporte para serviços de área de trabalho remota do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5caa0-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="5caa0-112">Suporte para a coexistência com o cliente App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5caa0-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="5caa0-113">O App-V 4.6 SP2 oferece suporte à coexistência com o cliente do Microsoft Application Virtualization 5,0.</span><span class="sxs-lookup"><span data-stu-id="5caa0-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="5caa0-114">Examine a documentação do App-V 5,0 para obter instruções sobre como configurar o cliente do App-V 5,0 para coexistência com o cliente App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="5caa0-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="5caa0-115">Para obter mais informações sobre o App-V 5,0, consulte [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on technet.</span><span class="sxs-lookup"><span data-stu-id="5caa0-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="5caa0-116">Capacidade de virtualização do Adobe Reader X com modo protegido</span><span class="sxs-lookup"><span data-stu-id="5caa0-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="5caa0-117">Você pode virtualizar o Adobe Reader X com o recurso modo protegido ativado usando os procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5caa0-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="5caa0-118">Antes, era preciso desabilitar o modo protegido para virtualizar o Adobe Reader X.</span><span class="sxs-lookup"><span data-stu-id="5caa0-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="5caa0-119">Antes de iniciar o sequenciador do App-V, crie o seguinte valor do registro em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span><span class="sxs-lookup"><span data-stu-id="5caa0-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5caa0-120">Nome</span><span class="sxs-lookup"><span data-stu-id="5caa0-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5caa0-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-122">Dados</span><span class="sxs-lookup"><span data-stu-id="5caa0-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="5caa0-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5caa0-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="5caa0-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="5caa0-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-126">um</span><span class="sxs-lookup"><span data-stu-id="5caa0-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="5caa0-127">Defina esse valor como <strong> 1 para </strong> iniciar o Adobe Reader X no modo protegido durante a fase de início.</span><span class="sxs-lookup"><span data-stu-id="5caa0-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5caa0-128">**Observação**  Em um computador que executa um sistema operacional de 64 bits, crie o valor do registro em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span><span class="sxs-lookup"><span data-stu-id="5caa0-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="5caa0-129">Para cada arquivo OSD-em seu pacote Adobe Reader X, adicione os seguintes itens no &lt; elemento policies &gt; :</span><span class="sxs-lookup"><span data-stu-id="5caa0-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="5caa0-130">Novo parâmetro de linha de comando do sequenciador</span><span class="sxs-lookup"><span data-stu-id="5caa0-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="5caa0-131">Ao criar um acelerador de pacote (PA) por meio da GUI do sequenciador, você pode selecionar um arquivo RTF ou TXT que forneça diretrizes de empacotamento e implantação para os administradores que aplicarão o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="5caa0-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="5caa0-132">Esta funcionalidade já está disponível usando a CLI do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="5caa0-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="5caa0-133">Especifique um caminho para um arquivo RTF ou TXT que fornece diretrizes de empacotamento e implantação ao criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="5caa0-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="5caa0-134">Não é mais necessário instalar o relatório de erros do aplicativo Microsoft</span><span class="sxs-lookup"><span data-stu-id="5caa0-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="5caa0-135">Ao instalar o cliente App-V 4.6 SP2 usando o setup.msi, você não precisa mais instalar o relatório de erros do aplicativo Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="5caa0-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="5caa0-136">O App-V 4.6 SP2 agora usa o relatório de erros da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5caa0-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="5caa0-137">Para obter mais informações, consulte [como instalar o cliente App-V usando Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span><span class="sxs-lookup"><span data-stu-id="5caa0-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="5caa0-138">Feedback do cliente e pacote cumulativo de hotfix</span><span class="sxs-lookup"><span data-stu-id="5caa0-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="5caa0-139">O App-V 4.6 SP2 inclui um pacote cumulativo de correções para solucionar problemas encontrados desde a versão App-V 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="5caa0-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="5caa0-140">O App-V 4.6 SP2 contém as correções mais recentes até e incluindo o hotfix 6 do Microsoft Application Virtualization 4,6 SP1.</span><span class="sxs-lookup"><span data-stu-id="5caa0-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="5caa0-141">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5caa0-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="5caa0-142">Notas de versão do App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="5caa0-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="5caa0-143">Fornece as informações mais atualizadas sobre problemas conhecidos com o App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="5caa0-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





