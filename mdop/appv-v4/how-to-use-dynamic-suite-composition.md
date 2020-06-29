---
title: Como usar a Dynamic Suite Composition
description: Como usar a Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796921"
---
# <span data-ttu-id="8c58b-103">Como usar a Dynamic Suite Composition</span><span class="sxs-lookup"><span data-stu-id="8c58b-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="8c58b-104">A composição do pacote dinâmico na virtualização de aplicativos permite que você defina um aplicativo como dependente de outro aplicativo, como middleware ou um plug-in.</span><span class="sxs-lookup"><span data-stu-id="8c58b-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="8c58b-105">Isso permite que o aplicativo interaja com o middleware ou plug-in no ambiente virtual, onde geralmente isso é evitado.</span><span class="sxs-lookup"><span data-stu-id="8c58b-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="8c58b-106">Isso é útil porque um pacote de aplicativo secundário pode ser usado com vários outros aplicativos, chamados de *aplicativos principais*, que permitem que cada aplicativo primário faça referência ao mesmo pacote secundário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="8c58b-107">Você pode usar a composição do pacote dinâmico ao sequenciar aplicativos que dependem de plug-ins, como controles ActiveX ou para aplicativos que dependem do middleware, como OLE DB ou JRE (Java Runtime Environment).</span><span class="sxs-lookup"><span data-stu-id="8c58b-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="8c58b-108">Se cada aplicativo que usou esses componentes dependentes requer sequenciamento, incluindo os componentes, as atualizações para esses componentes exigem a resequenciação de todos os aplicativos principais.</span><span class="sxs-lookup"><span data-stu-id="8c58b-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="8c58b-109">Se você sequenciar os aplicativos principais sem os componentes e, em seguida, sequenciar o middleware ou plug-in como um pacote secundário, somente o pacote secundário deverá ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="8c58b-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="8c58b-110">Uma vantagem dessa abordagem é que ele reduz o tamanho dos pacotes primários.</span><span class="sxs-lookup"><span data-stu-id="8c58b-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="8c58b-111">Outra vantagem é que ele oferece melhor controle das permissões de acesso nos aplicativos secundários.</span><span class="sxs-lookup"><span data-stu-id="8c58b-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="8c58b-112">Observe que o aplicativo secundário pode ser transmitido da maneira normal e não precisa ser totalmente armazenado em cache para ser executado.</span><span class="sxs-lookup"><span data-stu-id="8c58b-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="8c58b-113">Um pacote principal pode ter mais de um pacote secundário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="8c58b-114">No entanto, apenas um nível de dependência tem suporte, portanto, não é possível definir um pacote secundário como dependente de outro pacote secundário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="8c58b-115">Além disso, o aplicativo secundário só pode ser middleware ou um plug-in e não pode ser outro produto de software completo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="8c58b-116">Se você planeja fazer vários aplicativos principais dependentes de um único produto de middleware, certifique-se de testar essa configuração para determinar o efeito potencial sobre o desempenho do sistema antes de implantá-lo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="8c58b-117">**Importante**  As dependências do pacote podem ser especificadas como obrigatórias para um aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="8c58b-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="8c58b-118">Se um pacote secundário estiver sinalizado como obrigatório e não puder ser acessado por algum motivo durante o carregamento, a carga do pacote secundário falhará.</span><span class="sxs-lookup"><span data-stu-id="8c58b-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="8c58b-119">Além disso, o aplicativo principal falhará quando o usuário tentar iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="8c58b-120">Você pode usar os procedimentos a seguir para criar um pacote secundário, seja para um plug-in ou um componente middleware e, em seguida, pode usar o procedimento final para definir a dependência no arquivo OSD do pacote secundário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="8c58b-121">Para criar um pacote secundário para um plug-in usando a composição do pacote dinâmico</span><span class="sxs-lookup"><span data-stu-id="8c58b-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="8c58b-122">Em um computador de sequenciamento que está configurado com uma imagem limpa, instale o Application Virtualization Sequencer e salve o estado do computador.</span><span class="sxs-lookup"><span data-stu-id="8c58b-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="8c58b-123">Sequenciar o aplicativo principal e salvar o pacote na pasta de conteúdo no servidor.</span><span class="sxs-lookup"><span data-stu-id="8c58b-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="8c58b-124">Restaure o computador de sequenciamento para seu estado salvo da etapa 1.</span><span class="sxs-lookup"><span data-stu-id="8c58b-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="8c58b-125">Instale e configure o aplicativo principal localmente no computador de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8c58b-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="8c58b-126">**Importante**  Você deve especificar uma nova raiz de pacote para o pacote secundário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="8c58b-127">Inicie a fase de monitoramento do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="8c58b-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="8c58b-128">Instale o plug-in no computador de sequenciamento e configure-o conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="8c58b-129">Abra o aplicativo principal e confirme se o plug-in está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8c58b-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="8c58b-130">No console do sequenciador, crie um aplicativo fictício para representar o pacote secundário que conterá o plug-in e selecione um ícone.</span><span class="sxs-lookup"><span data-stu-id="8c58b-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="8c58b-131">Salve o pacote na pasta de conteúdo no servidor.</span><span class="sxs-lookup"><span data-stu-id="8c58b-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="8c58b-132">**Observação**  Para auxiliar no gerenciamento de pacotes secundários, é recomendável que o nome do pacote inclua o termo "pacote secundário" para enfatizar que esse é um pacote que não funcionará como um aplicativo autônomo, por exemplo, **\ [plug-in name \] pacote secundário**.</span><span class="sxs-lookup"><span data-stu-id="8c58b-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="8c58b-133">Para criar um pacote secundário para middleware usando a composição do pacote dinâmico</span><span class="sxs-lookup"><span data-stu-id="8c58b-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="8c58b-134">Em um computador de sequenciamento que está configurado com uma imagem limpa, instale o Application Virtualization Sequencer e salve o estado do computador.</span><span class="sxs-lookup"><span data-stu-id="8c58b-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="8c58b-135">Instale o middleware localmente no computador de sequenciamento e configure-o.</span><span class="sxs-lookup"><span data-stu-id="8c58b-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="8c58b-136">Sequenciar o aplicativo principal e salvar o pacote na pasta de conteúdo no servidor.</span><span class="sxs-lookup"><span data-stu-id="8c58b-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="8c58b-137">Restaure o computador de sequenciamento para seu estado salvo da etapa 1.</span><span class="sxs-lookup"><span data-stu-id="8c58b-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="8c58b-138">Inicie o sequenciador para criar um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="8c58b-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="8c58b-139">Inicie a fase de monitoramento do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="8c58b-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="8c58b-140">Instale o aplicativo middleware no computador de sequenciamento e configure-o como em uma instalação típica.</span><span class="sxs-lookup"><span data-stu-id="8c58b-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="8c58b-141">Conclua o processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8c58b-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="8c58b-142">Salve o pacote na pasta de conteúdo no servidor.</span><span class="sxs-lookup"><span data-stu-id="8c58b-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="8c58b-143">**Observação**  Para auxiliar no gerenciamento de pacotes secundários, é recomendável que o nome do pacote inclua o termo "pacote secundário" para enfatizar que esse é um pacote que não funcionará como um aplicativo autônomo, por exemplo, o **pacote secundário do \ [nome do middleware \]**.</span><span class="sxs-lookup"><span data-stu-id="8c58b-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="8c58b-144">Para definir a dependência no pacote primário</span><span class="sxs-lookup"><span data-stu-id="8c58b-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="8c58b-145">No servidor, abra o arquivo OSD do pacote secundário para edição.</span><span class="sxs-lookup"><span data-stu-id="8c58b-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="8c58b-146">(É uma boa ideia usar um editor de XML para fazer alterações no arquivo OSD; no entanto, você pode usar o bloco de notas como uma alternativa.)</span><span class="sxs-lookup"><span data-stu-id="8c58b-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="8c58b-147">Copie a linha **href de CodeBase** do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="8c58b-148">Abra o arquivo OSD do pacote primário para edição.</span><span class="sxs-lookup"><span data-stu-id="8c58b-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="8c58b-149">Insira a <strong> &lt; marca dependências &gt; </strong> após a marca de fechamento da \*\* &lt; /ENVLIST &gt; \*\* no final da seção \*\* &lt; VIRTUALENV &gt; \*\* , logo antes da marca \*\* &lt; /VIRTUALENV &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="8c58b-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="8c58b-150">Cole a linha **href de CodeBase** do pacote secundário após a marca de \*\* &lt; dependências &gt; \*\* que você acabou de criar.</span><span class="sxs-lookup"><span data-stu-id="8c58b-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="8c58b-151">Se o pacote secundário for um pacote obrigatório, o que significa que ele deve ser iniciado antes do pacote primário ser iniciado, adicione a propriedade **obrigatória = "true"** dentro da marca **codebase** .</span><span class="sxs-lookup"><span data-stu-id="8c58b-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="8c58b-152">Se não for obrigatório, a propriedade poderá ser omitida.</span><span class="sxs-lookup"><span data-stu-id="8c58b-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="8c58b-153">Feche a marca de \*\* &lt; dependências &gt; \*\* inserindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8c58b-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="8c58b-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="8c58b-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="8c58b-155">Examine as alterações feitas no arquivo OSD e salve e feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="8c58b-156">O exemplo a seguir mostra como a seção adicionada deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="8c58b-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="8c58b-157">Os valores de marca mostrados aqui são apenas por exemplo.</span><span class="sxs-lookup"><span data-stu-id="8c58b-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="8c58b-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="8c58b-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="8c58b-159">…</span><span class="sxs-lookup"><span data-stu-id="8c58b-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="8c58b-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="8c58b-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="8c58b-161">Se o pacote secundário tiver entradas na seção \*\* &lt; ENVLIST &gt; \*\* do arquivo OSD, você deverá copiar essas entradas para a mesma seção no pacote primário.</span><span class="sxs-lookup"><span data-stu-id="8c58b-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="8c58b-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c58b-162">Related topics</span></span>


[<span data-ttu-id="8c58b-163">Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="8c58b-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





