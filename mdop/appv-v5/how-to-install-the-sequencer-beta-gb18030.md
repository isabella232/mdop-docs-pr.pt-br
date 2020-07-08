---
title: Como instalar o sequenciador
description: Como instalar o sequenciador
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796378"
---
# Como instalar o sequenciador


Use o procedimento a seguir para instalar o sequenciador do Microsoft Application Virtualization (App-V) 5,0. O computador que executará o sequenciador não deve estar executando qualquer versão do cliente App-V 5,0.

Não há suporte para a atualização de uma instalação anterior do sequenciador App-V.

**Importante**  Para obter uma lista completa dos requisitos do sequenciador, consulte as seções do sequenciador de [pré-requisitos do App-v 5,0](app-v-50-prerequisites.md) e do [app-v 5,0 com suporte](app-v-50-supported-configurations.md).

 

Você também pode usar a linha de comando para instalar o App-V 5,0 Sequencer. A lista a seguir exibe informações sobre as opções para instalar o sequenciador usando a linha de comando e **appv\_sequencer\_setup.exe**:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Especifica o diretório de instalação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Habilita a participação no programa de aperfeiçoamento da experiência do usuário da Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Especifica onde o log de instalação será salvo, o local padrão é <strong> % temp% </strong> . Por exemplo, <strong> C:\ Logs \ log. log </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/q</p></td>
<td align="left"><p>Especifica uma instalação silenciosa ou silenciosa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Especifica a remoção do sequenciador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Aceita o contrato de licença. Isso é necessário para uma instalação automática. Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Especifica a ação de layout associado. Ele também extrai o Windows Installer (. msi) e arquivos de script para uma pasta sem instalar o App-V 5,0. Nenhum valor é esperado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Especifica o diretório de layout. Requer um valor de cadeia de caracteres. Exemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualização C:\Application" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? Ou/h ou/Help</p></td>
<td align="left"><p>Exibe a ajuda associada.</p></td>
</tr>
</tbody>
</table>

 

**Para instalar o sequenciador do App-V 5,0**

1.  Copie os arquivos de instalação do sequenciador do App-V 5,0 para o computador em que ele será instalado. Clique duas vezes **appv\_sequencer\_setup.exe** e, em seguida, clique em **instalar**.

2.  Na página **termos de licença para software** , você deve revisar os termos de licença. Para aceitar os termos de licença **, selecione aceito os termos de licença.** Clique em **Avançar**.

3.  Na página **usar o Microsoft Update para ajudar a manter o seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar a execução de atualizações da Microsoft **, selecione não quero usar o Microsoft Update**. Clique em **Avançar**.

4.  Na página do **programa de aperfeiçoamento da experiência do usuário** , para participar do programa, selecione **ingressar no programa de aperfeiçoamento da experiência do usuário**. Isso permitirá que as informações sejam coletadas sobre como você está usando o App-V 5,0. Se não quiser participar do programa, selecione **não quero participar do programa no momento**. Clique em **Instalar**.

5.  Para abrir o sequenciador, clique em **Iniciar** e em **Microsoft Application Virtualization Sequencer**.

**Para solucionar problemas de instalação do sequenciador do App-V 5,0**

-   Para obter mais informações sobre a instalação do sequenciador, você pode exibir o log de erros na pasta **% Temp%** . Para examinar os arquivos de log, clique em **Iniciar**, digite **% Temp%** e procure o **log appv\_**.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

 

 





