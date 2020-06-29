---
title: Configurando políticas de espaço de trabalho do MED-V
description: Configurando políticas de espaço de trabalho do MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799556"
---
# Configurando políticas de espaço de trabalho do MED-V


Uma política de espaço de trabalho do MED-V é um grupo de configurações configuráveis que definem como o ambiente virtualizado e os aplicativos são executados no computador host. Os tópicos desta seção descrevem todas as configurações configuráveis na política de espaço de trabalho do MED-V, bem como as configurações que influenciam o espaço de trabalho do MED-V.

Os seguintes tipos de espaço de trabalho do MED-V estão disponíveis:

-   **Persistente**– em um espaço de trabalho do MED-v persistente, todas as alterações e inclusões feitas pelo usuário no espaço de trabalho do MED-v são salvas no espaço de trabalho do MED-v entre as sessões. Além disso, um espaço de trabalho do MED-V persistente geralmente é usado em um ambiente de domínio.

-   **Reversível**— em um espaço de trabalho do MED-v reversível, na conclusão de cada sessão (ou seja, quando o espaço de trabalho do MED-v é interrompido), o espaço de trabalho do MED-v é revertido ao seu estado original durante a implantação. Nenhuma alteração ou acréscimo feita pelo usuário é salva no espaço de trabalho do MED-V entre as sessões. Um espaço de trabalho do MED-V reversível não pode ser usado em um ambiente de domínio.

É importante decidir o tipo de espaço de trabalho do MED-V que você está criando antes de implantar o espaço de trabalho do MED-V, porque não é recomendável reconfigurar o tipo de espaço de trabalho do MED-v após a implantação de uma política para os usuários.

**Observação**  Ao configurar uma política, um símbolo de aviso é exibido ao lado de campos obrigatórios que não estão preenchidos. Se um campo obrigatório não for preenchido, o símbolo também será exibido na guia.

 

## Nesta seção


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[Como aplicar configurações gerais a um espaço de trabalho do MED-V](how-to-apply-general-settings-to-a-med-v-workspace.md)  
Descreve as configurações gerais de um espaço de trabalho do MED-V e como aplicá-las a uma política.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Descreve as configurações da máquina virtual para um espaço de trabalho do MED-V e como aplicá-las a uma política.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[Como configurar um usuário ou grupo de domínio](how-to-configure-a-domain-user-or-groupmedvv2.md)  
Descreve como configurar usuários e grupos de domínio.

<a href="" id="how-to-configure-published-applications"></a>[Como configurar aplicativos publicados](how-to-configure-published-applicationsmedvv2.md)  
Descreve os aplicativos e menus publicados e como aplicá-los a uma política.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[Como definir as configurações da Web de um espaço de trabalho do MED-V](how-to-configure-web-settings-for-a-med-v-workspace.md)  
Descreve as configurações da Web disponíveis para um espaço de trabalho do MED-V e como aplicá-las a uma política.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Descreve a configuração de máquina virtual para um espaço de trabalho do MED-V e como aplicá-lo a uma política.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Como aplicar as configurações de rede a um espaço de trabalho do MED-V](how-to-apply-network-settings-to-a-med-v-workspace.md)  
Descreve as configurações de rede de um espaço de trabalho do MED-V e como aplicá-las a uma política.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[Como aplicar as configurações de desempenho a um espaço de trabalho do MED-V](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
Descreve as configurações de desempenho de um espaço de trabalho do MED-V e como aplicá-las a uma política.

<a href="" id="how-to-import-and-export-a-policy"></a>[Como importar e exportar uma política](how-to-import-and-export-a-policy.md)  
Descreve como importar e exportar uma política.

 

 





