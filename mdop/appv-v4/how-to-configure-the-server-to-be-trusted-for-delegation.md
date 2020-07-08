---
title: Como configurar o servidor para ser confiável para delegação
description: Como configurar o servidor para ser confiável para delegação
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797187"
---
# Como configurar o servidor para ser confiável para delegação


Ao instalar o software do servidor de gerenciamento do Microsoft Application Virtualization (App-V), você pode optar por instalá-lo usando uma arquitetura de sistema distribuído. Se você instalar o console, o serviço de gerenciamento da Web e o banco de dados em computadores diferentes, será necessário configurar o servidor de serviços de informações da Internet (IIS) para ser confiável para delegação. Isso é necessário porque o serviço Web de gerenciamento tentará se conectar ao repositório de dados do App-V usando as credenciais do administrador do App-V que está usando o console. O servidor de banco de dados no qual o repositório de dados está instalado não aceitará as credenciais do administrador do servidor IIS, a menos que o servidor IIS esteja configurado para ser confiável para delegação e, portanto, o serviço Web de gerenciamento não poderá se conectar ao repositório de dados do App-V.

**Observação**  Se você instalar o software do App-V Management Server em um único servidor e colocar o repositório de dados em um servidor separado, há uma situação em que você ainda deve configurar o servidor para ser confiável para delegação, embora o serviço Web de gerenciamento e o console de gerenciamento estejam no mesmo servidor. Essa situação ocorre se você precisar se conectar ao serviço Web de gerenciamento no console usando a opção **usar credenciais alternativas** .

 

O tipo de delegação que você pode usar depende do nível funcional do domínio que você configurou na infraestrutura dos serviços de domínio Active Directory (ADDS). A tabela a seguir lista os tipos de delegação que podem ser configurados para cada nível funcional de domínio do App-V. Instruções detalhadas seguem a tabela.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nível funcional do domínio</th>
<th align="left">Níveis de delegação disponíveis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 nativo</p></td>
<td align="left"><ul>
<li><p>Sem delegação (padrão)</p></li>
<li><p>Delegação irrestrita</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>Sem delegação (padrão)</p></li>
<li><p>¹ de delegação irrestrito</p></li>
<li><p>Delegação restrita (usar protocolos somente Kerberos)</p></li>
<li><p>Delegação restrita (usar qualquer protocolo de autenticação) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ não recomendado.

## Para configurar a delegação irrestrita quando o nível funcional do domínio for Windows 2000 nativo


No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.

****

1.  Clique em **Iniciar**, **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.

2.  Expanda domínio e, em seguida, expanda a pasta computadores.

3.  No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web e, em seguida, clique em **Propriedades**.

4.  Na guia **geral** , verifique se a caixa de seleção **confiar no computador para delegação** está marcada.

5.  Clique em **OK**.

## Para configurar a delegação irrestrita quando o nível funcional do domínio for Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2


No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.

****

1.  Clique em **Iniciar**, em **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.

2.  Expanda domínio e expanda a pasta computadores.

3.  No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web, selecione **Propriedades**e, em seguida, clique na guia **delegação** .

4.  Clique para selecionar **confiar neste computador para delegação a qualquer serviço (somente Kerberos)**.

5.  Clique em **OK**.

## Para configurar a delegação restrita quando o nível funcional do domínio for Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2


No controlador de domínio do domínio do seu servidor da Web, conclua as etapas a seguir.

****

1.  Clique em **Iniciar**, em **Ferramentas administrativas**e em **usuários e computadores do Active Directory**.

2.  Expanda domínio e, em seguida, expanda a pasta computadores.

3.  No painel direito, clique com o botão direito do mouse no nome do computador do servidor Web, selecione **Propriedades**e, em seguida, clique na guia **delegação** .

4.  Clique para selecionar **confiar neste computador para delegação apenas a serviços especificados**.

5.  Verifique se a **somente usar Kerberos** está selecionada e clique em **OK**.

6.  Clique no botão **Adicionar** . Na caixa de diálogo **Adicionar serviços** , clique em **usuários ou computadores**e, em seguida, navegue até ou digite o nome do Microsoft SQL Server que tem o repositório de dados App-V e é receber as credenciais de usuários do IIS. Clique em **OK**.

7.  Na lista **serviços disponíveis** , selecione o serviço MSSQLSvc que lista o número da porta na qual o Microsoft SQL Server está aceitando conexões para o banco de dados do App-V (a porta padrão é 1433). Clique em **OK**.

### Etapas adicionais para configurar o IIS 7 para delegação restrita

Se você estiver executando o serviço Web de gerenciamento em um servidor do IIS 7, deve completar as etapas a seguir para definir a variável *useAppPoolCredentials* do IIS 7 como true.

1.  Abra uma janela de prompt de comando com privilégios elevados. Para abrir uma janela de prompt de comando elevado, clique em **Iniciar**, clique em **todos os programas**, clique em **acessórios**, clique com o botão direito do mouse em **prompt de comando**e clique em **Executar como administrador**.

2.  Navegue até%windir%\\system32\\inetsrv.

3.  Digite **appcmd.exe set config-section: System. WebServer/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**e pressione Enter.

 

 





