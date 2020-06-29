---
title: Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro
description: Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797112"
---
# <span data-ttu-id="6b6a5-103">Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro</span><span class="sxs-lookup"><span data-stu-id="6b6a5-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="6b6a5-104">A instalação padrão do console de gerenciamento do App-V inclui suporte para comunicações seguras.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="6b6a5-105">Cada console de gerenciamento é configurado em uma base por conexão quando o console é iniciado pela primeira vez ou quando se conecta a um serviço de gerenciamento da Web do App-V adicional.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="6b6a5-106">A configuração padrão usa SSL na porta TCP 443.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="6b6a5-107">Você pode alterar o número da porta se o número da porta for modificado no servidor.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="6b6a5-108">Você pode usar o procedimento a seguir para se conectar a um serviço de gerenciamento da Web do App-V usando uma conexão segura.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="6b6a5-109">Como se conectar a um serviço de gerenciamento do App-V usando uma conexão SSL</span><span class="sxs-lookup"><span data-stu-id="6b6a5-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="6b6a5-110">Inicie o console de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="6b6a5-111">Clique em **Configurar conexão** no painel Ações do console.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="6b6a5-112">Digite o **nome do host do serviço Web**e certifique-se de que **usar conexão segura** esteja selecionado.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="6b6a5-113">**Importante**  O nome fornecido no nome do host do serviço Web deve coincidir com o nome comum no certificado ou a conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="6b6a5-114">Selecione as credenciais de logon apropriadas e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b6a5-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="6b6a5-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b6a5-115">Related topics</span></span>


[<span data-ttu-id="6b6a5-116">Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V</span><span class="sxs-lookup"><span data-stu-id="6b6a5-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





