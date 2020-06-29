---
ms.reviewer: ''
title: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0
description: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796301"
---
# <span data-ttu-id="326f8-103">Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="326f8-103">How to Use an App-V 4.6 Application From an App-V 5.0 Application</span></span>

<span data-ttu-id="326f8-104">*Observação:*\* App-V 4,6 saiu do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="326f8-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="326f8-105">O seguinte se aplica a um pacote App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="326f8-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="326f8-106">Use o procedimento a seguir para executar um aplicativo App-V 4.6 com aplicativos do App-V 5,0 em um cliente autônomo.</span><span class="sxs-lookup"><span data-stu-id="326f8-106">Use the following procedure to run an App-V4.6 application with App-V 5.0 applications on a standalone client.</span></span>

**<span data-ttu-id="326f8-107">Para executar aplicativos em um cliente autônomo</span><span class="sxs-lookup"><span data-stu-id="326f8-107">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="326f8-108">Selecione dois aplicativos em seu ambiente que podem ser abertos uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="326f8-108">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="326f8-109">Por exemplo, Microsoft Outlook e Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="326f8-109">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="326f8-110">Você pode acessar um anexo de email criado usando o Adobe Acrobat.</span><span class="sxs-lookup"><span data-stu-id="326f8-110">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="326f8-111">Converta os pacotes ou crie um novo pacote para qualquer um dos aplicativos usando o formato App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="326f8-111">Convert the packages, or create a new package for either of the applications using the App-V 5.0 format.</span></span> <span data-ttu-id="326f8-112">Para obter mais informações sobre como converter pacotes, consulte [como migrar pontos de extensão de um pacote app-v 4,6 para um pacote app-v 5,0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) ou [como migrar pontos de extensão de um pacote app-v 4,6 para o app-v 5,0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="326f8-112">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="326f8-113">Adicione e provisione o pacote usando o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="326f8-113">Add and provision the package using the App-V 5.0 management console.</span></span> <span data-ttu-id="326f8-114">Para obter mais informações sobre como adicionar e provisionar pacotes, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [como configurar o acesso aos pacotes usando o console de gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="326f8-114">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span></span>

4.  <span data-ttu-id="326f8-115">O aplicativo convertido agora é executado usando o App-V 5,0 e você pode abrir um aplicativo da outra.</span><span class="sxs-lookup"><span data-stu-id="326f8-115">The converted application now runs using App-V 5.0 and you can open one application from the other.</span></span> <span data-ttu-id="326f8-116">Por exemplo, se você converteu um pacote do Microsoft Office em um pacote do App-V 5,0 e o Adobe Acrobat ainda está sendo executado como um pacote App-V 4.6, você pode abrir um anexo do Adobe Acrobat Reader usando o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="326f8-116">For example, if you converted a Microsoft Office package to an App-V 5.0 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="326f8-117">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="326f8-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="326f8-118">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="326f8-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="326f8-119">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="326f8-119">Got an App-V issue?</span></span>** <span data-ttu-id="326f8-120">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="326f8-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="326f8-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="326f8-121">Related topics</span></span>


[<span data-ttu-id="326f8-122">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="326f8-122">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 








