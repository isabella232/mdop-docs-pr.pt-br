---
title: Considerações sobre segurança para o DaRT 8.0
description: Considerações sobre segurança para o DaRT 8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796064"
---
# <span data-ttu-id="2d850-103">Considerações sobre segurança para o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="2d850-103">Security Considerations for DaRT 8.0</span></span>


<span data-ttu-id="2d850-104">Este tópico contém uma breve visão geral sobre as contas e grupos, arquivos de log e outras considerações relacionadas à segurança do Microsoft Diagnostics e do conjunto de ferramentas de recuperação (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="2d850-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span> <span data-ttu-id="2d850-105">Para obter mais informações, siga os links neste artigo.</span><span class="sxs-lookup"><span data-stu-id="2d850-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="2d850-106">Considerações gerais sobre segurança</span><span class="sxs-lookup"><span data-stu-id="2d850-106">General security considerations</span></span>


<span data-ttu-id="2d850-107">**Compreender os riscos de segurança**.</span><span class="sxs-lookup"><span data-stu-id="2d850-107">**Understand the security risks**.</span></span> <span data-ttu-id="2d850-108">O DaRT 8,0 inclui funcionalidade que permite que um administrador ou um trabalho de suporte técnico execute as ferramentas do DaRT remotamente para resolver problemas em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="2d850-108">DaRT 8.0 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="2d850-109">Além disso, você pode salvar a imagem ISO (International Organization for Standardization) em uma unidade flash USB ou colocar a imagem ISO em uma rede para incluir seu conteúdo como uma partição de recuperação no disco rígido de um computador.</span><span class="sxs-lookup"><span data-stu-id="2d850-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="2d850-110">Esses recursos oferecem flexibilidade, mas também podem criar possíveis riscos de segurança que você deve considerar ao configurar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="2d850-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="2d850-111">**Proteja seus computadores fisicamente**.</span><span class="sxs-lookup"><span data-stu-id="2d850-111">**Physically secure your computers**.</span></span> <span data-ttu-id="2d850-112">Quando os administradores e os funcionários do suporte técnico não estão fisicamente em seus computadores, eles devem bloquear seus computadores e usar um protetor de tela seguro.</span><span class="sxs-lookup"><span data-stu-id="2d850-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="2d850-113">**Aplicar as atualizações de segurança mais recentes a todos os computadores**.</span><span class="sxs-lookup"><span data-stu-id="2d850-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="2d850-114">Mantenha-se informado sobre novas atualizações para sistemas operacionais assinando o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="2d850-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="2d850-115">Limitar o acesso do usuário final às ferramentas do DaRT</span><span class="sxs-lookup"><span data-stu-id="2d850-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="2d850-116">Ao criar a imagem de recuperação do DaRT, você pode selecionar as ferramentas que deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="2d850-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="2d850-117">Por motivos de segurança, talvez você queira restringir o acesso do usuário final às ferramentas do DaRT mais poderosas, como apagamento de disco e locksmith.</span><span class="sxs-lookup"><span data-stu-id="2d850-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="2d850-118">No DaRT 8,0, você pode desabilitar determinadas ferramentas durante a configuração e ainda disponibilizá-las para trabalhadores de assistência técnica quando o usuário final iniciar o recurso de conexão remota.</span><span class="sxs-lookup"><span data-stu-id="2d850-118">In DaRT 8.0, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="2d850-119">Você pode até mesmo configurar a imagem DaRT para que a opção de iniciar uma sessão de conexão remota seja a única ferramenta disponível para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="2d850-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="2d850-120">**Importante**  Depois que a conexão remota for estabelecida, todas as ferramentas que você incluiu na imagem de recuperação, incluindo aquelas que não estão disponíveis para o usuário final, ficarão disponíveis para qualquer trabalho de suporte técnico que esteja trabalhando no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="2d850-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="2d850-121">Para obter mais informações sobre como incluir ferramentas na imagem de recuperação do DaRT, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="2d850-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

## <span data-ttu-id="2d850-122">Proteger a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="2d850-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="2d850-123">Se você implantar a imagem de recuperação do DaRT salvando-a em uma unidade flash USB ou criando uma partição remota ou uma partição de recuperação, talvez queira incluir o método preferido de criptografia de unidade da sua empresa no ISO.</span><span class="sxs-lookup"><span data-stu-id="2d850-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="2d850-124">A criptografia da ISO ajuda a garantir que os usuários finais não possam usar a funcionalidade do DaRT se tivessem acesso à imagem de recuperação e garante que os usuários não autorizados não possam inicializar o DaRT em computadores que pertençam a outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="2d850-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="2d850-125">Se você usar um método de criptografia, certifique-se de implantá-lo e habilitá-lo em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="2d850-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="2d850-126">**Observação**  O DaRT 8,0 oferece suporte ao BitLocker nativamente.</span><span class="sxs-lookup"><span data-stu-id="2d850-126">**Note** DaRT 8.0 supports BitLocker natively.</span></span>

 

<span data-ttu-id="2d850-127">Para incluir a criptografia de unidade, adicione os arquivos de solução de criptografia ao criar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2d850-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="2d850-128">Sua solução de criptografia deve ser capaz de ser executada no WinPE.</span><span class="sxs-lookup"><span data-stu-id="2d850-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="2d850-129">Os usuários finais que inicializam a partir da ISO poderão acessar a solução de criptografia e desbloquear a unidade.</span><span class="sxs-lookup"><span data-stu-id="2d850-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="2d850-130">Manter a segurança entre dois computadores quando você usa a conexão remota</span><span class="sxs-lookup"><span data-stu-id="2d850-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="2d850-131">Por padrão, a comunicação entre dois computadores que estabeleceram uma sessão de **conexão remota** pode não ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="2d850-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="2d850-132">Portanto, para ajudar a manter a segurança entre os dois computadores, recomendamos que ambos os computadores façam parte da mesma rede.</span><span class="sxs-lookup"><span data-stu-id="2d850-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="2d850-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d850-133">Related topics</span></span>


[<span data-ttu-id="2d850-134">Segurança e privacidade do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="2d850-134">Security and Privacy for DaRT 8.0</span></span>](security-and-privacy-for-dart-80-dart-8.md)

 

 





