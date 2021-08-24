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
ms.openlocfilehash: 9f23a0eba923608fb6e25e44ee2843f3cde4c2dc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910806"
---
# <a name="getting-started---using-mbam-with-configuration-manager"></a>Introdução – Como usar o MBAM com o Configuration Manager


Ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode escolher uma topologia que integre o MBAM ao Configuration Manager 2007 ou System Center 2012 Configuration Manager. Para ver uma lista das versões com suporte do Configuration Manager compatíveis com o MBAM, consulte [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Na topologia integrada, os recursos de conformidade e relatório de hardware são removidos do MBAM e acessados do Configuration Manager.

**Importante**  
Windows To Go não é suportado quando você instala a topologia integrada do MBAM com o Configuration Manager 2007.

 

## <a name="using-mbam-with-configuration-manager"></a>Usando o MBAM com o Configuration Manager


A integração do MBAM baseia-se em um novo Configuration Pack que instala os três itens a seguir no Configuration Manager 2007 ou no System Center 2012 Configuration Manager, que são descritos em detalhes nas seguintes seções:

Dados de configuração que consistem em itens de configuração e uma linha de base de configuração

Coleção

Relatórios

### <a name="configuration-data"></a>Dados de Configuração

Os dados de configuração instalam uma linha de base de configuração, chamada "Proteção do BitLocker", que contém dois itens de configuração: "Proteção de Unidade de Sistema Operacional BitLocker" e "Proteção de Unidades de Dados Fixas do BitLocker". A linha de base de configuração é implantada na coleção, que também é criada quando o MBAM é instalado. Os dois itens de configuração fornecem a base para avaliar o status de conformidade dos computadores cliente. Essas informações são capturadas, armazenadas e avaliadas no Configuration Manager. Os itens de configuração são baseados nos requisitos de conformidade para unidades do sistema operacional (OSDs) e unidades de dados fixas (FDDs). Os detalhes necessários para os computadores implantados são coletados para que a conformidade para esses tipos de unidade possa ser avaliada. Por padrão, a linha de base de configuração avalia o status de conformidade a cada 12 horas e envia os dados de conformidade para o Configuration Manager.

### <a name="collection"></a>Coleção

O MBAM cria uma coleção chamada MbaM Supported Computers. A linha de base de configuração é direcionada a computadores cliente que estão nessa coleção. Esta é uma coleção dinâmica que, por padrão, é executado a cada 12 horas e avalia a associação. A associação se baseia em três critérios:

-   É uma versão com suporte do sistema operacional Windows sistema operacional. Atualmente, o MBAM dá suporte Windows 7 Enterprise e Windows 7 Ultimate, Windows 8 Enterprise e Windows Para Ir, quando o Windows To Go está em execução no Windows 8 Enterprise.

-   É um computador físico. Não há suporte para máquinas virtuais.

-   O Trusted Platform Module (TPM) está disponível. Uma versão compatível do TPM 1.2 ou posterior é necessária para Windows 7. Windows 8 e Windows Para Ir não exigem um TPM.

A coleção é avaliada em relação a todos os computadores e cria o subconjunto de computadores compatíveis que fornece a base para avaliação e relatórios de conformidade para a integração com o MBAM.

### <a name="reports"></a>Relatórios

Há quatro relatórios que você pode usar para exibir a conformidade. São eles:

-   **BitLocker Enterprise Painel** de Conformidade – fornece aos administradores de IT três exibições diferentes de informações sobre um único relatório: Distribuição de Status de Conformidade, Não Conformidade – Distribuição de Erros e Distribuição de Status de Conformidade por Tipo de Unidade. Opções de detalhamento no relatório permitem que os administradores de TI cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.

-   **BitLocker Enterprise Detalhes** de Conformidade – permite aos administradores de IT exibir informações sobre o status de conformidade de criptografia do BitLocker da empresa e inclui o status de conformidade para cada computador. Opções de detalhamento no relatório permitem que os administradores de TI cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.

-   Conformidade com o Computador Do **BitLocker** – permite que os administradores de IT exibiam um computador individual e determinem por que ele foi relatado com um determinado status de compatível ou não compatível. O relatório também exibe o estado de criptografia das unidades do sistema operacional (OSD) e unidades de dados fixas (FDDs).

-   **BitLocker Enterprise Resumo de Conformidade** – permite que os administradores de IT visualizam o status da conformidade da empresa com a política do MBAM. O estado de cada computador é avaliado e o relatório mostra um resumo da conformidade de todos os computadores na empresa em relação à política. Opções de detalhamento no relatório permitem que os administradores de TI cliquem nos dados e exibir uma lista de computadores que corresponderem ao estado selecionado.

## <a name="high-level-architecture-of-mbam-with-configuration-manager"></a>High-Level arquitetura do MBAM com o Configuration Manager


A imagem a seguir mostra a arquitetura do MBAM com a topologia do Configuration Manager. Essa configuração dá suporte a até 200.000 clientes MBAM em um ambiente de produção.

![arquitetura do mbam com o gerenciador de configuração.](images/mbam2-cmserver.gif)

Uma descrição dos servidores, bancos de dados e recursos dessa arquitetura é a seguir. Os recursos e bancos de dados do servidor na imagem da arquitetura estão listados no computador ou servidor em que recomendamos instalá-los.

-   **Servidor de Banco** de Dados – **** **O**Banco de Dados de Recuperação, **** o Banco de Dados de Auditoria e os Relatórios de Auditoria são instalados em um servidor Windows e têm suporte SQL Server instância. O banco de dados de recuperação armazena dados de recuperação coletados de computadores clientes do MBAM. O Banco de Dados de Auditoria armazena dados de atividade de auditoria coletados de computadores cliente que acessaram dados de recuperação. Os Relatórios de Auditoria fornecem dados sobre o status de conformidade dos computadores cliente em sua empresa.

-   **Servidor** de Site Principal do Gerenciador de Configurações – o Servidor do Configuration Manager contém a instalação do servidor MBAM com a topologia de integração System Center Configuration Manager, que deve ser instalada em um servidor de site principal do Configuration Manager. O Servidor do Configuration Manager coleta as informações de inventário de hardware de computadores cliente e é usado para relatar a conformidade do BitLocker de computadores cliente. Ao executar a instalação do servidor de Instalação do MBAM, uma coleção e os dados de configuração são instalados no Servidor de Site Principal do Configuration Manager.

-   **Servidor de** Administração e **** Monitoramento - O Servidor de Administração e Monitoramento está instalado em um servidor Windows e consiste no site de Administração e Monitoramento e nos serviços Web de monitoramento. O site administração e monitoramento é usado para auditar atividades e acessar dados de recuperação (por exemplo, chaves de recuperação do BitLocker). O **Portal de Autoatendido** também está instalado no Servidor de Administração e Monitoramento. O Portal permite que os usuários finais em computadores clientes faça logoff independentemente em um site para obter uma chave de recuperação se perderem ou esquecerem a senha do BitLocker. Os relatórios de auditoria também são instalados no Servidor de Administração e Monitoramento.

-   **Estação de Trabalho de** Gerenciamento - O Modelo **de** Política consiste em Objetos de Política de Grupo que definem as configurações de implementação do MBAM para criptografia de unidade BitLocker. Você pode instalar o modelo de Política em qualquer servidor ou estação de trabalho, mas ele é normalmente instalado em uma estação de trabalho de gerenciamento que é um servidor Windows ou computador cliente com suporte. A estação de trabalho não precisa ser um computador dedicado.

-   **Computador cliente do MBAM Client** and **Configuration Manager**

    -   O **Cliente MBAM** executa as seguintes tarefas:

        -   Usa Objetos de Política de Grupo para impor a criptografia BitLocker de computadores cliente na empresa.

        -   Coleta a chave de recuperação para os três tipos de unidade de dados do BitLocker: unidades do sistema operacional, unidades de dados fixas e unidades USB (dados removíveis).

        -   Coleta informações de recuperação e informações do computador sobre os computadores cliente.

    -   **Cliente do Gerenciador** de Configurações – o cliente do Configuration Manager permite que o Gerenciador de Configurações colete dados de compatibilidade de hardware sobre os computadores clientes e permite que o Gerenciador de Configurações informe informações de conformidade.

## <a name="related-topics"></a>Tópicos relacionados


[Usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





