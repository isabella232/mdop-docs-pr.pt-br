---
title: Valores de Registro do cliente do App-V
description: Valores de Registro do cliente do App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797599"
---
# <span data-ttu-id="9b1bf-103">Valores de Registro do cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="9b1bf-103">App-V Client Registry Values</span></span>


<span data-ttu-id="9b1bf-104">O cliente do Microsoft Application Virtualization (App-V) armazena sua configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="9b1bf-105">Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="9b1bf-106">Você também pode configurar várias ações do cliente alterando as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="9b1bf-107">Este tópico lista todas as chaves do registro do cliente do Application Virtualization (App-V) e explica seus usos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="9b1bf-108">Importante</span><span class="sxs-lookup"><span data-stu-id="9b1bf-108">Important</span></span>**  
<span data-ttu-id="9b1bf-109">Em um computador que executa um sistema operacional de 64 bits, as chaves e os valores descritos nas seções a seguir estarão em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="9b1bf-110">Chave de configuração</span><span class="sxs-lookup"><span data-stu-id="9b1bf-110">Configuration Key</span></span>


<span data-ttu-id="9b1bf-111">A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-112">Name</span></span></th>
<th align="left"><span data-ttu-id="9b1bf-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-113">Type</span></span></th>
<th align="left"><span data-ttu-id="9b1bf-114">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="9b1bf-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="9b1bf-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-117">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-118">Cliente de desktop do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9b1bf-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-119">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-120">Versão</span><span class="sxs-lookup"><span data-stu-id="9b1bf-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-121">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="9b1bf-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-123">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-124">Drivers</span><span class="sxs-lookup"><span data-stu-id="9b1bf-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-125">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="9b1bf-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-127">Se esse valor da chave estiver presente, ele conterá o nome do driver que causou um erro de parada na última vez que o núcleo foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="9b1bf-128">Depois de corrigir o erro de parada, você deve excluir esse valor de chave para que o sftlist possa começar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="9b1bf-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-130">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-131">Padrão = C:\Arquivos de Programas\microsoft Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="9b1bf-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-132">O local onde o cliente está instalado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-132">The location where the client is installed.</span></span> <span data-ttu-id="9b1bf-133">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-134">LogFilename</span><span class="sxs-lookup"><span data-stu-id="9b1bf-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-135">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-136">Padrão = CSIDL_COMMON_APPDATA a virtualização do \Microsoft\Application Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="9b1bf-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-137">O caminho e o nome do arquivo de log do cliente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="9b1bf-138">Observação</span><span class="sxs-lookup"><span data-stu-id="9b1bf-138">Note</span></span></strong><br/><p><span data-ttu-id="9b1bf-139">Se você estiver executando uma versão anterior do App-V 4,6, SP1 e modificar o nome ou o local do arquivo de log, será necessário reiniciar o serviço sftlist para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-140">LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="9b1bf-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-142">Padrão = 4, informativo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-143">Controla quais mensagens são gravadas no log.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="9b1bf-144">O valor indica um limite do que é registrado – tudo que é menor ou igual a esse valor é registrado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="9b1bf-145">Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="9b1bf-146">Intervalo de valores: 0x0 = nenhum, 0x1 = crítica, 0x2 = erro, 0x3 = aviso, 0x4 = informações (padrão), 0x5 = Verbose.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="9b1bf-147">O nível de log é configurável do console do cliente do Application Virtualization (App-V) e do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="9b1bf-148">Em um prompt de comando, o comando sftlist.exe/verboselog irá aumentar o nível de log para Verbose.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="9b1bf-149">Para obter mais informações sobre os detalhes da linha de comando, consulte</span><span class="sxs-lookup"><span data-stu-id="9b1bf-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="9b1bf-150">.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="9b1bf-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-153">Padrão = 4</span><span class="sxs-lookup"><span data-stu-id="9b1bf-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-154">Define o número de cópias de backup do arquivo de log que são mantidas quando ele é redefinido.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="9b1bf-155">O intervalo válido é de 0 a 9999.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-155">The valid range is 0–9999.</span></span> <span data-ttu-id="9b1bf-156">O padrão é 4.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-156">The default is 4.</span></span> <span data-ttu-id="9b1bf-157">Um valor 0 significa que nenhuma cópia será mantida.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-158">LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="9b1bf-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-160">Padrão = 256</span><span class="sxs-lookup"><span data-stu-id="9b1bf-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-161">Define o tamanho máximo em megabytes (MB) que o arquivo de log pode aumentar antes de ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="9b1bf-162">O tamanho padrão é de 256 MB.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-162">The default size is 256 MB.</span></span> <span data-ttu-id="9b1bf-163">Quando esse tamanho for atingido, uma redefinição de log será forçada na próxima tentativa de gravação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="9b1bf-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-166">Padrão = 0x4 (App-V 4,5)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="9b1bf-167">Padrão = 0x3 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-168">Indica o nível de log no qual as mensagens de log são gravadas no log de eventos do NT.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="9b1bf-169">O valor indica um limite do que é registrado, ou seja, tudo é igual a ou menor que o valor é registrado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="9b1bf-170">Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="9b1bf-171">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="9b1bf-171">Value Range</span></span></p>
<p><span data-ttu-id="9b1bf-172">0x0 = nenhum</span><span class="sxs-lookup"><span data-stu-id="9b1bf-172">0x0 = None</span></span></p>
<p><span data-ttu-id="9b1bf-173">0x1 = crítica</span><span class="sxs-lookup"><span data-stu-id="9b1bf-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="9b1bf-174">0x2 = erro</span><span class="sxs-lookup"><span data-stu-id="9b1bf-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="9b1bf-175">0x3 = aviso</span><span class="sxs-lookup"><span data-stu-id="9b1bf-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="9b1bf-176">0x4 = informações (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="9b1bf-177">0x5 = Verbose</span><span class="sxs-lookup"><span data-stu-id="9b1bf-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="9b1bf-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-180">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-181">Indica se o streaming do arquivo será habilitado independentemente de como o cliente foi configurado com o parâmetro APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="9b1bf-182">Se definido como FALSE, o transporte não habilitará o streaming de arquivos, mesmo que o parâmetro OSD HREF ou APPLICATIONSOURCEROOT contenha um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="9b1bf-183">0x0 = falso (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="9b1bf-184">0x1 = verdadeiro</span><span class="sxs-lookup"><span data-stu-id="9b1bf-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9b1bf-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-186">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="9b1bf-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="9b1bf-188">arquivo://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="9b1bf-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="9b1bf-189">arquivo://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="9b1bf-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-190">Habilita um administrador ou um sistema ESD (Electronic Software Distribution) para garantir que o carregamento do aplicativo seja executado de acordo com o esquema de gerenciamento de topologia.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="9b1bf-191">Use esse valor de chave para substituir a base de código do OSD do elemento HREF (por exemplo, o local de origem) de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="9b1bf-192">A raiz de origem do aplicativo suporta URLs e formatos de caminho UNC (Convenção Universal de nomenclatura).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="9b1bf-193">O formato correto para o caminho da URL é protocolo: URL do pedido: [porta] [/Path] [/], em que a porta e o caminho são opcionais.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="9b1bf-194">Se uma porta não for especificada, a porta padrão para o protocolo será usada.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="9b1bf-195">Somente a porção Protocol://Server: Port da URL OSD é substituída.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="9b1bf-196">O formato correto para o caminho UNC é \computername\sharefolder [pasta] [], em que a pasta é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="9b1bf-197">O nome do computador pode ser um FQDN (nome de domínio totalmente qualificado) ou um endereço IP, e ShareFolder pode ser uma letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="9b1bf-198">Somente a parte \computername\sharefolder ou letra da unidade do caminho OSD é substituída.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9b1bf-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-200">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="9b1bf-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="9b1bf-202">\computername\content</span><span class="sxs-lookup"><span data-stu-id="9b1bf-202">\computername\content</span></span></p>
<p><span data-ttu-id="9b1bf-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="9b1bf-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-204">Permite que um administrador especifique um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo sequenciado durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="9b1bf-205">Formatos aceitáveis para o OSDSourceRoot incluem caminhos e URLs UNC (http ou HTTPS).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="9b1bf-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-207">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="9b1bf-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="9b1bf-209">\computername\content</span><span class="sxs-lookup"><span data-stu-id="9b1bf-209">\computername\content</span></span></p>
<p><span data-ttu-id="9b1bf-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="9b1bf-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-211">Permite que um administrador especifique um local de origem para a recuperação de arquivo de ícone para um pacote de aplicativo sequenciado durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="9b1bf-212">Formatos aceitáveis para o IconSourceRoot incluem caminhos e URLs UNC (http ou HTTPS).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="9b1bf-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-215">Padrão = 5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-216">AutoLoad é um parâmetro de configuração da política de tempo de execução do cliente que permite que o bloco de recursos secundário de um aplicativo virtualizado seja transmitido para o cliente automaticamente em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="9b1bf-217">Os gatilhos AutoLoad são sinalizadores para indicar eventos que iniciam o carregamento automático de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="9b1bf-218">AutoLoad usa implicitamente o streaming em segundo plano para permitir que o aplicativo seja totalmente carregado no cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="9b1bf-219">O bloco de recursos principal será carregado primeiro, e os blocos de recursos restantes serão carregados em segundo plano para permitir operações em primeiro plano, como interação do usuário com aplicativos, para ocorrer e fornecer desempenho percebido otimizado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="9b1bf-220">Valores de máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="9b1bf-221">(0) nunca: não há bits definidos (valor é 0), nenhum carregamento automático será executado porque não há gatilhos definidos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="9b1bf-222">(1) OnLaunch: o carregamento será iniciado quando um usuário iniciar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="9b1bf-223">(2) OnRefresh: o carregamento será iniciado quando o aplicativo for publicado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="9b1bf-224">Isso ocorre sempre que o registro do pacote é adicionado ou atualizado, por exemplo, quando ocorre uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="9b1bf-225">(4) OnLogin: o carregamento começa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="9b1bf-226">(5) OnLaunch e OnLogin: default.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="9b1bf-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-229">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-230">Indica o que será carregado automaticamente quando um determinado disparador de autocarregamento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="9b1bf-231">Valores de máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="9b1bf-232">(0) nenhum: não é possível carregar automaticamente, independentemente de quais gatilhos podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="9b1bf-233">(1) PreviouslyUsed (padrão): se qualquer gatilho de AutoLoad estiver habilitado, carregue somente os pacotes nos quais pelo menos um aplicativo do pacote tenha sido usado anteriormente, ou seja, iniciado ou previamente armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="9b1bf-234">(2) All: se qualquer gatilho de AutoLoad estiver habilitado, todos os aplicativos no pacote (por pacote) ou todos os pacotes (definidos para o cliente) serão carregados automaticamente, independentemente de terem sido iniciados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="9b1bf-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-237">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-238">Indica que a autorização sempre é necessária, seja ou não um aplicativo que já esteja em cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="9b1bf-239">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-239">Possible values:</span></span></p>
<p><span data-ttu-id="9b1bf-240">0 = falso: sempre tente se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="9b1bf-241">Se não for possível estabelecer uma conexão com o servidor, o cliente ainda permite que o usuário inicie um aplicativo que tenha sido carregado anteriormente no cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="9b1bf-242">1 = verdadeiro (padrão): o aplicativo sempre deve ser autorizado na inicialização.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="9b1bf-243">Para aplicativos de fluxo RTSP, o token de autorização do usuário é enviado ao servidor para autorização.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="9b1bf-244">Para aplicativos baseados em arquivos, as ACLs de arquivo controlam se um usuário pode acessar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="9b1bf-245">Reinicie o serviço sftlist para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="9b1bf-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-247">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-248">AppData</span><span class="sxs-lookup"><span data-stu-id="9b1bf-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-249">Local onde o cache de ícone e as configurações de usuário são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="9b1bf-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-251">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="9b1bf-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-253">Diretório a ser usado para dados global App-V, incluindo caches de arquivos OSD, arquivos de ícone, informações de atalho e recursos de SystemGuard, como arquivos. ini.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="9b1bf-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-256">0 ou 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-257">Padrão = 0: um valor de 0 significa que o cliente tenta capturar exceções de programa internas para que outros aplicativos do usuário possam recuperar e continuar quando ocorrer uma falha.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="9b1bf-258">Um valor 1 significa que o cliente permite que as exceções de programa internas ocorram para que possam ser capturadas em um depurador.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-261">60</span><span class="sxs-lookup"><span data-stu-id="9b1bf-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-262">Tempo limite em segundos para solicitações de IPC internas entre núcleo e front-end.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="9b1bf-263">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="9b1bf-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-266">254</span><span class="sxs-lookup"><span data-stu-id="9b1bf-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-267">Esse valor é usado para indicar quanto tempo após ter sido iniciado que um programa pode desligar e não gerar nenhuma mensagem de erro quando outro aplicativo no mesmo pacote estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-270">Padrão = 60000</span><span class="sxs-lookup"><span data-stu-id="9b1bf-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-271">Define por quanto tempo em milissegundos o cliente esperará à medida que tenta serializar o programa começa no mesmo pacote.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="9b1bf-272">Se o cliente expirar, o programa será iniciado, mas não será serializado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-275">300</span><span class="sxs-lookup"><span data-stu-id="9b1bf-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-276">Tempo limite padrão em segundos para scripts no arquivo OSD se WAIT = TRUE.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="9b1bf-277">Você pode especificar o tempo limite de cada script com o tempo limite em vez de AGUARDAr.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="9b1bf-278">Um valor 0 significa que não há espera, e 0xFFFFFFFF significa esperar para sempre.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="9b1bf-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-280">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-281">Se, em HKLM ou HKCU, esse valor contiver um caminho válido para um arquivo de log, o SFTTray será gravado nesse log quando os programas iniciarem, desligar, falham ao iniciar e entrarem ou saírem do modo desconectado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="9b1bf-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-284">0x1A (26) erros de início de log e atividades de entrada e saída no modo desconectado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="9b1bf-285">0x1F (31) registra tudo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="9b1bf-286">0x0 (0) registra nada.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-287">Especifica quais são os cinco eventos registrados (valores de bitmask):</span><span class="sxs-lookup"><span data-stu-id="9b1bf-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="9b1bf-288">1 para o programa é iniciado</span><span class="sxs-lookup"><span data-stu-id="9b1bf-288">1 for program starts</span></span></p>
<p><span data-ttu-id="9b1bf-289">2 para erros de falha na inicialização</span><span class="sxs-lookup"><span data-stu-id="9b1bf-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="9b1bf-290">4 para desligamentos</span><span class="sxs-lookup"><span data-stu-id="9b1bf-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="9b1bf-291">8 para entrar no modo desconectado</span><span class="sxs-lookup"><span data-stu-id="9b1bf-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="9b1bf-292">16 para sair do modo desconectado para se reconectar a um servidor</span><span class="sxs-lookup"><span data-stu-id="9b1bf-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="9b1bf-293">Adicione qualquer combinação desses números para ativar as respectivas mensagens.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="9b1bf-294">O padrão é 0x1F, se não estiver no registro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-297">Padrão = 3000</span><span class="sxs-lookup"><span data-stu-id="9b1bf-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-298">Especifica em milissegundos quanto tempo a bandeja esperará ao tentar gravar no log de lançamento de lançamento se outro processo estiver usando.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="9b1bf-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-300">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-301">d:\files; C:\Documents and settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="9b1bf-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-302">Uma lista delimitada por ponto-e-vírgula com até cinco pastas para pesquisar arquivos SFT portáteis antes de solicitar que o usuário selecione um diretório.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="9b1bf-303">A barra invertida no caminho é opcional.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="9b1bf-304">Esse valor não está presente por padrão e deve ser definido manualmente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="9b1bf-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-306">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="9b1bf-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-308">Válido somente em HKCU.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-308">Valid only under HKCU.</span></span> <span data-ttu-id="9b1bf-309">O último local para o qual o usuário navegou durante a localização de um arquivo SFT para a importação de pacote.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="9b1bf-310">Definido automaticamente se o SFT for encontrado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="9b1bf-311">Isso é usado em importações sucessivas ao tentar localizar arquivos SFT automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-312">Chave compartilhada</span><span class="sxs-lookup"><span data-stu-id="9b1bf-312">Shared Key</span></span>


