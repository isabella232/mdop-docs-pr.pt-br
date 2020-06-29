---
title: Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V
description: Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799999"
---
# Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V


Todas as configurações de configuração da máquina virtual são configuradas no módulo de **política** , na guia **configuração da VM** .

## Como configurar a configuração da máquina virtual para um espaço de trabalho do MED-V persistente


**Para configurar a configuração de máquina virtual para um espaço de trabalho do MED-V persistente**

1.  Clique em um espaço de trabalho do MED-V persistente para ser configurado.

2.  Na seção **configuração de VM persistente** , configure as propriedades conforme descrito na tabela a seguir.

    **Observação**  
    As propriedades de configuração de VM persistente são habilitadas somente para um espaço de trabalho do MED-V persistente.



3.  No menu **política** , selecione **confirmar**.

**Propriedades de configuração de VM persistente**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Executar a configuração da VM</p></td>
<td align="left"><p>Marque esta caixa de seleção para executar um script de instalação na primeira vez em que o espaço de trabalho do MED-V for executado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Editor de scripts</p></td>
<td align="left"><p>Clique em para configurar o script de instalação. Para obter mais informações, consulte <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> como configurar ações de script </a> .</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esse botão estará habilitado apenas quando <strong> executar o script de configuração da VM </strong> estiver selecionado.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Mensagem exibida quando o script está em execução</p></td>
<td align="left"><p>Uma mensagem a ser exibida enquanto o script estiver em execução. Se deixado em branco, a mensagem padrão será exibida.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Este campo é habilitado somente quando <strong> a opção executar o script de configuração da VM </strong> está marcada.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Como configurar a configuração da máquina virtual para um espaço de trabalho do MED-V reversível


**Para configurar a configuração de máquina virtual para um espaço de trabalho do MED-V reversível**

1.  Clique em um espaço de trabalho do MED-V reversível para configurar.

2.  Na seção **configuração de VM reversível** , configure as propriedades conforme descrito na tabela a seguir.

    **Observação**  
    As propriedades de configuração da VM reversível são habilitadas somente para um espaço de trabalho do MED-V reversível.



3.  No menu **política** , selecione **confirmar**.

**Propriedades de configuração de VM reversível**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Renomear a VM com base no padrão de nome do computador</p></td>
<td align="left"><p>Marque esta caixa de seleção para atribuir um nome exclusivo a cada computador usando o espaço de trabalho do MED-V para que você possa diferenciar vários computadores usando o mesmo espaço de trabalho do MED-V.</p>
<p>Para obter mais informações sobre como configurar nomes de imagem de computador, consulte <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> como configurar propriedades do padrão de nome do computador VM </a> .</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Exemplos de configurações de máquina virtual](examples-of-virtual-machine-configurationsv2.md)









