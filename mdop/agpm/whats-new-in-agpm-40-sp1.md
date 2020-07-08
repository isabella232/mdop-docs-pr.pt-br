---
title: Novidades do AGPM 4.0 SP1
description: Novidades do AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797268"
---
# Novidades do AGPM 4.0 SP1


Este conteúdo "o que há de novo" descreve melhorias e configurações com suporte para o gerenciamento avançado de política de grupo (AGPM) 4,0 SP1 da Microsoft. Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, esse conteúdo deve ser considerado autoritativo e deve substituir o conteúdo incluído neste produto.

## <a href="" id="what-s-new"></a>O que há de novo


O AGPM 4,0 SP1 é compatível com os seguintes aprimoramentos:

### Extensões novas e alteradas do lado do cliente

As extensões do lado do cliente da política de grupo (CSEs) foram adicionadas ou alteradas para o AGPM dar suporte a novas políticas de grupo no Windows 8 e no Windows Server 2012. Essas políticas de grupo permitem que os administradores de política de grupo gerenciem e controlem as configurações de política de grupo específicas do Windows 8 que mudam entre dois objetos de política de grupo (GPOs) ou modelos. Você também pode criar GPOs personalizados, com configurações específicas do Windows 8, e configurar e salvar os GPOs como um modelo. Para exibir seu CSEs, use as configurações e os relatórios de diferença disponíveis no cliente do AGPM 4,0 SP1.

As extensões nova e alterada do lado do cliente da política de grupo são:

-   **Política de acesso central:** Permite que os administradores de política de grupo especifiquem políticas de acesso central em servidores de política de grupo, por exemplo, servidores de arquivos. A política de acesso central é uma política de autorização especificada por um item de GPO e aplicada a destinos de política para facilitar o acesso centralizado e o controle de recursos. Essas políticas de acesso central devem ser configuradas em um computador cliente de política de grupo no Active Directory. Uma política de grupo distribui o conhecimento de uma política de acesso central aplicável aos computadores que precisam aplicá-la.

-   **Alterações nas políticas de resolução de nomes:** Permite que os administradores de política de grupo definam as configurações de segurança do DNS e do DirectAccess em computadores cliente DNS. Novas guias para definir configurações de servidor DNS genérico e configurações de codificação foram adicionadas.

-   **Alterações de preferência de política de Grupo:** Adiciona suporte para a configuração e o gerenciamento de configurações do Internet Explorer 10 que foram adicionadas para o Windows 8.

-   **Conexões de aplicativos remotos e da área de trabalho:** Permite que os administradores de política de grupo especifiquem a URL de conexão padrão usada para conexões de aplicativos e área de trabalho remotos.

-   **Opções de inicialização do Windows to go:** Permite que os administradores de política de grupo configurem se o computador será inicializado no Windows to go se um dispositivo USB que contém um espaço de trabalho do Windows to go estiver conectado.

-   **Opções de hibernação do Windows to go:** Permite que os administradores de política de grupo configurem se um computador pode usar o estado de suspensão de hibernação (S4) quando o computador é iniciado a partir de um espaço de trabalho do Windows to go.

### Feedback do cliente e pacote cumulativo de hotfix

O AGPM 4,0 SP1 inclui um pacote cumulativo de correções para solucionar problemas encontrados desde o lançamento do AGPM 4,0. O AGPM 4,0 SP1 contém as mais recentes correções até e incluindo o gerenciamento avançado de política de grupo da Microsoft 4,0 hotfix 1.

### Relatórios de configurações e diferença mostram novas extensões de política de grupo

As novas extensões de política de grupo foram adicionadas às configurações e aos relatórios de diferença.

### Mudanças e suporte do instalador

As alterações e o suporte para o instalador do AGPM 4,0 SP1 são:

-   Se você instalar o AGPM 4,0 SP1 no Windows 8 ou no Windows Server 2012, o instalador do AGPM verificará se o software de pré-requisito necessário (console de gerenciamento de política de grupo e a estrutura .NET 3,5) está instalado. Se esses pré-requisitos não estiverem instalados, a instalação do AGPM 4,0 SP1 será bloqueada.

-   Quando você instala o AGPM 4,0 SP1, a ativação do WCF, a ativação não HTTP e o serviço de ativação de processos do Windows são habilitados automaticamente.

-   Nos sistemas operacionais cliente Windows Vista, Windows 7 e Windows 8, baixe a versão apropriada do kit de ferramentas de administração do sistema remoto para o sistema operacional antes de instalar o AGPM 4,0 SP1.

-   Há suporte para a compatibilidade com versões anteriores com sistemas operacionais com suporte.

### Capacidade de atualizar ou atualizar para o AGPM 4,0 SP1 sem digitar novamente os parâmetros de configuração

Você pode atualizar o cliente do AGPM ou o servidor para o AGPM 4,0 SP1 somente do AGPM 4,0 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de "atualização inteligente"), conforme mostrado na tabela a seguir. Se você estiver atualizando para o AGPM 4,0 SP1 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a "atualização clássica", que exige que você insira novamente os parâmetros de configuração. Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolher qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350)e atualizar o sistema operacional conforme apropriado antes de realizar uma atualização.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versão do AGPM a partir da qual você pode atualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Não aplicável</p></td>
<td align="left"><p>Atualização inteligente</p></td>
</tr>
</tbody>
</table>

 

## Configurações compatíveis


O AGPM dá suporte às configurações na tabela a seguir. Embora o AGPM dê suporte a configurações mistas, é altamente recomendável que você execute o cliente e o servidor do AGPM na mesma família de sistema operacional, por exemplo, Windows 8 com Windows Server 2012, Windows 7 com Windows Server 2008 R2 e assim por diante.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurações com suporte para o servidor AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Configurações com suporte para o cliente do AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Suporte do AGPM 4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7 ou Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou no Windows 7 ou no Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7 ou Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou no Windows 7 ou no Windows 8</p></td>
</tr>
</tbody>
</table>

 

## Pré-requisitos para a instalação do AGPM 4,0 SP1


A tabela a seguir descreve o comportamento no Windows 8 dos instaladores do cliente e do cliente do AGPM 4,0 SP1 quando o .NET 3,5 ou o console de gerenciamento de política de grupo (RSAT) estiver ausente.

**Cliente do AGPM 4,0 SP1**

**Servidor do AGPM 4,0 SP1**

**Sistema operacional**

**.NET**

**RSAT**

**.NET**

**RSAT**

**Windows 8**

Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado ou instalado no sistema, o instalador bloqueará a instalação.

Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado ou instalado no sistema, o instalador bloqueará a instalação.

**Windows Server 2012**

Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.

Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.

 

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

[Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





