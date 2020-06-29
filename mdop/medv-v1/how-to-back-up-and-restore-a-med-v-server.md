---
title: Como fazer backup e restaurar um servidor do MED-V
description: Como fazer backup e restaurar um servidor do MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799202"
---
# <span data-ttu-id="3f37e-103">Como fazer backup e restaurar um servidor do MED-V</span><span class="sxs-lookup"><span data-stu-id="3f37e-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="3f37e-104">É possível fazer o backup dos arquivos XML localizados no servidor e depois restaurá-los em caso de perda de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="3f37e-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="3f37e-105">Para fazer backup de um servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="3f37e-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="3f37e-106">Faça backup dos seguintes arquivos, localizados em \* &lt; installdir &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="3f37e-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="3f37e-107">**Observação**  Se a configuração tiver sido alterada do padrão, os arquivos poderão estar armazenados em um local diferente.</span><span class="sxs-lookup"><span data-stu-id="3f37e-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="3f37e-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="3f37e-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="3f37e-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="3f37e-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="3f37e-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="3f37e-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="3f37e-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="3f37e-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="3f37e-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="3f37e-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="3f37e-113">**Observação**  Também é possível fazer o backup do arquivo ServerSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="3f37e-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="3f37e-114">No entanto, se uma configuração específica tiver sido alterada (por exemplo, no servidor original, o diretório de VMS do MED-V está localizado em "*C:\\Vms*" e tal diretório não existe no novo servidor), ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="3f37e-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="3f37e-115">Para restaurar um servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="3f37e-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="3f37e-116">Instale um novo servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="3f37e-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="3f37e-117">Copie os arquivos de backup para o seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="3f37e-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="3f37e-118">&lt;InstallDir &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="3f37e-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="3f37e-119">Reinicie o serviço MED-V.</span><span class="sxs-lookup"><span data-stu-id="3f37e-119">Restart the MED-V service.</span></span>

 

 





