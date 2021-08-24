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
ms.openlocfilehash: a0f9349391794100a670e382bb18d0713f4b5b60
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910716"
---
# <a name="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology"></a>Arquitetura de alto nível do MBAM 2.5 com topologia de Integração do Configuration Manager

Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia de Integração do Configuration Manager. Essa topologia integra o MBAM com System Center Configuration Manager. Para implantar o MBAM com a topologia autônomo, consulte Arquitetura de alto nível do [MBAM 2.5 com Topologia autônomo.](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

Para ver uma lista das versões com suporte do software mencionado neste tópico, consulte CONFIGURAções com suporte do [MBAM 2.5](mbam-25-supported-configurations.md).

**Importante**  
Windows To Go não é suportado para a instalação de topologia de Integração do Configuration Manager quando você está usando o Configuration Manager 2007.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Número recomendado de servidores e número de clientes com suporte


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
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="differences-between-configuration-manager-integration-and-stand-alone-topologies"></a>Diferenças entre a Integração do Configuration Manager e topologias autônomos


As principais diferenças entre as topologias são:

-   Os recursos de conformidade e relatório são removidos do MBAM e acessados do Configuration Manager.

-   Os relatórios são exibidos no Console de Gerenciamento do Configuration Manager, com exceção do Relatório de Auditoria de Recuperação, que você continua a exibir no Site de Administração e Monitoramento do MBAM.

## <a name="recommended-mbam-high-level-architecture-with-the-configuration-manager-integration-topology"></a>Arquitetura de alto nível do MBAM recomendada com a topologia de Integração do Configuration Manager


O diagrama e a tabela a seguir descrevem a arquitetura de alto nível recomendada para MBAM com a topologia de Integração do Configuration Manager. As implantações de várias florestas do MBAM exigem uma confiança única ou de duas vias. As confianças de ida exigem que o domínio do servidor confie no domínio do cliente.

![mbam2\-5.](images/mbam2-5-cmserver.png)

### <a name="database-server"></a>Servidor de banco de dados

#### <a name="recovery-database"></a>Banco de dados de recuperação

Esse recurso é configurado em um computador executando Windows Server e com suporte SQL Server instância.

O **Banco de Dados de** Recuperação armazena dados de recuperação coletados de computadores cliente do MBAM.

#### <a name="audit-database"></a>Banco de dados de auditoria

Esse recurso é configurado em um computador executando Windows Server e com suporte SQL Server instância.

O **Banco de Dados de** Auditoria armazena dados de atividade de auditoria coletados de computadores cliente que acessaram dados de recuperação.

#### <a name="reports"></a>Relatórios

Esse recurso é configurado em um computador executando Windows Server e com suporte SQL Server instância.

Os **Relatórios fornecem** dados de auditoria de recuperação para os computadores cliente em sua empresa. Você pode exibir relatórios do console do Configuration Manager ou diretamente SQL Server Reporting Services.

### <a name="configuration-manager-primary-site-server"></a>Servidor de site principal do Configuration Manager

System Center Configuration Manager Recurso de integração

-   Esse recurso é configurado no Servidor de Site Principal do Configuration Manager, que é o servidor de camada superior em sua infraestrutura do Configuration Manager.

-   O **Servidor do Configuration Manager** coleta as informações de inventário de hardware de computadores cliente e é usado para relatar a conformidade do BitLocker de computadores cliente.

-   Quando você executar o assistente de Instalação de Monitoramento e Administração do Microsoft BitLocker para instalar o software do servidor, a coleção de Computadores Com Suporte do MBAM, a linha de base de configuração e os relatórios são configurados no Servidor de Site Principal do Configuration Manager.

-   O **console do Configuration Manager deve** ser instalado no mesmo computador no qual você instala o software do MBAM Server.

### <a name="administration-and-monitoring-server"></a>Servidor de administração e monitoramento

#### <a name="administration-and-monitoring-website"></a>Site de administração e monitoramento

Esse recurso é configurado em um computador que executa Windows Server.

O **site administração e monitoramento** é usado para:

-   Ajude os usuários finais a recuperar o acesso aos computadores quando estão bloqueados. (Essa área do site é comumente chamada de Help Desk.)

-   Exibir o Relatório de Auditoria de Recuperação, que mostra a atividade de recuperação para computadores cliente. Outros relatórios são exibidos no console do Configuration Manager.

#### <a name="self-service-portal"></a>Portal de autoatend

Esse recurso é configurado em um computador que executa Windows Server.

O **Portal de** Autoatendenciamento é um site que permite que os usuários finais em computadores clientes faça logoff independentemente em um site para obter uma chave de recuperação se perderem ou esquecerem a senha do BitLocker.

#### <a name="monitoring-web-services-for-this-website"></a>Monitorando serviços Web para este site

Esse recurso é instalado em um computador que executa o Windows Server.

Os **serviços Web de monitoramento** são usados pelo Cliente MBAM e pelos sites para se comunicar com o banco de dados.

**Importante**<br>O Serviço Web de Monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, já que os sites do MBAM se comunicam diretamente com o Banco de Dados de Recuperação. 

 

### <a name="management-workstation"></a>Estação de trabalho de gerenciamento

#### <a name="mbam-group-policy-templates"></a>Modelos de política de grupo do MBAM

-   Os Modelos de Política de Grupo do **MBAM** são configurações de Política de Grupo que definem configurações de implementação para MBAM, que permitem gerenciar a criptografia de unidade do BitLocker.

-   Antes de executar o MBAM, você deve baixar os Modelos de Política de Grupo de Modelos de Como Obter Modelos de Política de Grupo [MDOP (.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que está executando um servidor Windows ou um sistema operacional Windows com suporte.

    **OBSERVAÇÃO**<br>A estação de trabalho não precisa ser um computador dedicado.

     

### <a name="mbam-client-and-configuration-manager-client-computer"></a>Computador cliente do MBAM Client and Configuration Manager

#### <a name="mbam-client-software"></a>Software cliente MBAM

O **cliente MBAM**:

-   Usa Objetos de Política de Grupo para impor a criptografia de unidade do BitLocker em computadores cliente na empresa.

-   Coleta a chave de recuperação do BitLocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

-   Coleta informações de recuperação e informações do computador sobre os computadores cliente.

#### <a name="configuration-manager-client"></a>Cliente do Gerenciador de Configurações

O **Cliente do Configuration Manager permite** que o Configuration Manager colete dados de compatibilidade de hardware sobre os computadores cliente e informe informações de conformidade.

 

## <a name="differences-in-mbam-deployment-for-supported-configuration-manager-versions"></a>Diferenças na implantação do MBAM para versões suportadas do Configuration Manager


Ao implantar o MBAM com a topologia de Integração do Configuration Manager, você pode instalar o MBAM em um servidor de site principal. No entanto, a instalação do MBAM funciona de forma diferente para o System Center De configuração 2012 e o Configuration Manager 2007.

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
<td align="left"><p>System Center 2012 R2 Configuration Manager</p>
<p>Systems Center 2012 Configuration Manager</p></td>
<td align="left"><p>Se você instalar o MBAM em um servidor de site primário ou em um servidor de administração central, o MBAM executará todas as ações de instalação nesse servidor de site.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007 R2</p>
<p>Configuration Manager 2007</p></td>
<td align="left"><p>Se você instalar o MBAM em um servidor de site principal que faz parte de uma hierarquia maior do Configuration Manager com um servidor pai de site central, o MBAM identificará o servidor pai do site central e executará todas as ações de instalação nesse servidor pai. A instalação inclui a verificação de pré-requisitos e a instalação dos objetos e relatórios do Configuration Manager.</p>
<p>Por exemplo, se você instalar o MBAM em um servidor de site principal filho de um servidor pai de site central, o MBAM instalará todos os objetos e relatórios do Configuration Manager no servidor pai. Se você instalar o MBAM no servidor pai, o MBAM executará todas as ações de instalação nesse servidor pai.</p></td>
</tr>
</tbody>
</table>

 

## <a name="how-mbam-works-with-configuration-manager"></a>Como o MBAM funciona com o Configuration Manager


A integração do MBAM com o Configuration Manager baseia-se em um pacote de configuração que instala os itens descritos na tabela a seguir.

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
<td align="left"><p>Os dados de configuração instalam uma linha de base de configuração, chamada "Proteção do BitLocker", que contém dois itens de configuração:</p>
<ul>
<li><p>Proteção de Unidade do Sistema Operacional BitLocker</p></li>
<li><p>Proteção de Unidades de Dados Fixas do BitLocker</p></li>
</ul>
<p>A linha de base de configuração é implantada na coleção Computadores Com Suporte do MBAM, que também é criada quando o MBAM é instalado.</p>
<p>Os dois itens de configuração fornecem a base para avaliar o status de conformidade dos computadores cliente. Essas informações são capturadas, armazenadas e avaliadas no Configuration Manager.</p>
<p>Os itens de configuração se baseiam nos requisitos de conformidade para unidades do sistema operacional e unidades de dados fixas. Os detalhes necessários para os computadores implantados são coletados para que a conformidade para esses tipos de unidade possa ser avaliada.</p>
<p>Por padrão, a linha de base de configuração avalia o status de conformidade a cada 12 horas e envia os dados de conformidade para o Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Coleção MbaM Supported Computers</p></td>
<td align="left"><p>O MBAM cria uma coleção chamada MbaM Supported Computers. A linha de base de configuração é direcionada a computadores cliente que estão nessa coleção.</p>
<p>Esta é uma coleção dinâmica. Por padrão, ele é executado a cada 12 horas e avalia a associação, com base em três critérios:</p>
<ul>
<li><p>O computador é uma versão com suporte do Windows operacional.</p></li>
<li><p>O computador é um computador físico. Não há suporte para máquinas virtuais.</p></li>
<li><p>O computador tem um TPM (Trusted Platform Module) disponível. Uma versão compatível do TPM 1.2 ou posterior é necessária para Windows 7. Windows 10, Windows 8.1, Windows 8 e Windows Para Ir não exigem um TPM.</p></li>
</ul>
<p>A coleção é avaliada em relação a todos os computadores e um subconjunto de computadores compatíveis é criado, que fornece a base para avaliação de conformidade e relatórios para a integração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Relatórios</p></td>
<td align="left"><p>Quando você configura o MBAM com a topologia de Integração do Configuration Manager, você visualiza todos os relatórios no Configuration Manager, exceto o Relatório de Auditoria de Recuperação, o último dos quais você continua a exibir no Site de Administração e Monitoramento do MBAM. Os relatórios disponíveis no Configuration Manager são:</p>
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
<td align="left"><p>BitLocker Enterprise Painel de Conformidade</p></td>
<td align="left"><p>Fornece aos administradores de IT três exibições de informações em um único relatório: Distribuição de Status de Conformidade, Não Compatível – Distribuição de Erros e Distribuição de Status de Conformidade por Tipo de Unidade. Opções de detalhamento no relatório permitem que os administradores de IT cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Detalhes de conformidade</p></td>
<td align="left"><p>Permite aos administradores de IT exibir informações sobre o status de conformidade de criptografia BitLocker da empresa e inclui o status de conformidade para cada computador. Opções de detalhamento no relatório permitem que os administradores de IT cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade com o computador BitLocker</p></td>
<td align="left"><p>Permite aos administradores de IT exibir um computador individual e determinar por que ele foi relatado com um status compatível ou não compatível. O relatório também exibe o estado de criptografia das unidades do sistema operacional e unidades de dados fixas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Resumo de Conformidade</p></td>
<td align="left"><p>Permite aos administradores de IT exibir o status da conformidade da política do MBAM na empresa. O estado de cada computador é avaliado e o relatório mostra um resumo da conformidade de todos os computadores na empresa em relação à política. Opções de detalhamento no relatório permitem que os administradores de IT cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <a name="related-topics"></a>Tópicos relacionados


[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

[Arquitetura de alto nível do MBAM 2.5 com topologia autônoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Recursos ilustrados de uma implantação do MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <a name="got-a-suggestion-for-mbam"></a>Tem uma sugestão para MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, use o [Fórum technet do MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




