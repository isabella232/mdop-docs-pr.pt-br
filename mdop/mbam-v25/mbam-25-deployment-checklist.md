---
title: Lista de verificação para implantação do MBAM 2.5
description: Lista de verificação para implantação do MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799151"
---
# Lista de verificação para implantação do MBAM 2.5


Você pode usar esta lista de verificação para ajudá-lo durante a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com uma topologia autônoma.

**Observação**  
Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens que devem ser considerados ao implantar os recursos de administração e monitoramento do Microsoft BitLocker. Recomendamos que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tarefa</th>
<th align="left">Referências</th>
<th align="left">Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise e conclua todas as etapas de planejamento para preparar seu ambiente para a implantação do MBAM.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">Lista de verificação de planejamento para o MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de configurações compatíveis para garantir que o MBAM suporte os computadores cliente e servidor selecionados.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Instale o software MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Configurar os recursos do servidor do MBAM:</p>
<ul>
<li><p>Banco de dados de conformidade e auditoria e banco de dados de recuperação</p></li>
<li><p>Relatórios</p></li>
<li><p>Aplicativos Web</p></li>
<li><p>A topologia de integração do Configuration Manager (necessária somente se você estiver executando o MBAM com essa topologia)</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Observe os nomes dos servidores nos quais você configura cada recurso. Você usará essas informações em todo o processo de configuração.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">Configurando os recursos de servidor do MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Valide a configuração do MBAM.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">Validando a configuração de recursos de servidor do MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Copie o modelo de política de grupo do MBAM e edite as configurações de política de grupo.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copiando os modelos de política de grupo do MBAM 2,5 </a> e <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> editando as configurações de política de grupo do MBAM 2,5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implantar o software cliente do MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">Implantando o cliente do MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## Tópicos relacionados


[Implantando o MBAM 2.5](deploying-mbam-25.md)




## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




