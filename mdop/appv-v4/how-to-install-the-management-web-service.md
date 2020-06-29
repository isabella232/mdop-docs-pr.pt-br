---
title: Como instalar o Management Web Service
description: Como instalar o Management Web Service
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797093"
---
# Como instalar o Management Web Service


Use o procedimento a seguir para instalar o serviço Web de gerenciamento do Application Virtualization em um computador de destino na rede, com uma conta de logon com privilégios administrativos locais. Embora não seja necessário, recomendamos que você instale esse componente em seu servidor Web.

**Para instalar o serviço Web de gerenciamento**

1.  Verifique se nenhuma versão anterior do serviço Web do Application Virtualization está instalada em seu computador de destino.

2.  Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.

3.  Depois que o assistente de instalação abrir, na página de **boas-vindas** , clique em **Avançar**.

4.  Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.

5.  Na página **informações de registro** , especifique o **nome de usuário** e as informações da organização e clique em **Avançar**.

6.  Na página **tipo de instalação** , clique em **personalizado**e, em seguida, clique em **Avançar**.

    **Observação**  Se esse não for o primeiro componente que você instalou neste computador, a página **manutenção do programa** será exibida. Na página **manutenção do programa** , clique em **Modificar**.

     

7.  Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **serviço de gerenciamento do App Virt**, e clique em **Avançar**.

    **Observação**  Se um componente já estiver instalado no computador, desmarcá-lo na página de **instalação personalizada** , ele será desinstalado automaticamente.

     

8.  Na página **servidor de banco de dados** , clique em **conectar a um banco de dados disponível**e, em seguida, clique em **Avançar**.

    **Observação**  Em um ambiente de produção, a Microsoft pressupõe que você se conectará a um banco de dados existente. Se você quiser instalar um banco de dados, consulte [como instalar um banco de dados](how-to-install-a-database.md). Após instalar o banco de dados, continue com a etapa 13.

     

9.  Na página **tipo de servidor de banco de dados** , selecione um tipo de banco de dados na lista e clique em **Avançar**.

10. Na página **local do servidor de banco de dados** , selecione um servidor de banco de dados na lista de servidores disponíveis ou adicione um servidor marcando a caixa de seleção **usar o seguinte nome de host** e inserindo informações nas caixas nome do **servidor** e **número da porta** e, em seguida, clique em **Avançar**.

11. Na página **Selecionar Banco de dados** , selecione o banco de dados desejado e clique em **Avançar**.

12. Na página **configuração do usuário do banco** de dados, insira as credenciais que o serviço Web de gerenciamento usará para acessar o repositório de dados e clique em **Avançar**.

13. Na página **pronto para modificar o programa** , clique em **instalar**.

    **Observação**  Se este for o primeiro componente que você instalar, a página **pronto para instalar o programa** será exibida. Na página, clique em **instalar**.

     

14. Na página **Assistente de instalação concluído** , clique em **concluir**.

## Tópicos relacionados


[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

 

 





