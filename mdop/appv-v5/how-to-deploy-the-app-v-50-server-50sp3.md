---
title: Como implantar o servidor do App-V 5.0
description: Como implantar o servidor do App-V 5.0
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796434"
---
# Como implantar o servidor do App-V 5.0


Use o procedimento a seguir para instalar o servidor do App-V 5,0. Para obter informações sobre a implantação do servidor do App-V 5,0 SP3, consulte [sobre o app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).

**Antes de começar:**

-   Verifique se você instalou o software de pré-requisito. Consulte [pré-requisitos do App-V 5,0](app-v-50-prerequisites.md).

-   Examine a seção de servidor das [considerações de segurança do App-V 5,0](app-v-50-security-considerations.md).

-   Especifique uma porta onde cada componente será hospedado.

-   Adicione regras de firewall para permitir que as solicitações de entrada acessem as portas especificadas.

-   Se você usar scripts SQL, em vez do Windows Installer, para configurar o banco de dados de gerenciamento ou banco de dados de relatórios, será necessário executar os scripts SQL antes de instalar o servidor de gerenciamento ou o servidor de relatórios. Veja [como implantar os bancos de dados do App-V usando scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).

**Para instalar o servidor do App-V 5,0**

1. Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.

2. Inicie a instalação do servidor do App-V 5,0 clicando com o botão direito do mouse e executando **appv\_server\_setup.exe** como administrador e, em seguida, clique em **instalar**.

3. Revise e aceite os termos de licença e escolha se deseja habilitar as atualizações da Microsoft.

4. Na página **seleção de recursos** , selecione todos os componentes a seguir.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Componente</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Servidor de gerenciamento</p></td>
   <td align="left"><p>Fornece funcionalidade de gerenciamento geral para a infraestrutura do App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Banco de dados de gerenciamento</p></td>
   <td align="left"><p>Facilita a implantação de bancos de dados para gerenciamento do App-V.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Publishing Server</p></td>
   <td align="left"><p>Fornece funcionalidade de hospedagem e streaming para aplicativos virtuais.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Servidor de relatórios</p></td>
   <td align="left"><p>Oferece o App-V 5,0 Reporting Services.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Banco de dados de relatórios</p></td>
   <td align="left"><p>Facilita a implantação de bancos de dados para relatórios do App-V.</p></td>
   </tr>
   </tbody>
   </table>

     

5. Na página **local de instalação** , aceite o local padrão onde os componentes selecionados serão instalados ou altere o local digitando um novo caminho na linha local de **instalação** .

6. Na página **criar novo banco de dados de gerenciamento** inicial, configure a instância do **Microsoft SQL Server** e o **banco de dados do servidor de gerenciamento** selecionando a opção apropriada abaixo.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Método</th>
   <th align="left">O que você precisa fazer</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Você está usando uma instância personalizada do Microsoft SQL Server.</p></td>
   <td align="left"><p>Selecione <strong> usar a instância personalizada </strong> e digite o nome da instância.</p>
   <p>Use o formato <strong> InstanceName </strong> . O local de instalação presumido é o computador local.</p>
   <p>Sem suporte: um nome de servidor usando a <strong> instância forte de Format ServerName </strong> &lt; &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Você está usando um nome de banco de dados personalizado.</p></td>
   <td align="left"><p>Selecione <strong> configuração personalizada </strong> e digite o nome do banco de dados.</p>
   <p>O nome do banco de dados deve ser exclusivo ou haverá falha na instalação.</p></td>
   </tr>
   </tbody>
   </table>

     

7. Na página **Configurar** , aceite o valor padrão **usar este computador local**.

   **Observação**  
   Se você estiver instalando o servidor de gerenciamento e o banco de dados de gerenciamento lado a lado, algumas opções nessa página não estarão disponíveis. Nesse caso, as opções apropriadas são selecionadas por padrão e não podem ser alteradas.

     

