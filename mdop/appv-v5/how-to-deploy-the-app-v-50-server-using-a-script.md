---
title: Como implantar o servidor App-V 5.0 usando um script
description: Como implantar o servidor App-V 5.0 usando um script
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796432"
---
# <span data-ttu-id="7657a-103">Como implantar o servidor App-V 5.0 usando um script</span><span class="sxs-lookup"><span data-stu-id="7657a-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="7657a-104">Para concluir a configuração do servidor do **appv\_server\_setup.exe** com êxito usando a linha de comando, você deve especificar e combinar vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7657a-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="7657a-105">Use as tabelas a seguir para obter mais informações sobre como instalar o servidor do App-V 5,0 usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7657a-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="7657a-106">As informações nas tabelas a seguir também podem ser acessadas usando a linha de comando digitando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="7657a-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="7657a-107">Parâmetros e exemplos comuns</span><span class="sxs-lookup"><span data-stu-id="7657a-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-108">Para instalar o servidor de gerenciamento e o banco de dados de gerenciamento em um computador local.</span><span class="sxs-lookup"><span data-stu-id="7657a-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-109">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-117">Para usar uma instância personalizada do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-125">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7657a-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7657a-129">/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7657a-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7657a-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7657a-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7657a-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7657a-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-134">Para instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador local.</span><span class="sxs-lookup"><span data-stu-id="7657a-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-135">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-143">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-151">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7657a-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7657a-155">/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7657a-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7657a-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7657a-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7657a-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7657a-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-160">Para instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="7657a-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-161">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-169">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-177">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="7657a-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="7657a-181">/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="7657a-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="7657a-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="7657a-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. DomainName"</span><span class="sxs-lookup"><span data-stu-id="7657a-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="7657a-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7657a-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-186">Para instalar o banco de dados de gerenciamento e o servidor de gerenciamento no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="7657a-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-187">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-193">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-199">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7657a-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7657a-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="7657a-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7657a-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-206">Para instalar o banco de dados de gerenciamento em um computador diferente do servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7657a-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-207">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-213">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-219">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="7657a-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="7657a-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="7657a-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="7657a-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-226">Para instalar o Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="7657a-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-227">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-232">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="7657a-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="7657a-236">/PUBLISHING_WEBSITE_NAME = "serviço Microsoft AppV Publishing"</span><span class="sxs-lookup"><span data-stu-id="7657a-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="7657a-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="7657a-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-238">Para instalar o servidor de relatórios e o banco de dados de relatórios em um computador local.</span><span class="sxs-lookup"><span data-stu-id="7657a-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-239">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-240">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-241">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-242">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-245">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-246">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-247">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-248">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-249">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-250">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-253">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-254">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="7657a-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-257">/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="7657a-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7657a-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="7657a-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="7657a-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7657a-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-262">Para instalar o servidor de relatórios e usar um banco de dados de relatórios existente em um computador local.</span><span class="sxs-lookup"><span data-stu-id="7657a-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-263">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-264">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-265">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-266">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-270">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-271">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-272">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-273">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-274">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-278">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-281">/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="7657a-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7657a-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="7657a-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7657a-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7657a-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-286">Para instalar o servidor de relatórios usando um banco de dados de relatórios existente em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="7657a-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-287">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-288">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-289">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-290">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-294">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-295">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="7657a-296">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-297">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-298">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-302">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="7657a-305">/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="7657a-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="7657a-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="7657a-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="7657a-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</span><span class="sxs-lookup"><span data-stu-id="7657a-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="7657a-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7657a-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-310">Para instalar o banco de dados de relatórios no mesmo computador que o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="7657a-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-311">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-314">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-317">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-320">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="7657a-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-323">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="7657a-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7657a-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="7657a-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="7657a-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-330">Para instalar o banco de dados de relatórios em um computador diferente do que o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="7657a-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-331">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-334">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-337">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="7657a-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="7657a-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="7657a-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="7657a-340">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="7657a-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="7657a-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="7657a-343">Usar uma instância personalizada do exemplo do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="7657a-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="7657a-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="7657a-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="7657a-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</span><span class="sxs-lookup"><span data-stu-id="7657a-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="7657a-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="7657a-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="7657a-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="7657a-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="7657a-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="7657a-350">Definições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-350">Parameter Definitions</span></span>

