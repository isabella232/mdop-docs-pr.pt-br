---
title: Considerações de segurança do UE-V 1.0
description: Considerações de segurança do UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799384"
---
# Considerações de segurança do UE-V 1.0


Este tópico contém uma breve visão geral de contas e grupos, arquivos de log e outras considerações relacionadas à segurança para o Microsoft User Experience Virtualization (UE-V). Para obter mais informações, siga os links que são fornecidos aqui.

## Considerações de segurança para a configuração de UE-V


**Ao criar o compartilhamento de armazenamento configurações, limite o acesso de compartilhamento aos usuários que precisam de acesso.**

Como os pacotes de configurações podem conter informações pessoais, você deve ter cuidado para protegê-los assim que possível. Em geral, faça o seguinte:

-   Restrinja o compartilhamento apenas aos usuários que precisam de acesso. Crie um grupo de segurança para usuários que tenham pastas redirecionadas em um determinado compartilhamento e limite o acesso somente a esses usuários.

-   Ao criar o compartilhamento, oculte o compartilhamento colocando $ após o nome do compartilhamento. Isso ocultará o compartilhamento de navegadores casuais, e o compartilhamento não será visível em meus locais de rede.

-   Forneça aos usuários a quantidade mínima de permissões necessárias. As permissões necessárias são mostradas nas tabelas abaixo.

    1.  Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta de local de armazenamento de configuração:

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">Conta de usuário</th>
        <th align="left">Permissões recomendadas</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Todos</p></td>
        <td align="left"><p>Nenhuma permissão</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de segurança da UE-V</p></td>
        <td align="left"><p>Controle total</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Usar servidores Windows Server 2003 ou posteriores para hospedar compartilhamentos de arquivos redirecionados

Os arquivos de pacote de configurações do usuário contêm informações pessoais que são transferidas entre o computador cliente e o servidor que armazena os pacotes de configurações. Por isso, você deve garantir que os dados sejam protegidos enquanto trafegam pela rede.

Os dados das configurações do usuário são vulneráveis a essas possíveis ameaças: a interceptação dos dados durante a transmissão pela rede; adulteração dos dados durante a transmissão pela rede; e falsificação do servidor que hospeda os dados.

Vários recursos do Windows Server 2003 e versões mais recentes podem ajudar a proteger os dados do usuário:

-   **Kerberos** -Kerberos é padrão em todas as versões do Windows 2000 e windows Server 2003 e posterior. O Kerberos garante o mais alto nível de segurança aos recursos de rede. O NTLM autentica somente o cliente; O Kerberos autentica o servidor e o cliente. Quando o NTLM for usado, o cliente não saberá se o servidor é válido. Isso é particularmente importante se o cliente estiver trocando arquivos pessoais com o servidor, como é o caso dos perfis de roaming. O Kerberos oferece melhor segurança do que o NTLM. O Kerberos não está disponível no Windows NT versão 4,0 ou sistemas operacionais anteriores.

-   **IPSec** – o IP Security Protocol (IPSec) oferece autenticação, integridade e criptografia de dados no nível da rede. O IPsec garante o seguinte:

    -   Os dados em roaming são seguros da modificação de dados durante a rota.

    -   Os dados em roaming estão protegidos contra interceptação, visualização ou cópia.

    -   Os dados em roaming são seguros de serem acessados por partes não autenticadas.

-   **Assinatura SMB** – o protocolo de autenticação SMB (Server Message Block) dá suporte à autenticação de mensagens que impede ataques de mensagem ativa e "Man-in-the-middle". A assinatura SMB fornece essa autenticação colocando uma assinatura digital em cada SMB. A assinatura digital é então verificada pelo cliente e pelo servidor. Para usar a assinatura SMB, primeiro você deve habilitá-la ou exigi-la no cliente SMB e no servidor SMB. Observe que a assinatura SMB impõe uma penalidade de desempenho. Ele não consome mais largura de banda de rede, mas usa mais ciclos de CPU no lado do cliente e do servidor.

### Sempre usar o sistema de arquivos NTFS para volumes que contêm dados de usuários

