---
title: Notas de versão do App-V 4.6 SP1
description: Notas de versão do App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797605"
---
# Notas de versão do App-V 4.6 SP1


Para pesquisar essas notas de versão, pressione CTRL + F.

**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization (App-V). Estas notas da versão contêm informações que ajudam você a instalar com êxito o Application Virtualization (App-V) 4.6 SP1. Este documento contém informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do App-V, a alteração mais recente deve ser considerada autorizada.

 

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte o [site de segurança da Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conhecidos com o Application Virtualization 4.6 SP1


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.6 SP1. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Quando isso for possível, esses problemas serão resolvidos em versões posteriores.

### O caminho de SPRT será perdido se não terminar na barra (/)

Quando o caminho em HREF em um modelo de projeto não termina com uma barra ( **/** ), o href gerado não inclui o caminho. Isso ocorre quando o usuário manipula manualmente o arquivo **. SPRT** . Se você usar o sequenciador, ele sempre adiciona a barra diagonal ( **/** ) após o caminho.

SOLUÇÃO alternativa certifique-se de que o HREF tenha uma barra de avanço ( **/** ).

### Nome da pasta do usuário não corresponde ao nome do pacote

As pastas que contêm arquivos. pkg global e de usuário não incluem mais o nome do pacote. Anteriormente, o cliente App-V usado para usar a pasta raiz do pacote 8,3 nome curto como parte do nome da pasta. Isso permite que você o identifique facilmente. Ao usar o sequenciador do App-V 4,6 SP1, a pasta raiz do pacote 8,3 nomes curtos agora são cadeias de caracteres aleatórias. Isso torna difícil identificar as pastas que contêm os arquivos **. pkg** do pacote no computador que está executando o cliente App-V.

SOLUÇÃO alternativa use um dos seguintes métodos para identificar mais facilmente essas pastas do pacote:

1.  Ao criar o pacote usando o sequenciador, especifique um nome de pasta que siga a Convenção de nomenclatura do 8,3 para a pasta de aplicativo principal. Esse nome será usado como parte do nome da pasta do usuário como era o caso no App-V 4,6.

2.  O arquivo. sprj agora contém uma marca que exibe a cadeia de caracteres que é usada como o início do nome da pasta do usuário. Você pode usar o elemento **ShortName** do elemento **PACKAGEROOTFOLDER** para determinar o nome.

### Executando o App-V 4,6 SP1 em computadores com mais de 64 processadores

Quando você executa o App-V 4,6 SP1 em computadores com mais de 64 processadores instalados, o cliente App-V falha.

SOLUÇÃO alternativa nenhum. Não há suporte para essa configuração. Você deve executar o App-V 4,6 SP1on computadores com menos de 64 processadores.

### A atualização do Application Virtualization 4,6 SP1 não é oferecida em todas as localidades que usam o Microsoft Update

Quando você usa o Microsoft Update, a atualização do App-V 4,6 SP1 não está disponível para as seguintes localidades de idioma:

-   Cazaque

-   Híndi

-   Sérvio-cirílico

SOLUÇÃO alternativa se você estiver usando o Microsoft Windows Server Update Services (WSUS), use a versão em inglês da atualização ou baixe a atualização do catálogo do Microsoft Update.

### Após expandir o pacote pai, você não pode sequenciar um plug-in com componentes lado a lado

Quando você expande um pacote pai usando **ferramentas**  /  **expandir pacote para o sistema local** no console do App-V Sequencer e sequenciar um plug-in com componentes lado a lado, um erro de instalação é retornado. Por exemplo:

-   **HRESULT 0x80073712**

Isso ocorre quando o sequenciador grava o componente lado a lado no registro, mas não limpa o valor da seguinte chave do registro:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

SOLUÇÃO alternativa após expandir o pacote pai no computador que está executando o sequenciador, você precisa excluir o valor da seguinte chave do registro:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

Depois de excluir o valor, Sequence o plug-in.

### Informações de direitos autorais da versão

Este documento é fornecido "como está". As informações e os modos de exibição expressos neste documento, como URLs e outras referências de site da Internet, podem mudar sem aviso prévio. Você assume o risco de usá-lo.

Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios. Nenhuma associação ou conexão real é intencional ou deve ser inferida.

Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft. Você pode copiar e usar este documento para fins de referência interna. Você pode modificar esse documento para suas finalidades de referência internas.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.

Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.

 

 





