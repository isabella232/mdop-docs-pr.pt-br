---
title: Como configurar o arquivo de log do cliente
description: Como configurar o arquivo de log do cliente
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797197"
---
# <span data-ttu-id="18323-103">Como configurar o arquivo de log do cliente</span><span class="sxs-lookup"><span data-stu-id="18323-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="18323-104">Você pode usar os procedimentos a seguir para configurar o arquivo de log do cliente do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="18323-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="18323-105">Para alterar o local do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="18323-105">To change the log file location</span></span>**

-   <span data-ttu-id="18323-106">Edite o seguinte valor da chave do registro para especificar o novo caminho para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="18323-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="18323-107">Você deve reiniciar o serviço **sftlist** após alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="18323-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="18323-108">Este local também pode ser alterado interativamente após a instalação.</span><span class="sxs-lookup"><span data-stu-id="18323-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="18323-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="18323-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="18323-110">Para alterar o nível de relatório de log</span><span class="sxs-lookup"><span data-stu-id="18323-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="18323-111">Por padrão, o tipo de mensagens gravadas no log inclui todos os eventos de severidade nível 4 (informativo) ou superior.</span><span class="sxs-lookup"><span data-stu-id="18323-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="18323-112">O nível de gravidade é armazenado no valor da chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="18323-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="18323-113">Defina esse valor de chave como 5 para habilitar o registro em log detalhado.</span><span class="sxs-lookup"><span data-stu-id="18323-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="18323-114">Use o registro em log detalhado apenas por períodos curtos durante a solução de problemas, pois ele gerará um volume muito grande de mensagens e fará com que o log seja preenchido rapidamente.</span><span class="sxs-lookup"><span data-stu-id="18323-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="18323-115">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="18323-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="18323-116">Para alterar o tamanho do log</span><span class="sxs-lookup"><span data-stu-id="18323-116">To change the log size</span></span>**

-   <span data-ttu-id="18323-117">No Application Virtualization (App-V) 4,5, o tamanho do log é controlado pelo seguinte valor da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="18323-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="18323-118">Esse valor assume o valor padrão de 256MB e define o tamanho máximo, em MB, que o log pode crescer antes de ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="18323-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="18323-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="18323-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="18323-120">**Cuidado**  Esse valor da chave do registro deve ser definido como um valor maior do que zero para garantir que o arquivo de log seja redefinido.</span><span class="sxs-lookup"><span data-stu-id="18323-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="18323-121">Para alterar o número de cópias de backup</span><span class="sxs-lookup"><span data-stu-id="18323-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="18323-122">Quando o arquivo de log atinge o tamanho máximo, uma redefinição é forçada quando ocorre a próxima gravação do log.</span><span class="sxs-lookup"><span data-stu-id="18323-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="18323-123">Uma redefinição faz com que um novo arquivo de log seja criado, e o arquivo antigo é renomeado como um backup.</span><span class="sxs-lookup"><span data-stu-id="18323-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="18323-124">A configuração do registro a seguir controla o número de cópias de backup do arquivo de log que são mantidas quando o arquivo é redefinido.</span><span class="sxs-lookup"><span data-stu-id="18323-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="18323-125">O valor padrão é 4.</span><span class="sxs-lookup"><span data-stu-id="18323-125">The default value is 4.</span></span>

    <span data-ttu-id="18323-126">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="18323-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="18323-127">O formato dos nomes dos arquivos de log de backup é: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** e é baseado no tempo de redefinição, no tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="18323-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="18323-128">A tabela a seguir lista os símbolos usados na criação dos nomes de arquivo e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="18323-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="18323-129">Símbolo</span><span class="sxs-lookup"><span data-stu-id="18323-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="18323-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="18323-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="18323-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="18323-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-132">ano de 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="18323-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="18323-133">CM</span><span class="sxs-lookup"><span data-stu-id="18323-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-134">mês de 2 dígitos (01 – 12)</span><span class="sxs-lookup"><span data-stu-id="18323-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="18323-135">MM</span><span class="sxs-lookup"><span data-stu-id="18323-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-136">2 dígitos no dia do mês (01 – 31)</span><span class="sxs-lookup"><span data-stu-id="18323-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="18323-137">hh</span><span class="sxs-lookup"><span data-stu-id="18323-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-138">hora (00 – 23)</span><span class="sxs-lookup"><span data-stu-id="18323-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="18323-139">cm</span><span class="sxs-lookup"><span data-stu-id="18323-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-140">minutos (00 a 59)</span><span class="sxs-lookup"><span data-stu-id="18323-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="18323-141">ss</span><span class="sxs-lookup"><span data-stu-id="18323-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-142">segundos (00 a 59)</span><span class="sxs-lookup"><span data-stu-id="18323-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="18323-143">uuu</span><span class="sxs-lookup"><span data-stu-id="18323-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="18323-144">milissegundos (000 – 999)</span><span class="sxs-lookup"><span data-stu-id="18323-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="18323-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18323-145">Related topics</span></span>


[<span data-ttu-id="18323-146">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="18323-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





