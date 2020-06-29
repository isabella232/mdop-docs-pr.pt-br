---
title: Como instalar o Application Virtualization Management Server
description: Como instalar o Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797110"
---
# Como instalar o Application Virtualization Management Server


O servidor de gerenciamento do Application Virtualization publica seus aplicativos para os clientes. Em um ambiente de carga balanceada, que é típico de implantações grandes, todos os servidores em um grupo de servidores devem transmitir os mesmos aplicativos. Se os servidores de gerenciamento do Application Virtualization forem publicar diferentes aplicativos, atribua-os a grupos de servidores diferentes. Nesse caso, você também pode precisar aumentar a capacidade de um grupo de servidores.

Se você designou um computador de destino na rede, com uma conta de logon com privilégios de administrador local, você pode usar o procedimento a seguir para instalar o servidor de gerenciamento do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.

**Observação**  
O assistente de instalação pode criar um registro de grupo do servidor, se ele não existir, bem como um registro das associações do servidor de gerenciamento do Application Virtualization nesse grupo.



Depois de concluir o processo de instalação, reinicialize o servidor.

**Para instalar um servidor de gerenciamento do Application Virtualization**

1.  Verifique e, se necessário, desinstale as versões anteriores do servidor de gerenciamento do Application Virtualization instalada no computador de destino.

2.  Para abrir o assistente de **instalação do Microsoft Application Virtualization Management Server** , navegue até o local do programa do sistema de virtualização de aplicativos **setup.exe** na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo **Setup.exe** .

3.  Na página de **boas-vindas** , clique em **Avançar**.

4.  Na página **contrato de licença** , leia o contrato de licença e, para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**. Clique em **Avançar**.

5.  Na página **informações de registro** , você deve inserir o nome de usuário e a **organização**. Clique em **Avançar**.

6.  Na página **tipo de instalação** , selecione **personalizado**. Clique em **Avançar**. Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **servidor do Application Virtualization**, e clique em **Avançar**.

    **Tenha**  
    Se um componente já estiver instalado no computador, quando você desmarcar-o na janela de **instalação personalizada** , o componente será desinstalado automaticamente.



7.  Na página **banco de dados de configuração** , selecione um servidor de banco de dados na lista de servidores disponíveis ou adicione um servidor selecionando **usar o nome de host a seguir** e especificando o **nome do servidor** e os dados do **número da porta** . Clique em **Avançar**.

    **Observação**  
    O servidor de gerenciamento do Application Virtualization não dá suporte a SQL que diferencia maiúsculas de minúsculas.



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. Na página **modo de segurança de conexão** , selecione o certificado desejado na lista suspensa. Clique em **Avançar**.

   **Observação**  
   A configuração do **modo de conexão segura** exige que o servidor tenha um certificado do servidor provisionado para ele de uma infraestrutura de chave pública. Se um certificado do servidor não estiver instalado no servidor, essa opção não estará disponível e não poderá ser selecionada. Você deve conceder acesso de leitura à conta de serviço de rede para o certificado que está sendo usado.



9. Na página **configuração de porta TCP** , para usar a porta padrão (554), selecione **usar porta padrão (554)**. Para especificar uma porta personalizada, selecione **usar porta personalizada** e especifique o número da porta que será usado. Clique em **Avançar**.

   **Observação**  
   Ao instalar o servidor em um ambiente não seguro, você pode usar a porta padrão (554) ou pode definir uma porta personalizada.



10. Na página **grupo de administradores** , especifique o nome do grupo de segurança autorizado para gerenciar esse servidor no **nome do grupo**. Clique em **Avançar**. Confirme o grupo especificado e clique em **Avançar**.

11. Na página **grupo do provedor padrão** , especifique o nome do grupo do provedor padrão e clique em **Avançar**.

12. Na página **caminho do conteúdo** , especifique o local no computador de destino em que os arquivos SFT serão salvos e clique em **Avançar**.

   **Observação**  
   Se a porta HTTP ou RTSP do servidor de gerenciamento já estiver alocada, você será solicitado a escolher uma nova porta. Selecione a porta desejada e, em seguida, clique em **Avançar**.



13. Na página **pronto para instalar o programa** , para instalar o servidor de gerenciamento do Application Virtualization, clique em **instalar**.

   **Observação**  
   Se o erro 25120 for exibido quando você tentar concluir esta etapa, será necessário habilitar os **scripts e ferramentas de gerenciamento**do IIS. Para habilitar esse recurso do Windows, abra o painel de controle **programas e recursos** , selecione **Ativar ou desativar recursos do Windows**e navegue até **serviços de informações da Internet.**

   Em **ferramentas de gerenciamento da Web**, habilite **scripts e ferramentas de gerenciamento do IIS**.



14. Na tela **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.

   **Importante**  
   A instalação pode demorar alguns minutos para ser concluída. Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando que a instalação foi bem-sucedida.

   Não é necessário reinicializar o computador quando solicitado. No entanto, para otimizar o desempenho do sistema, é recomendável reinicializar.



## Tópicos relacionados


[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)









