---
title: Notas de versão do App-V 5.0
description: Notas de versão do App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796220"
---
# Notas de versão do App-V 5.0


**Para procurar um problema específico nestas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o App-V 5,0.

Estas notas da versão contêm informações necessárias para instalar com êxito o App-V 5,0. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do App-V 5,0, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Sobre a documentação do produto


Para obter informações sobre a documentação do App-V 5,0, consulte a home page do App-V 5,0 no Microsoft TechNet.

## Fornecer comentários


Estamos interessados em seus comentários sobre o App-V 5,0. Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .

**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras na nossa documentação e nas versões do produto.

 

Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conhecidos com o App-V 5,0


Esta seção contém notas de versão sobre os problemas conhecidos com o App-V 5,0.

### Não é possível terminar de adicionar pacotes ao usar cmdlets do PowerShell do servidor

Quando você adiciona um pacote usando o PowerShell, não há nenhum método para sair da adição de novos pacotes.

SOLUÇÃO alternativa: para parar de adicionar pacotes, pressione **Enter** depois de adicionar o pacote final.

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> App-V 5,0 o cliente rejeita pacotes de servidores cujo certificado SSL foi revogado

Ao usar o protocolo HTTPS, o cliente App-V 5,0, por padrão, rejeitará pacotes de servidores cujo certificado SSL foi revogado. Esse comportamento pode ser desativado por meio da configuração modificando a configuração **VerifyCertificateRevocationList** . A aplicação de uma nova configuração para essa configuração não entrará em vigor até que o serviço App-V 5,0 seja reiniciado.

SOLUÇÃO alternativa: reinicie o serviço App-V 5,0.

## Informações de direitos autorais da versão


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft. Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.








## Tópicos relacionados


[Sobre o App-V 5.0](about-app-v-50.md)

 

 





