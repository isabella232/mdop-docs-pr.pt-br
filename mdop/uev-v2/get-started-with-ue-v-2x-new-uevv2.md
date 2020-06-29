---
title: Introdução ao UE-V 2.x
description: Introdução ao UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799242"
---
# <span data-ttu-id="54fbc-103">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="54fbc-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="54fbc-104">Siga as etapas deste guia para implantar rapidamente o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1 em um pequeno ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="54fbc-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="54fbc-105">Isso ajuda você a determinar se a UE-V é a solução certa para gerenciar as configurações de usuário em vários dispositivos na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="54fbc-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="54fbc-106">**Observação**  As informações nesta seção são repetidas com mais detalhes em todo o restante da documentação.</span><span class="sxs-lookup"><span data-stu-id="54fbc-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="54fbc-107">Portanto, se você já sabe que o UE-V 2 é a solução certa e não precisa avaliá-lo, você pode começar a [preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="54fbc-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="54fbc-108">A instalação padrão do UE-V sincroniza as configurações padrão do Microsoft Windows e do Office e muitas configurações de aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="54fbc-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="54fbc-109">Certifique-se de que seu ambiente de teste inclui dois ou mais computadores de usuário que compartilham acesso à rede e você vai avaliar o UE-V em apenas um período curto.</span><span class="sxs-lookup"><span data-stu-id="54fbc-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="54fbc-110">[Etapa 1: confirmar pré-requisitos](#step1): Certifique-se de que seu ambiente seja capaz de executar o UE-V, incluindo detalhes sobre as configurações com suporte.</span><span class="sxs-lookup"><span data-stu-id="54fbc-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="54fbc-111">[Etapa 2: implantar o local de armazenamento de configurações para UE-V 2](#step2): todas as implantações do UE-v exigem um local para pacotes de configurações que contêm os valores de configuração sincronizados.</span><span class="sxs-lookup"><span data-stu-id="54fbc-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="54fbc-112">[Etapa 3: implantar o agente do UE-V 2](#step3): para sincronizar as configurações usando o UE-v, os dispositivos devem ter o UE-v Agent instalado e em execução.</span><span class="sxs-lookup"><span data-stu-id="54fbc-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="54fbc-113">[Etapa 4: testar a implantação de avaliação do UE-V 2](#step4): execute alguns testes em dois computadores com o UE-v Agent instalado e veja como funciona o UE-v.</span><span class="sxs-lookup"><span data-stu-id="54fbc-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="54fbc-114">Isso é tudo!</span><span class="sxs-lookup"><span data-stu-id="54fbc-114">That’s it!</span></span> <span data-ttu-id="54fbc-115">Depois de seguir as etapas, você poderá avaliar como o UE-V pode funcionar na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="54fbc-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="54fbc-116">**Avaliação posterior:** Você também pode executar etapas adicionais para configurar alguns aplicativos de terceiros e de linha de negócios para sincronizar suas configurações usando o UE-V, conforme detalhado em [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="54fbc-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="54fbc-117">Etapa 1: confirmar pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="54fbc-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="54fbc-118">Antes de prosseguir, verifique se o seu ambiente inclui estes requisitos para executar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="54fbc-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="54fbc-119">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="54fbc-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54fbc-120">Edição</span><span class="sxs-lookup"><span data-stu-id="54fbc-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54fbc-121">Service Pack</span><span class="sxs-lookup"><span data-stu-id="54fbc-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54fbc-122">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="54fbc-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54fbc-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="54fbc-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="54fbc-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="54fbc-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54fbc-125">7</span><span class="sxs-lookup"><span data-stu-id="54fbc-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-126">Ultimate, Enterprise ou Professional Edition</span><span class="sxs-lookup"><span data-stu-id="54fbc-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-127">SP1</span><span class="sxs-lookup"><span data-stu-id="54fbc-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-128">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-129">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-130">.NET Framework 4 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54fbc-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="54fbc-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-132">Standard, Enterprise, Datacenter ou servidor Web</span><span class="sxs-lookup"><span data-stu-id="54fbc-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-133">SP1</span><span class="sxs-lookup"><span data-stu-id="54fbc-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-135">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-136">.NET Framework 4 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54fbc-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="54fbc-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-138">Enterprise ou pro</span><span class="sxs-lookup"><span data-stu-id="54fbc-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-139">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="54fbc-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-140">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-141">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-142">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="54fbc-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54fbc-143">Windows Server 2012 R2 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54fbc-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-144">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="54fbc-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-145">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="54fbc-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-147">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-148">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="54fbc-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54fbc-149">Windows 10, pre-1607 verison</span><span class="sxs-lookup"><span data-stu-id="54fbc-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-150">Enterprise ou pro</span><span class="sxs-lookup"><span data-stu-id="54fbc-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="54fbc-151">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-152">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-153">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="54fbc-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54fbc-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54fbc-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-155">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="54fbc-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-156">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="54fbc-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="54fbc-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-158">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="54fbc-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="54fbc-159">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="54fbc-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54fbc-160">**Observação:** A partir do Windows 10, versão 1607, o UE-V está incluído no [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e não faz mais parte do Microsoft Desktop Optimization Pack</span><span class="sxs-lookup"><span data-stu-id="54fbc-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="54fbc-161">Também...</span><span class="sxs-lookup"><span data-stu-id="54fbc-161">Also…</span></span>

