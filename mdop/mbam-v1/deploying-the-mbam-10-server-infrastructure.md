---
title: Implantando a infraestrutura do Servidor do MBAM 1.0
description: Implantando a infraestrutura do Servidor do MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 63099d425b51bfde52eac59771007b1c765acf05
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910416"
---
# <a name="deploying-the-mbam-10-server-infrastructure"></a>Implantando a infraestrutura do Servidor do MBAM 1.0


Você pode instalar recursos do Microsoft BitLocker Administration and Monitoring (MBAM) Server em configurações diferentes usando um a cinco servidores. Geralmente, você deve usar uma configuração de três a cinco servidores para ambientes de produção, dependendo das suas necessidades de escalabilidade. Para obter mais informações sobre a escalabilidade de desempenho do MBAM e topologias de implantação recomendadas, consulte o White Paper sobre escalabilidade do [MBAM e](https://go.microsoft.com/fwlink/p/?LinkId=258314)High-Availability Guia.

## <a name="deploy-all-mbam-10-on-a-single-server"></a>Implantar todo o MBAM 1.0 em um único servidor


Nesta configuração, todos os recursos do MBAM são instalados em um único servidor. Essa topologia de implantação para infraestrutura de servidor MBAM dará suporte a até 21.000 computadores cliente MBAM.

**Importante**  
Essa configuração é suportada, mas é recomendável apenas para testes.

 

Os procedimentos nesta seção descrevem a instalação completa dos recursos do MBAM em um único servidor.

[Como instalar e configurar o MBAM em um servidor único](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <a name="deploy-mbam-10-on-distributed-servers"></a>Implantar o MBAM 1.0 em servidores distribuídos


Os recursos do MBAM podem ser instalados em configurações diferentes, dependendo das suas necessidades de escalabilidade. Para obter mais informações sobre como planejar a implantação de recursos do servidor MBAM, consulte [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).

Os procedimentos nesta seção descrevem a instalação completa dos recursos do MBAM em servidores distribuídos.

### <a name="three-computer-configuration"></a>Configuração de três computadores

O diagrama a seguir exibe a topologia de implantação de três computadores para MBAM. Recomendamos essa topologia para ambientes de produção que suportam até 55.000 clientes MBAM.

![mbam três topologias de implantação de computador.](images/mbam-3-server.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  O Banco de Dados de Recuperação e Hardware, o Banco de Dados de Conformidade e Auditoria e Os Relatórios de Conformidade e Auditoria são instalados em um servidor.

2.  O recurso Servidor de Administração e Monitoramento está instalado em um servidor.

3.  O modelo de Política de Grupo do MBAM é instalado em um computador capaz de modificar o GPO (Group Policy Objects).

### <a name="four-computer-configuration"></a>Configuração de quatro computadores

O diagrama a seguir exibe a topologia de implantação de quatro computadores para MBAM. Recomendamos essa topologia para ambientes de produção que suportam até 110.000 clientes MBAM.

![mbam quatro topologias de implantação de computador.](images/mbam-4-computer.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  O Banco de Dados de Recuperação e Hardware, o Banco de Dados de Conformidade e Auditoria e Os Relatórios de Conformidade e Auditoria são instalados em um servidor.

2.  O recurso Servidor de Administração e Monitoramento é instalado em um servidor configurado em um Cluster de Servidor de Balanceamento de Carga de Rede (NLB).

3.  O modelo de Política de Grupo do MBAM é instalado em um computador que é capaz de modificar os Objetos de Política de Grupo.

### <a name="five-computer-configuration"></a>Configuração de cinco computadores

O diagrama a seguir exibe a topologia de implantação de cinco computadores para MBAM. Recomendamos essa topologia para ambientes de produção que suportam até 135.000 clientes MBAM.

![mbam cinco topologias de implantação de computador.](images/mbam-5-computer.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  O Banco de Dados de Recuperação e Hardware está instalado em um servidor.

2.  Os Relatórios de Conformidade e Auditoria e Conformidade e Auditoria são instalados em um servidor.

3.  O recurso Servidor de Administração e Monitoramento é instalado em um servidor configurado em um Cluster de Servidor de Balanceamento de Carga de Rede (NLB).

4.  O modelo de Política de Grupo do MBAM é instalado em um computador capaz de modificar Objetos de Política de Grupo.

[Como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Como configurar os Balanceamento de Carga de Rede para o MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## <a name="other-resources-for-mbam-10-server-features-deployment"></a>Outros recursos para implantação de recursos do MBAM 1.0 Server


[Implantando o MBAM 1.0](deploying-mbam-10.md)

 

 





