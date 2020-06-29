---
title: Como localizar o texto de aviso do Portal de Autoatendimento
description: Como localizar o texto de aviso do Portal de Autoatendimento
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799927"
---
# <span data-ttu-id="1aa82-103">Como localizar o texto de aviso do Portal de Autoatendimento</span><span class="sxs-lookup"><span data-stu-id="1aa82-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="1aa82-104">Você pode configurar o texto de aviso localizado para exibir aos usuários finais por padrão no portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="1aa82-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="1aa82-105">O arquivo Notice.txt que exibe o texto do aviso está no diretório raiz a seguir:</span><span class="sxs-lookup"><span data-stu-id="1aa82-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="1aa82-106">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="1aa82-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="1aa82-107">Para exibir o texto de aviso localizado, crie um arquivo Notice.txt localizado e salve-o em uma pasta de idioma específico no seguinte diretório de exemplo:</span><span class="sxs-lookup"><span data-stu-id="1aa82-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="1aa82-108">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="1aa82-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="1aa82-109">**Observação**  Você pode configurar o caminho usando o item **NoticeTextPath** nas **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="1aa82-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="1aa82-110">O MBAM exibe o texto do aviso com base nas seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="1aa82-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="1aa82-111">Se você criar um arquivo **Notice.txt** localizado na pasta de idiomas apropriada, o MBAM exibirá o texto de aviso localizado se o arquivo de **Notice.txt** padrão existir.</span><span class="sxs-lookup"><span data-stu-id="1aa82-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="1aa82-112">Se o arquivo **Notice.txt** padrão estiver ausente, será exibida uma mensagem indicando que o arquivo padrão está ausente.</span><span class="sxs-lookup"><span data-stu-id="1aa82-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="1aa82-113">Se o MBAM não encontrar uma versão localizada do arquivo Notice.txt, ele exibirá o texto no arquivo de Notice.txt padrão.</span><span class="sxs-lookup"><span data-stu-id="1aa82-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="1aa82-114">Se o MBAM não encontrar um arquivo de Notice.txt padrão, ele exibirá o texto padrão no portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="1aa82-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="1aa82-115">**Observação**  Se o navegador de um usuário final estiver definido como um idioma que não tenha uma subpasta ou Notice.txt de idioma correspondente, o texto no arquivo Notice.txt do diretório raiz a seguir será exibido:</span><span class="sxs-lookup"><span data-stu-id="1aa82-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="1aa82-116">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="1aa82-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

 

**<span data-ttu-id="1aa82-117">Para criar um arquivo Notice.txt localizado</span><span class="sxs-lookup"><span data-stu-id="1aa82-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="1aa82-118">No servidor em que você configurou o portal de autoatendimento, crie uma &lt; *Language* &gt; pasta de idiomas no seguinte diretório de exemplo, em que &lt; o *idioma* &gt; representa o nome do idioma localizado:</span><span class="sxs-lookup"><span data-stu-id="1aa82-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="1aa82-119">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="1aa82-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    <span data-ttu-id="1aa82-120">**Observação**  Algumas pastas de idioma já existem, portanto, talvez você não precise criar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1aa82-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="1aa82-121">Se você precisar criar uma pasta de idiomas, consulte [referência da API do NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947) para obter uma lista dos nomes válidos que você pode usar para a pasta de &lt; *idiomas* &gt; .</span><span class="sxs-lookup"><span data-stu-id="1aa82-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="1aa82-122">Crie um arquivo Notice.txt que contenha o texto de aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="1aa82-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="1aa82-123">Salve o arquivo Notice.txt na pasta de &lt; *idiomas* &gt; .</span><span class="sxs-lookup"><span data-stu-id="1aa82-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="1aa82-124">Por exemplo, para criar um arquivo de Notice.txt localizado em espanhol, salve o arquivo Notice.txt localizado no seguinte exemplo de diretório:</span><span class="sxs-lookup"><span data-stu-id="1aa82-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="1aa82-125">&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\Es-es do serviço \\Self</span><span class="sxs-lookup"><span data-stu-id="1aa82-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="1aa82-126">O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="1aa82-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="1aa82-127">Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão.</span><span class="sxs-lookup"><span data-stu-id="1aa82-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="1aa82-128">Esse fallback recursivo imita as regras de carregamento de recursos do .NET.</span><span class="sxs-lookup"><span data-stu-id="1aa82-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="1aa82-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aa82-129">Related topics</span></span>


[<span data-ttu-id="1aa82-130">Personalizando o Portal de Autoatendimento para sua organização</span><span class="sxs-lookup"><span data-stu-id="1aa82-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="1aa82-131">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="1aa82-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1aa82-132">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1aa82-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1aa82-133">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1aa82-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





