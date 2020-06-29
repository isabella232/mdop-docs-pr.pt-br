---
title: Configurar os pré-requisitos de instalação
description: Configurar os pré-requisitos de instalação
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797499"
---
# <span data-ttu-id="c48e9-103">Configurar os pré-requisitos de instalação</span><span class="sxs-lookup"><span data-stu-id="c48e9-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="c48e9-104">As instruções a seguir são pré-requisitos para instalar e usar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="c48e9-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="c48e9-105">PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="c48e9-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="c48e9-106">Atualização do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c48e9-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="c48e9-107">Antivirus/configuração do software de backup</span><span class="sxs-lookup"><span data-stu-id="c48e9-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="c48e9-108">Como instalar e configurar o Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c48e9-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="c48e9-109">**Importante**  Se já existir uma versão do Virtual PC para Windows no computador host, você deverá desinstalá-la antes de instalar o Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c48e9-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="c48e9-110">Para instalar o Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c48e9-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="c48e9-111">Baixe o [computador virtual do Windows](https://go.microsoft.com/fwlink/?LinkId=195918) a partir do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="c48e9-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="c48e9-112">Execute o arquivo de instalação no computador host e siga as etapas no assistente.</span><span class="sxs-lookup"><span data-stu-id="c48e9-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="c48e9-113">**Importante**  O Windows Virtual PC inclui o pacote de componentes de integração, que fornece recursos que melhoram a interação entre o ambiente virtual e o computador físico.</span><span class="sxs-lookup"><span data-stu-id="c48e9-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="c48e9-114">Por exemplo, ele permite que o mouse se movimente entre o host e os computadores convidados.</span><span class="sxs-lookup"><span data-stu-id="c48e9-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="c48e9-115">O MED-V requer a instalação do pacote de componentes de integração.</span><span class="sxs-lookup"><span data-stu-id="c48e9-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="c48e9-116">Como instalar e configurar a atualização do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c48e9-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="c48e9-117">A atualização da Microsoft associada ao artigo KB977206 habilita o modo Windows XP para computadores sem a tecnologia de virtualização assistida por hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="c48e9-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="c48e9-118">Recomendamos que você instale esta atualização porque alguns recursos de integração podem não funcionar corretamente se o pacote de componentes de integração no sistema operacional convidado não corresponderem à versão do computador virtual do Windows instalada no computador host.</span><span class="sxs-lookup"><span data-stu-id="c48e9-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="c48e9-119">**Importante**  Você não precisa instalar esta atualização ao instalar o MED-V em computadores host que executam o Windows 7 com Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c48e9-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="c48e9-120">**Dica**  Além da atualização listada aqui, recomendamos que você examine todas as atualizações disponíveis do Windows Virtual PC e aplique essas atualizações adequadas ou necessárias para o seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="c48e9-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="c48e9-121">Para instalar a atualização do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c48e9-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="c48e9-122">Baixe a atualização necessária do Windows Virtual PC no centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c48e9-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="c48e9-123">[atualização de 32 bits](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="c48e9-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="c48e9-124">[atualização de 64 bits](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="c48e9-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="c48e9-125">Execute o arquivo de instalação no computador host no modo elevado e siga as etapas no assistente.</span><span class="sxs-lookup"><span data-stu-id="c48e9-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="c48e9-126">Para obter mais informações sobre o pacote de hotfix para o PC virtual do Windows, consulte o [artigo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="c48e9-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="c48e9-127">Como configurar antivírus/software de backup</span><span class="sxs-lookup"><span data-stu-id="c48e9-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="c48e9-128">Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, recomendamos que você possa excluir os seguintes tipos de arquivo de máquina virtual de qualquer processo de antivírus ou backup em execução no computador host:</span><span class="sxs-lookup"><span data-stu-id="c48e9-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="c48e9-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="c48e9-129">\*.VMC</span></span>

-   <span data-ttu-id="c48e9-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="c48e9-130">\*.VUD</span></span>

-   <span data-ttu-id="c48e9-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="c48e9-131">\*.VSV</span></span>

-   <span data-ttu-id="c48e9-132">\*. Wim</span><span class="sxs-lookup"><span data-stu-id="c48e9-132">\*.VHD</span></span>

## <span data-ttu-id="c48e9-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c48e9-133">Related topics</span></span>


[<span data-ttu-id="c48e9-134">Configurar os pré-requisitos do ambiente</span><span class="sxs-lookup"><span data-stu-id="c48e9-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="c48e9-135">Arquitetura de alto nível</span><span class="sxs-lookup"><span data-stu-id="c48e9-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="c48e9-136">Configurações com suporte na MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c48e9-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





