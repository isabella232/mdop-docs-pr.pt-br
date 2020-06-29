---
title: Interoperabilidade do App-V com o Windows AppLocker
description: Interoperabilidade do App-V com o Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799047"
---
# <span data-ttu-id="d5625-103">Interoperabilidade do App-V com o Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="d5625-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="d5625-104">A versão 4,5 SP1 do cliente do Microsoft Application Virtualization (App-V) oferece suporte ao recurso AppLocker do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d5625-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="d5625-105">O recurso AppLocker permite que os administradores de ti especifiquem quais aplicativos estão impedidos de serem executados em computadores.</span><span class="sxs-lookup"><span data-stu-id="d5625-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="d5625-106">Este documento descreve como configurar as regras do AppLocker para trabalhar com o ambiente virtual do App-V e aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="d5625-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="d5625-107">**Observação**  O Windows AppLocker deve ser habilitado primeiro antes da configuração de regras do Windows AppLocker para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="d5625-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="d5625-108">Para obter mais informações sobre como habilitar o Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="d5625-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="d5625-109">Configurando regras do Windows AppLocker para aplicativos virtuais</span><span class="sxs-lookup"><span data-stu-id="d5625-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="d5625-110">Os administradores locais podem criar regras do Windows AppLocker que restringem a execução de executáveis de programa (arquivos. exe), arquivos do Windows Installer (arquivos. msi e. msp) e scripts (arquivos. PS,. bat,. cmd,. vbs e. js).</span><span class="sxs-lookup"><span data-stu-id="d5625-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="d5625-111">O administrador faz isso usando um computador de referência que tenha o cliente App-V instalado e que tenha todos os aplicativos virtuais relevantes transmitidos para o cache do cliente.</span><span class="sxs-lookup"><span data-stu-id="d5625-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="d5625-112">Em seguida, o administrador usa a seção Windows AppLocker do snap-in console de gerenciamento da Microsoft (MMC) da política de segurança local no computador de referência para criar as regras.</span><span class="sxs-lookup"><span data-stu-id="d5625-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="d5625-113">Ao navegar para localizar um caminho de diretório ou arquivo específico para o qual você deseja criar uma regra, você pode acessar a unidade App-V usando o caminho para o compartilhamento oculto.</span><span class="sxs-lookup"><span data-stu-id="d5625-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="d5625-114">Por exemplo, você pode navegar até \\\\localhost\\Q $, onde a unidade App-V é a unidade Q. No entanto, para criar a regra, você deve editar o caminho para remover a referência a \\\\localhost\\Q $ e usar Q:\\ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d5625-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="d5625-115">Você deve iniciar cada aplicativo no computador de referência para acessar os arquivos do aplicativo, e os direitos administrativos são necessários para navegar até \\\\localhost\\Q $.</span><span class="sxs-lookup"><span data-stu-id="d5625-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





