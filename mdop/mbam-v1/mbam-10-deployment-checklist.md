---
title: Lista de verificação para implantação do MBAM 1.0
description: Lista de verificação para implantação do MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796024"
---
# Lista de verificação para implantação do MBAM 1.0


Esta lista de verificação foi projetada para facilitar a implantação do Microsoft BitLocker Administration and Monitoring (MBAM).

**Observação**  
Esta lista de verificação descreve as etapas recomendadas e fornece uma lista de alto nível de itens que devem ser considerados ao implantar os recursos do MBAM. Recomendamos que você copie esta lista de verificação para um programa de planilha e personalize-a para atender às suas necessidades específicas.



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
<td align="left"><p>Conclua a fase de planejamento para preparar o ambiente de computação para a implantação do MBAM.</p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Lista de Verificação de Planejamento do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Revise as informações sobre as configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação do recurso MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurações com suporte no MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Execute a instalação do MBAM para implantar recursos do MBAM Server na seguinte ordem:</p>
<ol>
<li><p>Recuperação e banco de dados de hardware</p></li>
<li><p>Banco de dados de status de conformidade</p></li>
<li><p>Auditoria e relatórios de conformidade</p></li>
<li><p>Servidor de administração e monitoramento</p></li>
<li><p>Modelo de política de grupo MBAM</p></li>
</ol>
<div class="alert">
<strong>Observação</strong><br/><p>Mantenha o controle dos nomes dos servidores em que cada recurso está instalado. Você usará essas informações durante todo o processo de instalação.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Implantando a infraestrutura do Servidor do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Adicione os grupos de segurança dos serviços de domínio Active Directory criados durante a fase de planejamento para os grupos de administradores de recursos de servidor de MBAM locais adequados nos servidores adequados.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planejando funções de administrador do MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> como gerenciar funções de administrador do MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Criar e implantar os objetos de política de grupo MBAM necessários.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Implantar Objetos de Política de Grupo no MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implantar o software cliente do MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Implantando o Cliente do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Implantando o MBAM 1.0](deploying-mbam-10.md)









