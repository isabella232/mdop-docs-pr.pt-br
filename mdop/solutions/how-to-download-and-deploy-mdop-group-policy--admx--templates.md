---
title: Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)
description: Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799968"
---
# Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)


Você pode gerenciar as configurações de recursos de determinadas tecnologias do Microsoft Desktop Optimization Pack (MDOP) (por exemplo, App-V, UE-V ou MBAM) usando os modelos de política de grupo, os arquivos. admx e. adml. Os modelos de política de grupo do MDOP estão disponíveis para download em um arquivo auto-extraível compactado, agrupado por tecnologia e versão.

## Modelos de política de grupo do MDOP

**Como baixar e implantar os modelos de política de grupo do MDOP**

1. Baixar os últimos [modelos de política de grupo do MDOP](https://www.microsoft.com/download/details.aspx?id=55531) 

2. Expanda o arquivo. cab baixado executando `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Aviso**  
   Não extraia os modelos diretamente para o diretório de implantação da política de grupo. Várias tecnologias e versões são agrupadas nesse arquivo.

3. Na pasta extraída, localize o arquivo Technology-Version. admx. Determinadas tecnologias do MDOP têm vários conjuntos de objetos de política de grupo (GPOs). Por exemplo, MBAM inclui configurações de gerenciamento MBAM e MBAM de usuário.

4. Localize o arquivo. adml apropriado por cultura de idioma (ou seja, *en-US* para inglês-Estados Unidos).

5. Copie os arquivos. admx e. adml para uma pasta de definição de política. Dependendo de onde você armazenar os modelos, você pode definir as configurações de política de grupo do dispositivo local ou de qualquer computador no domínio.

   - **Arquivos locais:** Para definir as configurações de política de grupo do dispositivo local, copie os arquivos de modelo para os seguintes locais:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo de arquivo</th>
   <th align="left">Local do arquivo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Modelo de política de grupo (. admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;policyDefinitionss fortes</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Arquivo de idioma da política de grupo (. adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;policyDefinitionss fortes</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - **Repositório central do domínio:** Para habilitar a configuração de configurações de política de grupo por um administrador de política de grupo de qualquer computador no domínio, copie os arquivos para os seguintes locais no controlador de domínio:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo de arquivo</th>
   <th align="left">Local do arquivo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Modelo de política de grupo (. admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;&gt;sysvol\domain\policies\PolicyDefinitionss fortes</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Arquivo de idioma da política de grupo (. adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;alta segurança &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>Por exemplo, o arquivo específico da linguagem ADML inglês americano será armazenado no%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
   </tr>
   </tbody>
   </table>

6. Edite as configurações de política de grupo usando o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM) para definir configurações de política de grupo para a tecnologia do MDOP.

### Política de grupo do MDOP por tecnologia

Para obter mais informações sobre a política de grupo do MDOP com suporte, consulte a documentação específica da tecnologia.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tecnologia do MDOP</th>
<th align="left">Pacotes de versão</th>
<th align="left">Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Application Virtualization (App-V)</strong></p></td>
<td align="left"><p>Service Packs do App-V 5,0 e do App-V 5,0</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>User Experience Virtualization (UE-V)</strong></p></td>
<td align="left"><p>UE-V 2,0 e UE-V 2,1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">Configurando o UE-V 2. x com objetos de política de grupo</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1,0 incluindo 1,0 SP1</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">Configurando o UE-V com objetos de Política de Grupo</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Microsoft BitLocker Administration and Monitoring (MBAM)</strong></p></td>
<td align="left"><p>MBAM 2,5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2,0, incluindo 2,0 SP1</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planejar Requisitos de Política de Grupo do MBAM 2.0</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">Implantar Objetos de Política de Grupo no MBAM 2.0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1,0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">Como editar Configurações GPO do MBAM 1.0</a></p></td>
</tr>
</tbody>
</table>

 

 

 





