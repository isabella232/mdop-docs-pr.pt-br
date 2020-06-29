---
title: Como instalar o cliente do App-V usando Setup.msi
description: Como instalar o cliente do App-V usando Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797104"
---
# <span data-ttu-id="46d66-103">Como instalar o cliente do App-V usando Setup.msi</span><span class="sxs-lookup"><span data-stu-id="46d66-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="46d66-104">Este tópico descreve como instalar o cliente App-V usando o programa setup.msi.</span><span class="sxs-lookup"><span data-stu-id="46d66-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="46d66-105">Antes de instalar o cliente App-V usando o programa setup.msi, você deve primeiro determinar se um software de pré-requisito deve ser instalado e, em seguida, deve instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="46d66-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="46d66-106">Para instalar o software de pré-requisito, consulte a seção [instalando o software de pré-requisito](#prereq-sw) deste tópico.</span><span class="sxs-lookup"><span data-stu-id="46d66-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="46d66-107">Para instalar o software cliente, confira o artigo [instalando o aplicativo App-V usando a seção de programas Setup.msi](#msi-setup) deste tópico.</span><span class="sxs-lookup"><span data-stu-id="46d66-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="46d66-108">Instalar software de pré-requisito</span><span class="sxs-lookup"><span data-stu-id="46d66-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="46d66-109">Você pode usar os procedimentos a seguir para instalar o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="46d66-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="46d66-110">Você pode criar um arquivo de comando e executar os comandos a partir do prompt de comando ou pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar os comandos.</span><span class="sxs-lookup"><span data-stu-id="46d66-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="46d66-111">**Observação**  As versões x86 do seguinte software são necessárias para as versões x86 e x64 do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="46d66-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="46d66-112">Para instalar o Microsoft VisualC + + 2005SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="46d66-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="46d66-113">Baixe o pacote de software do [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) a partir do centro de download da Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ).</span><span class="sxs-lookup"><span data-stu-id="46d66-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="46d66-114">\ [Valor de token de modelo \] da versão 4,5 SP2 e posterior do cliente App-V, baixar vcredist\_x86.exe do [pacote redistribuído do Microsoft Visual C++ 2005 Service Pack 1 atualização de segurança do ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valor de token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="46d66-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="46d66-115">Para instalar silenciosamente, use a opção de linha de comando "/Q" com vcredist\_x86.exe — por exemplo, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="46d66-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="46d66-116">Para instalar o software usando o arquivo vcredist\_x86.msi, use a opção de linha de comando "/C/T: &lt; fullpathtofolder &gt; " para extrair os arquivos vcredist.msi e vcredis1.cab de vcredist\_x86.exe para uma pasta temporária.</span><span class="sxs-lookup"><span data-stu-id="46d66-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="46d66-117">Para instalar silenciosamente, use a opção de linha de comando/quiet — por exemplo, **msiexec/i vcredist.msi** /Quiet.</span><span class="sxs-lookup"><span data-stu-id="46d66-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="46d66-118">Para instalar o Microsoft VisualC + + 2008SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="46d66-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="46d66-119">**Importante**  Para a versão 4.6 e posterior do cliente App-V, você também deve instalar a atualização de segurança ATL do pacote Microsoft Visual C++ 2008 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46d66-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="46d66-120">Baixe o pacote do software de [atualização de segurança do Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package](https://go.microsoft.com/fwlink/?LinkId=150700) do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="46d66-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="46d66-121">Para instalar silenciosamente, use a opção de linha de comando "/Q" com vcredist\_x86.exe — por exemplo, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="46d66-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="46d66-122">Para instalar o Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="46d66-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="46d66-123">Baixe o pacote de software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) a partir do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="46d66-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="46d66-124">Para instalar silenciosamente, use a opção de linha de comando/quiet — por exemplo, **msiexec/i msxml6\_x86.msi/Quiet**.</span><span class="sxs-lookup"><span data-stu-id="46d66-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="46d66-125">Para instalar o relatório de erros do aplicativo Microsoft</span><span class="sxs-lookup"><span data-stu-id="46d66-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="46d66-126">Ao instalar o relatório de erros do aplicativo Microsoft, você deve usar o parâmetro *APPGUID* para especificar o código do produto App-V.</span><span class="sxs-lookup"><span data-stu-id="46d66-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="46d66-127">O código do produto é exclusivo para cada tipo e versão do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="46d66-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="46d66-128">Selecione o código do produto correto na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46d66-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="46d66-129">**Importante**  Para o App-V 4.6 SP2 e posterior, você não precisa mais instalar o relatório de erros do aplicativo Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="46d66-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="46d66-130">O App-V agora usa o relatório de erros da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="46d66-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46d66-131">Versão</span><span class="sxs-lookup"><span data-stu-id="46d66-131">Version</span></span></th>
<th align="left"><span data-ttu-id="46d66-132">Código do produto para o cliente da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="46d66-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="46d66-133">Código de produto do cliente para serviços de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="46d66-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46d66-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="46d66-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="46d66-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="46d66-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46d66-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="46d66-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="46d66-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="46d66-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46d66-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="46d66-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="46d66-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="46d66-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46d66-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="46d66-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="46d66-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="46d66-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46d66-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="46d66-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="46d66-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="46d66-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46d66-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="46d66-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="46d66-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="46d66-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46d66-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="46d66-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="46d66-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="46d66-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46d66-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="46d66-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="46d66-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="46d66-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46d66-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="46d66-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="46d66-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="46d66-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="46d66-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="46d66-161">versão do ¹ App-V "Languages".</span><span class="sxs-lookup"><span data-stu-id="46d66-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="46d66-162">**Observação**  Se precisar localizar o código do produto, você pode usar o editor de banco de dados Orca.exe ou uma ferramenta semelhante para examinar os arquivos do Windows Installer para localizar o valor da propriedade *ProductCode* .</span><span class="sxs-lookup"><span data-stu-id="46d66-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="46d66-163">Para obter mais informações sobre como usar Orca.exe, consulte [ferramentas de desenvolvimento do Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="46d66-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="46d66-164">Localize o programa de instalação do relatório de erros do aplicativo Microsoft, dw20shared.msi, que pode ser encontrado na pasta **Support\\Watson** na mídia de lançamento.</span><span class="sxs-lookup"><span data-stu-id="46d66-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="46d66-165">Para instalar o software, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="46d66-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="46d66-166">Instalando o cliente App-V usando o programa Setup.msi</span><span class="sxs-lookup"><span data-stu-id="46d66-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="46d66-167">Use o procedimento a seguir para instalar o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="46d66-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="46d66-168">Verifique se todos os softwares de pré-requisito necessários foram instalados.</span><span class="sxs-lookup"><span data-stu-id="46d66-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="46d66-169">\ [Valor de token de modelo \] para a versão 4.6 e posterior do cliente App-V, o programa setup.msi verifica o sistema e, se o software de pré-requisito não estiver instalado, ele gerará uma mensagem de erro indicando que a instalação não pode continuar.</span><span class="sxs-lookup"><span data-stu-id="46d66-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="46d66-170">\ [Valor do token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="46d66-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="46d66-171">Para instalar o cliente do Application Virtualization usando o Setup.msi</span><span class="sxs-lookup"><span data-stu-id="46d66-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="46d66-172">Verifique se você está conectado com uma conta que tem direitos de administrador no computador.</span><span class="sxs-lookup"><span data-stu-id="46d66-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="46d66-173">Abra uma janela do prompt de comando usando direitos elevados e altere o diretório para a pasta que contém os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="46d66-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="46d66-174">Ao instalar a versão 4.6 ou posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46d66-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="46d66-175">A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.</span><span class="sxs-lookup"><span data-stu-id="46d66-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="46d66-176">Digite a cadeia de caracteres do comando instalar no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="46d66-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="46d66-177">Você também pode criar um arquivo de comando e executá-lo a partir do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="46d66-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="46d66-178">Você também pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="46d66-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="46d66-179">O exemplo de linha de comando a seguir mostra como setup.msi pode ser usado com vários parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="46d66-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="46d66-180">Para obter mais informações sobre esses parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="46d66-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="46d66-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "sistema de produção" SWIPUBSVRTYPE = "HTTP/secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "appsntype.xml/AppVirt/" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client" SWIFSDRIVE = "=" S "/q</span><span class="sxs-lookup"><span data-stu-id="46d66-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="46d66-182">Importante</span><span class="sxs-lookup"><span data-stu-id="46d66-182">Important</span></span>**  
    -   <span data-ttu-id="46d66-183">O comutador do Windows Installer "**/q**" é usado para fazer isso uma instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="46d66-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="46d66-184">Os **%** caracteres "" em "**% HomeDrive%**" devem ser precedidos pelo **^** caractere de escape "".</span><span class="sxs-lookup"><span data-stu-id="46d66-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="46d66-185">Caso contrário, o Shell de comando do Windows define o valor para aquele do usuário que está executando a instalação.</span><span class="sxs-lookup"><span data-stu-id="46d66-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="46d66-186">Para ativar o registro em log de instalação, use o msiexec switch **/l\ \* v filename. log**.</span><span class="sxs-lookup"><span data-stu-id="46d66-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="46d66-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46d66-187">Related topics</span></span>


[<span data-ttu-id="46d66-188">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="46d66-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





