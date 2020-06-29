---
title: Considerações sobre segurança para a UE-V 2.x
description: Considerações sobre segurança para a UE-V 2.x
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799517"
---
# Considerações sobre segurança para a UE-V 2.x


Este tópico contém uma breve visão geral de contas e grupos, arquivos de log e outras considerações relacionadas à segurança para o Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1. Para obter mais informações, siga os links que são fornecidos aqui.

## Considerações de segurança para a configuração de UE-V


**Importante**  Ao criar o compartilhamento de armazenamento configurações, limite o acesso de compartilhamento aos usuários que precisam de acesso.

 

Como os pacotes de configurações podem conter informações pessoais, você deve ter cuidado para protegê-los assim que possível. Em geral, faça o seguinte:

-   Restrinja o compartilhamento apenas aos usuários que precisam de acesso. Crie um grupo de segurança para os usuários que tenham pastas redirecionadas em um compartilhamento específico e limite o acesso a apenas esses usuários.

-   Ao criar o compartilhamento, oculte o compartilhamento colocando $ após o nome do compartilhamento. Essa adição oculta o compartilhamento de navegadores casuais, e o compartilhamento não fica visível em meus locais de rede.

-   Forneça aos usuários a quantidade mínima de permissões que eles devem ter. As tabelas a seguir mostram as permissões necessárias.

    1.  Defina as seguintes permissões do SMB em nível de compartilhamento para a pasta de local de armazenamento de configuração.

        | Conta de usuário | Permissões recomendadas |
        | - | - |
        | Todos | Nenhuma permissão |
        |Grupo de segurança da UE-V | Controle total |

    2.  Defina as seguintes permissões do sistema de arquivos NTFS para a pasta de local de armazenamento de configurações.

        | Conta de usuário | Permissões recomendadas | Pasta |
        | - | - | - |
        | Criador/proprietário | Controle total | Somente subpastas e arquivos|
        | Administradores de domínio | Controle total | Esta pasta, subpastas e arquivos |
        | Grupo de segurança de usuários do UE-V | Listar pasta/ler dados, criar pastas/acrescentar dados | Somente esta pasta |
        | Todos | Remover todas as permissões | Nenhuma permissão |

    3.  Defina as seguintes permissões do SMB em nível de compartilhamento para a pasta catálogo de modelos de configurações.

        | Conta de usuário | Permissões recomendadas |
        | - | - |
        | Todos | Nenhuma permissão |
        | Computadores do domínio | Ler níveis de permissão |
        | Administradores | Níveis de permissão de leitura/gravação |
         
    4.  Defina as seguintes permissões de NTFS para a pasta catálogo de modelos de configurações.

        | Conta de usuário | Permissões recomendadas | Aplicar a |
        | - | - | - |
        | Criador/proprietário | Controle total | Esta pasta, subpastas e arquivos |
        | Computadores do domínio | Listar o conteúdo e as permissões de leitura da pasta | Esta pasta, subpastas e arquivos|
        | Todos| Nenhuma permissão| Nenhuma permissão|
        | Administradores| Controle total| Esta pasta, subpastas e arquivos|

### Usar o WindowsServer a partir do WindowsServer2003 para hospedar compartilhamentos de arquivos redirecionados

Os arquivos de pacote de configurações do usuário contêm informações pessoais que são transferidas entre o computador cliente e o servidor que armazena os pacotes de configurações. Devido a esse processo, você deve garantir que os dados sejam protegidos enquanto trafegam pela rede.

Os dados de configurações do usuário são vulneráveis a essas possíveis ameaças: a interceptação dos dados durante a transmissão pela rede, a violação dos dados durante a transmissão pela rede e a falsificação do servidor que hospeda os dados.

A partir do Windows Server2003, vários recursos do sistema operacional Windows Server podem ajudar a proteger os dados do usuário:

-   **Kerberos** – Kerberos é padrão em todas as versões do Microsoft Windows2000Server e WindowsServer começando com windowsserver2003. O Kerberos garante o mais alto nível de segurança aos recursos de rede. O NTLM autentica somente o cliente; O Kerberos autentica o servidor e o cliente. Quando o NTLM for usado, o cliente não saberá se o servidor é válido. Essa diferença é especialmente importante se o cliente troca arquivos pessoais com o servidor, como é o caso com perfis de usuário móvel. O Kerberos oferece melhor segurança do que o NTLM. O Kerberos não está disponível no Microsoft WindowsNTServer 4,0 ou em sistemas operacionais anteriores.

