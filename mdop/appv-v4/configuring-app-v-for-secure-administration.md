---
title: Configuração do App-V para administração segura
description: Configuração do App-V para administração segura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798018"
---
# Configuração do App-V para administração segura


Em um ambiente em que a proteção de operações administrativas é importante, o App-V permite a comunicação segura entre o serviço de gerenciamento da Web do App-V e o console de gerenciamento do App-V. Como o serviço de gerenciamento é um aplicativo baseado na Web, ele exige a proteção do aplicativo do servidor de gerenciamento do App-V no servidor Web que hospeda o serviço de gerenciamento. Conforme mostrado na ilustração a seguir, esse processo inclui o uso de HTTPS para comunicação e a configuração do servidor IIS para permitir somente a autenticação integrada do Windows.

![configuração de rede do serviço Web App-v](images/appvmgmtwebservice.gif)

O serviço de gerenciamento da Web App-V é instalado como um aplicativo baseado na Web no IIS. Para que o serviço de gerenciamento da Web ofereça suporte a conexões seguras (SSL) entre o console de gerenciamento do App-V e o serviço de gerenciamento da Web, você precisará configurar o servidor IIS onde o serviço de gerenciamento da Web está instalado e configurar o console de gerenciamento do App-V.

## Nesta seção


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fornece informações úteis sobre como configurar certificados para dar suporte a conexões baseadas em SSL, para ajudar a proteger a comunicação do serviço de gerenciamento da Web do App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Fornece um procedimento passo a passo para se conectar a um serviço de gerenciamento da Web do App-V usando uma conexão segura.

 

 





