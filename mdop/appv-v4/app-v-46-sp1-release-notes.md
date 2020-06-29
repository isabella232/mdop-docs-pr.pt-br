---
title: Notas de versão do App-V 4.6 SP1
description: Notas de versão do App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797605"
---
# <span data-ttu-id="1bc03-103">Notas de versão do App-V 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="1bc03-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="1bc03-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="1bc03-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="1bc03-105">**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="1bc03-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="1bc03-106">Estas notas da versão contêm informações que ajudam você a instalar com êxito o Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="1bc03-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="1bc03-107">Este documento contém informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="1bc03-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="1bc03-108">Se houver uma diferença entre essas notas de versão e outras documentações do App-V, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="1bc03-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="1bc03-109">Proteger contra vulnerabilidades e vírus de segurança</span><span class="sxs-lookup"><span data-stu-id="1bc03-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="1bc03-110">Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="1bc03-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="1bc03-111">Para obter mais informações, consulte o [site de segurança da Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="1bc03-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="1bc03-112">Problemas conhecidos com o Application Virtualization 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="1bc03-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="1bc03-113">Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="1bc03-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="1bc03-114">Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto.</span><span class="sxs-lookup"><span data-stu-id="1bc03-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="1bc03-115">Quando isso for possível, esses problemas serão resolvidos em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="1bc03-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="1bc03-116">O caminho de SPRT será perdido se não terminar na barra (/)</span><span class="sxs-lookup"><span data-stu-id="1bc03-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="1bc03-117">Quando o caminho em HREF em um modelo de projeto não termina com uma barra ( **/** ), o href gerado não inclui o caminho.</span><span class="sxs-lookup"><span data-stu-id="1bc03-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="1bc03-118">Isso ocorre quando o usuário manipula manualmente o arquivo **. SPRT** .</span><span class="sxs-lookup"><span data-stu-id="1bc03-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="1bc03-119">Se você usar o sequenciador, ele sempre adiciona a barra diagonal ( **/** ) após o caminho.</span><span class="sxs-lookup"><span data-stu-id="1bc03-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="1bc03-120">SOLUÇÃO alternativa certifique-se de que o HREF tenha uma barra de avanço ( **/** ).</span><span class="sxs-lookup"><span data-stu-id="1bc03-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="1bc03-121">Nome da pasta do usuário não corresponde ao nome do pacote</span><span class="sxs-lookup"><span data-stu-id="1bc03-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="1bc03-122">As pastas que contêm arquivos. pkg global e de usuário não incluem mais o nome do pacote.</span><span class="sxs-lookup"><span data-stu-id="1bc03-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="1bc03-123">Anteriormente, o cliente App-V usado para usar a pasta raiz do pacote 8,3 nome curto como parte do nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="1bc03-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="1bc03-124">Isso permite que você o identifique facilmente.</span><span class="sxs-lookup"><span data-stu-id="1bc03-124">This lets you easily identify it.</span></span> <span data-ttu-id="1bc03-125">Ao usar o sequenciador do App-V 4,6 SP1, a pasta raiz do pacote 8,3 nomes curtos agora são cadeias de caracteres aleatórias.</span><span class="sxs-lookup"><span data-stu-id="1bc03-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="1bc03-126">Isso torna difícil identificar as pastas que contêm os arquivos **. pkg** do pacote no computador que está executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="1bc03-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="1bc03-127">SOLUÇÃO alternativa use um dos seguintes métodos para identificar mais facilmente essas pastas do pacote:</span><span class="sxs-lookup"><span data-stu-id="1bc03-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="1bc03-128">Ao criar o pacote usando o sequenciador, especifique um nome de pasta que siga a Convenção de nomenclatura do 8,3 para a pasta de aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="1bc03-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="1bc03-129">Esse nome será usado como parte do nome da pasta do usuário como era o caso no App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="1bc03-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="1bc03-130">O arquivo. sprj agora contém uma marca que exibe a cadeia de caracteres que é usada como o início do nome da pasta do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bc03-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="1bc03-131">Você pode usar o elemento **ShortName** do elemento **PACKAGEROOTFOLDER** para determinar o nome.</span><span class="sxs-lookup"><span data-stu-id="1bc03-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="1bc03-132">Executando o App-V 4,6 SP1 em computadores com mais de 64 processadores</span><span class="sxs-lookup"><span data-stu-id="1bc03-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="1bc03-133">Quando você executa o App-V 4,6 SP1 em computadores com mais de 64 processadores instalados, o cliente App-V falha.</span><span class="sxs-lookup"><span data-stu-id="1bc03-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="1bc03-134">SOLUÇÃO alternativa nenhum.</span><span class="sxs-lookup"><span data-stu-id="1bc03-134">WORKAROUND None.</span></span> <span data-ttu-id="1bc03-135">Não há suporte para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="1bc03-135">This configuration is not supported.</span></span> <span data-ttu-id="1bc03-136">Você deve executar o App-V 4,6 SP1on computadores com menos de 64 processadores.</span><span class="sxs-lookup"><span data-stu-id="1bc03-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="1bc03-137">A atualização do Application Virtualization 4,6 SP1 não é oferecida em todas as localidades que usam o Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="1bc03-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="1bc03-138">Quando você usa o Microsoft Update, a atualização do App-V 4,6 SP1 não está disponível para as seguintes localidades de idioma:</span><span class="sxs-lookup"><span data-stu-id="1bc03-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="1bc03-139">Cazaque</span><span class="sxs-lookup"><span data-stu-id="1bc03-139">Kazakh</span></span>

