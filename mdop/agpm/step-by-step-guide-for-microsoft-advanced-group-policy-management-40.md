---
title: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
description: Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 567f9a8b14bc05a226b93947e6311ea93c0bf3b2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910706"
---
# <a name="step-by-step-guide-for-microsoft-advanced-group-policy-management-40"></a>Guia passo a passo do Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft


Este guia passo a passo demonstra técnicas avançadas para gerenciamento de Política de Grupo que usam o Console de Gerenciamento de Política de Grupo (GPMC) e o AgPM (Gerenciamento Avançado de Política de Grupo) da Microsoft. O AGPM aumenta os recursos do GPMC, fornecendo:

-   Funções padrão para delegação de permissões para gerenciar GPOs (Objetos de Política de Grupo) para vários administradores de Política de Grupo, além da capacidade de delegar o acesso a GPOs no ambiente de produção.

-   Um arquivo morto para permitir que os administradores de Política de Grupo criem e modifiquem GPOs offline antes que os GPOs sejam implantados em um ambiente de produção.

-   A capacidade de reverter para qualquer versão anterior de um GPO no arquivo morto e limitar o número de versões armazenadas no arquivo morto.

-   Recurso de check-in e check-out para GPOs para garantir que os administradores da Política de Grupo não sobrescrevem o trabalho uns dos outros.

-   A capacidade de pesquisar GPOs com atributos específicos e filtrar a lista de GPOs exibidos.

## <a name="agpm-scenario-overview"></a>Visão geral do cenário AGPM


Para esse cenário, você usará uma conta de usuário separada para cada função no AGPM para demonstrar como a Política de Grupo pode ser gerenciada em um ambiente que tenha vários administradores de Política de Grupo com diferentes níveis de permissões. Especificamente, você executará as seguintes tarefas:

-   Usando uma conta que seja membro do grupo Administradores de Domínio, instale o SERVIDOR AGPM e atribua a função de Administrador AGPM a uma conta ou grupo.

-   Usando contas às quais você atribuirá funções AGPM, instale o Cliente AGPM.

-   Usando uma conta que tenha a função administrador agpm, configure AGPM e delegar acesso a GPOs atribuindo funções a outras contas.

-   Em uma conta que tenha a função Editor, solicite que um novo GPO seja criado que você aprove usando uma conta que tenha a função Aprovador. Use a conta editor para verificar o GPO fora do arquivo morto, editar o GPO, verificar o GPO no arquivo morto e, em seguida, solicitar a implantação.

-   Usando uma conta que tenha a função Aprovador, revise o GPO e implante-o em seu ambiente de produção.

-   Usando uma conta que tenha a função Editor, crie um modelo de GPO e use-o como ponto de partida para criar um novo GPO.

-   Usando uma conta que tenha a função Aprovador, exclua e restaure um GPO.

