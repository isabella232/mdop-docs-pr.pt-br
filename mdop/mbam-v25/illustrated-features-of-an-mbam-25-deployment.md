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
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795989"
---
# Recursos ilustrados de uma implantação do MBAM 2.5


Este tópico descreve os recursos individuais que compõem uma implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para as seguintes topologias:

-   MBAM autônomo

-   Integração do System Center Configuration Manager

**Importante**  
Esses recursos não representam a arquitetura recomendada para a implantação do MBAM. Use estas informações apenas como um guia para compreender os recursos individuais que compõem uma implantação do MBAM. Consulte [arquitetura de alto nível para o MBAM 2,5](high-level-architecture-for-mbam-25.md) para a arquitetura recomendada para mbam.



Para obter uma lista das versões com suporte do software mencionadas neste tópico, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

## <a href="" id="bkmk-standalone"></a> Topologia autônoma do MBAM


A imagem e a tabela a seguir explicam os recursos em uma topologia autônoma do MBAM.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|Tipo de recurso|Descrição|Banco de dados|
|-|-|-|
|Banco de dados de recuperação|Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.|Esse recurso é configurado em um servidor que executa o Windows Server e uma instância do SQL Server com suporte.|
|Banco de dados de auditoria e conformidade|Esse banco de dados armazena dados de conformidade, que são usados principalmente para os relatórios que o SQL Server Reporting Services hospeda.|Esse recurso é configurado em um servidor que executa o Windows Server e uma instância do SQL Server com suporte.|
|Relatórios de conformidade e auditoria|||
|Serviço Web de relatório|Esse serviço Web permite a comunicação entre o site de administração e monitoramento e a instância do SQL Server na qual os dados de relatório são armazenados.|Esse recurso é instalado em um servidor que executa o Windows Server.|
|Site de relatório (site de administração e monitoramento)|Você vê relatórios do site Administração e monitoramento. Os relatórios fornecem dados de status de conformidade e auditoria de recuperação sobre os computadores cliente da sua empresa.|Esse recurso está configurado em um servidor que executa o Windows Server.|
|SQL Server Reporting Services (SSRS)|Os relatórios são configurados em uma instância de banco de dados SSRS. Os relatórios podem ser visualizados diretamente do SSRS ou do site de administração e monitoramento.|Esse recurso é configurado em um servidor que executa o Windows Server e uma instância do SQL Server compatível que está executando o SSRS.|
|Servidor de autoatendimento|||
|Web Service de auto-atendimento|Este serviço Web é usado pelo cliente MBAM e pelo site de administração e monitoramento e pelo portal de autoatendimento para se comunicar com o banco de dados de recuperação.|Esse recurso é instalado em um computador que executa o Windows Server.|
|Site de autoatendimento (portal de autoatendimento)|Este site permite que os usuários finais em computadores cliente se conectem de forma independente a um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.|Esse recurso é configurado em um computador que executa o Windows Server.|
|Servidor de administração e monitoramento|||
|Serviço Web de administração e monitoramento|O serviço Web de monitoramento é usado pelo cliente MBAM e pelos websites para se comunicar com os bancos de dados.|Esse recurso é instalado em um computador que executa o Windows Server.|

**Importante**  
O serviço Web de autoatendimento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, no qual o cliente MBAM, o site de administração e monitoramento e o portal de autoatendimento se comunicam diretamente com o banco de dados de recuperação.

**Importante**  
O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois o cliente MBAM e os sites se comunicam diretamente com o banco de dados de recuperação.


## <a href="" id="bkmk-cmintegrated"></a>Topologia de integração do System Center Configuration Manager

A imagem e a tabela a seguir explicam os recursos na topologia de integração do System Center Configuration Manager.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**Importante**  
O serviço Web de autoatendimento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, no qual o cliente MBAM, o site de administração e monitoramento e o portal de autoatendimento se comunicam diretamente com o banco de dados de recuperação.

**Aviso**  
O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois o cliente MBAM e os sites se comunicam diretamente com o banco de dados de recuperação.


|                        Tipo de recurso                        |                                                                                                    Descrição                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Servidor de autoatendimento                     |                                                                                                                                                                                                                   |
|                  Web Service de auto-atendimento                  |                                                 Este serviço Web é usado pelo cliente MBAM e pelo portal de autoatendimento para se comunicar com o banco de dados de recuperação.                                                  |
|                    Site de autoatendimento                    |                          Este site permite que os usuários finais em computadores cliente se conectem de forma independente a um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.                          |
| Servidor de administração e monitoramento/relatório de auditoria de recuperação |                                                                                                                                                                                                                   |
|         Serviço Web de administração e monitoramento          |                               Esse serviço Web permite a comunicação entre o site de administração e monitoramento e os bancos de dados do SQL Server nos quais os dados de relatório são armazenados.                               |
|           Site de administração e monitoramento            | O relatório de auditoria de recuperação é exibido no site de administração e monitoramento. Use o console do Configuration Manager para ver todos os outros relatórios ou exibir relatórios diretamente do SQL Server Reporting Services. |
|                         Bancos de dados                          |                                                                                                                                                                                                                   |
|                     Banco de dados de recuperação                      |                                                                 Esse banco de dados armazena dados de recuperação coletados de computadores cliente do MBAM.                                                                  |
|                       Banco de dados de auditoria                       |                                                                   Este banco de dados armazena informações de auditoria sobre tentativas e atividades de recuperação.                                                                    |
|               Recursos do Configuration Manager               |                                                                                                                                                                                                                   |
|          Console de gerenciamento do Configuration Manager          |                                                                   Este console é integrado ao Configuration Manager e é usado para exibir relatórios.                                                                   |
|               Relatórios do Configuration Manager                |                                                             Relatórios mostram dados de auditoria de conformidade e recuperação para computadores cliente na sua empresa.                                                              |
|               SQL Server Reporting Services                |                                                O SSRS permite os relatórios do MBAM. Os relatórios podem ser visualizados diretamente do SSRS ou do console do Configuration Manager.                                                 |

## Tópicos relacionados

[Arquitetura de alto nível do MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




