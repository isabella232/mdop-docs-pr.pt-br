---
title: Administrar o MBAM 1.0 usando PowerShell
description: Administrar o MBAM 1.0 usando PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799612"
---
# <span data-ttu-id="3ca02-103">Administrar o MBAM 1.0 usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ca02-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="3ca02-104">O monitoramento e administração do Microsoft BitLocker (MBAM) fornece o conjunto de cmdlets do Windows PowerShell listados a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ca02-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="3ca02-105">Os administradores podem usar esses cmdlets do PowerShell para executar várias tarefas do MBAM Server a partir do prompt de comando, e não do site de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="3ca02-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="3ca02-106">Como administrar o MBAM usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ca02-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="3ca02-107">Use os cmdlets do PowerShell descritos aqui para administrar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="3ca02-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3ca02-108">Nome</span><span class="sxs-lookup"><span data-stu-id="3ca02-108">Name</span></span></th>
<th align="left"><span data-ttu-id="3ca02-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca02-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ca02-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="3ca02-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-111">Adiciona um novo modelo de hardware ao inventário de hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="3ca02-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="3ca02-112">Esse cmdlet também pode especificar se o hardware tem ou não suporte para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3ca02-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ca02-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="3ca02-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-114">Solicita uma chave de recuperação MBAM que permitirá que um usuário Desbloqueie um computador ou unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="3ca02-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ca02-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="3ca02-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-116">Obtém um inventário de hardware mestre que contém dados que indicam se os modelos de hardware são compatíveis ou são incompatíveis com a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3ca02-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ca02-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3ca02-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-118">Fornece uma senha de proprietário do TPM para um usuário gerenciar o acesso de TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="3ca02-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="3ca02-119">Ajuda os usuários quando o TPM os bloqueou e não aceitará mais o PIN.</span><span class="sxs-lookup"><span data-stu-id="3ca02-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ca02-120">Install-MBAM</span><span class="sxs-lookup"><span data-stu-id="3ca02-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-121">Instala os recursos do MBAM que fornecem ferramentas avançadas de política de grupo, criptografia, recuperação de chave e relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="3ca02-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ca02-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="3ca02-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-123">Remove os modelos de hardware do inventário de hardware.</span><span class="sxs-lookup"><span data-stu-id="3ca02-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ca02-124">Set-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="3ca02-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-125">Permite o gerenciamento de um inventário de hardware mestre para designar se os modelos de hardware são compatíveis ou não podem executar a criptografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3ca02-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ca02-126">Desinstalar-MBAM</span><span class="sxs-lookup"><span data-stu-id="3ca02-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ca02-127">Remove os recursos MBAM instalados anteriormente que fornecem ferramentas avançadas de política, criptografia, recuperação de chave e relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="3ca02-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3ca02-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ca02-128">Related topics</span></span>


[<span data-ttu-id="3ca02-129">Operações do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3ca02-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





