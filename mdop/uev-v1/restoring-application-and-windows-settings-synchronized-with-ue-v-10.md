---
title: Restauração de configurações de aplicativos e do Windows com a UE-V 1.0
description: Restauração de configurações de aplicativos e do Windows com a UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795984"
---
# <span data-ttu-id="7ed17-103">Restauração de configurações de aplicativos e do Windows com a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ed17-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="7ed17-104">Os recursos do WMI e do PowerShell da Microsoft User Experience Virtualization (UE-V) oferecem a capacidade de restaurar pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="7ed17-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="7ed17-105">Os comandos do WMI e do PowerShell permitem restaurar as configurações do aplicativo e do Windows para os valores de configurações que estavam no computador na primeira vez que o aplicativo foi iniciado após a instalação do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="7ed17-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="7ed17-106">Essa ação de restauração é realizada em uma base de configurações por aplicativo ou Windows.</span><span class="sxs-lookup"><span data-stu-id="7ed17-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="7ed17-107">As configurações serão restauradas na próxima vez que o aplicativo for executado ou quando o usuário fizer logon no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7ed17-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="7ed17-108">Para restaurar as configurações do aplicativo e as configurações do Windows com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ed17-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="7ed17-109">Abra a janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ed17-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="7ed17-110">Para importar o módulo Microsoft UE-V PowerShell, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="7ed17-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="7ed17-111">Digite o seguinte cmdlet do PowerShell para restaurar as configurações do aplicativo e as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="7ed17-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7ed17-112">Cmdlet do PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ed17-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7ed17-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ed17-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ed17-114">Restore-UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="7ed17-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ed17-115">Restaura as configurações do usuário para um aplicativo ou restaura um grupo de configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="7ed17-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="7ed17-116">Para restaurar as configurações do aplicativo e as configurações do Windows com WMI</span><span class="sxs-lookup"><span data-stu-id="7ed17-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="7ed17-117">Abra uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ed17-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="7ed17-118">Digite o seguinte comando WMI para restaurar as configurações do aplicativo e as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="7ed17-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="7ed17-119">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="7ed17-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="7ed17-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ed17-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7ed17-121">Invoke-WmiMethod-namespace root\Microsoft\UEV-Setting UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="7ed17-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7ed17-122">Restaura as configurações do usuário para um aplicativo ou restaura um grupo de configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="7ed17-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="7ed17-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ed17-123">Related topics</span></span>


[<span data-ttu-id="7ed17-124">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ed17-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="7ed17-125">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7ed17-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





