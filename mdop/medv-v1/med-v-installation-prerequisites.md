---
title: Pré-requisitos de instalação do MED-V
description: Pré-requisitos de instalação do MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799578"
---
# Pré-requisitos de instalação do MED-V


Estes são pré-requisitos para a instalação do MED-V:

[Requisitos do Active Directory](#bkmk-activedirectoryrequirements)

[Banco de dados de relatório](#bkmk-howtoinstallthereportdatabase)

[Antivirus/configuração do software de backup](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Requisitos do Active Directory


Ao configurar o servidor MED-V, se os usuários não fizerem parte do mesmo domínio ao qual o servidor pertence, uma relação de confiança deve ser definida entre os domínios.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Como instalar o banco de dados de relatórios


O banco de dados de relatórios é necessário para armazenar todos os logs do espaço de trabalho do MED-V. O banco de dados de log é usado para gerar relatórios do MED-V. Para obter informações sobre relatórios, consulte [relatórios do MED-V](med-v-reporting.md).

O SQL Server pode ser instalado no mesmo servidor do servidor MED-V ou em um servidor remoto. Se estiver instalando em um servidor remoto, consulte [instalando o SQL Server em um servidor remoto](#bkmk-installingsqlserveronaremoteserver).

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Instalando o SQL Server em um servidor remoto

**Para instalar o SQL Server em um servidor remoto**

1.  Configure o seguinte no servidor remoto:

    -   Nome da instância — instância padrão

    -   Modo de autenticação – modo misto

    -   Usuário – o usuário padrão criado é "SA"

    -   Senha — senha desejada

    -   Configurações de agrupamento — padrão

    -   Erro nas configurações do relatório de uso — padrão

2.  Instale os seguintes arquivos no servidor MED-V:

    -   Para instalar os pré-requisitos para a coleção de objetos do pacote de gerenciamento do Microsoft SQL Server2008, baixe o [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) a partir do centro de download da Microsoft.

    -   Para instalar os pré-requisitos para a coleção de objetos do pacote de gerenciamento do Microsoft SQL Server2005, baixe o [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) a partir do centro de download da Microsoft.

    -   Para instalar os arquivos dll necessários para o Microsoft SQL Server2008, baixe a [coleção de objetos de gerenciamento do Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) a partir do centro de download da Microsoft.

    -   Para instalar os arquivos dll necessários para o Microsoft SQL Server2005, baixe os [objetos de gerenciamento do Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) no centro de download da Microsoft.

    -   Para instalar os pacotes de instalação autônomos que fornecem valor adicional para SQL Server2008, baixe o [pacote de recursos do Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) do centro de download da Microsoft.

    -   Para instalar os pacotes de instalação autônomos que fornecem valor adicional para SQL Server2005, baixe o [Feature Pack para Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) do centro de download da Microsoft.

    Para obter mais informações sobre esses arquivos, consulte [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) ou [pacote de recursos para Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Antivirus/configuração do software de backup


Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, é recomendável que seja possível excluir os seguintes tipos de arquivo de máquina virtual de qualquer Antivirus ou processamento de backup em execução no host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Como instalar e configurar o Microsoft Virtual PC2007 SP1


**Importante**  Se o Virtual PC para Windows existir no computador host, desinstale-o antes de instalar o virtual PC2007 SP1.

 

**Para instalar o Microsoft Virtual PC2007 SP1**

1.  Baixe o virtual PC2007 SP1 do centro de download da Microsoft para o [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).

2.  Execute o arquivo de instalação no computador host e siga o assistente.

3.  Instale a atualização do PC2007 SP1 do virtual no computador host no modo elevado.

    Para obter mais informações, consulte [a descrição do pacote de hotfix do Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Observação**  A atualização do PC2007 SP1 virtual é necessária para executar o PC2007 virtual SP1.

     

## Tópicos relacionados


[Configurações com suporte](supported-configurationsmedv-orientation.md)

 

 





