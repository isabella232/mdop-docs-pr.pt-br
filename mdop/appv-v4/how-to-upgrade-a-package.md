---
title: Como fazer upgrade de um pacote
description: Como fazer upgrade de um pacote
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796938"
---
# <span data-ttu-id="61c95-103">Como fazer upgrade de um pacote</span><span class="sxs-lookup"><span data-stu-id="61c95-103">How to Upgrade a Package</span></span>


<span data-ttu-id="61c95-104">O processo para uma atualização automática é o mesmo para adicionar uma versão do pacote no console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="61c95-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="61c95-105">Uma atualização automática é realizada quando você resequencia o aplicativo em um pacote existente.</span><span class="sxs-lookup"><span data-stu-id="61c95-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="61c95-106">Em seguida, você pode adicionar essa nova versão aos seus servidores para transmissão.</span><span class="sxs-lookup"><span data-stu-id="61c95-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="61c95-107">Quando você atualiza um pacote com uma nova versão, pode deixar a versão existente no lugar ou excluí-la e deixar apenas a mais recente.</span><span class="sxs-lookup"><span data-stu-id="61c95-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="61c95-108">Talvez você queira deixar a versão antiga em vigor para a compatibilidade com documentos herdados ou para poder testar a nova versão antes de disponibilizá-la para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="61c95-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="61c95-109">Para atualizar um pacote automaticamente</span><span class="sxs-lookup"><span data-stu-id="61c95-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="61c95-110">Copie o novo arquivo SFT para a pasta de conteúdo do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="61c95-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="61c95-111">**Observação**  Se a resequenciagem não adicionou recursos que alteraram os arquivos Open Software Descriptor (OSD), Icon (ICO) ou Sequencer Project (SPRJ), você não precisará copiá-los.</span><span class="sxs-lookup"><span data-stu-id="61c95-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="61c95-112">Você pode incluir esses arquivos se desejar que todos esses arquivos exibam a mesma data.</span><span class="sxs-lookup"><span data-stu-id="61c95-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="61c95-113">No painel esquerdo do console de gerenciamento do servidor do Application Virtualization, expanda **pacotes**.</span><span class="sxs-lookup"><span data-stu-id="61c95-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="61c95-114">Clique com o botão direito do mouse no pacote que você deseja atualizar e selecione **Adicionar versão**.</span><span class="sxs-lookup"><span data-stu-id="61c95-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="61c95-115">Na caixa de diálogo **Adicionar versão do pacote** , procure ou digite o nome do caminho completo da nova versão do aplicativo no **caminho completo do campo arquivo** .</span><span class="sxs-lookup"><span data-stu-id="61c95-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="61c95-116">Deve ser um arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="61c95-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="61c95-117">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="61c95-117">Click **Next**.</span></span>

6.  <span data-ttu-id="61c95-118">A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo, caso ainda não tenha feito isso.</span><span class="sxs-lookup"><span data-stu-id="61c95-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="61c95-119">Clique em **concluir** depois de verificar as informações.</span><span class="sxs-lookup"><span data-stu-id="61c95-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="61c95-120">A nova versão agora está completa e pronta para transmitir.</span><span class="sxs-lookup"><span data-stu-id="61c95-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="61c95-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61c95-121">Related topics</span></span>


[<span data-ttu-id="61c95-122">Como gerenciar pacotes no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="61c95-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





