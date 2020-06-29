---
title: Como recuperar uma unidade corrompida
description: Como recuperar uma unidade corrompida
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799095"
---
# Como recuperar uma unidade corrompida


Você pode usar esse procedimento com o site de administração e monitoramento (também conhecido como o Help Desk) para recuperar uma unidade corrompida protegida pelo BitLocker. Para fazer isso, você irá concluir as tarefas descritas na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes e mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crie um arquivo de pacote de chave de recuperação acessando a <strong> </strong> área de recuperação de unidade do site de administração e monitoramento.</p></td>
<td align="left"><p>Para acessar a <strong> área de recuperação da unidade </strong> , você deve ser atribuído à função usuários da assistência técnica do MBAM ou à função usuários avançados da assistência técnica do MBAM. Você pode ter atribuído a essas funções nomes diferentes quando você as criou. Para obter mais informações, consulte <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> planejando para contas e grupos do MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copie o arquivo do pacote para o computador que contém a unidade corrompida.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Use o <code>repair-bde</code> comando para concluir o processo de recuperação.</p></td>
<td align="left"><p>Para evitar uma possível perda de dados, é altamente recomendável que você examine o <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-bde </a> antes de usá-lo.</p></td>
</tr>
</tbody>
</table>

 

**Para recuperar uma unidade corrompida**

1.  Abra um navegador da Web e navegue até o **site de administração e monitoramento**.

2.  No painel esquerdo, selecione **recuperação de unidade** para abrir a página **recuperar acesso a uma unidade criptografada** .

3.  Insira o domínio de logon do Windows do usuário final e o nome de usuário, o motivo para desbloquear a unidade e a ID da senha de recuperação do usuário final.

    **Observação**  Se você for membro do grupo de acesso de usuários avançados da assistência técnica, não será necessário inserir o nome de domínio ou o nome de usuário do usuário.

     

4.  Clique em **Enviar**. A chave de recuperação será exibida.

5.  Clique em **salvar**e selecione **pacote de chave de recuperação**. O pacote da chave de recuperação será criado em seu computador.

6.  Copie o pacote da chave de recuperação para o computador que tem a unidade corrompida.

7.  Abra um prompt de comando com privilégios elevados. Para fazer isso, clique em **Iniciar** e digite `cmd` na caixa de texto **Pesquisar programas e arquivos** . Clique com o botão direito do mouse **cmd.exe**e selecione **Executar como administrador**.

8.  No prompt de comando, digite o seguinte:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Observação**  Substitua &lt; *unidade fixa* &gt; por uma unidade de disco rígido disponível com espaço livre igual ou maior que os dados na unidade corrompida. Os dados na unidade corrompida são recuperados e movidos para a unidade de disco rígido especificada.

     


## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