8. Na página inicial do **banco de dados criar novo relatório** , configure a **instância do Microsoft SQL Server** e o **banco de dados do servidor de relatórios** selecionando a opção apropriada abaixo.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Método</th>
   <th align="left">O que você precisa fazer</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Você está usando uma instância personalizada do Microsoft SQL Server.</p></td>
   <td align="left"><p>Selecione <strong> usar a instância personalizada </strong> e digite o nome da instância.</p>
   <p>Use o formato <strong> InstanceName </strong> . O local de instalação presumido é o computador local.</p>
   <p>Sem suporte: um nome de servidor usando a <strong> instância forte de Format ServerName </strong> &lt; &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Você está usando um nome de banco de dados personalizado.</p></td>
   <td align="left"><p>Selecione <strong> configuração personalizada </strong> e digite o nome do banco de dados.</p>
   <p>O nome do banco de dados deve ser exclusivo ou haverá falha na instalação.</p></td>
   </tr>
   </tbody>
   </table>

     

9. Na página **Configurar** , aceite o valor padrão: **Use este computador local**.

   **Observação**  
   Se você estiver instalando o servidor de gerenciamento e o banco de dados de gerenciamento lado a lado, algumas opções nessa página não estarão disponíveis. Nesse caso, as opções apropriadas são selecionadas por padrão e não podem ser alteradas.

     

10. Na página **Configurar** (configuração do servidor de gerenciamento), especifique o seguinte:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Item para configurar</th>
    <th align="left">Descrição e exemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Digite o grupo de anúncios com permissões suficientes para gerenciar o ambiente do App-V.</p></td>
    <td align="left"><p>Exemplo: MyDomain\MyUser</p>
    <p>Após a instalação, você pode adicionar mais usuários ou grupos usando o console de gerenciamento. Entretanto, não há suporte para grupos de segurança global e grupos de distribuição dos serviços de domínio Active Directory (AD DS). Você deve usar <strong> o domínio local </strong> ou <strong> grupos universais </strong> são necessários para executar essa ação.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de publicação.</p></td>
    <td align="left"><p>Se você não tiver um nome personalizado, não faça alterações.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</p></td>
    <td align="left"><p>Exemplo: <strong> 12345</strong></p>
    <p>Certifique-se de que a porta especificada não está sendo usada por outro site.</p></td>
    </tr>
    </tbody>
    </table>

     

11. Na página **Configurar** o **Publishing Server Configuration** , especifique o seguinte:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Item para configurar</th>
    <th align="left">Descrição e exemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Especifique a URL para o serviço de gerenciamento.</p></td>
    <td align="left"><p>Exemplo<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de publicação.</p></td>
    <td align="left"><p>Se você não tiver um nome personalizado, não faça alterações.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</p></td>
    <td align="left"><p>Exemplo: 54321</p>
    <p>Certifique-se de que a porta especificada não está sendo usada por outro site.</p></td>
    </tr>
    </tbody>
    </table>

     

12. Na página **servidor de relatórios** , especifique o seguinte:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Item para configurar</th>
    <th align="left">Descrição e exemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome </strong> do site: especifique o nome personalizado que será usado para executar o serviço de relatório.</p></td>
    <td align="left"><p>Se você não tiver um nome personalizado, não faça alterações.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Vinculação </strong> de porta: especifique um número de porta exclusivo que será usado pelo App-V.</p></td>
    <td align="left"><p>Exemplo: 55555</p>
    <p>Certifique-se de que a porta especificada não está sendo usada por outro site.</p></td>
    </tr>
    </tbody>
    </table>

     

13. Para iniciar a instalação, clique em **instalar** na página **pronto** e, em seguida, clique em **Fechar** na página **concluída** .

14. Para verificar se a configuração foi concluída com êxito, abra um navegador da Web e digite a seguinte URL:

    **http:// &lt; Nome do computador do servidor de gerenciamento &gt; : &lt; número da porta do serviço de gerenciamento &gt; /Console.html**.

    Exemplo: **http://localhost:12345/console.html** . Se a instalação for bem-sucedida, o console de gerenciamento do App-V será exibido sem erros.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.0](deploying-app-v-50.md)

[Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[Como instalar o servidor de publicação em um computador remoto](how-to-install-the-publishing-server-on-a-remote-computer.md)

[Como implantar o servidor App-V 5.0 usando um script](how-to-deploy-the-app-v-50-server-using-a-script.md)

[Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





