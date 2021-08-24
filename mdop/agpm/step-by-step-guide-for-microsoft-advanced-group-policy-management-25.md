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
ms.openlocfilehash: 4b63406442cd3560266bb9c05c5deb384f141104
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910676"
---
# <a name="step-by-step-guide-for-microsoft-advanced-group-policy-management-25"></a>Guia passo a passo do Gerenciamento Avançado de Política de Grupo 2.5 da Microsoft


Este guia passo a passo demonstra técnicas avançadas para gerenciamento de Política de Grupo usando o Console de Gerenciamento de Política de Grupo (GPMC) e o AgPM (Gerenciamento Avançado de Política de Grupo) da Microsoft. O AGPM aumenta os recursos do GPMC, fornecendo:

-   Funções padrão para delegação de permissões para gerenciar objetos de Política de Grupo (GPOs) para vários administradores de Política de Grupo.

-   Um arquivo morto para permitir que os administradores de Política de Grupo criem e modifiquem GPOs offline antes de implantá-los em um ambiente de produção.

-   A capacidade de reverter para qualquer versão anterior de um GPO.

-   Recurso de check-in/check-out para GPOs para garantir que os administradores de Política de Grupo não sobrescrevem inadvertidamente o trabalho uns dos outros.

## <a name="agpm-scenario-overview"></a>Visão geral do cenário AGPM


Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a Política de Grupo pode ser gerenciada em um ambiente com vários administradores de Política de Grupo com níveis diferentes de permissões. Especificamente, você executará as seguintes tarefas:

-   Usando uma conta que seja membro do grupo Administradores de Domínio, instale o SERVIDOR AGPM e atribua a função de Administrador AGPM a uma conta ou grupo.

-   Usando contas às quais você atribuirá funções AGPM, instale o Cliente AGPM.

-   Usando uma conta com a função administrador agpm, configure AGPM e delegar acesso a GPOs atribuindo funções a outras contas.

-   Usando uma conta com a função Editor, solicite a criação de um GPO, que você aprovará usando uma conta com a função Aprovador. Com a conta editor, verifique o GPO fora do arquivo morto, edite o GPO, verifique o GPO no arquivo morto e solicite a implantação.

-   Usando uma conta com a função Aprovador, revise o GPO e implante-o em seu ambiente de produção.

-   Usando uma conta com a função Editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.

-   Usando uma conta com a função Aprovador, exclua e restaure um GPO.

