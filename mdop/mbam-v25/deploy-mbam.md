---
title: Implantação do MBAM 2.5 em uma configuração autônoma
description: Apresentando como implantar o MBAM 2.5 em uma configuração autônomo.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 1ceccf3973bb131484f91917c2b80cd676d1c31b
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910466"
---
# <a name="deploying-mbam-25-in-a-standalone-configuration"></a>Implantando o MBAM 2.5 em uma configuração autônoma

Este artigo fornece instruções passo a passo para instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 em uma configuração autônoma. Neste guia, vamos usar uma configuração de dois servidores. Um dos dois servidores será um servidor de banco de dados executando Microsoft SQL Server 2012. Este servidor hospedará os bancos de dados e relatórios do MBAM. O servidor adicional será um servidor Windows Server 2012 Web hospedando "Servidor de Administração e Monitoramento" e "Portal de Autoatendamento".

## <a name="preparation-steps-before-installing-mbam-25-server-software"></a>Etapas de preparação antes de instalar o software de servidor MBAM 2.5

### <a name="step-1-installation-and-configuration-of-servers"></a>Etapa 1: Instalação e configuração de servidores

Antes de começar a configurar o MBAM 2.5, precisamos garantir que ambos os servidores sejam configurados de acordo com os requisitos do sistema MBAM. Consulte os [requisitos mínimos do sistema do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)e selecione uma configuração que atenda a esses requisitos. 

#### <a name="step-11-deploying-prerequisites-for-database-and-reporting-server"></a>Etapa 1.1: Implantando pré-requisitos para o banco de dados e o servidor de relatórios

1. Instale e configure um servidor executando Windows sistema operacional Server 2008 R2 (ou posterior).

2. Instale Windows PowerShell 3.0.

3. Instale Microsoft SQL Server 2008 R2 ou uma versão posterior que inclua o service pack mais recente. Se você estiver instalando uma nova instância do SQL Server para MBAM, certifique-se de que o SQL Server que você instalar inclua o colamento SQL_Latin1_General_CP1_CI_AS. Você terá que instalar os seguintes recursos SQL Server:

    * Mecanismo de Banco de Dados
    * Reporting Services
    * Conectividade de Ferramentas do Cliente
    * Ferramentas de Gerenciamento – Concluídas

    > [!Note]
    > Opcionalmente, você também pode instalar o [recurso Transparent Data Encryption (TDE) no SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services deve ser instalado e configurado no modo "nativo" e não no modo não configurado ou "SharePoint".

    ![Os recursos SQL Server necessários.](images/deploying-MBAM-1.png)

4. Se você planeja usar o SSL para o site de Administração e Monitoramento, configure o SQL Server Reporting Services (SSRS) para usar o protocolo SSL (Secure Sockets Layer) antes de configurar o site de Administração e Monitoramento. Caso contrário, o recurso Relatórios usará o transporte de dados NÃO criptografado (HTTP) em vez de criptografado (HTTPS).

    Você pode seguir [Configure SSL Connections](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) on a Native Mode Report Server to configure SSL on Report Server.
    
    > [!Note]
    > Você pode seguir o guia SQL Server de instalação para sua respectiva versão do SQL Server para instalar SQL Server. Os links são os seguinte:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Na pós-instalação do SQL Server, certifique-se de provisionar a conta de usuário no SQL Server e atribua as seguintes permissões ao usuário que configurará o banco de dados do MBAM e as funções de relatório no servidor de banco de dados.

    Funções para a instância de SQL Server:
        
    * dbcreator
    * processadmin

    Direitos para a instância de SQL Server Reporting Services:
    
    * Criar Pastas
    * Publicar relatórios

Seu servidor de banco de dados está pronto para a configuração de funções do MBAM 2.5. Vamos para o próximo servidor.

#### <a name="step-12-deploying-prerequisites-for-administration-and-monitoring-server"></a>Etapa 1.2: Implantando pré-requisitos para o servidor de administração e monitoramento

Escolha um servidor que atenda à configuração de hardware, conforme explicado no documento de requisitos do sistema [MBAM.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements) Ele deve estar executando Windows Server 2008 R2 ou um sistema operacional posterior juntamente com o service pack e as atualizações mais recentes. Depois que o servidor estiver pronto, instale as seguintes funções e recursos:

##### <a name="roles"></a>Funções

* Ferramentas de Gerenciamento do Servidor Web (IIS) (Selecione Scripts e Ferramentas de Gerenciamento do IIS).)

* Serviços de Função de Servidor Web

    * Recursos HTTP comuns<br />
      Conteúdo Estático<br />
      Documento Padrão

    * Desenvolvimento de aplicativo<br />
      ASP.NET<br />
      Extensibilidade .NET<br />
      Extensões ISAPI<br />
      Filtros ISAPI<br />
      Segurança<br />
      Autenticação do Windows<br />
      Filtragem de solicitação

    * Ferramentas de Gerenciamento do IIS do Serviço Web

##### <a name="feature"></a>Recurso

* .NET Framework recursos 4.5
  
  * Microsoft .NET Framework 4.5
  
    Para Windows Server 2012 ou Windows Server 2012 R2, o .NET Framework 4.5 já está instalado para essas versões do Windows Server. No entanto, você deve habilita-lo.
  
    Para Windows Server 2008 R2, o .NET Framework 4.5 não está incluído no Windows Server 2008 R2. Portanto, você deve baixar .NET Framework 4.5 e instalá-lo separadamente.
  
  * Ativação do WCF<br />
    Ativação HTTP<br />
    Ativação não HTTP
  
  * Ativação TCP
  
  * Windows Serviço de Ativação de Processo:<br />
    Modelo de Processo<br />
    .NET Framework Ambiente<br />
    APIs de configuração

