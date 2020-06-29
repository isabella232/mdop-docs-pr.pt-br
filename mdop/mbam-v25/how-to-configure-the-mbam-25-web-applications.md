---
title: Como configurar os aplicativos Web do MBAM 2.5
description: Como configurar os aplicativos Web do MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799484"
---
# Como configurar os aplicativos Web do MBAM 2.5


Este tópico explica como configurar os aplicativos da Web do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para a [arquitetura de alto nível recomendada para o MBAM 2,5](high-level-architecture-for-mbam-25.md) usando um dos seguintes métodos:

-   Um cmdlet do Windows PowerShell

-   O assistente de configuração do servidor do MBAM

Os aplicativos Web incluem os seguintes websites e seus serviços Web correspondentes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Website</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Site de administração e monitoramento</p></td>
<td align="left"><p>Site em que os usuários especificados podem exibir relatórios e ajudar os usuários finais a recuperarem seus computadores quando eles esquecem seu PIN ou senha</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portal de autoatendimento</p></td>
<td align="left"><p>O website que os usuários finais podem acessar para restabelecer o acesso de forma independente a seus computadores se eles esquecerem do PIN ou da senha</p></td>
</tr>
</tbody>
</table>



**Antes de iniciar a configuração:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Onde obter instruções</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Examine a arquitetura recomendada para MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitetura de alto nível do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Examine as configurações com suporte para MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complete os pré-requisitos obrigatórios em cada servidor.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Certifique-se de configurar o SSRS (serviços do SQL ServerReporting) para usar a SSL (Secure Sockets Layer) antes de configurar o site de administração e monitoramento. Caso contrário, o recurso relatórios irá usar HTTP em vez de HTTPS.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5-pré-requisitos do servidor que se aplicam somente à topologia de integração do Configuration Manager </a> (se aplicável)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Registre os SPNs (nomes de entidade de serviço) da conta do pool de aplicativos para os sites. Você só precisará fazer esta etapa se não tiver direitos de domínio administrativo nos serviços de domínio Active Directory (AD DS). Se você tiver esses direitos no AD DS, o MBAM criará os SPNs para você.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Planejamento de formas para proteger os sites do MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você planeja instalar os sites em um servidor e nos serviços Web em outro, poderá configurá-los somente usando o <strong> cmdlet Enable-MbamWebApplication do </strong> Windows PowerShell. O assistente de configuração do servidor do MBAM não dá suporte à configuração desses itens em servidores separados.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets para configurar os recursos do MBAM Server.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar os aplicativos Web usando o Windows PowerShell**

1.  Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.

2.  Use o cmdlet **Enable-MbamWebApplication** para configurar os aplicativos Web usando o Windows PowerShell. Para obter informações sobre esse cmdlet, digite **Get-Help Enable-MbamWebApplication**.

**Para definir as configurações de todos os aplicativos Web usando o assistente**

1. No servidor em que você deseja configurar os aplicativos Web, inicie o assistente de configuração do MBAM Server. Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.

2. Clique em **Adicionar novos recursos**, selecione **site de administração e monitoramento** e portal de **autoatendimento**e clique em **Avançar**. O assistente verifica se todos os pré-requisitos para os aplicativos da Web foram atendidos.

3. Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar. Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.