<span data-ttu-id="9b1bf-313">A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controla os valores compartilhados entre componentes do App-V.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="9b1bf-314">A tabela a seguir fornece informações sobre os valores do registro associados à chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-315">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-317">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-318">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-319">DumpPath</span><span class="sxs-lookup"><span data-stu-id="9b1bf-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-320">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-321">Padrão = C:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-322">Caminho padrão para criar arquivos de despejo ao gerar um minidespejo em uma exceção.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="9b1bf-323">Usa como padrão C:\ Se não especificado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="9b1bf-324">O instalador do cliente define essa chave para o &lt; diretório de dados globais do App Virtualization &gt; \Dumps.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="9b1bf-325">O instalador do sequenciador define essa chave para o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-326">DumpPathSizeLimit</span><span class="sxs-lookup"><span data-stu-id="9b1bf-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-328">1000</span><span class="sxs-lookup"><span data-stu-id="9b1bf-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-329">Especifica a quantidade total máxima de espaço em disco em megabytes que pode ser usada para armazenar minidespejos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="9b1bf-330">Padrão = 1000 MB.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-331">Chave de rede</span><span class="sxs-lookup"><span data-stu-id="9b1bf-331">Network Key</span></span>


<span data-ttu-id="9b1bf-332">A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controla uma variedade de parâmetros relacionados à rede.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="9b1bf-333">Essa chave é usada principalmente pelo agente de transporte de rede.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="9b1bf-334">A tabela a seguir fornece informações sobre os valores do registro associados à chave de rede.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-335">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-336">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-337">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-338">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-339">Online</span><span class="sxs-lookup"><span data-stu-id="9b1bf-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-341">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-342">Habilita ou desabilita o modo offline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-342">Enables or disables offline mode.</span></span> <span data-ttu-id="9b1bf-343">Se definido como 0, o cliente não se comunicará com os servidores de gerenciamento do App-V ou servidores de publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="9b1bf-344">Em operações desconectadas, o cliente pode iniciar um aplicativo carregado mesmo quando não estiver conectado a um servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="9b1bf-345">No modo offline, o cliente não tenta se conectar a um servidor de gerenciamento do App-V ou ao servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="9b1bf-346">Você deve permitir que operações desconectadas possam funcionar offline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="9b1bf-347">O valor padrão é 1 habilitado (online) e 0 está desabilitado (offline).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="9b1bf-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-350">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-351">Habilita ou desabilita a operação desconectada.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="9b1bf-352">O valor padrão é 1 habilitado e 0 está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="9b1bf-353">Quando operações desconectadas estão habilitadas, o cliente App-V pode iniciar um aplicativo carregado mesmo quando não estiver conectado a um servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-356">Padrão = 1000</span><span class="sxs-lookup"><span data-stu-id="9b1bf-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-357">Esse valor especifica o tempo limite de conexão TCP em milissegundos para determinar quando acessar o modo de operações desconectadas.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="9b1bf-358">Esse valor pode ser usado para substituir o ConnectTimeout padrão de 20 segundos (App-V Connect time out para transações de rede) ou o tempo limite TCP do sistema de aproximadamente 25 segundos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="9b1bf-359">Isso leva o cliente para o modo de operações desconectadas rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="9b1bf-360">Aplicado à próxima conexão.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="9b1bf-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-363">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-364">Aplicável somente se AllowDisconnectedOperation for 1, habilitado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="9b1bf-365">Esse valor determina se haverá um limite de tempo para o tempo que o cliente terá permissão para operar em operações desconectadas.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="9b1bf-366">1 = limitado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-366">1=limited.</span></span> <span data-ttu-id="9b1bf-367">0 = ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="9b1bf-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-370">Padrão = 129600</span><span class="sxs-lookup"><span data-stu-id="9b1bf-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-371">Indica por quantos minutos um aplicativo pode ser usado no modo de operação desconectado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-372">Os valores válidos são 1 – 999999 em dias expressos em minutos (1 – 1439998560 minutos).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="9b1bf-373">O valor padrão é 90 dias ou 129.600 minutos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-374">Protocolo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-376">Padrão = 8</span><span class="sxs-lookup"><span data-stu-id="9b1bf-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-377">Protocolo padrão a ser usado (TCP versus SSL).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="9b1bf-378">Configurar na caixa de diálogo opções.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-381">cedido</span><span class="sxs-lookup"><span data-stu-id="9b1bf-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-382">Leia o tempo limite para transações de rede em segundos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="9b1bf-383">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-386">cedido</span><span class="sxs-lookup"><span data-stu-id="9b1bf-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-387">Tempo limite de gravação para transações de rede em segundos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="9b1bf-388">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="9b1bf-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-391">cedido</span><span class="sxs-lookup"><span data-stu-id="9b1bf-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-392">Tempo limite de conexão para transações de rede em segundos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="9b1bf-393">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="9b1bf-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-396">3D</span><span class="sxs-lookup"><span data-stu-id="9b1bf-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-397">O número de vezes para tentar restabelecer uma sessão interrompida.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="9b1bf-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-400">15</span><span class="sxs-lookup"><span data-stu-id="9b1bf-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-401">O número de segundos de espera entre as tentativas para restabelecer uma sessão interrompida.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-402">Tecla http</span><span class="sxs-lookup"><span data-stu-id="9b1bf-402">Http Key</span></span>


