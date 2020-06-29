---
title: Referência de linha de comando para instalação do cliente
description: Referência de linha de comando para instalação do cliente
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799930"
---
# <span data-ttu-id="abda3-103">Referência de linha de comando para instalação do cliente</span><span class="sxs-lookup"><span data-stu-id="abda3-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="abda3-104">Para instalar o MED-V na linha de comando</span><span class="sxs-lookup"><span data-stu-id="abda3-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="abda3-105">Na linha de comando, execute o pacote MED-V. msi seguido de qualquer um dos parâmetros opcionais descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="abda3-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="abda3-106">O pacote MED-V. msi é chamado *MED-V\_x.msi*, em que *x* é o número da versão.</span><span class="sxs-lookup"><span data-stu-id="abda3-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="abda3-107">Por exemplo, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="abda3-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="abda3-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="abda3-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="abda3-109">Valor</span><span class="sxs-lookup"><span data-stu-id="abda3-109">Value</span></span></th>
<th align="left"><span data-ttu-id="abda3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="abda3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-111">/Quiet</span><span class="sxs-lookup"><span data-stu-id="abda3-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="abda3-112">Instalação silenciosa</span><span class="sxs-lookup"><span data-stu-id="abda3-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-113">/log &lt; caminho completo para o arquivo de log&gt;</span><span class="sxs-lookup"><span data-stu-id="abda3-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-114">O caminho completo para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="abda3-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="abda3-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-116">O caminho completo para o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="abda3-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="abda3-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-118">O caminho completo para a pasta da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abda3-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="abda3-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-120">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-120">1,0</span></span></strong></p>
<p><span data-ttu-id="abda3-121">Padrão: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="abda3-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abda3-122">Instala as ferramentas de administração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="abda3-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="abda3-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-124">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-124">1,0</span></span></strong></p>
<p><span data-ttu-id="abda3-125">Padrão: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="abda3-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abda3-126">Inicia automaticamente o cliente MED-V toda vez que o usuário faz logon no Windows.</span><span class="sxs-lookup"><span data-stu-id="abda3-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="abda3-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-128">nome do host ou IP</span><span class="sxs-lookup"><span data-stu-id="abda3-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="abda3-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-130">porta</span><span class="sxs-lookup"><span data-stu-id="abda3-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="abda3-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-132">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-132">1,0</span></span></strong></p>
<p><span data-ttu-id="abda3-133">para <strong> https </strong> ou <strong> http</span><span class="sxs-lookup"><span data-stu-id="abda3-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="abda3-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-135">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-135">1,0</span></span></strong></p>
<p><span data-ttu-id="abda3-136">Padrão: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="abda3-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abda3-137">Inicia o MED-V na conclusão da instalação do MED-V.</span><span class="sxs-lookup"><span data-stu-id="abda3-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="abda3-138">Observação</span><span class="sxs-lookup"><span data-stu-id="abda3-138">Note</span></span></strong><br/><p><span data-ttu-id="abda3-139">É recomendável definir START_MEDV = 0 em caso de caso o MED-V seja instalado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="abda3-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="abda3-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-141">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-141">1,0</span></span></strong></p>
<p><span data-ttu-id="abda3-142">Padrão: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="abda3-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abda3-143">Cria um atalho na área de trabalho, que inicia o cliente MED-V.</span><span class="sxs-lookup"><span data-stu-id="abda3-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="abda3-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="abda3-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-145">RAM em MB</span><span class="sxs-lookup"><span data-stu-id="abda3-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="abda3-146">Ao instalar o MED-V, verifica se o computador tem a quantidade mínima de RAM especificada.</span><span class="sxs-lookup"><span data-stu-id="abda3-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="abda3-147">Caso contrário, a instalação será abortada.</span><span class="sxs-lookup"><span data-stu-id="abda3-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="abda3-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="abda3-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="abda3-149">1, 0</span><span class="sxs-lookup"><span data-stu-id="abda3-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="abda3-150">Omite a validação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="abda3-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











