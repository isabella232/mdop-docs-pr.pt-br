---
title: Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento
description: Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799269"
---
# <span data-ttu-id="33c3a-103">Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento</span><span class="sxs-lookup"><span data-stu-id="33c3a-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="33c3a-104">Você pode configurar uma versão localizada da instrução "HelpdeskText" do portal de autoatendimento, que informa os usuários finais sobre como obter ajuda adicional quando estiverem usando o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="33c3a-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="33c3a-105">Se você configurar o texto localizado para a instrução, conforme descrito nas instruções a seguir, o MBAM exibirá a versão localizada.</span><span class="sxs-lookup"><span data-stu-id="33c3a-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="33c3a-106">Se MBAM não encontrar a versão localizada, ele exibirá o valor que está no parâmetro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="33c3a-107">**Observação**  Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="33c3a-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="33c3a-108">Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="33c3a-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="33c3a-109">Para exibir uma versão localizada da instrução HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="33c3a-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="33c3a-110">No servidor em que você configurou o portal de autoatendimento, navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="33c3a-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="33c3a-111">No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="33c3a-112">No campo **nome** , digite **HelpdeskText**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para o texto.</span><span class="sxs-lookup"><span data-stu-id="33c3a-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="33c3a-113">Por exemplo, para criar uma instrução HelpdeskText localizada em espanhol, nomeie o parâmetro **HelpdeskText \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="33c3a-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="33c3a-114">O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**.</span><span class="sxs-lookup"><span data-stu-id="33c3a-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="33c3a-115">Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão.</span><span class="sxs-lookup"><span data-stu-id="33c3a-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="33c3a-116">Esse fallback recursivo imita as regras de carregamento de recursos do .NET.</span><span class="sxs-lookup"><span data-stu-id="33c3a-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="33c3a-117">Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="33c3a-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="33c3a-118">No campo **valor** , digite o texto localizado que você deseja exibir para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="33c3a-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="33c3a-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33c3a-119">Related topics</span></span>


[<span data-ttu-id="33c3a-120">Personalizando o Portal de Autoatendimento para sua organização</span><span class="sxs-lookup"><span data-stu-id="33c3a-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="33c3a-121">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="33c3a-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="33c3a-122">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="33c3a-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="33c3a-123">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="33c3a-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



