---
title: Arquitetura de alto nível
description: Arquitetura de alto nível
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800043"
---
# Arquitetura de alto nível


Esta seção descreve a arquitetura do sistema de alto nível e o design de componentes da virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.

## Arquitetura do sistema


O MED-V aprimora o Windows Virtual PC para executar dois sistemas operacionais em um dispositivo, adicionando entrega de imagem virtual, provisionamento baseado em política de grupo e gerenciamento centralizado. Ao usar o MED-V, você pode facilmente configurar, implantar e gerenciar imagens do Windows Virtual PC corporativo em qualquer área de trabalho baseada no Windows com o Windows 7 Professional, Enterprise ou Windows 7 Ultimate. A solução MED-V inclui os seguintes componentes:

<a href="" id="---------------med-v-host"></a> **Host MED-V**  
Um ambiente do Windows 7 que inclui um agente de host do MED-V, um sistema ESD (distribuição de software eletrônico), um sistema de gerenciamento de registro e um convidado do MED-V. O host do MED-V interage com o MED-V Guest para que determinadas funções de configuração e informações do sistema possam ser processadas.

<a href="" id="-------------------med-v-host-agent"></a> **Agente de host do MED-V**  
O software MED-V contido no host MED-V que fornece um canal para se comunicar com o convidado do MED-V. Ele também fornece funcionalidade como a configuração pela primeira vez e a publicação do aplicativo.

**Observação**  Após a instalação do MED-V e dos componentes obrigatórios, o MED-V deve ser configurado. A configuração do MED-V é chamada de configuração pela primeira vez.

 

<a href="" id="esd-system"></a>**Sistema ESD**  
Seu método de distribuição de software existente que permite implantar e instalar os arquivos de pacote do espaço de trabalho do MED-V que o MED-V cria.

<a href="" id="registry-management-system"></a>**Sistema de gerenciamento de registros**  
Seu método existente de gerenciamento de preferências e configurações de política de grupo.

<a href="" id="windows-virtual-pc-image"></a>**Imagem do PC virtual do Windows**  
Uma máquina virtual definida pelo administrador que contém os seguintes componentes:

<a href="" id="corporate-operating-system"></a>**Sistema operacional corporativo**  
Seu sistema operacional corporativo padrão.

<a href="" id="management-and-security-tools"></a>**Ferramentas de gerenciamento e segurança**  
Suas ferramentas de gerenciamento e segurança padrão, como proteção contra vírus.

<a href="" id="-----------------------med-v-guest"></a> **Convidado do MED-V**  
Um ambiente do Windows XP SP3, como parte de um PC virtual do Windows em execução no Windows 7 que contém os seguintes componentes:

<a href="" id="---------------------------med-v-guest-agent"></a> **Agente de convidado do MED-V**  
O software MED-V contido no convidado do MED-V que fornece um canal para se comunicar com o host do MED-V. Ele também dá suporte ao agente de host do MED-V com funções como executar a configuração inicial.

**Observação**  O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.

 

<a href="" id="esd-client"></a>**Cliente ESD**  
Uma parte opcional do seu sistema ESD que instala pacotes de software e o status dos relatórios para o sistema ESD.

## Tópicos relacionados


[Planejamento da compatibilidade do sistema operacional para aplicativos](planning-for-application-operating-system-compatibility.md)

[Preparar o ambiente de implantação para a MED-V](prepare-the-deployment-environment-for-med-v.md)

 

 





