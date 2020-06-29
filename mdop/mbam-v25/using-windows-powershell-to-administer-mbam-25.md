---
title: Usando o Windows PowerShell para administrar o MBAM 2.5
description: Usando o Windows PowerShell para administrar o MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796074"
---
# <span data-ttu-id="22513-103">Usando o Windows PowerShell para administrar o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22513-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="22513-104">Este tópico descreve os cmdlets do Windows PowerShell para administração e monitoramento do Microsoft BitLocker (MBAM) relacionados à recuperação de computadores ou unidades quando os usuários são bloqueados.</span><span class="sxs-lookup"><span data-stu-id="22513-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="22513-105">Para cmdlets que você usa para configurar os recursos do MBAM Server, consulte [configurando recursos do MBAM do 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="22513-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="22513-106">Cmdlets para recuperar computadores ou unidades que são gerenciados pelo MBAM</span><span class="sxs-lookup"><span data-stu-id="22513-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="22513-107">Use os seguintes cmdlets do Windows PowerShell para recuperar computadores ou unidades que são gerenciados pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="22513-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22513-108">Nome</span><span class="sxs-lookup"><span data-stu-id="22513-108">Name</span></span></th>
<th align="left"><span data-ttu-id="22513-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="22513-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22513-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="22513-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="22513-111">Solicita uma chave de recuperação MBAM que permite aos usuários desbloquear um computador ou unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="22513-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22513-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="22513-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="22513-113">Fornece aos usuários uma senha de proprietário do TPM que eles podem usar para desbloquear um Trusted Platform Module (TPM) quando o TPM os bloqueou e não aceitará mais o PIN.</span><span class="sxs-lookup"><span data-stu-id="22513-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="22513-114">Ajuda do cmdlet MBAM</span><span class="sxs-lookup"><span data-stu-id="22513-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="22513-115">A ajuda do Windows PowerShell para cmdlets MBAM está disponível nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="22513-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22513-116">Formato de ajuda do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="22513-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="22513-117">Mais informações</span><span class="sxs-lookup"><span data-stu-id="22513-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22513-118">Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="22513-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22513-119">Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções em <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="22513-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22513-120">No TechNet como páginas da Web</span><span class="sxs-lookup"><span data-stu-id="22513-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22513-121">No centro de download como um arquivo. docx do Word</span><span class="sxs-lookup"><span data-stu-id="22513-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22513-122">No centro de download como um arquivo. pdf</span><span class="sxs-lookup"><span data-stu-id="22513-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="22513-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22513-123">Related topics</span></span>


[<span data-ttu-id="22513-124">Administrando os recursos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="22513-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="22513-125">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="22513-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="22513-126">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="22513-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="22513-127">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="22513-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="22513-128">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="22513-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





