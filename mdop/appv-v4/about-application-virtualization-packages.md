---
title: Sobre pacotes do Application Virtualization
description: Sobre pacotes do Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797654"
---
# Sobre pacotes do Application Virtualization


Na virtualização do aplicativo, um *pacote* é a saída do processo de sequenciamento. Use pacotes ao implantar aplicativos em seus servidores pela primeira vez e quando atualizar aplicativos com uma nova versão. Os pacotes permitem que você controle as versões do aplicativo virtual em seus servidores de gerenciamento do Application Virtualization. Um único pacote pode conter um ou mais aplicativos. Cada pacote de aplicativo contém um conjunto de arquivos como uma unidade autônoma.

## Gerenciando pacotes


Depois que o sequenciador cria um pacote de um ou mais aplicativos como parte de seu processo, você pode copiar os arquivos gerados do sequenciador para um servidor de gerenciamento do Application Virtualization e disponibilizá-los para streaming.

Os pacotes disponíveis aparecem no contêiner **pacotes** no painel esquerdo do console de gerenciamento do Application Virtualization. Quando você importa um aplicativo com um arquivo de projeto de sequenciador (SPRJ) ou um arquivo Open Software Descriptor (OSD), uma entrada relacionada aparece no contêiner **pacotes** . No console de gerenciamento de servidor do Application Virtualization, você pode implantar, atualizar ou excluir pacotes e versões deles.

Cada aplicativo virtual tem um pacote associado. Este pacote inclui os seguintes arquivos:

-   SFT — o arquivo que transmite o aplicativo aos clientes.

-   OSD — o arquivo Open Software Descriptor contém as informações necessárias para localizar e iniciar o aplicativo.

-   ICO — o arquivo de ícone que representa visualmente o aplicativo em interfaces do usuário e atalhos.

-   SPRJ — o arquivo de projeto do sequenciador.

Quando você importa o arquivo SPRJ, todos os aplicativos sequenciados estão disponíveis para implantação, por padrão, mas os aplicativos não estão habilitados para streaming. Você pode optar por transmitir todos ou alguns dos aplicativos no pacote. Por exemplo, se você tiver sequenciado e importado o Microsoft Office, poderá optar por não implantar alguns aplicativos, como o assistente para salvar minhas configurações. Nesse caso, clique com o botão direito do mouse em cada aplicativo que você deseja implantar, escolha **Propriedades**e verifique se a caixa **habilitado** está desmarcada (em branco). Somente os aplicativos com a caixa **habilitado** selecionada serão transmitidos para os computadores cliente.

Depois de resequenciar um pacote e produzir um novo arquivo SFT para streaming, você pode atualizar o pacote antigo com rapidez e facilidade por meio do console de gerenciamento do servidor do Application Virtualization.

O único cenário operacional que requer o uso do nó **pacotes** é quando você introduz uma nova versão (arquivo SFT) para o pacote. Sempre que você importa aplicativos, atribui acesso e licenças para aplicativos e assim por diante, o sistema do Application Virtualization acompanha essas informações no nível do pacote. Isso significa que, quando você autoriza um usuário a usar um aplicativo, está fornecendo permissão ao usuário para executar qualquer aplicativo no mesmo pacote.

### Versão do pacote

Uma versão do pacote é representada por um arquivo SFT específico. Quando você atualiza um pacote (aplica uma atualização a um aplicativo ou adiciona um aplicativo a um pacote), você gera um novo arquivo SFT. Toda vez que você cria um novo arquivo SFT, você está criando uma nova versão de pacote.

Quando você importa aplicativos por meio do console de gerenciamento do servidor do Application Virtualization, o software cria automaticamente um pacote e uma versão do pacote, se eles ainda não existirem.

## Tópicos relacionados


[Sobre aplicativos do Application Virtualization](about-application-virtualization-applications.md)

[Sobre o Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Como gerenciar pacotes no Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