![processo de desenvolvimento de objeto de política de grupo.](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <a name="requirements"></a>Requisitos


Os computadores nos quais você deseja instalar o AGPM devem atender aos seguintes requisitos e você deve criar contas para uso neste cenário.

**Observação**  
Se você tiver o AGPM 2.5 instalado e estiver atualizando do Windows Server® 2003 para o Windows Server 2008 R2 ou Windows Server 2008, ou estão atualizando do Windows Vista sem service packs instalados para o Windows 7 ou Windows Vista® com Service Pack 1 (SP1), você deve atualizar o sistema operacional antes de poder atualizar para o AGPM 4.0.

Se você tiver o AGPM 3.0 instalado, não será preciso atualizar o sistema operacional antes de atualizar para o AGPM 4.0

 

Em um ambiente misto que inclui sistemas operacionais mais novos e antigos, há algumas limitações para a funcionalidade, conforme indicado na tabela a seguir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional no qual o AGPM Server 4.0 é executado</th>
<th align="left">Sistema operacional no qual o Cliente AGPM 4.0 é executado</th>
<th align="left">Status do suporte ao AGPM 4.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou Windows 7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Sem Suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou Windows 7</p></td>
</tr>
</tbody>
</table>

 

### <a name="agpm-server-requirements"></a>Requisitos do Servidor AGPM

O AGPM Server 4.0 requer o Windows Server 2008 R2, o Windows Server 2008, o Windows 7 e o GPMC do RSAT (Remote Server Administration Tools) ou o Windows Vista com SP1 e o GPMC do RSAT instalado. Há suporte para versões de 32 e 64 bits.

Antes de instalar o SERVIDOR AGPM, você deve ser membro do grupo Administradores de Domínio e os seguintes recursos Windows devem estar presentes, a menos que seja notado de outra forma:

-   GPMC

    -   Windows Server 2008 R2 ou Windows Server 2008: se o GPMC não estiver presente, ele será instalado automaticamente pelo AGPM.

    -   Windows 7: você deve instalar o GPMC do RSAT antes de instalar o AGPM. Para obter mais informações, consulte [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista com SP1: você deve instalar o GPMC do RSAT antes de instalar o AGPM. Para obter mais informações, consulte [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   O .NET Framework 3.5 ou versões posteriores

    -   Windows Servidor 2008 R2 ou Windows 7: se a versão .NET Framework 3.5 ou posterior não estiver presente, o .NET Framework 3.5 será instalado automaticamente pelo AGPM.

    -   Windows Server 2008 ou Windows Vista com SP1: você deve instalar o .NET Framework 3.5 ou uma versão posterior antes de instalar o AGPM.

Os seguintes Windows recursos são exigidos pelo SERVIDOR AGPM e serão instalados automaticamente se eles não estão presentes:

-   Ativação do WCF; Ativação não HTTP

-   Serviço de Ativação de Processos do Windows

    -   Modelo de Processo

    -   O ambiente .NET

    -   APIs de configuração

### <a name="agpm-client-requirements"></a>Requisitos do cliente AGPM

O Cliente AGPM 4.0 requer o Windows Server 2008 R2, o Windows Server 2008, o Windows 7 e o GPMC da RSAT, ou Windows Vista com SP1 e o GPMC do RSAT instalado. Há suporte para versões de 32 e 64 bits. O Cliente AGPM pode ser instalado em um computador que está executando o SERVIDOR AGPM.

Os seguintes Windows recursos são exigidos pelo Cliente AGPM e, a menos que sejam notados de outra forma, são instalados automaticamente se eles não estão presentes:

-   GPMC

    -   Windows Server 2008 R2 ou Windows Server 2008: se o GPMC não estiver presente, ele será instalado automaticamente pelo AGPM.

    -   Windows 7: você deve instalar o GPMC do RSAT antes de instalar o AGPM. Para obter mais informações, consulte [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .

    -   Windows Vista com SP1: você deve instalar o GPMC do RSAT antes de instalar o AGPM. Para obter mais informações, consulte [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .

-   A .NET Framework versão 3.0 ou posterior

    -   Windows Server 2008 R2 ou Windows 7: se a versão .NET Framework 3.0 ou posterior não estiver presente, o .NET Framework 3.5 será instalado automaticamente pelo AGPM.

    -   Windows Server 2008 ou Windows Vista com SP1: se a versão .NET Framework 3.0 ou posterior não estiver presente, o .NET Framework 3.0 será instalado automaticamente pelo AGPM.

### <a name="scenario-requirements"></a>Requisitos de cenário

Antes de começar esse cenário, crie quatro contas de usuário. Durante o cenário, você atribuirá uma das seguintes funções AGPM a cada uma dessas contas: Administrador AGPM (Controle Total), Aprovador, Editor e Revistor. Essas contas devem ser capazes de enviar e receber mensagens de email. Atribua **permissão de GPOs de** link às contas que possuem as funções Administrador, Aprovador e Editor do AGPM (opcionalmente).

**Observação**  
**A permissão de GPOs** de link é atribuída a membros dos Administradores de Domínio e Enterprise Administradores por padrão. Para atribuir permissão **de GPOs** de link a usuários ou grupos adicionais (como contas que têm as **** funções de Administrador agpm ou aprovador), clique no nó do domínio e clique na guia Delegação, selecione **Vincular GPOs**, clique em **Adicionar**e selecione usuários ou grupos aos quais você deseja atribuir a permissão.

 

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

6.  Na caixa **de diálogo Caminho** do Arquivo Morto, selecione um local para o arquivo morto em relação ao Servidor AGPM. O caminho do arquivo morto pode apontar para uma pasta no Servidor AGPM ou em outro lugar. No entanto, você deve selecionar um local com espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por este SERVIDOR AGPM. Clique em **Avançar**.

7.  Na caixa de diálogo Conta de **Serviço AGPM,** selecione uma conta de serviço na qual o Serviço AGPM será executado e clique em **Próximo**.

    Essa conta deve ser membro do grupo Administradores de Domínio ou, para uma configuração de privilégios mínimos, os seguintes grupos em cada domínio gerenciado pelo Servidor AGPM:

    -   Proprietários do Criador da Política de Grupo

    -   Operadores de Backup

    Além disso, essa conta requer permissão de Controle Total para as seguintes pastas:

    -   A pasta de arquivo morto AGPM, para a qual essa permissão é concedida automaticamente durante a instalação do SERVIDOR AGPM se estiver instalada em uma unidade local.

    -   A pasta temporária do sistema local, normalmente %windir%\\temp.

8.  Na caixa **de diálogo Proprietário do** Arquivo Morto, selecione uma conta ou grupo ao qual você atribui a função Administrador AGPM (Controle Total). Os administradores agpm podem atribuir funções e permissões AGPM a outros administradores de Política de Grupo, para que, posteriormente, você possa atribuir a função de Administrador AGPM a administradores adicionais de Política de Grupo. Para esse cenário, selecione a conta a ser acionável na função administrador agpm. Clique em **Avançar**.

9.  Na caixa **de diálogo Configuração** da Porta, digite uma porta na qual o Serviço AGPM deve escutar. Não desmarcar a caixa de seleção **Adicionar exceção** de porta ao firewall, a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta. Clique em **Avançar**.

10. Na caixa **de diálogo Idiomas,** selecione um ou mais idiomas de exibição para instalar para o SERVIDOR AGPM.

11. Clique **em Instalar**e clique em Concluir **para** sair do Assistente de Instalação.

    **Cuidado**  
    Não altere as configurações do Serviço AGPM por **meio de Ferramentas Administrativas** e **Serviços** no sistema operacional. Isso pode impedir que o Serviço AGPM seja a partir. Para obter informações sobre como alterar as configurações do serviço, consulte Help for Advanced Group Policy Management.

     

### <a name="step-2-install-agpm-client"></a><a href="" id="bkmk-config2"></a>Etapa 2: Instalar o cliente AGPM

Cada administrador de Política de Grupo, qualquer pessoa que crie, edite, implante, revise ou exclua GPOs, deve ter o Cliente AGPM instalado em computadores que eles usam para gerenciar GPOs. O nó Controle de Alteração, que você usa para executar muitas das tarefas de gerenciamento de GPO, aparece no Console de Gerenciamento de Política de Grupo somente se você instalar o Cliente AGPM. Para esse cenário, você instala o Cliente AGPM em pelo menos um computador. Você não precisa instalar o Cliente AGPM nos computadores dos usuários finais que não executam a administração da Política de Grupo.

**Para instalar o Cliente AGPM no computador de um administrador de Política de Grupo**

1.  Inicie o CD do Microsoft Desktop Optimization Pack e siga as instruções na tela para selecionar Gerenciamento Avançado de Política **de Grupo - Cliente**.

2.  Na caixa **de diálogo** Bem-vindo, clique em **Próximo**.

3.  Na caixa de diálogo Termos de Licença de Software da **Microsoft,** aceite os termos e clique em **Próximo**.

4.  Na caixa **de diálogo Caminho do** Aplicativo, selecione um local no qual instalar o Cliente AGPM. Clique em **Avançar**.

5.  Na caixa **de diálogo Servidor AGPM,** digite o nome DNS ou o endereço IP do Servidor AGPM e a porta à qual você deseja se conectar. A porta padrão para o Serviço AGPM é 4600. Não des limpar a caixa de seleção Permitir Console de Gerenciamento da Microsoft por meio do **firewall,** a menos que você configure manualmente exceções de porta ou use regras para configurar exceções de porta. Clique em **Avançar**.

6.  Na caixa **de diálogo Idiomas,** selecione um ou mais idiomas de exibição para instalar para o Cliente AGPM.

7.  Clique **em Instalar**e clique em Concluir **para** sair do Assistente de Instalação.

### <a name="step-3-configure-an-agpm-server-connection"></a><a href="" id="bkmk-config3"></a>Etapa 3: Configurar uma conexão do Servidor AGPM

O AGPM armazena todas as versões de cada GPO (Objeto de Política de Grupo) controlado, ou seja, cada GPO para o qual o AGPM fornece controle de alteração, em um arquivo morto central. Isso permite que os administradores de Política de Grupo visualizam e alterem GPOs offline sem afetar imediatamente a versão implantada de cada GPO.

Nesta etapa, você configura uma conexão do SERVIDOR AGPM e garante que todos os administradores de Política de Grupo se conectem ao mesmo Servidor AGPM. (Para obter informações sobre como configurar vários servidores AGPM, consulte Help for Advanced Group Policy Management.)

**Para configurar uma conexão do SERVIDOR AGPM para todos os administradores de Política de Grupo**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com a conta de usuário selecionada como o Proprietário do Arquivo Morto. Esse usuário tem a função de Administrador AGPM (Controle Total).

2.  Clique **em Iniciar**, aponte para Ferramentas **Administrativas**e clique em **Gerenciamento de Política** de Grupo para abrir o GPMC.

3.  Edite um GPO aplicado a todos os administradores de Política de Grupo.

4.  Na janela Editor de Gerenciamento de Política de **Grupo,** clique duas vezes em **Configuração**do Usuário, **Políticas,** Modelos **Administrativos,** **Windows Componentes**e **AGPM**.

5.  No painel de detalhes, clique duas vezes em **AGPM: Especifique o Servidor AGPM padrão (todos os domínios)**.

6.  Na janela **Propriedades,** selecione **Habilitado e** digite o nome DNS ou endereço IP e porta (por exemplo, **server.contoso.com:4600**) para o servidor que hospeda o arquivo morto. Por padrão, o Serviço AGPM usa a porta 4600.

7.  Clique **em OK**e feche a janela Editor de Gerenciamento de Política **de** Grupo. Quando a Política de Grupo é atualizada, a conexão do Servidor AGPM é configurada para cada administrador de Política de Grupo.

### <a name="step-4-configure-e-mail-notification"></a><a href="" id="bkmk-config4"></a>Etapa 4: Configurar a notificação de email

Como administrador agpm (Controle Total), você designa os endereços de email de Aprovadores e Administradores AGPM para os quais uma mensagem de email que contém uma solicitação é enviada quando um Editor tenta criar, implantar ou excluir um GPO. Você também determina o alias do qual essas mensagens são enviadas.

**Para configurar a notificação de email para AGPM**

1.  No **Editor de Gerenciamento de Política de Grupo,** navegue até a pasta Alterar **Controle** 

2.  No painel de detalhes, clique na guia **Delegação de** Domínio.

3.  No campo **Endereço de email** De, digite o alias de email para AGPM a partir do qual as notificações devem ser enviadas.

4.  No campo **Para endereço de email,** digite o endereço de email da conta de usuário à qual você pretende atribuir a função Aprovador.

5.  No campo **servidor SMTP,** digite um servidor de email SMTP válido.

6.  Nos campos **Nome de usuário** e **Senha,** digite as credenciais de um usuário que tenha acesso ao serviço SMTP. Clique em **Aplicar**.

### <a name="step-5-delegate-access"></a><a href="" id="bkmk-config5"></a>Etapa 5: Acesso delegado

Como administrador agpm (Controle Total), você delega acesso no nível de domínio a GPOs, atribuindo funções à conta de cada administrador de Política de Grupo.

**Observação**  
Você também pode delegar o acesso no nível gpo em vez do nível de domínio. Para obter mais informações, consulte Ajuda para Gerenciamento Avançado de Política de Grupo.

 

**Importante**  
Você deve restringir a associação ao grupo Proprietários de Criadores de Política de Grupo para que ele não possa ser usado para contornar o gerenciamento AGPM do acesso a GPOs. (No **Console**de Gerenciamento **** de Política de Grupo , clique em Objetos de Política de Grupo na floresta e no domínio no qual você deseja gerenciar GPOs, clique em Delegação **e,** em seguida, configure as configurações para atender às necessidades da sua organização.)

 

**Para delegar o acesso a todos os GPOs em todo um domínio**

1.  Na guia **Delegação de** Domínio, clique no botão **Adicionar,** selecione a conta de usuário do administrador de Política de Grupo para servir como Aprovador e clique em **OK**.

2.  Na caixa **de diálogo Adicionar Grupo ou** Usuário, selecione a função **Aprovador** para atribuir essa função à conta e clique em **OK**. (Essa função inclui a função Revistor.)

3.  Clique no **botão Adicionar,** selecione a conta de usuário do administrador de Política de Grupo para servir como Editor e clique em **OK**.

4.  Na caixa **de diálogo Adicionar Grupo ou** Usuário, selecione a função **Editor** para atribuir essa função à conta e clique em **OK**. (Essa função inclui a função Revistor.)

5.  Clique no **botão Adicionar,** selecione a conta de usuário do administrador de Política de Grupo para servir como Revistor e clique em **OK**.

6.  Na caixa **de diálogo Adicionar Grupo ou** Usuário, selecione a função **Revistor** para atribuir somente essa função à conta.

## <a name="steps-for-managing-gpos"></a>Etapas para gerenciar GPOs


Você deve concluir as etapas a seguir para criar, editar, revisar e implantar GPOs usando o AGPM. Além disso, você criará um modelo, excluirá um GPO e restaurará um GPO excluído.

[Etapa 1: Criar um GPO](#bkmk-manage1)

[Etapa 2: Editar um GPO](#bkmk-manage2)

[Etapa 3: Revisar e implantar um GPO](#bkmk-manage3)

[Etapa 4: Usar um modelo para criar um GPO](#bkmk-manage4)

[Etapa 5: Excluir e restaurar um GPO](#bkmk-manage5)

### <a name="step-1-create-a-gpo"></a><a href="" id="bkmk-manage1"></a>Etapa 1: Criar um GPO

Em um ambiente com vários administradores de Política de Grupo, aqueles com a função Editor podem solicitar que novos GPOs sejam criados. No entanto, essa solicitação deve ser aprovada por alguém com a função Aprovador.

Nesta etapa, você usa uma conta que tem a função Editor para solicitar que um novo GPO seja criado. Usando uma conta que tenha a função Aprovador, você aprova essa solicitação para criar o GPO.

**Para solicitar que um novo GPO seja criado e gerenciado por meio do AGPM**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário atribuída à função Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Clique com o botão direito do mouse no nó **Alterar Controle** e clique em **Novo GPO Controlado.**

4.  Na caixa **de diálogo Novo GPO** Controlado:

    1.  Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.**

    2.  Digite **MyGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique **em Criar ao** vivo para que o novo GPO seja implantado no ambiente de produção imediatamente após a aprovação. Clique em **Enviar**.

5.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo GPO é exibido na **guia Pendente.**

**Para aprovar a solicitação pendente para criar um GPO**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha a função de Aprovador no AGPM.

2.  Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias AGPM com a solicitação do Editor para criar um GPO.

3.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

4.  Na guia **Conteúdo,** clique na guia **Pendente** para exibir os GPOs pendentes.

5.  Clique com o botão **direito do mouse em MyGPO**e clique em **Aprovar**.

6.  Clique **em Sim** para confirmar a aprovação e mova o GPO para a guia **Controlado.**

### <a name="step-2-edit-a-gpo"></a><a href="" id="bkmk-manage2"></a>Etapa 2: Editar um GPO

Você pode usar GPOs para configurar configurações de computador ou usuário e implantá-las em muitos computadores ou usuários. Nesta etapa, você usa uma conta que tem a função Editor para verificar um GPO do arquivo morto, editar o GPO offline, verificar o GPO editado no arquivo morto e solicitar a implantação do GPO para o ambiente de produção. Para esse cenário, você configura uma configuração no GPO para exigir que a senha seja de pelo menos oito caracteres.

**Para verificar o GPO no arquivo morto para edição**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que tenha a função de Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo** no painel de detalhes, clique na guia **Controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e clique **em Check-Out**.

5.  Digite um comentário a ser exibido no histórico do GPO durante o check-out e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-out**.

**Para editar o GPO offline e configurar o tamanho mínimo da senha**

1.  Na guia **Controlado,** clique com o botão direito do mouse em **MyGPO**e clique em **Editar** para abrir a janela Editor de Gerenciamento de Política de **Grupo** e alterar uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **Configuração do**Computador, clique duas vezes em **Políticas,** **Windows Configurações,** **Segurança Configurações,** Políticas de Conta **e**Política **de Senha.**

    2.  No painel de detalhes, clique duas vezes em **Tamanho mínimo da senha**.

    3.  Na janela propriedades, marque a caixa de seleção **Definir essa** configuração de política, defina o número de caracteres como **8**e clique em **OK**.

2.  Feche a janela **Editor de Gerenciamento de Política de** Grupo.

**Para verificar o GPO no arquivo morto**

1.  Na guia **Controlado,** clique com o botão direito do mouse **em MyGPO** e clique **em Check-In**.

2.  Digite um comentário e clique em **OK**.

3.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-In**.

**Para solicitar a implantação do GPO para o ambiente de produção**

1.  Na guia **Controlado,** clique com o botão direito do mouse **em MyGPO** e clique em **Implantar**.

2.  Como essa conta não é um Aprovador ou Administrador agpm, você deve enviar uma solicitação de implantação. Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.** Digite um comentário a ser exibido no histórico do GPO e clique em **Enviar**.

3.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. **MyGPO** é exibido na lista de GPOs na **guia Pendente.**

### <a name="step-3-review-and-deploy-a-gpo"></a><a href="" id="bkmk-manage3"></a>Etapa 3: Revisar e implantar um GPO

Nesta etapa, você age como um Aprovador, criando relatórios e analisando as configurações e as alterações nas configurações no GPO para determinar se você deve aprove-los. Depois de avaliar o GPO, você o implanta no ambiente de produção e vincula o GPO a um domínio ou a uma unidade organizacional (OU). O GPO entra em vigor quando a Política de Grupo é atualizada para computadores nesse domínio ou UO.

**Para revisar as configurações no GPO**

1. Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário atribuída à função de Aprovador no AGPM. Qualquer administrador de Política de Grupo com a função Revistor, que está incluída em todas as outras funções, pode revisar as configurações em um GPO.

2. Abra a caixa de entrada de email da conta e observe que você recebeu uma mensagem de email do alias AGPM com uma solicitação do Editor para implantar um GPO.

3. Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

4. Na guia **Conteúdo** no painel de detalhes, clique na **guia Pendente.**

5. Clique duas vezes **em MyGPO** para exibir seu histórico.

6. Revise as configurações na versão mais recente do MyGPO:

   1.  Na janela **Histórico,** clique com o botão direito do mouse na versão GPO com o carimbo de hora mais recente, clique em **Configurações**e clique em **Relatório HTML** para exibir um resumo das configurações do GPO.

   2.  No navegador da Web, clique em **mostrar tudo** para exibir todas as configurações no GPO. Feche a janela do navegador.

7. Compare a versão mais recente do MyGPO com a primeira versão verificada no arquivo morto:

   1. Na janela **Histórico,** clique na versão GPO com o carimbo de data/hora mais recente. Pressione CTRL e clique na versão GPO mais antiga para a qual a Versão do Computador não é **\\***. ****

   2. Clique no **botão Diferenças.** A **seção Políticas de Conta/Política** de Senha é realçada em verde e precedida por **\[+\]**. Isso indica que a configuração está configurada somente na última versão do GPO.

   3. Clique **em Políticas de Conta/Política de Senha.** A **configuração** tamanho mínimo da senha também é realçada em verde e precedida por **\[+\]**, indicando que ela está configurada somente na última versão do GPO.

   4. Feche o navegador da Web.

**Para implantar o GPO no ambiente de produção**

1.  Na guia **Pendente,** clique com o botão direito do mouse **em MyGPO** e clique em **Aprovar**.

2.  Digite um comentário para incluir no histórico do GPO.

3.  Clique em **Sim**. Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O GPO é implantado no ambiente de produção.

**Para vincular o GPO a um domínio ou unidade organizacional**

1.  No GPMC, clique com o botão direito do mouse no domínio ou em uma unidade organizacional (OU) à qual você deseja aplicar o GPO configurado e clique em Vincular um **GPO Existente**.

2.  Na caixa **de diálogo Selecionar GPO,** clique **em MyGPO**e clique em **OK**.

### <a name="step-4-use-a-template-to-create-a-gpo"></a><a href="" id="bkmk-manage4"></a>Etapa 4: Usar um modelo para criar um GPO

Nesta etapa, você usa uma conta que tem a função Editor para criar e usar um modelo. Esse modelo é uma versão estática de um GPO para uso como ponto de partida para a criação de novos GPOs. Embora não seja possível editar um modelo, você pode criar um novo GPO com base em um modelo. Os modelos são úteis para criar rapidamente vários GPOs que incluem muitas das mesmas configurações de política.

**Para criar um modelo com base em um GPO existente**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que recebe a função de Editor no AGPM.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo** no painel de detalhes, clique na **guia Controlado.**

4.  Clique com o botão direito do mouse em **MyGPO**e clique em Salvar como **Modelo** para criar um modelo incorporando todas as configurações atualmente no MyGPO.

5.  Digite **MyTemplate** como o nome do modelo e um comentário e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo modelo aparece na guia **Modelos.**

**Para solicitar que um novo GPO seja criado e gerenciado por meio do AGPM**

1.  Clique na **guia Controlado.**

2.  Clique com o botão direito do mouse no nó **Alterar Controle** e clique em **Novo GPO Controlado.**

3.  Na caixa **de diálogo Novo GPO** Controlado:

    1.  Para receber uma cópia da solicitação, digite seu endereço de email no **campo Cc.**

    2.  Digite **MyOtherGPO** como o nome do novo GPO.

    3.  Digite um comentário para o novo GPO.

    4.  Clique **em Criar ao** vivo para que o novo GPO seja implantado no ambiente de produção imediatamente após a aprovação.

    5.  For **From GPO template**, select **MyTemplate**. Clique em **Enviar**.

4.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O novo GPO é exibido na **guia Pendente.**

Use uma conta atribuída à função de Aprovador para aprovar a solicitação pendente para criar o GPO como você fez na Etapa [1: Criar um GPO](#bkmk-manage1). MyTemplate incorpora todas as configurações que você configurou no MyGPO. Como MyOtherGPO foi criado usando MyTemplate, ele contém inicialmente todas as configurações que o MyGPO continha no momento em que MyTemplate foi criado. Você pode confirmar isso gerando um relatório de diferença para comparar MyOtherGPO com MyTemplate.

**Para verificar o GPO no arquivo morto para edição**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário que recebe a função de Editor no AGPM.

2.  Clique com o botão **direito do mouse em MyOtherGPO**e clique em **Check-Out**.

3.  Digite um comentário a ser exibido no histórico do GPO durante o check-out e clique em **OK**.

4.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. Na guia **Controlado,** o estado do GPO é identificado como **Check-out**.

**Para editar o GPO offline e configurar a duração do bloqueio da conta**

1.  Na guia **Controlado,** clique com o botão direito do mouse em **MyOtherGPO**e clique em **Editar** para abrir a janela Editor de Gerenciamento de Política de **Grupo** e alterar uma cópia offline do GPO. Para esse cenário, configure o tamanho mínimo da senha:

    1.  Em **Configuração do**Computador, clique duas vezes em **Políticas,** **Windows Configurações,** Segurança **Configurações,** Políticas de Conta **e**Política de Bloqueio **de Conta.**

    2.  No painel de detalhes, clique duas vezes em **Duração do bloqueio da conta.**

    3.  Na janela propriedades, marque Definir essa configuração de **política,** defina a duração como **30** minutos e clique em **OK**.

2.  Feche a janela **Editor de Gerenciamento de Política de** Grupo.

Verifique MyOtherGPO no arquivo morto e solicite a implantação como você fez para o MyGPO na [Etapa 2: Editar um GPO](#bkmk-manage2). Você pode comparar MyOtherGPO com MyGPO ou MyTemplate usando relatórios de diferença. Qualquer conta que inclua a função Revistor (Administrador DO AGPM \[Controle Total\], Aprovador, Editor ou Revistor) pode gerar relatórios.

**Para comparar um GPO a outro GPO e a um modelo**

1.  Para comparar MyGPO e MyOtherGPO:

    1.  Na guia **Controlado,** clique em **MyGPO**. Pressione CTRL e clique em **MyOtherGPO**.

    2.  Clique com o botão **direito do mouse em MyOtherGPO**, aponte para **Diferenças**e clique em **Relatório HTML**.

2.  Para comparar MyOtherGPO e MyTemplate:

    1.  Na guia **Controlado,** clique **em MyOtherGPO**.

    2.  Clique com o botão **direito do mouse em MyOtherGPO,** aponte para **Diferenças**e clique em **Modelo**.

    3.  Selecione **MyTemplate** e **RELATÓRIO HTML**e clique em **OK**.

### <a name="step-5-delete-and-restore-a-gpo"></a><a href="" id="bkmk-manage5"></a>Etapa 5: Excluir e restaurar um GPO

Nesta etapa, você age como um Aprovador para excluir um GPO.

**Para excluir um GPO**

1.  Em um computador no qual você instalou o Cliente AGPM, faça logon com uma conta de usuário atribuída à função de Aprovador.

2.  Na árvore **Console de Gerenciamento de Política de Grupo,** clique em Alterar **Controle** na floresta e no domínio no qual você deseja gerenciar GPOs.

3.  Na guia **Conteúdo,** clique na guia **Controlado** para exibir os GPOs controlados.

4.  Clique com o botão direito do mouse em **MyGPO**e clique em **Excluir**. Clique **em Excluir GPO do** arquivo morto e da produção para excluir a versão no arquivo morto e a versão implantada do GPO no ambiente de produção.

5.  Digite um comentário a ser exibido na trilha de auditoria do GPO e clique em **OK**.

6.  Quando a janela Progresso do **AGPM** indicar que o progresso geral está concluído, clique em **Fechar**. O GPO é removido da guia **Controlado** **** e é exibido na guia Lixeira, onde pode ser restaurado ou destruído.

Ocasionalmente, você pode descobrir depois de excluir um GPO de que ele ainda é necessário. Nesta etapa, você age como um Aprovador para restaurar um GPO que foi excluído.

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

     

 

 





