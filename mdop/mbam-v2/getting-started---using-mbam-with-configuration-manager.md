---
title: Introdução – Como usar o MBAM com o Configuration Manager
description: Introdução – Como usar o MBAM com o Configuration Manager
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799618"
---
# Introdução – Como usar o MBAM com o Configuration Manager


Ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode escolher uma topologia que integre o MBAM com o Configuration Manager 2007 ou SystemCenter2012 ConfigurationManager. Para obter uma lista das versões compatíveis do Configuration Manager que o MBAM oferece suporte, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Na topologia integrada, os recursos de relatórios e conformidade de hardware são removidos do MBAM e são acessados do Configuration Manager.

**Importante**  Não há suporte para o Windows to go ao instalar a topologia integrada do MBAM com o Configuration Manager 2007.

 

## Usando o MBAM com o Configuration Manager


A integração do MBAM é baseada em um novo pacote de configuração que instala os três itens a seguir no Configuration Manager 2007 ou SystemCenter2012 ConfigurationManager, que estão descritos em detalhes nas seguintes seções:

Dados de configuração que consistem em itens de configuração e uma linha de base de configuração

Coleção

Relatórios

### Dados de configuração

Os dados de configuração instalam uma linha de base de configuração, chamada "proteção BitLocker", que contém dois itens de configuração: "proteção de unidade de sistema operacional BitLocker" e "proteção de unidades de dados fixas BitLocker". A linha de base de configuração é implantada na coleção, que também é criada quando o MBAM está instalado. Os dois itens de configuração fornecem a base para avaliar o status de conformidade dos computadores cliente. Essas informações são capturadas, armazenadas e avaliadas no Configuration Manager. Os itens de configuração se baseiam nos requisitos de conformidade para unidades do sistema operacional (OSDs) e unidades de dados fixos (FDDs). Os detalhes necessários para os computadores implantados são coletados para que a conformidade desses tipos de unidade possa ser avaliada. Por padrão, a linha de base de configuração avalia o status de conformidade a cada 12 horas e envia os dados de conformidade para o Configuration Manager.

### Coleção

MBAM cria uma coleção chamada MBAM computadores com suporte. A linha de base de configuração é direcionada para computadores cliente que estão nesta coleção. Essa é uma coleção dinâmica que, por padrão, é executada a cada 12 horas e avalia a associação. A associação se baseia em três critérios:

-   É uma versão com suporte do sistema operacional Windows. Atualmente, o MBAM oferece suporte somente ao Windows 7 Enterprise e ao Windows 7 Ultimate, ao Windows 8 Enterprise e ao Windows to go, quando o Windows to go estiver em execução no Windows 8 Enterprise.

-   É um computador físico. Não há suporte para máquinas virtuais.

-   O Trusted Platform Module (TPM) está disponível. Uma versão compatível do TPM 1,2 ou posterior é necessária para o Windows 7. O Windows 8 e o Windows to go não exigem um TPM.

A coleção é avaliada em relação a todos os computadores e cria o subconjunto de computadores compatíveis que fornece a base para avaliação de conformidade e relatórios para a integração com o MBAM.

### Relatórios

Há quatro relatórios que você pode usar para ver a conformidade. São eles:

-   **Painel de conformidade do BitLocker Enterprise** – fornece aos administradores de ti três exibições de informações em um único relatório: distribuição de status de conformidade, não compatível – distribuição de erros e distribuição de status de conformidade por tipo de unidade. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e visualizem uma lista de computadores que correspondem ao estado que você selecionar.

-   **Detalhes de conformidade corporativa do BitLocker** – permite que os administradores de ti exibam informações sobre o status de conformidade de criptografia do BitLocker da empresa e inclui o status de conformidade de cada computador. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e visualizem uma lista de computadores que correspondem ao estado que você selecionar.