### <span data-ttu-id="7657a-351">Parâmetros gerais</span><span class="sxs-lookup"><span data-stu-id="7657a-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-352">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-353">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-354">/QUIET</span><span class="sxs-lookup"><span data-stu-id="7657a-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-355">Especifica a instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="7657a-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="7657a-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-357">Especifica uma desinstalação.</span><span class="sxs-lookup"><span data-stu-id="7657a-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="7657a-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-359">Especifica a ação de layout.</span><span class="sxs-lookup"><span data-stu-id="7657a-359">Specifies layout action.</span></span> <span data-ttu-id="7657a-360">Isso extrai os arquivos MSIs e script para uma pasta sem realmente instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="7657a-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="7657a-361">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="7657a-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-363">Especifica o diretório de layout.</span><span class="sxs-lookup"><span data-stu-id="7657a-363">Specifies the layout directory.</span></span> <span data-ttu-id="7657a-364">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-364">Takes a string.</span></span> <span data-ttu-id="7657a-365">Por exemplo,/LAYOUTDIR = "servidor de virtualização C:\Application"</span><span class="sxs-lookup"><span data-stu-id="7657a-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="7657a-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-367">Especifica o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="7657a-367">Specifies the installation directory.</span></span> <span data-ttu-id="7657a-368">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-368">Takes a string.</span></span> <span data-ttu-id="7657a-369">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-369">E.g.</span></span> <span data-ttu-id="7657a-370">/INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="7657a-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="7657a-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-372">Habilita o Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="7657a-372">Enables Microsoft Update.</span></span> <span data-ttu-id="7657a-373">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="7657a-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-375">Aceita o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="7657a-375">Accepts the license agreement.</span></span> <span data-ttu-id="7657a-376">Isso é necessário para uma instalação automática.</span><span class="sxs-lookup"><span data-stu-id="7657a-376">This is required for an unattended installation.</span></span> <span data-ttu-id="7657a-377">Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-378">Parâmetros de instalação do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7657a-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-379">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-380">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-382">Especifica que o servidor de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="7657a-383">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-385">Especifica a conta que terá permissão de acesso de administrador ao servidor de gerenciamento essa conta pode ser uma conta de usuário individual ou um grupo.</span><span class="sxs-lookup"><span data-stu-id="7657a-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="7657a-386">Exemplo de uso: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="7657a-387">Se <strong> /MANAGEMENT_SERVER </strong> não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="7657a-388">Especifica a conta que será permitida para o acesso de administrador ao servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7657a-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="7657a-389">Pode ser uma conta de usuário ou um grupo.</span><span class="sxs-lookup"><span data-stu-id="7657a-389">This can be a user account or a group.</span></span> <span data-ttu-id="7657a-390">Por exemplo, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-392">Especifica o nome do site que será criado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7657a-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="7657a-393">Por exemplo,/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft App-V"</span><span class="sxs-lookup"><span data-stu-id="7657a-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-395">Especifica o número da porta que será usada pelo serviço de gerenciamento que será usado.</span><span class="sxs-lookup"><span data-stu-id="7657a-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="7657a-396">Por exemplo,/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="7657a-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-397">Parâmetros para o banco de dados do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7657a-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-398">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-399">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="7657a-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-401">Especifica que o banco de dados de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="7657a-402">Você deve ter permissões de banco de dados suficientes para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="7657a-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="7657a-403">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-405">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="7657a-406">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-408">Especifica o nome da instância SQL personalizada que deve ser usada para criar um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7657a-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="7657a-409">Exemplo de uso: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="7657a-410">Se/DB_PREDEPLOY_MANAGEMENT não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-412">Especifica o nome do novo banco de dados de gerenciamento que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="7657a-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="7657a-413">Exemplo de uso: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="7657a-414">Se/DB_PREDEPLOY_MANAGEMENT não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-416">Indica se o servidor de gerenciamento que vai acessar o banco de dados está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="7657a-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="7657a-417">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-419">Especifica a conta de máquina do computador remoto em que o servidor de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="7657a-420">Exemplo de uso: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</span><span class="sxs-lookup"><span data-stu-id="7657a-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-422">Indica a conta de administrador que será usada para instalar o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7657a-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="7657a-423">Exemplo de uso: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "DOMAIN\alias"</span><span class="sxs-lookup"><span data-stu-id="7657a-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-424">Parâmetros para instalar o Publishing Server</span><span class="sxs-lookup"><span data-stu-id="7657a-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-425">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-426">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-428">Especifica que o servidor de publicação será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="7657a-429">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-431">Especifica a URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado.</span><span class="sxs-lookup"><span data-stu-id="7657a-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="7657a-432">Exemplo de uso: <strong> http:// &lt; Management Server Name &gt; : número de &lt; porta do servidor de gerenciamento &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="7657a-433">Se/PUBLISHING_SERVER não for usado, este parâmetro será ignorado</span><span class="sxs-lookup"><span data-stu-id="7657a-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-435">Especifica o nome do site que será criado para o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="7657a-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="7657a-436">Por exemplo,/PUBLISHING_WEBSITE_NAME = "serviço Microsoft App-V Publishing"</span><span class="sxs-lookup"><span data-stu-id="7657a-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-438">Especifica o número da porta usada pelo serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="7657a-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="7657a-439">Por exemplo,/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="7657a-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-440">Parâmetros do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="7657a-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-441">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-442">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="7657a-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-444">Especifica que o servidor de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="7657a-445">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-447">Especifica o nome do site que será criado para o serviço de relatório.</span><span class="sxs-lookup"><span data-stu-id="7657a-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="7657a-448">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-448">E.g.</span></span> <span data-ttu-id="7657a-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="7657a-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-451">Especifica o número da porta que o serviço de relatórios vai usar.</span><span class="sxs-lookup"><span data-stu-id="7657a-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="7657a-452">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-452">E.g.</span></span> <span data-ttu-id="7657a-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="7657a-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="7657a-454">Parâmetros para usar um banco de dados do servidor de relatórios existente</span><span class="sxs-lookup"><span data-stu-id="7657a-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-455">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-456">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-458">Indica que o Microsoft SQL Server está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="7657a-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="7657a-459">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-461">Especifica o nome do computador remoto no qual o SQL Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="7657a-462">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-462">Takes a string.</span></span> <span data-ttu-id="7657a-463">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-463">E.g.</span></span> <span data-ttu-id="7657a-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-465">/EXISTING_ DB_SQLINSTANCE_USE_DEFAULT de relatório <em></span><span class="sxs-lookup"><span data-stu-id="7657a-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-466">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="7657a-467">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-469">Especifica o nome da instância SQL personalizada que deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="7657a-470">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-470">Takes a string.</span></span> <span data-ttu-id="7657a-471">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-471">E.g.</span></span> <span data-ttu-id="7657a-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYsqlserver&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-473">/EXISTING_ _DB_NAME DE RELATÓRIO</span><span class="sxs-lookup"><span data-stu-id="7657a-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-474">Especifica o nome do banco de dados de relatórios existente que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="7657a-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="7657a-475">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-475">Takes a string.</span></span> <span data-ttu-id="7657a-476">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-476">E.g.</span></span> <span data-ttu-id="7657a-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-478">Parâmetros para instalar o banco de dados do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="7657a-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-479">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-480">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="7657a-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-482">Especifica que o banco de dados de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="7657a-483">As permissões do DBA são necessárias para esta instalação.</span><span class="sxs-lookup"><span data-stu-id="7657a-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="7657a-484">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="7657a-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-486">Especifica o nome da instância SQL personalizada que deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="7657a-487">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-487">Takes a string.</span></span> <span data-ttu-id="7657a-488">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-488">E.g.</span></span> <span data-ttu-id="7657a-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYsqlserver&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-491">Especifica o nome do novo banco de dados de relatórios que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="7657a-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="7657a-492">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-492">Takes a string.</span></span> <span data-ttu-id="7657a-493">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-493">E.g.</span></span> <span data-ttu-id="7657a-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-496">Indica que o servidor de relatórios que vai acessar o banco de dados está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="7657a-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="7657a-497">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-499">Especifica a conta de máquina do computador remoto em que o servidor de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="7657a-500">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-500">Takes a string.</span></span> <span data-ttu-id="7657a-501">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-501">E.g.</span></span> <span data-ttu-id="7657a-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="7657a-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-504">Indica a conta de administrador que será usada para instalar o servidor de relatórios do App-V.</span><span class="sxs-lookup"><span data-stu-id="7657a-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="7657a-505">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-505">Takes a string.</span></span> <span data-ttu-id="7657a-506">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-506">E.g.</span></span> <span data-ttu-id="7657a-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; DOMAIN\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="7657a-508">Parâmetros para usar um banco de dados existente do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7657a-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7657a-509">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7657a-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7657a-510">Informações</span><span class="sxs-lookup"><span data-stu-id="7657a-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7657a-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-512">Indica que o SQL Server está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="7657a-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="7657a-513">Parâmetro de opção; portanto, nenhum valor é esperado. Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-515">Especifica o nome do computador remoto no qual o SQL Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="7657a-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="7657a-516">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7657a-516">Takes a string.</span></span> <span data-ttu-id="7657a-517">Ex.</span><span class="sxs-lookup"><span data-stu-id="7657a-517">E.g.</span></span> <span data-ttu-id="7657a-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="7657a-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7657a-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-520">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="7657a-521">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="7657a-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="7657a-522">Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7657a-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7657a-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-524">Especifica o nome da instância SQL personalizada que será usada.</span><span class="sxs-lookup"><span data-stu-id="7657a-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="7657a-525">Exemplo de uso <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="7657a-526">Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7657a-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="7657a-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7657a-528">Especifica o nome do banco de dados de gerenciamento existente que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="7657a-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="7657a-529">Exemplo de uso: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="7657a-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="7657a-530">Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7657a-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="7657a-531">Tem uma sugestão para o App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="7657a-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="7657a-532">Adicione ou vote em sugestões <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> aqui </a> .</span><span class="sxs-lookup"><span data-stu-id="7657a-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="7657a-533">Tem um App-V emissão </strong> e?</span><span class="sxs-lookup"><span data-stu-id="7657a-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="7657a-534">Use o <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Fórum do TechNet do App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="7657a-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="7657a-535">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7657a-535">Related topics</span></span>

[<span data-ttu-id="7657a-536">Implantação do servidor App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7657a-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