4. Use as descrições a seguir para inserir os valores de campo no assistente.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Campo</strong></th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Certificado de segurança</strong></p></td>
   <td align="left"><p>Selecione um certificado criado anteriormente para criptografar opcionalmente a comunicação entre os serviços Web e o servidor no qual você está configurando os sites. Se você optar <strong> por não usar um certificado </strong> , talvez sua comunicação à Web não seja segura.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Nome do host</strong></p></td>
   <td align="left"><p>Nome do computador host em que você está configurando os sites.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Caminho de instalação</strong></p></td>
   <td align="left"><p>Caminho onde você está instalando os sites.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Número da porta a ser usado para a comunicação de site e serviço.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você deve definir uma exceção de firewall para permitir a comunicação por meio da porta especificada.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Conta e senha de domínio do pool de aplicativos do serviço Web</strong></p></td>
   <td align="left"><p>Conta de usuário do domínio e senha para o pool de aplicativos de serviço Web.</p>
   <p>Se você inserir um nome de usuário no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , você deverá digitar esse mesmo valor neste campo.</p>
   <p>Se você inserir um nome de grupo no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , o valor que você inserir nesse campo deverá ser um membro desse grupo.</p>
   <p>Se você não especificar credenciais, as credenciais que foram especificadas para qualquer aplicativo da Web habilitado anteriormente serão usadas. Todos os aplicativos Web devem usar as mesmas credenciais de pool de aplicativos. Se você especificar credenciais diferentes para diferentes aplicativos da Web, o valor especificado mais recentemente será usado.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Para aumentar a segurança, defina a conta especificada nas credenciais para ter direitos de usuário limitados. Além disso, defina a senha da conta para nunca expirar.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Verifique se a conta interna do IIS \ _IUSRS ou a conta do pool de aplicativos foi adicionada às configurações de segurança local de **um cliente após autenticação** e **logon como um trabalho em lotes** .

   Para verificar se ela foi adicionada às configurações de segurança locais, abra o **Editor de política de segurança local**, expanda o nó **políticas locais** , clique no nó **atribuição de direitos de usuário** e clique duas vezes em **representar um cliente após autenticação** e **faça logon como uma** política de trabalho em lotes no painel direito.

**Para configurar informações de conexão para bancos de dados usando o assistente**

1.  Use as descrições de campo a seguir para configurar as informações de conexão no Assistente para o banco de dados de conformidade e auditoria.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome do SQL Server</strong></p></td>
    <td align="left"><p>Nome do servidor em que o banco de dados de conformidade e auditoria está configurado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instância de banco de dados do SQL Server</strong></p></td>
    <td align="left"><p>Nome da instância do SQL Server na qual o banco de dados de conformidade e auditoria está configurado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nome do banco de dados</strong></p></td>
    <td align="left"><p>Nome do banco de dados de conformidade e auditoria.</p></td>
    </tr>
    </tbody>
    </table>



2.  Use as descrições de campo a seguir para configurar as informações de conexão no assistente do banco de dados de recuperação.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome do SQL Server</strong></p></td>
    <td align="left"><p>Nome do servidor em que o banco de dados de recuperação está configurado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instância de banco de dados do SQL Server</strong></p></td>
    <td align="left"><p>Nome da instância do SQL Server na qual o banco de dados de recuperação está configurado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nome do banco de dados</strong></p></td>
    <td align="left"><p>Nome do banco de dados de recuperação.</p></td>
    </tr>
    </tbody>
    </table>



**Para configurar os aplicativos Web usando o assistente**

1. Use as descrições a seguir para inserir os valores de campo no Assistente para configurar o site de administração e monitoramento.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Grupo de domínio da função helpdesk avançado</strong></p></td>
   <td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso a todas as áreas do site Administração e monitoramento, exceto a área relatórios.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de domínio da função helpdesk</strong></p></td>
   <td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso às <strong> áreas gerenciar TPM </strong> e <strong> unidade </strong> de recuperação do site de administração e monitoramento.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Usar a integração do System Center Configuration Manager</strong></p></td>
   <td align="left"><p>Marque esta caixa de seleção se você estiver configurando o MBAM com a topologia de integração do Configuration Manager. Marcar essa caixa de seleção faz com que todos os relatórios, exceto o relatório de auditoria de recuperação, sejam exibidos no Configuration Manager em vez de no site de administração e monitoramento.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de domínio da função de relatório</strong></p></td>
   <td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso somente leitura à área relatórios do site de administração e monitoramento.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>URL do SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>URL para o servidor SSRS em que os relatórios do MBAM são configurados.</p>
   <p>Exemplos de URLs de relatório:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo de nome do host</th>
   <th align="left">Exemplo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Exemplo com um nome de domínio totalmente qualificado</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Exemplo com um nome de host personalizado</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Diretório virtual</strong></p></td>
   <td align="left"><p>Diretório virtual do site Administração e monitoramento. Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site, por exemplo:</p>
   <p>http (s):// &lt; <em> nome do host </em> &gt; : &lt; <em> porta </em> &gt; /helpdesk/</p>
   <p>Se você não especificar um diretório virtual, o valor da <strong> assistência técnica </strong> será usado.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Grupo de domínio da função </strong> de migração de dados (opcional)</p></td>
   <td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso para usar os cmdlets Write-MBAM * para gravar informações de recuperação via este ponto de extremidade.</p></td>
   </tr>
   </tbody>
   </table>



