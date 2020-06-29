---
title: Arquitetura de alto nível
description: Arquitetura de alto nível
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799825"
---
# Arquitetura de alto nível


A solução MED-V inclui os seguintes elementos:

-   **Máquina virtual definida pelo administrador**— encapsula um ambiente de área de trabalho completo, incluindo um sistema operacional, aplicativos e ferramentas de gerenciamento e segurança opcionais.

-   **Repositório de imagens**— armazena todas as imagens virtuais em um servidor IIS padrão e habilita o gerenciamento de versão de imagens virtuais, a recuperação de imagens autenticadas pelo cliente e o download eficiente (de uma nova imagem ou atualizações) via tecnologia de transferência de corte.

-   **Servidor de gerenciamento**— associa imagens virtuais do repositório de imagens juntamente com as políticas de uso do administrador ao Active Directory® usuários ou grupos. O servidor de gerenciamento também agrega eventos dos clientes e os armazena em um banco de dados externo (Microsoft SQL Server®) para fins de monitoramento e relatórios.

-   **Console de gerenciamento**— permite que os administradores controlem o servidor de gerenciamento e o repositório de imagens.

-   **Cliente de usuário final**

    1.  Ciclo de vida da imagem virtual — autenticação, recuperação de imagens, imposição de políticas de uso.

    2.  Gerenciamento de sessões de máquinas virtuais — Iniciar, parar, bloquear a máquina virtual.

    3.  Experiência única na área de trabalho: os aplicativos instalados na máquina virtual diretamente disponíveis por meio do menu Iniciar da área de trabalho padrão e integrados a outros aplicativos na área de trabalho do usuário.

Toda a comunicação entre o cliente e os servidores (servidor de gerenciamento e o repositório de imagens) é realizada sobre um canal HTTP ou HTTPS padrão.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





