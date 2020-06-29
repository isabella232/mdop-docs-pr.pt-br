---
title: Como adicionar ou atualizar pacotes usando o Console de Gerenciamento
description: Como adicionar ou atualizar pacotes usando o Console de Gerenciamento
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796507"
---
# <span data-ttu-id="000e8-103">Como adicionar ou atualizar pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="000e8-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="000e8-104">Você pode o procedimento a seguir para adicionar ou atualizar um pacote para o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="000e8-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="000e8-105">Para atualizar um pacote que já existe no console de gerenciamento, use as etapas a seguir e importe o pacote atualizado usando o mesmo **nome**do pacote.</span><span class="sxs-lookup"><span data-stu-id="000e8-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="000e8-106">Para adicionar um pacote ao console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="000e8-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="000e8-107">Clique na guia **pacotes** no painel de navegação da exibição do console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="000e8-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="000e8-108">O console exibe a lista de pacotes que foram adicionados ao servidor juntamente com as informações de status sobre cada pacote.</span><span class="sxs-lookup"><span data-stu-id="000e8-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="000e8-109">Quando um pacote é selecionado, informações detalhadas sobre o pacote são exibidas no painel **pacotes** .</span><span class="sxs-lookup"><span data-stu-id="000e8-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="000e8-110">Clique na caixa de listagem suspensa **desagrupada** e especifique como os pacotes devem ser exibidos no console.</span><span class="sxs-lookup"><span data-stu-id="000e8-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="000e8-111">Você também pode clicar no cabeçalho da coluna associada para classificar os pacotes.</span><span class="sxs-lookup"><span data-stu-id="000e8-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="000e8-112">Para especificar o pacote que você deseja adicionar, clique em **Adicionar ou atualizar pacotes**.</span><span class="sxs-lookup"><span data-stu-id="000e8-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="000e8-113">Digite o caminho completo para o pacote que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="000e8-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="000e8-114">Use o formato de caminho UNC ou HTTP, por exemplo, **\\\\servername\\sharename\\foldername\\packagename.AppV** ou **http://server.1234/file.appv** , e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="000e8-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="000e8-115">**Importante**  Você deve selecionar um pacote com a extensão de nome de arquivo **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="000e8-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="000e8-116">A página exibe a mensagem de status \*\*adicionando &lt; PackageName &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="000e8-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="000e8-117">Clique em **importar status** para verificar o status de um pacote importado.</span><span class="sxs-lookup"><span data-stu-id="000e8-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="000e8-118">Clique em **OK** para adicionar o pacote e feche a página **Adicionar pacote** .</span><span class="sxs-lookup"><span data-stu-id="000e8-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="000e8-119">Se houve um erro durante a importação, clique em **detalhes** na página **importação de pacote** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="000e8-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="000e8-120">O pacote recém-adicionado agora está disponível no painel **pacotes** .</span><span class="sxs-lookup"><span data-stu-id="000e8-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="000e8-121">Clique em **fechar** para fechar a página **Adicionar ou atualizar pacotes** .</span><span class="sxs-lookup"><span data-stu-id="000e8-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="000e8-122">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="000e8-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="000e8-123">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="000e8-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="000e8-124">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="000e8-124">Got an App-V issue?</span></span>** <span data-ttu-id="000e8-125">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="000e8-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="000e8-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="000e8-126">Related topics</span></span>


[<span data-ttu-id="000e8-127">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="000e8-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