<span data-ttu-id="9b1bf-403">A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controla os parâmetros relacionados ao streaming http.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="9b1bf-404">Essa chave é usada principalmente pelo agente de transporte de rede.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="9b1bf-405">A tabela a seguir fornece informações sobre os valores do registro associados à tecla http.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-406">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-407">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-408">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-409">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="9b1bf-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-412">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-413">Controla o comportamento do streaming HTTP quando uma conexão com o servidor HTTP pode ser estabelecida e o arquivo de pacote não existe mais no servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="9b1bf-414">Se o valor não existir ou se não for definido como 1, o cliente App-V não permitirá que você inicie um aplicativo que tenha sido carregado anteriormente no cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-415">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-416">Se esse valor for definido como 1, o cliente App-V permitirá que você inicie um aplicativo que tenha sido carregado anteriormente no cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-417">Chave do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="9b1bf-417">File System Key</span></span>


<span data-ttu-id="9b1bf-418">Os valores contidos na chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controlam os parâmetros do sistema de arquivos para App-V.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="9b1bf-419">A tabela a seguir fornece informações sobre os valores do registro associados à chave AppFS.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-420">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-421">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-422">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-423">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="9b1bf-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-426">4096</span><span class="sxs-lookup"><span data-stu-id="9b1bf-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-427">Tamanho máximo em megabytes do arquivo de cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="9b1bf-428">Se você alterar esse valor no registro, deverá definir o estado como 0 e reinicializar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-429">FileName</span><span class="sxs-lookup"><span data-stu-id="9b1bf-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-430">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="9b1bf-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-432">Local do arquivo de cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-432">Location of file system cache file.</span></span> <span data-ttu-id="9b1bf-433">Se você alterar esse valor no registro, deverá deixar o tamanho do registro igual e reinicializar ou definir o estado como 0 e reiniciar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-434">DriveLetter</span><span class="sxs-lookup"><span data-stu-id="9b1bf-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-435">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-436">P:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-437">Unidade onde o sistema de arquivos App-V será montado, se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="9b1bf-438">Esse valor é definido pelo ouvinte ou pelo instalador, e ele é lido pelo sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-439">Estado</span><span class="sxs-lookup"><span data-stu-id="9b1bf-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-441">0x100</span><span class="sxs-lookup"><span data-stu-id="9b1bf-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-442">Estado do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-442">State of file system.</span></span> <span data-ttu-id="9b1bf-443">Definido como 0 e reinicializar para limpar completamente o cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="9b1bf-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-445">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="9b1bf-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-447">Caminho para symlinks, definido em HKCU.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="9b1bf-448">Não modifique (use o diretório de dados em configuração para alterar).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="9b1bf-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-450">String</span><span class="sxs-lookup"><span data-stu-id="9b1bf-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-451">Armazenamento Client\AppFS C:\Users\Public\Documents\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="9b1bf-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-452">Caminho para dados do sistema de arquivos globais.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-452">Path for global file system data.</span></span> <span data-ttu-id="9b1bf-453">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="9b1bf-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-456">Padrão = 90</span><span class="sxs-lookup"><span data-stu-id="9b1bf-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-457">Especifica a porcentagem máxima do arquivo de cache do sistema de arquivos que pode ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="9b1bf-458">Não modifique.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="9b1bf-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-461">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-462">O recurso gerenciamento de espaço em cache do sistema de arquivos usa um algoritmo menos recentemente usado (LRU) e é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="9b1bf-463">Se o espaço necessário para um novo pacote exceder o espaço livre disponível no cache, o cliente App-V usará esse recurso para determinar quais pacotes existentes, que podem ser excluídos do cache, podem ser excluídos do cache para liberar espaço para o novo pacote.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="9b1bf-464">O cliente exclui o pacote com a data mais recente acessada se for anterior ao valor especificado no valor do registro MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="9b1bf-465">Os valores são 0 (desabilitados) e 1 (padrão, habilitado).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="9b1bf-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-468">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-469">Para determinar quando o pacote pode ser selecionado para descarte, defina esse valor do registro como igual ao número mínimo de dias que você deseja que decorra desde o último pacote ter sido acessado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="9b1bf-470">Os pacotes que foram usados mais recentemente não são descartados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-471">Chave de permissões</span><span class="sxs-lookup"><span data-stu-id="9b1bf-471">Permissions Key</span></span>