-   <span data-ttu-id="54fbc-162">**Licença do MDOP:** Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="54fbc-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="54fbc-163">Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="54fbc-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="54fbc-164">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte como obter o MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="54fbc-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="54fbc-165">**Credenciais administrativas** para qualquer computador no qual você irá instalar</span><span class="sxs-lookup"><span data-stu-id="54fbc-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="54fbc-166">Etapa 2: implantar o local de armazenamento de configurações para UE-V 2</span><span class="sxs-lookup"><span data-stu-id="54fbc-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="54fbc-167">Você precisará implantar um local de armazenamento de configurações, um compartilhamento de rede padrão onde as configurações do usuário são armazenadas em um arquivo de pacote de configurações.</span><span class="sxs-lookup"><span data-stu-id="54fbc-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="54fbc-168">Ao criar o compartilhamento de armazenamento de configurações, você deve limitar o acesso aos usuários que precisam dele.</span><span class="sxs-lookup"><span data-stu-id="54fbc-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="54fbc-169">[Implantar um local de armazenamento de configurações](https://technet.microsoft.com/library/dn458891.aspx#ssl) fornece informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="54fbc-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="54fbc-170">Criar um compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="54fbc-170">Create a network share</span></span>**

1.  <span data-ttu-id="54fbc-171">Crie um novo grupo de segurança e adicione usuários do UE-V a ele.</span><span class="sxs-lookup"><span data-stu-id="54fbc-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="54fbc-172">Crie uma nova pasta no computador centralizado que armazena os pacotes de configurações do UE-V e conceda aos usuários do UE-V acesso às permissões de grupo para a pasta.</span><span class="sxs-lookup"><span data-stu-id="54fbc-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="54fbc-173">O administrador que dá suporte a UE-V deve ter permissões para esta pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="54fbc-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="54fbc-174">Atribua permissão a usuários do UE-V para criar um diretório quando eles se conectam.</span><span class="sxs-lookup"><span data-stu-id="54fbc-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="54fbc-175">Conceda permissão total a todas as subpastas desse diretório, mas bloqueie o acesso a qualquer coisa acima.</span><span class="sxs-lookup"><span data-stu-id="54fbc-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="54fbc-176">Defina as seguintes permissões de bloco de mensagens de servidor (SMB) de nível de compartilhamento para a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="54fbc-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="54fbc-177">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="54fbc-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="54fbc-178">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="54fbc-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="54fbc-179">Todos</span><span class="sxs-lookup"><span data-stu-id="54fbc-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-180">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="54fbc-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="54fbc-181">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="54fbc-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-182">Controle total</span><span class="sxs-lookup"><span data-stu-id="54fbc-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="54fbc-183">Defina as seguintes permissões do sistema de arquivos NTFS para a pasta de local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="54fbc-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="54fbc-184">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="54fbc-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="54fbc-185">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="54fbc-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="54fbc-186">Pasta</span><span class="sxs-lookup"><span data-stu-id="54fbc-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="54fbc-187">Criador/proprietário</span><span class="sxs-lookup"><span data-stu-id="54fbc-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-188">Controle total</span><span class="sxs-lookup"><span data-stu-id="54fbc-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-189">Somente subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="54fbc-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="54fbc-190">Grupo de segurança de usuários do UE-V</span><span class="sxs-lookup"><span data-stu-id="54fbc-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-191">Listar pasta/ler dados, criar pastas/acrescentar dados</span><span class="sxs-lookup"><span data-stu-id="54fbc-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="54fbc-192">Somente esta pasta</span><span class="sxs-lookup"><span data-stu-id="54fbc-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="54fbc-193">Observação de segurança:</span><span class="sxs-lookup"><span data-stu-id="54fbc-193">Security Note:</span></span>**

