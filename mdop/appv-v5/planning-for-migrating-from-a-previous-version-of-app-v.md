---
title: Planejamento para a migração de uma versão anterior do App-V
description: Planejamento para a migração de uma versão anterior do App-V
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796258"
---
# Planejamento para a migração de uma versão anterior do App-V


Use as informações a seguir para planejar como migrar para o App-V 5,0 de versões anteriores do App-V.

## Requisitos de migração


Antes de iniciar qualquer atualização, examine os seguintes requisitos:

-   Se você estiver atualizando de uma versão anterior ao App-V 4,6 SP2, atualize para a versão App-V 4,6 SP3 primeiro antes de atualizar para o App-V 5,0 ou posterior. Nesse cenário, atualize os clientes App-V primeiro e, em seguida, atualize os componentes do servidor.
**Observação:** O App-V 4,6 tem saído do suporte básico.

-   O App-V 5,0 oferece suporte somente a pacotes criados usando o App-V 5,0 ou pacotes que foram convertidos no formato App-V 5,0 (**. AppV**).

-   App-V 5,0 SP3 somente: se você estiver atualizando o App-V Server do App-V 5,0 SP1, consulte [sobre o app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) para obter instruções.

## Executando o cliente App-V 5,0 simultaneamente com o App-V 4,6


Você pode executar o cliente App-V 5,0 simultaneamente no mesmo computador com o cliente App-V 4.6 SP3.

Ao executar clientes do App-V coexistentes, você pode:

-   Converta um pacote App-V 4,6 SP3 para o formato App-V 5,0 e publique ambos os pacotes, quando ambos os clientes estiverem em execução.

-   Defina a política de migração para o pacote convertido, que permite que o pacote App-V 5,0 convertido assuma as associações de tipo de arquivo e atalhos do pacote App-V 4,6.

### Cenários de coexistência com suporte

A tabela a seguir mostra os cenários de coexistência do App-V com suporte. Recomendamos que você instale as atualizações mais recentes disponíveis de uma determinada versão quando estiver executando clientes coexistentes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de cliente do App-V 4,6</th>
<th align="left">Tipo de cliente do App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,6 SP3</p></td>
<td align="left"><p>App-V 5,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 SP3 RDS</p></td>
<td align="left"><p>App-V 5,0 RDS</p></td>
</tr>
</tbody>
</table>

 

### Requisitos para a execução de clientes coexistentes

Para executar clientes coexistentes, você deve:

-   Instale o cliente App-V 4.6 antes de instalar o cliente App-V 5,0.

-   Habilite a configuração da política de grupo **habilitar modo de migração** , que está no nó de coexistência do cliente **App-V** &gt; **Client Coexistence** . Para obter o modelo. admx de implantação, consulte [como baixar e implantar modelos de política de grupo do MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

### Downloads e documentação do cliente

A tabela a seguir fornece um link para a documentação do TechNet sobre as versões. A documentação do TechNet sobre o cliente App-V se aplica a ambos os clientes, a menos que especificado de outra forma.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do App-V</th>
<th align="left">Link para a documentação do TechNet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">Sobre o Microsoft Application Virtualization 4.6 SP3</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.0 SP3</p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)">Sobre o Microsoft Application Virtualization 5,0 SP3</a></p></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre como configurar a coexistência do cliente do App-V 5,0, consulte:

-   [Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [Coexistência e migração do App-V 5,0](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Convertendo pacotes "versão anterior" usando o conversor de pacote


Antes de migrar um pacote, criado usando o App-V 4.6 SP3 ou anterior, para o App-V 5,0, examine os seguintes requisitos:

-   Você deve converter o pacote para o formato de arquivo **. AppV** .

-   O conversor de pacote dá suporte somente à conversão direta de pacotes que foram criados usando o App-V 4,5 e posterior. Para usar o conversor de pacote em um pacote criado com uma versão anterior, você deve usar uma versão App-V 4.5 ou posterior do sequenciador para atualizar o pacote e, em seguida, executar a conversão do pacote.

Para obter mais informações sobre como usar o conversor de pacote para converter um pacote, consulte [como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md). Depois de converter o arquivo, você poderá implantá-lo em computadores de destino que executam o cliente App-V 5,0.






## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

 

 





