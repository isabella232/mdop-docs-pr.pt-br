---
title: Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)
description: Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797656"
---
# <span data-ttu-id="65c47-103">Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="65c47-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="65c47-104">Você pode usar aceleradores de pacotes do App-V para sequenciar automaticamente aplicativos grandes e complexos.</span><span class="sxs-lookup"><span data-stu-id="65c47-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="65c47-105">Além disso, ao aplicar um acelerador de pacote App-V, você nem sempre é obrigado a instalar manualmente um aplicativo para criar o pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="65c47-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="65c47-106">**Observação**  Em alguns casos, você será solicitado a instalar um aplicativo localmente no computador que está executando o sequenciador do App-V antes de poder usar o acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="65c47-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="65c47-107">Se você precisar instalar um aplicativo, deverá instalar o aplicativo para o local padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65c47-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="65c47-108">Esta instalação não é monitorada pelo App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="65c47-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="65c47-109">Quando o acelerador do pacote do App-V é criado, o autor do acelerador de pacote determina se o aplicativo deve ser instalado localmente é necessário.</span><span class="sxs-lookup"><span data-stu-id="65c47-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="65c47-110">O sequenciador do App-V extrai os arquivos necessários do acelerador de pacotes do App-V e a mídia de instalação associada para criar um pacote virtual sem ter que monitorar a instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65c47-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="65c47-111">**Importante**  Aviso de isenção de responsabilidade: o Microsoft Application Virtualization Sequencer não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote.</span><span class="sxs-lookup"><span data-stu-id="65c47-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="65c47-112">Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65c47-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="65c47-113">É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="65c47-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="65c47-114">Os aceleradores de pacotes do App-V e os modelos de projeto diferem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="65c47-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="65c47-115">Aceleradores de pacote são específicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65c47-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="65c47-116">Os modelos de projeto permitem que os usuários salvem as configurações mais comuns específicas de uma organização e as apliquem a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="65c47-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="65c47-117">Você também pode criar modelos de projeto no prompt de comando, enquanto em contraste, você deve usar o console do App-V Sequencer para criar aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="65c47-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="65c47-118">Além disso, não há suporte para a criação de um pacote usando um acelerador de pacote e a aplicação de um modelo de projeto.</span><span class="sxs-lookup"><span data-stu-id="65c47-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="65c47-119">Compartilhando aceleradores de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="65c47-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="65c47-120">Esta seção fornece informações de práticas recomendadas sobre como compartilhar aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="65c47-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="65c47-121">Se você planeja compartilhar aceleradores de pacote, informações como nomes de computador, informações da conta do usuário e informações sobre os aplicativos associados podem estar incluídas nos aceleradores de pacote. a lista a seguir descreve os métodos que você deve considerar ao criar aceleradores de pacote:</span><span class="sxs-lookup"><span data-stu-id="65c47-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="65c47-122">**Nome de usuário**.</span><span class="sxs-lookup"><span data-stu-id="65c47-122">**User name**.</span></span> <span data-ttu-id="65c47-123">Ao fazer logon no computador que executa o App-V Sequencer, você deve usar uma conta de usuário genérica, como a conta de **administrador** interna para administrar o computador/domínio.</span><span class="sxs-lookup"><span data-stu-id="65c47-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="65c47-124">Você não deve usar uma conta com base em um nome de usuário existente.</span><span class="sxs-lookup"><span data-stu-id="65c47-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="65c47-125">**Nome do computador**.</span><span class="sxs-lookup"><span data-stu-id="65c47-125">**Computer Name**.</span></span> <span data-ttu-id="65c47-126">Especifique um nome geral e não identificado para o computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="65c47-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="65c47-127">**URL do servidor**.</span><span class="sxs-lookup"><span data-stu-id="65c47-127">**Server URL**.</span></span> <span data-ttu-id="65c47-128">No console do sequenciador, na guia **implantação** , use as configurações padrão para as informações de configuração da URL do servidor.</span><span class="sxs-lookup"><span data-stu-id="65c47-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="65c47-129">**Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="65c47-129">**Applications**.</span></span> <span data-ttu-id="65c47-130">Se você não deseja compartilhar a lista de aplicativos que foram instalados no computador que executa o sequenciador quando você criou o acelerador de pacote, você deve excluir o arquivo **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="65c47-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="65c47-131">Esse arquivo está localizado no diretório raiz do pacote do pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="65c47-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="65c47-132">Você também deve analisar quaisquer configurações ou arquivos de configuração associados ao pacote de aplicativo virtual para garantir que os aplicativos não contenham informações pessoais.</span><span class="sxs-lookup"><span data-stu-id="65c47-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="65c47-133">Proteger aceleradores de pacotes do App-V</span><span class="sxs-lookup"><span data-stu-id="65c47-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="65c47-134">Sempre salve os aceleradores de pacotes do App-V e qualquer mídia de instalação associada em um local seguro na rede para proteger os aceleradores de pacotes do App-V e os arquivos de instalação contra violações ou se tornarem corrompidos.</span><span class="sxs-lookup"><span data-stu-id="65c47-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="65c47-135">Como os aceleradores de pacote também podem conter informações específicas de senha e usuário, você deve salvar aceleradores de pacotes do App-V em um local seguro, e você deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o editor possa ser verificado quando o acelerador de pacote for aplicado.</span><span class="sxs-lookup"><span data-stu-id="65c47-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="65c47-136">Para obter mais informações sobre assinaturas digitais, consulte [diretrizes de aplicativos sobre práticas de assinatura digital para segurança do Common Criteria](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="65c47-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="65c47-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c47-137">Related topics</span></span>


[<span data-ttu-id="65c47-138">Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="65c47-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="65c47-139">Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="65c47-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





