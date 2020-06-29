---
title: Considerações sobre segurança para o DaRT 7.0
description: Considerações sobre segurança para o DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799131"
---
# <span data-ttu-id="78e8b-103">Considerações sobre segurança para o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="78e8b-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="78e8b-104">O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui funcionalidade que permite que um administrador execute as ferramentas do DaRT remotamente para resolver problemas em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="78e8b-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="78e8b-105">Em versões anteriores do DaRT, um técnico ou administrador do suporte técnico tinha que estar fisicamente em um computador de usuário final e inicializar o DaRT usando o CD ou DVD que incluiu a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="78e8b-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="78e8b-106">Agora, o técnico da assistência técnica ou o administrador podem executar os mesmos procedimentos remotamente.</span><span class="sxs-lookup"><span data-stu-id="78e8b-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="78e8b-107">Além disso, no DaRT7, além de gravar um CD ou DVD, agora você pode salvar a imagem ISO (organização internacional de normalização) em uma unidade flash USB.</span><span class="sxs-lookup"><span data-stu-id="78e8b-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="78e8b-108">Você também pode colocar a imagem ISO em uma rede ou incluir seu conteúdo como uma partição de recuperação em um disco rígido do computador.</span><span class="sxs-lookup"><span data-stu-id="78e8b-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="78e8b-109">O recurso **conexão remota** no DaRT7 permite que os usuários finais acessem o DART usando um desses métodos de implantação novos.</span><span class="sxs-lookup"><span data-stu-id="78e8b-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="78e8b-110">Portanto, eles podem iniciar o DaRT com facilidade e acessar as ferramentas DaRT.</span><span class="sxs-lookup"><span data-stu-id="78e8b-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="78e8b-111">As novas funcionalidades no DaRT7 fornecem muito mais flexibilidade em como usar o DaRT na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="78e8b-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="78e8b-112">No entanto, eles também criam seu próprio conjunto de problemas de segurança que devem ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="78e8b-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="78e8b-113">Recomendamos que você considere as seguintes dicas de segurança ao configurar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="78e8b-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="78e8b-114">Para ajudar a manter a segurança ao criar a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="78e8b-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="78e8b-115">Ao criar a imagem de recuperação do DaRT, você pode selecionar as ferramentas que deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="78e8b-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="78e8b-116">Por motivos de segurança, talvez você queira restringir o acesso do usuário final às ferramentas do DaRT mais poderosas, como apagamento de disco e locksmith.</span><span class="sxs-lookup"><span data-stu-id="78e8b-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="78e8b-117">No DaRT7, você pode desabilitar determinadas ferramentas durante a configuração e ainda disponibilizá-las aos agentes do helpdesk quando o usuário final iniciar o recurso de conexão remota.</span><span class="sxs-lookup"><span data-stu-id="78e8b-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="78e8b-118">Você pode até mesmo configurar a imagem DaRT para que a opção de iniciar uma sessão de conexão remota seja a única ferramenta disponível para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="78e8b-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="78e8b-119">**Importante**  Depois que a conexão remota for estabelecida, todas as ferramentas que você incluiu na imagem de recuperação, incluindo aquelas que não estão disponíveis para o usuário final, ficarão disponíveis para o agente de helpdesk trabalhando no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="78e8b-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="78e8b-120">Para obter mais informações sobre como incluir ferramentas na imagem de recuperação do DaRT, consulte [como usar o assistente de imagem de recuperação do DART para criar a imagem de recuperação](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="78e8b-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="78e8b-121">Para ajudar a manter a segurança criptografando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="78e8b-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="78e8b-122">Se você usar uma das opções de implantação novas no DaRT7, por exemplo, salvar em uma unidade flash USB ou criar uma partição remota ou uma partição de recuperação, poderá incluir o método preferido de criptografia de unidade da sua empresa na ISO.</span><span class="sxs-lookup"><span data-stu-id="78e8b-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="78e8b-123">Isso ajudará a garantir que um usuário final não possa usar a funcionalidade do DaRT caso ele tenha acesso à imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="78e8b-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="78e8b-124">Além disso, ele também garantirá que os usuários não autorizados não possam inicializar o DaRT em computadores que pertençam a outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="78e8b-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="78e8b-125">O método de criptografia deve ser implantado e habilitado em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="78e8b-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="78e8b-126">**Observação**  O DaRT7 é compatível com o BitLocker nativamente.</span><span class="sxs-lookup"><span data-stu-id="78e8b-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="78e8b-127">Para ajudar a manter a segurança entre dois computadores durante a conexão remota</span><span class="sxs-lookup"><span data-stu-id="78e8b-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="78e8b-128">Por padrão, a comunicação entre dois computadores que estabeleceram uma sessão de **conexão remota** pode não ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="78e8b-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="78e8b-129">Portanto, para ajudar a manter a segurança entre os dois computadores, recomendamos que ambos os computadores façam parte da mesma rede.</span><span class="sxs-lookup"><span data-stu-id="78e8b-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="78e8b-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78e8b-130">Related topics</span></span>


[<span data-ttu-id="78e8b-131">Operações do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="78e8b-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





