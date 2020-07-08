---
title: Como validar a instalação do MBAM com o Configuration Manager
description: Como validar a instalação do MBAM com o Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799112"
---
# Como validar a instalação do MBAM com o Configuration Manager


Depois de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) com o Configuration Manager, valide se a instalação configurou com êxito todos os recursos necessários para o MBAM completando as etapas a seguir.

**Para validar a instalação do recurso do servidor MBAM com o Configuration Manager**

1.  No servidor em que o System Center Configuration Manager está implantado, abra o **painel de controle**. Selecione o programa que é usado para desinstalar ou alterar um programa. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos na lista de programas e recursos.

    **Observação**  Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.

     

2.  Use o console do Configuration Manager para confirmar se uma nova coleção, chamada "computadores com suporte para MBAM", é exibida.

    Para exibir a coleção com o Configuration Manager 2007: clique em **banco de dados do site** ( &lt; **Sitecom** &gt;  -  &lt; **nome_do_servidor** &gt; , &lt; **SiteName** &gt; ), gerenciamento do **computador**.

    Para exibir a coleção com SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **conjuntos de dispositivos**.

3.  Use o console do Configuration Manager para verificar se os seguintes relatórios estão listados na pasta **MBAM** :

    -   Conformidade do computador BitLocker

    -   Painel de conformidade do BitLocker Enterprise

    -   Detalhes de conformidade corporativa do BitLocker

    -   Resumo de conformidade empresarial do BitLocker

    Para exibir os relatórios com o Configuration Manager 2007: clique em **relatórios**, **serviços de relatório**, \ \ \ \ &lt; **nomedoservidor** &gt; , **pastas de relatório**

    Para exibir os relatórios com o SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **monitoramento** , **relatórios**e **relatórios**.

4.  Use o console do Configuration Manager para confirmar se a linha de base de configuração "proteção BitLocker" está listada.

    Para exibir as linhas de base de configuração com o Configuration Manager 2007: clique em **Gerenciamento de configuração desejado**, em **linhas de base de configuração**.

    Para exibir as linhas de base de configuração com o SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **configurações de conformidade**, **linhas de base de configuração**.

5.  Use o console do Configuration Manager para confirmar se os seguintes itens de configuração novos são exibidos:

    -   Proteção de unidades de dados fixas do BitLocker

    -   Proteção de unidade do sistema operacional BitLocker

    Para exibir os itens de configuração com o Configuration Manager 2007: clique em **Gerenciamento de configuração desejado**, **itens de configuração**.

    Para exibir os itens de configuração com SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **configurações de conformidade**, **itens de configuração**.

## Tópicos relacionados


[Como implantar o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





