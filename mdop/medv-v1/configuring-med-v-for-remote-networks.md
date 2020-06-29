---
title: Configurando o MED-V para redes remotas
description: Configurando o MED-V para redes remotas
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799929"
---
# <span data-ttu-id="37fcf-103">Configurando o MED-V para redes remotas</span><span class="sxs-lookup"><span data-stu-id="37fcf-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="37fcf-104">Você pode configurar o MED-V para trabalhar de dentro de uma rede, remotamente ou de dentro da rede e remotamente.</span><span class="sxs-lookup"><span data-stu-id="37fcf-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="37fcf-105">Para configurar o MED-V para trabalhar de dentro de uma rede</span><span class="sxs-lookup"><span data-stu-id="37fcf-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="37fcf-106">Configure um servidor MED-V e uma distribuição de imagens dentro da rede.</span><span class="sxs-lookup"><span data-stu-id="37fcf-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="37fcf-107">Para configurar o MED-V para trabalhar remotamente</span><span class="sxs-lookup"><span data-stu-id="37fcf-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="37fcf-108">Configurar um servidor MED-V e um servidor de distribuição de imagens que podem ser acessados pela Internet.</span><span class="sxs-lookup"><span data-stu-id="37fcf-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="37fcf-109">Se necessário, configure um proxy reverso de rede de perímetro (também chamado de DMZ).</span><span class="sxs-lookup"><span data-stu-id="37fcf-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="37fcf-110">Defina o método de autenticação, no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="37fcf-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="37fcf-111">Para configurar o MED-V para funcionar de dentro de uma rede e remotamente</span><span class="sxs-lookup"><span data-stu-id="37fcf-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="37fcf-112">Configurar um servidor MED-V Server e servidor de distribuição de imagens dentro da rede.</span><span class="sxs-lookup"><span data-stu-id="37fcf-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="37fcf-113">Certifique-se de que os servidores estejam acessíveis na Internet.</span><span class="sxs-lookup"><span data-stu-id="37fcf-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="37fcf-114">Configure a resolução DNS para que, quando o cliente tentar se conectar a um servidor, ele se conecte automaticamente ao servidor correto (na rede ou pela Internet) com base no local do cliente.</span><span class="sxs-lookup"><span data-stu-id="37fcf-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="37fcf-115">Se necessário, configure um proxy reverso de rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="37fcf-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="37fcf-116">Defina o método de autenticação, no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .</span><span class="sxs-lookup"><span data-stu-id="37fcf-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="37fcf-117">**Observação**  Durante a aplicação de novas configurações, o serviço deve ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="37fcf-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="37fcf-118">Você pode alterar o esquema de autenticação do IIS para um dos seguintes: BASIC, DIGEST, NTLM ou NEGOTIAte.</span><span class="sxs-lookup"><span data-stu-id="37fcf-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="37fcf-119">O padrão é NEGOTIAte e usa a seguinte entrada:</span><span class="sxs-lookup"><span data-stu-id="37fcf-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="37fcf-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37fcf-120">Related topics</span></span>


[<span data-ttu-id="37fcf-121">Planejamento e design da infraestrutura do MED-V</span><span class="sxs-lookup"><span data-stu-id="37fcf-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





