---
title: Notas de versão do MED-V 1.0
description: Notas de versão do MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799903"
---
# <span data-ttu-id="575ee-103">Notas de versão do MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="575ee-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="575ee-104">Problemas conhecidos com o MED-V</span><span class="sxs-lookup"><span data-stu-id="575ee-104">Known Issues with MED-V</span></span>


<span data-ttu-id="575ee-105">Esta seção fornece as informações mais atualizadas sobre problemas gerais com a plataforma da virtualização de área de trabalho do Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="575ee-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="575ee-106">Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto.</span><span class="sxs-lookup"><span data-stu-id="575ee-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="575ee-107">Sempre que possível, esses problemas serão resolvidos em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="575ee-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="575ee-108">Downloads de arquivos não seguem regras de redirecionamento da Web</span><span class="sxs-lookup"><span data-stu-id="575ee-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="575ee-109">Downloads de arquivos não seguem regras de redirecionamento da Web definidas em uma política do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="575ee-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="575ee-110">Ao expandir uma janela do aplicativo publicado pelo console para tela inteira, ele desaparece</span><span class="sxs-lookup"><span data-stu-id="575ee-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="575ee-111">Se você expandir uma janela de aplicativo publicado no console (como cmd.exe) para tela inteira dentro de um espaço de trabalho do MED-V configurado no modo de integração sem falhas, a janela do aplicativo poderá desaparecer ou não responder.</span><span class="sxs-lookup"><span data-stu-id="575ee-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="575ee-112">Ao trabalhar no modo de área de trabalho completo, os locais dos ícones na área de trabalho não são salvos</span><span class="sxs-lookup"><span data-stu-id="575ee-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="575ee-113">Ao trabalhar no modo de área de trabalho completo, as alterações de localização manual dos ícones na área de trabalho não são salvas entre sessões do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="575ee-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="575ee-114">Uma imagem local e uma imagem de teste com o mesmo nome não podem existir no mesmo domínio</span><span class="sxs-lookup"><span data-stu-id="575ee-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="575ee-115">Se uma imagem local estiver incluída no domínio e o administrador criar uma nova versão da mesma imagem com o mesmo nome de computador que uma imagem de teste, quando a imagem de teste entrar no domínio, a ação de ingresso no domínio falhará ou será bem-sucedida e a imagem local será removida do domínio.</span><span class="sxs-lookup"><span data-stu-id="575ee-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="575ee-116">O MED-V não oferece suporte aos recursos do Windows Aero</span><span class="sxs-lookup"><span data-stu-id="575ee-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="575ee-117">O MED-V não oferece suporte aos recursos do Windows Aero (como o Aero Flip 3D).</span><span class="sxs-lookup"><span data-stu-id="575ee-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="575ee-118">O console de gerenciamento pode ser usado por apenas um usuário do Windows por computador</span><span class="sxs-lookup"><span data-stu-id="575ee-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="575ee-119">O console de gerenciamento do MED-V pode ser usado apenas por administradores e pelo usuário do Windows que instalou o aplicativo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="575ee-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="575ee-120">O utilitário de configuração do servidor MED-V testa a conectividade do Microsoft SQL Server em contexto do usuário, em vez do contexto do serviço do servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="575ee-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="575ee-121">O MED-V usa o contexto do serviço do servidor MED-V para coletar relatórios do banco de dados relatórios do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="575ee-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="575ee-122">O utilitário de configuração do MED-V Server verifica o banco de dados e testa a cadeia de conexão do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="575ee-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="575ee-123">Ele não valida o acesso do serviço do servidor MED-V ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="575ee-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