-   **IPSec** – o IP Security Protocol (IPSec) oferece autenticação, integridade e criptografia de dados no nível da rede. O IPsec garante o seguinte:

    -   Os dados em roaming são seguros da modificação de dados enquanto os dados são direcionados para o caminho.

    -   Os dados em roaming estão protegidos contra interceptação, visualização ou cópia.

    -   Os dados em roaming são seguros do acesso por partes não autenticadas.

-   **Assinatura SMB** – o protocolo de autenticação SMB (Server Message Block) dá suporte à autenticação de mensagens, que impede ataques de mensagem ativa e "Man-in-the-middle". A assinatura SMB fornece essa autenticação colocando uma assinatura digital em cada SMB. A assinatura digital é então verificada pelo cliente e pelo servidor. Para usar a assinatura SMB, primeiro você deve habilitá-la, ou precisará exigi-la no cliente SMB e no servidor SMB. Observe que a assinatura SMB impõe uma penalidade de desempenho. Ele não consome mais largura de banda de rede, mas usa mais ciclos de CPU no lado do cliente e do servidor.

### Sempre usar o sistema de arquivos NTFS para volumes que armazenam dados do usuário

Para a configuração mais segura, configure os servidores que hospedam os arquivos de configurações do UE-V para usar o sistema de arquivos NTFS. Ao contrário do sistema de arquivos FAT, o NTFS dá suporte a listas de controle de acesso discricional (DACLs) e às SACLs (listas de controle de acesso do sistema). As DACLs e SACLs controlam quem pode realizar operações em um arquivo e quais eventos disparam o log de ações executadas em um arquivo.

### Não confie no EFS para criptografar arquivos de usuários quando eles forem transmitidos pela rede

Quando você usa o sistema de arquivos com criptografia (EFS) para criptografar arquivos em um servidor remoto, os dados criptografados não são criptografados durante o trânsito pela rede; Ele só se torna criptografado quando está armazenado em disco.

Este processo de criptografia não se aplica quando o sistema inclui segurança de protocolo Internet (IPsec) ou criação e controle de versão distribuídas (WebDAV). O IPsec criptografa dados enquanto eles são transportados por uma rede TCP/IP. Se o arquivo for criptografado antes de ser copiado ou movido para uma pasta WebDAV em um servidor, ele permanecerá criptografado durante a transmissão e enquanto estiver armazenado no servidor.

### Permitir que o UE-V Agent Crie pastas para cada usuário

Para garantir que o UE-V funcione de maneira ideal, crie somente o compartilhamento de raiz no servidor e deixe que o UE-V Agent crie as pastas para cada usuário. O UE-V cria essas pastas de usuário com a segurança adequada.

Esta configuração de permissão permite que os usuários criem pastas para armazenamento de configurações. O UE-V Agent cria e protege uma pasta de pacote de configurações enquanto é executado no contexto do usuário. Os usuários recebem controle total da pasta de pacotes de configurações. Outros usuários não herdam o acesso a essa pasta. Você não precisa criar e proteger diretórios de usuário individuais. O agente que é executado no contexto do usuário faz isso automaticamente.

**Observação**  A segurança adicional pode ser configurada quando um servidor Windows for usado para o compartilhamento de armazenamento de configurações. O UE-V pode ser configurado para verificar se o grupo Administradores local ou o usuário atual é o proprietário da pasta em que os pacotes de configurações estão armazenados. Para habilitar a segurança adicional, use o seguinte comando:

1.  Adicione a chave de registro \ _DWORD do RepositoryOwnerCheckEnabled a `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Defina o valor da chave do registro como *1*.

Quando essa configuração está implementada, o UE-V Agent verifica se o grupo Administradores local ou o usuário atual é o proprietário da pasta de pacotes configurações. Caso contrário, o UE-V Agent não concederá acesso à pasta.

 

Se você precisar criar pastas para os usuários, certifique-se de ter as permissões corretas definidas.

É altamente recomendável que você não crie pastas previamente. Em vez disso, deixe que o UE-V Agent crie a pasta para o usuário.

### Verifique as permissões corretas para armazenar as configurações do UE-V 2 em um diretório base ou diretório personalizado

Se você redirecionar as configurações do UE-V para o diretório base de um usuário ou um diretório personalizado do Active Directory (AD), certifique-se de que as permissões no diretório sejam definidas apropriadamente para a sua organização.






## Tópicos relacionados


[Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





