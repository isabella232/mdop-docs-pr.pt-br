---
title: Avaliando o MBAM 2.5 em um ambiente de teste
description: Avaliando o MBAM 2.5 em um ambiente de teste
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799215"
---
# Avaliando o MBAM 2.5 em um ambiente de teste


Este tópico descreve como você pode configurar um ambiente de teste para avaliar a administração e o monitoramento do Microsoft BitLocker (MBAM) 2,5 na topologia autônoma ou de integração do System Center Configuration Manager.

## Avaliando o MBAM 2,5 usando a topologia autônoma


Para avaliar o MBAM usando a topologia autônoma, use as informações contidas nas tabelas a seguir para instalar o software do servidor do MBAM e configure os recursos do servidor MBAM em seu ambiente de teste.

**Para avaliar o MBAM 2,5 usando a topologia autônoma**

1. Antes de instalar o MBAM, faça o seguinte:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verifique se você instalou todo o software de pré-requisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verifique o hardware, a RAM e outras especificações necessárias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar os cmdlets para configurar o MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale o software do servidor do MBAM e configure os recursos desejados.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Como configurar os bancos de dados do MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar o recurso relatórios.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Como configurar os relatórios do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar os aplicativos Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Como configurar os aplicativos Web do MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. Em um computador cliente, faça o seguinte:

   1.  Instale o cliente MBAM em um computador cliente.

   2.  Aplique os objetos de política de grupo do MBAM (GPOs) ao computador.

   3.  Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rápido e em intervalos regulares:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Observação**  
       Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de teste.



   4.  Reinicie o **serviço de cliente de gerenciamento BitLocker**.

## Avaliando o MBAM 2,5 usando a topologia de integração do Configuration Manager do System Center 2012


Para avaliar o MBAM usando a topologia de integração do Configuration Manager, use as informações nas tabelas a seguir para instalar o software do servidor do MBAM e configure os recursos do servidor MBAM em seu ambiente de teste. Depois de instalar o cliente MBAM em um computador cliente, você executará etapas adicionais para forçar o cliente MBAM a reportar o status do computador para o MBAM mais rápido.

**Para avaliar o MBAM 2,5 usando a topologia de integração do Configuration Manager do System Center 2012**

1. Antes de instalar o MBAM, confira o software de pré-requisito e a configuração com suporte.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verifique se você instalou todo o software de pré-requisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verifique o hardware, a RAM e outras especificações necessárias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar os cmdlets para configurar o MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Criar ou editar os arquivos. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Edite o arquivo Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Criar ou editar o arquivo Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale o software do servidor do MBAM e configure os recursos desejados.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado. Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Como configurar os bancos de dados do MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar o recurso relatórios.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Como configurar os relatórios do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar os aplicativos Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Como configurar os aplicativos Web do MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar o System Center Configuration Manager para instalar os objetos do Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. Em um computador cliente, faça o seguinte:

   1.  Instale o cliente do MBAM e o cliente do Configuration Manager em um computador cliente.

   2.  Aplicar os objetos de política de grupo do MBAM ao computador.

   3.  Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rápido e em intervalos regulares:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Observação**  
       Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de teste.



   4.  Reinicie o **serviço de cliente de gerenciamento BitLocker**.

   5.  No painel de controle, abra o **Gerenciador de configurações**e, em seguida, clique na guia **ações** .

   6.  Selecione **ciclo de inventário de hardware**e clique em **executar agora**. Esta etapa executa o inventário de hardware usando as novas classes importadas para seus arquivos. mof e, em seguida, envia os dados ao servidor do Configuration Manager.

   7.  Selecione **recuperação de política de máquina & ciclo de avaliação**e, em seguida, clique em **executar agora** para aplicar os objetos de política de grupo relevantes para esse computador cliente.



4. No console do Configuration Manager, faça o seguinte:

   1.  No painel de navegação, clique com o botão direito do mouse em **computadores com suporte do MBAM**, clique em **Atualizar Associação**e em **Sim** para forçar o computador cliente a denunciar sua associação imediatamente.

   2.  No painel de navegação, clique em **computadores com suporte MBAM** para verificar se o computador cliente aparece na coleção.

