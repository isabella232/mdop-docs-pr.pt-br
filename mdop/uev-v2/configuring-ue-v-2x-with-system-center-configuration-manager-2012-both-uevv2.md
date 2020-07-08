---
title: Configurando o UE-V 2. x com o System Center Configuration Manager 2012
description: Configurando o UE-V 2. x com o System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799466"
---
# Configurando o UE-V 2. x com o System Center Configuration Manager 2012


Depois de instalar o Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 ou o 2,1 SP1 e seus recursos obrigatórios, a UE-V deve estar configurada. O pacote de configuração do UE-V fornece uma maneira para os administradores usarem o recurso configurações de conformidade do System Center Configuration Manager 2012 SP1 ou posterior para aplicar configurações consistentes entre sites nos quais o UE-V e o Configuration Manager estão instalados.

## Recursos compatíveis com o UE-V Configuration Pack


O pacote de configuração do UE-V inclui ferramentas para executar as seguintes tarefas:

-   Criar ou atualizar as linhas de base de distribuição do modelo de local de configurações do UE-V.

    -   Definir modelos UE-V a serem registrados ou não registrados

    -   Atualizar itens de configuração do modelo UE-V e linhas de base como modelos são adicionados ou atualizados

    -   Distribuir e registrar modelos do UE-V usando a correção padrão de item de configuração

-   Crie ou atualize um item de configuração de política do UE-V Agent para definir ou limpar essas configurações.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tamanho máximo do pacote</p></td>
    <td align="left"><p>Habilitar/desabilitar a sincronização de aplicativos do Windows</p></td>
    <td align="left"><p>Aguarde a sincronização durante o início do aplicativo</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Definindo o atraso de importação</p></td>
    <td align="left"><p>Sincronizar aplicativos do Windows não listados</p></td>
    <td align="left"><p>Aguarde a sincronização durante o logon</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Notificação de importação de configurações</p></td>
    <td align="left"><p>URL do contato de ti</p></td>
    <td align="left"><p>Aguarde o tempo limite de sincronização</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Caminho de armazenamento de configurações</p></td>
    <td align="left"><p>Texto descritivo do contato do contato</p></td>
    <td align="left"><p>Caminho do catálogo de modelos de configurações</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Ativação de sincronização</p></td>
    <td align="left"><p>Ícone de bandeja habilitado</p></td>
    <td align="left"><p>Iniciar/parar o serviço de agente do UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Método de sincronização</p></td>
    <td align="left"><p>Notificação de primeira utilização</p></td>
    <td align="left"><p>Definir quais aplicativos do Windows serão as configurações de roaming</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tempo limite de sincronização</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   Verifique a conformidade confirmando que o UE-V está em execução.

## Gerar um item de configuração de política do UE-V Agent


Todas as políticas e políticas do UE-V Agent são distribuídas por meio de um único item de configuração que é gerado usando a ferramenta de UevAgentPolicyGenerator.exe. Essa ferramenta lê a configuração desejada de um arquivo de configuração XML e cria um CI contendo as configurações de descoberta e correção necessárias para colocar a máquina em conformidade.

O arquivo CAB do item de configuração da política do UE-V Agent é criado usando a ferramenta de linha de comando UevTemplateBaselineGenerator.exe, que tem os seguintes parâmetros:

-   Código do site do site &lt;&gt;

-   PolicyName &lt; nome &gt; opcional: padrão para "política de agente do UE-V", se não estiver presente

-   Descrição do PolicyDescription &lt; &gt; opcional: uma descrição será fornecida se não estiver presente

-   CabFilePath &lt; caminho completo para o item de configuração. Arquivo CAB&gt;

-   ConfigurationFile &lt; caminho completo para arquivo XML de configuração do agente&gt;

**Observação**  Pode ser necessário alterar a política de execução do PowerShell para permitir que esses scripts sejam executados em seu ambiente. Execute estas etapas no console do Configuration Manager:

1.  Selecionar ** &gt; &gt; Propriedades de configurações do cliente de administração**

2.  Na guia **agente do usuário** , defina a **política de execução do PowerShell** como **ignorar**

<a href="" id="create"></a>**Criar o primeiro item de configuração da política do UE-V**

1.  Copie o arquivo de configuração de configurações padrão do diretório de instalação do UE-V config Pack para um local visível para o seu console de administração do ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    O arquivo de configuração padrão contém cinco seções:

    <a href="" id="computer-policy"></a>**Política de computador**  
    Todas as configurações no nível da máquina UE-V. O atributo desirestate pode ser

    -   **Definido** para ter o valor atribuído no registro

    -   **Desmarque** para remover a configuração

    -   **Não gerenciado** para que o item de configuração seja deixado em seu estado atual

    Não remova as linhas desta seção. Em vez disso, defina ostate desejado como ' não gerenciado ' se você não quiser que o Configuration Manager altere os valores atuais ou padrão.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    Todas as configurações de nível de usuário do UE-V. Essas entradas substituem as configurações da máquina para um usuário. O atributo desirestate pode ser

    -   **Definido** para ter o valor atribuído no registro

    -   **Desmarque** para remover a configuração

    -   **Não gerenciado** para que o item de configuração seja deixado em seu estado atual

    Não remova as linhas desta seção. Em vez disso, defina ostate desejado como ' não gerenciado ' se você não quiser que o Configuration Manager altere os valores atuais ou padrão.

    <a href="" id="services"></a>**Serviços**  
    As entradas nesta seção controlam a operação do serviço. O arquivo de configuração padrão contém uma única entrada para o UevAgentService. O atributo desirestate pode ser definido como **running** ou **Stopped**.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    Todas as configurações de sincronização do aplicativo Windows em nível de máquina. Cada PackageFamilyName listado nesta seção pode ser atribuído umstate desejado de

    -   **Habilitado** para ter configurações de roaming

    -   **Desabilitado** para impedir que as configurações sejam móveis

    -   **Desmarcada** para que a entrada seja removida do controle UE-V

    Linhas adicionais podem ser adicionadas a esta seção com base na lista de aplicativos do Windows instalados que podem ser visualizados usando o cmdlet do PowerShell GetAppxPackage.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    É idêntico ao Windows8AppsComputerPolicy com configurações que substituem as configurações do computador para um usuário individual.