-   **Conformidade com o computador BitLocker** – permite que os administradores de ti visualizem um computador individual e determine por que ele foi reportado com um determinado status de conformidade ou não compatível. O relatório também exibe o estado de criptografia das unidades de sistema operacional (OSD) e unidades de dados fixos (FDDs).

-   **Resumo de conformidade com o BitLocker Enterprise** – permite que os administradores de ti exibam o status da conformidade da empresa com a política MBAM. O estado de cada computador é avaliado, e o relatório mostra um resumo da conformidade de todos os computadores na empresa em relação à política. As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e visualizem uma lista de computadores que correspondem ao estado que você selecionar.

## Arquitetura de alto nível do MBAM com o Configuration Manager


A imagem a seguir mostra a arquitetura MBAM com a topologia do Configuration Manager. Essa configuração oferece suporte a até 200.000 clientes do MBAM em um ambiente de produção.

![arquitetura MBAM com o Configuration Manager](images/mbam2-cmserver.gif)

A seguir está uma descrição dos servidores, bancos de dados e recursos dessa arquitetura. Os recursos do servidor e os bancos de dados na imagem da arquitetura estão listados no computador ou servidor onde recomendamos que você os instale.

-   **Servidor de banco de dados** – o **banco de dados de recuperação**, o banco de dados de **auditoria**e os **relatórios de auditoria** são instalados em um servidor Windows e na instância SqlServer com suporte O banco de dados de recuperação armazena dados de recuperação coletados de computadores cliente do MBAM. O banco de dados de auditoria armazena dados de atividades de auditoria coletados de computadores cliente que acessam dados de recuperação. Os relatórios de auditoria fornecem dados sobre o status de conformidade dos computadores cliente na sua empresa.

-   **Servidor de site primário do Configuration Manager** – o servidor do Configuration Manager contém a instalação do servidor do MBAM com a topologia de integração do System Center Configuration Manager, que deve ser instalada em um servidor de site primário do Configuration Manager. O servidor do Configuration Manager coleta as informações do inventário de hardware dos computadores cliente e é usada para denunciar a compatibilidade do BitLocker em computadores cliente. Quando você executa a instalação do servidor de configuração do MBAM, um conjunto e os dados de configuração são instalados no servidor de site primário do Configuration Manager.

-   **Servidor de administração e monitoramento** – o **servidor de administração e monitoramento** está instalado em um servidor Windows e consiste no site de administração e monitoramento e nos serviços Web de monitoramento. O site de administração e monitoramento é usado para auditar a atividade e para acessar dados de recuperação (por exemplo, as chaves de recuperação do BitLocker). O **portal de autoatendimento** também é instalado no servidor de administração e monitoramento. O portal permite que os usuários finais em computadores cliente façam logon independentemente em um site para obter uma chave de recuperação se eles perdem ou esquecem a senha do BitLocker. Os relatórios de auditoria também são instalados no servidor de administração e monitoramento.

-   **Estação de trabalho de gerenciamento** – o **modelo de política** consiste em objetos de política de grupo que definem as configurações de implementação MBAM para a criptografia de unidade de disco Você pode instalar o modelo de política em qualquer servidor ou estação de trabalho, mas ele é instalado normalmente em uma estação de trabalho de gerenciamento que é um computador cliente ou servidor com suporte. A estação de trabalho não precisa ser um computador dedicado.

-   **Cliente MBAM** e computador **cliente do Configuration Manager**

    -   O **cliente MBAM** executa as seguintes tarefas:

        -   Usa objetos de política de grupo para impor a criptografia BitLocker dos computadores cliente da empresa.

        -   Coleta a chave de recuperação dos três tipos de unidade de dados BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).

        -   Coleta informações de recuperação e informações do computador dos computadores cliente.

    -   **Cliente do Configuration Manager** – o cliente do Configuration Manager permite que o Configuration Manager colete dados de compatibilidade de hardware sobre os computadores cliente e permite que o Configuration Manager informe as informações de conformidade.

## Tópicos relacionados


[Usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





