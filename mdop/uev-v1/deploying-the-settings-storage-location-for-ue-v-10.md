---
title: Implantação da localização do armazenamento de configurações para a UE-V 1.0
description: Implantação da localização do armazenamento de configurações para a UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799912"
---
# Implantação da localização do armazenamento de configurações para a UE-V 1.0


A implantação do Microsoft User Experience Virtualization (UE-V Virtualization) requer um local de armazenamento de configurações onde as configurações do usuário estão armazenadas em um arquivo de pacote de configurações. O local de armazenamento de configurações pode ser configurado de uma destas duas maneiras:

-   **Active Directory Home Directory** – se um diretório base for definido para o usuário no Active Directory, o UE-V Agent usará esse local para armazenar pacotes de local de configurações. O UE-V Agent cria dinamicamente a pasta de armazenamento específica do usuário abaixo da raiz do diretório base. O agente só usará o diretório base do Active Directory se um local de armazenamento de configurações não estiver definido.

-   **Criar um compartilhamento de armazenamento de configurações** – o compartilhamento de armazenamento de configurações é um compartilhamento de rede padrão acessível a usuários do UE-V.

## Implantar um compartilhamento de armazenamento de configurações de UE-V


Ao criar o compartilhamento de armazenamento de configurações, você deve limitar o acesso somente aos usuários que precisam de acesso. As permissões necessárias são mostradas nas tabelas abaixo.

**Para implantar o compartilhamento de rede UE-V**

1.  Crie um novo grupo de segurança para usuários do UE-V.

2.  Crie uma nova pasta no computador centralizado que armazenará os pacotes de configurações do UE-V e conceda os usuários do UE-V com permissões de grupo para a pasta. O administrador que suporta UE-V precisará de permissões para essa pasta compartilhada.

3.  Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta de local de armazenamento de configuração:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
    <td align="left"><p>Controle total</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Defina as seguintes permissões de NTFS para a pasta de local de armazenamento de configurações:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    <th align="left"><strong>Pasta</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Criador/proprietário</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Somente subpastas e arquivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
    <td align="left"><p>Listar pasta/ler dados, criar pastas/acrescentar dados</p></td>
    <td align="left"><p>Somente esta pasta</p></td>
    </tr>
    </tbody>
    </table>

     

5.  Clique em **OK** para fechar as caixas de diálogo.

Esta configuração de permissão permite que os usuários criem pastas para armazenamento de configurações. O UE-V Agent cria e protege uma `settingspackage` pasta durante a execução no contexto do usuário. O usuário recebe controle total para a `settingspackage` pasta. Outros usuários não herdam o acesso a essa pasta. Você não precisa criar e proteger diretórios de usuário individuais, pois isso será feito automaticamente pelo agente que é executado no contexto do usuário.

**Observação**  É possível configurar mais segurança quando um Windows Server é utilizado para o compartilhamento de armazenamento de configurações. O UE-V pode ser configurado para verificar se o grupo do administrador local ou o usuário atual é o proprietário da pasta na qual os pacotes de configurações são armazenados. Para habilitar a segurança adicional, conclua o seguinte:

1.  Adicione uma chave do registro **reg \ _DWORD** chamada "RepositoryOwnerCheckEnabled" ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**

2.  Defina o valor da chave do registro como 1.

 

## Tópicos relacionados


[Implantação da UE-V 1.0](deploying-ue-v-10.md)

[Configurações com suporte para a UE-V 1.0](supported-configurations-for-ue-v-10.md)

Implantar o armazenamento central para configurações de virtualização de experiência do usuário modelos de configurações e pacotes [de configurações instalando o UE-V Generator](installing-the-ue-v-generator.md)

[Implantação do agente da UE-V](deploying-the-ue-v-agent.md)

 

 





