---
title: Como instalar o cliente MED-V
description: Como instalar o cliente MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800023"
---
# <span data-ttu-id="865de-103">Como instalar o cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="865de-103">How to Install MED-V Client</span></span>


<span data-ttu-id="865de-104">Em um cenário baseado em pacote de implantação, a instalação do cliente do MED-V está incluída no pacote de implantação e instalada diretamente do pacote.</span><span class="sxs-lookup"><span data-stu-id="865de-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="865de-105">Importante</span><span class="sxs-lookup"><span data-stu-id="865de-105">Important</span></span>**  
<span data-ttu-id="865de-106">Ao usar um pacote de implantação que não inclua uma imagem, certifique-se de que a imagem seja carregada na Web ou por push para a pasta de pré-teste antes de instalar o pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="865de-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="865de-107">Para instalar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="865de-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="865de-108">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="865de-108">Do one of the following:</span></span>

    -   <span data-ttu-id="865de-109">Baixe o pacote do MED-V na Web.</span><span class="sxs-lookup"><span data-stu-id="865de-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="865de-110">Insira o DVD ou USB de implantação na unidade host.</span><span class="sxs-lookup"><span data-stu-id="865de-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="865de-111">Se o MED-V não iniciar automaticamente, clique duas vezes MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="865de-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="865de-112">Uma caixa de diálogo é exibida listando os componentes que já estão instalados e os que estão sendo instalados no momento.</span><span class="sxs-lookup"><span data-stu-id="865de-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="865de-113">Observação</span><span class="sxs-lookup"><span data-stu-id="865de-113">Note</span></span>**  
    <span data-ttu-id="865de-114">Se houver uma versão do Microsoft Virtual PC sem suporte no computador host, será exibida uma mensagem informando que você deseja desinstalar a versão existente e executar o instalador novamente.</span><span class="sxs-lookup"><span data-stu-id="865de-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="865de-115">Se necessário, reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="865de-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="865de-116">Quando a instalação estiver concluída, o MED-V será iniciado e será exibida uma mensagem informando que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="865de-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="865de-117">Conecte-se ao MED-V usando o nome de usuário e a senha a seguir:</span><span class="sxs-lookup"><span data-stu-id="865de-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="865de-118">Digite o nome de domínio e o nome de usuário seguidos da senha do usuário do domínio que tem permissão para funcionar com o MED-V.</span><span class="sxs-lookup"><span data-stu-id="865de-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="865de-119">Exemplo: "domínio \ _name \\user\ _name", "senha"</span><span class="sxs-lookup"><span data-stu-id="865de-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="865de-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="865de-120">Related topics</span></span>


[<span data-ttu-id="865de-121">Como configurar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="865de-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="865de-122">Como carregar uma imagem do MED-V no servidor</span><span class="sxs-lookup"><span data-stu-id="865de-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="865de-123">Referência de linha de comando para instalação do cliente</span><span class="sxs-lookup"><span data-stu-id="865de-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