<span data-ttu-id="9b1bf-472">Para ajudar a evitar erros, os administradores podem usar a chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions para controlar o acesso a algumas ações para usuários não administrativos, por exemplo, para impedir que os usuários descarreguem acidentalmente programas.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="9b1bf-473">Os usuários com direitos administrativos podem dar a si qualquer uma dessas permissões.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="9b1bf-474">Em sistemas compartilhados, como um sistema de host de sessão de área de trabalho remota (host de sessão de RD) (antigo Terminal Server), tenha cuidado ao conceder permissões adicionais a usuários, pois algumas dessas permissões permitem que os usuários controlem os aplicativos usados por todos os usuários do sistema.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="9b1bf-475">Os valores possíveis para essas configurações são 1 (Allow) e 0 (não permite).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="9b1bf-476">As configurações da chave Permissions controlam todas as interfaces que permitem as ações nomeadas.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="9b1bf-477">Isso inclui a caixa de diálogo opções, SFTTray e SFTMime.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="9b1bf-478">Essas configurações não afetam os administradores.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-478">These settings do not affect administrators.</span></span> <span data-ttu-id="9b1bf-479">A tabela a seguir fornece informações sobre os valores do registro associados à chave de permissões.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="9b1bf-480">Dados de tipo de nome (exemplos) Descrição ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="9b1bf-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="9b1bf-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-481">DWORD</span></span>

