---
title: Tecnologia Trim Transfer do MED-V
description: Tecnologia Trim Transfer do MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799822"
---
# <span data-ttu-id="15ba9-103">Tecnologia Trim Transfer do MED-V</span><span class="sxs-lookup"><span data-stu-id="15ba9-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="15ba9-104">A tecnologia de eliminação de duplicação avançada da transferência de corte do MED-V acelera o download de imagens de máquinas virtuais iniciais e atualizadas na LAN ou WAN, reduzindo assim a largura de banda de rede necessária para transportar uma máquina virtual de espaço de trabalho do MED-V para vários usuários finais.</span><span class="sxs-lookup"><span data-stu-id="15ba9-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="15ba9-105">Essa tecnologia inovadora usa dados locais existentes para criar a imagem da máquina virtual, aproveitando o fato de que, em muitos casos, grande parte da máquina virtual (por exemplo, arquivos do sistema e do aplicativo) já existe no disco do usuário final.</span><span class="sxs-lookup"><span data-stu-id="15ba9-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="15ba9-106">Por exemplo, se uma máquina virtual que contém o WindowsXP for entregue a um cliente executando uma cópia local do WindowsXP, o MED-V removerá automaticamente os elementos WindowsXP redundantes da transferência.</span><span class="sxs-lookup"><span data-stu-id="15ba9-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="15ba9-107">Para garantir um espaço de trabalho válido e funcional, o cliente MED-V Verifica criptograficamente a integridade dos dados locais antes de usá-los, garantindo que os blocos de dados locais sejam absolutamente idênticos aos da imagem da máquina virtual desejada.</span><span class="sxs-lookup"><span data-stu-id="15ba9-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="15ba9-108">Blocos que não correspondem não são usados.</span><span class="sxs-lookup"><span data-stu-id="15ba9-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="15ba9-109">O processo é eficiente na largura de banda e é transparente, e as transferências são executadas em segundo plano, utilizando recursos de CPU e CPU não utilizados.</span><span class="sxs-lookup"><span data-stu-id="15ba9-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="15ba9-110">Ao atualizar para uma nova versão de imagem (por exemplo, quando os administradores querem distribuir um novo aplicativo ou patch), somente os elementos que foram alterados ("deltas") são baixados, e não toda a máquina virtual, reduzindo significativamente a largura de banda e o tempo de entrega necessários para a rede.</span><span class="sxs-lookup"><span data-stu-id="15ba9-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="15ba9-111">Você pode configurar quais pastas serão indexadas no host como parte do protocolo de transferência de corte, com base no sistema operacional do host.</span><span class="sxs-lookup"><span data-stu-id="15ba9-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="15ba9-112">Essas configurações são definidas no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="15ba9-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="15ba9-113">Durante a aplicação de novas configurações, o serviço deve ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="15ba9-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





