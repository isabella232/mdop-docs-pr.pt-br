---
title: Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager
description: Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799737"
---
# Arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager

Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia de integração do Configuration Manager. Essa topologia integra o MBAM com o System Center Configuration Manager. Para implantar o MBAM com a topologia autônoma, consulte [arquitetura de alto nível do MBAM 2,5 com topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autônoma.

Para obter uma lista das versões com suporte do software mencionadas neste tópico, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

**Importante**  Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.

 

## Número recomendado de servidores e número de clientes com suporte


O número recomendado de servidores e o número de clientes com suporte em um ambiente de produção é o seguinte:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitetura recomendada</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número de servidores e outros computadores</p></td>
<td align="left"><p>Três servidores</p>
<p>Uma estação de trabalho</p></td>
</tr>
<tr class="even">
<td align="left"><p>Número de computadores cliente com suporte</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Diferenças entre a integração do Configuration Manager e as topologias autônomas


As principais diferenças entre as topologias são:

-   Os recursos de conformidade e relatório são removidos do MBAM e são acessados do Configuration Manager.

-   Os relatórios são exibidos no console de gerenciamento do Configuration Manager, com exceção do relatório de auditoria de recuperação, que você continua a exibir no site de administração e monitoramento do MBAM.

## Arquitetura de alto nível MBAM recomendada com a topologia de integração do Configuration Manager


O diagrama e a tabela a seguir descrevem a arquitetura de alto nível recomendada para o MBAM com a topologia de integração do Configuration Manager. MBAM implantações de várias florestas exigem confiança unidirecional ou bidirecional. As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente.

![mbam2\-5](images/mbam2-5-cmserver.png)

### Servidor de banco de dados

#### Banco de dados de recuperação

Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.

O **banco** de dados de recuperação armazena dados de recuperação coletados de computadores cliente do MBAM.

#### Banco de dados de auditoria

Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.

O **banco** de dados de auditoria armazena dados de atividades de auditoria coletados de computadores cliente que acessam dados de recuperação.

#### Relatórios

Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.

Os **relatórios** fornecem dados de auditoria de recuperação para os computadores cliente da sua empresa. Você pode exibir relatórios do console do Configuration Manager ou diretamente do SQL Server Reporting Services.

### Servidor de site primário do Configuration Manager

Recurso de integração do System Center Configuration Manager

-   Esse recurso está configurado no servidor de site primário do Configuration Manager, que é o servidor de nível superior na infraestrutura do Configuration Manager.

-   O **servidor do Configuration Manager** coleta as informações do inventário de hardware dos computadores cliente e é usada para denunciar a compatibilidade do BitLocker em computadores cliente.

-   Quando você executa o assistente de configuração de administração e administração do Microsoft BitLocker para instalar o software do servidor, o conjunto de computadores com suporte MBAM, a linha de base de configuração e os relatórios são configurados no servidor de site primário do Configuration Manager.

-   O **console do Configuration Manager** deve ser instalado no mesmo computador em que você instala o software MBAM Server.

### Servidor de administração e monitoramento

#### Site de administração e monitoramento

Esse recurso é configurado em um computador que executa o Windows Server.

O **site de administração e monitoramento** é usado para:

-   Ajude os usuários finais a recuperarem o acesso aos seus computadores quando estiverem bloqueados. (Essa área do site geralmente é chamada de suporte técnico).

-   Exibir o relatório de auditoria de recuperação, que mostra a atividade de recuperação para computadores cliente. Outros relatórios são exibidos no console do Configuration Manager.

#### Portal de autoatendimento

Esse recurso é configurado em um computador que executa o Windows Server.

O **portal de autoatendimento** é um site que permite aos usuários finais nos computadores cliente fazerem logon independentemente em um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.

#### Monitorando serviços Web para este site

Esse recurso é instalado em um computador que executa o Windows Server.

Os **Serviços Web de monitoramento** são usados pelo cliente MBAM e pelos websites para se comunicar ao banco de dados.

**Importante**<br>O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois os sites do MBAM se comunicam diretamente com o banco de dados de recuperação. 

 

### Estação de trabalho de gerenciamento

#### Modelos de política de grupo MBAM

-   Os **modelos de política de grupo do MBAM** são configurações de política de grupo que definem configurações de implementação para MBAM, que permitem que você gerencie a criptografia de unidade de disco BitLocker.

-   Antes de executar o MBAM, você deve baixar os modelos de política de grupo de [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que esteja executando um servidor Windows ou sistema operacional Windows com suporte.

    **OBSERVAÇÃO**<br>A estação de trabalho não precisa ser um computador dedicado.

     

### Cliente MBAM e computador cliente do Configuration Manager

#### Software cliente MBAM

O **cliente MBAM**:

-   Usa objetos de política de grupo para impor a criptografia de unidade de disco BitLocker em computadores cliente da empresa.

-   Coleta a chave de recuperação do BitLocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta informações de recuperação e informações do computador dos computadores cliente.

#### Cliente do Gerenciador de Configurações

O **cliente do Configuration Manager** permite que o Configuration Manager colete dados de compatibilidade de hardware sobre os computadores cliente e informe as informações de conformidade.

 

## Diferenças na implantação do MBAM para versões do Gerenciador de configurações com suporte


Ao implantar o MBAM com a topologia de integração do Configuration Manager, você pode instalar o MBAM em um servidor de site primário. No entanto, a instalação do MBAM funciona de forma diferente para o Gerenciador de configuração do Center2012 e Manager2007 de configuração do sistema.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do Configuration Manager</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gerenciador de configuração do sistema Center2012 R2</p>
<p>Gerenciador de configuração do Center2012 do sistema</p></td>
<td align="left"><p>Se você instalar o MBAM em um servidor de site primário ou em um servidor de administração central, o MBAM executará todas as ações de instalação nesse servidor de site.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manager2007 de configuração R2</p>
<p>Manager2007 de configuração</p></td>
<td align="left"><p>Se você instalar o MBAM em um servidor de site primário que faz parte de uma hierarquia do Configuration Manager maior com um servidor pai do site central, MBAM identificará o servidor pai do site central e executará todas as ações de instalação nesse servidor pai. A instalação inclui verificar pré-requisitos e instalar objetos e relatórios do Configuration Manager.</p>
<p>Por exemplo, se você instalar o MBAM em um servidor de site primário que seja filho de um servidor pai de site central, o MBAM instalará todos os objetos e relatórios do Configuration Manager no servidor pai. Se você instalar o MBAM no servidor pai, o MBAM executará todas as ações de instalação nesse servidor pai.</p></td>
</tr>
</tbody>
</table>

 

## Como o MBAM funciona com o Configuration Manager


A integração do MBAM com o Configuration Manager se baseia em um pacote de configuração que instala os itens descritos na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Itens instalados no Configuration Manager</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dados de configuração</p></td>
<td align="left"><p>Os dados de configuração instalam uma linha de base de configuração, chamada "proteção BitLocker", que contém dois itens de configuração:</p>
<ul>
<li><p>Proteção de unidade do sistema operacional BitLocker</p></li>
<li><p>Proteção de unidades de dados fixas do BitLocker</p></li>
</ul>
<p>A linha de base de configuração é implantada no conjunto de computadores com suporte MBAM, que também é criado quando o MBAM está instalado.</p>
<p>Os dois itens de configuração fornecem a base para avaliar o status de conformidade dos computadores cliente. Essas informações são capturadas, armazenadas e avaliadas no Configuration Manager.</p>
<p>Os itens de configuração se baseiam nos requisitos de conformidade para unidades do sistema operacional e unidades de dados fixas. Os detalhes necessários para os computadores implantados são coletados para que a conformidade desses tipos de unidade possa ser avaliada.</p>
<p>Por padrão, a linha de base de configuração avalia o status de conformidade every12 horas e envia os dados de conformidade para o Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conjunto de computadores com suporte MBAM</p></td>
<td align="left"><p>MBAM cria uma coleção chamada MBAM computadores com suporte. A linha de base de configuração é direcionada para computadores cliente que estão nesta coleção.</p>
<p>Esta é uma coleção dinâmica. Por padrão, ele executa every12 horas e avalia a associação, com base em três critérios:</p>
<ul>
<li><p>O computador é uma versão com suporte do sistema operacional Windows.</p></li>
<li><p>O computador é um computador físico. Não há suporte para máquinas virtuais.</p></li>
<li><p>O computador tem um TPM (Trusted Platform Module) que está disponível. Uma versão compatível do TPM 1.2 ou posterior é necessária para o Windows7. O Windows10, o Windows 8.1, o Windows8 e o Windows to go não exigem um TPM.</p></li>
</ul>
<p>A coleção é avaliada em todos os computadores e um subconjunto de computadores compatíveis é criado, o que fornece a base para a avaliação de conformidade e a geração de relatórios para a integração com o MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Relatórios</p></td>
<td align="left"><p>Quando você configura o MBAM com a topologia de integração do Configuration Manager, você vê todos os relatórios no Configuration Manager, exceto o relatório de auditoria de recuperação, o último que você continua a exibir no site de administração e monitoramento do MBAM. Os relatórios disponíveis no Configuration Manager são:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Relatório</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Painel de conformidade do BitLocker Enterprise</p></td>
<td align="left"><p>Fornece aos administradores de ti três exibições de informações em um único relatório: distribuição de status de conformidade, não compatível – distribuição de erros e distribuição de status de conformidade por tipo de unidade. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes de conformidade corporativa do BitLocker</p></td>
<td align="left"><p>Permite que os administradores de ti exibam informações sobre o status de conformidade de criptografia do BitLocker da empresa e inclui o status de conformidade de cada computador. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade do computador BitLocker</p></td>
<td align="left"><p>Permite que os administradores de ti visualizem um computador individual e determine por que ele foi reportado com um status de conformidade ou não compatível. O relatório também exibe o estado de criptografia das unidades de sistema operacional e unidades de dados fixas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Resumo de conformidade empresarial do BitLocker</p></td>
<td align="left"><p>Permite que os administradores de ti exibam o status da conformidade da política do MBAM na empresa. O estado de cada computador é avaliado, e o relatório mostra um resumo da conformidade de todos os computadores na empresa em relação à política. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados


[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitetura de alto nível do MBAM 2.5 com topologia autônoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Recursos ilustrados de uma implantação do MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




