---
title: Notas de versão do DaRT 10
description: Notas de versão do DaRT 10
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799175"
---
# <span data-ttu-id="f5652-103">Notas de versão do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="f5652-103">Release Notes for DaRT 10</span></span>


**<span data-ttu-id="f5652-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="f5652-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="f5652-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="f5652-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

<span data-ttu-id="f5652-106">Estas notas da versão contêm informações necessárias para instalar com êxito o diagnóstico e o conjunto de ferramentas de recuperação 10.</span><span class="sxs-lookup"><span data-stu-id="f5652-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 10.</span></span> <span data-ttu-id="f5652-107">As notas de versão também contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="f5652-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="f5652-108">Se houver uma diferença entre essas notas de versão e outra documentação do DaRT, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="f5652-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="f5652-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="f5652-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="f5652-110">Problemas conhecidos com o DaRT 10</span><span class="sxs-lookup"><span data-stu-id="f5652-110">Known issues with DaRT 10</span></span>


### <span data-ttu-id="f5652-111">O Disk Commander não consegue reparar um registro de inicialização mestre corrompido em uma partição física no Windows 10</span><span class="sxs-lookup"><span data-stu-id="f5652-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 10</span></span>

<span data-ttu-id="f5652-112">No Windows 10, o "restaurar o registro mestre de inicialização (MBR) ou o cabeçalho da tabela de partição GUID (GPT)" no Disk Commander não pode reparar um registro de inicialização mestre corrompido em uma partição física e, portanto, não pode inicializar o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f5652-112">In Windows 10, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="f5652-113">**Solução alternativa:** Inicie **o reparo de inicialização**, clique em **solucionar problemas**, clique em **Opções avançadas**e clique em **Iniciar reparo**.</span><span class="sxs-lookup"><span data-stu-id="f5652-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="f5652-114">Várias instâncias de apagamento de disco que destinam-se à mesma unidade fazem todas as instâncias, exceto a última para denunciar uma falha</span><span class="sxs-lookup"><span data-stu-id="f5652-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="f5652-115">Se você iniciar várias instâncias do apagamento de disco e, em seguida, tentar apagar a mesma unidade usando duas instâncias de apagamento de disco separadas, todas as instâncias, exceto a última, relatarão uma falha na limpeza da unidade.</span><span class="sxs-lookup"><span data-stu-id="f5652-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="f5652-116">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f5652-116">**Workaround:** None.</span></span>

### <span data-ttu-id="f5652-117">O apagamento de disco pode não limpar todos os dados em unidades de estado sólido com memória flash</span><span class="sxs-lookup"><span data-stu-id="f5652-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="f5652-118">Se você usar apagamento de disco para limpar dados em uma unidade de estado sólido (SSD) com memória flash, todos os dados podem não ser apagados.</span><span class="sxs-lookup"><span data-stu-id="f5652-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="f5652-119">Esse problema ocorre porque o firmware de SSD controla a localização física de gravações durante a execução do apagamento de disco.</span><span class="sxs-lookup"><span data-stu-id="f5652-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="f5652-120">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f5652-120">**Workaround:** None.</span></span>

### <span data-ttu-id="f5652-121">A restauração do sistema falha quando você executa o assistente do locksmith ou o editor do registro</span><span class="sxs-lookup"><span data-stu-id="f5652-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="f5652-122">Se você executar o assistente do locksmith, editor do registro e possivelmente outras ferramentas, a restauração do sistema falhará.</span><span class="sxs-lookup"><span data-stu-id="f5652-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="f5652-123">**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie a restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="f5652-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="f5652-124">A verificação do verificador de arquivos do sistema (SFC) falha ao executar após iniciar e fechar o assistente do locksmith ou o gerenciamento do computador</span><span class="sxs-lookup"><span data-stu-id="f5652-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="f5652-125">Se você iniciar e fechar o assistente do locksmith ou ferramentas no gerenciamento do computador, o verificador de arquivos do sistema falhará para executar.</span><span class="sxs-lookup"><span data-stu-id="f5652-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="f5652-126">**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie o verificador de arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f5652-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="f5652-127">O instalador do DaRT não falha quando o kit de avaliação e implantação do Windows não está instalado</span><span class="sxs-lookup"><span data-stu-id="f5652-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="f5652-128">Se você instalar o DaRT 10 usando a linha de comando para executar o Windows Installer (. msi) e o kit de avaliação e implantação do Windows (WindowsADK) não tiver sido instalado, a instalação do DaRT não será bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5652-128">If you install DaRT 10 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="f5652-129">Atualmente, o instalador do DaRT 10 instala todos os componentes, exceto a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="f5652-129">Currently, the DaRT 10 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="f5652-130">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="f5652-130">**Workaround:** None.</span></span>

## <span data-ttu-id="f5652-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5652-131">Related topics</span></span>


[<span data-ttu-id="f5652-132">Sobre o DaRT 10</span><span class="sxs-lookup"><span data-stu-id="f5652-132">About DaRT 10</span></span>](about-dart-10.md)

 

 





