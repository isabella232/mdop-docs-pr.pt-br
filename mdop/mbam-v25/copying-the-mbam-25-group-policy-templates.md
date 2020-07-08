---
title: Copiando os modelos de Política de Grupo do MBAM 2.5
description: Copiando os modelos de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799629"
---
# Copiando os modelos de Política de Grupo do MBAM 2.5


Antes de implantar a instalação do cliente do MBAM, você deve baixar os modelos de política de grupo do MBAM, que contêm configurações de política de grupo que definem as configurações de implementação MBAM para a criptografia de unidade de disco BitLocker. Depois de baixar os modelos, você define as configurações de política de grupo para implementar em sua empresa.

## Baixar e implantar os modelos de política de grupo do MDOP


Os modelos de política de grupo do MDOP estão disponíveis para download em um arquivo auto-extraível compactado, agrupado por tecnologia e versão.

**Como baixar e implantar os modelos de política de grupo do MDOP**

1. Baixe os modelos de política de grupo do MDOP nos [modelos administrativos de política de grupo do Microsoft Desktop Optimization Pack Pack](https://www.microsoft.com/download/details.aspx?id=55531).

2. Execute o arquivo baixado para extrair as pastas de modelo.

   **Aviso**  
   Não extraia os modelos diretamente para o diretório de implantação da política de grupo. Várias tecnologias e versões são agrupadas nesse arquivo.



3. Na pasta extraída, localize o arquivo Technology-Version. admx. Determinadas tecnologias do MDOP têm vários conjuntos de objetos de política de grupo (GPOs). Por exemplo, MBAM inclui configurações de gerenciamento MBAM e MBAM de usuário.

4. Localize o arquivo. adml apropriado por cultura de idioma (ou seja, *en* para inglês-Estados Unidos).

5. Copie os arquivos. admx e. adml para uma pasta de definição de política. Dependendo de onde você armazenar os modelos, você pode definir as configurações de política de grupo do dispositivo local ou de qualquer computador no domínio.

   **Arquivos locais.** Para definir as configurações de política de grupo do dispositivo local, copie os arquivos de modelo para os seguintes locais:

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



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. Edite as configurações de política de grupo usando o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM) para definir configurações de política de grupo para a tecnologia do MDOP. Consulte [editando as configurações de política de grupo do MBAM 2,5](editing-the-mbam-25-group-policy-settings.md) para obter mais informações.

   Para obter descrições das configurações de política de grupo, consulte [planejando requisitos de política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).


## Tópicos relacionados


[Implantando objetos de Política de Grupo do MBAM 2.5](deploying-mbam-25-group-policy-objects.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






