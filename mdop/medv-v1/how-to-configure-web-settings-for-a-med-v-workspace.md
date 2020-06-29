---
title: Como definir as configurações da Web de um espaço de trabalho do MED-V
description: Como definir as configurações da Web de um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799998"
---
# <span data-ttu-id="235f4-103">Como definir as configurações da Web de um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="235f4-104">Os sites que só podem ser exibidos em versões mais antigas do Internet Explorer e que não existem no sistema operacional do host podem ser exibidos em versões mais antigas do Internet Explorer dentro do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="235f4-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="235f4-105">O usuário não precisa abrir um navegador no espaço de trabalho do MED-V para exibir os sites da Web especificados.</span><span class="sxs-lookup"><span data-stu-id="235f4-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="235f4-106">O usuário pode abrir um navegador no host e ser redirecionado automaticamente para o espaço de trabalho do MED-V e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="235f4-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="235f4-107">Os procedimentos a seguir descrevem como você pode definir uma lista de regras de navegação na Web para um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="235f4-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="235f4-108">Todos os sites incluídos nas regras podem ser pesquisados no espaço de trabalho do MED-V ou no host, conforme definido pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="235f4-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="235f4-109">Todos os sites não definidos dentro das regras são acessados a partir do ambiente em que foram solicitados.</span><span class="sxs-lookup"><span data-stu-id="235f4-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="235f4-110">No entanto, você também pode configurá-los como um grupo, para ser navegado no espaço de trabalho do MED-V ou no host.</span><span class="sxs-lookup"><span data-stu-id="235f4-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="235f4-111">Observação</span><span class="sxs-lookup"><span data-stu-id="235f4-111">Note</span></span>**  
<span data-ttu-id="235f4-112">As configurações da Web são aplicadas apenas ao Internet Explorer e a outros navegadores.</span><span class="sxs-lookup"><span data-stu-id="235f4-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="235f4-113">Todas as configurações da Web são definidas no módulo de **política** , na guia **Web** .</span><span class="sxs-lookup"><span data-stu-id="235f4-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="235f4-114">Como definir configurações da Web para o espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="235f4-115">Para definir configurações da Web para o espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="235f4-116">Clique no espaço de trabalho do MED-V para ser configurado.</span><span class="sxs-lookup"><span data-stu-id="235f4-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="235f4-117">Marque a caixa **de seleção procurar na lista de URLs definidas na tabela a seguir** para redirecionar o usuário para um navegador dentro do espaço de trabalho ou host do MED-V, quando o usuário navegar para uma URL que está em conformidade com as regras da Web especificadas.</span><span class="sxs-lookup"><span data-stu-id="235f4-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="235f4-118">Clique em uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="235f4-118">Click one of the following:</span></span>

    -   <span data-ttu-id="235f4-119">**No espaço de trabalho**— Redirecione para um navegador no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="235f4-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="235f4-120">**No host**— Redirecione para um navegador no host.</span><span class="sxs-lookup"><span data-stu-id="235f4-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="235f4-121">Marque a caixa de seleção **procurar todas as outras URLs** para redirecionar todas as URLs excluídas das regras da Web para o host ou o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="235f4-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="235f4-122">Clique em uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="235f4-122">Click one of the following:</span></span>

    -   <span data-ttu-id="235f4-123">**No espaço de trabalho**, redirecione todas as outras URLs para um navegador no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="235f4-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="235f4-124">**No host**— redirecione todas as outras URLs para um navegador no host.</span><span class="sxs-lookup"><span data-stu-id="235f4-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="235f4-125">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="235f4-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="235f4-126">Como adicionar uma regra da Web</span><span class="sxs-lookup"><span data-stu-id="235f4-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="235f4-127">Para adicionar uma regra da Web</span><span class="sxs-lookup"><span data-stu-id="235f4-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="235f4-128">Marque a caixa **de seleção procurar na lista de URLs definida na tabela a seguir** para habilitar as regras de navegação na Web.</span><span class="sxs-lookup"><span data-stu-id="235f4-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="235f4-129">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="235f4-129">Click **Add**.</span></span>

    <span data-ttu-id="235f4-130">Uma nova regra da Web é adicionada.</span><span class="sxs-lookup"><span data-stu-id="235f4-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="235f4-131">Configure as propriedades da regra da Web conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="235f4-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="235f4-132">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="235f4-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="235f4-133">Propriedades da Web do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="235f4-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="235f4-134">Property</span></span></th>
<th align="left"><span data-ttu-id="235f4-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="235f4-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="235f4-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="235f4-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="235f4-137">Sufixo do domínio </strong> – o acesso a qualquer endereço de host que termina com o sufixo especificado na <strong> </strong> propriedade valor e é definido de acordo com a opção definida na <strong> navegação na Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="235f4-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="235f4-138">Prefixo </strong> de IP – acesso a qualquer endereço IP completo ou parcial no intervalo do prefixo especificado na <strong> </strong> propriedade valor e é definido de acordo com a opção definida na navegação na <strong> Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="235f4-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="235f4-139">Todos os endereços locais </strong> – acesso a todos os endereços sem um &#39;. &#39; e é definido de acordo com a opção definida na <strong> navegação na Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="235f4-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="235f4-140">Valor</span><span class="sxs-lookup"><span data-stu-id="235f4-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="235f4-141">Se <strong> sufixo </strong> do domínio for selecionado na <strong> </strong> propriedade tipo, insira um sufixo de domínio.</span><span class="sxs-lookup"><span data-stu-id="235f4-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="235f4-142">Observação</span><span class="sxs-lookup"><span data-stu-id="235f4-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="235f4-143">Não insira &quot; \* &quot; antes do sufixo.</span><span class="sxs-lookup"><span data-stu-id="235f4-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="235f4-144">Sufixos de domínio também dão suporte a aliases.</span><span class="sxs-lookup"><span data-stu-id="235f4-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="235f4-145">Se prefixo IP estiver selecionado na <strong> propriedade tipo </strong> , insira um endereço IP completo ou parcial.</span><span class="sxs-lookup"><span data-stu-id="235f4-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="235f4-146">Como excluir uma regra da Web</span><span class="sxs-lookup"><span data-stu-id="235f4-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="235f4-147">Para excluir uma regra da Web</span><span class="sxs-lookup"><span data-stu-id="235f4-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="235f4-148">No painel **da Web** , selecione a regra da Web a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="235f4-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="235f4-149">Clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="235f4-149">Click **Remove**.</span></span>

    <span data-ttu-id="235f4-150">A regra da Web é excluída.</span><span class="sxs-lookup"><span data-stu-id="235f4-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="235f4-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="235f4-151">Related topics</span></span>


[<span data-ttu-id="235f4-152">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="235f4-153">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="235f4-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









