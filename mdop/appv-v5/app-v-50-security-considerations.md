---
title: Considerações de segurança do App-V 5.0
description: Considerações de segurança do App-V 5.0
author: dansimp
ms.assetid: 1e7292a0-7972-4b4f-85a9-eaf33f6c563a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fcd740345be7f532502b8996d8d2b1f4437ed6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796592"
---
# Considerações de segurança do App-V 5.0


Este tópico contém uma breve visão geral das contas e dos grupos, dos arquivos de log e outras considerações relacionadas à segurança do App-V 5,0.

**Importante**  
O App-V 5,0 não é um produto de segurança e não fornece garantias para um ambiente seguro.



## O recurso PackageStoreAccessControl (PSAC) foi preterido


Em vigor a partir de junho de 2014, o PackageStoreAccessControl (PSAC) que foi introduzido no Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) foi preterido em ambientes com um único usuário e vários usuários.

## Considerações gerais sobre segurança


**Compreender os riscos de segurança.** O risco mais sério para o App-V 5,0 é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia então reconfigurar dados de chave nos clientes do App-V 5,0. A perda da funcionalidade do App-V 5,0 por um curto período de tempo devido a um ataque de negação de serviço geralmente não teria um impacto catastrófico.

**Proteja seus computadores fisicamente**. A segurança está incompleta sem segurança física. Qualquer pessoa com acesso físico a um servidor do App-V 5,0 pode atacar potencialmente toda a base de clientes. Qualquer ataque físico potencial deve ser considerado de alto risco e diminuído apropriadamente. Os servidores do App-V 5,0 devem ser armazenados em uma sala de servidor fisicamente seguro com acesso controlado. Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.

**Aplicar as atualizações de segurança mais recentes a todos os computadores**. Para se manter informado sobre as atualizações mais recentes dos sistemas operacionais, do Microsoft SQL Server e do App-V 5,0, assine o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Use senhas fortes ou frases secretas**. Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do App-V 5,0 e do App-V 5,0. Nunca use senhas em branco. Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Contas e grupos no App-V 5,0


Uma prática recomendada para o gerenciamento de contas de usuários é criar grupos globais de domínio e adicionar contas de usuário a eles. Em seguida, adicione as contas globais do domínio aos grupos locais do App-V 5,0 nos servidores App-V 5,0.

**Observação**  
As contas de computador cliente App-V que precisam se conectar ao servidor de publicação devem fazer parte do grupo local de **usuários** do servidor de publicação. Por padrão, todos os computadores no domínio fazem parte do grupo **usuários autorizados** , que faz parte do grupo local **usuários** .



### <a href="" id="-------------app-v-5-0-server-security"></a> Segurança do App-V 5,0 Server

Nenhum grupo é criado automaticamente durante a configuração do App-V 5,0. Você deve criar os seguintes grupos globais dos serviços de domínio Active Directory para gerenciar operações do servidor do App-V 5,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome do grupo</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Grupo de administração do App-V Management</p></td>
<td align="left"><p>Usado para gerenciar o servidor de gerenciamento do App-V 5,0. Esse grupo é criado durante a instalação do servidor de gerenciamento do App-V 5,0.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Não há nenhum método para criar o grupo usando o console de gerenciamento após concluir a instalação.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Leitura/gravação de banco de dados para conta de serviço de gerenciamento</p></td>
<td align="left"><p>Fornece acesso de leitura/gravação ao banco de dados de gerenciamento. Essa conta deve ser criada durante a instalação do banco de dados de gerenciamento do App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conta de administrador de instalação do App-V Management Service</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isso só será necessário se o banco de dados de gerenciamento estiver sendo instalado separadamente do serviço.</p>
</div>
<div>

</div></td>
<td align="left"><p>Fornece acesso público à tabela de versão de esquema no banco de dados de gerenciamento. Essa conta deve ser criada durante a instalação do banco de dados de gerenciamento do App-V 5,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conta de administrador de instalação do App-V Reporting Service</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isso só é necessário se o banco de dados de relatórios estiver sendo instalado separadamente do serviço.</p>
</div>
<div>

</div></td>
<td align="left"><p>Acesso público à tabela de versão de esquema em banco de dados de relatório. Essa conta deve ser criada durante a instalação do banco de dados de relatórios do App-V 5,0.</p></td>
</tr>
</tbody>
</table>



Considere as seguintes informações adicionais:

-   Acesso aos compartilhamentos de pacote-se houver um compartilhamento no mesmo computador que o servidor de gerenciamento, o serviço de **rede** requer acesso de leitura ao compartilhamento. Além disso, cada computador cliente App-V deve ter acesso de leitura ao compartilhamento de pacote.

    **Observação**  
    Em versões anteriores do App-V, o compartilhamento de pacote era chamado de compartilhamento de conteúdo.



-   Registrar servidores de publicação com o servidor de gerenciamento-um servidor de publicação deve ser registrado com o servidor de gerenciamento. Por exemplo, ele deve ser adicionado ao banco de dados para que as contas do computador do servidor de publicação possam chamar a API do serviço de gerenciamento.

### <a href="" id="-------------app-v-5-0-package-security"></a> Segurança do pacote do App-V 5,0

Os itens a seguir o ajudarão a planejar a segurança para garantir que os pacotes virtualizados sejam seguros.

-   Se um instalador do aplicativo aplicar uma ACL (lista de controle de acesso) a um arquivo ou diretório, essa ACL não será mantida no pacote. Quando o pacote é implantado, se o arquivo ou diretório for modificado por um usuário, ele herdará a ACL no **% USERPROFILE%** ou herdará a ACL do diretório do computador de destino. O primeiro caso ocorre se o arquivo ou diretório não existir em um local do sistema de arquivos virtual; o último caso ocorre se o arquivo ou diretório existir em um local do sistema de arquivos virtual, por exemplo, **% windir%**.

## <a href="" id="---------app-v-5-0-log-files"></a> Arquivos de log do App-V 5,0


Durante a instalação do App-V 5,0, os arquivos de log de instalação são criados na pasta **% Temp%** do usuário da instalação.
