---
title: Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo
description: Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796346"
---
# <span data-ttu-id="c98bc-103">Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="c98bc-103">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="c98bc-104">Use o modelo ADMX do Microsoft Application Virtualization (App-V) 5,1 para configurar as definições do aplicativo cliente do App-V 5,1 usando o modelo ADMX e a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c98bc-104">Use the Microsoft Application Virtualization (App-V) 5.1 ADMX template to configure App-V 5.1 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="c98bc-105">Para modificar a configuração do cliente do App-V 5,1 usando a política de grupo</span><span class="sxs-lookup"><span data-stu-id="c98bc-105">To modify App-V 5.1 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="c98bc-106">Para modificar a configuração do cliente do App-V 5,1, localize os arquivos **admxtemplate** disponíveis com o app-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="c98bc-106">To modify the App-V 5.1 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.1.</span></span>

    <span data-ttu-id="c98bc-107">**Observação**  Use o link a seguir para baixar os **modelos do ADMX**do App-V 5,1: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="c98bc-107">**Note** Use the following link to download the App-V 5.1 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="c98bc-108">No computador em que você gerencia a política de grupo, normalmente o controlador de domínio, copie o arquivo template **. admx** para o seguinte diretório: \*\* &lt; unidade de instalação &gt; \ \ Windows \ \ policyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="c98bc-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="c98bc-109">Em seguida, no mesmo computador, copie o arquivo **. adml** para o seguinte diretório: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="c98bc-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="c98bc-110">Depois de copiar os arquivos, abra o console de gerenciamento de política de grupo, para modificar as políticas associadas aos seus clientes do App-V 5,1 navegar para políticas de **configuração do computador**  /  **Policies**  /  sistema de**modelos administrativos**  /  **System**  /  **-V**.</span><span class="sxs-lookup"><span data-stu-id="c98bc-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.1 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="c98bc-111">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="c98bc-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c98bc-112">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c98bc-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c98bc-113">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="c98bc-113">Got an App-V issue?</span></span>** <span data-ttu-id="c98bc-114">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c98bc-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c98bc-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c98bc-115">Related topics</span></span>


[<span data-ttu-id="c98bc-116">Implantação do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c98bc-116">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="c98bc-117">Sobre as configurações do cliente</span><span class="sxs-lookup"><span data-stu-id="c98bc-117">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

 

 





