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
# Configurando o MED-V para redes remotas


Você pode configurar o MED-V para trabalhar de dentro de uma rede, remotamente ou de dentro da rede e remotamente.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**Para configurar o MED-V para trabalhar de dentro de uma rede**

-   Configure um servidor MED-V e uma distribuição de imagens dentro da rede.

**Para configurar o MED-V para trabalhar remotamente**

1.  Configurar um servidor MED-V e um servidor de distribuição de imagens que podem ser acessados pela Internet.

2.  Se necessário, configure um proxy reverso de rede de perímetro (também chamado de DMZ).

3.  Defina o método de autenticação, no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .

**Para configurar o MED-V para funcionar de dentro de uma rede e remotamente**

1.  Configurar um servidor MED-V Server e servidor de distribuição de imagens dentro da rede.

2.  Certifique-se de que os servidores estejam acessíveis na Internet.

3.  Configure a resolução DNS para que, quando o cliente tentar se conectar a um servidor, ele se conecte automaticamente ao servidor correto (na rede ou pela Internet) com base no local do cliente.

4.  Se necessário, configure um proxy reverso de rede de perímetro.

5.  Defina o método de autenticação, no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .

**Observação**  Durante a aplicação de novas configurações, o serviço deve ser reiniciado.

 

-   Você pode alterar o esquema de autenticação do IIS para um dos seguintes: BASIC, DIGEST, NTLM ou NEGOTIAte. O padrão é NEGOTIAte e usa a seguinte entrada:

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

## Tópicos relacionados


[Planejamento e design da infraestrutura do MED-V](med-v-infrastructure-planning-and-design.md)

 

 