<span data-ttu-id="9b1bf-482">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-482">Default=0</span></span>

<span data-ttu-id="9b1bf-483">Um valor de 1 permite que os usuários selecionem uma letra de unidade diferente para ser usada como unidade do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="9b1bf-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="9b1bf-484">ChangeCacheSize</span></span>

<span data-ttu-id="9b1bf-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-485">DWORD</span></span>

<span data-ttu-id="9b1bf-486">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-486">Default=0</span></span>

<span data-ttu-id="9b1bf-487">Um valor de 1 permite que os usuários alterem o tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="9b1bf-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="9b1bf-488">ChangeLogSettings</span></span>

<span data-ttu-id="9b1bf-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-489">DWORD</span></span>

<span data-ttu-id="9b1bf-490">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-490">Default=0</span></span>

<span data-ttu-id="9b1bf-491">Um valor 1 permite aos usuários modificar o nível de log, alterar sua localização e redefini-lo por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="9b1bf-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-492">AddApp</span></span>

<span data-ttu-id="9b1bf-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-493">DWORD</span></span>

<span data-ttu-id="9b1bf-494">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-494">Default=0</span></span>

<span data-ttu-id="9b1bf-495">Um valor 1 permite que os usuários adicionem aplicativos explicitamente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="9b1bf-496">Isso não afeta os aplicativos que são adicionados por meio da atualização de publicação nem impede os usuários de iniciar (e, portanto, adicionar implicitamente) aplicativos que ainda não foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="9b1bf-497">Valores são 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-497">Values are 0 or 1.</span></span>

