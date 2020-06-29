---
title: Sobre Sequenciamento de Fases
description: Sobre Sequenciamento de Fases
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797638"
---
# <span data-ttu-id="a6c50-103">Sobre Sequenciamento de Fases</span><span class="sxs-lookup"><span data-stu-id="a6c50-103">About Sequencing Phases</span></span>


<span data-ttu-id="a6c50-104">O sequenciamento é o processo pelo qual você cria um pacote de aplicativo sequenciado usando o sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a6c50-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="a6c50-105">Durante o sequenciamento, o sequenciador monitora e registra todos os processos de instalação e configuração de um aplicativo e cria os seguintes arquivos: ICO, OSD, SFT e SPRJ.</span><span class="sxs-lookup"><span data-stu-id="a6c50-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="a6c50-106">Esses arquivos contêm todas as informações necessárias sobre um aplicativo e permitem que o aplicativo seja executado em um ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="a6c50-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="a6c50-107">As quatro fases para sequenciar um aplicativo e a criação de um pacote de aplicativo virtual são instalação, inicialização, personalização e salvamento.</span><span class="sxs-lookup"><span data-stu-id="a6c50-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="a6c50-108">A lista a seguir fornece informações sobre cada uma das fases:</span><span class="sxs-lookup"><span data-stu-id="a6c50-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="a6c50-109">**Fase de instalação**– durante a fase de instalação, você especifica o nome do pacote e um comentário associado opcional que será associado ao pacote.</span><span class="sxs-lookup"><span data-stu-id="a6c50-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="a6c50-110">Você também pode configurar opções avançadas de monitoramento durante essa fase.</span><span class="sxs-lookup"><span data-stu-id="a6c50-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="a6c50-111">As opções de monitoramento avançado incluem especificar o tamanho do bloco e se você vai instalar atualizações automáticas durante o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="a6c50-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="a6c50-112">O sequenciador registra todas as informações e configurações necessárias necessárias para criar um pacote de aplicativo virtual e as configurações de arquivo e registro associadas.</span><span class="sxs-lookup"><span data-stu-id="a6c50-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="a6c50-113">**Importante**  Para exibir as opções avançadas, selecione **Mostrar opções de monitoramento avançado** na página **informações do pacote** .</span><span class="sxs-lookup"><span data-stu-id="a6c50-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="a6c50-114">**Fase de lançamento**– durante a fase de lançamento, você pode especificar qualquer associação de arquivo e descritores de segurança necessários que devem ser configurados com o pacote.</span><span class="sxs-lookup"><span data-stu-id="a6c50-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="a6c50-115">Você deve abrir o aplicativo quantas vezes forem necessárias para garantir a funcionalidade e estabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6c50-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="a6c50-116">**Fase de personalização**– durante a fase de personalização, você pode configurar seu pacote usando os arquivos. OSD associados.</span><span class="sxs-lookup"><span data-stu-id="a6c50-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="a6c50-117">Você pode especificar se qualquer script associado deve ser executado dentro ou fora do ambiente virtual, especificar ações adicionais que devem ser realizadas, especificar como os scripts associados são executados (de forma síncrona ou assíncrona) e especificar quaisquer scripts adicionais que devem ser executados no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a6c50-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="a6c50-118">**Fase de salvamento**– durante a fase de salvamento, todos os arquivos necessários para o pacote de aplicativo virtual são criados.</span><span class="sxs-lookup"><span data-stu-id="a6c50-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="a6c50-119">Os arquivos criados são. sprj,. SFT,. OSD,. ico,. xml Manifest e o arquivo Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="a6c50-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="a6c50-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6c50-120">Related topics</span></span>


[<span data-ttu-id="a6c50-121">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="a6c50-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