<span data-ttu-id="54fbc-194">Se você criar o compartilhamento de armazenamento configurações em um computador que esteja executando um sistema operacional Windows Server, configure o UE-V para verificar se o grupo Administradores local ou o usuário atual é o proprietário da pasta em que os pacotes de configurações estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="54fbc-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="54fbc-195">Para habilitar essa segurança adicional, especifique essa configuração no editor do registro do Windows Server:</span><span class="sxs-lookup"><span data-stu-id="54fbc-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="54fbc-196">Adicione uma chave do registro **reg \ _DWORD** chamada **"RepositoryOwnerCheckEnabled"** ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="54fbc-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="54fbc-197">Defina o valor da chave do registro como *1*.</span><span class="sxs-lookup"><span data-stu-id="54fbc-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="54fbc-198">Etapa 3: implantar o agente do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="54fbc-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="54fbc-199">O UE-V Agent sincroniza o aplicativo e as configurações do Windows entre os computadores e os dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="54fbc-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="54fbc-200">Para fins de avaliação, instale o agente em pelo menos dois computadores em seu ambiente de teste que pertençam ao mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="54fbc-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="54fbc-201">Execute o arquivo AgentSetup.exe a partir da linha de comando para instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="54fbc-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="54fbc-202">Ele é instalado em sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="54fbc-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="54fbc-203">Você deve especificar o parâmetro de linha de comando SettingsStoragePath como o compartilhamento de rede da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="54fbc-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="54fbc-204">[Implantar um agente do UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fornece informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="54fbc-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="54fbc-205">Etapa 4: testar a implantação de avaliação do UE-V 2</span><span class="sxs-lookup"><span data-stu-id="54fbc-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="54fbc-206">Agora você pode executar alguns testes em sua implantação de avaliação do UE-V para ver como o UE-V funciona.</span><span class="sxs-lookup"><span data-stu-id="54fbc-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="54fbc-207">No primeiro computador (computador A), faça uma ou mais destas alterações:</span><span class="sxs-lookup"><span data-stu-id="54fbc-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="54fbc-208">Abra a área de trabalho do Windows e mova a barra de tarefas para um local diferente na janela.</span><span class="sxs-lookup"><span data-stu-id="54fbc-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="54fbc-209">Alterar as fontes padrão.</span><span class="sxs-lookup"><span data-stu-id="54fbc-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="54fbc-210">Abra a calculadora e defina como **científico**.</span><span class="sxs-lookup"><span data-stu-id="54fbc-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="54fbc-211">Altere o comportamento de qualquer aplicativo do Windows, conforme detalhado no [Gerenciamento de modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="54fbc-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="54fbc-212">Desabilitar a sincronização e os perfis móveis das configurações de conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="54fbc-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="54fbc-213">Faça logoff do computador A. as configurações são salvas em um pacote de configurações do UE-V quando os usuários travam, fazem logoff, saem de um aplicativo ou quando o provedor de sincronização é executado (a cada 30 minutos por padrão).</span><span class="sxs-lookup"><span data-stu-id="54fbc-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="54fbc-214">Faça logon no segundo computador (computador B) como o mesmo usuário do computador A.</span><span class="sxs-lookup"><span data-stu-id="54fbc-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="54fbc-215">Abra a área de trabalho do Windows e verifique se o local da barra de tarefas corresponde ao do computador A. Verifique se as fontes padrão correspondem e se a calculadora está definida como **científica**.</span><span class="sxs-lookup"><span data-stu-id="54fbc-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="54fbc-216">Verifique também a alteração feita em qualquer aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="54fbc-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="54fbc-217">Você pode alterar as configurações do computador B de volta para o computador original.</span><span class="sxs-lookup"><span data-stu-id="54fbc-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="54fbc-218">Em seguida, faça logon no computador B e conecte-se ao computador A para verificar as alterações.</span><span class="sxs-lookup"><span data-stu-id="54fbc-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="54fbc-219">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="54fbc-219">Other resources for this product</span></span>


-   [<span data-ttu-id="54fbc-220">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="54fbc-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="54fbc-221">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54fbc-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="54fbc-222">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54fbc-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="54fbc-223">Solução de problemas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="54fbc-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="54fbc-224">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="54fbc-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