<span data-ttu-id="9b1bf-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-498">LoadApp</span></span> 

<span data-ttu-id="9b1bf-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-499">DWORD</span></span> 

<span data-ttu-id="9b1bf-500">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-500">0</span></span>

<span data-ttu-id="9b1bf-501">Não permite que um usuário carregue um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="9b1bf-502">Esse é o padrão para os hosts da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="9b1bf-503">Se você for um usuário móvel, talvez queira carregar completamente seus aplicativos no cache para usá-los durante a operação desconectada ou o modo offline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="9b1bf-504">Para transmitir aplicativos do servidor de gerenciamento do App-V ou do App-V Streaming Server, você deve estar conectado a um servidor para carregar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="9b1bf-505">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-505">1</span></span>

<span data-ttu-id="9b1bf-506">Permite que um usuário carregue um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-506">Allows a user to load an application.</span></span> <span data-ttu-id="9b1bf-507">Este é o padrão para áreas de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="9b1bf-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-508">UnloadApp</span></span> 

<span data-ttu-id="9b1bf-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-509">DWORD</span></span> 

<span data-ttu-id="9b1bf-510">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-510">0</span></span>

<span data-ttu-id="9b1bf-511">Não permite que um usuário descarregue um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="9b1bf-512">Quando você carrega ou descarrega um pacote, todos os aplicativos no pacote são carregados em ou removidos do cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="9b1bf-513">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-513">1</span></span>

<span data-ttu-id="9b1bf-514">Permite que um usuário descarregue um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="9b1bf-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-515">LockApp</span></span> 

<span data-ttu-id="9b1bf-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-516">DWORD</span></span> 

<span data-ttu-id="9b1bf-517">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-517">0</span></span>

<span data-ttu-id="9b1bf-518">Não permite que um usuário bloqueie e desbloqueie um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="9b1bf-519">Esse é o padrão para os hosts da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="9b1bf-520">Um aplicativo bloqueado não pode ser removido do cache para criar espaço para novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="9b1bf-521">Para remover um aplicativo bloqueado do cache da área de trabalho do App-V ou do cliente para serviços de área de trabalho remota (anteriormente Terminal Services), você deve desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="9b1bf-522">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-522">1</span></span>

<span data-ttu-id="9b1bf-523">Permite que um usuário bloqueie e desbloqueie um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="9b1bf-524">Este é o padrão para áreas de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="9b1bf-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="9b1bf-525">ManageTypes</span></span> 

<span data-ttu-id="9b1bf-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-526">DWORD</span></span> 

<span data-ttu-id="9b1bf-527">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-527">0</span></span>

<span data-ttu-id="9b1bf-528">Não permite que um usuário adicione, edite ou remova associações de tipo de arquivo para aquele usuário sozinha.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="9b1bf-529">Esse é o padrão para os hosts da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="9b1bf-530">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-530">1</span></span>

