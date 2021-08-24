---
title: Recursos ilustrados de uma implantação do MBAM 2.5
description: Recursos ilustrados de uma implantação do MBAM 2.5
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 139980fb6712b40685a41bab45610da670803afa
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910616"
---
# <a name="illustrated-features-of-an-mbam-25-deployment"></a>Recursos ilustrados de uma implantação do MBAM 2.5


Este tópico descreve os recursos individuais que compoem uma implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 para as seguintes topologias:

-   MBAM Autônomo

-   System Center Configuration Manager Integração

**Importante**  
Esses recursos não representam a arquitetura recomendada para a implantação do MBAM. Use essas informações apenas como um guia para entender os recursos individuais que comem uma implantação do MBAM. Consulte [Arquitetura de alto nível para MBAM 2.5](high-level-architecture-for-mbam-25.md) para a arquitetura recomendada para MBAM.



Para ver uma lista das versões com suporte do software mencionado neste tópico, consulte CONFIGURAções com suporte do [MBAM 2.5](mbam-25-supported-configurations.md).

## <a name="mbam-stand-alone-topology"></a><a href="" id="bkmk-standalone"></a> Topologia autônomo do MBAM


A imagem e a tabela a seguir explicam os recursos em uma topologia autônomo do MBAM.

![mbab2\-5.](images/mbam2-5-standalonecomponents.png)

|Tipo de recurso|Descrição|Banco de dados|
|-|-|-|
|Banco de Dados de Recuperação|Esse banco de dados armazena dados de recuperação coletados de computadores clientes do MBAM.|Esse recurso é configurado em um servidor que executa Windows Server e uma instância SQL Server com suporte.|
|Banco de dados de conformidade e auditoria|Esse banco de dados armazena dados de conformidade, que são usados principalmente para os Relatórios que SQL Server Reporting Services hosts.|Esse recurso é configurado em um servidor que executa Windows Server e uma instância SQL Server com suporte.|
|Relatórios de conformidade e auditoria|||
|Serviço Web de relatórios|Esse serviço Web permite a comunicação entre o Site de Administração e Monitoramento e SQL Server instância em que os dados de relatório são armazenados.|Esse recurso é instalado em um servidor que executa Windows Server.|
|Site de Relatórios (Site de Administração e Monitoramento)|Você exibirá Relatórios do Site de Administração e Monitoramento. Os Relatórios fornecem dados de status de auditoria e conformidade de recuperação sobre os computadores cliente em sua empresa.|Esse recurso é configurado em um servidor que executa Windows Server.|
|SQL Server Reporting Services (SSRS)|Os relatórios são configurados em uma instância de banco de dados SSRS. Os relatórios podem ser exibidos diretamente do SSRS ou do Site de Administração e Monitoramento.|Esse recurso é configurado em um servidor que executa o Windows Server e uma instância SQL Server com suporte que está executando o SSRS.|
|Self-Service Server|||
|Self-Service Web Service|Esse serviço Web é usado pelo Cliente MBAM e pelo Site de Administração e Monitoramento e Self-Service Portal para se comunicar com o Banco de Dados de Recuperação.|Esse recurso é instalado em um computador que executa o Windows Server.|
|Self-Service Site (Portal de Autoatend)|Este site permite que os usuários finais em computadores clientes entre independentemente em um site para obter uma chave de recuperação se perderem ou esquecerem a senha do BitLocker.|Esse recurso é configurado em um computador que executa Windows Server.|
|Servidor de Administração e Monitoramento|||
|Serviço Web de Administração e Monitoramento|O Serviço Web de Monitoramento é usado pelo Cliente MBAM e pelos sites para se comunicar com os bancos de dados.|Esse recurso é instalado em um computador que executa o Windows Server.|

**Importante**  
O Self-Service Web Service não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, no qual o Cliente MBAM, o Site de Administração e Monitoramento e o Portal Self-Service se comunicam diretamente com o Banco de Dados de Recuperação.

**Importante**  
O Serviço Web de Monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 desde que o Cliente MBAM e os sites se comunicam diretamente com o Banco de Dados de Recuperação.


## <a name="system-center-configuration-manager-integration-topology"></a><a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager Topologia de integração

A imagem e a tabela a seguir explicam os recursos na topologia System Center Configuration Manager Integração.

![mbam2\-5.](images/mbam2-5-cmcomponents.png)

**Importante**  
O Self-Service Web Service não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, no qual o Cliente MBAM, o Site de Administração e Monitoramento e o Portal Self-Service se comunicam diretamente com o Banco de Dados de Recuperação.

**Aviso**  
O Serviço Web de Monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 desde que o Cliente MBAM e os sites se comunicam diretamente com o Banco de Dados de Recuperação.


|                        Tipo de recurso                        |                                                                                                    Descrição                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service Server                     |                                                                                                                                                                                                                   |
|                  Self-Service Web Service                  |                                                 Esse serviço Web é usado pelo Cliente MBAM e pelo Portal Self-Service para se comunicar com o Banco de Dados de Recuperação.                                                  |
|                    Self-Service Site                    |                          Este site permite que os usuários finais em computadores clientes entre independentemente em um site para obter uma chave de recuperação se perderem ou esquecerem a senha do BitLocker.                          |
| Relatório de auditoria do Servidor de Administração e Monitoramento/Recuperação |                                                                                                                                                                                                                   |
|         Serviço Web de Administração e Monitoramento          |                               Esse serviço Web permite a comunicação entre o Site de Administração e Monitoramento e os bancos de dados SQL Server onde os dados de relatório são armazenados.                               |
|           Site de Administração e Monitoramento            | O relatório de Auditoria de Recuperação é exibido no Site de Administração e Monitoramento. Use o console do Configuration Manager para exibir todos os outros relatórios ou exibir relatórios diretamente do SQL Server Reporting Services. |
|                         Bancos de dados                          |                                                                                                                                                                                                                   |
|                     Banco de Dados de Recuperação                      |                                                                 Esse banco de dados armazena dados de recuperação coletados de computadores clientes do MBAM.                                                                  |
|                       Banco de Dados de Auditoria                       |                                                                   Esse banco de dados armazena informações de auditoria sobre tentativas e atividades de recuperação.                                                                    |
|               Recursos do Configuration Manager               |                                                                                                                                                                                                                   |
|          Console de Gerenciamento do Configuration Manager          |                                                                   Esse console é integrado ao Configuration Manager e é usado para exibir relatórios.                                                                   |
|               Relatórios do Configuration Manager                |                                                             Relatórios mostram dados de auditoria de conformidade e recuperação para computadores cliente em sua empresa.                                                              |
|               SQL Server Reporting Services                |                                                O SSRS habilita os Relatórios do MBAM. Os relatórios podem ser exibidos diretamente do SSRS ou do console do Configuration Manager.                                                 |

## <a name="related-topics"></a>Tópicos relacionados

[Arquitetura de alto nível do MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

## <a name="got-a-suggestion-for-mbam"></a>Tem uma sugestão para MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, use o [Fórum technet do MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




