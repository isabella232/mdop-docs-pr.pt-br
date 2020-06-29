---
title: Planejando a implantação de servidor do MBAM 2.5
description: Planejando a implantação de servidor do MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799827"
---
# Planejando a implantação de servidor do MBAM 2.5


Este tópico lista os recursos que você implanta para as topologias autônomas e do Configuration Manager do MBAM e lista a ordem em que você precisa implementá-las. Há uma configuração recomendada para cada topologia. No entanto, você pode configurar bancos de dados e recursos do MBAM Server em configurações diferentes e entre vários servidores, dependendo dos requisitos de escalabilidade.

## Considerações importantes de planejamento para ambas as topologias


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conhecer</th>
<th align="left">Detalhes ou finalidade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Antes de iniciar a implantação, examine o seguinte:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></li>
</ul></td>
<td align="left"><p>Cada recurso MBAM tem pré-requisitos específicos que devem ser atendidos antes de iniciar a instalação do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>As chaves de recuperação do BitLocker no MBAM expiram após um único uso.</p></td>
<td align="left"><p>Um único uso significa que a chave de recuperação foi recuperada por meio do site de administração e monitoramento (também conhecido como Help Desk), do portal de autoatendimento ou do cmdlet Get- <strong> MbamBitLockerRecoveryKey do </strong> Windows PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mantenha o controle dos nomes dos computadores nos quais você configura cada recurso. Você usará essas informações em todo o processo de configuração.</p></td>
<td align="left"><p>Talvez você queira usar a <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> lista de verificação de implantação do MBAM 2,5 </a> para essa finalidade.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar apenas as configurações de política de grupo no nó MDOP MBAM (gerenciamento de BitLocker). Não altere as configurações de política de grupo no nó criptografia de unidade de disco BitLocker.</p></td>
<td align="left"><p>Se você alterar as configurações de política de grupo no nó de criptografia de unidade de disco BitLocker, o MBAM não funcionará.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Planejando a implantação do MBAM Server – topologia autônoma


Para a topologia autônoma, uma configuração de dois servidores é recomendada para ambientes de produção, embora configurações de três a quatro servidores possam ser usadas.

A infraestrutura de servidor para a topologia autônoma do MBAM contém os seguintes recursos, que devem ser configurados na ordem listada:

1.  Bancos de dados (banco de dados de conformidade e auditoria e banco de dados de recuperação)

2.  Relatórios

3.  Aplicativos Web (e seus serviços Web correspondentes)

    -   Site de administração e monitoramento

    -   Portal de autoatendimento

Para obter uma descrição desses recursos, consulte [arquitetura de alto nível do MBAM 2,5 com topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autônoma.

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Planejando a implantação do MBAM Server – topologia do Configuration Manager


Para a topologia de integração do Configuration Manager, uma configuração de três servidores é recomendada para ambientes de produção, embora as configurações de servidores adicionais possam ser usadas.

A infraestrutura de servidor para a topologia do Gerenciador de configuração do MBAM contém os seguintes recursos, que devem ser configurados ou executados na ordem listada:

1.  Bancos de dados (banco de dados de conformidade e auditoria e banco de dados de recuperação)

2.  Relatórios

3.  Aplicativos Web (e seus serviços Web correspondentes)

    -   Site de administração e monitoramento

    -   Portal de autoatendimento

4.  Integração do System Center Configuration Manager

Para obter uma descrição desses recursos, consulte [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Tópicos relacionados


[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

[Implantando a infraestrutura de servidor do MBAM 2.5](deploying-the-mbam-25-server-infrastructure.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





