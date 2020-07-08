---
title: Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação
description: Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799169"
---
# Como usar o Assistente de Imagem de Recuperação do DaRT para criar a imagem de recuperação


O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui o **Assistente de imagem de recuperação do DART** que é usado no Windows para criar uma imagem ISO (organização internacional) inicializável (ISO). Uma imagem ISO é um arquivo que representa o conteúdo bruto de um CD.

O **Assistente de imagem de recuperação do DART** requer as seguintes informações:

-   **Imagem de inicialização**° °, você deve fornecer o caminho de um DVD do Windows 7 ou arquivos de origem do Windows 7 necessários para criar a imagem de recuperação do DART.

-   **Seleção**de ferramentas ° °, você pode selecionar as ferramentas a serem incluídas na imagem de recuperação do DART.

-   **Conexões remotas**° °, você pode selecionar se deseja que a imagem de recuperação do DART inclua a capacidade de estabelecer uma conexão remota entre o helpdesk e o computador do usuário final.

-   **Ferramentas de depuração para Windows**° °, você será solicitado a fornecer o local das ferramentas de depuração para Windows.

-   **Definições para sistema autônomo do sistema de limpeza do sistema**, você pode decidir entre baixar as definições mais recentes no momento em que cria a imagem de recuperação ou baixar as definições mais tarde.

-   **Drivers**° ° onde você será perguntado se deseja adicionar drivers à imagem ISO.

-   **Arquivos adicionais**° °, você pode adicionar arquivos à imagem ISO que podem ajudar a diagnosticar problemas.

-   **Local da imagem ISO**° °, você será solicitado a especificar onde a imagem ISO deve ser localizada.

-   **Unidade de CD/DVD**° °, você será solicitado a especificar se a unidade de CD ou DVD deve ser usada para gravar o CD ou DVD.

**Observação**  O tamanho da imagem ISO pode variar, dependendo das ferramentas que foram selecionadas no assistente de **imagem de recuperação do DART**.

 

## Para criar a imagem de recuperação usando o assistente de imagem de recuperação do DaRT


Siga estas instruções para usar o **Assistente de imagem de recuperação DART** para criar a imagem de recuperação do DART.

### Para selecionar as ferramentas a serem incluídas na imagem de recuperação do DaRT

O **Assistente de imagem de recuperação do DART** apresenta uma caixa de diálogo de **seleção de ferramenta** . Você pode selecionar ou remover as ferramentas da lista de ferramentas a serem incluídas na imagem de recuperação do DaRT, realçando uma ferramenta e clicando nos botões **habilitar** ou **desabilitar** .

Depois de selecionar todas as ferramentas que você deseja incluir na imagem de recuperação, clique em **Avançar**.

### Para adicionar a opção de permitir conectividade remota

Você pode marcar a caixa de seleção **permitir conexões remotas** para fornecer a opção na janela do **conjunto de ferramentas de diagnóstico e recuperação** para estabelecer uma conexão remota entre o agente da assistência técnica e um computador de usuário final. Depois que um agente de helpdesk estabelece uma conexão remota, ele pode executar as ferramentas DaRT no computador do usuário final a partir de um local remoto.

Você pode marcar a caixa de seleção **especificar o número da porta** para inserir um número de porta específico que será usado ao estabelecer uma conexão remota. Você pode especificar um número de porta entre 1 e 65535. Recomendamos que o número da porta seja 1024 ou superior para minimizar a possibilidade de um conflito.

Você também pode criar uma mensagem personalizada que será recebida por um usuário final quando ele estabelecer uma conexão remota. A mensagem pode ter no máximo 2048 caracteres.

