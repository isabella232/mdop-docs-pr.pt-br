---
title: Como usar a Dynamic Suite Composition
description: Como usar a Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796921"
---
# Como usar a Dynamic Suite Composition


A composição do pacote dinâmico na virtualização de aplicativos permite que você defina um aplicativo como dependente de outro aplicativo, como middleware ou um plug-in. Isso permite que o aplicativo interaja com o middleware ou plug-in no ambiente virtual, onde geralmente isso é evitado. Isso é útil porque um pacote de aplicativo secundário pode ser usado com vários outros aplicativos, chamados de *aplicativos principais*, que permitem que cada aplicativo primário faça referência ao mesmo pacote secundário.

Você pode usar a composição do pacote dinâmico ao sequenciar aplicativos que dependem de plug-ins, como controles ActiveX ou para aplicativos que dependem do middleware, como OLE DB ou JRE (Java Runtime Environment). Se cada aplicativo que usou esses componentes dependentes requer sequenciamento, incluindo os componentes, as atualizações para esses componentes exigem a resequenciação de todos os aplicativos principais. Se você sequenciar os aplicativos principais sem os componentes e, em seguida, sequenciar o middleware ou plug-in como um pacote secundário, somente o pacote secundário deverá ser atualizado.

Uma vantagem dessa abordagem é que ele reduz o tamanho dos pacotes primários. Outra vantagem é que ele oferece melhor controle das permissões de acesso nos aplicativos secundários. Observe que o aplicativo secundário pode ser transmitido da maneira normal e não precisa ser totalmente armazenado em cache para ser executado.

Um pacote principal pode ter mais de um pacote secundário. No entanto, apenas um nível de dependência tem suporte, portanto, não é possível definir um pacote secundário como dependente de outro pacote secundário. Além disso, o aplicativo secundário só pode ser middleware ou um plug-in e não pode ser outro produto de software completo.

Se você planeja fazer vários aplicativos principais dependentes de um único produto de middleware, certifique-se de testar essa configuração para determinar o efeito potencial sobre o desempenho do sistema antes de implantá-lo.

**Importante**  As dependências do pacote podem ser especificadas como obrigatórias para um aplicativo principal. Se um pacote secundário estiver sinalizado como obrigatório e não puder ser acessado por algum motivo durante o carregamento, a carga do pacote secundário falhará. Além disso, o aplicativo principal falhará quando o usuário tentar iniciá-lo.

 

Você pode usar os procedimentos a seguir para criar um pacote secundário, seja para um plug-in ou um componente middleware e, em seguida, pode usar o procedimento final para definir a dependência no arquivo OSD do pacote secundário.

**Para criar um pacote secundário para um plug-in usando a composição do pacote dinâmico**

1.  Em um computador de sequenciamento que está configurado com uma imagem limpa, instale o Application Virtualization Sequencer e salve o estado do computador.

2.  Sequenciar o aplicativo principal e salvar o pacote na pasta de conteúdo no servidor.

3.  Restaure o computador de sequenciamento para seu estado salvo da etapa 1.

4.  Instale e configure o aplicativo principal localmente no computador de sequenciamento.

    **Importante**  Você deve especificar uma nova raiz de pacote para o pacote secundário.

     

5.  Inicie a fase de monitoramento do sequenciador.

6.  Instale o plug-in no computador de sequenciamento e configure-o conforme necessário.

7.  Abra o aplicativo principal e confirme se o plug-in está funcionando corretamente.

8.  No console do sequenciador, crie um aplicativo fictício para representar o pacote secundário que conterá o plug-in e selecione um ícone.

9.  Salve o pacote na pasta de conteúdo no servidor.

    **Observação**  Para auxiliar no gerenciamento de pacotes secundários, é recomendável que o nome do pacote inclua o termo "pacote secundário" para enfatizar que esse é um pacote que não funcionará como um aplicativo autônomo, por exemplo, **\ [plug-in name \] pacote secundário**.

     

**Para criar um pacote secundário para middleware usando a composição do pacote dinâmico**

1.  Em um computador de sequenciamento que está configurado com uma imagem limpa, instale o Application Virtualization Sequencer e salve o estado do computador.

2.  Instale o middleware localmente no computador de sequenciamento e configure-o.

3.  Sequenciar o aplicativo principal e salvar o pacote na pasta de conteúdo no servidor.

4.  Restaure o computador de sequenciamento para seu estado salvo da etapa 1.

5.  Inicie o sequenciador para criar um novo pacote.

6.  Inicie a fase de monitoramento do sequenciador.

7.  Instale o aplicativo middleware no computador de sequenciamento e configure-o como em uma instalação típica.

8.  Conclua o processo de sequenciamento.

9.  Salve o pacote na pasta de conteúdo no servidor.

    **Observação**  Para auxiliar no gerenciamento de pacotes secundários, é recomendável que o nome do pacote inclua o termo "pacote secundário" para enfatizar que esse é um pacote que não funcionará como um aplicativo autônomo, por exemplo, o **pacote secundário do \ [nome do middleware \]**.

     

**Para definir a dependência no pacote primário**

1. No servidor, abra o arquivo OSD do pacote secundário para edição. (É uma boa ideia usar um editor de XML para fazer alterações no arquivo OSD; no entanto, você pode usar o bloco de notas como uma alternativa.)

2. Copie a linha **href de CodeBase** do arquivo.

3. Abra o arquivo OSD do pacote primário para edição.

4. Insira a <strong> &lt; marca dependências &gt; </strong> após a marca de fechamento da ** &lt; /ENVLIST &gt; ** no final da seção ** &lt; VIRTUALENV &gt; ** , logo antes da marca ** &lt; /VIRTUALENV &gt; ** .

5. Cole a linha **href de CodeBase** do pacote secundário após a marca de ** &lt; dependências &gt; ** que você acabou de criar.

6. Se o pacote secundário for um pacote obrigatório, o que significa que ele deve ser iniciado antes do pacote primário ser iniciado, adicione a propriedade **obrigatória = "true"** dentro da marca **codebase** . Se não for obrigatório, a propriedade poderá ser omitida.

7. Feche a marca de ** &lt; dependências &gt; ** inserindo o seguinte:

   **&lt;/DEPENDENCIES&gt;**

8. Examine as alterações feitas no arquivo OSD e salve e feche o arquivo. O exemplo a seguir mostra como a seção adicionada deve ser exibida. Os valores de marca mostrados aqui são apenas por exemplo.

   **&lt;VIRTUALENV&gt;**

        **&lt;ENVLIST&gt;**

   **…**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **&lt;/VIRTUALENV&gt;**

9. Se o pacote secundário tiver entradas na seção ** &lt; ENVLIST &gt; ** do arquivo OSD, você deverá copiar essas entradas para a mesma seção no pacote primário.

## Tópicos relacionados


[Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





