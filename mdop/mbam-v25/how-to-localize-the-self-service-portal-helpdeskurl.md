---
title: Como localizar o "HelpdeskURL" do Portal de Autoatendimento
description: Como localizar o "HelpdeskURL" do Portal de Autoatendimento
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799926"
---
# <span data-ttu-id="b29f9-103">Como localizar o "HelpdeskURL" do Portal de Autoatendimento</span><span class="sxs-lookup"><span data-stu-id="b29f9-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="b29f9-104">Você pode configurar uma versão localizada da URL do portal de autoatendimento para exibir aos usuários finais por padrão.</span><span class="sxs-lookup"><span data-stu-id="b29f9-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="b29f9-105">A URL do portal de autoatendimento é representada pelo parâmetro **HelpdeskURL**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="b29f9-106">Se você criar uma versão localizada, conforme descrito nas instruções a seguir, a administração e o monitoramento do Microsoft BitLocker (MBAM) localiza e exibe a versão localizada.</span><span class="sxs-lookup"><span data-stu-id="b29f9-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="b29f9-107">Se o MBAM não encontrar uma versão localizada, ele exibirá a URL configurada para o parâmetro **HelpDeskURL**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="b29f9-108">**Observação**  Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="b29f9-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="b29f9-109">Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="b29f9-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="b29f9-110">Para localizar a URL do portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="b29f9-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="b29f9-111">No servidor em que você configurou o portal de autoatendimento, navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="b29f9-112">No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="b29f9-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="b29f9-113">No campo **nome** , digite **HelpdeskURL**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para a URL.</span><span class="sxs-lookup"><span data-stu-id="b29f9-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="b29f9-114">Por exemplo, para criar uma versão localizada do `HelpdeskURL` valor em espanhol, nomeie o parâmetro **HelpdeskURL \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="b29f9-115">O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="b29f9-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="b29f9-116">Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão.</span><span class="sxs-lookup"><span data-stu-id="b29f9-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="b29f9-117">Esse fallback recursivo imita as regras de carregamento de recursos do .NET.</span><span class="sxs-lookup"><span data-stu-id="b29f9-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="b29f9-118">Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="b29f9-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="b29f9-119">No campo **valor** , digite a versão localizada do `HelpdeskURL` valor que você deseja exibir para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="b29f9-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="b29f9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b29f9-120">Related topics</span></span>


[<span data-ttu-id="b29f9-121">Personalizando o Portal de Autoatendimento para sua organização</span><span class="sxs-lookup"><span data-stu-id="b29f9-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="b29f9-122">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="b29f9-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b29f9-123">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="b29f9-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b29f9-124">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b29f9-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




