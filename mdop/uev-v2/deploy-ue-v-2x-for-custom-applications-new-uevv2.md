---
title: Implantar o UE-V 2. x para aplicativos personalizados
description: Implantar o UE-V 2. x para aplicativos personalizados
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799465"
---
# Implantar o UE-V 2. x para aplicativos personalizados


Microsoft User Experience Virtualization (UE-V) 2,0. o 2,1 e o 2,1 SP1 usam arquivos XML denominados **modelos de localização de configurações** para monitorar e sincronizar as configurações do aplicativo da área de trabalho e as configurações da área de trabalho do Windows entre os computadores Por padrão, alguns modelos de local das configurações estão incluídos no UE-V. Mas se você quiser sincronizar configurações para aplicativos da área de trabalho diferentes daqueles incluídos nos modelos padrão, poderá criar seus próprios modelos de local de configurações personalizadas usando o UE-V Generator.

Depois de ler o material de planejamento em [preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) e decidir que você deseja sincronizar as configurações para aplicativos personalizados (terceiros, de linha de negócios, etc.), você vai implantar os recursos da UE-V conforme descrito neste tópico. Para começar, aqui estão as principais etapas necessárias para sincronizar as configurações para aplicativos personalizados:

-   [Instalar o gerador UEV](#uevgen)

    Use o gerador UEV para criar modelos de local de configurações XML personalizadas.

-   [Configurar um catálogo de modelos de configurações do UE-V](#deploycatalogue)

    Você pode definir esse caminho onde modelos de localização de configurações personalizadas são armazenados.

-   [Criar modelos de local de configurações personalizadas](#createcustomtemplates)

    Esses modelos personalizados permitem que os usuários sincronizem as configurações para aplicativos personalizados.

-   [Implantar os modelos de local de configurações personalizadas](#deploycustomtemplates)

    Depois de testar o modelo personalizado para garantir que as configurações sejam sincronizadas corretamente, você pode implantar esses modelos de uma destas maneiras:

    -   Por meio da infraestrutura de implantação existente, como o Configuration Manager

    -   Usando as preferências de política de grupo

    -   [Implantar um catálogo de modelos de configurações do UE-V](#deploycatalogue)

    **Observação**  Os modelos implantados usando ESD ou a política de grupo devem ser registrados com o WMI (Instrumentação de gerenciamento do Windows) do UE-V ou o Windows PowerShell.

     

## Preparar-se para implantar o UE-V 2. x para aplicativos personalizados


Antes de começar a implantar os recursos do UE-V que manipulam aplicativos personalizados, há apenas algumas coisas a serem revisadas.

### O UE-V Generator

O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações. O aplicativo que é monitorado deve ser um aplicativo tradicional. Você usa o UE-V Generator para criar modelos de local de configurações, mas não pode criar um modelo de local de configurações a partir desses tipos de aplicativos:

-   Aplicativos virtualizados

-   Aplicativos oferecidos por meio dos serviços de terminal

-   Aplicativos Java

-   Aplicativos do Windows  

**Observação**  Os modelos de local das configurações do UE-V não podem ser criados em aplicativos virtualizados ou aplicativos de serviços de terminal. No entanto, as configurações sincronizadas usando os modelos podem ser aplicadas a esses aplicativos. Para criar modelos compatíveis com o VDI (Virtual Desktop Infrastructure) e aplicativos de serviços de terminal, abra uma versão do pacote do Windows Installer (. msi) do aplicativo usando o UE-V Generator. Para obter mais informações sobre a sincronização de configurações para aplicativos virtuais, consulte [usando o UE-V 2. x com aplicativos de virtualização de aplicativo](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).

 

**Locais excluídos:** O processo de descoberta exclui locais que normalmente armazenam arquivos de software do aplicativo que não sincronizam configurações bem entre computadores de usuário ou ambientes de computação. Por padrão, eles são excluídos:

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows

-   Todas as chaves do registro localizadas na seção HKEY \ _LOCAL \ _MACHINE

-   Arquivos localizados em diretórios de arquivos de programas

-   Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow

-   Arquivos do sistema operacional do Windows localizados em% SystemRoot%

Se as chaves do registro e os arquivos armazenados em locais excluídos forem necessários para sincronizar as configurações do aplicativo, você pode adicionar manualmente os locais ao modelo de local de configurações durante o processo de criação de modelos.
No entanto, somente as alterações feitas em HKEY \ _CURRENT \ _USER Hive serão Sync-Ed.

### Substituir os modelos padrão da Microsoft

O UE-V Agent instala um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft e configurações do Windows. Se você personalizar esses modelos ou criar modelos de local de configurações para sincronizar as configurações de aplicativos personalizados, o UE-V Agent pode ser configurado para usar um catálogo de modelos de configurações para armazenar os modelos. Nesse caso, será necessário incluir os modelos padrão juntamente com os modelos personalizados no catálogo de modelos de configurações.

Ao [implantar um agente do UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), você pode usar o parâmetro de linha de comando `RegisterMSTemplates` para desabilitar o registro dos modelos padrão da Microsoft.

Ao usar a política de grupo para definir o caminho do catálogo de modelos de configurações, você pode optar por substituir os modelos padrão da Microsoft. Se você definir as configurações de política para substituir os modelos padrão da Microsoft, todos os modelos padrão da Microsoft instalados pelo UE-V Agent serão excluídos e somente os modelos localizados no catálogo de modelos de configurações serão usados. O parâmetro de configuração do UE-V Agent `RegisterMSTemplates` deve ser definido como *true* para substituir o modelo padrão da Microsoft.

**Observação**  Se você desabilitar essa configuração de política após a habilitação, o UE-V Agent não restaurará os modelos padrão da Microsoft.

 

Se houver modelos personalizados no catálogo de modelos de configurações que usam a mesma ID que os modelos padrão da Microsoft, e o UE-V Agent não estiver configurado para substituir os modelos padrão da Microsoft, os modelos da Microsoft serão ignorados.

Você também pode substituir os modelos padrão usando os recursos do Windows PowerShell do UE-V. Para substituir o modelo padrão da Microsoft pelo Windows PowerShell, cancele o registro de todos os modelos padrão da Microsoft e registre os modelos personalizados.

**Observação**  Os pacotes de configurações antigas permanecerão no local de armazenamento configurações, mesmo se você implantar novos modelos de local de configurações para um aplicativo. Esses pacotes não são lidos pelo agente, mas nenhum deles é excluído automaticamente.

 

## <a href="" id="uevgen"></a>Instalar o UEV 2. x Generator


Instale o gerador do 2,0 do Microsoft User Experience Virtualization (UE-V) em um computador que você pode usar para criar um modelo de local de configurações personalizado. Esse computador deve ter os aplicativos instalados para os quais modelos de localização de configurações personalizadas serão gerados.

**Para instalar o UE-V Generator**

1.  Como usuário com direitos de administrador local, localize o arquivo de instalação do gerador do UE-V **ToolSetup.exe** fornecido com o software UE-v. Ou, se você souber a arquitetura do computador, poderá executar o arquivo apropriado do Windows Installer (. msi), **ToolsSetupx64.msi** ou **ToolsSetupx86.msi**.

2.  Clique duas vezes no arquivo de instalação. O assistente de configuração do gerador do User Experience Virtualization é aberto. Clique em **Avançar** para continuar.

3.  Aceite os termos de licença para software Microsoft e clique em **Avançar**.

4.  Clique nas opções do programa de aperfeiçoamento da experiência do usuário e opções do Microsoft Update.

5.  Selecione a pasta de destino na qual instalar o UE-V Generator e clique em **Avançar**.

6.  Clique em **instalar** para começar a instalação.

    **Observação**  Uma solicitação de **controle de conta de usuário** é exibida antes de o aplicativo ser instalado. É necessário ter permissão para instalar o UE-V Generator.

     

7.  Clique em **concluir** para fechar o assistente após a conclusão da instalação. Você deve reiniciar o computador para poder executar o UE-V Generator.

    Para verificar se a instalação foi bem-sucedida, clique em **Iniciar**, clique em **todos os programas**, clique em **virtualização da experiência do usuário da Microsoft**e, em seguida, clique em **gerador do Microsoft User Experience Virtualization**.

    **Observação**  O gerador UE-V 2 somente pode ser usado para criar modelos para agentes UE-V 2. Em uma implantação mista dos agentes do UE-V 1,0 e do UE-V 2, você deve continuar a usar o gerador do UE-V 1,0 até ter atualizado todos os agentes do UE-V.

     

## <a href="" id="deploycatalogue"></a>Implantar um catálogo de modelos de configurações


O catálogo de modelos de configurações de experiência de usuário da experiência do usuário é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens (SMB) que armazena todos os modelos de local de configurações personalizadas. Uma tarefa agendada no UE-V Agent verifica esse local uma vez por dia e atualiza seu comportamento de sincronização, com base nos modelos desta pasta.

O UE-V Agent registra os modelos que foram adicionados ou atualizados nesta pasta após a última vez que a pasta foi verificada e cancela o registro de modelos que são removidos. Por padrão, os modelos são registrados e não registrados uma vez por dia em 3:30 A.M. Hora local pelo Agendador de tarefas e na inicialização do sistema. Para personalizar a frequência desta tarefa agendada, consulte [alterando a frequência das tarefas agendadas de UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

Você pode definir o caminho do catálogo de modelos de configurações usando as opções de linha de comando de instalação, a política de grupo, a WMI ou o Windows PowerShell. Os modelos armazenados no caminho do catálogo de modelos de configurações são automaticamente registrados e não são registrados por uma tarefa agendada.

**Para configurar o catálogo de modelos de configurações para UE-V 2. x**

1.  Crie uma nova pasta no computador que armazena o catálogo de modelos de configurações do UE-V.

2.  Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta catálogo de modelos de configurações.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computadores do domínio</p></td>
    <td align="left"><p>Ler níveis de permissão</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Níveis de permissão de leitura/gravação</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Defina as seguintes permissões do sistema de arquivos NTFS para a pasta catálogo de modelos de configurações.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Conta de usuário</th>
    <th align="left">Permissões recomendadas</th>
    <th align="left">Aplicar a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Criador/proprietário</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computadores do domínio</p></td>
    <td align="left"><p>Listar conteúdo da pasta e ler</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Esta pasta, subpastas e arquivos</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Clique em **OK** para fechar as caixas de diálogo.

No mínimo, o compartilhamento de rede deve conceder permissões para o grupo computadores do domínio. Além disso, conceda permissões de acesso à pasta de compartilhamento de rede para administradores que devem gerenciar os modelos armazenados.

## <a href="" id="createcustomtemplates"></a>Criar modelos de local de configurações personalizadas


Use o UE-V Generator para criar modelos de local de configurações para aplicativos de linha de negócios ou outros aplicativos personalizados. Depois que o modelo de um aplicativo for criado, você poderá implantá-lo nos computadores para que as configurações sejam sincronizadas para esse aplicativo.

**Para criar um modelo de local de configurações de UE-V com o UE-V Generator**

1.  Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.

2.  Clique em **criar um modelo de local de configurações**.

3.  Especifique o aplicativo. Navegue até o caminho do arquivo do aplicativo (. exe) ou o atalho do aplicativo (. lnk) para o qual você deseja criar um modelo de local de configurações. Especifique os argumentos de linha de comando, se houver e diretório de trabalho, se houver. Clique em **Avançar** para continuar.

    **Observação**  Antes de o aplicativo ser iniciado, o sistema exibe uma solicitação de **controle de conta de usuário**. É necessário ter permissão para monitorar o registro e os locais de arquivo que o aplicativo usa para armazenar as configurações.

     

4.  Depois que o aplicativo for iniciado, feche o aplicativo. O gerador do UE-V registra os locais onde o aplicativo armazena suas configurações.

5.  Após a conclusão do processo, clique em **Avançar** para continuar.

6.  Revise e marque as caixas de seleção que estão próximas às configurações locais do registro e locais dos arquivos de configurações a serem sincronizados para este aplicativo. A lista inclui as duas categorias a seguir para locais de configurações:

    -   **Padrão**: configurações de aplicativo que são armazenadas no registro nas chaves hKey \ _CURRENT \ _USER ou nas pastas de arquivo em \ \ **Users** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **roaming**. O gerador do UE-V inclui essas configurações por padrão.

    -   Não **padrão**: as configurações do aplicativo armazenadas fora dos locais são especificadas nas práticas recomendadas para armazenamento de dados de configurações (opcional). Isso inclui arquivos e pastas em **usuários** \ \ \ [nome de usuário \] \ \ **AppData**  \\  **local**. Revise esses locais para determinar se devem ser incluídos no modelo de local de configurações. Marque as caixas de seleção de locais para incluí-las.

    Clique em **Avançar** para continuar.

7.  Revise e edite quaisquer **Propriedades**, locais **do registro** e locais de **arquivos** para o modelo de local de configurações.

    -   Edite as seguintes propriedades na guia **Propriedades** :

        -   **Nome do aplicativo**: o nome do aplicativo que está escrito na descrição das propriedades dos arquivos de programa.

        -   **Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa. Esse nome geralmente tem a extensão de nome de arquivo. exe.

        -   **Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo. Essa propriedade, em conjunto com a **versão do arquivo**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do produto.

        -   **Versão do arquivo**: o número da versão do arquivo. exe do aplicativo. Essa propriedade, em conjunto com a **versão do produto**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do programa.

        -   **Nome do autor do modelo** (opcional): o nome do autor do modelo de local de configurações.

        -   **Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.

    -   A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações. Edite os locais do registro usando o menu suspenso **tarefas** . As tarefas permitem que você adicione novas chaves, edite o nome ou o escopo das chaves existentes, exclua as chaves e procure o registro no qual as chaves estão localizadas. Use o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada. Use **todas as configurações e subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.

    -   A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais de arquivos que estão incluídos no modelo de local de configurações. Edite os locais de arquivos usando o menu suspenso **tarefas** . Tarefas para locais de arquivos permitem adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer. Deixe a máscara de arquivo vazia para incluir todos os arquivos na pasta especificada.

8.  Clique em **criar**e, em seguida, clique em **salvar** para salvar o modelo de local de configurações no computador.

9.  Clique em **fechar** para fechar o assistente de modelo de configurações. Saia do aplicativo do gerador do UE-V.

    Depois de criar o modelo de local de configurações para um aplicativo, você deve testar o modelo. Implante o modelo em um ambiente de laboratório antes de colocá-lo em produção na empresa.

[Referência de esquema de modelo de aplicativo para UE-V](https://technet.microsoft.com/library/dn763947.aspx) detalha a estrutura XML do modelo de local de configurações do UE-v e fornece orientação para a edição desses arquivos.

## <a href="" id="deploycustomtemplates"></a>Implantar os modelos de local de configurações personalizadas


Depois de criar um modelo de local de configurações com o UE-V Generator, você deve testá-lo para garantir que as configurações do aplicativo sejam sincronizadas corretamente. Em seguida, você pode implantar com segurança o modelo de local de configurações em computadores da empresa.

Os modelos de local de configurações podem ser implantados usando um destes métodos:

-   Um sistema ESD (Enterprise Software Distribution), como o System Center Configuration Manager

-   Preferências da Política de Grupo

-   Um catálogo de modelos de configurações de UE-V

Os modelos implantados usando um sistema ESD ou objetos de política de grupo devem ser registrados por meio da WMI (Instrumentação de gerenciamento do Windows) do UE-V ou do Windows PowerShell. Os modelos armazenados na localização do catálogo de modelos de configurações são automaticamente registrados pelo UE-V Agent.

**Para usar o caminho do catálogo de modelos de configurações para implantar os modelos de local das configurações do UE-V**

1.  Navegue até a pasta de compartilhamento de rede que é definida como o catálogo de modelos de configurações.

2.  Adicione, remova ou atualize os modelos de local de configurações no catálogo de modelos de configurações para refletir a configuração de modelo de agente do UE-V que você deseja para computadores UE-V.

    **Observação**  Os modelos em computadores são atualizados diariamente. A atualização é baseada em alterações no catálogo de modelos de configurações.

     

3.  Para atualizar manualmente os modelos em um computador que executa o UE-V Agent, abra um prompt de comando elevado e navegue até **% Program Files%\\Microsoft Virtualization Experience User Experience \ \ Agent \ \ &lt; x86 ou x64 &gt; **e execute **ApplySettingsTemplateCatalog.exe**.

    **Observação**  Este programa é executado automaticamente durante a inicialização do computador e o diário em 3:30 A. M. para coletar novos modelos que foram adicionados recentemente ao catálogo.

     






## Tópicos relacionados


[Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





