---
title: Avaliação do MBAM 2.0
description: Avaliação do MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799532"
---
# Avaliação do MBAM 2.0


Antes de implantar o Microsoft BitLocker Administration and Monitoring (MBAM) em um ambiente de produção, você deve avaliá-lo em um ambiente de teste. As informações neste tópico podem ser usadas para configurar a administração e o monitoramento do Microsoft BitLocker com uma topologia autônoma em um ambiente de teste de servidor único para fins de avaliação apenas. Uma topologia de servidor único não é recomendada para ambientes de produção.

Para obter instruções sobre como implantar o MBAM em um ambiente de teste, consulte [como instalar e configurar o MBAM em um único servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Configurando o ambiente de teste


Mesmo que você esteja configurando uma instância de não-produção de MBAM para avaliar em um ambiente de teste, você ainda deve verificar se atendeu os pré-requisitos e requisitos de hardware e software. Antes de iniciar a instalação, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md)e [preparando seu ambiente para o MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

### Planejar uma implantação de avaliação do MBAM

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
<td align="left"><p>Examine as informações de introdução sobre o MBAM para obter noções básicas sobre o produto antes de começar a planejar a implantação.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Introdução ao MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje os pré-requisitos de implantação do MBAM 2,0 e prepare o ambiente de computação.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Pré-requisitos para implantação do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e configure MBAM requisitos da política de grupo.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planejar Requisitos de Política de Grupo do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e crie os grupos de segurança do ActiveDirectoryDomainServices necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planejamento para Funções de Administrador do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plano para a implantação de recursos do MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Planejar implantação de servidor MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plano para implantar a implantação do cliente MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planejar implantação de cliente MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Executar uma implantação de avaliação do MBAM

Depois de concluir as instalações de pré-requisitos de software e planejamento necessárias para preparar o ambiente de computação para a instalação do MBAM, você pode começar a implantação de avaliação do MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação de recursos do MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurações com suporte no MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Execute a instalação do MBAM para implantar recursos do MBAM Server em um único servidor para fins de avaliação.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">Como instalar e configurar o MBAM em um servidor único</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Adicione os grupos de segurança do ActiveDirectoryDomainServices, que você criou durante a fase de planejamento, aos grupos locais do recurso de servidor local adequado MBAM no novo servidor MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planejando funções de administrador do MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> como gerenciar funções de administrador do MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Criar e implantar objetos obrigatórios de política de grupo do MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Implantar Objetos de Política de Grupo no MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implantar o software cliente do MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Implantando o Cliente do MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Configurar computadores de laboratório para avaliação do MBAM


Esta seção contém informações que podem ser usadas para acelerar o relatório de status do cliente MBAM. No entanto, essas modificações devem ser usadas somente para fins de teste.

**Observação**  As informações na seção a seguir descrevem como modificar o registro do Windows. Usar o editor do registro incorretamente pode causar sérios problemas que podem exigir a reinstalação do Windows. A Microsoft não pode garantir que os problemas resultantes do uso incorreto do editor do registro possam ser resolvidos. Use o editor do registro por sua conta e risco.

 

### Modificar as configurações de frequência de relatório de status do cliente do MBAM

As frequências de reutilização de cliente e status de ativação do cliente MBAM têm um valor mínimo de 90 minutos quando são definidas usando a política de grupo. Você pode usar o registro do Windows para alterar essas frequências para um valor inferior em computadores cliente do MBAM para ajudar a acelerar o teste.

Para modificar as configurações de frequência de relatório de status do cliente do MBAM:

1.  Use um editor de registro para navegar até **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.

2.  Altere os valores de **ClientWakeupFrequency** e **StatusReportingFrequency** para **1** como o valor mínimo com suporte do cliente. Essa alteração faz com que o cliente do MBAM denuncie a cada minuto.

3.  Reinicie o **serviço de cliente de gerenciamento de BitLocker**.

**Observação**  Para definir valores que sejam tão baixos, você deve defini-los no registro manualmente.

 

### Modificar o atraso de inicialização do serviço do cliente MBAM

Além das frequências de reativação do cliente MBAM e status, há um atraso aleatório de até 90 minutos quando o serviço de agente cliente do MBAM é iniciado em computadores cliente. Se você não quiser o atraso aleatório, crie um valor **DWORD** de **NoStartupDelay** em **HKLM\\Software\\Microsoft\\MBAM**, defina seu valor como **1**e, em seguida, reinicie o serviço de cliente de **Gerenciamento de BitLocker**.

## Tópicos relacionados


[Introdução ao MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