2. Use a seguinte descrição para inserir os valores de campo no Assistente para configurar o portal de autoatendimento.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Diretório virtual</strong></p></td>
   <td align="left"><p>Diretório virtual do aplicativo Web. Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site, por exemplo:</p>
   <p>http (s):// &lt; <em> nome do host </em> &gt; : &lt; <em> porta </em> &gt; /SelfService/</p>
   <p>Se você não especificar um diretório virtual, o valor <strong> SelfService </strong> será usado.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Nome da empresa</p></td>
   <td align="left"><p>Especifique um nome de empresa para o portal de autoatendimento, por exemplo:</p>
   <p>Contoso IT</p>
   <p>O nome da empresa é exibido por todos os usuários do portal de autoatendimento.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Texto da URL do helpdesk</p></td>
   <td align="left"><p>Especifique uma instrução de texto que direcione os usuários para o website do helpdesk da sua organização, por exemplo:</p>
   <p>Assistência técnica ou departamento de ti do contato</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>URL do helpdesk</p></td>
   <td align="left"><p>Especifique a URL do site do helpdesk da sua organização, por exemplo:</p>
   <p>http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Aviso de arquivo de texto</p></td>
   <td align="left"><p>Selecione um arquivo que contenha o aviso que você deseja que seja exibido aos usuários na página inicial do portal de autoatendimento.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Não exibir texto de aviso para usuários</p></td>
   <td align="left"><p>Marque esta caixa de seleção para especificar que o texto de aviso não será exibido para os usuários.</p></td>
   </tr>
   </tbody>
   </table>



3. Quando terminar as entradas, clique em **Avançar**.

   O assistente verifica se todos os pré-requisitos para os aplicativos da Web foram atendidos.

4. Clique em **Avançar** para continuar.

5. Na página **Resumo** , examine os recursos que serão adicionados.

   **Observação**  
   Para criar um script do Windows PowerShell para as entradas feitas, clique em **Exportar script do PowerShell** e salve o script.



6. Clique em **Adicionar** para adicionar os aplicativos Web ao servidor e, em seguida, clique em **fechar**.

   Para personalizar o portal de autoatendimento adicionando texto de aviso personalizado, o nome da sua empresa, os ponteiros para obter mais informações e assim por diante, consulte [Personalizando o portal de autoatendimento da sua organização](customizing-the-self-service-portal-for-your-organization.md).

**Para configurar o portal de autoatendimento se os computadores cliente não puderem acessar a CDN**

1.  Determine se você está executando o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Em caso afirmativo, não faça nada. Sua configuração do portal de autoatendimento está completa.

    **Observação**  
    O monitoramento e administração do Microsoft BitLocker (MBAM) 2,5 SP1 instala os arquivos JavaScript na configuração e, portanto, não precisa estar conectado à rede de entrega de conteúdo do Microsoft Ajax para configurar o portal de autoatendimento. As etapas a seguir serão necessárias somente se você estiver usando uma versão do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 anterior ao SP1.



2.  Determine se seus computadores cliente têm acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax.

    A CDN oferece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript. Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, apenas o nome da empresa e a conta sob a qual o usuário final se conectou serão exibidos. Nenhuma mensagem de erro será mostrada.

3.  Siga um destes procedimentos:

    -   Se seus computadores cliente tiverem acesso à CDN, não faça nada. Sua configuração do portal de autoatendimento está completa.

    -   Se seus computadores cliente não tiverem acesso à CDN, conclua as etapas em [como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a rede de distribuição de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Tópicos relacionados


[Logs de eventos do servidor](server-event-logs.md)

[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Personalizando o Portal de Autoatendimento para sua organização](customizing-the-self-service-portal-for-your-organization.md)

[Validando a configuração de recursos de servidor do MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





