---
title: Como implantar os bancos de dados do App-V usando scripts SQL
description: Como implantar os bancos de dados do App-V usando scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796418"
---
# Como implantar os bancos de dados do App-V usando scripts SQL


Use as instruções a seguir para usar scripts SQL, em vez do Windows Installer, para:

-   Instalar os bancos de dados do App-V 5,0

-   Atualizar os bancos de dados do 5,0 para uma versão mais recente

**Como instalar os bancos de dados do App-V usando scripts SQL**

1. Antes de instalar os scripts de banco de dados, revise e mantenha uma cópia dos termos de licença do App-V. Ao executar os scripts de banco de dados, você está concordando com os termos de licença. Se não aceitá-los, você não deve usar este software.

2. Copie o **appv\_server\_setup.exe** da mídia de versão do App-V para um local temporário.

3. Em um prompt de comando, execute **appv\_server\_setup.exe** e especifique um local temporário para extrair os scripts de banco de dados.

   Exemplo: appv\_server\_setup.exe/layout c:\\ &lt; caminho do local temporário&gt;

4. Navegue até o local temporário que você criou, abra a pasta **DatabaseScripts** extraída e revise o arquivo de Readme.txt apropriado para obter instruções:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Banco de dados</th>
   <th align="left">Localização do arquivo Readme.txt a ser usado</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Banco de dados de gerenciamento</p></td>
   <td align="left"><p>Subpasta ManagementDatabase</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Se você estiver atualizando ou instalando o banco de dados de gerenciamento do App-V 5,0 SP3, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts do SQL para instalar ou atualizar o banco de dados do servidor de gerenciamento do App-v 5,0 SP3 falha </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Banco de dados de relatórios</p></td>
   <td align="left"><p>Subpasta ReportingDatabase</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Implantação do servidor App-V 5.0](deploying-the-app-v-50-server.md)

[Como implantar o servidor do App-V 5.0](how-to-deploy-the-app-v-50-server-50sp3.md)









