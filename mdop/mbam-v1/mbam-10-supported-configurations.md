---
title: Configurações com suporte no MBAM 1.0
description: Configurações com suporte no MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799772"
---
# Configurações com suporte no MBAM 1.0


Este tópico especifica os requisitos necessários para instalar e executar o Microsoft BitLocker Administration and Monitoring (MBAM) em seu ambiente.

## <a href="" id="---------mbam-server-system-requirements"></a> Requisitos do sistema do MBAM Server


### Requisitos do sistema operacional do servidor

A tabela a seguir lista os sistemas operacionais suportados para a instalação do Microsoft BitLocker Administration and Monitoring Server.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou servidor Web</p></td>
<td align="left"><p>SP2 somente</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou servidor Web</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Aviso**  
Não há suporte para a instalação de serviços, relatórios ou bancos de dados do MBAM em um computador controlador de domínio.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>Requisitos de memória de acesso randômico (RAM) do servidor

Não há nenhuma necessidade de RAM específica para a instalação do MBAM Server.

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de banco de dados do SQL Server

A tabela a seguir lista as versões do SQL Server com suporte para a instalação do recurso MBAM Server.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Recurso do servidor MBAM</th>
<th align="left">Versão do SQL Server</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Relatórios de conformidade e auditoria</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter ou edição para desenvolvedores</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Recuperação e banco de dados de hardware</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter ou edição para desenvolvedores</p>
<div class="alert">
<strong>Importante</strong><br/><p>Não há suporte para as edições padrão do SQL Server para a recuperação de MBAM e instalação de recursos do servidor de banco de dados de hardware</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Banco de dados de auditoria e conformidade</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter ou edição para desenvolvedores</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Requisitos do sistema do cliente MBAM


### Requisitos do sistema operacional do cliente

A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MBAM.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Edição Enterprise</p></td>
<td align="left"><p>Nenhum, SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Última edição</p></td>
<td align="left"><p>Nenhum, SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Requisitos de RAM do cliente

Não há requisitos de RAM específicos para a instalação do cliente do MBAM.

## Tópicos relacionados


[Planejar a implantação do MBAM 1.0](planning-to-deploy-mbam-10.md)

[Pré-requisitos para implantação do MBAM 1.0](mbam-10-deployment-prerequisites.md)









