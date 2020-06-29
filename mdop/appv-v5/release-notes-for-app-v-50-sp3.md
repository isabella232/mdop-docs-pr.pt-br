---
title: Notas de versão do App-V 5.0 SP3
description: Notas de versão do App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796221"
---
# <span data-ttu-id="15913-103">Notas de versão do App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="15913-103">Release Notes for App-V 5.0 SP3</span></span>


<span data-ttu-id="15913-104">Estes são problemas conhecidos do Microsoft Application Virtualization (App-V) 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="15913-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.0 SP3.</span></span>

## <span data-ttu-id="15913-105">Arquivos de servidor falha ao ser excluído após uma nova instalação do App-V 5,0 SP3 Server</span><span class="sxs-lookup"><span data-stu-id="15913-105">Server files fail to get deleted after a new App-V 5.0 SP3 Server installation</span></span>


<span data-ttu-id="15913-106">Se você desinstalar o servidor App-V 5,0 SP1 e instalar o aplicativo App-V 5,0 SP3, a instalação falhará e a versão errada do servidor de gerenciamento será instalada.</span><span class="sxs-lookup"><span data-stu-id="15913-106">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.0 SP3 Server, the installation fails and the wrong version of the Management server is installed.</span></span> <span data-ttu-id="15913-107">Os seguintes erros são exibidos:</span><span class="sxs-lookup"><span data-stu-id="15913-107">The following errors are displayed:</span></span>

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

<span data-ttu-id="15913-108">O problema ocorre porque os arquivos do servidor não estão sendo excluídos ao desinstalar o App-V 5,0 SP1, portanto, o processo de instalação do App-V 5,0 SP3 emite erroneamente uma atualização em vez de uma nova instalação.</span><span class="sxs-lookup"><span data-stu-id="15913-108">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the App-V 5.0 SP3 installation process erroneously does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="15913-109">**Solução alternativa**: exclua a seguinte chave do registro antes de começar a instalar o App-V 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="15913-109">**Workaround**: Delete the following registry key before you start installing App-V 5.0 SP3:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## <span data-ttu-id="15913-110">Consultar o AD DS pode fazer com que alguns aplicativos funcionem incorretamente</span><span class="sxs-lookup"><span data-stu-id="15913-110">Querying AD DS can cause some applications to work incorrectly</span></span>


<span data-ttu-id="15913-111">Quando você recebe pacotes atualizados consultando os serviços de domínio do Active Directory para associações de grupo atualizadas, isso pode fazer com que alguns aplicativos funcionem incorretamente se os aplicativos dependerem do token de acesso do usuário.</span><span class="sxs-lookup"><span data-stu-id="15913-111">When you receive updated packages by querying Active Directory Domain Services for updated group memberships, it can cause some applications to work incorrectly if the applications depend on the user’s access token.</span></span> <span data-ttu-id="15913-112">Além disso, consultas frequentes em associação a grupos podem causar sobrecarregar o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="15913-112">In addition, frequent group membership queries can cause the domain controller to overload.</span></span> <span data-ttu-id="15913-113">Para obter mais informações sobre os tokens de acesso do usuário, consulte [tokens do Access](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span><span class="sxs-lookup"><span data-stu-id="15913-113">For more information about user access tokens, see [Access Tokens](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span></span>

<span data-ttu-id="15913-114">**Solução alternativa**: Aguarde até que o usuário faça logoff e logon novamente antes de consultar associações de grupo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="15913-114">**Workaround**: Wait until the user logs off and then logs back on before you query for updated group memberships.</span></span> <span data-ttu-id="15913-115">Não use a chave do registro, descrita em [pacote de hotfix 2 para Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087), para consultar associações de grupo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="15913-115">Do not use the registry key, described in [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://support.microsoft.com/kb/2897087), to query for updated group memberships.</span></span>






## <span data-ttu-id="15913-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15913-116">Related topics</span></span>


[<span data-ttu-id="15913-117">Sobre o App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="15913-117">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

 

 





