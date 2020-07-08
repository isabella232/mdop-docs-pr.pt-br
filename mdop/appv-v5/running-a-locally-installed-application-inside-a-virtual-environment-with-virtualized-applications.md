---
title: Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados
description: Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796218"
---
# Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados


Você pode executar um aplicativo instalado localmente em um ambiente virtual, juntamente com aplicativos que foram virtualizados usando o Microsoft Application Virtualization (App-V). Você pode querer fazer isso se:

-   Deseja instalar e executar um aplicativo localmente em computadores cliente, mas deseja virtualizar e executar plug-ins específicos que funcionem com esse aplicativo local.

-   Está Solucionando problemas em um pacote do cliente App-V e deseja abrir um aplicativo local dentro do ambiente virtual do App-V.

Use qualquer um dos seguintes métodos para abrir um aplicativo local dentro do ambiente virtual do App-V:

-   [Chave do registro RunVirtual](#bkmk-runvirtual-regkey)

-   [Cmdlet Get-AppvClientPackage do PowerShell](#bkmk-get-appvclientpackage-posh)

-   [Opções de linha de comando/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [Chave do gancho de linha de/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Cada método realiza essencialmente a mesma tarefa, mas alguns métodos podem ser mais adequados para alguns aplicativos do que outros, dependendo se o aplicativo virtualizado já está em execução.

## <a href="" id="bkmk-runvirtual-regkey"></a>Chave do registro RunVirtual


Para adicionar um aplicativo instalado localmente a um pacote ou a um ambiente virtual do grupo de conexão, adicione uma subchave à `RunVirtual` chave do registro no editor do registro, conforme descrito nas seções a seguir.

Não há nenhuma configuração de política de grupo disponível para gerenciar essa chave do registro, portanto, você precisa usar o System Center Configuration Manager ou outro sistema ESD (distribuição de software eletrônico) ou editar manualmente o registro.

### <a href="" id="bkmk-"></a>Métodos com suporte de publicação de pacotes ao usar RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do App-V</th>
<th align="left">Métodos de publicação com suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Publicado globalmente ou para o usuário</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 até App-V 5,0 SP2</p></td>
<td align="left"><p>Publicado globalmente apenas</p></td>
</tr>
</tbody>
</table>

 

### Etapas para criar a subchave

1.  Usando as informações da tabela a seguir, crie uma nova chave do registro usando o nome do arquivo executável, por exemplo, **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Método de publicação de pacote</th>
    <th align="left">Onde criar a chave do registro</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Publicado globalmente</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Exemplo </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Publicado para o usuário</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Exemplo </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>O grupo conexão pode conter:</p>
    <ul>
    <li><p>Pacotes que são publicados apenas globalmente ou apenas para o usuário</p></li>
    <li><p>Pacotes publicados globalmente e para o usuário</p></li>
    </ul></td>
    <td align="left"><p>A tecla HKEY_LOCAL_MACHINE ou HKEY_CURRENT_USER, mas todas as seguintes opções devem ser verdadeiras:</p>
    <ul>
    <li><p>Se quiser incluir vários pacotes no ambiente virtual, você deve incluí-los em um grupo de conexão habilitado.</p></li>
    <li><p>Crie apenas uma subchave para um dos pacotes no grupo de conexão. Se, por exemplo, você tiver um pacote publicado globalmente e outro pacote publicado para o usuário, crie uma subchave para qualquer um desses pacotes, mas não ambos. Embora você crie uma subchave para apenas um dos pacotes, todos os pacotes no grupo de conexão, além do aplicativo local, estarão disponíveis no ambiente virtual.</p></li>
    <li><p>A chave na qual você cria a subchave deve corresponder ao método de publicação usado para o pacote.</p>
    <p>Por exemplo, se você publicou o pacote para o usuário, deverá criar a subchave em <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Defina o valor da nova subchave do registro como o PackageID e VersionId do pacote, separando os valores com um sublinhado.

    **Sintaxe**: &lt; PackageID &gt; \ _ &lt; VersionId&gt;

    **Exemplo**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    O aplicativo no exemplo anterior produziria um arquivo de exportação do registro (arquivo. reg) como o seguinte:

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Cmdlet Get-AppvClientPackage do PowerShell


Você pode usar o cmdlet **Start-AppVVirtualProcess** para recuperar o nome do pacote e iniciar um processo dentro do ambiente virtual do pacote especificado. Esse método permite iniciar qualquer comando dentro do contexto de um pacote do App-V, independentemente de o pacote estar em execução no momento.

Use a sintaxe de exemplo a seguir e substitua o nome do ** &lt; &gt; pacote do pacote:**

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Se não souber o nome exato do pacote, você pode usar a linha de comando **Get-AppvClientPackage \ * executable\\** <em> , em que **executável </em> * é o nome do aplicativo, por exemplo: Get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>Opções de linha de comando/appvpid: &lt; PID&gt;


Você pode aplicar a opção **/appvpid &lt; : &gt; pid** a qualquer comando, que permite que esse comando seja executado em um processo virtual que você seleciona especificando a identificação do processo (PID). Usar esse método inicia o novo executável no mesmo ambiente do App-V como um executável que já está em execução.

Exemplo: `cmd.exe /appvpid:8108`

Para localizar a ID do processo (PID) do seu processo App-V, execute o comando **tasklist.exe** de um prompt de comando elevado.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>Chave do gancho de linha de/appvve: &lt; GUID&gt;


Essa opção permite executar um comando local dentro do ambiente virtual de um pacote do App-V. Ao contrário da opção **/appvid** , em que o ambiente virtual já deve estar em execução, essa opção permite que você inicie o ambiente virtual.

Syntax `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Exemplo: `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Para obter o GUID do pacote e a versão do seu aplicativo, execute o cmdlet **Get-AppvClientPackage** . Concatene a opção **/appvve** com o seguinte:

-   Dois pontos

-   GUID do pacote do pacote desejado

-   Um sublinhado

-   ID da versão do pacote desejado

Se você não souber o nome exato do pacote, use a linha de comando **Get-AppvClientPackage \ * executable\\** <em> , em que ** </em> executável* é o nome do aplicativo, por exemplo: Get-AppvClientPackage \ * Word \ *.

Esse método permite iniciar qualquer comando dentro do contexto de um pacote do App-V, independentemente de o pacote estar em execução no momento.






## Tópicos relacionados


[Referência técnica para o App-V 5.0](technical-reference-for-app-v-50.md)

 

 





