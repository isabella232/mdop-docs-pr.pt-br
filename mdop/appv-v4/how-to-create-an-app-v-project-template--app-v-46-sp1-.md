---
title: Como criar um modelo de projeto App-V (App-V 4.6 SP1)
description: Como criar um modelo de projeto App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797167"
---
# Como criar um modelo de projeto App-V (App-V 4.6 SP1)


Você pode usar um modelo de projeto App-V para salvar configurações comumente aplicadas associadas a um pacote de aplicativo virtual existente. Essas configurações podem ser aplicadas quando você cria novos pacotes de aplicativo virtual em seu ambiente que podem ajudar a simplificar o processo de criação de pacotes de aplicativos virtuais.

**Observação**  Você só pode aplicar um modelo de projeto App-V ao criar um novo pacote de aplicativo virtual. Não há suporte para a aplicação de modelos de projeto a pacotes de aplicativos virtuais existentes.

 

Para obter mais informações sobre como aplicar um modelo de projeto App-V, consulte [como aplicar um modelo de projeto App-v (App-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).

Os modelos de projetos do App-V diferem dos aceleradores de aplicativos do App-v porque os aceleradores de aplicativo do App-V são específicos do aplicativo, e os modelos de projeto do App-V podem ser aplicados a vários aplicativos. Além disso, você não pode usar um modelo de projeto quando usa um acelerador de pacote para criar um pacote de aplicativo virtual.

As seguintes configurações gerais são salvas com um modelo de projeto App-V:

-   **Opções avançadas de monitoramento**. Permite que o Microsoft Update seja executado durante o monitoramento, a troca **de base. dll**.

-   **Configurações de implantação do pacote**. Contém **protocolo**, **nome do host**, **porta**, **caminho**, **sistemas operacionais**, **impor descritores de segurança**, **criar MSI**, **compactar pacote**.

-   **Opções gerais**. Permite gerar pacote **MSI (Microsoft Windows Installer)** , permitir a **virtualização de eventos**, **permitir a virtualização de serviços**, **acrescentar a versão do pacote ao nome do arquivo**.

-   **Itens de exclusão**. Contém a lista de padrões de exclusão.

**Para criar um modelo de projeto**

1.  Para iniciar o sequenciador do App-v, no computador que está executando o sequenciador do App-v, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer**Virtualization.

2.  Se o pacote de aplicativo virtual estiver aberto no momento no sequenciador App-V, pule para a etapa 3 deste procedimento. Para abrir o pacote de aplicativo virtual existente que contém as configurações que você deseja salvar com o modelo de projeto App-V, clique em **arquivo**  /  **abrir** e clique em **Editar** **pacote**. Na página **selecionar pacote** , clique em **procurar** e localize o pacote de aplicativo virtual que você deseja abrir. Clique em **Editar**.

3.  No console do App-V Sequencer, clique em **arquivo**  /  **salvar como modelo**. Depois de revisar as configurações que serão salvas com o novo modelo, clique em **OK**. Especifique um nome que será associado ao novo modelo de projeto do App-V. Clique em **Salvar**.

    O novo modelo de projeto do App-V é salvo no diretório especificado na etapa 3 deste procedimento.

## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Como aplicar um modelo de projeto do App-V (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





