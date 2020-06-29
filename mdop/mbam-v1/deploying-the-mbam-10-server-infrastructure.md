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
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799620"
---
# Implantando a infraestrutura do Servidor do MBAM 1.0


Você pode instalar os recursos do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) em diferentes configurações usando um a cinco servidores. Geralmente, você deve usar uma configuração de três a cinco servidores para ambientes de produção, dependendo de suas necessidades de escalabilidade. Para obter mais informações sobre a escalabilidade de desempenho de MBAM e topologias de implantação recomendadas, consulte o [White Paper MBAM Redimensionation and High-Availability Guide](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## Implantar todas as MBAM 1,0 em um único servidor


Nesta configuração, todos os recursos do MBAM são instalados em um único servidor. Esta topologia de implantação para a infraestrutura do MBAM Server dará suporte a até 21.000 MBAM computadores cliente.

**Importante**  Essa configuração tem suporte, mas recomendamos que ela seja testada apenas.

 

Os procedimentos desta seção descrevem a instalação completa dos recursos do MBAM em um único servidor.

[Como instalar e configurar o MBAM em um servidor único](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## Implantar o MBAM 1,0 em servidores distribuídos


Os recursos do MBAM podem ser instalados em configurações diferentes, dependendo de suas necessidades de escalabilidade. Para obter mais informações sobre como planejar a implantação de recursos do MBAM Server, consulte [planejando a implantação do MBAM 1,0 Server](planning-for-mbam-10-server-deployment.md).

Os procedimentos desta seção descrevem a instalação completa dos recursos do MBAM em servidores distribuídos.

### Configuração de três computadores

O diagrama a seguir exibe a topologia de implantação de três computadores para MBAM. Recomendamos Esta topologia para ambientes de produção que dão suporte a até 55.000 clientes MBAM.

![MBAM a topologia de implantação do computador](images/mbam-3-server.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  Bancos de dados de recuperação e de hardware, conformidade e auditoria, e conformidade e relatórios de auditoria são instalados em um servidor.

2.  O recurso de servidor de administração e monitoramento está instalado em um servidor.

3.  MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar objetos de política de grupo (GPO).

### Configuração de quatro computadores

O diagrama a seguir exibe a topologia de implantação de quatro computadores para MBAM. Recomendamos Esta topologia para ambientes de produção que dão suporte a até 110.000 clientes MBAM.

![MBAM 4 topologia de implantação do computador.](images/mbam-4-computer.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  Bancos de dados de recuperação e de hardware, conformidade e auditoria, e conformidade e relatórios de auditoria são instalados em um servidor.

2.  O recurso de administração e administração do servidor está instalado em um servidor configurado em um cluster de servidor de balanceamento de carga de rede (NLB).

3.  MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar os objetos de política de grupo.

### Configuração de cinco computadores

O diagrama a seguir exibe a topologia de implantação de cinco computadores para MBAM. Recomendamos Esta topologia para ambientes de produção que dão suporte a até 135.000 clientes MBAM.

![MBAM cinco topologia de implantação do computador.](images/mbam-5-computer.jpg)

Nesta configuração, os recursos do MBAM são instalados na seguinte configuração:

1.  Recuperação e banco de dados de hardware instalado em um servidor.

2.  O banco de dados de conformidade e auditoria e a conformidade e os relatórios de auditoria são instalados em um servidor.

3.  O recurso de administração e administração do servidor está instalado em um servidor configurado em um cluster de servidor de balanceamento de carga de rede (NLB).

4.  MBAM modelo de política de grupo está instalado em um computador que é capaz de modificar objetos de política de grupo.

[Como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Como configurar os Balanceamento de Carga de Rede para o MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## Outros recursos para a implantação de recursos do MBAM 1,0 Server


[Implantando o MBAM 1.0](deploying-mbam-10.md)

 

 





