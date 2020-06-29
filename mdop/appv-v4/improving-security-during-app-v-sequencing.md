---
title: Como melhorar a segurança durante o sequenciamento do App-V
description: Como melhorar a segurança durante o sequenciamento do App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796909"
---
# <span data-ttu-id="99519-103">Como melhorar a segurança durante o sequenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="99519-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="99519-104">Os aplicativos de empacotamento para sequenciamento são a maior tarefa em andamento em uma infraestrutura do App-V.</span><span class="sxs-lookup"><span data-stu-id="99519-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="99519-105">Como essa tarefa está em andamento, você deve considerar com cuidado a criação de políticas e procedimentos a serem seguidos durante a sequenciamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="99519-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="99519-106">No App-V 4.5, durante o sequenciamento, você pode capturar listas de controle de acesso (ACLs) nos ativos de arquivo do aplicativo virtualizado.</span><span class="sxs-lookup"><span data-stu-id="99519-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="99519-107">Verificação de vírus no sequenciador</span><span class="sxs-lookup"><span data-stu-id="99519-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="99519-108">É uma prática recomendada instalar o software de digitalização no computador de sequenciamento e, em seguida, verificar o computador em busca de vírus e malware.</span><span class="sxs-lookup"><span data-stu-id="99519-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="99519-109">Depois que o computador de sequenciamento é examinado e gratuito de qualquer vírus ou malware, desabilite o software de digitalização, incluindo todo o antivírus e software de detecção de malware, no computador de sequenciamento antes de sequenciar qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99519-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="99519-110">Isso acelera o processo de sequenciamento e impede que os componentes do software de digitalização sejam detectados durante o sequenciamento e incluídos no pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="99519-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="99519-111">Capturando ACLs em arquivos (NTFS)</span><span class="sxs-lookup"><span data-stu-id="99519-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="99519-112">O sequenciador captura as permissões de NTFS (as ACLs) dos arquivos que são monitorados durante a fase de instalação de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="99519-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="99519-113">(Antes do lançamento do App-V 4.5, as ACLs não eram capturadas como parte do processo de sequenciamento.) Este novo recurso permite que determinados aplicativos sejam executados para usuários com um nível baixo de permissão que normalmente exigiria privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="99519-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="99519-114">Esse recurso também permite que o engenheiro de sequenciamento Capture as configurações de segurança identificadas pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="99519-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="99519-115">A falha na aplicação das configurações recomendadas pelo fornecedor pode deixar o aplicativo aberto para atacar ou usar indevido para os usuários.</span><span class="sxs-lookup"><span data-stu-id="99519-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="99519-116">Para obter informações sobre se você deve ou não implantar um aplicativo com ACLs abertas, consulte o grupo de suporte do aplicativo ou o fornecedor do software.</span><span class="sxs-lookup"><span data-stu-id="99519-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="99519-117">**Importante**  Embora o sequenciador Capture as ACLs de NTFS ao monitorar a fase de instalação do sequenciamento, ele não captura as ACLs para o registro.</span><span class="sxs-lookup"><span data-stu-id="99519-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="99519-118">Os usuários têm acesso total a todas as chaves do registro para aplicativos virtuais, exceto para serviços.</span><span class="sxs-lookup"><span data-stu-id="99519-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="99519-119">No entanto, se um usuário modificar o registro de um aplicativo virtual, essa alteração será armazenada em um local específico ( `uservol_sftfs_v1.pkg` ) e não afetará outros usuários.</span><span class="sxs-lookup"><span data-stu-id="99519-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="99519-120">Durante a fase de instalação, um engenheiro de sequenciamento pode modificar as permissões padrão dos arquivos, se necessário.</span><span class="sxs-lookup"><span data-stu-id="99519-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="99519-121">Depois que o processo de sequenciamento estiver concluído, mas antes de salvar o pacote, o engenheiro de sequenciamento poderá optar por impor descritores de segurança que foram capturados durante a fase de instalação.</span><span class="sxs-lookup"><span data-stu-id="99519-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="99519-122">É uma prática recomendada forçar descritores de segurança se nenhuma outra solução permitir que o aplicativo seja executado corretamente quando virtualizado.</span><span class="sxs-lookup"><span data-stu-id="99519-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