<span data-ttu-id="9b1bf-531">Permite que um usuário adicione, edite e remova associações de tipo de arquivo somente para esse usuário e não globalmente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="9b1bf-532">Este é o padrão para áreas de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="9b1bf-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="9b1bf-533">RefreshServer</span></span> 

<span data-ttu-id="9b1bf-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-534">DWORD</span></span> 

<span data-ttu-id="9b1bf-535">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-535">0</span></span>

<span data-ttu-id="9b1bf-536">Não permite que um usuário Acione uma atualização de configurações MIME.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="9b1bf-537">Esse é o padrão para os hosts da sessão da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="9b1bf-538">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-538">1</span></span>

<span data-ttu-id="9b1bf-539">Permite que um usuário Acione uma atualização de configurações MIME.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="9b1bf-540">Este é o padrão para áreas de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="9b1bf-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="9b1bf-541">UpdateOSDFile</span></span>

<span data-ttu-id="9b1bf-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-542">DWORD</span></span>

<span data-ttu-id="9b1bf-543">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-543">Default= 0</span></span>

<span data-ttu-id="9b1bf-544">Um valor de 1 permite que um usuário use um arquivo OSD modificado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="9b1bf-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-545">ImportApp</span></span> 

<span data-ttu-id="9b1bf-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-546">DWORD</span></span> 

<span data-ttu-id="9b1bf-547">0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-547">0</span></span>

<span data-ttu-id="9b1bf-548">Não permite que um usuário importe aplicativos para o cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="9b1bf-549">A diferença entre Load e Import é que, quando uma carga é disparada, o cliente obtém o pacote do local configurado atualmente contido na URL OSD, ASR ou override.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="9b1bf-550">Ao usar a importação, um local para obter o pacote deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="9b1bf-551">um</span><span class="sxs-lookup"><span data-stu-id="9b1bf-551">1</span></span>

<span data-ttu-id="9b1bf-552">Permite que um usuário importe aplicativos para o cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="9b1bf-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="9b1bf-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="9b1bf-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-554">DWORD</span></span>

<span data-ttu-id="9b1bf-555">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-555">Default=0</span></span>