2.  Edite o arquivo de configuração alterando os campos estado e valor desejados.

3.  Execute este comando em um computador que executa o console de administração do ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  Importar o arquivo CAB usando o console do ConfigMgr ou o PowerShell Import-CMConfigurationItem

**Atualizar um item de configuração de política do UE-V**

1.  Edite o arquivo de configuração alterando os campos estado e valor desejados.

2.  Execute o comando da etapa 3 em [criar o primeiro item de configuração da política do UE-V](#create). Se você alterou o nome com o parâmetro PolicyName, certifique-se de inserir o mesmo nome.

3.  Reimportar o arquivo CAB. A versão no ConfigMgr será atualizada.

## Gerar uma linha de base de modelo UE-V
Os modelos do UE-V são distribuídos usando uma linha de base contendo vários itens de configuração. Cada item de configuração contém os scripts de descoberta e correção necessários para instalar um modelo de UE-V. O modelo real UE-V é inserido no script de correção para distribuição usando a funcionalidade padrão de item de configuração.

A linha de base do modelo UE-V é criada usando a ferramenta de linha de comando UevTemplateBaselineGenerator.exe, que tem os seguintes parâmetros:

-   Código do site do site &lt;&gt;

-   Nome da linha de basename &lt; &gt; (opcional: padrões para "linha de base de distribuição do modelo do UE-V", se não estiverem presentes)

-   &lt;Descrição &gt; do BaselineDescription (opcional: uma descrição será fornecida se não estiver presente)

-   &lt;Pasta de modelos do TemplateFolder UE-V&gt;

-   Registrar a &lt; lista de arquivos de modelo separados por vírgula&gt;

-   Remover registro da &lt; lista de modelos separados por vírgula&gt;

-   CabFilePath &lt; caminho completo para o arquivo CAB da linha de base a ser gerado&gt;

O resultado é um arquivo CAB de linha de base que está pronto para ser importado para o Configuration Manager. Se, em uma data futura, você atualizar ou adicionar um modelo, poderá executar novamente o comando usando o mesmo nome de linha de base. Importar os resultados do CAB em atualizações de versão do CI nos modelos alterados.

### <a href="" id="create2"></a>Criar a primeira linha de base de modelo UE-V

1.  Crie um conjunto "mestre" de modelos do UE-V em um local de pasta estável visível para a máquina que está executando o console de administração do ConfigMgr. À medida que os modelos são adicionados ou atualizados, essa pasta é onde elas são puxadas para distribuição. A lista inicial de modelos pode ser copiada de um computador com a UE-V instalada. O local padrão do modelo é C:\\Arquivos de experiência do usuário do Files\\Microsoft Virtualization\\Templates.

2.  Crie um arquivo text.bat onde você possa adicionar o comando gerador de modelos. Isso é opcional, mas tornará a regeneração mais simples se você salvar os parâmetros do comando.

3.  Adicione o comando e os parâmetros ao arquivo. bat que irá gerar a linha de base. O exemplo a seguir cria uma linha de base que distribui o bloco de notas e a calculadora:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  Execute o arquivo. bat para criar UevTemplateBaseline.cab pronto para importação no Configuration Manager.

### Atualizar uma linha de base de modelo UE-V

O gerador de modelos usa a versão do modelo para determinar se um modelo deve ser atualizado. Se você fizer uma alteração no modelo e atualizar a versão, o gerador da linha de base comparará o modelo em sua pasta mestra com o modelo contido no IC no servidor do ConfigMgr. Se for encontrada uma diferença, a linha de base e as versões de IC modificadas serão atualizadas.

Para distribuir um novo modelo do bloco de notas, execute estas etapas:

1.  Atualize o modelo e a versão do modelo localizada &lt; no &gt; elemento Version do modelo.

2.  Copie o modelo para seu diretório de modelo mestre.

3.  Execute o comando no arquivo. bat que você criou na etapa 3 em [criar a primeira linha de base de modelo UE-V](#create2).

4.  Importe o arquivo CAB gerado para o ConfigMgr usando o console ou o CMBaseline de importação do PowerShell.

## Obter o pacote de configuração do UE-V


É possível baixar o pacote de configuração do UE-V para o Configuration Manager 2012 SP1 ou posterior [aqui](https://go.microsoft.com/fwlink/?LinkId=317263).






## Tópicos relacionados


[Gerenciar as configurações da UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





