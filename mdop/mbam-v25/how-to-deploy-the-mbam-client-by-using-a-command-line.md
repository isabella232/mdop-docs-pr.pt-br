---
title: Como implantar o cliente do MBAM usando uma linha de comando
description: Como implantar o cliente do MBAM usando uma linha de comando
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799482"
---
# <span data-ttu-id="a7317-103">Como implantar o cliente do MBAM usando uma linha de comando</span><span class="sxs-lookup"><span data-stu-id="a7317-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="a7317-104">Você pode usar uma linha de comando para implantar o software cliente do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="a7317-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="a7317-105">Linha de comando para implantar o software cliente do MBAM</span><span class="sxs-lookup"><span data-stu-id="a7317-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="a7317-106">Digite o seguinte comando no prompt de comando para aceitar automaticamente o contrato de licença de usuário final ao implantar o software cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7317-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="a7317-107">MBAMClientSetup.exe/acceptEula = Sim</span><span class="sxs-lookup"><span data-stu-id="a7317-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="a7317-108">**Observação**  As opções da linha de comando **/Ju** e **/JM** não são suportadas e não podem ser usadas para instalar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7317-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="a7317-109">Digite o seguinte comando no prompt de comando para extrair e instalar o MSP:</span><span class="sxs-lookup"><span data-stu-id="a7317-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="a7317-110">&lt;Caminho de/extract MBAMClientSetup.exe para extrair MSI &gt; /AcceptEula = Sim</span><span class="sxs-lookup"><span data-stu-id="a7317-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="a7317-111">Em seguida, instale o MSI silenciosamente executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a7317-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="a7317-112">msiexec/i &lt; caminho para MSI, &gt; /QB AllUsers = 1 reboot = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="a7317-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="a7317-113">**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM.</span><span class="sxs-lookup"><span data-stu-id="a7317-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="a7317-114">No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto após aceitar o EULA.</span><span class="sxs-lookup"><span data-stu-id="a7317-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="a7317-115">OPTIname \ _FOR \ _MICROSOFT \ _UPDATES = 1 opção de linha de comando</span><span class="sxs-lookup"><span data-stu-id="a7317-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="a7317-116">Opcionalmente, você pode especificar a opção de linha de comando `OPTIN_FOR_MICROSOFT_UPDATES=1` durante a instalação do software cliente para instalar automaticamente as atualizações da Microsoft em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="a7317-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="a7317-117">Especificar essa opção faz com que o Microsoft Update inicie automaticamente e procure atualizações disponíveis para instalar após a conclusão da instalação do software cliente.</span><span class="sxs-lookup"><span data-stu-id="a7317-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="a7317-118">Você pode usar essa opção de linha de comando com um dos seguintes métodos de instalação.</span><span class="sxs-lookup"><span data-stu-id="a7317-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7317-119">Instalar o software cliente do MBAM usando</span><span class="sxs-lookup"><span data-stu-id="a7317-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="a7317-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a7317-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a7317-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="a7317-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a7317-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="a7317-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a7317-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="a7317-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="a7317-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="a7317-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="a7317-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7317-125">Related topics</span></span>


[<span data-ttu-id="a7317-126">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a7317-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="a7317-127">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="a7317-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a7317-128">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a7317-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a7317-129">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a7317-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




