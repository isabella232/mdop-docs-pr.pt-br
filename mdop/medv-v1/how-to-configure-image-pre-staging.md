---
title: Como definir a pré-configuração de imagens
description: Como definir a pré-configuração de imagens
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799866"
---
# <span data-ttu-id="724e7-103">Como definir a pré-configuração de imagens</span><span class="sxs-lookup"><span data-stu-id="724e7-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="724e7-104">**Observação**  Pré-preparação de imagem é útil somente para o download inicial da imagem.</span><span class="sxs-lookup"><span data-stu-id="724e7-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="724e7-105">Não há suporte para a atualização de imagem.</span><span class="sxs-lookup"><span data-stu-id="724e7-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="724e7-106">Como definir a pré-configuração de imagens</span><span class="sxs-lookup"><span data-stu-id="724e7-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="724e7-107">Para configurar o pré-teste de imagem</span><span class="sxs-lookup"><span data-stu-id="724e7-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="724e7-108">No computador cliente, no diretório de armazenamento de imagens, crie uma pasta para a imagem de pré-teste e nomeie-a em *imagens do MED-V*.</span><span class="sxs-lookup"><span data-stu-id="724e7-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="724e7-109">**Observação**  Essa pasta deve ser chamada *de imagens do MED-V*.</span><span class="sxs-lookup"><span data-stu-id="724e7-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="724e7-110">Na pasta de imagens do MED-V, crie uma subpasta e nomeie-a *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="724e7-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="724e7-111">**Observação**  Essa pasta deve ser chamada de *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="724e7-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="724e7-112">Para aplicar a segurança da ACL (listas de controle de acesso) à pasta de *imagens do MED-V* , defina a seguinte ACL:</span><span class="sxs-lookup"><span data-stu-id="724e7-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="724e7-113">Usuários do NT AUTHORITY\\Authenticated: (OI) (CI) (acesso especial:)</span><span class="sxs-lookup"><span data-stu-id="724e7-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="724e7-114">ARQUIVO \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="724e7-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="724e7-115">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="724e7-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="724e7-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="724e7-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="724e7-117">**Observação**  É recomendável aplicar a segurança de ACL à pasta de *imagens do MED-V* .</span><span class="sxs-lookup"><span data-stu-id="724e7-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="724e7-118">Para aplicar a segurança de ACL à pasta *PrestagedImages* , defina a seguinte ACL:</span><span class="sxs-lookup"><span data-stu-id="724e7-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="724e7-119">Usuários do NT AUTHORITY\\Authenticated: (OI) (CI) (acesso especial:)</span><span class="sxs-lookup"><span data-stu-id="724e7-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="724e7-120">LEIA \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="724e7-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="724e7-121">SINCRONIZAR</span><span class="sxs-lookup"><span data-stu-id="724e7-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="724e7-122">ARQUIVO \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="724e7-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="724e7-123">ARQUIVO \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="724e7-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="724e7-124">ARQUIVO \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="724e7-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="724e7-125">ARQUIVO \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="724e7-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="724e7-126">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="724e7-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="724e7-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="724e7-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="724e7-128">**Observação**  É recomendável aplicar a segurança de ACL à pasta *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="724e7-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="724e7-129">Empurre os arquivos de imagem (CKM e INDEX Files) para a pasta *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="724e7-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="724e7-130">**Observação**  Depois que os arquivos de imagem forem enviados para a pasta de pré-teste, é recomendável executar uma verificação de integridade de dados e marcá-los como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="724e7-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="724e7-131">Inclua o seguinte parâmetro na instalação do cliente MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V images"*.</span><span class="sxs-lookup"><span data-stu-id="724e7-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="724e7-132">Como atualizar o local de pré-teste</span><span class="sxs-lookup"><span data-stu-id="724e7-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="724e7-133">Para atualizar o local de pré-teste</span><span class="sxs-lookup"><span data-stu-id="724e7-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="724e7-134">A chave do registro, *PrestagedImagesPath*, aponta para o local da imagem padrão.</span><span class="sxs-lookup"><span data-stu-id="724e7-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="724e7-135">Ele está localizado no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="724e7-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="724e7-136">Em x86-</span><span class="sxs-lookup"><span data-stu-id="724e7-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="724e7-137">Em um x64-</span><span class="sxs-lookup"><span data-stu-id="724e7-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="724e7-138">Se a imagem estiver em um local diferente, altere o caminho.</span><span class="sxs-lookup"><span data-stu-id="724e7-138">If the image is in a different location, change the path.</span></span>

 

 





