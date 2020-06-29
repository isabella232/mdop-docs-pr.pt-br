---
title: Como adicionar uma versão de pacote
description: Como adicionar uma versão de pacote
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797918"
---
# <span data-ttu-id="ba761-103">Como adicionar uma versão de pacote</span><span class="sxs-lookup"><span data-stu-id="ba761-103">How to Add a Package Version</span></span>


<span data-ttu-id="ba761-104">No console de gerenciamento do servidor do Application Virtualization, ao resequenciar um pacote, você pode usar o procedimento a seguir para adicionar a nova versão aos seus servidores para transmissão.</span><span class="sxs-lookup"><span data-stu-id="ba761-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="ba761-105">**Observação**  Quando você atualiza um pacote com uma nova versão, pode deixar a versão existente no lugar ou excluí-la e deixar apenas a mais recente.</span><span class="sxs-lookup"><span data-stu-id="ba761-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="ba761-106">Talvez você queira deixar a versão antiga em vigor para a compatibilidade com documentos herdados ou para poder testar a nova versão antes de disponibilizá-la para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="ba761-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="ba761-107">Para adicionar uma versão de pacote</span><span class="sxs-lookup"><span data-stu-id="ba761-107">To add a package version</span></span>**

1.  <span data-ttu-id="ba761-108">Copie o novo arquivo SFT para a pasta de conteúdo do servidor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ba761-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="ba761-109">Se o resequenciamento não adicionar alterações aos arquivos Open Software Descriptor (OSD), Icon (ICO) ou Sequencer Project (SPRJ), você não precisará copiá-los.</span><span class="sxs-lookup"><span data-stu-id="ba761-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="ba761-110">Você pode incluir esses arquivos se desejar que todos os arquivos exibam a mesma data.</span><span class="sxs-lookup"><span data-stu-id="ba761-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="ba761-111">No painel esquerdo do console de gerenciamento do servidor do Application Virtualization, expanda o nó **pacotes** .</span><span class="sxs-lookup"><span data-stu-id="ba761-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="ba761-112">Clique com o botão direito do mouse no pacote que você deseja atualizar e escolha **Adicionar versão**.</span><span class="sxs-lookup"><span data-stu-id="ba761-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="ba761-113">Na caixa de diálogo **Adicionar versão do pacote** , procure ou digite o nome do caminho para o novo arquivo do aplicativo no campo **caminho completo do arquivo de pacote** .</span><span class="sxs-lookup"><span data-stu-id="ba761-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="ba761-114">Deve ser um arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="ba761-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="ba761-115">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ba761-115">Click **Next**.</span></span>

6.  <span data-ttu-id="ba761-116">A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo, caso ainda não tenha feito isso.</span><span class="sxs-lookup"><span data-stu-id="ba761-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="ba761-117">Clique em **concluir** depois de verificar as informações.</span><span class="sxs-lookup"><span data-stu-id="ba761-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="ba761-118">A nova versão agora está completa e pronta para transmitir.</span><span class="sxs-lookup"><span data-stu-id="ba761-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="ba761-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba761-119">Related topics</span></span>


[<span data-ttu-id="ba761-120">Como excluir um pacote</span><span class="sxs-lookup"><span data-stu-id="ba761-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="ba761-121">Como gerenciar pacotes no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ba761-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





