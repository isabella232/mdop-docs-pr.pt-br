---
title: Implantação do MBAM 2.5 em uma configuração autônoma
description: Apresentando como implantar o MBAM 2,5 em uma configuração autônoma.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799871"
---
# Implantando o MBAM 2,5 em uma configuração autônoma

Este artigo fornece instruções passo a passo para instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma configuração autônoma. Neste guia, usaremos uma configuração de dois servidores. Um dos dois servidores será um servidor de banco de dados executando o Microsoft SQL Server 2012. Este servidor hospedará os bancos de dados e relatórios do MBAM. O servidor adicional será um servidor Web do Windows Server 2012 que hospeda "servidor de administração e monitoramento" e "portal de autoatendimento".

## Etapas de preparação antes de instalar o software MBAM 2,5 Server

### Etapa 1: instalação e configuração de servidores

Antes de começarmos a configurar o MBAM 2,5, precisamos garantir que os dois servidores sejam configurados de acordo com os requisitos do sistema do MBAM. Veja os [requisitos mínimos do sistema do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)e selecione uma configuração que atenda a esses requisitos. 

#### Etapa 1,1: Implantando pré-requisitos de banco de dados e servidor de relatórios

1. Instale e configure um servidor que esteja executando o sistema operacional Windows Server 2008 R2 (ou posterior).

2. Instale o Windows PowerShell 3,0.

