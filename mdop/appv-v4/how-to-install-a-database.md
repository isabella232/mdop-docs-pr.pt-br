---
title: Como instalar um banco de dados
description: Como instalar um banco de dados
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797113"
---
# Como instalar um banco de dados


Você pode usar o procedimento a seguir para instalar um banco de dados para a implantação baseada em servidor da virtualização de aplicativos se um banco de dados ainda não estiver disponível. Em geral, em um ambiente de produção, você se conectará a um banco de dados existente.

**Importante**  Para instalar o banco de dados, você deve usar uma conta de rede com as permissões apropriadas. Se a sua organização exigir que apenas administradores de banco de dados possam criar e conduzir atualizações de banco de dados, os scripts estarão disponíveis para permitir que essa tarefa seja realizada.

 

**Para instalar um banco de dados**

1.  Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.

2.  Na **página de boas-vindas**, clique em **Avançar**.

3.  Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.

4.  Na página **informações de registro** , especifique o **nome de usuário** e as informações da **organização** e clique em **Avançar**.

5.  Na página **tipo de instalação** , selecione **personalizado** e clique em **Avançar**.

6.  Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **servidor do Application Virtualization**, e clique em **Avançar**.

    **Observação**  Se um componente já estiver instalado no computador, desmarque-o na tela de **instalação personalizada** , ele será desinstalado automaticamente.

     

7.  Na página **servidor de banco de dados** , digite as senhas, atribua um caminho de instalação, salve as informações e clique em **Avançar**.

8.  Selecione um nome para o banco de dados e clique em **Avançar**.

    **Observação**  Se o erro 25109 for exibido quando você tentar concluir esta etapa, você terá configurado incorretamente as permissões necessárias para instalar o banco de dados. Para obter detalhes sobre como configurar as permissões SQL necessárias, consulte <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  Na tela **servidor de diretório** , insira um nome de domínio e credenciais que os servidores de virtualização de aplicativos e o serviço Web de gerenciamento usarão para acessar seu controlador de domínio, salvar essas informações e, em seguida, clique em **Avançar**.

    **Observação**  A instalação usará como padrão o domínio do computador atual.

     

10. Na página **grupo de administradores** , digite o nome de um grupo que terá privilégios de administrador, salve essas informações e clique em **Avançar**.

    **Observação**  Você também pode inserir os primeiros caracteres do nome de um grupo que terão privilégios de administração, clicar em **Avançar**e, na tela **selecionar grupo administrador** , selecione o grupo na lista resultante. Em seguida, salve essas informações e clique em **Avançar**.

     

11. Na página **grupo de provedores padrão** , insira o nome completo de um grupo que controlará o acesso aos aplicativos, salve essas informações e clique em **Avançar**.

    **Observação**  Você também pode inserir os primeiros caracteres do nome de um grupo que controlará o acesso aos aplicativos, clique em **Avançar**e, na tela **selecionar grupo de provedor padrão** , selecione o grupo na lista. Em seguida, salve essas informações e clique em **Avançar**.

     

12. Na página **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.

    **Importante**  A instalação pode demorar alguns minutos para ser concluída. Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando se a instalação foi bem-sucedida.

     

## Tópicos relacionados


[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

 

 





