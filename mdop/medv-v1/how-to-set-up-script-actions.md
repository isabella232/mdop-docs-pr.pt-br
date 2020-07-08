---
title: Como configurar ações de script
description: Como configurar ações de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795987"
---
# Como configurar ações de script


O editor de ações de script permite que o administrador crie ações a serem executadas durante a configuração do espaço de trabalho do MED-V, bem como definir a ordem na qual elas são executadas.

Veja a seguir uma lista de ações que podem ser adicionadas ao script de configuração de domínio:

-   **Reinicie o Windows**— reinicie o Windows.

-   **Ingressar no domínio**— se estiver ingressando em um domínio, inclua esta ação e configure o nome de usuário, a senha, o nome de domínio totalmente qualificado, o nome de domínio NetBIOS e a unidade organizacional (opcional).

-   **Verifique a conectividade**-configure um servidor para se conectar e verifique se o espaço de trabalho do MED-V pode se conectar a um recurso de rede (como o servidor de domínio).

-   **Linha de comando**— configure um script no espaço de trabalho do MED-V e insira uma linha de comando que inclua o caminho do script e os argumentos do script.

-   **Renomear computador**— renomeie o computador da máquina virtual com base nas configurações definidas.

-   **Desabilitar o logon automático**— desabilitar o logon automático do Windows. Esta ação deve ser adicionada ao final dos scripts que adicionam o computador ao domínio.

## <a href="" id="how-to-set-up-script-actions-"></a>Como configurar ações de script


**Para configurar as ações de script**

1.  Na guia **configuração da VM** , clique em **Editor de script**.

2.  Na caixa de diálogo **ações de script** , clique em **Adicionar**e, no submenu, clique nas ações desejadas.

3.  Configure as ações conforme descrito nas tabelas a seguir.

    **Observação** 
     **Renomear computador** está configurado na guia **configurações da VM** . Para obter mais informações, consulte [como configurar as propriedades do padrão de nome do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. Defina a ordem das ações selecionando uma ação e clicando em **para cima** ou **para baixo**.

5. Clique em **OK**.

**Observação**  
Ao executar o script de domínio de junção, para que o script funcione, o usuário conectado na máquina virtual do espaço de trabalho do MED-V deve ter direitos de administrador local.



**Observação**  
Ao executar o script Disable auto-logon, é recomendável desabilitar a conta de convidado local usada para o logon automático quando a configuração inicial for concluída.



### <a href="" id="bkmk-joindomainproperties"></a>

**Ingressar em Propriedades de domínio**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Credenciais a serem usadas ao ingressar na VM no domínio</p></td>
<td align="left"><p>Selecione uma das seguintes credenciais para usar ao ingressar na VM no domínio:</p>
<ul>
<li><p><strong>Use as credenciais do MED-V </strong> – as credenciais do usuário final.</p></li>
<li><p><strong>Use as seguintes credenciais </strong> : as credenciais especificadas; Insira um nome de usuário e senha nos campos correspondentes.</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>As credenciais que você insere são visíveis para todos os usuários do espaço de trabalho do MED-V. Não é recomendável fornecer credenciais de administrador do domínio.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Domínio no qual ingressar</p></td>
<td align="left"><p>Selecione uma destas opções:</p>
<ul>
<li><p><strong>Use o nome de domínio utilizado ao iniciar o espaço de trabalho </strong> — ingresse no domínio inserido pelo usuário final ao fazer logon no cliente MED-V.</p>
<p>Para definir o mapeamento do NetBIOS para nomes de domínio totalmente qualificados, clique em <strong> tabela de mapeamento de domínio global </strong> . Na tabela de mapeamento de domínio global, clique em <strong> Adicionar </strong> , insira um <strong> nome de domínio NetBIOS </strong> e um <strong> nome de domínio totalmente qualificado </strong> e clique em <strong> OK </strong> .</p></li>
<li><p><strong>Use o nome de domínio a seguir </strong> — ingresse no domínio especificado; Insira um nome de domínio e um nome de domínio NetBIOS nos campos correspondentes.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidade organizacional</p></td>
<td align="left"><p>Uma unidade organizacional (OU) pode ser especificada para ingressar o computador em uma UO específica. O formato deve seguir um nome diferenciado da OU: OU = &lt; unidade organizacional &gt; , &lt; controlador &gt; de domínio (por exemplo, ou = QATest, DC = Il, DC = MED-V, DC = com).</p>
<div class="alert">
<strong>Aviso</strong><br/><p>Só há suporte para uma única OU de nível, conforme mostrado no exemplo acima.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**Verificar Propriedades de conectividade**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Endereço IP</p></td>
<td align="left"><p>O endereço IP do servidor para o qual você está verificando a conexão.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>A porta do servidor para a qual você está verificando a conexão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tempo limite</p></td>
<td align="left"><p>O número de segundos para esperar por uma resposta antes do tempo limite.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**Propriedades da linha de comando**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Caminho</p></td>
<td align="left"><p>O caminho da linha de comando.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Argumentos</p></td>
<td align="left"><p>Argumentos de linha de comando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aguardar saída</p></td>
<td align="left"><p>Marque a caixa de seleção para aguardar um retorno antes de continuar com as ações do script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Falha em erro</p></td>
<td align="left"><p>Marque esta caixa de seleção se o retorno for algo diferente do valor especificado.</p>
<p>Digite o valor que indicará o comando como sucesso.</p>
<p>Padrão: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Executar apenas uma vez</p></td>
<td align="left"><p>Marque esta caixa de seleção para executar a linha de comando somente uma vez. Se o script falhar ou for cancelado, esse comando não será executado novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esta linha de comando causa uma reinicialização do Windows no espaço de trabalho</p></td>
<td align="left"><p>Marque esta caixa de seleção se a linha de comando causar uma reinicialização após a conclusão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir interação</p></td>
<td align="left"><p>Marque esta caixa de seleção se o comando exigir a interação do usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mensagem de progresso</p></td>
<td align="left"><p>Mensagem a ser exibida para o usuário enquanto o comando está em execução.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mensagem de falha</p></td>
<td align="left"><p>Mensagem a ser exibida para o usuário se o comando falhar.</p></td>
</tr>
</tbody>
</table>

 

Durante a configuração da ação da linha de comando, várias variáveis podem ser usadas conforme definido na tabela a seguir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valor</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>%MEDVUser%</p></td>
<td align="left"><p>Um nome de usuário autenticado.</p></td>
<td align="left"><p>Nome de usuário autenticado do MED-V. O nome de usuário e a senha podem ser usados no script de configuração de VM de domínio ingressar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%MEDVPassword%</p></td>
<td align="left"><p>Uma senha autenticada.</p></td>
<td align="left"><p>Senha autenticada do MED-V. O nome de usuário e a senha podem ser usados no script de configuração de VM de domínio ingressar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>%MEDVDomain%</p></td>
<td align="left"><p>Domínio configurado.</p></td>
<td align="left"><p>O domínio configurado na autenticação do MED-V. Ele pode ser usado no script de configuração da VM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>Nome do computador.</p></td>
<td align="left"><p>O nome de computador exclusivo configurado no aplicativo de gerenciamento. Ele pode ser usado no script de configuração da VM.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Como definir a configuração de máquina virtual de um espaço de trabalho do MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Como configurar as propriedades de padrão de nomes do computador VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





