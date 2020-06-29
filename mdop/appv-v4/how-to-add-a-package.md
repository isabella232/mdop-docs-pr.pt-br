---
title: Como adicionar um pacote
description: Como adicionar um pacote
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797917"
---
# <span data-ttu-id="ab34b-103">Como adicionar um pacote</span><span class="sxs-lookup"><span data-stu-id="ab34b-103">How to Add a Package</span></span>


<span data-ttu-id="ab34b-104">Você pode adicionar um pacote do console de gerenciamento do servidor do Application Virtualization das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ab34b-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="ab34b-105">Importar um aplicativo, que cria o pacote automaticamente no processo.</span><span class="sxs-lookup"><span data-stu-id="ab34b-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="ab34b-106">Adicione um pacote manualmente.</span><span class="sxs-lookup"><span data-stu-id="ab34b-106">Add a package manually.</span></span>

<span data-ttu-id="ab34b-107">É recomendável importar aplicativos em vez de adicioná-los manualmente.</span><span class="sxs-lookup"><span data-stu-id="ab34b-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="ab34b-108">Para obter mais informações sobre como importar aplicativos, consulte [como importar um aplicativo](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="ab34b-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="ab34b-109">Para adicionar um pacote manualmente</span><span class="sxs-lookup"><span data-stu-id="ab34b-109">To add a package manually</span></span>**

1.  <span data-ttu-id="ab34b-110">No console de gerenciamento do servidor do Application Virtualization, clique com o botão direito do mouse no nó **pacotes** no painel esquerdo e escolha **novo pacote**.</span><span class="sxs-lookup"><span data-stu-id="ab34b-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="ab34b-111">Na caixa de diálogo **novo pacote** , digite um nome no campo **nome do pacote** .</span><span class="sxs-lookup"><span data-stu-id="ab34b-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="ab34b-112">Procure ou digite um nome de caminho no campo **caminho completo do arquivo de pacote** .</span><span class="sxs-lookup"><span data-stu-id="ab34b-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="ab34b-113">Deve ser um arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="ab34b-113">This must be an SFT file.</span></span>

    <span data-ttu-id="ab34b-114">**Observação**  Se você navegar até o arquivo SFT, substitua o caminho local (como C:\\Arquivos de Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) pelo nome de host estático ou endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab34b-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="ab34b-115">Usar a variável *% SFT \ _SOFTGRIDSERVER%* exige configuração do computador por cliente.</span><span class="sxs-lookup"><span data-stu-id="ab34b-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="ab34b-116">Nas caixas de diálogo que fazem referência a servidores de aplicativos virtuais, você deve usar um local de rede, como o nome de host estático ou o endereço IP do servidor, que os usuários possam acessar.</span><span class="sxs-lookup"><span data-stu-id="ab34b-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="ab34b-117">O arquivo Open Software Descriptor (OSD) do aplicativo pode substituir a variável de espaço reservado *% SFT \ _SOFTGRIDSERER%* com o nome de host estático ou o endereço IP do servidor estático.</span><span class="sxs-lookup"><span data-stu-id="ab34b-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="ab34b-118">Se você deixar a variável de espaço reservado, será necessário definir essa variável em cada computador cliente que acessará esse servidor.</span><span class="sxs-lookup"><span data-stu-id="ab34b-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="ab34b-119">Defina uma variável de usuário ou sistema em cada computador para SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="ab34b-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="ab34b-120">O valor da variável deve ser o nome de host estático ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab34b-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="ab34b-121">Se você definir uma variável, saia da sessão do cliente, desconecte-se do Microsoft Windows e, em seguida, reinicie a sessão em cada computador que tenha uma sessão em execução e o conjunto de variáveis.</span><span class="sxs-lookup"><span data-stu-id="ab34b-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="ab34b-122">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ab34b-122">Click **Next**.</span></span>

5.  <span data-ttu-id="ab34b-123">A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo para o local, caso ainda não tenha feito isso.</span><span class="sxs-lookup"><span data-stu-id="ab34b-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="ab34b-124">Clique em **concluir** depois de verificar as informações.</span><span class="sxs-lookup"><span data-stu-id="ab34b-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="ab34b-125">**Observação**  Se você estiver gerenciando aplicativos em um servidor remoto, na caixa de diálogo seguinte, digite apenas o caminho do arquivo relativo à raiz de conteúdo do servidor.</span><span class="sxs-lookup"><span data-stu-id="ab34b-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="ab34b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab34b-126">Related topics</span></span>


[<span data-ttu-id="ab34b-127">Como importar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="ab34b-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="ab34b-128">Como gerenciar pacotes no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ab34b-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