Para obter mais informações sobre como executar remotamente as ferramentas DaRT, consulte [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

### Para adicionar as ferramentas de depuração para Windows à imagem de recuperação do DaRT

Na caixa de diálogo **analisador de falha** do **Assistente de imagem de recuperação DART**, você será solicitado a especificar o local das ferramentas de depuração para Windows. Se não tiver uma cópia das ferramentas, você poderá baixá-las da Microsoft. O link a seguir para a página de download é fornecido no assistente: [baixar e instalar as ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

Você pode especificar o local das ferramentas de depuração no computador no qual você está executando o **Assistente de imagem de recuperação DART**ou pode decidir usar as ferramentas localizadas no computador de destino. Se você decidir usar uma cópia em outro computador, deve verificar se as ferramentas estão instaladas em cada computador no qual você está diagnosticando uma falha.

**Observação**  Se você incluir o **Crash Analyzer** na imagem ISO, recomendamos que você também inclua as ferramentas de depuração para Windows.

 

Siga estas etapas para adicionar as ferramentas de depuração para Windows:

1.  Adicionais Clique no hiperlink para baixar as ferramentas de depuração para Windows.

2.  Selecione uma das seguintes opções:

    -   **Use as ferramentas de depuração para Windows no local a seguir**. Se você selecionar essa opção, poderá navegar até o local das ferramentas.

    -   **Localize as ferramentas de depuração para Windows no sistema que você está reparando**. Se você selecionar essa opção, o **Crash Analyzer** não funcionará se as ferramentas de depuração para Windows não forem encontradas no computador com problema.

3.  Depois de concluir, clique em **Avançar**.

### Para adicionar definições do standalone System Sweeper à imagem de recuperação do DaRT

As definições são um repositório de malware e outros softwares potencialmente indesejados conhecidos. Como o malware está sendo desenvolvido continuamente, o **standalone System Sweeper** depende das definições atuais para determinar se o software que está tentando instalar, executar ou alterar as configurações em um computador é um software potencialmente indesejado ou mal-intencionado.

Para incluir as definições mais recentes na imagem de recuperação do DaRT (recomendado), clique em **Sim, baixar as definições mais recentes.** A atualização de definição é iniciada automaticamente. Você deve estar conectado à Internet para concluir esse processo.

Para ignorar a atualização de definição, clique em **não, baixar manualmente as definições mais tarde**. As definições não serão incluídas na imagem de recuperação do DaRT.

Se você decidir não incluir as definições mais recentes na imagem de recuperação ou se as definições incluídas na imagem de recuperação não estiverem mais atualizadas na hora em que você está pronto para usar a **limpeza do sistema autônomo**, obtenha as definições mais recentes antes de iniciar uma verificação seguindo as instruções fornecidas na limpeza do **sistema autônomo**.

**Importante**  Não é possível verificar se não há definições.

 

Depois de concluir, clique em **Avançar**.

### Para adicionar drivers à imagem de recuperação do DaRT

**Cuidado**  Por padrão, quando você adiciona um driver à imagem de recuperação do DaRT, todos os arquivos e subpastas adicionais localizados nessa pasta são adicionados à imagem de recuperação. Para obter mais informações, consulte solução de problemas para o [DaRT 7,0](troubleshooting-dart-70-new-ia.md).

 

Você deve incluir drivers adicionais na imagem de recuperação do DaRT7 que pode ser necessário ao reparar um computador. Geralmente, eles podem incluir armazenamento ou controladores de rede que não estão incluídos no DVD do Windows.

**Importante**  Quando você selecionar os drivers a serem incluídos, lembre-se de que a conectividade sem fio (como Bluetooth ou 802.11 a/b/g/n) não é compatível com o DaRT.

 

**Para adicionar um driver de controlador de rede ou armazenamento à imagem de recuperação**

1.  Na caixa de diálogo **drivers adicionais** do **Assistente de imagem de recuperação DART**, clique em **Adicionar dispositivo**.

2.  Navegue até o arquivo a ser adicionado ao driver e clique em **abrir**.

    **Observação**  O arquivo de **Driver** é fornecido pelo fabricante do controlador de armazenamento ou de rede.

     

3.  Repita as etapas 1 e 2 para cada driver que você deseja incluir.

4.  Depois de concluir, clique em **Avançar**.

### Para adicionar arquivos à imagem de recuperação do DaRT

Siga estas etapas para adicionar arquivos à imagem de recuperação para que você possa usá-los para diagnosticar problemas do computador.

1.  Na caixa de diálogo **arquivos adicionais** do **Assistente de imagem de recuperação DART**, clique em **Mostrar arquivos**. Isso abre uma janela do Explorer que exibe a pasta que contém os arquivos compartilhados.

2.  Crie uma subpasta na pasta listada na caixa de diálogo.

3.  Copie os arquivos que você deseja para a nova subpasta.

4.  Depois de concluir, clique em **Avançar.**

### Para selecionar um local para o ISO que contém a imagem de recuperação do DaRT

Siga estas etapas para especificar o local onde a imagem ISO é criada:

1.  Na caixa de diálogo **criar imagem de inicialização** do **Assistente de imagem de recuperação DART**, clique em **procurar**.

2.  Navegue até o local preferencial na janela **salvar como** e, em seguida, clique em **salvar**.

3.  Depois de concluir, clique em **Avançar**.

O tamanho da imagem ISO vai variar, dependendo das ferramentas selecionadas e dos arquivos que você adicionar no assistente.

O assistente requer que a imagem ISO tenha uma extensão de nome de arquivo **. ISO** porque a maioria dos programas que grava um CD ou DVD requer essa extensão. Se você não especificar um local diferente, a imagem ISO será criada na área de trabalho com o nome **DaRT70. ISO**.

### Para gravar a imagem de recuperação em um CD ou DVD

Se o **Assistente de imagem de recuperação do DART** detectar uma unidade de CD-RW compatível em seu computador, ele será disponibilizado para gravar a imagem ISO em um disco para você. Se você quiser gravar um CD ou DVD e o assistente não reconhecer sua unidade, você deverá usar outro programa, como o programa incluído na unidade. Você pode usar um duplicador, um serviço de duplicação ou um CD ou um software de gravação de DVD para fazer cópias adicionais.

1.  Na caixa de diálogo **gravar em CD/DVD gravável** do **Assistente de imagem de recuperação do DART**, selecione **gravar a imagem na seguinte unidade de CD/DVD gravável**.

2.  Selecione a unidade de CD ou DVD.

    **Observação**  Se uma unidade não for reconhecida e você instalar uma nova unidade, você poderá clicar em **Atualizar lista de unidades** para forçar o assistente a atualizar a lista de unidades disponíveis.

     

3.  Clique em **Avançar**.

## Tópicos relacionados


[Criação da imagem de recuperação do DaRT 7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





