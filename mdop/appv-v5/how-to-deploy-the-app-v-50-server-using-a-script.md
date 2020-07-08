---
title: Como implantar o servidor App-V 5.0 usando um script
description: Como implantar o servidor App-V 5.0 usando um script
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796432"
---
# Como implantar o servidor App-V 5.0 usando um script


Para concluir a configuração do servidor do **appv\_server\_setup.exe** com êxito usando a linha de comando, você deve especificar e combinar vários parâmetros.

Use as tabelas a seguir para obter mais informações sobre como instalar o servidor do App-V 5,0 usando a linha de comando.

>[!NOTE]
> As informações nas tabelas a seguir também podem ser acessadas usando a linha de comando digitando o seguinte comando:
>```
> appv\_server\_setup.exe /?
>```

## Parâmetros e exemplos comuns

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de gerenciamento e o banco de dados de gerenciamento em um computador local.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador local.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador remoto.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. DomainName"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o banco de dados de gerenciamento e o servidor de gerenciamento no mesmo computador.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o banco de dados de gerenciamento em um computador diferente do servidor de gerenciamento.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o Publishing Server.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "serviço Microsoft AppV Publishing"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de relatórios e o banco de dados de relatórios em um computador local.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <ul>
    <li><p>/appv_server_setup.exe/QUIET</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de relatórios e usar um banco de dados de relatórios existente em um computador local.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o servidor de relatórios usando um banco de dados de relatórios existente em um computador remoto.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "serviço de relatórios do Microsoft AppV"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o banco de dados de relatórios no mesmo computador que o servidor de relatórios.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar o banco de dados de relatórios em um computador diferente do que o servidor de relatórios.</p></td>
    <td align="left"><p>Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Usar uma instância personalizada do exemplo do Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SQLINSTANCENAME"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## Definições de parâmetro

### Parâmetros gerais

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/QUIET</p></td>
    <td align="left"><p>Especifica a instalação silenciosa.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/UNINSTALL</p></td>
    <td align="left"><p>Especifica uma desinstalação.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>Especifica a ação de layout. Isso extrai os arquivos MSIs e script para uma pasta sem realmente instalar o produto. Nenhum valor é esperado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>Especifica o diretório de layout. Usa uma cadeia de caracteres. Por exemplo,/LAYOUTDIR = "servidor de virtualização C:\Application"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>Especifica o diretório de instalação. Usa uma cadeia de caracteres. Ex. /INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Habilita o Microsoft Update. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>Aceita o contrato de licença. Isso é necessário para uma instalação automática. Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros de instalação do servidor de gerenciamento

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>Especifica que o servidor de gerenciamento será instalado. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>Especifica a conta que terá permissão de acesso de administrador ao servidor de gerenciamento essa conta pode ser uma conta de usuário individual ou um grupo. Exemplo de uso: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . Se <strong> /MANAGEMENT_SERVER </strong> não for especificado, isso será ignorado. Especifica a conta que será permitida para o acesso de administrador ao servidor de gerenciamento. Pode ser uma conta de usuário ou um grupo. Por exemplo, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica o nome do site que será criado para o serviço de gerenciamento. Por exemplo,/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft App-V"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica o número da porta que será usada pelo serviço de gerenciamento que será usado. Por exemplo,/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros para o banco de dados do servidor de gerenciamento

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>Especifica que o banco de dados de gerenciamento será instalado. Você deve ter permissões de banco de dados suficientes para concluir a instalação. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica que a instância SQL padrão deve ser usada. Nenhum valor é esperado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica o nome da instância SQL personalizada que deve ser usada para criar um novo banco de dados. Exemplo de uso: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer" </strong> . Se/DB_PREDEPLOY_MANAGEMENT não for especificado, isso será ignorado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Especifica o nome do novo banco de dados de gerenciamento que deve ser criado. Exemplo de uso: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Se/DB_PREDEPLOY_MANAGEMENT não for especificado, isso será ignorado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica se o servidor de gerenciamento que vai acessar o banco de dados está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Especifica a conta de máquina do computador remoto em que o servidor de gerenciamento será instalado. Exemplo de uso: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica a conta de administrador que será usada para instalar o servidor de gerenciamento. Exemplo de uso: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "DOMAIN\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros para instalar o Publishing Server

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>Especifica que o servidor de publicação será instalado. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>Especifica a URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado. Exemplo de uso: <strong> http:// &lt; Management Server Name &gt; : número de &lt; porta do servidor de gerenciamento &gt; </strong> . Se/PUBLISHING_SERVER não for usado, este parâmetro será ignorado</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica o nome do site que será criado para o serviço de publicação. Por exemplo,/PUBLISHING_WEBSITE_NAME = "serviço Microsoft App-V Publishing"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica o número da porta usada pelo serviço de publicação. Por exemplo,/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros do servidor de relatório

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>Especifica que o servidor de relatórios será instalado. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica o nome do site que será criado para o serviço de relatório. Ex. /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica o número da porta que o serviço de relatórios vai usar. Ex. /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### Parâmetros para usar um banco de dados do servidor de relatórios existente

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica que o Microsoft SQL Server está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Especifica o nome do computador remoto no qual o SQL Server está instalado. Usa uma cadeia de caracteres. Ex. /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ DB_SQLINSTANCE_USE_DEFAULT de relatório <em></p></td>
    <td align="left"><p>Indica que a instância SQL padrão deve ser usada. Parâmetro de opção; portanto, nenhum valor é esperado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica o nome da instância SQL personalizada que deve ser usada. Usa uma cadeia de caracteres. Ex. /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYsqlserver&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ _DB_NAME DE RELATÓRIO</p></td>
    <td align="left"><p>Especifica o nome do banco de dados de relatórios existente que deve ser usado. Usa uma cadeia de caracteres. Ex. /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros para instalar o banco de dados do servidor de relatório

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>Especifica que o banco de dados de relatórios será instalado. As permissões do DBA são necessárias para esta instalação. Nenhum valor é esperado</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Especifica o nome da instância SQL personalizada que deve ser usada. Usa uma cadeia de caracteres. Ex. /REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYsqlserver&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>Especifica o nome do novo banco de dados de relatórios que deve ser criado. Usa uma cadeia de caracteres. Ex. /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica que o servidor de relatórios que vai acessar o banco de dados está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Especifica a conta de máquina do computador remoto em que o servidor de relatórios será instalado. Usa uma cadeia de caracteres. Ex. /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica a conta de administrador que será usada para instalar o servidor de relatórios do App-V. Usa uma cadeia de caracteres. Ex. /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; DOMAIN\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parâmetros para usar um banco de dados existente do servidor de gerenciamento

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Informações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica que o SQL Server está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado. Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Especifica o nome do computador remoto no qual o SQL Server está instalado. Usa uma cadeia de caracteres. Ex. /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica que a instância SQL padrão deve ser usada. Parâmetro de opção; portanto, nenhum valor é esperado. Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica o nome da instância SQL personalizada que será usada. Exemplo de uso <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Especifica o nome do banco de dados de gerenciamento existente que deve ser usado. Exemplo de uso: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Se/DB_PREDEPLOY_MANAGEMENT for especificado, será ignorado.</p>
    <p></p>
    <p><strong>Tem uma sugestão para o App-V </strong> ? Adicione ou vote em sugestões <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> aqui </a> . <strong>Tem um App-V emissão </strong> e? Use o <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Fórum do TechNet do App-V </a> .</p></td>
</tr>
</tbody>
</table>
  

## Tópicos relacionados

[Implantação do servidor App-V 5.0](deploying-the-app-v-50-server.md)

 

 





