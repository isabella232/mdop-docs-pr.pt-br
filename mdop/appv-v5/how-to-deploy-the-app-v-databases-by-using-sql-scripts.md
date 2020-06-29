---
title: Como implantar os bancos de dados do App-V usando scripts SQL
description: Como implantar os bancos de dados do App-V usando scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796418"
---
# <span data-ttu-id="22757-103">Como implantar os bancos de dados do App-V usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="22757-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="22757-104">Use as instruções a seguir para usar scripts SQL, em vez do Windows Installer, para:</span><span class="sxs-lookup"><span data-stu-id="22757-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="22757-105">Instalar os bancos de dados do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="22757-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="22757-106">Atualizar os bancos de dados do 5,0 para uma versão mais recente</span><span class="sxs-lookup"><span data-stu-id="22757-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="22757-107">Como instalar os bancos de dados do App-V usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="22757-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="22757-108">Antes de instalar os scripts de banco de dados, revise e mantenha uma cópia dos termos de licença do App-V.</span><span class="sxs-lookup"><span data-stu-id="22757-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="22757-109">Ao executar os scripts de banco de dados, você está concordando com os termos de licença.</span><span class="sxs-lookup"><span data-stu-id="22757-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="22757-110">Se não aceitá-los, você não deve usar este software.</span><span class="sxs-lookup"><span data-stu-id="22757-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="22757-111">Copie o **appv\_server\_setup.exe** da mídia de versão do App-V para um local temporário.</span><span class="sxs-lookup"><span data-stu-id="22757-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="22757-112">Em um prompt de comando, execute **appv\_server\_setup.exe** e especifique um local temporário para extrair os scripts de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="22757-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="22757-113">Exemplo: appv\_server\_setup.exe/layout c:\\ &lt; caminho do local temporário&gt;</span><span class="sxs-lookup"><span data-stu-id="22757-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="22757-114">Navegue até o local temporário que você criou, abra a pasta **DatabaseScripts** extraída e revise o arquivo de Readme.txt apropriado para obter instruções:</span><span class="sxs-lookup"><span data-stu-id="22757-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="22757-115">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="22757-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="22757-116">Localização do arquivo Readme.txt a ser usado</span><span class="sxs-lookup"><span data-stu-id="22757-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="22757-117">Banco de dados de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="22757-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="22757-118">Subpasta ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="22757-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="22757-119">Importante</span><span class="sxs-lookup"><span data-stu-id="22757-119">Important</span></span></strong><br/><p><span data-ttu-id="22757-120">Se você estiver atualizando ou instalando o banco de dados de gerenciamento do App-V 5,0 SP3, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts do SQL para instalar ou atualizar o banco de dados do servidor de gerenciamento do App-v 5,0 SP3 falha </a> .</span><span class="sxs-lookup"><span data-stu-id="22757-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="22757-121">Banco de dados de relatórios</span><span class="sxs-lookup"><span data-stu-id="22757-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="22757-122">Subpasta ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="22757-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="22757-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22757-123">Related topics</span></span>


[<span data-ttu-id="22757-124">Implantação do servidor App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="22757-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="22757-125">Como implantar o servidor do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="22757-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









