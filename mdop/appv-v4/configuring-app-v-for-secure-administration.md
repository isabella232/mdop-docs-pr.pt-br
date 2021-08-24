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
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910476"
---
# <a name="configuring-app-v-for-secure-administration"></a>Configuração do App-V para administração segura


Em um ambiente em que a segurança de operações administrativas é importante, o App-V permite a comunicação segura entre o Serviço de Gerenciamento da Web do App-V e o Console de Gerenciamento do App-V. Como o Serviço de Gerenciamento é um aplicativo baseado na Web, ele requer a segurança do aplicativo Servidor de Gerenciamento do App-V no servidor Web que hospeda o Serviço de Gerenciamento. Conforme mostrado na ilustração a seguir, esse processo inclui o uso de HTTPS para comunicação e a configuração do servidor IIS para permitir apenas Windows Autenticação Integrada.

![configuração de rede de serviço Web do app-v.](images/appvmgmtwebservice.gif)

O Serviço de Gerenciamento web do App-V é instalado como um aplicativo baseado na Web no IIS. Para que o Serviço de Gerenciamento da Web suporte a conexões seguras (SSL) entre o Console de Gerenciamento do App-V e o Serviço de Gerenciamento da Web, você precisará configurar o servidor IIS onde o Serviço de Gerenciamento da Web está instalado e configurar o Console de Gerenciamento do App-V.

## <a name="in-this-section"></a>Nesta seção


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fornece informações úteis sobre como configurar certificados para dar suporte a conexões baseadas em SSL, para ajudar a proteger a comunicação para o Serviço de Gerenciamento web do App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Fornece um procedimento passo a passo para se conectar a um Serviço de Gerenciamento web do App-V usando uma conexão segura.

 

 