Para a configuração mais segura, configure os servidores que hospedam os arquivos de configurações do UE-V para usar o sistema de arquivos NTFS. Diferentemente do FAT, o NTFS dá suporte a listas de controle de acesso discricional (DACLs) e listas de controle de acesso do sistema (SACLs). As DACLs e SACLs controlam quem pode realizar operações em um arquivo e quais eventos dispararão o log de ações executadas em um arquivo.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>Não confie no EFS para criptografar os arquivos dos usuários quando transmitidos pela rede

Quando você usa o sistema de arquivos com criptografia (EFS) para criptografar arquivos em um servidor remoto, os dados criptografados não são criptografados durante o trânsito pela rede; Ele só se torna criptografado quando armazenado em disco.

As exceções a isso são quando o sistema inclui segurança de protocolo Internet (IPsec) ou criação e controle de versão distribuídas (WebDAV). O IPsec criptografa dados enquanto eles são transportados por uma rede TCP/IP. Se o arquivo for criptografado antes de ser copiado ou movido para uma pasta WebDAV em um servidor, ele permanecerá criptografado durante a transmissão e enquanto estiver armazenado no servidor.

### Criptografar o cache de arquivos offline

Por padrão, o cache de arquivos offline é protegido em partições NTFS por ACLs, mas a criptografia do cache melhora ainda mais a segurança em um computador local. Por padrão, o cache no computador local não é criptografado, portanto, os arquivos criptografados armazenados em cache da rede não serão criptografados no computador local. Isso pode representar um risco de segurança em alguns ambientes.

Quando a criptografia está habilitada, todos os arquivos no cache de arquivos offline são criptografados. Isso inclui a criptografia de arquivos existentes, bem como os arquivos que são adicionados mais tarde. A cópia em cache no computador local é afetada, mas a cópia de rede associada não está.

O cache pode ser criptografado de uma destas duas maneiras:

1.  Por meio da política de grupo. -Habilite a configuração **criptografar o cache de arquivos offline** , localizada em arquivos do computador Configuration\\Administrative Templates\\Network\\Offline, no editor de política de grupo.

2.  Manualmente. -Selecione Ferramentas e, em seguida, clique em opções de pasta no menu de comando do Windows Explorer. Selecione a guia arquivos offline e, em seguida, marque a caixa de seleção **criptografar arquivos offline para proteger os dados** .

### Permitir que o UE-V Agent Crie pastas para cada usuário

Para garantir que o UE-V funcione de maneira ideal, crie somente o compartilhamento de raiz no servidor e deixe que o UE-V Agent crie as pastas para cada usuário. O UE-V criará essas pastas de usuário com a segurança adequada.

Esta configuração de permissão permite que os usuários criem pastas para armazenamento de configurações. O UE-V Agent cria e protege uma pasta settingspackage durante a execução no contexto do usuário. O usuário recebe controle total para a pasta settingspackage. Outros usuários não herdam o acesso a essa pasta. Você não precisa criar e proteger diretórios de usuário individuais. Isso será feito automaticamente pelo agente que é executado no contexto do usuário.

**Observação**  
É possível configurar mais segurança quando um Windows Server é utilizado para o compartilhamento de armazenamento de configurações. O UE-V pode ser configurado para verificar se o grupo do administrador local ou o usuário atual é o proprietário da pasta na qual os pacotes de configurações são armazenados. Para habilitar a segurança adicional, use o seguinte comando:

1.  Adicione uma chave do registro REG \ _DWORD chamada "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Defina o valor da chave do registro como 1.

Quando essa configuração está implementada, o UE-V Agent verifica se o grupo do administrador local ou o usuário atual é o proprietário da pasta settingspackage. Se não for, o UE-V Agent não permitirá acesso à pasta.



Se você deve criar pastas para os usuários e garantir que você tenha as permissões corretas definidas.

É altamente recomendável que você não crie pastas e, em vez disso, permita que o UE-V Agent crie a pasta para o usuário.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>Garantir que as permissões corretas sejam definidas ao armazenar as configurações de UE-V no diretório base de um usuário

Se você redirecionar as configurações do UE-V para o diretório base de um usuário, certifique-se de que as permissões no diretório base do usuário sejam definidas apropriadamente para a sua organização.

## Tópicos relacionados


[Segurança e privacidade do UE-V 1.0](security-and-privacy-for-ue-v-10.md)









