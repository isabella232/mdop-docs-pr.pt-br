---
title: Pré-requisitos para clientes do MBAM 2.5
description: Pré-requisitos para clientes do MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799978"
---
# <span data-ttu-id="09eed-103">Pré-requisitos para clientes do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="09eed-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="09eed-104">Antes de instalar o software cliente MBAM nos computadores dos usuários finais, verifique se o seu ambiente e os computadores cliente atendem aos pré-requisitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="09eed-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09eed-105">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="09eed-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="09eed-106">Detalhes</span><span class="sxs-lookup"><span data-stu-id="09eed-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09eed-107">O domínio da empresa deve conter pelo menos um controlador de domínio do Windows Server 2008 (ou posterior).</span><span class="sxs-lookup"><span data-stu-id="09eed-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09eed-108">O computador cliente deve estar conectado à intranet da empresa.</span><span class="sxs-lookup"><span data-stu-id="09eed-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09eed-109">Para computadores cliente do Windows 7 somente: cada cliente deve ter a funcionalidade do Trusted Platform Module (TPM) (TPM 1,2 ou posterior).</span><span class="sxs-lookup"><span data-stu-id="09eed-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09eed-110">Para o Windows 8,1, Windows 10 RTM ou Windows 10 versão 1511 computadores cliente somente: se você quiser que o MBAM possa armazenar e gerenciar as chaves de recuperação do TPM, o provisionamento automático do TPM deve estar desativado e MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="09eed-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="09eed-111">Somente no MBAM 2,5 SP1, você não precisa mais desativar o provisionamento automático do TPM, mas deve certificar-se de que os objetos de política de grupo TPM estejam definidos para não fazer a caução do OwnerAuth do TPM para o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="09eed-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="09eed-112">Considerações sobre segurança do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="09eed-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09eed-113">Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM.</span><span class="sxs-lookup"><span data-stu-id="09eed-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="09eed-114">No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM.</span><span class="sxs-lookup"><span data-stu-id="09eed-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="09eed-115">No MBAM 2,5 SP1, você deve ativar o provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="09eed-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="09eed-116">Consulte <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> </a> a senha de proprietário do TPM para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="09eed-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09eed-117">O chip TPM deve estar ativado no BIOS e ser redefinido do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="09eed-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="09eed-118">Consulte a documentação do BIOS para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09eed-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09eed-119">O disco rígido do computador deve ter pelo menos duas partições e deve ser formatado com o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="09eed-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09eed-120">O disco rígido do computador deve ter um BIOS compatível com TPM e compatível com dispositivos USB durante a inicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="09eed-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="09eed-121">Observação</span><span class="sxs-lookup"><span data-stu-id="09eed-121">Note</span></span></strong><br/><p><span data-ttu-id="09eed-122">Verifique se o teclado, o vídeo ou o mouse estão diretamente conectados e não são gerenciados por meio de um botão de teclado, vídeo ou mouse (KVM).</span><span class="sxs-lookup"><span data-stu-id="09eed-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="09eed-123">Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.</span><span class="sxs-lookup"><span data-stu-id="09eed-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09eed-124">Se você usar um proxy, ele deve estar visível no contexto do sistema.</span><span class="sxs-lookup"><span data-stu-id="09eed-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="09eed-125">O MBAM é executado no contexto do sistema, não no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="09eed-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="09eed-126">Importante</span><span class="sxs-lookup"><span data-stu-id="09eed-126">Important</span></span>**  
<span data-ttu-id="09eed-127">Se o BitLocker tiver sido usado sem o MBAM, MBAM poderá ser instalado e utilizar as informações existentes do TPM.</span><span class="sxs-lookup"><span data-stu-id="09eed-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="09eed-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09eed-128">Related topics</span></span>


[<span data-ttu-id="09eed-129">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="09eed-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="09eed-130">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="09eed-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="09eed-131">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="09eed-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="09eed-132">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="09eed-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="09eed-133">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="09eed-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






