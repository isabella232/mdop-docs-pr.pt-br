---
title: Como instalar o MBAM com o Configuration Manager
description: Como instalar o MBAM com o Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799610"
---
# Como instalar o MBAM com o Configuration Manager


Esta seção descreve as etapas para instalar o MBAM com o Configuration Manager usando a configuração recomendada, que é ilustrada em [introdução-usando o MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). As etapas são divididas nas seguintes tarefas:

-   Instalar e configurar o MBAM no servidor do Configuration Manager

-   Instalar os bancos de dados de recuperação e auditoria no servidor de banco de dados

-   Instalar os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento

Antes de começar a instalação, certifique-se de ter editado ou criado os arquivos MOF necessários. Para obter instruções, consulte [como criar ou editar os arquivos MOF](how-to-create-or-edit-the-mof-files.md).

**Importante**  Se você estiver usando uma instância do SQL Server Reporting Services (SSRS) não padrão, deverá iniciar a configuração do MBAM usando a seguinte linha de comando para especificar a instância do SSRS nomeado:

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**Para instalar o MBAM no servidor do Configuration Manager**

1.  No servidor do Configuration Manager, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

    **Observação**  Para obter os arquivos de log de instalação, você precisa usar o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o Configuration Manager. Os arquivos de log são criados no local que você especificar.

    Arquivos de log de instalação adicionais são criados na pasta% temp% no computador do usuário que está instalando o Configuration Manager.

     

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , selecione **integração do System Center Configuration Manager**e, em seguida, clique em **Avançar**.

5.  Na página **selecionar recursos para instalar** , selecione a **integração do System Center Configuration Manager**.

    **Observação**  Na página **verificando pré-requisitos** , clique em **Avançar** depois que o assistente de instalação verifica os pré-requisitos para a sua instalação e confirma se nenhuma delas está ausente. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente.**

     

6.  Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**. Usar o Microsoft Updates não ativa as atualizações automáticas no Windows.

7.  Clique em **Avançar** para continuar.

8.  Na página **Resumo da instalação** , examine a lista de recursos que serão instalados e clique em **instalar** para começar a instalar os recursos do MBAM. Clique em **voltar** para voltar ao assistente se precisar revisar ou alterar as configurações de instalação ou clique em **Cancelar** para sair da instalação. A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.

9.  Clique em **concluir** para sair do assistente.

**Para instalar os bancos de dados de recuperação e auditoria no servidor de banco de dados**

1.  No servidor de banco de dados, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , selecione a topologia de **integração do System Center Configuration Manager** e clique em **Avançar**.

5.  Na lista de recursos a serem instalados, selecione **banco de dados de recuperação** e **banco de dados de auditoria**e desmarque os recursos restantes.

    **Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.

     

6.  Na página **Configurar o banco de dados de recuperação** , especifique os nomes dos computadores que executarão o recurso de servidor de administração e monitoramento. Após a implantação do recurso de servidor de administração e monitoramento, ele usa sua conta de domínio para se conectar ao banco de dados.

7.  Clique em **Avançar** para continuar.

8.  Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação. Você também deve especificar o local em que o banco de dados será localizado e onde as informações do log serão localizadas.

9.  Clique em **Avançar** para continuar com o assistente de instalação de configuração do MBAM.

10. Na página **Configurar o banco de dados de auditoria** , especifique a conta de usuário que será usada para acessar o banco de dados para relatórios.

11. Especifique os nomes de computador dos computadores que executarão o servidor de administração e monitoramento e os relatórios de auditoria. Após a implantação e o monitoramento e os recursos de relatórios de auditoria serem implantados, as contas de domínio deles serão usadas para se conectar aos bancos de dados.

    **Observação**  Se você estiver instalando o banco de dados de auditoria sem o recurso relatórios de auditoria, será necessário adicionar uma exceção no computador de banco de dados de auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server. O número da porta padrão é 1433.

     

12. Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria. Você também deve especificar onde as informações do log e do banco de dados serão localizadas.

13. Clique em **instalar** para iniciar a instalação e, em seguida, clique em **concluir** para concluir a instalação.

**Para instalar os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento**

1.  No servidor de administração e monitoramento, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , selecione a topologia de **integração do System Center Configuration Manager** e clique em **Avançar**.

5.  Na lista de recursos a serem instalados, selecione **Administração e monitoramento do servidor** e do **portal de autoatendimento**e desmarque os recursos restantes.

    **Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.

     

6.  Instale o portal de autoatendimento seguindo as etapas na seção **para instalar o portal** de autoatendimento em [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

    **Observação**  Se os computadores cliente não terão acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que oferece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, conclua as etapas na seção **para configurar o portal de autoatendimento quando os usuários finais não puderem acessar a seção de rede de distribuição de conteúdo da Microsoft** [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.

     

7.  Para instalar os recursos do servidor de administração e monitoramento, siga as etapas na seção **para instalar o recurso de servidor de administração e monitoramento** em [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

8.  Clique em **concluir** para concluir a instalação.

## Tópicos relacionados


[Como validar a instalação do MBAM com o Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Como implantar o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





