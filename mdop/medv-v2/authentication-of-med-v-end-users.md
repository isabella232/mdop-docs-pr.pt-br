---
title: Autenticação de usuários finais da MED-V
description: Autenticação de usuários finais da MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799562"
---
# Autenticação de usuários finais da MED-V


A autenticação do Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 para usuários finais é um problema de segurança muito importante. Nesse contexto, a autenticação se refere a verificar a identidade do usuário final do MED-V.

A seção a seguir fornece informações e orientação sobre a autenticação do usuário final no MED-V.

## Autenticação de usuário no MED-V


A autenticação no MED-V geralmente ocorre em dois níveis: quando um usuário acessa o MED-V pela primeira vez e sempre que eles alteram a senha.

Dependendo de como você configurou as configurações do MED-V para autenticação, o usuário final geralmente é solicitado em algum ponto para inserir a senha, seja na primeira vez em que o MED-V é iniciado ou na primeira vez que tentam abrir um aplicativo publicado.

Há vários aspectos da autenticação de usuários finais que você pode controlar, incluindo os seguintes:

Se as credenciais que o usuário final insere são armazenadas no Gerenciador de credenciais

De que maneira o usuário final receberá a opção de inserir e salvar sua senha

Dependendo do processo preferido da sua empresa para gerenciar a autenticação do usuário final, você pode especificar se o cache de credenciais ocorre para um determinado espaço de trabalho do MED-V. O armazenamento em cache das credenciais de um usuário final é útil porque elas são solicitadas apenas uma vez por sua senha. Se o usuário final não tiver permissão para salvar a senha ou se decidir não fazê-lo, todas as vezes que iniciarem uma nova sessão do MED-V, eles devem inseri-la novamente. Por exemplo, se o MED-V estiver configurado para ser iniciado quando o usuário final fizer logon no host, mas a autenticação estiver desabilitada, o usuário final será solicitado apenas uma vez durante o logon. Nesse caso, as credenciais são válidas até que o usuário final efetue logoff do host.

Se for necessário, você pode usar o Gerenciador de credenciais para remover todas as credenciais de usuário final armazenadas.

Por padrão, o armazenamento de credenciais está desabilitado, mas você pode alterar essa configuração por meio de um dos seguintes métodos:

**Durante a criação do pacote do espaço de trabalho do MED-V**. Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).

**Após a implantação do espaço de trabalho do MED-V**. Edite o parâmetro UxCredentialCacheEnabled do cmdlet do MED-V para definir a chave do registro dos serviços de terminal. Para obter mais informações, consulte a ajuda do Windows PowerShell.

Após a implantação do espaço de trabalho do MED-V, você pode definir sua preferência para a autenticação de usuário final modificando a política de serviços de terminal chamada DisablePasswordSaving. DisablePasswordSaving controla se a caixa de seleção Salvar senha é exibida na janela de diálogo do cliente RDP e se o prompt de credenciais do MED-V é exibido.

Veja a seguir o caminho da política da política de serviços de terminal chamada DisablePasswordSaving.

**Regedit**

HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving

**Observação**  
As alterações feitas no DisablePasswordSaving só afetam o prompt RDP para uma máquina virtual.



A tabela a seguir lista as maneiras diferentes pelas quais você pode definir suas configurações para o armazenamento de credenciais e os efeitos das diferentes configurações:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Configuração</th>
<th align="left">Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Desabilitado</strong></p></td>
<td align="left"><p>O prompt do MED-V é apresentado e uma caixa de seleção para aceitar está disponível e desmarcada. Se o usuário final marcar a caixa de seleção, as credenciais serão armazenadas em cache para uso posterior. O usuário final também tem a vantagem de ser avisado apenas quando a senha expira.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Se o usuário final não marcar a caixa de seleção, o prompt do cliente de conexão de área de trabalho remota (RDC) será apresentado em vez do prompt do MED-V, e a caixa de seleção a ser aceita será desmarcada. Se o usuário final marcar a caixa de seleção, a credencial do cliente RDC será armazenada para uso posterior.</p>
<div class="alert">
<strong>Importante</strong><br/><p>A RDC não valida as credenciais quando o usuário termina de inseri-las. Se o usuário final armazenar as credenciais em cache por meio do prompt de RDC, há um risco de que credenciais incorretas possam ser armazenadas. Nesse caso, as credenciais incorretas devem ser excluídas no Gerenciador de credenciais do Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Habilitado</strong></p></td>
<td align="left"><div class="alert">
<strong>Observação</strong><br/><p>Essa configuração é mais segura porque não permite que as credenciais do usuário final sejam armazenadas em cache.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Por padrão, a instalação do MED-V define uma chave do registro no convidado para suprimir o prompt "senha sobre para expirar". O usuário final é solicitado apenas por uma alteração de senha no host. As credenciais que são atualizadas no host são passadas para o convidado.

**Tenha**  
Se você usar a política de grupo em seu ambiente, saiba que ela pode substituir a chave do registro que faz com que os prompts de senha do convidado reapareçam.



### Questões de segurança com a autenticação

Embora o armazenamento em cache das credenciais do usuário final forneça a melhor experiência do usuário, você deve estar ciente dos riscos envolvidos.

Quando o cache de credenciais está habilitado, a credencial do domínio do usuário final é armazenada em um formato reversível dentro do Gerenciador de credenciais do Windows. Como resultado, um invasor pode gravar uma ferramenta que é executada como um processo no nível do sistema ou um processo do usuário final e recupera as credenciais do usuário final. Você só pode diminuir esse risco Configurando DisablePasswordSaving como **habilitado**.

Essa mesma preocupação existe quando a autenticação do MED-V está desabilitada, mas a configuração de política dos serviços de terminal está habilitada.

## Tópicos relacionados


[Práticas recomendadas de segurança para operações da MED-V](security-best-practices-for-med-v-operations.md)









