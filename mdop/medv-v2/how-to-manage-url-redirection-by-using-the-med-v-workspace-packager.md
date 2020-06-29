---
title: Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V
description: Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799548"
---
# <span data-ttu-id="346d4-103">Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="346d4-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="346d4-104">Você pode usar o pacote do espaço de trabalho do MED-V para gerenciar o redirecionamento de URL no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="346d4-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="346d4-105">Para gerenciar o redirecionamento de endereço Web em um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="346d4-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="346d4-106">Para abrir o **pacote do espaço de trabalho do MED-V**, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="346d4-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="346d4-107">No painel principal do **pacote de espaço de trabalho do MED-V** , clique em **gerenciar redirecionamento da Web**.</span><span class="sxs-lookup"><span data-stu-id="346d4-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="346d4-108">Na janela **gerenciar redirecionamento da Web** , você pode digitar, colar ou importar uma lista das URLs redirecionadas para o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="346d4-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="346d4-109">Observação</span><span class="sxs-lookup"><span data-stu-id="346d4-109">Note</span></span>**  
    <span data-ttu-id="346d4-110">O redirecionamento de URL no MED-V só oferece suporte aos protocolos HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="346d4-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="346d4-111">O MED-V não oferece suporte para FTP ou outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="346d4-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="346d4-112">Clique em **salvar como...**</span><span class="sxs-lookup"><span data-stu-id="346d4-112">Click **Save as…**</span></span> <span data-ttu-id="346d4-113">para salvar os arquivos de redirecionamento de URL atualizados na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="346d4-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="346d4-114">O MED-V cria um arquivo de registro que contém as informações atualizadas de redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="346d4-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="346d4-115">Implante a chave do registro atualizada usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="346d4-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="346d4-116">Para obter mais informações sobre como usar a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="346d4-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="346d4-117">O MED-V também cria um script do Windows PowerShell na pasta especificada que você pode usar para recriar o pacote do espaço de trabalho do MED-V atualizado.</span><span class="sxs-lookup"><span data-stu-id="346d4-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="346d4-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="346d4-118">Related topics</span></span>


[<span data-ttu-id="346d4-119">Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V</span><span class="sxs-lookup"><span data-stu-id="346d4-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="346d4-120">Gerenciar o redirecionamento da URL da MED-V</span><span class="sxs-lookup"><span data-stu-id="346d4-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









