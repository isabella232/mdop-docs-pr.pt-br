---
title: Configurando o servidor do MED-V para o modo de cluster
description: Configurando o servidor do MED-V para o modo de cluster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799928"
---
# Configurando o servidor do MED-V para o modo de cluster


Você pode configurar o servidor MED-V no modo de cluster. No modo de cluster, dois servidores são usados e todos os arquivos identificados como mútuos nos dois servidores são colocados em um sistema de arquivos. O servidor acessa os arquivos do sistema de arquivos, em vez de armazenar os arquivos localmente.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**Para configurar o servidor MED-V no modo de cluster**

1.  Instale e configure o MED-V em um dos servidores.

2.  Crie uma rede compartilhada em um local central onde todos os servidores possam acessá-la.

3.  Copie o conteúdo da pasta * &lt; installdir &gt; /Servers/ConfigurationServer* para a rede compartilhada.

4.  Instale o MED-V Server em todos os servidores designados.

5.  Na rede compartilhada, atribua acesso total a todas as contas de sistema do MED-V Server.

6.  Em cada servidor, faça o seguinte:

    1.  No arquivo * &lt; InstallDir &gt; /Servers/ServerConfiguration.xml* , defina o valor de * &lt; StorePath &gt; * para o caminho de rede compartilhada.

    2.  Copie o arquivo * &lt; InstsallDir &gt; /Servers/KeyPair.xml* do servidor original para todos os servidores MED-V.

    3.  Reinicie o serviço MED-V.

**Observação**  Se todos os servidores tiverem as mesmas configurações locais (como portas de escuta, servidor IIS, permissões de gerenciamento, banco de dados de relatório e assim por diante), a * &lt; &gt; ServerSettings.xml/Servers/* de um banco de dados do installdir também pode ser compartilhada por todos os servidores.

 

## Tópicos relacionados


[Planejamento e design da infraestrutura do MED-V](med-v-infrastructure-planning-and-design.md)

 

 





