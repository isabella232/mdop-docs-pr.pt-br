---
title: Como instalar o Console de Gerenciamento
description: Como instalar o Console de Gerenciamento
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797098"
---
# Como instalar o Console de Gerenciamento


Você pode usar o procedimento a seguir para instalar o console de gerenciamento do Application Virtualization em um computador de destino na rede. Você deve usar uma conta de rede com privilégios de administrador no computador de destino. Você pode usar o console para configurar e gerenciar a plataforma de sistema do Application Virtualization.

Antes de concluir esse procedimento, você deve instalar o serviço Web de gerenciamento do Application Virtualization nesse ou em outro computador. O serviço Web de gerenciamento permite que você acesse o repositório de dados e o controlador de domínio. Para obter mais informações sobre como instalar o serviço Web, consulte [como instalar o serviço Web de gerenciamento](how-to-install-the-management-web-service.md).

**Para instalar o console de gerenciamento**

1.  Verifique se não há versões anteriores do console de gerenciamento instaladas no computador de destino.

2.  Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.

3.  Na **página de boas-vindas**, clique em **Avançar**.

4.  Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.

5.  Na página **informações de registro** , especifique o **nome de usuário** e as informações da **organização** e clique em **Avançar**.

6.  Na página **tipo de instalação** , clique em **personalizado** e, em seguida, clique em **Avançar**.

7.  Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto **console de gerenciamento**, e clique em **Avançar**.

    **Observação**  Se um componente já estiver instalado no computador, desmarque-o na tela instalação personalizada, ele será desinstalado automaticamente.

     

8.  Na tela **pronto para modificar o programa** , clique em **instalar**.

    **Observação**  Se este for o primeiro componente que você instalar, a página **pronto para instalar o programa** será exibida. Para iniciar a instalação, clique em **instalar**.

     

9.  Na tela **Assistente de instalação concluído** , clique em **concluir**. Clique em **OK** para reiniciar o computador e concluir a instalação.

10. No painel de controle do Windows, clique duas vezes em **Ferramentas administrativas** e, em seguida, clique em **console de gerenciamento do Application Virtualization** para exibir o console de gerenciamento.

11. Clique no ícone **conectar** ou clique com o botão direito do mouse no contêiner de **sistemas de virtualização de aplicativos** e clique em **conectar ao sistema do Application Virtualization**.

12. Na tela **conectar-se ao sistema do Application Virtualization** , digite o nome e a porta do host do computador do serviço Web de gerenciamento, altere as informações de segurança e as credenciais de logon, se necessário, e clique em **OK**.

13. Depois de se conectar ao computador do serviço Web de gerenciamento, clique em **arquivo** no menu **console** e, em seguida, clique em **sair**. Clique em **Sim** para salvar as configurações do console.

## Tópicos relacionados


[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

 

 