Para que o portal de autoatendam funcione, você também deve baixar e [instalar ASP.NET MVC 4.0](https://go.microsoft.com/fwlink/?linkid=392271).

A próxima etapa é criar os usuários e grupos de MBAM necessários no Active Directory.

### <a name="step-2-creating-users-and-groups-in-active-directory-domain-services"></a>Etapa 2: criar usuários e grupos nos Serviços de Domínio do Active Directory
 
Como parte dos pré-requisitos, você deve definir determinadas funções e contas usadas no MBAM para fornecer direitos de segurança e acesso a servidores e recursos específicos, como os bancos de dados que estão sendo executados na instância do SQL Server e os aplicativos Web que estão sendo executados no Servidor de Administração e Monitoramento.

Crie os seguintes grupos e usuários no Active Directory. (Você pode usar qualquer nome para os grupos e usuários.) Os usuários não têm que ter direitos de usuário maiores. Uma conta de usuário de domínio é suficiente. Você terá que especificar o nome desses grupos durante a configuração do MBAM 2.5:

* **MBAMAppPool**  

  **Tipo**: Usuário de Domínio

  **Descrição**: usuário de domínio que tem permissão de Leitura ou Gravação para o Banco de Dados de Conformidade e Auditoria e o Banco de Dados de Recuperação para permitir que os aplicativos Web acessem os dados e relatórios nesses bancos de dados. Ele também será usado pelo pool de aplicativos para os aplicativos Web.

  **Funções de conta (durante a configuração do MBAM)**:

  1. Conta de domínio do pool de aplicativos de serviço Web

  2. Usuário de leitura/gravação de banco de dados de conformidade e auditoria e banco de dados de recuperação para relatórios

* **MBAMROUser**

  **Tipo**: Usuário de Domínio

  **Descrição**: Usuário de domínio que terá Read-Only acesso ao Banco de Dados de Conformidade e Auditoria para permitir que os relatórios acessem os dados de conformidade e auditoria neste banco de dados. Também será a conta de usuário de domínio que a instância SQL Server Reporting Services local usa para acessar o Banco de Dados de Conformidade e Auditoria.

  **Funções de conta (durante a configuração do MBAM)**:

  1. Usuário somente leitura de banco de dados de conformidade e auditoria para relatórios

  2. Conta de usuário de domínio de Banco de Dados de Auditoria e Conformidade

* **MBAMAdvHelpDsk**

  **Tipo**: Grupo de Domínios

  **Descrição**: Grupo de acesso dos usuários avançados do Helpdesk do MBAM: grupo de usuários de domínio cujos membros têm acesso a todas as áreas do Site de Administração e Monitoramento. Os usuários que têm essa função precisam inserir apenas a chave de recuperação, não o domínio e o nome de usuário do usuário, quando estão ajudando os usuários a recuperar suas unidades. Se um usuário for membro do grupo Usuários de Ajuda do MBAM e do grupo Usuários Avançados de Ajuda do MBAM, as permissões do grupo Usuários avançados do MbaM Helpdesk substituem as permissões do Grupo de Ajuda do MBAM.

  **Funções de conta (durante a configuração do MBAM)**: Usuários avançados do MBAM Helpdesk

* **MBAMHelpDsk**

  **Tipo**: Grupo de Domínios

  **Descrição**: Grupo de acesso de usuários do MbaM Helpdesk: grupo de usuários de domínio cujos membros têm acesso às áreas Gerenciar TPM e Recuperar Unidade do Site de Administração e Monitoramento do MBAM. As pessoas que têm essa função devem preencher todos os campos quando usarem qualquer opção. Isso inclui o domínio e o nome da conta do usuário.

  **Funções de conta (durante a configuração do MBAM)**: Usuários do MbaM Helpdesk

* **MBAMRUGrp**

  **Tipo**: Grupo de Domínios

  **Descrição**: Grupo de usuários de domínio cujos membros têm acesso somente leitura aos relatórios na área Relatórios do Site de Administração e Monitoramento.

  **Funções de conta (durante a configuração do MBAM)**:

  1. Relata o grupo de acesso de domínio somente leitura

  2. Grupo de acesso de usuários de relatório do MBAM

### <a name="step-3-optional-configure-and-install-ssl-certificate-on-administration-and-monitoring-server"></a>Etapa 3 (Opcional): Configurar e instalar o certificado SSL no servidor de administração e monitoramento

Embora seja opcional, é altamente recomendável que você use um certificado para ajudar a proteger a comunicação entre o Cliente MBAM e o Site de Administração e Monitoramento e os sites Self-Service Portal. Não recomendamos que você use certificados auto-assinados por motivos óbvios de segurança. Sugerimos que você use um Certificado de Tipo de Servidor Web de uma Autoridade de Certificação confiável. Para fazer isso, você pode consultar a seção "Usando Certificado Aprovado pela Autoridade de Certificação" de [KB 2754259](https://support.microsoft.com/help/2754259).

Depois que o certificado for emitido, você deverá adicionar o certificado ao armazenamento pessoal do Servidor de Administração e Monitoramento. Para adicionar o certificado, abra o armazenamento certificados no computador local. Para fazer isso, siga estas etapas:

1. Selecione Iniciar com o direito e selecione Executar.

   ![Selecione.](images/deploying-MBAM-2.png)

2. Digite "MMC.EXE" (sem aspas) e selecione **OK**.

   ![Caixa executar.](images/deploying-MBAM-3.png) 

3. Selecione **Arquivo** no novo MMC que você abriu e selecione **Adicionar/Remover Snap-in**.
   
   ![Selecione.](images/deploying-MBAM-4.png)

4. Realça o snap-in **Certificados** e selecione **Adicionar**.

   ![Adicionar ou remover janela snap-ins.](images/deploying-MBAM-5.png)

5. Selecione a **opção Conta de** computador e selecione **Next**.
   
   ![Janela de snap-in certificados.](images/deploying-MBAM-6.png)

6. Selecione **Computador Local** na próxima tela e selecione **Concluir**.
   
   ![Selecione Janela Computador.](images/deploying-MBAM-7.png)

7. Agora você adicionou o snap-in Certificados. Isso permitirá que você trabalhe com quaisquer certificados no armazenamento de certificados do computador.

   ![Adicionar ou remover janela snap-ins.](images/deploying-MBAM-8.png)

8. Importe o certificado do servidor Web para o armazenamento de certificados do computador.

   Agora que você tem acesso ao snap-in Certificados, você pode importar o certificado do servidor Web para o armazenamento de certificados do computador. Para fazer isso, siga as próximas etapas.

9. Abra o snap-in Certificados (Computador Local) e navegue até **Personal** e, em **seguida, Certificados**.
   
   ![Janela de snap-in Certificados (Computador Local).](images/deploying-MBAM-9.png)

   > [!Note]
   > O snap-in Certificados pode não estar listado. Se não estiver, nenhum certificado será instalado.

10. Selecione **Certificados com a direita,** selecione **Todas as Tarefas**e selecione **Importar**.

    ![Janela de snap-in Certificados (Computador Local).](images/deploying-MBAM-10.png)

11. Quando o assistente for iniciado, selecione **Next**. Navegue até o arquivo que você criou que contém seu certificado de servidor e chave privada e selecione **Next**.

    ![Janela Do Assistente de Importação de Certificados.](images/deploying-MBAM-11.png)

12. Insira a senha se você especificou uma para o arquivo quando a criou.

   ![Insira a janela senha.](images/deploying-MBAM-12.png)

   > [!Note]
   > Certifique-se de que a opção Marcar a chave como **exportável** está selecionada se você deseja ser capaz de exportar o par de chaves novamente deste computador. Como medida de segurança adicionada, talvez você queira deixar essa opção des limpa para garantir que ninguém possa fazer um backup da sua chave privada.
 
13. Selecione **Próximo**e, em seguida, selecione o Armazenamento de **Certificados** para o qual você deseja salvar o certificado.

    ![Janela Do Assistente de Importação de Certificados.](images/deploying-MBAM-13.png)

    > [!Note]
    > Você deve selecionar **Pessoal**, porque é um certificado de servidor Web. Se você incluiu o certificado na hierarquia de certificação, ele também será adicionado a esse armazenamento.
 
14. Selecione **Próximo**e, em seguida, selecione **Concluir**.

    ![Janela Do Assistente de Importação de Certificados.](images/deploying-MBAM-14.png)

Agora você verá o certificado de servidor para seu servidor Web na lista De certificados pessoais. Ele será anotado pelo nome comum do servidor. (Você pode encontrar isso na seção assunto do certificado.)

Para mais referências:

[Considerações sobre segurança do MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planejamento de formas para proteger os sites do MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

A próxima etapa é registrar um nome de princípio de serviço para a conta do pool de aplicativos.

### <a name="step-4-configuring-ssl-certificate-for-mbam-web-server"></a>Etapa 4: Configurando o certificado SSL para o MBAM Web Server

Se você estiver usando a comunicação SSL entre o cliente e o servidor, certifique-se de que o certificado tenha OIDs de Uso de Chave Aprimoradas (1.3.6.1.5.5.7.3.1) e (1.3.6.1.5.5.7.3.2). Ou seja, você deve garantir que a Autenticação do Servidor e a Autenticação do Cliente sejam adicionadas.

Se você receber um erro de certificado ao tentar procurar URLs de serviço, você está usando um certificado emitido para um nome diferente ou você está navegando usando uma URL incorreta.

Embora o navegador possa solicitar uma mensagem de erro de certificado, mas permitir que você continue, o serviço Web do MBAM não ignorará erros de certificado e bloqueará a conexão. Você observará erros relacionados a certificados no log de eventos de Administrador do MBAM do cliente MBAM. Se você estiver usando um alias para se conectar ao servidor de Administração e Monitoramento, deverá emitir um certificado para o nome do alias. Ou seja, o nome do assunto do certificado deve ser o nome de alias e o nome DNS do servidor local deve ser adicionado ao campo **Nome** Alternativo do Assunto do certificado.

Exemplo:

Se o nome virtual for "bitlocker.contoso.com" e o nome do servidor de Administração e Monitoramento do MBAM for "adminserver.contoso.com", o certificado deverá ser emitido para bitlocker.contoso.com (nome do assunto) e adminserver.contoso.com deve ser adicionado ao campo **Nome** Alternativo do Assunto do certificado.

Da mesma forma, se você tiver vários servidores de Administração e Monitoramento instalados para equilibrar a carga usando um balanceador de carga, você deve emitir o certificado SSL para o nome virtual. Ou seja, o campo nome do assunto do certificado deve ter o nome virtual e os nomes de todos os servidores locais devem ser adicionados no campo **Nome** Alternativo do Assunto do certificado.

Exemplo:

Se o nome virtual for "bitlocker.contoso.com" e os servidores são "adminserver1.contoso.com" e "adminiserver2.contoso.com", o certificado deve ser emitido para bitlocker.contoso.com (nome do assunto) e adminserver1.contoso.com, e adminiserver2.contoso.com deve ser adicionado ao campo **Nome** Alternativo do Assunto do certificado.

As etapas para configurar a comunicação SSL usando o MBAM são descritas no seguinte artigo da Base de Dados de Conhecimento: [KB 2754259](https://support.microsoft.com/help/2754259).

### <a name="step-5-register-spns-for-the-application-pool-account-and-configure-constrained-delegation"></a>Etapa 5: Registrar SPNS para a conta do pool de aplicativos e configurar a delegação restrita

> [!Note]
> A delegação restrita é necessária apenas para 2,5 e não é necessária para 2,5 Service Pack 1 e posterior.

Para permitir que os servidores MBAM autententem a comunicação do Site de Administração e Monitoramento e do Portal Self-Service, você deve registrar um SpN (Nome de Entidade de Serviço) para o nome do host na conta de domínio que você está usando para o pool de aplicativos Web. O artigo a seguir contém instruções passo a passo para registrar SPNs: [Planning How to Secure the MBAM Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Depois de configurar o SPN, você deve configurar a delegação restrita no SPN. Para fazer isso, siga estas etapas:

1. Vá para o Active Directory e encontre as credenciais do pool de aplicativos que você configurou para sites do MBAM nas etapas anteriores.

2. Clique com o botão direito do mouse nas credenciais e selecione **propriedades**.

3. Selecione a **guia delegação.**

4. Selecione a opção para autenticação Kerberos.

5. Selecione **procurar**e procurar novamente as credenciais do pool de aplicativos. Em seguida, você deve ver todos os SPNs que estão definidos na conta creds do pool de aplicativos. (O SPN deve se parecer com "http/bitlocker.fqdn.com"). Realça o SPN que é o mesmo que o nome de host especificado durante a instalação do MBAM.

6. Clique em **OK**.

Agora você é bom com pré-requisitos. Nas próximas etapas, você instalará o software MBAM nos servidores e o configurará.

## <a name="installing-and-configuring-mbam-25-server-software"></a>Instalando e configurando o software de servidor do MBAM 2.5

### <a name="step-6-install-mbam-25-server-software"></a>Etapa 6: Instalar o software de servidor MBAM 2.5 

Para instalar o software do MBAM Server usando o assistente de Instalação de Administração e Monitoramento do Microsoft BitLocker no Servidor de Banco de Dados e no Servidor de Administração e Monitoramento, siga estas etapas.

1. No servidor no qual você deseja instalar o MBAM, execute o MBAMserversetup.exe para iniciar o assistente de Instalação de Monitoramento e Administração do Microsoft BitLocker.

2. Na página Bem-vindo, selecione **Próximo**.

3. Leia e aceite o Contrato de Licença de Software da Microsoft e selecione **Próximo** para continuar a instalação.

4. Decida se deve usar o Microsoft Update ao verificar se há atualizações e selecione **Next**.

5. Decida se participará do Programa de Aperfeiçoamento da Experiência do Cliente e selecione **Next**.

6. Para iniciar a instalação, selecione **Instalar**.

7. Para configurar os recursos do servidor depois que o software do MBAM Server terminar de instalar, marque a caixa de seleção Executar **Configuração do Servidor MBAM** depois que o assistente fechar. Ou, você pode configurar o MBAM posteriormente usando o atalho configuração do **servidor MBAM** que a instalação do servidor cria no **menu** Iniciar.

8. Selecione **Concluir**.

Para obter mais informações, [consulte Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### <a name="step-7-configure-mbam-25-database-and-reports-role"></a>Etapa 7: Configurar a função de banco de dados e relatórios do MBAM 2.5

Nesta etapa, configuraremos os bancos de dados do MBAM 2.5 e o componente de relatório usando o Assistente de MBAM:

1. Configure o Banco de Dados de Conformidade e Auditoria e o Banco de Dados de Recuperação usando o assistente:
   
   1. No servidor no qual você deseja configurar os bancos de dados, inicie o assistente de Configuração do **Servidor DO MBAM**. Você pode selecionar **Configuração do Servidor MBAM** no menu **Iniciar** para abrir o assistente.

   2. Selecione **Adicionar Novos Recursos,** selecione Conformidade e Banco de **Dados de Auditoria,** Banco de Dados de **Recuperação**e Relatórios e selecione **Próximo**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.

   3. Se a verificação de pré-requisito for bem-sucedida, selecione **Próximo** para continuar. Caso contrário, resolva os pré-requisitos ausentes e selecione **Verificar pré-requisitos novamente**.
   
   4. Usando as descrições a seguir, insira os valores de campo no assistente:

2. Banco de dados de conformidade e auditoria

   |Campo   |Descrição|
   |-------|-------|
   |SQL Server nome |Nome do servidor no qual você está configurando o Banco de Dados de Conformidade e Auditoria. <br /> Você deve adicionar uma exceção no computador de Banco de Dados de Conformidade e Auditoria para habilitar o tráfego de entrada na SQL Server porta. O número de porta padrão é 1433.|
   |SQL Server de banco de dados    |Nome da instância do banco de dados onde os dados de conformidade e auditoria serão armazenados. Se você estiver usando a instância padrão, deverá deixar esse campo em branco. Você também deve especificar onde as informações do banco de dados estarão localizadas.|
   |Nome do banco de dados   |Nome do banco de dados que armazenará os dados de conformidade. Você deve observar o nome do banco de dados que você está especificando aqui porque você terá que fornecer essas informações em etapas posteriores.|
   |Usuário ou grupo de domínio de permissão de leitura/gravação  |Especifique o nome do usuário MBAMAppPool conforme configurado na etapa 2.|
   |Usuário ou grupo de domínio de acesso somente leitura   |Especifique o nome do usuário MBAMROUser conforme configurado na etapa 2.|

3. Banco de dados de recuperação.

   |Campo   |Descrição|
   |-----|-----|
   |SQL Server nome |Nome do servidor no qual você está configurando o Banco de Dados de Recuperação. Você deve adicionar uma exceção no computador banco de dados de recuperação para habilitar o tráfego de entrada na SQL Server porta. O número de porta padrão é 1433.|
   |SQL Server de banco de dados    |Nome da instância do banco de dados onde os dados de recuperação serão armazenados. Se você estiver usando a instância padrão, deverá deixar esse campo em branco. Você também deve especificar onde as informações do banco de dados estarão localizadas.|
   |Nome do banco de dados   |Nome do banco de dados que armazenará os dados de recuperação.|
   |Usuário ou grupo de domínio de permissão de leitura/gravação  |Usuário de domínio ou grupo que tenha permissão de leitura/gravação para esse banco de dados para permitir que os aplicativos Web acessem os dados e relatórios neste banco de dados. <br />Se você inserir um usuário nesse campo, ele deverá ter o mesmo valor que o valor no campo conta de domínio do pool de aplicativos de serviço **Web** na página Configurar Aplicativos **Web.** <br />Se você inserir um grupo neste campo, o valor no campo conta de domínio do pool de aplicativos de serviço **Web** na página Configurar Aplicativos **Web** deve ser um membro do grupo que você inserir neste campo.|
   
   Quando terminar suas entradas, selecione **Próximo**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.
   
   Se a verificação de pré-requisito for bem-sucedida, selecione **Próximo** para continuar. Caso contrário, resolva os pré-requisitos ausentes e selecione **Next novamente.**

4. Relatórios.

   |Campo   |Descrição|
   |----|----|
   |SQL Server Reporting Services instância  |Instância de SQL Server Reporting Services onde os relatórios serão configurados. Se você estiver usando a instância padrão, deverá deixar esse campo em branco.|
   |Grupo de domínios de função de relatório |Especifique o nome do MBAMRUGrp conforme mencionado na etapa 2.|
   |SQL Server nome |Nome do servidor no qual o Banco de Dados de Conformidade e Auditoria está configurado.|
   |SQL Server de banco de dados    |Nome da instância do banco de dados em que os dados de conformidade e auditoria estão configurados. Se você estiver usando a instância padrão, deverá deixar esse campo em branco. <br />Você deve adicionar uma exceção no computador Relatórios para habilitar o tráfego de entrada na porta do Reporting Server. (A porta padrão é 80.)|
   |Nome do banco de dados|  Nome do Banco de Dados de Conformidade e Auditoria. Por padrão, o nome do banco de dados é Status de Conformidade do MBAM.|
   |Conta de domínio de Banco de Dados de Conformidade e Auditoria    |Especifique o nome do usuário MBAMROUser conforme configurado na etapa 2.|
   
   Quando terminar suas entradas, selecione **Próximo**. O assistente verifica se todos os pré-requisitos para o recurso Relatórios são atendidos. Selecione Avançar para continuar. Na página **Resumo,** revise os recursos que serão adicionados.
   
   Para obter mais informações, consulte o seguinte artigo: [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### <a name="step-8-configure-the-mbam-25-web-applications-role"></a>Etapa 8: Configurar a função de aplicativos Web do MBAM 2.5

1. No servidor no qual você deseja configurar os aplicativos Web, inicie o assistente de Configuração do Servidor MBAM. Você pode selecionar **Configuração do Servidor MBAM** no menu **Iniciar** para abrir o assistente.

2. Selecione **Adicionar Novos Recursos,** selecione **Site de Administração** e Monitoramento e Portal de **Autoatendados**e selecione **Próximo**. O assistente verifica se todos os pré-requisitos para os bancos de dados são atendidos.

3. Se a verificação de pré-requisito for bem-sucedida, selecione **Próximo** para continuar. Caso contrário, resolva os pré-requisitos ausentes e selecione **Verificar pré-requisitos novamente**.

4. Use as descrições a seguir para inserir os valores de campo no assistente.

   |Campo   |Descrição|
   |-----|-----|
   |Certificado de segurança    |Selecione um certificado criado anteriormente na etapa 3 para, opcionalmente, criptografar a comunicação entre os serviços Web e o servidor no qual você está configurando o Site de Administração e Monitoramento. Se você selecionar Não usar um certificado, sua comunicação da Web pode não ser segura.|
   |Nome do host   |Nome do computador host no qual você está configurando o Site de Administração e Monitoramento. <br />Não precisa ser o nome do host do computador, pode ser qualquer coisa. No entanto, se o nome do host for diferente do nome netbios do computador, você terá que criar um registro A e garantir que o SPN use o nome de host personalizado, não o nome netbios. Isso é comum em cenários de balanceamento de carga.|
   |Caminho de instalação   |Caminho no qual você está instalando o Site de Administração e Monitoramento.|
   |Port    |Número da porta a ser usado para comunicação do site. <br /> Você deve definir uma exceção de firewall para habilitar a comunicação por meio da porta especificada.|
   |Conta e senha de domínio do pool de aplicativos de serviço Web    |Especifique a conta de usuário e a senha do usuário MBAMAppPool conforme configurado na etapa 2. <br /> Para melhorar a segurança, de definir a conta especificada nas credenciais para ter direitos de usuário limitados. Além disso, de definir a senha da conta para nunca expirar.|

5. Verifique se a conta interna IIS_IUSRS ou a conta do pool de aplicativos foi adicionada à representação de um cliente após **a** autenticação e ao **Logoff** como um trabalho em lotes configurações de segurança local.

   Para verificar se a conta foi adicionada às configurações de segurança local, abra o **** editor de Política de Segurança **Local,** expanda **** o nó Políticas **Locais,** selecione o nó Atribuição de Direitos do Usuário e selecione Representar um cliente após **a** autenticação e Faça logoff como políticas de trabalho em lote no painel direito.

6. Use as descrições de campo a seguir para configurar as informações de conexão no assistente para o Banco de Dados de Conformidade e Auditoria.
   |Campo   |Descrição|
   |------|------|
   |SQL Server nome |Nome do servidor no qual o Banco de Dados de Conformidade e Auditoria está configurado.|
   |SQL Server de banco de dados    |Nome da instância de SQL Server (por exemplo) e na qual o Banco de Dados de Conformidade e Auditoria \<Server Name\> está configurado. Deixe isso em branco se você estiver usando a instância padrão.|
   |Nome do banco de dados   |Nome do Banco de Dados de Conformidade e Auditoria. Por padrão, é "Status de Conformidade do MBAM".|

7. Use as descrições de campo a seguir para configurar as informações de conexão no assistente para o Banco de Dados de Recuperação.
   |Campo   |Descrição|
   |----|----|
   |SQL Server nome |Nome do servidor no qual o Banco de Dados de Recuperação está configurado.|
   |SQL Server de banco de dados    |Nome da instância de SQL Server (por exemplo, ) na qual o Banco de Dados \<Server Name\> de Recuperação está configurado. Deixe isso em branco se você estiver usando a instância padrão.|
   |Nome do banco de dados   |Nome do Banco de Dados de Recuperação. Por padrão, é "Recuperação de MBAM e Hardware".|

8. Use as descrições a seguir para inserir os valores de campo no assistente para configurar o Site de Administração e Monitoramento.
   |Campo   |Descrição|
   |----|----|
   |Grupo de domínio de função de Ajuda Avançada |Especifique o nome do Grupo MBAMAdvHelpDsk conforme configurado na etapa 2.|
   |Grupo de domínios de função helpdesk  |Especifique o nome do Grupo MBAMHelpDsk conforme configurado na etapa 2.|
   |Usar System Center Configuration Manager Integração |Selecione para limpar essa caixa de seleção.     |
   |Grupo de domínios de função de relatório |Especifique o nome do Grupo MBAMRUGrp conforme configurado na etapa 2.    |
   |SQL Server Reporting Services URL   |Especifique a URL do Serviço Web para o servidor SSRS no qual os relatórios do MBAM estão configurados. Você pode encontrar essas informações entrando no Reporting Services Configuration Manager no Servidor de Banco de Dados. <br /> Exemplo de um nome de domínio totalmente qualificado: https://MyReportServer.Contoso.com/ReportServer <br />Exemplo de um nome de host personalizado: https://MyReportServer/ReportServer|
   |Diretório virtual   |Diretório virtual do Site de Administração e Monitoramento. Esse nome corresponde ao diretório físico do site no servidor e é anexado ao nome de host do site. Por exemplo: <br />http(s):// *\<host name\>* : *\<port\>* /HelpDesk/ <br />Se você não especificar um diretório virtual, o valor HelpDesk será usado.     |

9. Use a descrição a seguir para inserir os valores de campo no assistente para configurar a Self-Service Portal.

   |Campo   |Descrição|
   |----|----|
   |Diretório virtual   |Diretório virtual do aplicativo Web. Esse nome corresponde ao diretório físico do site no servidor e é anexado ao nome de host do site. Por exemplo:<br />http(s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Se você não especificar um diretório virtual, o valor "SelfService" será usado.|

10. Quando terminar suas entradas, selecione **Próximo**. O assistente verifica se todos os pré-requisitos para os aplicativos Web são atendidos.

11. Selecione **Próximo** para continuar.

12. Na página **Resumo,** revise os recursos que serão adicionados.

13. Selecione **Adicionar** para adicionar os aplicativos Web ao servidor e selecione **Fechar**.

## <a name="customizing-and-validating-steps-after-installing-mbam-25-server-software"></a>Personalização e validação de etapas após a instalação do software de servidor do MBAM 2.5

### <a name="step-9-customizing-the-self-server-portal-for-your-organization"></a>Etapa 9: Personalização do portal de auto-servidor para sua organização

Para personalizar o portal Self-Service adicionando texto de aviso personalizado, nome da empresa, ponteiros para mais informações e assim por diante, consulte Personalização do portal Self-Service para sua [organização.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)
 
### <a name="step-10-configure-the-self-server-portal-if-client-computers-cannot-access-the-cdn"></a>Etapa 10: Configurar o portal de auto-servidor se os computadores cliente não puderem acessar o CDN 

Determine se seus computadores clientes têm acesso ao microsoft AJAX Rede de Distribuição de Conteúdo (CDN). O CDN fornece ao portal Self-Service acesso necessário a determinados arquivos JavaScript. Se você não configurar o portal Self-Service quando os computadores cliente não puderem acessar o CDN, somente o nome da empresa e a conta na qual o usuário se inscreveu serão exibidos. Nenhuma mensagem de erro será mostrada.

Siga um destes procedimentos:

* Se os computadores clientes têm acesso à CDN, não faça nada. Sua configuração Self-Service Portal está concluída.

* Se os computadores clientes não têm acesso ao CDN, siga as etapas em Como configurar o portal Self-Service quando os computadores cliente não podem acessar o [Microsoft Rede de Distribuição de Conteúdo](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### <a name="step-11-validate-the-mbam-25-server-feature-configuration"></a>Etapa 11: Validar a configuração do recurso do servidor MBAM 2.5 

Para validar sua implantação do MBAM Server para usar a topologia autônoma, siga estas etapas.

1. Em cada servidor no qual um recurso MBAM é implantado, selecione **Programas**e Recursos do Painel de  >  ****  >  **Controle.** Verifique se a Administração e o Monitoramento do **Microsoft BitLocker** aparecem na lista **Programas e Recursos.**
   > [!Note]
   > Para executar a validação, você deve usar uma conta de domínio que tenha credenciais administrativas de computador local em cada servidor.

2. No servidor no qual o Banco de Dados de Recuperação está configurado, abra o SQL Server Management Studio e verifique se o banco de dados de Recuperação e Hardware do **MBAM** está configurado.

3. No servidor em que o Banco de Dados de Conformidade e Auditoria está configurado, abra o SQL Server Management Studio e verifique se o Banco de Dados de Status de Conformidade do MBAM está configurado.

4. No servidor onm em que o recurso Relatórios está configurado, abra um navegador da Web usando credenciais administrativas e navegue até a página inicial do site SQL Server Reporting Services site.
   
   O local de página inicial padrão de uma SQL Server Reporting Services site é o seguinte: http(s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Para encontrar a URL real, use a ferramenta Reporting Services Configuration Manager e selecione as instâncias especificadas durante a instalação.
   
5. Verifique se uma pasta de relatórios chamada Administração e Monitoramento do Microsoft BitLocker contém uma fonte de dados chamada MaltaDataSource. Essa fonte de dados contém pastas que têm nomes que representam localidades de idioma (por exemplo, en-us). Os relatórios estão nas pastas de idioma.

   > [!Note]
   > Se SQL Server Reporting Services (SSRS) foi configurada como uma instância nomeada, a URL deve se parecer com o seguinte: http(s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Se o SSRS não estiver configurado para usar o SSL (Secure Socket Layer), a URL dos relatórios será definida como "HTTP" em vez de "HTTPS" ao instalar o servidor MBAM. Se você, em seguida, for para o Site de Administração e Monitoramento (também conhecido como Helpdesk) e selecionar um relatório, receberá a seguinte mensagem: "Somente Conteúdo Seguro é Exibido". Para mostrar o relatório, selecione **Mostrar Todo o Conteúdo**.

6. No servidor no qual o recurso Site de Administração e Monitoramento **** está configurado, execute o Gerenciador de Servidores, navegue até Funções e selecione **Web Server (IIS)**  >  **Serviços de Informações da Internet (IIS).**

7. Em **Conexões,** navegue até \<computer name\> e selecione **Sites**  >  **Microsoft BitLocker Administration and Monitoring**. Verifique se os seguintes estão listados:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. No servidor no qual o Site de Administração e Monitoramento e o Portal Self-Service estão configurados, abra um navegador da Web usando credenciais administrativas.

9. Navegue até os seguintes sites para verificar se eles carregam com êxito:
   * https(s):// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/ (confirme cada link para navegação e relatórios)
   * http(s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Presume-se que você configurou os recursos do servidor na porta padrão sem criptografia de rede. Se você configurou os recursos do servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada. Por exemplo: http(s):// \<host name\> : \<port\> /HelpDesk/ http(s):// : / Se os recursos do servidor foram configurados para usar criptografia de rede, altere o http:// \<host name\> \<port\> / \<virtualdirectory\> para https://.
   
10. Navegue até os seguintes serviços Web para verificar se eles são carregados com êxito. Uma página é aberta para indicar que o serviço está sendo executado. No entanto, a página não exibe metadados.

    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### <a name="step-12-configure-the-mbam-group-policy-templates"></a>Etapa 12: Configurar os modelos de política de Grupo do MBAM

Para implantar o MBAM, você precisa definir as configurações da Política de Grupo que definem as configurações de implementação do MBAM para Criptografia de Unidade do BitLocker. Para concluir essa tarefa, você deve copiar os modelos de Política de Grupo do MBAM para um servidor ou estação de trabalho que possa executar o GPMC (Console de Gerenciamento de Política de Grupo) ou o AgPM (Gerenciamento Avançado de Política de Grupo) e editar as configurações.

> [!Important]
> Não altere as configurações da Política de Grupo no **nó BitLocker Drive Encryption** ou o MBAM não funcionará corretamente. Quando você configura as configurações da Política de Grupo no nó **MDOP MBAM (Gerenciamento do BitLocker),** o MBAM configura automaticamente as configurações de Criptografia de Unidade do **BitLocker** para você.
 
#### <a name="copying-the-mbam-25-group-policy-templates"></a>Copiando os modelos de Política de Grupo do MBAM 2.5

Antes de instalar o Cliente MBAM, você deve copiar GPOs (Objetos de Política de Grupo) específicos do MBAM para a estação de trabalho de gerenciamento. Esses GPOs definem as configurações de implementação do MBAM para o BitLocker. Você pode copiar os modelos de Política de Grupo para qualquer servidor ou estação de trabalho que seja um servidor baseado em Windows ou computador cliente com suporte e que possa executar o GPMC (Console de Gerenciamento de Política de Grupo) ou o Gerenciamento Avançado de Política de Grupo (AGPM).

Para obter mais informações, [consulte Copying the MBAM 2.5 Group Policy Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### <a name="editing-mbam-25-gpo-settings"></a>Editar configurações de GPO do MBAM 2.5

Depois de criar os GPOs necessários, você deve implantar as configurações da Política de Grupo do MBAM nos computadores cliente da sua organização. Para exibir e criar GPOs, você deve ter o Console de Gerenciamento de Política de Grupo (GPMC) ou o AGPM (Gerenciamento Avançado de Política de Grupo) instalado.

Para obter mais informações, consulte [Editing the MBAM 2.5 Group Policy Configurações](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) [and Planning for MBAM 2.5 Group Policy Requirements](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### <a name="step-13-deploying-the-mbam-25-client"></a>Etapa 13: Implantando o cliente MBAM 2.5

Dependendo de quando você implantar o software microsoft BitLocker Administration and Monitoring Client, você pode habilitar o BitLocker em um computador em sua organização antes que o usuário receba o computador ou depois configurando a Política de Grupo e implantando o software cliente MBAM usando um sistema de implantação de software empresarial.
 
#### <a name="deploy-the-mbam-client-to-desktop-or-portable-computers"></a>Implantar o cliente MBAM em computadores desktop ou portáteis

Depois de configurar as configurações da Política de Grupo, você pode usar um produto do sistema de implantação de software empresarial, como o Microsoft System Center 2012 Configuration Manager ou o Active Directory Domain Services (AD DS) para implantar os arquivos de instalação do cliente MBAM Windows Installer para os computadores de destino. Você pode usar os arquivos MbamClientSetup.exe de 32 ou 64 bits ou os arquivos MBAMClient.msi de 32 ou 64 bits. Eles são fornecidos juntamente com o software cliente MBAM.

Para obter mais informações, [consulte How to Deploy the MBAM Client to Desktop or Laptop Computers](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### <a name="deploy-the-mbam-client-as-part-of-a-windows-deployment"></a>Implantar o Cliente MBAM como parte de uma implantação Windows implantação

Em organizações nas quais os computadores são recebidos e configurados centralmente, você pode instalar o Cliente MBAM para gerenciar a Criptografia de Unidade do BitLocker em cada computador antes que qualquer dado do usuário seja gravado nele. O benefício desse processo é que todos os computadores são compatíveis com o BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma suposição importante para esse cenário é que a política da organização é instalar uma imagem de Windows corporativa antes que o computador seja entregue ao usuário. Se as configurações da Política de Grupo estão configuradas para exigir um PIN, os usuários são solicitados a definir um PIN após receberem a política.

Para obter mais informações, [consulte How to Deploy the MBAM Client as Part of a Windows Deployment](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### <a name="how-to-deploy-the-mbam-client-by-using-a-command-line"></a>Como implantar o cliente MBAM usando uma linha de comando

Para obter mais [informações, consulte How to Deploy the MBAM Client by Using a Command Line](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### <a name="post-deployment-of-clients"></a>Pós-implantação de clientes

Agora que você concluiu a atividade de implantação, você deve revisar os logs a seguir e determinar se os clientes estão relatando com êxito para o banco de dados do MBAM.

## <a name="faq"></a>Perguntas frequentes

### <a name="how-to-create-a-load-balanced-iis-servers"></a>Como criar servidores IIS balanceados de carga

* O SPN deve ser registrado apenas no nome amigável (por exemplo: bitlocker.corp.net) e não deve ser registrado em servidores individuais do IIS.

* Se um certificado for usado, o certificado deverá ter nomes FQDN e NetBIOS inseridos no campo Nome Alternativo de Assunto para todos os servidores do IIS no grupo de balanceio de carga e também como o Nome Amigável (por exemplo: bitlocker.corp.net). **** Caso contrário, o certificado será relatado como não confiável pelo navegador quando você procurar endereços balanceados de carga.

Para obter mais informações, consulte [IIS Network Load Balancing and](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) [Registering SPNs for the application pool account](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### <a name="how-to-configure-a-certificate"></a>Como configurar um certificado

* Você terá que ter dois certificados. Um certificado é usado para SQL servidor e o outro é usado para o IIS. Eles devem ser instalados antes de iniciar a instalação do MBAM.

* Recomendamos que você use o instalador para adicionar o certificado à configuração do IIS em vez de editar manualmente o arquivo web.config.

* O certificado não será aceito pelo Configurador do MBAM se o campo "Emitido para" no certificado não corresponder ao nome do servidor. Nesse caso, crie temporariamente um certificado auto-assinado no Console do IIS e use-o no Configurador. Isso garantirá que os Aplicativos Web sejam instalados para SSL e HTTPS. Depois disso, você pode alterar o certificado para um de vinculações do IIS para o site do MBAM.

### <a name="the-sql-permissions-requirement-for-installation"></a>O SQL de permissões para instalação

Crie uma conta para o Pool de Aplicativos do MBAM e dê a ele apenas permissões SecurityAdmin, Public e DBCreator.

Consulte [Configuração do banco de dados do MBAM – permissões mínimas](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) para obter mais informações.

> [!Note]
> * Em algumas situações, mais permissões são necessárias para as operações iniciais de instalação e atualização.
> * Use uma conta que tenha SA temporária para a instalação.
> * Não inicie o Configurador no contexto de uma conta de usuário (Executar Como) que não tenha permissões suficientes para fazer alterações no SQL Server porque isso causará erros de instalação.
> * Você deve estar conectado usando uma conta que tenha permissões SQL Server. Somente SQL Server bancos de dados podem ser criados ou atualizados executando o Configurator do MBAM remotamente. Para o servidor SSRS, você deve instalar o MBAM e executar o Configurator localmente para instalar ou atualizar os relatórios do SSRS do MBAM.

### <a name="the-permission-required-for-spn-registration"></a>A permissão necessária para o Registro spn

Uma conta usada para a instalação do portal do IIS deve ter permissões Write ServicePrincipalName e Write Validated SPN. Sem essas permissões, a instalação retornará uma mensagem de aviso informando que não pode registrar o SPN.

> [!Note]
> Você receberá esta mensagem de aviso duas vezes. Isso não significa que o SPN deve ter dois objetos registrados nele.

Para obter mais informações, [consulte MbaM Setup fails with "Register SPN Deferred" error message](https://support.microsoft.com/help/2754138/).

### <a name="did-i-have-to-update-the-admx-templates-to-the-latest-version"></a>Tive que atualizar os modelos ADMX para a versão mais recente?

Você verá várias opções de sistema operacional no nó raiz do MBAM para GPO depois de atualizar os modelos ADMX para suas versões mais recentes. Por exemplo, Windows 7, Windows 8.1 e Windows 10 versão 1511 e versões posteriores.

Para obter mais informações sobre como atualizar os modelos ADMX, consulte os seguintes artigos:
* [Como baixar e implantar os modelos de Política de Grupo do MDOP (.admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planejamento para os requisitos de Política de Grupo do MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modelos administrativos da Política de Grupo do Pacote de Otimização da Área de Trabalho da Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