3. Instale o Microsoft SQL Server 2008 R2 ou uma versão posterior que inclua o Service Pack mais recente. Se você estiver instalando uma nova instância do SQL Server para MBAM, verifique se o SQL Server que você instala inclui o agrupamento SQL_Latin1_General_CP1_CI_AS. Você terá que instalar os seguintes recursos do SQL Server:

    * Mecanismo de banco de dados
    * Serviços de relatório
    * Conectividade de ferramentas de cliente
    * Ferramentas de gerenciamento – concluir

    > [!Note]
    > Opcionalmente, você também pode instalar o [recurso de criptografia de dados transparente (TDE) no SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    O SQL Server Reporting Services deve ser instalado e configurado no modo "nativo" e não no modo não configurado ou "SharePoint".

    ![Os recursos necessários do SQL Server](images/deploying-MBAM-1.png)

4. Se você pretende usar SSL para o site de administração e monitoramento, certifique-se de configurar o SSRS (SQL Server Reporting Services) para usar o protocolo SSL (Secure Sockets Layer) antes de configurar o site de administração e monitoramento. Caso contrário, o recurso relatórios usará um transporte de dados não criptografado (HTTP) em vez de criptografado (HTTPS).

    Você pode seguir [Configurar conexões SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) em um servidor de relatório do modo nativo para configurar SSL no servidor de relatório.
    
    > [!Note]
    > Você pode seguir o guia de instalação do SQL Server para sua respectiva versão do SQL Server para instalar o SQL Server. Os links são os seguintes:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Na pós-instalação do SQL Server, certifique-se de que você provisiona a conta de usuário no SQL Server e atribua as seguintes permissões ao usuário que irá configurar as funções de relatório e banco de dados do MBAM no servidor de banco de dados.

    Funções para a instância do SQL Server:
        
    * dbcreator
    * processadmin

    Direitos para a instância do SQL Server Reporting Services:
    
    * Criar pastas
    * Publicar relatórios

O servidor de banco de dados está pronto para a configuração das funções do MBAM 2,5. Vamos mover para o próximo servidor.

#### Etapa 1,2: Implantando pré-requisitos para o servidor de administração e monitoramento

Escolha um servidor que atenda à configuração de hardware conforme explicado no [documento requisitos do sistema do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements). Ele deve estar executando o Windows Server 2008 R2 ou um sistema operacional posterior em conjunto com Service Packs e atualizações mais recentes. Depois que o servidor estiver pronto, instale as seguintes funções e recursos:

##### Funções

* Ferramentas de gerenciamento do servidor Web (IIS) (selecione Ferramentas e scripts de gerenciamento do IIS).

* Serviços de função de servidor Web

    * Recursos HTTP comuns<br />
      Conteúdo estático<br />
      Documento padrão

    * Desenvolvimento de aplicativo<br />
      ASP.NET<br />
      Extensibilidade .NET<br />
      Extensões ISAPI<br />
      Filtros ISAPI<br />
      Segurança<br />
      Autenticação do Windows<br />
      Filtragem de solicitações

    * Ferramentas de gerenciamento do IIS do serviço Web

##### Recurso

* Recursos do .NET Framework 4,5
  
  * Microsoft .NET Framework 4,5
  
    Para o Windows Server 2012 ou o Windows Server 2012 R2, o .NET Framework 4,5 já está instalado para essas versões do Windows Server. No entanto, você deve habilitá-la.
  
    Para o Windows Server 2008 R2, o .NET Framework 4,5 não está incluído no Windows Server 2008 R2. Portanto, você deve baixar o .NET Framework 4,5 e instalá-lo separadamente.
  
  * Ativação do WCF<br />
    Ativação de HTTP<br />
    Ativação não HTTP
  
  * Ativação de TCP
  
  * Serviço de ativação de processos do Windows:<br />
    Modelo de processo<br />
    Ambiente do .NET Framework<br />
    APIs de configuração

Para que o portal de autoatendimento funcione, você também deve [baixar e instalar o ASP.NET MVC 4,0](https://go.microsoft.com/fwlink/?linkid=392271).

A próxima etapa é criar os usuários e grupos MBAM necessários no Active Directory.

### Etapa 2: Criando usuários e grupos nos serviços de domínio Active Directory
 
Como parte dos pré-requisitos, você deve definir determinadas funções e contas que são usadas no MBAM para fornecer direitos de segurança e acesso a servidores e recursos específicos, como os bancos de dados que estão sendo executados na instância do SQL Server e os aplicativos Web que estão em execução no servidor de administração e monitoramento.

Crie os grupos e usuários a seguir no Active Directory. (Você pode usar qualquer nome para os grupos e usuários.) Os usuários não precisam ter mais direitos de usuário. Uma conta de usuário do domínio é suficiente. Você precisará especificar o nome desses grupos durante a configuração do MBAM 2,5:

* **MBAMAppPool**  

  **Tipo**: usuário do domínio

  **Descrição**: usuário do domínio que tem permissão de leitura ou gravação para o banco de dados de conformidade e auditoria e o banco de dados de recuperação para permitir que os aplicativos Web acessem os dados e relatórios nestes bancos de dados. Ele também será usado pelo pool de aplicativos para os aplicativos Web.

  **Funções da conta (durante a configuração do MBAM)**:

  1. Conta de domínio do pool de aplicativos do serviço Web

  2. Banco de dados de auditoria e recuperação e usuário de leitura/gravação do banco de dados de auditoria para relatórios

* **MBAMROUser**

  **Tipo**: usuário do domínio

  **Descrição**: usuário do domínio que terá acesso somente leitura ao banco de dados de conformidade e auditoria para permitir que os relatórios acessem os dados de conformidade e auditoria neste banco de dados. Também será a conta de usuário do domínio que a instância local do SQL Server Reporting Services usa para acessar o banco de dados de auditoria e conformidade.

  **Funções da conta (durante a configuração do MBAM)**:

  1. O banco de dados de auditoria e o usuário somente leitura para relatórios

  2. Conta de usuário do domínio de banco de dados de auditoria e conformidade

* **MBAMAdvHelpDsk**

  **Tipo**: grupo de domínio

  **Descrição**: MBAM grupo de acesso de usuários avançados do helpdesk: grupo de usuários do domínio cujos membros têm acesso a todas as áreas do site de administração e monitoramento. Os usuários que têm essa função precisam inserir apenas a chave de recuperação, e não o domínio do usuário e o nome de usuário, quando eles estão ajudando os usuários a recuperar suas unidades. Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões de grupo usuários da assistência avançada do MBAM poderão substituir as permissões do grupo MBAM helpdesk.

  **Funções da conta (durante a configuração do MBAM)**: MBAM usuários avançados da assistência técnica

* **MBAMHelpDsk**

  **Tipo**: grupo de domínio

  **Descrição**: grupo de acesso de usuários da assistência técnica MBAM: grupo de usuários do domínio cujos membros têm acesso às áreas gerenciar TPM e recuperação de unidade do site de administração e monitoramento do MBAM. As pessoas que têm essa função devem preencher todos os campos quando usarem qualquer uma dessas opções. Isso inclui o nome do domínio e da conta do usuário.

  **Funções da conta (durante a configuração do MBAM)**: usuários da assistência técnica MBAM

* **MBAMRUGrp**

  **Tipo**: grupo de domínio

  **Descrição**: grupo de usuários do domínio cujos membros têm acesso somente leitura aos relatórios na área relatórios do site Administração e monitoramento.

  **Funções da conta (durante a configuração do MBAM)**:

  1. Grupo de acesso de domínio somente leitura de relatórios

  2. Grupo de acesso de usuários de relatório MBAM

### Etapa 3 (opcional): configurar e instalar o certificado SSL no servidor de administração e monitoramento

Embora seja opcional, é altamente recomendável que você use um certificado para ajudar a proteger a comunicação entre o cliente do MBAM e o site de administração e monitoramento e os websites do portal de autoatendimento. Não recomendamos o uso de certificados auto-assinados por motivos de segurança óbvios. Sugerimos que você use um certificado de tipo de servidor Web de uma autoridade de certificação confiável. Para fazer isso, você pode fazer referência à seção "usando certificado aprovado por autoridade de certificação" no [KB 2754259](https://support.microsoft.com/help/2754259).

Após a emissão do certificado, você deve adicionar o certificado ao repositório pessoal do servidor de administração e monitoramento. Para adicionar o certificado, abra o repositório de certificados no computador local. Para fazer isso, execute estas etapas:

1. Selecione Iniciar com o botão direito do mouse e selecione executar.

   ![Selecionar ](images/deploying-MBAM-2.png)

2. Digite "MMC.EXE" (sem as aspas) e, em seguida, selecione **OK**.

   ![Caixa executar](images/deploying-MBAM-3.png) 

3. Selecione **arquivo** no novo MMC aberto e selecione **Adicionar/remover snap-in**.
   
   ![Selecionar](images/deploying-MBAM-4.png)

4. Realce o snap-in de **certificados** e selecione **Adicionar**.

   ![Janela Adicionar ou remover snap-ins](images/deploying-MBAM-5.png)

5. Selecione a opção **conta do computador** e, em seguida, selecione **Avançar**.
   
   ![Janela do snap-in de certificados](images/deploying-MBAM-6.png)

6. Selecione **computador local** na tela seguinte e, em seguida, selecione **concluir**.
   
   ![Janela Selecionar computador](images/deploying-MBAM-7.png)

7. Agora você adicionou o snap-in de certificados. Isso permitirá que você trabalhe com qualquer certificado no repositório de certificados do computador.

   ![Janela Adicionar ou remover snap-ins](images/deploying-MBAM-8.png)

8. Importar o certificado do servidor Web para o repositório de certificados do computador.

   Agora que você tem acesso ao snap-in de certificados, você pode importar o certificado do servidor Web para o repositório de certificados do computador. Para fazer isso, siga as próximas etapas.

9. Abra o snap-in de certificados (computador local) e navegue até **pessoal** e, em seguida, **certificados**.
   
   ![Janela de snap-in de certificados (computador local)](images/deploying-MBAM-9.png)

   > [!Note]
   > O snap-in certificados pode não estar listado. Se não for, nenhum certificado será instalado.

10. Clique com o botão direito do mouse em **certificados**, selecione **todas as tarefas**e, em seguida, selecione **importar**.

    ![Janela de snap-in de certificados (computador local)](images/deploying-MBAM-10.png)

11. Quando o assistente for iniciado, selecione **Avançar**. Navegue até o arquivo que você criou que contém o certificado do servidor e a chave privada e selecione **Avançar**.

    ![Janela do assistente de importação de certificados](images/deploying-MBAM-11.png)

12. Digite a senha se você especificou uma para o arquivo quando a criou.

   ![Janela inserir senha](images/deploying-MBAM-12.png)

   > [!Note]
   > Verifique se a opção **marcar a chave como exportável** está selecionada para poder exportar o par de chaves novamente deste computador. Como uma medida de segurança adicional, talvez você queira deixar esta opção desmarcada para garantir que ninguém possa fazer um backup da sua chave privada.
 
13. Selecione **Avançar**e, em seguida, selecione o **repositório de certificados** no qual você deseja salvar o certificado.

    ![Janela do assistente de importação de certificados](images/deploying-MBAM-13.png)

    > [!Note]
    > Você deve selecionar **pessoal**, pois é um certificado de servidor Web. Se você incluiu o certificado na hierarquia de certificação, ele também será adicionado a essa loja.
 
14. Selecione **Avançar**e, em seguida, selecione **concluir**.

    ![Janela do assistente de importação de certificados](images/deploying-MBAM-14.png)

Agora, você verá o certificado do servidor para o seu servidor Web na lista de certificados pessoais. Ele será indicado pelo nome comum do servidor. (Você pode encontrar isso na seção assunto do certificado.)

Para referência adicional:

[Considerações sobre segurança do MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planejamento de formas para proteger os sites do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

A próxima etapa é registrar um nome principal de serviço para a conta do pool de aplicativos.

### Etapa 4: Configurando o certificado SSL para o servidor Web MBAM

Se você estiver usando a comunicação SSL entre o cliente e o servidor, certifique-se de que o certificado tenha os OIDs de uso avançado de chave (1.3.6.1.5.5.7.3.1) e (1.3.6.1.5.5.7.3.2). Ou seja, você deve verificar se a autenticação do servidor e a autenticação do cliente foram adicionadas.

Se você receber um erro de certificado ao tentar procurar URLs de serviço, você está usando um certificado que foi emitido para um nome diferente ou está navegando usando uma URL incorreta.

Embora o navegador possa emitir uma mensagem de erro de certificado, mas você pode continuar, o serviço Web do MBAM não ignorará erros de certificado e bloqueará a conexão. Você notará erros relacionados a certificado no log de eventos de administrador do MBAM do cliente MBAM. Se estiver usando um alias para se conectar ao servidor de administração e monitoramento, você deve emitir um certificado para o nome do alias. Ou seja, o nome do requerente do certificado deve ser o nome do alias, e o nome DNS do servidor local deve ser adicionado ao campo **nome alternativo do assunto** do certificado.

Exemplo:

Se o nome virtual for "bitlocker.contoso.com" e o nome do servidor de monitoramento e administração do MBAM for "adminserver.contoso.com," o certificado deve ser emitido para bitlocker.contoso.com (nome do requerente) e adminserver.contoso.com deve ser adicionado ao campo **nome alternativo do assunto** do certificado.

Da mesma forma, se você tiver vários servidores de administração e monitoramento instalados para balancear a carga usando um balanceador de carga, você deve emitir o certificado SSL para o nome virtual. Ou seja, o campo de nome do requerente do certificado deve ter o nome virtual e os nomes de todos os servidores locais devem ser adicionados no campo **nome alternativo do assunto** do certificado.

Exemplo:

Se o nome virtual for "bitlocker.contoso.com" e os servidores forem "adminserver1.contoso.com" e "adminiserver2.contoso.com", o certificado deve ser emitido para bitlocker.contoso.com (nome do requerente) e adminserver1.contoso.com, e adminiserver2.contoso.com devem ser adicionados ao campo **nome alternativo do assunto** do certificado.

As etapas para configurar a comunicação SSL usando o MBAM são descritas no seguinte artigo da base de dados de conhecimento: [KB 2754259](https://support.microsoft.com/help/2754259).

### Etapa 5: registrar os SPNS da conta do pool de aplicativos e configurar a delegação restrita

> [!Note]
> A delegação restrita é necessária apenas para o 2,5 e não é necessária para o 2,5 Service Pack 1 e versões posteriores.

Para habilitar os servidores MBAM para autenticar a comunicação a partir do site de administração e monitoramento e do portal de autoatendimento, você deve registrar um SPN (nome da entidade de serviço) para o nome do host na conta de domínio que você está usando para o pool de aplicativos Web. O artigo a seguir contém instruções passo a passo para registrar SPNs: [planejando como proteger os sites do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Depois de configurar o SPN, você deve configurar a delegação restrita no SPN. Para fazer isso, execute estas etapas:

1. Vá para Active Directory e localize as credenciais do pool de aplicativos que você configurou para os sites do MBAM nas etapas anteriores.

2. Clique com o botão direito do mouse nas credenciais e selecione **Propriedades**.

3. Selecione a guia **delegação** .

4. Selecione a opção para autenticação Kerberos.

5. Selecione **procurar**e navegue novamente para as credenciais do pool de aplicativos. Em seguida, você deve ver todos os SPNs configurados na conta creds do pool de aplicativos. (O SPN deve se parecer com "http/BitLocker. FQDN. com"). Realce o SPN que é igual ao nome do host especificado durante a instalação do MBAM.

6. Selecione **OK**.

Agora, você é bom com pré-requisitos. Nas próximas etapas, você vai instalar o software MBAM nos servidores e configurá-lo.

## Instalando e Configurando o software MBAM 2,5 Server

### Etapa 6: instalar o software MBAM 2,5 Server 

Para instalar o software MBAM Server usando o assistente de configuração de monitoramento e administração do Microsoft BitLocker no servidor de banco de dados e no servidor de administração e monitoramento, siga estas etapas.

1. No servidor em que você deseja instalar o MBAM, execute MBAMserversetup.exe para iniciar o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

2. Na página de boas-vindas, selecione **Avançar**.

3. Leia e aceite o contrato de licença de software da Microsoft e selecione **Avançar** para continuar a instalação.

4. Decida se deseja usar o Microsoft Update ao verificar se há atualizações e, em seguida, selecione **Avançar**.

5. Decida se deseja participar do programa de aperfeiçoamento da experiência do usuário e, em seguida, selecione **Avançar**.

6. Para iniciar a instalação, selecione **instalar**.

7. Para configurar os recursos de servidor após a instalação do software do servidor MBAM, marque a caixa de seleção **executar configuração do servidor do MBAM após o assistente se fechar** . Ou você pode configurar o MBAM mais tarde usando o atalho de **configuração do servidor do MBAM** que a instalação do servidor cria no menu **Iniciar** .

8. Selecione **concluir**.

Para obter mais informações, consulte [instalando o software de servidor MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### Etapa 7: configurar o banco de dados e a função de relatórios do MBAM 2,5

Nesta etapa, configuraremos o componente de relatório e bancos de dados do MBAM 2,5 usando o assistente MBAM:

1. Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação usando o assistente:
   
   1. No servidor no qual você deseja configurar os bancos de dados, inicie o assistente de **configuração do servidor do MBAM**. Você pode selecionar a **configuração do servidor do MBAM** no menu **Iniciar** para abrir o assistente.

   2. Selecione **Adicionar novos recursos**, selecione **banco de dados de auditoria e conformidade**, **banco de dados de recuperação e relatórios**e, em seguida, selecione **Avançar**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.

   3. Se a verificação de pré-requisito for bem-sucedida, selecione **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e selecione **verificar pré-requisitos novamente**.
   
   4. Usando as descrições a seguir, insira os valores de campo no assistente:

2. Banco de dados de auditoria e conformidade

   |Campo   |Descrição|
   |-------|-------|
   |Nome do SQL Server |Nome do servidor no qual você está configurando o banco de dados de conformidade e auditoria. <br /> Você deve adicionar uma exceção no computador de banco de dados de conformidade e auditoria para habilitar o tráfego de entrada na porta do SQL Server. O número da porta padrão é 1433.|
   |Instância de banco de dados do SQL Server    |Nome da instância do banco de dados em que os dados de conformidade e auditoria serão armazenados. Se estiver usando a instância padrão, você deve deixar este campo em branco. Você também deve especificar onde as informações do banco de dados serão localizadas.|
   |Nome do banco de dados   |Nome do banco de dados que armazenará os dados de conformidade. Você deve observar o nome do banco de dados que você está especificando aqui porque precisará fornecer essas informações em etapas posteriores.|
   |Usuário ou grupo de domínio de permissão de leitura/gravação  |Especifique o nome do usuário MBAMAppPool como configurado na etapa 2.|
   |Usuário ou grupo de domínio de acesso somente leitura   |Especifique o nome do usuário MBAMROUser como configurado na etapa 2.|

3. Banco de dados de recuperação.

   |Campo   |Descrição|
   |-----|-----|
   |Nome do SQL Server |Nome do servidor no qual você está configurando o banco de dados de recuperação. Você deve adicionar uma exceção no computador do banco de dados de recuperação para habilitar o tráfego de entrada recebido na porta do SQL Server. O número da porta padrão é 1433.|
   |Instância de banco de dados do SQL Server    |Nome da instância de banco de dados na qual os dados de recuperação serão armazenados. Se estiver usando a instância padrão, você deve deixar este campo em branco. Você também deve especificar onde as informações do banco de dados serão localizadas.|
   |Nome do banco de dados   |Nome do banco de dados que armazenará os dados de recuperação.|
   |Usuário ou grupo de domínio de permissão de leitura/gravação  |Usuário ou grupo de domínio que tem permissão de leitura/gravação para esse banco de dados para habilitar os aplicativos Web para acessar os dados e relatórios nesse banco de dados. <br />Se você inserir um usuário nesse campo, ele deve ter o mesmo valor que o valor no campo **conta de domínio do pool de aplicativos de serviço Web** na página **configurar aplicativos Web** . <br />Se você inserir um grupo nesse campo, o valor no campo **conta de domínio do pool de aplicativos do serviço Web** na página **configurar aplicativos Web** deve ser um membro do grupo que você inserir nesse campo.|
   
   Quando terminar as entradas, selecione **Avançar**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.
   
   Se a verificação de pré-requisito for bem-sucedida, selecione **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e, em seguida, selecione **Avançar** novamente.

4. Gerente.

   |Campo   |Descrição|
   |----|----|
   |Instância do SQL Server Reporting Services  |Instância do SQL Server Reporting Services em que os relatórios serão configurados. Se estiver usando a instância padrão, você deve deixar este campo em branco.|
   |Grupo de domínio da função de relatório |Especifique o nome do MBAMRUGrp conforme mencionado na etapa 2.|
   |Nome do SQL Server |Nome do servidor no qual o banco de dados de conformidade e auditoria está configurado.|
   |Instância de banco de dados do SQL Server    |Nome da instância do banco de dados em que os dados de conformidade e auditoria estão configurados. Se estiver usando a instância padrão, você deve deixar este campo em branco. <br />Você deve adicionar uma exceção no computador relatórios para habilitar o tráfego de entrada na porta do servidor de relatórios. (A porta padrão é 80).|
   |Nome do banco de dados|  Nome do banco de dados de conformidade e auditoria. Por padrão, o nome do banco de dados é MBAM status de conformidade.|
   |Conta de domínio de banco de dados de auditoria e conformidade    |Especifique o nome do usuário MBAMROUser como configurado na etapa 2.|
   
   Quando terminar as entradas, selecione **Avançar**. O assistente verifica se todos os pré-requisitos do recurso relatórios foram atendidos. Selecione Avançar para continuar. Na página **Resumo** , examine os recursos que serão adicionados.
   
   Para obter mais informações, consulte o seguinte artigo: [como configurar os bancos de dados do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### Etapa 8: configurar a função de aplicativos Web do MBAM 2,5

1. No servidor no qual você deseja configurar os aplicativos Web, inicie o assistente de configuração do MBAM Server. Você pode selecionar a **configuração do servidor do MBAM** no menu **Iniciar** para abrir o assistente.

2. Selecione **Adicionar novos recursos**, selecione **site de administração e monitoramento** e **portal de autoatendimento**e, em seguida, selecione **Avançar**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.

3. Se a verificação de pré-requisito for bem-sucedida, selecione **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e selecione **verificar pré-requisitos novamente**.

4. Use as descrições a seguir para inserir os valores de campo no assistente.

   |Campo   |Descrição|
   |-----|-----|
   |Certificado de segurança    |Selecione um certificado criado anteriormente na etapa 3 para criptografar opcionalmente a comunicação entre os serviços Web e o servidor no qual você está configurando o site de administração e monitoramento. Se você selecionar não usar um certificado, talvez sua comunicação à Web não seja segura.|
   |Nome do host   |Nome do computador host no qual você está configurando o site de administração e monitoramento. <br />Ele não precisa ser o nome do host do computador, mas pode ser algo. No entanto, se o nome do host for diferente do nome NetBIOS do computador, você precisará criar um registro A e garantir que o SPN use o nome de host personalizado, e não o nome NetBIOS. Isso é comum em cenários de balanceamento de carga.|
   |Caminho de instalação   |Caminho no qual você está instalando o site de administração e monitoramento.|
   |Port    |Número da porta a ser usada para a comunicação do site. <br /> Você deve definir uma exceção de firewall para permitir a comunicação por meio da porta especificada.|
   |Conta e senha de domínio do pool de aplicativos do serviço Web    |Especifique a conta de usuário e a senha do usuário do MBAMAppPool conforme configurado na etapa 2. <br /> Para aumentar a segurança, defina a conta especificada nas credenciais para ter direitos de usuário limitados. Além disso, defina a senha da conta para nunca expirar.|

5. Verifique se a conta de IIS_IUSRS interna ou a conta do pool de aplicativos foi adicionada às configurações de segurança de **representar um cliente após a autenticação** e **logon como um trabalho em lotes** local.

   Para verificar se a conta foi adicionada às configurações de segurança locais, abra o **Editor de política de segurança local**, expanda o nó **políticas locais** , selecione o nó **atribuição de direitos de usuário** e, em seguida, selecione **representar um cliente após autenticação** e **faça logon como** políticas de trabalho em lotes no painel do lado direito.

6. Use as descrições de campo a seguir para configurar as informações de conexão no Assistente para o banco de dados de conformidade e auditoria.
   |Campo   |Descrição|
   |------|------|
   |Nome do SQL Server |Nome do servidor no qual o banco de dados de conformidade e auditoria está configurado.|
   |Instância de banco de dados do SQL Server    |Nome da instância do SQL Server (por exemplo, \<Server Name\> ) e em que o banco de dados de auditoria e conformidade está configurado. Deixe em branco se você estiver usando a instância padrão.|
   |Nome do banco de dados   |Nome do banco de dados de conformidade e auditoria. Por padrão, é "MBAM status de conformidade".|

7. Use as descrições de campo a seguir para configurar as informações de conexão no assistente do banco de dados de recuperação.
   |Campo   |Descrição|
   |----|----|
   |Nome do SQL Server |Nome do servidor no qual o banco de dados de recuperação está configurado.|
   |Instância de banco de dados do SQL Server    |Nome da instância do SQL Server (por exemplo, \<Server Name\> ) em que o banco de dados de recuperação está configurado. Deixe em branco se você estiver usando a instância padrão.|
   |Nome do banco de dados   |Nome do banco de dados de recuperação. Por padrão, é "recuperação e hardware de MBAM".|

8. Use as descrições a seguir para inserir os valores de campo no Assistente para configurar o site de administração e monitoramento.
   |Campo   |Descrição|
   |----|----|
   |Grupo de domínio da função helpdesk avançado |Especifique o nome do grupo MBAMAdvHelpDsk conforme configurado na etapa 2.|
   |Grupo de domínio da função helpdesk  |Especifique o nome do grupo MBAMHelpDsk conforme configurado na etapa 2.|
   |Usar a integração do System Center Configuration Manager |Marque esta caixa de seleção para desmarcar essa caixa de seleção.     |
   |Grupo de domínio da função de relatório |Especifique o nome do grupo MBAMRUGrp conforme configurado na etapa 2.    |
   |URL do SQL Server Reporting Services   |Especifique a URL do serviço Web para o servidor SSRS no qual os relatórios do MBAM são configurados. Você pode encontrar essas informações ao fazer logon no Gerenciador de configuração do Reporting Services no servidor de banco de dados. <br /> Exemplo de um nome de domínio totalmente qualificado:https://MyReportServer.Contoso.com/ReportServer <br />Exemplo de um nome de host personalizado:https://MyReportServer/ReportServer|
   |Diretório virtual   |Diretório virtual do site Administração e monitoramento. Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site. Por exemplo: <br />http (s):// *\<host name\>* : *\<port\>* /helpdesk/ <br />Se você não especificar um diretório virtual, o valor da assistência técnica será usado.     |

9. Use a seguinte descrição para inserir os valores de campo no Assistente para configurar o portal de autoatendimento.

   |Campo   |Descrição|
   |----|----|
   |Diretório virtual   |Diretório virtual do aplicativo Web. Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site. Por exemplo:<br />http (s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Se você não especificar um diretório virtual, o valor "SelfService" será usado.|

10. Quando terminar as entradas, selecione **Avançar**. O assistente verifica se todos os pré-requisitos para os aplicativos da Web são atendidos.

11. Selecione **Avançar** para continuar.

12. Na página **Resumo** , examine os recursos que serão adicionados.

13. Selecione **Adicionar** para adicionar os aplicativos Web ao servidor e, em seguida, selecione **fechar**.

## Personalizando e validando etapas após a instalação do software MBAM 2,5 Server

### Etapa 9: personalizar o portal de servidor de autoatendimento para sua organização

Para personalizar o portal de autoatendimento adicionando texto de aviso personalizado, o nome da sua empresa, os ponteiros para obter mais informações e assim por diante, consulte [Personalizando o portal de autoatendimento da sua organização](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### Etapa 10: configurar o portal de servidor de autoatendimento se os computadores cliente não puderem acessar a CDN 

Determine se seus computadores cliente têm acesso à rede de distribuição de conteúdo (CDN) do Microsoft AJAX. A CDN oferece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript. Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, somente o nome da empresa e a conta na qual o usuário se conectou serão exibidos. Nenhuma mensagem de erro será mostrada.

Siga um destes procedimentos:

* Se seus computadores cliente tiverem acesso à CDN, não faça nada. Sua configuração do portal de autoatendimento está completa.

* Se seus computadores cliente não tiverem acesso à CDN, siga as etapas em [como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a rede de entrega de conteúdo da Microsoft](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### Etapa 11: validar a configuração de recursos do servidor do MBAM 2,5 

Para validar sua implantação do MBAM Server para usar a topologia autônoma, siga estas etapas.

1. Em cada servidor em que um recurso do MBAM é implantado, selecione programas **Control Panel**  >  **Programs**  >  **e recursos**do painel de controle. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .
   > [!Note]
   > Para executar a validação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.

2. No servidor em que o banco de dados de recuperação está configurado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está configurado.

3. No servidor OM que o banco de dados conformidade e auditoria está configurado, abra o SQL Server Management Studio e verifique se o banco de dados de status de conformidade do MBAM está configurado.

4. No servidor ONM qual o recurso relatórios está configurado, abra um navegador da Web usando credenciais administrativas e navegue até a home page do site do SQL Server Reporting Services.
   
   O local da Home Page padrão de uma instância do site do SQL Server Reporting Services é o seguinte: http (s):// *\<MBAM Reports Server Name\>* : *\<port\>* /reports.aspx
   
   Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias que você especificou durante a configuração.
   
5. Verifique se uma pasta de relatórios chamada administração e administração do Microsoft BitLocker contém uma fonte de dados chamada MaltaDataSource. Essa fonte de dados contém pastas que têm nomes que representam as localidades do idioma (por exemplo, en-US). Os relatórios estão nas pastas de idiomas.

   > [!Note]
   > Se o SQL Server Reporting Services (SSRS) tiver sido configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http (s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Se o SSRS não tiver sido configurado para usar o Secure Socket Layer (SSL), a URL dos relatórios será definida como "HTTP" em vez de "HTTPS" quando você instalar o servidor MBAM. Se, em seguida, você acessar o site de administração e monitoramento (também conhecido como assistência técnica) e selecionar um relatório, receberá a seguinte mensagem: "apenas conteúdo seguro é exibido". Para mostrar o relatório, selecione **mostrar todo o conteúdo**.

6. No servidor no qual o recurso de site Administração e monitoramento está configurado, execute o Gerenciador de servidores, navegue até **funções**e, em seguida, selecione **servidor Web (IIS)**  >  Gerenciador de**serviços de informações da Internet (IIS)** .

7. Em **conexões**, navegue até \<computer name\> e selecione **sites**  >  **Microsoft BitLocker Administration and Monitoring**. Verifique se os seguintes itens estão listados:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. No servidor em que o site de administração e monitoramento e o portal de autoatendimento estão configurados, abra um navegador da Web usando credenciais administrativas.

9. Navegue até os seguintes websites para verificar se eles são carregados com êxito:
   * https (s):// \<MBAM Administration Server Name\> : \<port\> /helpdesk/(confirme cada link para navegação e relatórios)
   * http (s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Pressupõe-se que você configurou os recursos do servidor na porta padrão sem criptografia de rede. Se você configurou os recursos de servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada. Por exemplo: http (s):// \<host name\> : \<port\> /helpdesk/http (s):// \<host name\> : \<port\> / \<virtualdirectory\> /se os recursos do servidor foram configurados para usar a criptografia de rede, altere http://para https://.
   
10. Navegue até os serviços da Web a seguir para verificar se eles são carregados com êxito. Uma página é aberta para indicar que o serviço está em execução. No entanto, a página não exibe metadados.

    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### Etapa 12: configurar os modelos de política de grupo do MBAM

Para implantar o MBAM, você precisa definir configurações de política de grupo que definem as configurações de implementação de MBAM para a criptografia de unidade de disco BitLocker. Para concluir essa tarefa, você deve copiar os modelos de política de grupo do MBAM para um servidor ou uma estação de trabalho que pode executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) e, em seguida, editar as configurações.

> [!Important]
> Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** ou o MBAM não funcionará corretamente. Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.
 
#### Copiar os modelos de política de grupo do MBAM 2,5

Antes de instalar o cliente do MBAM, você deve copiar objetos de política de grupo (GPOs) específicos do MBAM para a estação de trabalho de gerenciamento. Esses GPOs definem as configurações de implementação do MBAM para o BitLocker. Você pode copiar os modelos de política de grupo para qualquer servidor ou estação de trabalho compatível com um servidor ou computador cliente compatível com Windows e que possa executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM).

Para obter mais informações, consulte [copiando os modelos de política de grupo do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### Editando MBAM 2,5 configurações do GPO

Depois de criar os GPOs necessários, você deve implantar as configurações de política de grupo do MBAM para os computadores cliente da sua organização. Para exibir e criar GPOs, você deve ter o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) instalado.

Para obter mais informações, consulte [editando as configurações de política de grupo do MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) e [planejando para MBAM 2,5 requisitos da política de grupo](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### Etapa 13: Implantando o cliente do MBAM 2,5

Dependendo de quando implantar o software cliente de administração e monitoramento do Microsoft BitLocker, você pode habilitar o BitLocker em um computador em sua organização antes de o usuário receber o computador ou depois de configurar a política de grupo e implantar o software cliente do MBAM usando um sistema de implantação de software corporativo.
 
#### Implantar o cliente do MBAM em computadores de mesa ou portáteis

Depois de definir as configurações de política de grupo, você pode usar um produto de sistema de implantação de software corporativo, como o Gerenciador de configuração do Microsoft System Center 2012 ou os serviços de domínio Active Directory (AD DS) para implantar os arquivos de instalação do cliente do MBAM no Windows Installer para computadores de destino. Você pode usar os arquivos de 32 bits ou 64 bits MbamClientSetup.exe ou os arquivos de 32 bits ou 64 bits MBAMClient.msi. Eles são fornecidos juntamente com o software cliente MBAM.

Para obter mais informações, consulte [como implantar o cliente do MBAM em computadores desktop ou laptop](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### Implantar o cliente MBAM como parte de uma implantação do Windows

Em organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia de unidade de disco BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que todos os computadores são compatíveis com o BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização é instalar uma imagem corporativa do Windows antes que o computador seja entregue ao usuário. Se as configurações de política de grupo estiverem definidas para exigir um PIN, os usuários serão solicitados a definir um PIN depois de receberem a política.

Para obter mais informações, consulte [como implantar o cliente MBAM como parte de uma implantação do Windows](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### Como implantar o cliente MBAM usando uma linha de comando

Para obter mais informações [, consulte como implantar o cliente MBAM usando uma linha de comando](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### Pós-implantação de clientes

Agora que você concluiu a atividade de implantação, examine os logs a seguir e determine se os clientes são reportados com êxito para o banco de dados do MBAM.

## Perguntas frequentes

### Como criar servidores IIS com balanceamento de carga

* O SPN deve ser registrado somente para o nome amigável (por exemplo: bitlocker.corp.net) e não deve ser registrado em servidores IIS individuais.

* Se um certificado for usado, o certificado deve ter nomes de FQDN e NetBIOS inseridos no campo de **nome alternativo do assunto** para todos os servidores IIS no grupo de balanceamento de carga e também como o nome amigável (por exemplo: BitLocker.Corp.net). Caso contrário, o certificado será reportado como não confiável para o navegador quando você navegar pelos endereços com carga balanceada.

Para obter mais informações, consulte os SPNs de [balanceamento de carga de rede do IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) e [o registro de SPNs para a conta do pool de aplicativos](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### Como configurar um certificado

* Você terá que ter dois certificados. Um certificado é usado para SQL Server e o outro é usado para o IIS. Eles devem ser instalados antes de iniciar a instalação do MBAM.

* Recomendamos que você use o instalador para adicionar o certificado à configuração do IIS, em vez de editar manualmente o arquivo web.config.

* O certificado não será aceito pelo configurador MBAM se o campo "emitido para" no certificado não corresponder ao nome do servidor. Nesse caso, crie temporariamente um certificado auto-assinado do console do IIS e use-o no configurador. Isso fará com que o Nsure os aplicativos Web sejam instalados para SSL e HTTPS. Depois disso, você pode alterar o certificado para uma das associações do IIS para o site do MBAM.

### O requisito de permissões SQL para instalação

Crie uma conta para o pool de aplicativos MBAM e dê a ela somente as permissões SecurityAdmin, pública e DBCreator.

Consulte [configuração de banco de dados do MBAM – permissões mínimas](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) para obter mais informações.

> [!Note]
> * Em algumas situações, são necessárias mais permissões para as operações de instalação e atualização iniciais.
> * Use uma conta que tenha o SA temporário para a instalação.
> * Não inicie o configurador no contexto de uma conta de usuário (executar como) que não tenha permissões suficientes para fazer alterações no SQL Server porque isso causará erros de instalação.
> * Você deve estar conectado usando uma conta que tem permissões no SQL Server. Somente bancos de dados do SQL Server podem ser criados ou atualizados executando o MBAM configurador remotamente. Para o servidor SSRS, você deve instalar o MBAM e executar o configurador localmente para instalar ou atualizar os relatórios do SSRS do MBAM.

### A permissão necessária para o registro de SPN

Uma conta que é usada para a instalação do portal do IIS deve ter permissões de Write servicePrincipalName e de SPN validadas para gravação. Sem essas permissões, a instalação retornará uma mensagem de aviso que informa que não pode registrar o SPN.

> [!Note]
> Esta mensagem de aviso será exibida duas vezes. Isso não significa que o SPN deve ter dois objetos registrados nele.

Para saber mais, confira [falha na instalação do MBAM com a mensagem de erro "registrar o SPN adiado"](https://support.microsoft.com/help/2754138/).

### Era necessário atualizar os modelos ADMX para a versão mais recente?

Você verá várias opções do sistema operacional no nó raiz MBAM para GPO após atualizar os modelos ADMX para as versões mais recentes. Por exemplo, Windows 7, Windows 8,1 e Windows 10, versão 1511 e versões posteriores.

Para obter mais informações sobre como atualizar os modelos ADMX, consulte os seguintes artigos:
* [Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planejamento para os requisitos de Política de Grupo do MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modelos administrativos de política de grupo do Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
