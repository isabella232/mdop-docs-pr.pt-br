---
title: Como implantar o cliente do MBAM usando uma linha de comando
description: Como implantar o cliente do MBAM usando uma linha de comando
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799482"
---
# Como implantar o cliente do MBAM usando uma linha de comando


Você pode usar uma linha de comando para implantar o software cliente do Microsoft BitLocker Administration and Monitoring (MBAM).

## Linha de comando para implantar o software cliente do MBAM


Digite o seguinte comando no prompt de comando para aceitar automaticamente o contrato de licença de usuário final ao implantar o software cliente MBAM.

**MBAMClientSetup.exe/acceptEula = Sim**

**Observação**  As opções da linha de comando **/Ju** e **/JM** não são suportadas e não podem ser usadas para instalar o software cliente do MBAM.

 

Digite o seguinte comando no prompt de comando para extrair e instalar o MSP:

**&lt;Caminho de/extract MBAMClientSetup.exe para extrair MSI &gt; /AcceptEula = Sim**

Em seguida, instale o MSI silenciosamente executando o seguinte comando:

**msiexec/i &lt; caminho para MSI, &gt; /QB AllUsers = 1 reboot = ReallySuppress**

**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM. No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto após aceitar o EULA.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>OPTIname \ _FOR \ _MICROSOFT \ _UPDATES = 1 opção de linha de comando


Opcionalmente, você pode especificar a opção de linha de comando `OPTIN_FOR_MICROSOFT_UPDATES=1` durante a instalação do software cliente para instalar automaticamente as atualizações da Microsoft em computadores cliente. Especificar essa opção faz com que o Microsoft Update inicie automaticamente e procure atualizações disponíveis para instalar após a conclusão da instalação do software cliente.

Você pode usar essa opção de linha de comando com um dos seguintes métodos de instalação.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Instalar o software cliente do MBAM usando</th>
<th align="left">Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados


[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




