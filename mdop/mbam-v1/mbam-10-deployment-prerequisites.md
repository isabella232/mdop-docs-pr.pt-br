---
title: Pré-requisitos para implantação do MBAM 1.0
description: Pré-requisitos para implantação do MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799117"
---
# Pré-requisitos para implantação do MBAM 1.0


Antes de começar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), verifique se você atende aos pré-requisitos necessários para instalar o produto. Esta seção contém informações para ajudá-lo a preparar com êxito o ambiente de computação antes de implantar os recursos de clientes e servidores do MBAM.

## Pré-requisitos de instalação para recursos do MBAM Server


Cada um dos recursos do servidor MBAM tem pré-requisitos específicos que devem ser atendidos para que possam ser instalados com êxito. A instalação do MBAM verifica se todos os pré-requisitos são atendidos antes do início da instalação.

### Pré-requisitos de instalação do servidor de administração e monitoramento

A tabela a seguir contém os pré-requisitos de instalação do MBAM Administration and Monitoring Server:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Função do Windows ServerWeb Server</strong></p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor compatível com o recurso de servidor administração e monitoramento do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ferramentas de gerenciamento do servidor Web (IIS)</strong></p></td>
<td align="left"><p><strong>Ferramentas e scripts de gerenciamento do IIS</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Serviços de função de servidor Web</strong></p></td>
<td align="left"><p><strong>Recursos comuns de HTTP:</strong></p>
<ul>
<li><p>Conteúdo estático</p></li>
<li><p>Documento padrão</p></li>
</ul>
<p><strong>Desenvolvimento de aplicativos:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidade .NET</p></li>
<li><p>Extensões ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Segurança</strong></p>
<ul>
<li><p>Autenticação do Windows</p></li>
<li><p>Filtragem de solicitações</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Recursos do Windows Server</strong></p></td>
<td align="left"><p><strong>Recursos do Microsoft .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Ativação do WCF</p>
<ul>
<li><p>Ativação de HTTP</p></li>
<li><p>Ativação não HTTP</p></li>
</ul></li>
</ul>
<p><strong>Serviço de Ativação de Processos do Windows</strong></p>
<ul>
<li><p>Modelo de processo</p></li>
<li><p>Ambiente .NET</p></li>
<li><p>APIs de configuração</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Observação**  Para obter uma lista dos sistemas operacionais compatíveis, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).

 

### Pré-requisitos de instalação dos relatórios de conformidade e auditoria

Os relatórios de conformidade e auditoria devem ser instalados em uma versão com suporte do SQLServer. Os pré-requisitos de instalação para esse recurso incluem SQL Server Reporting Services (SSRS).

O SSRS deve ser instalado e executado durante a instalação do MBAM Server. O SSRS também deve ser configurado no modo "nativo", não no modo "não configurado" ou "SharePoint".

**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).

 

### Pré-requisitos de instalação para o banco de dados de recuperação e hardware

O banco de dados de recuperação e de hardware deve ser instalado em uma versão com suporte do SQLServer.

O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do servidor MBAM. O recurso de criptografia de dados transparente (TDE) deve estar habilitado.

**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).

 

O recurso TDE SQLServer executa a criptografia e a descriptografia de entrada/saída (e/s) em tempo real dos arquivos de dados e log. O TDE protege os dados que são "em repouso", que incluem os dados e os arquivos de log. Ele fornece a capacidade de obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.

**Observação**  Como o TDE executa a descriptografia em tempo real das informações do banco de dados, as informações da chave de recuperação ficarão visíveis se a conta na qual você está conectado tiver permissões para o banco de dados quando você exibir as tabelas de informações de chave de recuperação do SQL.

 

### Pré-requisitos de instalação para o banco de dados de conformidade e auditoria

O banco de dados de auditoria e conformidade deve ser instalado em uma versão com suporte do SQLServer.

O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do MBAM Server.

**Observação**  Para obter uma lista dos sistemas operacionais compatíveis e das versões do SQLServer, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).

 

## Pré-requisitos de instalação para clientes MBAM


Os pré-requisitos necessários que você precisa atender antes de iniciar a instalação do cliente do MBAM são os seguintes:

-   Recurso de TPM (Trusted Platform Module) v 1.2

-   O chip TPM deve estar ativado no BIOS e deve ser redefinido do sistema operacional. Para obter mais informações, consulte a documentação do BIOS.

**Aviso**  Verifique se o teclado, o mouse e o vídeo estão conectados diretamente ao computador, em vez de a um botão de teclado, vídeo, mouse (KVM). Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.

 

## Tópicos relacionados


[Planejar a implantação do MBAM 1.0](planning-to-deploy-mbam-10.md)

[Configurações com suporte no MBAM 1.0](mbam-10-supported-configurations.md)

 

 