5. No computador cliente, no painel de controle, abra novamente o **Gerenciador de configuração** e faça o seguinte:

   1.  Clique na guia **ações** e, em seguida, execute novamente a **recuperação da política do computador & ciclo de avaliação**.

   2.  Clique na guia **configurações** , selecione a linha de base do BitLocker e, em seguida, clique em **avaliar**.

6. No console do Configuration Manager, verifique se o computador cliente é exibido no relatório de conformidade para empresas: da seguinte maneira:

   1.  No painel de navegação, selecione o espaço de trabalho **monitoramento** .

   2.  Na árvore de console, expanda relatórios de relatório de **visão geral** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.

   3.  Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel de resultados.

## Avaliando o MBAM 2,5 usando a topologia de integração do System Center Configuration Manager 2007


Para avaliar o MBAM usando a topologia de integração do Configuration Manager, siga as mesmas etapas para instalar e configurar o MBAM em seu ambiente de teste conforme você usa em um ambiente de produção. Depois de instalar o cliente MBAM em um computador cliente, conclua as etapas adicionais neste tópico para permitir que o cliente do MBAM comece a reportar o status do computador para o MBAM mais rápido.

**Para avaliar o MBAM usando a topologia de integração do Configuration Manager 2007**

1. Antes de instalar o MBAM, faça o seguinte:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verifique se você instalou todo o software de pré-requisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verifique o hardware, a RAM e outras especificações necessárias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Criar ou editar os arquivos. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Edite o arquivo Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Criar ou editar o arquivo Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale o software do servidor do MBAM e configure os recursos desejados.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarefa</th>
   <th align="left">Onde obter instruções</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado. Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalando o software de servidor do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Como configurar os bancos de dados do MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar o recurso relatórios.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Como configurar os relatórios do MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurar os aplicativos Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Como configurar os aplicativos Web do MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar o System Center Configuration Manager para instalar os objetos do Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. Em um computador cliente, faça o seguinte:

   1.  Instale o cliente MBAM em um computador cliente.

   2.  Aplicar os objetos de política de grupo do MBAM ao computador.

   3.  Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rapidamente e em intervalos mais rápidos:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Observação**  
       Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de avaliação.



   4.  Reinicie o **serviço de cliente de gerenciamento BitLocker**.

   5.  No painel de controle, abra o **Gerenciador de configurações**e, em seguida, clique na guia **ações** .

   6.  Selecione **recuperação de política de máquina & ciclo de avaliação**e, em seguida, clique em **executar agora** para aplicar os objetos de política de grupo relevantes para esse computador cliente.

   7.  Selecione **ciclo de inventário de hardware**e clique em **executar agora**. Esta etapa executa o inventário de hardware usando as novas classes que você importou para seus arquivos. mof e, em seguida, envia os dados ao servidor do Configuration Manager.

4. No console do Configuration Manager, faça o seguinte:

   1.  No painel de navegação, clique com o botão direito do mouse em **computadores com suporte do MBAM**, clique em **Atualizar Associação**e em **Sim** para forçar o computador cliente a denunciar sua associação imediatamente.

   2.  No painel de navegação, clique em **computadores com suporte MBAM** para verificar se o computador cliente aparece na coleção.

5. No computador cliente, no painel de controle, abra novamente o **Gerenciador de configuração** e faça o seguinte:

   1.  Clique na guia **ações** e, em seguida, execute novamente a **recuperação da política do computador & ciclo de avaliação**.

   2.  Clique na guia **configurações** , selecione a linha de base do BitLocker e clique em **avaliar**.

6. No console do Configuration Manager, verifique se o computador cliente é exibido no relatório de conformidade empresarial, da seguinte maneira

   1.  No painel de navegação, expanda **Gerenciamento de computador** &gt; **relatório** &gt; do **Reporting Services** &gt; ** &lt; Server Name &gt; MBAM**.

   2.  No nó **MBAM** , selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel de resultados.


## Tópicos relacionados


[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