![processo de desenvolvimento de objeto de política de grupo.](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <a name="requirements"></a>Requisitos


Os computadores nos quais você deseja instalar o AGPM devem atender aos seguintes requisitos e você deve criar contas para uso neste cenário.

### <a name="agpm-server-requirements"></a>Requisitos do Servidor AGPM

O AGPM Server 2.5 requer Windows Vista® (versão de 32 bits) sem service packs instalados ou Windows Server® 2003 (versão de 32 bits), bem como o GPMC. Além disso, você deve ser membro do grupo Administradores de Domínio para instalar o SERVIDOR AGPM.

Você deve instalar o SERVIDOR AGPM em um servidor membro ou controlador de domínio com a versão mais recente do GPMC disponível para você e com suporte do AGPM. O AGPM usa o GPMC para fazer backup e restaurar GPOs, e versões mais recentes do GPMC fornecem configurações de política adicionais não disponíveis nas versões anteriores. Se a versão do GPMC no servidor AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a Política de Grupo, o SERVIDOR AGPM não poderá armazenar essas configurações de política não disponíveis na versão mais antiga do GPMC.

Especificamente, se o servidor AGPM estiver executando o Windows Server 2003 e a versão do GPMC que o acompanhava, e os computadores dos administradores da Política de Grupo estão executando o Windows Vista e a versão do GPMC que o acompanha, você ainda poderá gerenciar a maioria das configurações de política. No entanto, as configurações de política do GPMC no Windows Vista que não estão disponíveis no GPMC no Windows Server 2003, como as relacionadas ao redirecionamento de pasta, rede sem fio (IEEE 802.11) e impressoras implantadas, não podem ser armazenadas pelo Servidor AGPM, mesmo que os administradores possam configurá-los usando o AGPM em seus computadores.

Se você deve instalar o SERVIDOR AGPM em um computador com uma versão mais antiga do GPMC do que os administradores da Política de Grupo em execução, consulte a Referência de Política de Grupo Configurações para obter detalhes sobre quais configurações de política estão disponíveis com quais sistemas operacionais. Para baixar a Referência Configurações Política de Grupo, consulte <https://go.microsoft.com/fwlink/?LinkID=106147> .

**Observação**  
Os arquivos não podem ser migrados de um Servidor AGPM ou de um Servidor GPOVault executando o Windows Server 2003 para um Servidor AGPM executando o Windows Vista.

Para o Windows Server 2003, se o GPOVault Server estiver instalado no computador no qual você deseja instalar o AGPM Server, é recomendável que você não desinstale o GPOVault Server antes de iniciar a instalação. A instalação do SERVIDOR AGPM desinstalará o GPOVault Server e transferirá automaticamente seus dados de arquivo morto GPOVault existentes para um arquivo morto AGPM.

 

### <a name="agpm-client-requirements"></a>Requisitos do cliente AGPM

O Cliente AGPM 2.5 requer Windows Vista (versão de 32 bits) sem service packs instalados ou Windows Server 2003 (versão de 32 bits), bem como o GPMC. O cliente AGPM pode ser instalado em um computador que executa o SERVIDOR AGPM.

### <a name="scenario-requirements"></a>Requisitos de cenário

Antes de começar esse cenário, crie quatro contas de usuário. Durante o cenário, você atribuirá uma das seguintes funções AGPM a cada uma dessas contas: Administrador AGPM (Controle Total), Aprovador, Editor e Revistor. Essas contas devem ser capazes de enviar e receber mensagens de email. Atribua **permissão de GPOs de** link às contas com as funções Administrador, Aprovador e Editor do AGPM (opcionalmente).

**Observação**  
**A permissão de GPOs** de link é atribuída a membros dos Administradores de Domínio e Enterprise Administradores por padrão. Para atribuir permissão **de GPOs** de link a usuários ou grupos adicionais (como contas com as funções **** de Administrador agpm ou aprovador), clique no nó do domínio e clique na guia Delegação, selecione **Vincular GPOs**, clique em **Adicionar**e selecione usuários ou grupos aos quais atribuir a permissão.

 

Para esse cenário, você executa ações com contas diferentes. Você pode fazer logon com cada conta conforme indicado ou usar o comando **Executar** como para iniciar o GPMC com a conta indicada.

**Observação**  
Para usar o comando **Executar como** com GPMC no Windows Server 2003, clique em Iniciar **,** aponte para **Ferramentas**Administrativas, clique com o botão direito do mouse em Gerenciamento de Política de Grupo **e**clique em **Executar como**. Clique **no usuário a seguir** e insira credenciais para uma conta.

Para usar o comando **Executar** como com GPMC no **** Windows Vista, clique no botão Iniciar, aponte para Executar **e**digite **runas /user:** <em> DomainName\\UserName </em> **"mmc %windir%\\system32\\gpmc.msc"** e clique em **OK**. Digite a senha da conta quando solicitado.

 

## <a name="steps-for-installing-and-configuring-agpm"></a>Etapas para instalar e configurar o AGPM


Você deve concluir as etapas a seguir para instalar e configurar o AGPM.

[Etapa 1: Instalar o SERVIDOR AGPM](#bkmk-config1)

[Etapa 2: Instalar o cliente AGPM](#bkmk-config2)

[Etapa 3: Configurar uma conexão do Servidor AGPM](#bkmk-config3)

[Etapa 4: Configurar a notificação de email](#bkmk-config4)

[Etapa 5: Acesso delegado](#bkmk-config5)

### <a name="step-1-install-agpm-server"></a><a href="" id="bkmk-config1"></a>Etapa 1: Instalar o SERVIDOR AGPM

Nesta etapa, instale o SERVIDOR AGPM no servidor membro ou controlador de domínio que executará o Serviço AGPM e configure o arquivo morto. Todas as operações do AGPM são gerenciadas por meio Windows serviço e são executadas com as credenciais do serviço. O arquivo morto gerenciado por um Servidor AGPM pode ser hospedado nesse servidor ou em outro servidor na mesma floresta.

**Para instalar o SERVIDOR AGPM no computador que hospedará o Serviço AGPM**

1.  Faça logoff com uma conta que seja membro do grupo Administradores de Domínio.

2.  Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar Gerenciamento Avançado de Política **de Grupo - Servidor**.

3.  Na caixa **de diálogo** Bem-vindo, clique em **Próximo**.

4.  Na caixa de diálogo Termos de Licença de Software da **Microsoft,** aceite os termos e clique em **Próximo**.

5.  Na caixa **de diálogo Caminho do** Aplicativo, selecione um local no qual instalar o SERVIDOR AGPM. O computador no qual o SERVIDOR AGPM está instalado hospedará o Serviço AGPM e gerenciará o arquivo morto. Clique em **Avançar**.

6.  Na caixa **de diálogo Caminho do** Arquivo Morto, selecione um local para o arquivo morto em relação ao Servidor AGPM. O caminho do arquivo morto pode apontar para uma pasta no Servidor AGPM ou em outro lugar, mas você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por este SERVIDOR AGPM. Clique em **Avançar**.

7.  Na caixa de diálogo Conta de **Serviço AGPM,** selecione uma conta de serviço na qual o Serviço AGPM será executado e clique em **Próximo**.

8.  Na caixa **de diálogo Proprietário** do Arquivo Morto, selecione uma conta ou grupo ao qual atribuir inicialmente a função administrador agpm (Controle Total). Esse administrador agpm pode atribuir funções e permissões AGPM a outros administradores de Política de Grupo (incluindo a função de Administrador AGPM). Para esse cenário, selecione a conta a ser acionável na função administrador agpm. Clique em **Avançar**.

9.  Clique **em Instalar**e clique em Concluir **para** sair do Assistente de Instalação.

    **Cuidado**  
    Não modifique as configurações do Serviço AGPM por meio **de Ferramentas Administrativas** e **Serviços** no sistema operacional. Isso pode impedir o início do Serviço AGPM. Para obter informações sobre como modificar configurações para o serviço, consulte Ajuda para Gerenciamento Avançado de Política de Grupo.

     

### <a name="step-2-install-agpm-client"></a><a href="" id="bkmk-config2"></a>Etapa 2: Instalar o cliente AGPM

Cada administrador de Política de Grupo, qualquer pessoa que crie, edite, implante, revise ou exclua GPOs, deve ter o Cliente AGPM instalado em computadores que eles usam para gerenciar GPOs. Para esse cenário, você instala o Cliente AGPM em pelo menos um computador. Você não precisa instalar o Cliente AGPM nos computadores dos usuários finais que não executam a administração da Política de Grupo.

**Para instalar o Cliente AGPM no computador de um administrador de Política de Grupo**

1.  Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar Gerenciamento Avançado de Política **de Grupo - Cliente**.

2.  Na caixa **de diálogo** Bem-vindo, clique em **Próximo**.

3.  Na caixa de diálogo Termos de Licença de Software da **Microsoft,** aceite os termos e clique em **Próximo**.

4.  Na caixa **de diálogo Caminho do** Aplicativo, selecione um local no qual instalar o Cliente AGPM. Clique em **Avançar**.

5.  Na caixa **de diálogo Servidor AGPM,** digite o nome do computador totalmente qualificado e a porta para o Servidor AGPM ao qual se conectar. A porta padrão para o Serviço AGPM é 4600. Clique em **Avançar**.

6.  Clique **em Instalar**e clique em Concluir **para** sair do Assistente de Instalação.

### <a name="step-3-configure-an-agpm-server-connection"></a><a href="" id="bkmk-config3"></a>Etapa 3: Configurar uma conexão do Servidor AGPM

O AGPM armazena todas as versões de cada objeto gpo (GPO) controlado — um GPO para o qual o AGPM fornece controle de alteração — em um arquivo morto central, para que os administradores de Política de Grupo possam exibir e modificar GPOs offline sem afetar imediatamente a versão implantada de cada GPO.

Nesta etapa, você configura uma conexão do SERVIDOR AGPM e garante que todos os administradores de Política de Grupo se conectem ao mesmo Servidor AGPM. (Para obter informações sobre a configuração de vários servidores AGPM, consulte Ajuda para Gerenciamento Avançado de Política de Grupo.)

**Para configurar uma conexão do SERVIDOR AGPM para todos os administradores de Política de Grupo**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com a conta de usuário selecionada como o Proprietário do Arquivo Morto. Esse usuário tem a função de Administrador AGPM (Controle Total).

2.  Clique **em Iniciar**, aponte para Ferramentas **Administrativas**e clique em Gerenciamento de Política de **Grupo** para abrir o Console de Gerenciamento de Política de **Grupo (GPMC).**

3.  Na árvore Console de Gerenciamento de Política de **Grupo,** edite um GPO aplicado a todos os administradores de Política de Grupo.

4.  Na janela Editor de Objeto de Política de **Grupo,** clique em Configuração do **Usuário,** **Modelos Administrativos** **e Windows Componentes**.

5.  Se **o AGPM** não estiver listado em **Windows Componentes**:

    1.  Clique com o botão direito do mouse **em Modelos Administrativos** e selecione **Adicionar/Remover Modelos.**

    2.  Clique **em Adicionar**, selecione **agpm.admx** ou **agpm.adm,** clique em **Abrir**e clique em **Fechar**.

6.  Em **Windows Componentes,** clique duas vezes em **AGPM**.

7.  No painel de detalhes, clique duas vezes em **Servidor AGPM (todos os domínios).**

8.  Na janela Propriedades do **Servidor AGPM (todos os domínios),** selecione Habilitado e digite o nome e a porta do computador totalmente qualificados (por exemplo, server.contoso.com:4600) para o servidor que hospeda o arquivo morto. **** A porta usada pelo Serviço AGPM é a porta 4600.

9.  Clique **em OK**e, em seguida, feche a janela Editor de Objeto de Política **de** Grupo. Quando a Política de Grupo é atualizada, a conexão do Servidor AGPM é configurada para cada administrador de Política de Grupo.

### <a name="step-4-configure-e-mail-notification"></a><a href="" id="bkmk-config4"></a>Etapa 4: Configurar a notificação de email

Como administrador agpm (Controle Total), você designa os endereços de email de Aprovadores e Administradores AGPM para os quais uma mensagem de email contendo uma solicitação é enviada quando um Editor tenta criar, implantar ou excluir um GPO. Você também determina o alias do qual essas mensagens são enviadas.

**Para configurar a notificação de email para AGPM**

1.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

2.  No painel de detalhes, clique na guia **Delegação de** Domínio.

3.  No campo **De,** digite o alias de email para AGPM a partir do qual as notificações devem ser enviadas.

4.  No campo **Para,** digite o endereço de email da conta de usuário à qual você pretende atribuir a função Aprovador.

5.  No campo **servidor SMTP,** digite um servidor de email SMTP válido.

6.  Nos campos **Nome de usuário** e **Senha,** digite as credenciais de um usuário com acesso ao serviço SMTP.

7.  Clique em **Aplicar**.

### <a name="step-5-delegate-access"></a><a href="" id="bkmk-config5"></a>Etapa 5: Acesso delegado

Como administrador agpm (Controle Total), você delega acesso no nível de domínio a GPOs, atribuindo funções à conta de cada administrador de Política de Grupo.

**Observação**  
Você também pode delegar o acesso no nível GPO, em vez do nível de domínio. Para obter detalhes, consulte Help for Advanced Group Policy Management.

 

**Importante**  
Você deve restringir a associação ao grupo Proprietários de Criadores de Política de Grupo, portanto, ela não pode ser usada para contornar o gerenciamento AGPM do acesso a GPOs. (No **Console**de Gerenciamento **** de Política de Grupo , clique em Objetos de Política de Grupo na floresta e no domínio no qual você deseja gerenciar GPOs, clique em Delegação **e,** em seguida, configure as configurações para atender às necessidades da sua organização.)

 

**Para delegar o acesso a todos os GPOs em todo um domínio**

1.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

2.  Na guia **Delegação de Domínio,** clique no **botão** Avançado.

3.  Na caixa **de diálogo** Permissões:

    1.  Clique na conta de usuário de um **** administrador de Política de Grupo e marque a caixa de seleção Aprovador para atribuir essa função à conta. Des limpar **a caixa de** seleção Editor. (Essa função inclui a função Revistor.)

    2.  Clique na conta de usuário de outro administrador de Política de Grupo e marque a caixa de seleção **Editor** para atribuir essa função à conta. (Essa função inclui a função Revistor.)

    3.  Clique em uma terceira **** conta e marque a caixa de seleção Revistor para atribuir apenas a função Revistor à conta desse administrador de Política de Grupo. Des limpar **a caixa de** seleção Editor.

    4.  Clique no **botão Avançado.**

4.  Na caixa **de diálogo Segurança Avançada Configurações:**

    1.  Selecione um administrador de Política de Grupo e clique em **Editar**.

    2.  Para **Aplicar em**, selecione Este objeto e objetos **aninhados**e clique em **OK** na caixa de diálogo **Entrada** **de** Permissão.

    3.  Repita para cada administrador de Política de Grupo.

5.  Na caixa **de diálogo Segurança Avançada Configurações,** clique em **OK**.

6.  Na caixa **de diálogo** Permissões, clique em **OK**.

## <a name="steps-for-managing-gpos"></a>Etapas para gerenciar GPOs


Você deve concluir as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM. Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.

[Etapa 1: Criar um GPO](#bkmk-manage1)

[Etapa 2: Editar um GPO](#bkmk-manage2)

[Etapa 3: Revisar e implantar um GPO](#bkmk-manage3)

[Etapa 4: Usar um modelo para criar um GPO](#bkmk-manage4)

[Etapa 5: Excluir e restaurar um GPO](#bkmk-manage5)

### <a name="step-1-create-a-gpo"></a><a href="" id="bkmk-manage1"></a>Etapa 1: Criar um GPO

Em um ambiente com vários administradores de Política de Grupo, aqueles com a função Editor têm a capacidade de solicitar a criação de novos GPOs, mas essa solicitação deve ser aprovada por alguém com a função Aprovador porque a criação de um novo GPO afeta o ambiente de produção.

Nesta etapa, você usa uma conta com a função Editor para solicitar a criação de um novo GPO. Usando uma conta com a função Aprovador, você aprova essa solicitação e conclui a criação de um GPO.

**Para solicitar a criação de um novo GPO gerenciado por meio do AGPM**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Clique com o botão direito do mouse no nó **Alterar Controle** e clique em **Novo GPO Controlado.**

4.  Na caixa **de diálogo Novo GPO** Controlado:

    1.  Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.**

    2.  Digite **MyGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique **em Criar ao vivo** para que o novo GPO seja implantado no ambiente de produção imediatamente após a aprovação.

    5.  Clique em **Enviar**.

5.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo GPO é exibido na **guia Pendente.**

**Para aprovar a solicitação pendente para criar um GPO**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Aprovador no AGPM.

2.  Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias AGPM com a solicitação do Editor para criar um GPO.

3.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

4.  Na guia **Conteúdo,** clique na guia **Pendente** para exibir os GPOs pendentes.

5.  Clique com o botão **direito do mouse em MyGPO**e clique em **Aprovar**.

6.  Clique **em Sim** para confirmar a aprovação da criação do GPO. O GPO é movido para a **guia Controlado.**

### <a name="step-2-edit-a-gpo"></a><a href="" id="bkmk-manage2"></a>Etapa 2: Editar um GPO

Você pode usar GPOs para configurar configurações de computador ou usuário e implantá-las em muitos computadores ou usuários. Nesta etapa, você usa uma conta com a função Editor para verificar um GPO do arquivo morto, editar o GPO offline, verificar o GPO editado no arquivo morto e solicitar a implantação do GPO para o ambiente de produção. Para esse cenário, você configura uma configuração no GPO para exigir que a senha seja pelo menos oito caracteres de comprimento.

**Para verificar o GPO no arquivo morto para edição**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo** no painel de detalhes, clique na guia **Controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e clique **em Check-Out**.

5.  Digite um comentário a ser exibido no **Histórico** do GPO enquanto ele está com check-out e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-out**.

**Para editar o GPO offline e configurar o tamanho mínimo da senha**

1.  Na guia **Controlado,** clique com o botão direito do **** mouse em **MyGPO**e clique em **Editar** para abrir a janela Editor de Objeto de Política de Grupo e fazer alterações em uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **Configuração do**Computador, clique duas vezes em **Windows Configurações,** clique duas vezes em Segurança **Configurações,** clique duas vezes em Políticas de Conta **e**clique duas vezes em Política **de Senha.**

    2.  No painel de detalhes, clique duas vezes em **Tamanho mínimo da senha**.

    3.  Na janela propriedades, marque a caixa de seleção **Definir essa** configuração de política, defina o número de caracteres como **8**e clique em **OK**.

2.  Feche a **janela Editor de Objeto de Política de** Grupo.

**Para verificar o GPO no arquivo morto**

1.  Na guia **Controlado,** clique com o botão direito do mouse **em MyGPO** e clique **em Check-In**.

2.  Digite um comentário e clique em **OK**.

3.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-In**.

**Para solicitar a implantação do GPO para o ambiente de produção**

1.  Na guia **Controlado,** clique com o botão direito do mouse **em MyGPO** e clique em **Implantar**.

2.  Como essa conta não é um Aprovador ou Administrador agpm, você deve enviar uma solicitação de implantação. Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.** Digite um comentário a ser exibido no **Histórico** do GPO e clique em **Enviar**.

3.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. **MyGPO** é exibido na lista de GPOs na **guia Pendente.**

### <a name="step-3-review-and-deploy-a-gpo"></a><a href="" id="bkmk-manage3"></a>Etapa 3: Revisar e implantar um GPO

Nesta etapa, você age como um Aprovador, criando relatórios e analisando as configurações e as alterações nas configurações no GPO para determinar se você deve aprove-los. Depois de avaliar o GPO, você o implanta no ambiente de produção e o vincula a um domínio ou a uma unidade organizacional (UO) para que ela entre em vigor quando a Política de Grupo for atualizada para computadores nesse domínio ou OU.

**Para revisar as configurações no GPO**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Aprovador no AGPM. (Qualquer administrador de Política de Grupo com a função Revistor, que está incluída em todas as outras funções, pode revisar as configurações em um GPO.)

2.  Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias AGPM com uma solicitação do Editor para implantar um GPO.

3.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

4.  Na guia **Conteúdo** no painel de detalhes, clique na **guia Pendente.**

5.  Clique duas vezes **em MyGPO** para exibir seu histórico.

6.  Revise as configurações na versão mais recente do MyGPO:

    1.  Na janela **Histórico,** clique com o botão direito do mouse na versão gpo com o data/hora mais recente, clique em **Configurações**e clique em **Relatório HTML** para exibir um resumo das configurações do GPO.

    2.  No navegador da Web, clique em **mostrar** tudo para exibir todas as configurações no GPO.

    3.  Feche a janela do navegador.

7.  Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:

    1.  Na janela **Histórico,** clique na versão GPO com o data/hora mais recente. Pressione **CTRL** e clique na versão GPO mais antiga que tenha um estado **de Check-In**.

    2.  Clique no **botão Diferenças.** A **seção Políticas de Conta/Política** de Senha é realçada em verde e precedida por **\[+\]**, indicando que essa configuração está configurada somente na última versão do GPO.

    3.  Clique **em Políticas de Conta/Política de Senha.** A **configuração** tamanho mínimo da senha também é realçada em verde e precedida por **\[+\]**, indicando que ela está configurada somente na última versão do GPO.

    4.  Feche o navegador da Web.

**Para implantar o GPO no ambiente de produção**

1.  Na guia **Pendente,** clique com o botão direito do mouse **em MyGPO** e clique em **Aprovar**.

2.  Digite um comentário para incluir no histórico do GPO.

3.  Clique em **Sim**. Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O GPO é implantado no ambiente de produção.

**Para vincular o GPO a um domínio ou unidade organizacional**

1.  No GPMC, clique com o botão direito do mouse no domínio ou em uma UO para aplicar o GPO que você configurou e clique em Vincular um **GPO Existente**.

2.  Na caixa **de diálogo Selecionar GPO,** clique **em MyGPO**e clique em **OK**.

### <a name="step-4-use-a-template-to-create-a-gpo"></a><a href="" id="bkmk-manage4"></a>Etapa 4: Usar um modelo para criar um GPO

Nesta etapa, você usa uma conta com a função Editor para criar um modelo , uma versão estática e inediável de um GPO para uso como ponto de partida para a criação de novos GPOs e, em seguida, criar um novo GPO com base nesse modelo. Os modelos são úteis para criar rapidamente vários GPOs que incluem muitas das mesmas configurações.

**Para criar um modelo com base em um GPO existente**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo** no painel de detalhes, clique na **guia Controlado.**

4.  Clique com o botão direito do mouse em **MyGPO**e clique em Salvar como **Modelo** para criar um modelo incorporando todas as configurações atualmente no MyGPO.

5.  Digite **MyTemplate** como o nome do modelo e um comentário e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo modelo aparece na guia **Modelos.**

**Para solicitar a criação de um novo GPO gerenciado por meio do AGPM**

1.  Clique na **guia Controlado.**

2.  Clique com o botão direito do mouse no nó **Alterar Controle** e clique em **Novo GPO Controlado.**

3.  Na caixa **de diálogo Novo GPO** Controlado:

    1.  Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.**

    2.  Digite **MyOtherGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique **em Criar ao**vivo , para que o novo GPO seja implantado no ambiente de produção imediatamente após a aprovação.

    5.  For **From GPO template**, select **MyTemplate**.

    6.  Clique em **Enviar**.

4.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo GPO é exibido na **guia Pendente.**

Use uma conta atribuída à função de Aprovador para aprovar a solicitação pendente para criar o GPO como você fez na Etapa [1: Criar um GPO](#bkmk-manage1). MyTemplate incorpora todas as configurações que você configurou no MyGPO. Como MyOtherGPO foi criado usando MyTemplate, ele contém inicialmente todas as configurações que o MyGPO continha no momento em que MyTemplate foi criado. Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO com MyTemplate.

**Para verificar o GPO no arquivo morto para edição**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Editor no AGPM.

2.  Clique com o botão **direito do mouse em MyOtherGPO**e clique em **Check-Out**.

3.  Digite um comentário a ser exibido no histórico do GPO durante o check-out e clique em **OK**.

4.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-out**.

**Para editar o GPO offline e configurar a duração do bloqueio da conta**

1.  Na guia **** **Controlado,** clique com o botão direito do mouse em **MyOtherGPO**e clique em **Editar** para abrir a janela Editor de Objeto de Política de Grupo e fazer alterações em uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **Configuração do**Computador, clique duas **Windows Configurações,** clique duas vezes em Segurança **Configurações,** clique duas vezes em Políticas de Conta **e**clique duas vezes em Política de Bloqueio **de Conta.**

    2.  No painel de detalhes, clique duas vezes em **Duração do bloqueio da conta.**

    3.  Na janela propriedades, marque Definir essa configuração de **política,** defina a duração como **30** minutos e clique em **OK**.

2.  Feche a **janela Editor de Objeto de Política de** Grupo.

Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [Etapa 2: Editar um GPO](#bkmk-manage2). Você pode comparar MyOtherGPO com MyGPO ou MyTemplate usando relatórios de diferença. Qualquer conta que inclua a função Revistor (Administrador DO AGPM \[Controle Total\], Aprovador, Editor ou Revistor) pode gerar relatórios.

**Para comparar um GPO a outro GPO e a um modelo**

1.  Para comparar MyGPO e MyOtherGPO:

    1.  Na guia **Controlado,** clique em **MyGPO**. Pressione **CTRL** e clique em **MyOtherGPO**.

    2.  Clique com o botão direito do **mouse em MyOtherGPO,** aponte para **Diferenças**e clique em **Relatório HTML**.

2.  Para comparar MyOtherGPO e MyTemplate:

    1.  Na guia **Controlado,** clique **em MyOtherGPO**.

    2.  Clique com o botão **direito do mouse em MyOtherGPO,** aponte para **Diferenças**e clique em **Modelo**.

    3.  Selecione **MyTemplate** e **RELATÓRIO HTML**e clique em **OK**.

### <a name="step-5-delete-and-restore-a-gpo"></a><a href="" id="bkmk-manage5"></a>Etapa 5: Excluir e restaurar um GPO

Nesta etapa, você age como um Aprovador para excluir um GPO.

**Para excluir um GPO**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha sido atribuída a função de Aprovador.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo,** clique na guia **Controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e clique em **Excluir**. Clique **em Excluir GPO** do arquivo morto e da produção para excluir a versão no arquivo morto, bem como a versão implantada do GPO no ambiente de produção.

5.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O GPO é removido da guia **Controlado** **** e é exibido na guia Lixeira, onde pode ser restaurado ou destruído.

Ocasionalmente, você pode descobrir após excluir um GPO de que ele ainda é necessário. Nesta etapa, você age como um Aprovador para restaurar um GPO que foi excluído.

**Para restaurar um GPO excluído**

1.  Na guia **Conteúdo,** clique na guia **Lixeira** para exibir GPOs excluídos.

2.  Clique com o botão direito do mouse em **MyGPO**e clique em **Restaurar**.

3.  Digite um comentário a ser exibido no histórico do GPO e clique em **OK**.

4.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O GPO é removido da guia **Lixeira** e é exibido na **guia Controlado.**

    **Observação**  
    Restaurar um GPO para o arquivo morto não o reimplanta automaticamente para o ambiente de produção. Para retornar o GPO ao ambiente de produção, implante o GPO como na [Etapa 3: Revisar e implantar um GPO](#bkmk-manage3).

     

Depois de editar e implantar um GPO, você pode descobrir que alterações recentes no GPO estão causando um problema. Nesta etapa, você age como um Aprovador para reverter para uma versão anterior do GPO. Você pode reverter para qualquer versão no histórico do GPO. Você pode usar comentários e rótulos para identificar versões boas conhecidas e quando alterações específicas foram feitas.

**Para reverter para uma versão anterior de um GPO**

1.  Na guia **Conteúdo,** clique na guia **Controlado** para exibir os GPOs controlados.

2.  Clique duas vezes **em MyGPO** para exibir seu histórico.

3.  Clique com o botão direito do mouse na versão a ser implantada, clique em **Implantar**e clique em **Sim**.

4.  Quando a **janela Progresso** indicar que o progresso geral está concluído, clique em **Fechar**. Na janela **Histórico,** clique em **Fechar**.

    **Observação**  
    Para verificar se a versão que foi reimplantada é a versão pretendida, examine um relatório de diferença para as duas versões. Na janela **Histórico** do GPO, selecione as duas versões, clique com o botão direito do mouse neles, aponte para **Diferença**e clique em Relatório **HTML** ou **Relatório XML.**

     

 

 





