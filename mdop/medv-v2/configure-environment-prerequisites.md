---
title: Configurar os pré-requisitos do ambiente
description: Configurar os pré-requisitos do ambiente
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799874"
---
# Configurar os pré-requisitos do ambiente


Antes de poder implantar e executar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, você deve garantir que seu ambiente atenda aos seguintes pré-requisitos mínimos.

**Windows 7**

O agente de host do MED-V e o pacote de espaço de trabalho do MED-V só têm suporte no Windows 7 ou versões mais recentes.

**Windows XP SP3**

O agente de convidado do MED-V só tem suporte no Windows XP SP3.

**.NET Framework 3,5 SP1**

O host do MED-V e os agentes convidados e o pacote do espaço de trabalho do MED-V exigem o Microsoft .NET Framework 3,5 SP1.

**Importante**  Você também deve instalar a atualização [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , que aborda vários problemas conhecidos de compatibilidade do aplicativo.

 

**Observação**  Você deve instalar manualmente o .NET Framework 3,5 SP1 e o Update KB959209 na imagem do PC virtual do Windows que você prepara para usar com o MED-V. No entanto, por padrão, o Microsoft .NET Framework 3,5 SP1 e a atualização são incluídos quando você instala o Windows 7 no computador host.

 

**Uma infra-estrutura do Active Directory**

A política de grupo fornece o gerenciamento centralizado e a configuração de sistemas operacionais, aplicativos e configurações dos usuários em um ambiente do Active Directory.

## Tópicos relacionados


[Configurar os pré-requisitos de instalação](configure-installation-prerequisites.md)

[Arquitetura de alto nível](high-level-architecturemedv2.md)

[Configurações com suporte na MED-V 2.0](med-v-20-supported-configurations.md)

 

 





