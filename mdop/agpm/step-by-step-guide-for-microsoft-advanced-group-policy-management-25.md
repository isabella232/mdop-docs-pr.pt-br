---
title: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft
description: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797676"
---
# Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft


Este guia passo a passo demonstra técnicas avançadas de gerenciamento de política de grupo usando o console de gerenciamento de política de grupo (GPMC) e o gerenciamento avançado de política de grupo (AGPM) da Microsoft. O AGPM aumenta a funcionalidade do GPMC, fornecendo:

-   Funções padrão para delegar permissões para gerenciar GPOs (objetos de política de grupo) para vários administradores de política de grupo.

-   Um arquivo morto para permitir que os administradores de política de grupo criem e modifiquem os GPOs offline antes de implantá-los em um ambiente de produção.

-   A capacidade de reverter para qualquer versão anterior de um GPO.

-   Funcionalidade de check-in/check-out para os GPOs para garantir que os administradores de política de grupo não substituam acidentalmente o trabalho uns dos outros.

## Visão geral do cenário do AGPM


Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a política de grupo pode ser gerenciada em um ambiente com vários administradores de política de grupo com diferentes níveis de permissões. Especificamente, você vai executar as seguintes tarefas:

-   Usando uma conta que seja membro do grupo Domain admins, instale o servidor do AGPM e atribua a função de administrador do AGPM a uma conta ou grupo.

-   Usando contas às quais você atribuirá funções do AGPM, instale o cliente do AGPM.

-   Usar uma conta com a função de administrador do AGPM, configurar o AGPM e o acesso de representante a GPOs atribuindo funções a outras contas.

-   Usando uma conta com a função editor, solicite a criação de um GPO, que você Então aprova usando uma conta com a função de aprovador. Com a conta editor, verifique o GPO do arquivo morto, edite o GPO, verifique o GPO no arquivo e solicite a implantação.

-   Usando uma conta com a função Aprovador, examine o GPO e implante-o em seu ambiente de produção.

-   Usando uma conta com a função editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.

-   Usar uma conta com a função Aprovador, excluir e restaurar um GPO.

