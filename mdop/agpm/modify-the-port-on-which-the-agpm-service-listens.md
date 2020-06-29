---
title: Modificar a porta na qual o serviço do AGPM escuta
description: Modificar a porta na qual o serviço do AGPM escuta
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797735"
---
# <span data-ttu-id="99bdc-103">Modificar a porta na qual o serviço do AGPM escuta</span><span class="sxs-lookup"><span data-stu-id="99bdc-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="99bdc-104">O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção.</span><span class="sxs-lookup"><span data-stu-id="99bdc-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="99bdc-105">Por padrão, o serviço do AGPM escuta na porta 4600.</span><span class="sxs-lookup"><span data-stu-id="99bdc-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="99bdc-106">Você pode alterar essa porta modificando o arquivo de índice de arquivo de gerenciamento avançado de política de grupo (AGPM) para cada arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="99bdc-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="99bdc-107">**Observação**  Antes de modificar a porta na qual o serviço do AGPM escuta, é recomendável que você faça backup do arquivo de índice do arquivamento do AGPM (gpostate.xml).</span><span class="sxs-lookup"><span data-stu-id="99bdc-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="99bdc-108">Esse arquivo está localizado na pasta inserida como o caminho do arquivo morto durante a instalação do gerenciamento avançado de política de grupo-servidor.</span><span class="sxs-lookup"><span data-stu-id="99bdc-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="99bdc-109">Por padrão, esse local desse arquivo é% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="99bdc-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="99bdc-110">Se você não souber qual computador hospeda o arquivo, poderá seguir o procedimento para modificar o caminho do arquivo morto para exibir o caminho de arquivo morto atual.</span><span class="sxs-lookup"><span data-stu-id="99bdc-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="99bdc-111">Para obter mais informações, consulte [Modificar o caminho do arquivo morto](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="99bdc-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="99bdc-112">Uma conta de usuário com acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) e o arquivo de índice do arquivo morto é necessário para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="99bdc-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="99bdc-113">Para modificar a porta na qual o serviço do AGPM escuta</span><span class="sxs-lookup"><span data-stu-id="99bdc-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="99bdc-114">No computador que hospeda o arquivo morto, abra o arquivo de índice de arquivo (gpostate.xml) em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="99bdc-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="99bdc-115">No arquivo, procure **AGPM: Port = "4600"**.</span><span class="sxs-lookup"><span data-stu-id="99bdc-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="99bdc-116">Substitua **4600** pela porta na qual o serviço do AGPM deve escutar; em seguida, salve e feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="99bdc-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="99bdc-117">No servidor do AGPM, reinicie o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="99bdc-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="99bdc-118">(Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service.md).)</span><span class="sxs-lookup"><span data-stu-id="99bdc-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="99bdc-119">Modifique a porta na conexão do servidor do AGPM para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="99bdc-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="99bdc-120">(Para obter mais informações, consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).)</span><span class="sxs-lookup"><span data-stu-id="99bdc-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="99bdc-121">Repita para cada servidor de arquivamento e AGPM.</span><span class="sxs-lookup"><span data-stu-id="99bdc-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="99bdc-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="99bdc-122">Additional references</span></span>

-   [<span data-ttu-id="99bdc-123">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="99bdc-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





