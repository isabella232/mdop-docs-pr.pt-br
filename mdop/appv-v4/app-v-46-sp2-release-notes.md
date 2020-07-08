---
title: Notas de versão do App-V 4.6 SP2
description: Notas de versão do App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799053"
---
# Notas de versão do App-V 4.6 SP2


**Para pesquisar essas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Application Virtualization (App-V) 4.6 SP2.

Estas notas da versão contêm informações necessárias para instalar com êxito o Application Virtualization 4,6 SP2. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do App-V 4.6 SP2, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Sobre a documentação do produto


Para obter mais informações sobre a documentação do App-V, consulte a página de [virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=232982) no Microsoft TechNet.

## Fornecendo comentários


Estamos interessados em seus comentários sobre o App-V 4.6 SP2. Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .

**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar mudanças futuras para nossa documentação e versões de produtos.

 

Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>Problemas conhecidos com o App-V 4.6 SP2


### O suporte curto a nomes de arquivo está desabilitado para unidades físicas não pertencentes ao sistema durante a sequência

Quando você sequencia no Windows 8 ou no Windows Server 2012, o suporte para nomes de arquivo curtos (8,3) é desabilitado por padrão para unidades físicas que não sejam do sistema.

A unidade física subjacente associada ao diretório de aplicativos virtual primário (por exemplo, "Q:\\appname") na estação de sequenciamento deve fornecer suporte a curto (8,3) para o aplicativo do App-V 4.6 SP2 gerar nomes de arquivo curtos ao criar pacotes de aplicativos virtuais. O suporte ao nome do arquivo curto (8,3) é desabilitado por padrão para unidades físicas que não são do sistema no Windows 8 ou no Windows Server 2012.

**Solução alternativa:** Habilite o suporte a curto File Name (8,3) em unidades físicas não pertencentes ao sistema. Você pode usar o comando a seguir para habilitar o suporte curto a nomes de arquivo no Windows 8 ou no Windows Server 2012.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

Por exemplo, use o seguinte comando se a letra da unidade for "p:":

``` syntax
fsutil 8dot3name set Q: 0
```

**Observação**  Você não precisa alterar essa configuração no cliente App-V porque o sistema de arquivos App-V manipula corretamente caminhos curtos no Windows 8 ou no Windows Server 2012.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> O App-V não substitui o manipulador padrão do tipo de arquivo ou associações de protocolo no Windows 8

Se você selecionar um aplicativo padrão usando **programas padrão** no **painel de controle** no Windows 8, o App-V não substituirá as associações de tipo de arquivo associadas a esse aplicativo.

**Solução alternativa:** Nenhuma.

### O Outlook 2010 virtualizado não é oferecido como uma opção para links do mailto clicáveis no Windows 8

A extensão do mailto para Shell não oferece o Outlook 2010 virtualizado no Windows 8. Por exemplo, se você clicar em um link mailto: do Outlook virtualizado do Outlook 2010 que está em execução no Windows 8, uma nova janela de email não será criada. Esta opção funciona corretamente no Windows 7 e em versões anteriores do sistema operacional Windows.

**Solução alternativa:** Nenhuma.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> A atualização do Application Virtualization 4,6 SP2 não é oferecida em todas as localidades que usam o Microsoft Update

Quando você usa o Microsoft Update, a atualização do App-V 4.6 SP2 não está disponível para as seguintes localidades de idioma:

-   Cazaque

-   Híndi

-   Sérvio-cirílico

**Solução alternativa:** Se você estiver usando o Microsoft Windows Server Update Services (WSUS), use a versão em inglês da atualização ou baixe a atualização do catálogo do Microsoft Update.

## Informações de direitos autorais da versão


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft. Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.



## Tópicos relacionados


[Sobre o Microsoft Application Virtualization 4.6 SP2](about-microsoft-application-virtualization-46-sp2.md)

 

 