![processo de desenvolvimento de objetos de política de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## Requisitos


Os computadores em que você deseja instalar o AGPM devem atender aos seguintes requisitos, e você deve criar contas para uso nesse cenário.

### Requisitos do servidor do AGPM

O servidor do AGPM 2.5 requer o WindowsVista® (versão de 32 bits) sem Service Packs instalados ou Windows Server® 2003 (versão de 32 bits), bem como o GPMC. Além disso, você deve ser membro do grupo Domain admins para instalar o servidor do AGPM.

Você deve instalar o servidor do AGPM em um servidor membro ou controlador de domínio com a versão mais recente do GPMC que está disponível para você e com o suporte do AGPM. O AGPM usa o GPMC para fazer backup e restaurar GPOs, e as versões mais recentes do GPMC fornecem configurações de política adicionais não disponíveis nas versões anteriores. Se a versão do GPMC em seu servidor do AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a política de grupo, o servidor do AGPM não poderá armazenar essas configurações de política não estarão disponíveis na versão anterior do GPMC.

Especificamente, se o seu servidor do AGPM estiver executando o Windows Server2003 e a versão do GPMC que o acompanha, e os computadores dos administradores de política de grupo estiverem executando o WindowsVista e a versão do GPMC que o acompanha, você ainda poderá gerenciar a maioria das configurações de política. No entanto, as configurações de política do GPMC no Windows Vista que não estão disponíveis no GPMC no Windows Server 2003, como aquelas relacionadas ao redirecionamento de pastas, à rede sem fio (IEEE 802,11) e às impressoras implantadas, não podem ser armazenadas pelo servidor do AGPM, mesmo que os administradores possam configurá-las usando o AGPM em seus computadores.

Se você precisar instalar o servidor do AGPM em um computador com uma versão mais antiga do GPMC do que os administradores de política de grupo estão em execução, consulte a referência de configurações da política de grupo para obter detalhes sobre quais configurações de política estão disponíveis com quais sistemas operacionais. Para baixar a referência de configurações de política de grupo, consulte <https://go.microsoft.com/fwlink/?LinkID=106147> .

**Observação**  Não é possível migrar arquivos de um servidor do AGPM ou um servidor do GPOVault que executa o Windows Server2003 para um servidor do AGPM executando o WindowsVista.

Para o Windows Server2003, se o GPOVault Server estiver instalado no computador em que você deseja instalar o servidor do AGPM, é recomendável que você não desinstale o GPOVault Server antes de começar a instalação. A instalação do servidor do AGPM desinstalará o GPOVault Server e transferirá automaticamente os dados de arquivo morto existentes do GPOVault para um arquivo do AGPM.

 

### Requisitos do cliente do AGPM

O cliente do AGPM 2.5 requer o WindowsVista (versão de 32 bits) sem Service Packs instalados ou Windows Server2003 (versão de 32 bits), bem como o GPMC. O cliente do AGPM pode ser instalado em um computador que esteja executando o servidor do AGPM.

### Requisitos do cenário

Antes de iniciar esse cenário, crie quatro contas de usuário. Durante o cenário, você atribuirá uma das seguintes funções do AGPM a cada uma dessas contas: administrador do AGPM (controle total), Aprovador, editor e revisor. Essas contas devem ser capazes de enviar e receber mensagens de email. Atribua a permissão de **vincular GPOs** às contas com as funções do editor do administrador do AGPM, Aprovador e (opcionalmente).

**Observação** 
 A permissão **vincular GPOs** é atribuída a membros de administradores de domínio e administradores corporativos por padrão. Para atribuir permissões de **GPOs de link** a usuários ou grupos adicionais (como contas com funções de administrador ou aprovador do AGPM), clique no nó do domínio e, em seguida, clique na guia **delegação** , selecione **vincular GPOs**, clique em **Adicionar**e selecione os usuários ou grupos aos quais atribuir a permissão.

 

Para esse cenário, você executa ações com contas diferentes. Você pode fazer logon com cada conta conforme indicado ou pode usar o comando **Executar como** para iniciar o GPMC com a conta indicada.

**Observação**  Para usar o comando **Executar como** com o GPMC no Windows Server2003, clique em **Iniciar**, aponte para **Ferramentas administrativas**, clique com o botão direito do mouse em **Gerenciamento de política de grupo**e clique em **Executar como**. Clique **no seguinte usuário** e insira as credenciais de uma conta.

Para usar o comando **Executar como** com o GPMC no Windows Vista, clique no botão **Iniciar** , aponte para **executar**e digite **runas/User:** <em> DomainName\\UserName </em> **"mmc%windir%\\system32\\gpmc.msc"** e clique em **OK**. Digite a senha da conta quando for solicitado.

 

## Etapas para instalar e configurar o AGPM


Você deve completar as etapas a seguir para instalar e configurar o AGPM.

[Etapa 1: instalar o servidor do AGPM](#bkmk-config1)

[Etapa 2: instalar o cliente do AGPM](#bkmk-config2)

[Etapa 3: configurar uma conexão com o servidor do AGPM](#bkmk-config3)

[Etapa 4: configurar a notificação por email](#bkmk-config4)

[Etapa 5: delegar acesso](#bkmk-config5)

### <a href="" id="bkmk-config1"></a>Etapa 1: instalar o servidor do AGPM

Nesta etapa, você instala o servidor do AGPM no servidor membro ou controlador de domínio que executará o serviço do AGPM e você poderá configurar o arquivo morto. Todas as operações do AGPM são gerenciadas por meio desse serviço do Windows e são executadas com as credenciais do serviço. O arquivo gerenciado por um servidor do AGPM pode ser hospedado nesse servidor ou em outro servidor na mesma floresta.

**Para instalar o servidor do AGPM no computador que irá hospedar o serviço do AGPM**

1.  Faça logon com uma conta que seja membro do grupo Domain admins.

2.  Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **Advanced Group Policy Management-Server**.

3.  Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.

4.  Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.

5.  Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o servidor do AGPM. O computador no qual o servidor do AGPM está instalado hospedará o serviço do AGPM e gerenciará o arquivo morto. Clique em **Avançar**.

6.  Na caixa de diálogo **caminho do arquivo morto** , selecione um local para o arquivo morto relativo ao servidor do AGPM. O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados do histórico gerenciados por esse servidor do AGPM. Clique em **Avançar**.

7.  Na caixa de diálogo **conta de serviço do AGPM** , selecione uma conta de serviço na qual o serviço do AGPM será executado e clique em **Avançar**.

8.  Na caixa de diálogo **proprietário do arquivo** , selecione uma conta ou grupo à qual atribuir inicialmente a função de administrador do AGPM (controle total). Esse administrador do AGPM pode atribuir funções do AGPM e permissões a outros administradores de política de grupo (incluindo a função de administrador do AGPM). Para esse cenário, selecione a conta a ser usada na função de administrador do AGPM. Clique em **Avançar**.

9.  Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.

    **Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional. Isso pode impedir que o serviço do AGPM seja iniciado. Para saber mais sobre como modificar as configurações do serviço, confira ajuda para gerenciamento avançado de política de grupo.

     

### <a href="" id="bkmk-config2"></a>Etapa 2: instalar o cliente do AGPM

Cada administrador da política de grupo — qualquer pessoa que cria, edita, implanta, revisa ou exclui GPOs — deve ter o cliente do AGPM instalado em computadores que eles usam para gerenciar GPOs. Para esse cenário, instale o cliente do AGPM em pelo menos um computador. Você não precisa instalar o cliente do AGPM nos computadores dos usuários finais que não executam a administração da política de grupo.

**Para instalar o cliente do AGPM no computador de um administrador de política de grupo**

1.  Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar **gerenciamento avançado de política de grupo-cliente**.

2.  Na caixa de diálogo de **boas-vindas** , clique em **Avançar**.

3.  Na caixa de diálogo **termos de licença para software da Microsoft** , aceite os termos e clique em **Avançar**.

4.  Na caixa de diálogo **caminho do aplicativo** , selecione um local no qual instalar o cliente do AGPM. Clique em **Avançar**.

5.  Na caixa de diálogo **servidor do AGPM** , digite o nome do computador totalmente qualificado e a porta do servidor do AGPM ao qual se conectar. A porta padrão do serviço do AGPM é 4600. Clique em **Avançar**.

6.  Clique em **instalar**e, em seguida, clique em **concluir** para sair do assistente de configuração.

### <a href="" id="bkmk-config3"></a>Etapa 3: configurar uma conexão com o servidor do AGPM

O AGPM armazena todas as versões de cada objeto de política de grupo (GPO) controlado — um GPO para o qual o AGPM fornece controle de alterações — em um arquivo central, para que os administradores de política de grupo possam exibir e modificar os GPOs offline sem afetar imediatamente a versão implantada de cada GPO.

Nesta etapa, você configura uma conexão do servidor do AGPM e garante que todos os administradores de política de grupo se conectam ao mesmo servidor de AGPM. (Para obter informações sobre como configurar vários servidores de AGPM, consulte a ajuda para gerenciamento avançado de política de grupo.)

**Para configurar uma conexão do servidor do AGPM para todos os administradores de política de grupo**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com a conta de usuário selecionada como o proprietário do arquivo. Esse usuário tem a função de administrador do AGPM (controle total).

2.  Clique em **Iniciar**, aponte para **Ferramentas administrativas**e clique em **Gerenciamento de política de grupo** para abrir o **GPMC (console de gerenciamento de política de grupo)**.

3.  Na árvore de **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo.

4.  Na janela **Editor de objeto de política de grupo** , clique em **configuração do usuário**, **modelos administrativos**e **componentes do Windows**.

5.  Se o **AGPM** não estiver listado em **componentes do Windows**:

    1.  Clique com o botão direito do mouse em **modelos administrativos** e selecione **Adicionar/remover modelos**.

    2.  Clique **em Adicionar**, selecione **AGPM. admx** ou **AGPM. adm**, clique em **abrir**e, em seguida, clique em **fechar**.

6.  Em **componentes do Windows**, clique duas vezes em **AGPM**.

7.  No painel de detalhes, clique duas vezes em **servidor do AGPM (todos os domínios)**.

8.  Na janela de **Propriedades do servidor do AGPM (todos os domínios)** , selecione **habilitado** e digite o nome do computador e a porta totalmente qualificados (por exemplo, Server.contoso.com:4600) para o servidor que hospeda o arquivo morto. A porta usada pelo serviço do AGPM é a porta 4600.

9.  Clique em **OK**e feche a janela do **Editor de objeto de política de grupo** . Quando a política de grupo é atualizada, a conexão do servidor do AGPM é configurada para cada administrador de política de grupo.

### <a href="" id="bkmk-config4"></a>Etapa 4: configurar a notificação por email

Como administrador do AGPM (controle total), você designa os endereços de email de aprovadores e administradores do AGPM para quem uma mensagem de email contendo uma solicitação é enviada quando um editor tenta criar, implantar ou excluir um GPO. Você também pode determinar o alias do qual essas mensagens são enviadas.

**Para configurar a notificação por email para o AGPM**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  No painel de detalhes, clique na guia de **delegação de domínio** .

3.  No campo **de** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.

4.  No campo **para** , digite o endereço de email da conta de usuário à qual você pretende atribuir a função de aprovador.

5.  No campo **servidor SMTP** , digite um servidor de email SMTP válido.

6.  Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.

7.  Clique em **Aplicar**.

### <a href="" id="bkmk-config5"></a>Etapa 5: delegar acesso

Como administrador do AGPM (controle total), você delega o acesso no nível do domínio aos GPOs, atribuindo funções à conta de cada administrador de política de grupo.

**Observação**  Você também pode delegar o acesso no nível do GPO em vez do nível do domínio. Para obter detalhes, consulte ajuda para gerenciamento avançado de política de grupo.

 

**Importante**  Você deve restringir a participação no grupo proprietários criadores de política de grupo, portanto, não pode ser usado para burlar o gerenciamento de AGPM do acesso a GPOs. (No **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio dos quais você deseja gerenciar GPOs, clique em **delegação**e, em seguida, defina as configurações para atender às necessidades da sua organização.)

 

**Para delegar o acesso a todos os GPOs em um domínio**

1.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

2.  Na guia **delegação de domínio** , clique no botão **avançado** .

3.  Na caixa de diálogo **permissões** :

    1.  Clique na conta de usuário de um administrador de política de grupo e marque a caixa de seleção **Aprovador** para atribuir essa função à conta. Desmarque a caixa de seleção **Editor** . (Essa função inclui a função de revisor.)

    2.  Clique na conta de usuário de outro administrador de política de grupo e, em seguida, marque a caixa de seleção **Editor** para atribuir essa função à conta. (Essa função inclui a função de revisor.)

    3.  Clique em uma terceira conta e marque a caixa **de seleção revisor para** atribuir apenas a função de revisor à conta desse administrador de política de grupo. Desmarque a caixa de seleção **Editor** .

    4.  Clique no botão **avançado** .

4.  Na caixa de diálogo **configurações de segurança avançadas** :

    1.  Selecione um administrador de política de grupo e, em seguida, clique em **Editar**.

    2.  Em **aplicar**em, selecione **este objeto e objetos aninhados**e, em seguida, clique em **OK** na caixa de diálogo **entrada** de **permissão** .

    3.  Repita para cada administrador de política de grupo.

5.  Na caixa de diálogo **configurações de segurança avançadas** , clique em **OK**.

6.  Na caixa de diálogo **permissões** , clique em **OK**.

## Etapas para gerenciar GPOs


Você deve completar as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM. Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.

[Etapa 1: criar um GPO](#bkmk-manage1)

[Etapa 2: editar um GPO](#bkmk-manage2)

[Etapa 3: revisar e implantar um GPO](#bkmk-manage3)

[Etapa 4: usar um modelo para criar um GPO](#bkmk-manage4)

[Etapa 5: excluir e restaurar um GPO](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a>Etapa 1: criar um GPO

Em um ambiente com vários administradores de política de grupo, aqueles com a função editor têm a capacidade de solicitar a criação de novos GPOs, mas essa solicitação deve ser aprovada por alguém com a função de aprovador porque a criação de um novo GPO impacta o ambiente de produção.

Nesta etapa, você usa uma conta com a função de editor para solicitar a criação de um novo GPO. Usando uma conta com a função Aprovador, você aprova essa solicitação e conclui a criação de um GPO.

**Para solicitar a criação de um novo GPO gerenciado por meio do AGPM**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de editor no AGPM.

2.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

3.  Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.

4.  Na caixa de diálogo **novo GPO controlado** :

    1.  Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .

    2.  Digite **MyGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique em **criar ao vivo** para que o novo GPO seja implantado para o ambiente de produção imediatamente após a aprovação.

    5.  Clique em **Enviar**.

5.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O novo GPO será exibido na guia **pendente** .

**Para aprovar a solicitação pendente para criar um GPO**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM.

2.  Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com a solicitação do editor para criar um GPO.

3.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

4.  Na guia **conteúdo** , clique na guia **pendente** para exibir os GPOs pendentes.

5.  Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **aprovar**.

6.  Clique em **Sim** para confirmar a aprovação da criação do GPO. O GPO será movido para a guia **controlado** .

### <a href="" id="bkmk-manage2"></a>Etapa 2: editar um GPO

Você pode usar GPOs para configurar o computador ou o usuário e implantá-los em muitos computadores ou usuários. Nesta etapa, você usa uma conta com a função de editor para fazer check-out de um GPO do arquivo, editar o GPO offline, verificar o GPO editado no arquivo morto e solicitar a implantação do GPO ao ambiente de produção. Nesse cenário, você define uma configuração no GPO para exigir que a senha tenha pelo menos oito caracteres de comprimento.

**Para fazer check-out do GPO do arquivo para edição**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.

2.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

3.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e clique em **check-out**.

5.  Digite um comentário a ser exibido no **histórico** do GPO durante o check-out e, em seguida, clique em **OK**.

6.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.

**Para editar o GPO offline e configurar o tamanho mínimo da senha**

1.  Na guia **controlado** , clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de objeto de política de grupo** e fazer alterações em uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **configuração do computador**, clique duas vezes em **configurações do Windows**, clique duas vezes em **configurações de segurança**, clique duas vezes em políticas de **conta**e clique duas vezes em **política de senha**.

    2.  No painel de detalhes, clique duas vezes em **tamanho mínimo da senha**.

    3.  Na janela Propriedades, marque a caixa de seleção **definir esta configuração de política** , defina o número de caracteres para **8**e, em seguida, clique em **OK**.

2.  Feche a janela do **Editor de objeto de política de grupo** .

**Para verificar o GPO no arquivo morto**

1.  Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **check-in**.

2.  Digite um comentário e, em seguida, clique em **OK**.

3.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO é identificado como **checked-in**.

**Para solicitar a implantação do GPO ao ambiente de produção**

1.  Na guia **controlado** , clique com o botão direito do mouse em **MyGPO** e clique em **implantar**.

2.  Como essa conta não é um Aprovador ou administrador do AGPM, você deve enviar uma solicitação de implantação. Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** . Digite um comentário a ser exibido no **histórico** do GPO e, em seguida, clique em **Enviar**.

3.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. **MyGPO** é exibido na lista de GPOs na guia **pendente** .

### <a href="" id="bkmk-manage3"></a>Etapa 3: revisar e implantar um GPO

Nesta etapa, você atua como Aprovador, criando relatórios e analisando as configurações e alterando as configurações no GPO para determinar se devem ser aprovadas. Depois de avaliar o GPO, implante-o no ambiente de produção e vincule-o a um domínio ou a uma UO (unidade organizacional) para que ele tenha efeito quando a política de grupo for atualizada para computadores nesse domínio ou unidade organizacional.

**Para revisar as configurações no GPO**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída à função de aprovador no AGPM. (Qualquer administrador de política de grupo com a função revisor, que está incluído em todas as outras funções, pode revisar as configurações em um GPO.)

2.  Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias do AGPM com uma solicitação de editor para implantar um GPO.

3.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

4.  Na guia **conteúdo** do painel detalhes, clique na guia **pendente** .

5.  Clique duas vezes em **MyGPO** para exibir seu histórico.

6.  Examine as configurações na versão mais recente do MyGPO:

    1.  Na janela do **histórico** , clique com o botão direito do mouse na versão do GPO com o carimbo de data e hora mais recente, clique em **configurações**e, em seguida, clique em **relatório HTML** para exibir um resumo das configurações do GPO.

    2.  No navegador da Web, clique em **Mostrar tudo** para exibir todas as configurações no GPO.

    3.  Feche a janela do navegador.

7.  Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:

    1.  Na janela do **histórico** , clique na versão do GPO com o carimbo de data e hora mais recente. Pressione **Ctrl** e clique na versão mais antiga do GPO que tem o estado **check-in**.

    2.  Clique no botão **diferenças** . A seção **políticas de conta/política de senha** é realçada em verde e precedida por **\ [+ \]**, indicando que essa configuração é definida somente na versão mais recente do GPO.

    3.  Clique em **políticas de conta/política de senha**. A configuração **comprimento mínimo da senha** também é realçada em verde e precedida por **\ [+ \]**, indicando que ela está configurada somente na última versão do GPO.

    4.  Fechar o navegador da Web.

**Para implantar o GPO no ambiente de produção**

1.  Na guia **pendente** , clique com o botão direito do mouse em **MyGPO** e, em seguida, clique em **aprovar**.

2.  Digite um comentário para incluir no histórico do GPO.

3.  Clique em **Sim**. Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é implantado no ambiente de produção.

**Para vincular o GPO a um domínio ou unidade organizacional**

1.  No GPMC, clique com o botão direito do mouse no domínio ou em uma UO à qual deseja aplicar o GPO que você configurou e clique em **vincular um GPO existente**.

2.  Na caixa de diálogo **selecionar GPO** , clique em **MyGPO**e, em seguida, clique em **OK**.

### <a href="" id="bkmk-manage4"></a>Etapa 4: usar um modelo para criar um GPO

Nesta etapa, você usa uma conta com a função de editor para criar um modelo, uma versão estática e não editável de um GPO para uso como ponto de partida para a criação de novos GPOs e, em seguida, cria um novo GPO com base nesse modelo. Os modelos são úteis para criar rapidamente vários GPOs que incluam muitas das mesmas configurações.

**Para criar um modelo com base em um GPO existente**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.

2.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

3.  Na guia **conteúdo** do painel detalhes, clique na guia **controlado** .

4.  Clique com o botão direito do mouse em **MyGPO**e clique em **salvar como modelo** para criar um modelo que incorpora todas as configurações no MyGPO.

5.  Digite **MyTemplate** como o nome do modelo e um comentário e, em seguida, clique em **OK**.

6.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O novo modelo aparece na guia **modelos** .

**Para solicitar a criação de um novo GPO gerenciado por meio do AGPM**

1.  Clique na guia **controlado** .

2.  Clique com o botão direito do mouse no nó de **controle de alterações** e clique em **novo GPO controlado**.

3.  Na caixa de diálogo **novo GPO controlado** :

    1.  Para receber uma cópia da solicitação, digite o seu endereço de email no campo **CC** .

    2.  Digite **MyOtherGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique em **criar ao vivo**, portanto, o novo GPO será implantado para o ambiente de produção imediatamente após a aprovação.

    5.  Em **modelo de GPO**, selecione **MyTemplate**.

    6.  Clique em **Enviar**.

4.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O novo GPO será exibido na guia **pendente** .

Use uma conta que tenha sido atribuída à função de aprovador para aprovar a solicitação pendente para criar o GPO da mesma forma que você fez na [etapa 1: criar um GPO](#bkmk-manage1). MyTemplate incorpora todas as configurações que você configurou no MyGPO. Como o MyOtherGPO foi criado usando MyTemplate, inicialmente ele contém todas as configurações que MyGPO contidas no momento em que MyTemplate foi criado. Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO ao MyTemplate.

**Para fazer check-out do GPO do arquivo para edição**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de editor no AGPM.

2.  Clique com o botão direito do mouse em **MyOtherGPO**e clique em **check-out**.

3.  Digite um comentário a ser exibido no histórico do GPO durante o check-out e, em seguida, clique em **OK**.

4.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. Na guia **controlado** , o estado do GPO é identificado como Checked- **out**.

**Para editar o GPO offline e configurar a duração do bloqueio de conta**

1.  Na guia **controlado** , clique com o botão direito do mouse em **MyOtherGPO**e, em seguida, clique em **Editar** para abrir a janela do **Editor de objeto de política de grupo** e fazer alterações em uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **configuração do computador**, clique duas vezes em **configurações do Windows**, clique duas vezes em **configurações de segurança**, clique duas vezes em políticas de **conta**e clique duas vezes em política de **bloqueio de conta**.

    2.  No painel de detalhes, clique duas vezes em **duração do bloqueio de conta**.

    3.  Na janela Propriedades, marque **definir esta configuração de política**, defina a duração como **30** minutos e clique em **OK**.

2.  Feche a janela do **Editor de objeto de política de grupo** .

Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [etapa 2: editar um GPO](#bkmk-manage2). Você pode comparar o MyOtherGPO ao MyGPO ou ao MyTemplate usando relatórios de diferença. Qualquer conta que inclua a função de Revisor (administrador do AGPM \ [controle total \], Aprovador, editor ou revisor) pode gerar relatórios.

**Para comparar um GPO a outro GPO e a um modelo**

1.  Para comparar o MyGPO e o MyOtherGPO:

    1.  Na guia **controlado** , clique em **MyGPO**. Pressione **Ctrl** e clique em **MyOtherGPO**.

    2.  Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **relatório HTML**.

2.  Para comparar MyOtherGPO e MyTemplate:

    1.  Na guia **controlado** , clique em **MyOtherGPO**.

    2.  Clique com o botão direito do mouse em **MyOtherGPO**, aponte para **diferenças**e clique em **modelo**.

    3.  Selecione meu **modelo** e **relatório HTML**e, em seguida, clique em **OK**.

### <a href="" id="bkmk-manage5"></a>Etapa 5: excluir e restaurar um GPO

Nesta etapa, você atua como um Aprovador para excluir um GPO.

**Para excluir um GPO**

1.  Em um computador no qual você instalou o cliente do AGPM, faça logon com uma conta de usuário que tenha atribuído a função de aprovador.

2.  Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.

3.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e, em seguida, clique em **excluir**. Clique em **excluir GPO do arquivo e da produção** para excluir a versão no arquivo e a versão implantada do GPO no ambiente de produção.

5.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

6.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO é removido da guia **controlado** e é exibido na guia **Lixeira** , onde ele pode ser restaurado ou destruído.

Às vezes, você pode descobrir depois de excluir um GPO que ainda é necessário. Nesta etapa, você atua como um Aprovador para restaurar um GPO que foi excluído.

**Para restaurar um GPO excluído**

1.  Na guia **conteúdo** , clique na guia da **Lixeira** para exibir os GPOs excluídos.

2.  Clique com o botão direito do mouse em **MyGPO**e clique em **restaurar**.

3.  Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.

4.  Quando a janela de **progresso do AGPM** indicar que o progresso geral foi concluído, clique em **fechar**. O GPO será removido da guia **Lixeira** e será exibido na guia **controlado** .

    **Observação**  Restaurar um GPO para o arquivo não o reimplanta automaticamente no ambiente de produção. Para retornar o GPO ao ambiente de produção, implante o GPO da [etapa 3: revise e implante um GPO](#bkmk-manage3).

     

Depois de editar e implantar um GPO, você pode descobrir que alterações recentes no GPO estão causando um problema. Nesta etapa, você atua como um Aprovador para reverter para uma versão anterior do GPO. Você pode reverter para qualquer versão do histórico do GPO. Você pode usar comentários e rótulos para identificar versões válidas conhecidas e quando foram feitas alterações específicas.

**Para reverter para uma versão anterior de um GPO**

1.  Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.

2.  Clique duas vezes em **MyGPO** para exibir seu histórico.

3.  Clique com o botão direito do mouse na versão a ser implantada, clique em **implantar**e, em seguida, clique em **Sim**.

4.  Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**. Na janela do **histórico** , clique em **fechar**.

    **Observação**  Para verificar se a versão que foi reimplementada é a versão pretendida, examine um relatório de diferença para as duas versões. Na janela do **histórico** do GPO, selecione as duas versões, clique com o botão direito do mouse nelas, aponte para **diferença**e clique em **relatório HTML** ou **relatório XML**.

     

 

 





