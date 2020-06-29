---
title: Notas de versão do App-V 4.6 SP3
description: Notas de versão do App-V 4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797596"
---
# <span data-ttu-id="d3d53-103">Notas de versão do App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d3d53-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="d3d53-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="d3d53-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="d3d53-105">Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="d3d53-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="d3d53-106">Estas notas da versão contêm informações que ajudam você a instalar com êxito o Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="d3d53-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="d3d53-107">Este documento contém informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="d3d53-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="d3d53-108">Se houver uma diferença entre essas notas de versão e outras documentações do App-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="d3d53-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d3d53-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="d3d53-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d3d53-110">Proteger contra vulnerabilidades e vírus de segurança</span><span class="sxs-lookup"><span data-stu-id="d3d53-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="d3d53-111">Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="d3d53-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="d3d53-112">Para obter mais informações, consulte o [site de segurança da Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="d3d53-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="d3d53-113">Problemas conhecidos com o Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d3d53-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="d3d53-114">Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="d3d53-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="d3d53-115">Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto.</span><span class="sxs-lookup"><span data-stu-id="d3d53-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="d3d53-116">Quando isso for possível, esses problemas serão resolvidos em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d3d53-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="d3d53-117">Não é possível abrir hiperlinks usando o Internet Explorer11 no Microsoft Windows 8,1 no ambiente virtual</span><span class="sxs-lookup"><span data-stu-id="d3d53-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="d3d53-118">A tentativa de abrir hiperlinks dentro de um ambiente virtual falhará no Windows 8,1 usando o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d3d53-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="d3d53-119">Isso ocorre porque o Internet Explorer 11 agora vem com o modo de proteção avançada (EPM) habilitado por padrão, e isso faz com que o App-V seja incapaz de acessar as chaves de registro, arquivos e objetos de porta de comunicação necessários.</span><span class="sxs-lookup"><span data-stu-id="d3d53-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="d3d53-120">SOLUÇÃO alternativa: desabilite o EPM no Internet Explorer11 antes de abrir um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="d3d53-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="d3d53-121">Isso permitirá que você abra o Internet Explorer dentro do ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="d3d53-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="d3d53-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3d53-122">Related topics</span></span>


[<span data-ttu-id="d3d53-123">Sobre o Microsoft Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d3d53-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