-   <span data-ttu-id="1bc03-140">Híndi</span><span class="sxs-lookup"><span data-stu-id="1bc03-140">Hindi</span></span>

-   <span data-ttu-id="1bc03-141">Sérvio-cirílico</span><span class="sxs-lookup"><span data-stu-id="1bc03-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="1bc03-142">SOLUÇÃO alternativa se você estiver usando o Microsoft Windows Server Update Services (WSUS), use a versão em inglês da atualização ou baixe a atualização do catálogo do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="1bc03-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="1bc03-143">Após expandir o pacote pai, você não pode sequenciar um plug-in com componentes lado a lado</span><span class="sxs-lookup"><span data-stu-id="1bc03-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="1bc03-144">Quando você expande um pacote pai usando **ferramentas**  /  **expandir pacote para o sistema local** no console do App-V Sequencer e sequenciar um plug-in com componentes lado a lado, um erro de instalação é retornado.</span><span class="sxs-lookup"><span data-stu-id="1bc03-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="1bc03-145">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1bc03-145">For example:</span></span>

-   **<span data-ttu-id="1bc03-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="1bc03-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="1bc03-147">Isso ocorre quando o sequenciador grava o componente lado a lado no registro, mas não limpa o valor da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="1bc03-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="1bc03-148">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="1bc03-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="1bc03-149">SOLUÇÃO alternativa após expandir o pacote pai no computador que está executando o sequenciador, você precisa excluir o valor da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="1bc03-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="1bc03-150">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="1bc03-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="1bc03-151">Depois de excluir o valor, Sequence o plug-in.</span><span class="sxs-lookup"><span data-stu-id="1bc03-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="1bc03-152">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="1bc03-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="1bc03-153">Este documento é fornecido "como está".</span><span class="sxs-lookup"><span data-stu-id="1bc03-153">This document is provided “as-is”.</span></span> <span data-ttu-id="1bc03-154">As informações e os modos de exibição expressos neste documento, como URLs e outras referências de site da Internet, podem mudar sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="1bc03-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="1bc03-155">Você assume o risco de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="1bc03-155">You bear the risk of using it.</span></span>

<span data-ttu-id="1bc03-156">Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios.</span><span class="sxs-lookup"><span data-stu-id="1bc03-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="1bc03-157">Nenhuma associação ou conexão real é intencional ou deve ser inferida.</span><span class="sxs-lookup"><span data-stu-id="1bc03-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="1bc03-158">Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bc03-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="1bc03-159">Você pode copiar e usar este documento para fins de referência interna.</span><span class="sxs-lookup"><span data-stu-id="1bc03-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="1bc03-160">Você pode modificar esse documento para suas finalidades de referência internas.</span><span class="sxs-lookup"><span data-stu-id="1bc03-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="1bc03-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bc03-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="1bc03-162">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="1bc03-162">All other trademarks are property of their respective owners.</span></span>

 

 





