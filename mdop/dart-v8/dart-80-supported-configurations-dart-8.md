---
title: Configurações compatíveis do DaRT 8.0
description: Configurações compatíveis do DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799370"
---
# Configurações compatíveis do DaRT 8.0


Este tópico especifica o software de pré-requisito e os requisitos de configuração com suporte que são necessários para instalar e executar o Microsoft Diagnostic and Recovery Toolset (DaRT) 8,0 em seu ambiente. Os requisitos do sistema operacional e os requisitos do sistema necessários para executar o DaRT 8,0 são especificados. Para obter informações sobre pré-requisitos que você precisa considerar para criar a imagem de recuperação do DaRT, consulte [planejando criar a imagem de recuperação do dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).

Para configurações compatíveis que se aplicam a versões posteriores, consulte a documentação da versão aplicável.

Você pode instalar o DaRT de uma de duas maneiras. Você pode instalar toda a funcionalidade em um computador administrador de ti, no qual executará todas as tarefas associadas à execução do DaRT. Você também pode instalar, no computador administrador, somente a funcionalidade DaRT que cria a imagem de recuperação e, em seguida, instalar a funcionalidade usada para executar o DaRT (ou seja, o Visualizador de conexão remota do DaRT) em um computador de suporte técnico.

## <a href="" id="---------dart-8-0-prerequisite-software"></a> Software de pré-requisito DaRT 8,0


Certifique-se de que os seguintes pré-requisitos são atendidos antes de instalar o DaRT.

### Pré-requisitos do computador administrador

A tabela a seguir lista os pré-requisitos de instalação do computador administrador quando você está instalando o DaRT 8,0 e todas as ferramentas do DaRT.

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
<td align="left"><p><strong>Kit de avaliação e desenvolvimento do Windows (ADK)</strong></p></td>
<td align="left"><p>Obrigatório para o assistente de recuperação de imagem de DaRT. Contém as ferramentas de implantação, que são usadas para personalizar, implantar e fazer a manutenção de imagens do Windows e contém o ambiente de pré-instalação do Windows (Windows PE). O ADK não será necessário se você estiver instalando apenas o Visualizador de conexão remota e/ou o Crash Analyzer.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Exigido pelo assistente de imagem de recuperação DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Kit de desenvolvimento do Windows ou kit de desenvolvimento de software (opcional)</strong></p></td>
<td align="left"><p>O Crash Analyzer requer as ferramentas de depuração do Windows 8 do kit de driver do Windows para analisar os arquivos de despejo de memória.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Imagem ISO do Windows 8 64-bit</strong></p></td>
<td align="left"><p>O DaRT requer a imagem do Windows RE (ambiente de recuperação do Windows) da mídia do Windows 8. Baixe a versão de 32 bits ou 64 bits do Windows 8, dependendo do tipo de imagem de recuperação do DaRT que você deseja criar. Se você oferecer suporte a ambos os tipos de sistema em seu ambiente, baixe ambas as versões do Windows 8.</p></td>
</tr>
</tbody>
</table>

 

### Pré-requisitos do computador de suporte técnico

A tabela a seguir lista os pré-requisitos de instalação do computador com suporte técnico quando você está executando o Visualizador de conexão remota DaRT 8,0.

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
<td align="left"><p><strong>Visualizador de conexão remota DaRT 8,0</strong></p></td>
<td align="left"><p>Deve ser instalado em um sistema operacional Windows 8.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Exigido pelo assistente de imagem de recuperação DaRT</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ferramentas de depuração para Windows</strong></p></td>
<td align="left"><p>Obrigatório apenas se você estiver instalando a ferramenta Crash Analyzer</p></td>
</tr>
</tbody>
</table>

 

### Pré-requisitos do computador do usuário final

Não há nenhum software obrigatório que deve ser instalado em computadores de usuário final, exceto o sistema operacional Windows 8.

## <a href="" id="---------dart-operating-system-requirements"></a> Requisitos do sistema operacional DaRT


### Requisitos do sistema de computador administrador

A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do administrador do DaRT.

**Observação**  Certifique-se de atribuir espaço suficiente para as ferramentas adicionais que você deseja instalar no computador administrador.

 

**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
<th align="left">Requisitos do Sistema Operacional</th>
<th align="left">Requisito de RAM para executar o DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão, corporativo, Data Center</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>512 MB</p></td>
<td align="left"><p>1.0 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Requisitos do sistema do computador de suporte técnico DaRT

Se você permitir que um suporte técnico ajude a solucionar problemas com computadores remotamente, você deve ter o Visualizador de conexão remota instalado no computador de suporte. Opcionalmente, você pode instalar a ferramenta Crash Analyzer no computador de suporte técnico.

O DaRT 8,0 permite que um trabalhador de suporte técnico se conecte a um computador DaRT 8,0 usando o DaRT 7,0 ou o DaRT 8,0 Remote Connection Viewer. O Visualizador de conexão remota do DaRT 7,0 exige um sistema operacional Windows 7, enquanto o Visualizador de conexão remota do DaRT 8,0 requer o Windows 8. O Visualizador de conexão remota do DaRT 8,0 e todas as outras ferramentas do DaRT 8,0 podem ser instaladas apenas em um computador com Windows 8.

A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do DaRT Help Desk.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
<th align="left">Requisitos do Sistema Operacional</th>
<th align="left">Requisitos de RAM para executar o DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (somente com o Visualizador de conexão remota 8,0)</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (somente com o Visualizador de conexão remota 7,0)</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits ou 32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão, corporativo, Data Center</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>51</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

O DaRT também tem os seguintes requisitos mínimos de hardware para o computador do usuário final:

Uma unidade de CD ou DVD ou uma porta USB-necessária apenas se você estiver implantando o DaRT na sua empresa usando um CD, DVD ou USB.

Suporte do BIOS para iniciar o computador a partir de um CD ou DVD, uma unidade flash USB ou de uma partição remota ou de recuperação.

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> Requisitos do sistema para o computador de usuário final do DaRT

A janela do conjunto de ferramentas de diagnóstico e recuperação do DaRT requer que o computador do usuário final use um dos seguintes sistemas operacionais juntamente com a quantidade especificada de memória do sistema disponível para o DaRT:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
<th align="left">Requisitos do Sistema Operacional</th>
<th align="left">Requisitos de RAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas as edições</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão, corporativo, Data Center</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>512 MB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejamento da implantação do DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





