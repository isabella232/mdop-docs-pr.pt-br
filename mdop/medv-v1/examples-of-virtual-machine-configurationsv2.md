---
title: Exemplos de configurações de máquina virtual
description: Exemplos de configurações de máquina virtual
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799502"
---
# Exemplos de configurações de máquina virtual


Veja a seguir exemplos de configurações típicas da máquina virtual: uma em um espaço de trabalho do MED-V persistente e uma em um espaço de trabalho do MED-V reversível.

**Observação**  Esses exemplos não são destinados ao uso em todos os ambientes. Ajuste a configuração de acordo com seu ambiente.

 

**Para configurar uma configuração de domínio típica em um espaço de trabalho do MED-V persistente**

1.  Configure o Sysprep na imagem base para criar um SID exclusivo. Para obter mais informações, consulte [criando uma imagem do Virtual PC para o MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).

2.  Na guia **configuração da VM** , marque a caixa de seleção **executar configuração da VM** .

3.  Na seção **padrão de nome de computador da VM** , configure o padrão para o nome da imagem do computador. Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

4.  Clique em **Editor de script**e, na caixa de diálogo Editor de script de configuração da **VM** , configure as seguintes ações:

    1.  **Renomear computador**

    2.  **Reiniciar o Windows**

    3.  **Verificar a conectividade**

    4.  **Ingressar no domínio**

    5.  **Desabilitar logon automático**

    Para obter mais informações, consulte [como configurar ações de script](how-to-set-up-script-actions.md).

5.  No menu **política** , clique em **confirmar**.

**Para configurar uma configuração típica em um espaço de trabalho reversível**

1.  Na guia **configuração da VM** , marque a caixa de seleção **renomear a VM com base no padrão de nome do computador** .

2.  Na seção **padrão de nome de computador da VM** , configure o padrão para o nome da imagem do computador. Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

3.  No menu **política** , clique em **confirmar**.

## Tópicos relacionados


[Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Como configurar as propriedades de padrão de nomes do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[Como configurar ações de script](how-to-set-up-script-actions.md)

 

 





