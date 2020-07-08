---
title: Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell
description: Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796371"
---
# Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell


Um grupo de conexões App-V permite que você execute todos os aplicativos virtuais como um conjunto definido de pacotes em um único ambiente virtual. Por exemplo, você pode virtualizar um aplicativo e seus plug-ins usando pacotes separados, mas executá-los juntos em um único grupo de conexão.

Um arquivo XML de grupo de conexão define o grupo de conexão que é executado no computador em que você instalou o cliente App-V. Para obter informações sobre o arquivo XML do grupo de conexão e como configurá-lo, consulte [sobre o arquivo do grupo de conexão](about-the-connection-group-file.md).

Este tópico explica os seguintes procedimentos:

-   [Para adicionar e publicar os pacotes do App-V no grupo de conexão](#bkmk-add-pub-pkgs-in-cg)

-   [Para adicionar e habilitar o grupo de conexão no cliente App-V](#bkmk-add-enable-cg-on-clt)

-   [Para habilitar ou desabilitar um grupo de conexões para um usuário específico](#bkmk-enable-cg-for-user-poshtopic)

-   [Para permitir que somente administradores habilitem grupos de conexão](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**Para adicionar e publicar os pacotes do App-V no grupo de conexão**

1.  Para adicionar e publicar os pacotes do App-V 5,0 no computador que está executando o cliente App-V, digite o seguinte comando:

    Add-AppvClientPackage – path c:\\tmpstore\\quartfin.AppV | Publicar-AppvClientPackage

2.  Repita a **etapa 1** deste procedimento para cada pacote no grupo de conexão.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**Para adicionar e habilitar o grupo de conexão no cliente App-V**

1.  Adicione o grupo de conexão digitando o seguinte comando:

    Add-AppvClientConnectionGroup – caminho c:\\tmpstore\\financ.xml

2.  Habilite o grupo de conexão digitando o seguinte comando:

    Enable-AppvClientConnectionGroup – nome "aplicativos financeiros"

    Quando qualquer aplicativo virtual que esteja nos pacotes de membros são executados no computador de destino, eles serão executados dentro do ambiente virtual do grupo de conexão e estarão disponíveis para todos os aplicativos virtuais nos outros pacotes do grupo de conexão.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**Para habilitar ou desabilitar um grupo de conexões para um usuário específico**

1.  Examine a descrição e os requisitos do parâmetro:

    -   O parâmetro permite que um administrador habilite ou desabilite um grupo de conexão para um usuário específico.

    -   Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.

    -   Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.

    -   Você deve estar conectado com credenciais administrativas para usar o parâmetro.

    -   O usuário final deve estar conectado.

    -   Você deve fornecer o SID (identificador de segurança) do usuário final.

2.  Use os seguintes cmdlets e adicione o parâmetro Optional **– userid** , em que **-deusers** representa o Sid (identificador de segurança) do usuário final:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Exemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**Para permitir que somente administradores habilitem grupos de conexão**

1.  Examine a descrição e a necessidade de usar este cmdlet:

    -   Use este cmdlet e parâmetro para configurar o cliente App-V para permitir que somente administradores (não usuários finais) habilitem ou desabilitem grupos de conexão.

    -   Você deve estar usando pelo menos o App-V 5,0 SP3 para usar este cmdlet.

2.  Execute o seguinte cmdlet e parâmetro:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Parâmetro e valores</th>
    <th align="left">Exemplo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0-falso</p></li>
    <li><p>1-verdadeiro</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

[Administração do App-V usando o PowerShell](administering-app-v-by-using-powershell.md)

 

 





