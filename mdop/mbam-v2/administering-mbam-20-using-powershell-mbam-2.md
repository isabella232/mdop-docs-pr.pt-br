---
title: Administrar o MBAM 2.0 usando o PowerShell
description: Administrar o MBAM 2.0 usando o PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799285"
---
# <span data-ttu-id="ca37d-103">Administrar o MBAM 2.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca37d-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="ca37d-104">O monitoramento e administração do Microsoft BitLocker (MBAM) fornece o conjunto de cmdlets do Windows PowerShell listados a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca37d-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="ca37d-105">Os administradores podem usar estes cmdlets do PowerShell para executar várias tarefas de administração e monitoramento do Microsoft BitLocker da linha de comando, em vez de no site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca37d-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="ca37d-106">Como administrar o MBAM usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca37d-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="ca37d-107">Use os cmdlets do PowerShell descritos aqui para administrar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca37d-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca37d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ca37d-108">Name</span></span></th>
<th align="left"><span data-ttu-id="ca37d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca37d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca37d-110">Install-MBAM</span><span class="sxs-lookup"><span data-stu-id="ca37d-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca37d-111">Instala os recursos do MBAM que fornecem relatórios avançados de política, criptografia, recuperação de chave e conformidade.</span><span class="sxs-lookup"><span data-stu-id="ca37d-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca37d-112">Desinstalar-MBAM</span><span class="sxs-lookup"><span data-stu-id="ca37d-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca37d-113">Remove os recursos do MBAM que fornecem ferramentas avançadas de política, criptografia, recuperação de chave e relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="ca37d-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca37d-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="ca37d-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca37d-115">Solicita uma chave de recuperação MBAM que permitirá aos usuários desbloquear um computador ou unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="ca37d-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca37d-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="ca37d-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca37d-117">Fornece aos usuários uma senha de proprietário do TPM que eles podem usar para desbloquear um Trusted Platform Module (TPM) quando o TPM os bloqueou e não aceitará mais o PIN.</span><span class="sxs-lookup"><span data-stu-id="ca37d-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ca37d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca37d-118">Related topics</span></span>


[<span data-ttu-id="ca37d-119">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ca37d-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