<span data-ttu-id="9b1bf-556">Um valor de 1 permite que os usuários modifiquem as configurações de atualização para os servidores (atualizar ao fazer logon e atualização periódica).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="9b1bf-557">Isso não significa que o usuário pode modificar outras configurações do servidor (caminho, host e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="9b1bf-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="9b1bf-558">ManageServers</span></span>

<span data-ttu-id="9b1bf-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-559">DWORD</span></span>

<span data-ttu-id="9b1bf-560">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-560">Default=0</span></span>

<span data-ttu-id="9b1bf-561">Um valor 1 permite que o usuário adicione, edite e remova servidores, exceto para editar as configurações de atualização, que são controladas pela permissão ChangeRefreshSettings.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="9b1bf-562">PublishShortcut</span><span class="sxs-lookup"><span data-stu-id="9b1bf-562">PublishShortcut</span></span>

<span data-ttu-id="9b1bf-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-563">DWORD</span></span>

<span data-ttu-id="9b1bf-564">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-564">Default=0</span></span>

<span data-ttu-id="9b1bf-565">Um valor 1 permite que os usuários publiquem atalhos por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="9b1bf-566">Isso não afeta os atalhos que são publicados durante uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="9b1bf-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="9b1bf-567">ViewAllApplications</span></span>

<span data-ttu-id="9b1bf-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-568">DWORD</span></span>

<span data-ttu-id="9b1bf-569">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-569">Default=0</span></span>

<span data-ttu-id="9b1bf-570">Um valor 1 exibe todos os aplicativos por meio da interface do usuário; caso contrário, somente os aplicativos do usuário são exibidos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="9b1bf-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-571">RepairApp</span></span>

<span data-ttu-id="9b1bf-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-572">DWORD</span></span>

<span data-ttu-id="9b1bf-573">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-573">Default=1</span></span>

<span data-ttu-id="9b1bf-574">Um valor de 1 permite que o usuário use a ação de reparo em aplicativos no SFTMime ou no console de gerenciamento de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="9b1bf-575">Ao reparar um aplicativo, você remove qualquer configuração de usuário personalizada e restaura as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="9b1bf-576">Essa ação não altera ou exclui atalhos ou associações de tipo de arquivo, e não remove o aplicativo do cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="9b1bf-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-577">ClearApp</span></span>

<span data-ttu-id="9b1bf-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-578">DWORD</span></span>

<span data-ttu-id="9b1bf-579">Padrão = 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-579">Default=1</span></span>

<span data-ttu-id="9b1bf-580">Um valor 1 permite que o usuário use a ação limpar em aplicativos no SFTMime ou o console de gerenciamento de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="9b1bf-581">Ao limpar um aplicativo do console, você não pode mais usar esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="9b1bf-582">No entanto, o aplicativo permanece em cache e ainda está disponível para outros usuários no mesmo sistema.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="9b1bf-583">Após uma atualização de publicação, os aplicativos limpos ficarão novamente disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="9b1bf-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="9b1bf-584">DeleteApp</span></span>

<span data-ttu-id="9b1bf-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-585">DWORD</span></span>

<span data-ttu-id="9b1bf-586">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-586">Default=0</span></span>

<span data-ttu-id="9b1bf-587">Um valor de 1 permite que o usuário use a ação de exclusão em aplicativos no SFTMime ou o console de gerenciamento de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="9b1bf-588">Quando você exclui um aplicativo, o aplicativo selecionado não estará mais disponível para os usuários do cliente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="9b1bf-589">Os atalhos e associações de tipo de arquivo são excluídos e o aplicativo é excluído do cache.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="9b1bf-590">No entanto, se outro aplicativo se refere a dados no cache do sistema de arquivos ou dados de configurações para o aplicativo selecionado, esses itens não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="9b1bf-591">Após uma atualização de publicação, os aplicativos excluídos ficarão novamente disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="9b1bf-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="9b1bf-592">ToggleOfflineMode</span></span>

<span data-ttu-id="9b1bf-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-593">DWORD</span></span>

<span data-ttu-id="9b1bf-594">Um valor 1 permite que os usuários selecionem executar o cliente no modo offline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="9b1bf-595">No modo offline, o cliente de virtualização de aplicativo pode iniciar um aplicativo carregado mesmo quando ele não está conectado a um servidor de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="9b1bf-596">Configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="9b1bf-596">Custom Settings</span></span>


<span data-ttu-id="9b1bf-597">A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contém valores específicos para componentes de front-end.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="9b1bf-598">Todas as configurações personalizadas são armazenadas como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="9b1bf-599">A tabela a seguir fornece informações sobre os valores do registro associados à chave CustomSettings.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-600">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-601">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-602">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-603">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="9b1bf-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-606">Padrão = 30</span><span class="sxs-lookup"><span data-stu-id="9b1bf-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-607">Tempo em segundos durante os quais a área de notificação do Application Virtualization exibirá mensagens de erro, como &quot; falha na inicialização &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b1bf-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="9b1bf-608">Valor mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="9b1bf-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-611">Padrão = 10</span><span class="sxs-lookup"><span data-stu-id="9b1bf-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="9b1bf-612">Tempo em segundos que a área de notificação do appvmed exibirá mensagens de sucesso como o &quot; Word foi iniciado &quot; ou o Excel será &quot; desligado &quot; .</span><span class="sxs-lookup"><span data-stu-id="9b1bf-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="9b1bf-613">Se 0, essas mensagens serão suprimidas.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="9b1bf-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-616">Padrão = 0</span><span class="sxs-lookup"><span data-stu-id="9b1bf-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-617">0 = mostrar bandeja quando aplicativos virtualizados estiverem em uso.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="9b1bf-618">1 = mostrar bandeja sempre.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="9b1bf-619">2 = nunca mostrar a bandeja.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="9b1bf-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-622">Quando apresentar e definido como um valor de 1, permite que os aplicativos de atualização de item de menu sejam exibidos no menu de bandeja e podem ser acessados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="9b1bf-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-625">Quando apresentar e definido como um valor de 1, permite que os aplicativos de carregamento de item de menu sejam exibidos no menu de bandeja e são acessíveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-626">Configurações de relatório</span><span class="sxs-lookup"><span data-stu-id="9b1bf-626">Reporting Settings</span></span>


<span data-ttu-id="9b1bf-627">A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contém valores específicos para relatório para um servidor de gerenciamento App-V.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="9b1bf-628">A tabela a seguir fornece informações sobre os valores do registro associados à chave de relatório.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b1bf-629">Nome</span><span class="sxs-lookup"><span data-stu-id="9b1bf-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-630">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b1bf-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-631">Dados (exemplos)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="9b1bf-632">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b1bf-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b1bf-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="9b1bf-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-635">Padrão = 20</span><span class="sxs-lookup"><span data-stu-id="9b1bf-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-636">Esse valor especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="9b1bf-637">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="9b1bf-638">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="9b1bf-639">Quando um novo registro for adicionado (na parte inferior da lista), um ou mais dos registros mais antigos (topo da lista) serão excluídos para liberar espaço.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="9b1bf-640">Um aviso será registrado no log do cliente e no log de eventos na primeira vez que isso ocorrer, e ele não será registrado novamente até que o cache seja limpo com êxito na transmissão e o log tenha sido preenchido novamente.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b1bf-641">Datablockize</span><span class="sxs-lookup"><span data-stu-id="9b1bf-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="9b1bf-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-643">Padrão = 65536</span><span class="sxs-lookup"><span data-stu-id="9b1bf-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b1bf-644">Esse valor especifica o tamanho máximo em bytes a ser transmitido ao servidor ao mesmo tempo na atualização de publicação, para evitar falhas de transmissão permanente quando o log atingir um tamanho significativo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="9b1bf-645">O valor padrão é 65536.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-645">The default value is 65536.</span></span> <span data-ttu-id="9b1bf-646">Ao transmitir dados de relatório para o servidor, um bloco de registros de aplicativo — menor ou igual ao tamanho do bloco em bytes de dados XML — será removido do cache e enviado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="9b1bf-647">Cada bloco terá os dados de cliente gerais e os dados da lista de pacotes globais preparados, e esses dados não serão fatorados nos cálculos de tamanho do bloco; o potencial existe para uma lista de pacotes extremamente grandes resultar em falhas de transmissão com largura de banda baixa ou conexões não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9b1bf-648">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b1bf-648">Related topics</span></span>


[<span data-ttu-id="9b1bf-649">Referência do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="9b1bf-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









