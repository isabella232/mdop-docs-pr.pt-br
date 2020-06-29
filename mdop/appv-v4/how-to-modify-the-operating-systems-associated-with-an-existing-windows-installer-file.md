---
title: Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer
description: Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797028"
---
# Como modificar os sistemas operacionais associados a um arquivo existente do Windows Installer


Use o procedimento a seguir para modificar as versões do sistema operacional associadas a um arquivo existente do Windows Installer (**MSI**) que foi criado usando o sequenciador App-V.

**Para modificar os sistemas operacionais de um arquivo existente do Windows Installer**

1.  Instale o sequenciador do App-V em um computador em seu ambiente que tenha somente o sistema operacional instalado. Você também pode instalar o sequenciador em um computador que executa um ambiente virtual, por exemplo, Microsoft Virtual PC. Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que você pode reutilizar com uma configuração adicional mínima. Para obter mais informações sobre como instalar o App-V Sequencer, consulte [como instalar o sequenciador](how-to-install-the-sequencer.md).

2.  Copie todo o pacote de aplicativo virtual que contém o arquivo do Windows Installer que você deseja modificar para o computador que executa o sequenciador.

3.  Para modificar o arquivo do Windows Installer, abra o console do sequenciador, selecione **pacote**  /  **aberto**e, em seguida, navegue até o local onde o pacote do aplicativo virtual associado ao arquivo do Windows Installer foi salvo.

4.  Para adicionar ou remover sistemas operacionais, selecione a guia **implantação** no console do sequenciador. Para especificar sistemas operacionais adicionais que serão associados ao arquivo do Windows Installer, selecione o sistema operacional desejado e, em seguida, clique na seta que aponta para o controle de lista do sistema operacional **selecionado** .

    Para remover uma associação de sistema operacional, selecione o sistema operacional que você deseja remover e, em seguida, clique na seta que aponta para o controle de lista do sistema operacional **disponível** .

5.  Para criar um novo Windows Installer que será associado ao pacote de aplicativo virtual, selecione **gerar pacote do Microsoft Windows Installer (MSI)**. Você também pode selecionar **ferramentas**  /  **Create MSI**.

    **Observação**  Se você selecionar **ferramentas** / , **criar MSI** para criar um novo arquivo do Windows Installer, ignore a **etapa 6** deste procedimento.

     

6.  Para salvar o pacote de aplicativo virtual, **Package**selecione  /  **salvar**pacote.

## Tópicos relacionados


[Tarefas para o Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





