---
title: Lista de verificação para implantação do MBAM 2.0
description: Lista de verificação para implantação do MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799872"
---
# Lista de verificação para implantação do MBAM 2.0


Esta lista de verificação pode ser usada para ajudá-lo durante a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com uma topologia autônoma.

**Observação**  
Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens a serem considerados ao implantar recursos de administração e monitoramento do Microsoft BitLocker. É recomendável que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.



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
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Lista de Verificação de Planejamento do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação de recursos do MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurações com suporte no MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Execute a instalação do MBAM para implantar recursos do MBAM Server na seguinte ordem:</p>
<ol>
<li><p>Banco de dados de recuperação</p></li>
<li><p>Banco de dados de auditoria e conformidade</p></li>
<li><p>Auditoria e relatórios de conformidade</p></li>
<li><p>Servidor de autoatendimento</p></li>
<li><p>Servidor de administração e monitoramento</p></li>
<li><p>Modelo de política de grupo MBAM</p></li>
</ol>
<div class="alert">
<strong>Observação</strong><br/><p>Mantenha o controle dos nomes dos servidores em que cada recurso está instalado. Essas informações serão usadas em todo o processo de instalação.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Implantação da infraestrutura de servidor do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Adicione os grupos de segurança dos serviços de domínio do Active Directory criados durante a fase de planejamento ao recurso apropriado do servidor de MBAM local Administradores grupos em servidores adequados.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planejando funções de administrador do MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> como gerenciar funções de administrador do MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Criar e implantar objetos obrigatórios de política de grupo do MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Implantar Objetos de Política de Grupo no MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implantar o software cliente do MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Implantando o Cliente do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Implantando o MBAM 2.0](deploying-mbam-20-mbam-2.md)









