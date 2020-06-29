---
title: Atualizando de versões anteriores do MBAM
description: Atualizando de versões anteriores do MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799346"
---
# Atualizando de versões anteriores do MBAM


Você pode atualizar a administração e o monitoramento do Microsoft BitLocker (MBAM) para o MBAM 2.0, com a topologia autônoma ou a topologia do Configuration Manager, fazendo o seguinte:

-   **Substituição manual** in-loco do servidor – para atualizar o servidor do MBAM, desinstale manualmente o MBAM usando o instalador ou o painel de controle e instale a infraestrutura do MBAM 2.0. Não é necessário remover os bancos de dados. Desinstalar o servidor MBAM 1,0 deixa os bancos de dados do MBAM intactos. Se você especificar os mesmos bancos de dados que o MBAM 1,0 estava usando, a instalação do MBAM 2.0 mantém dados do MBAM 1,0 nos bancos de dados e converte os bancos de dados para trabalhar com MBAM 2.0.

-   **Atualização do cliente distribuído** -se você estiver usando a topologia MBAM autônoma, poderá atualizar os clientes do MBAM gradualmente após a instalação da infraestrutura de servidor do MBAM 2,0. O servidor MBAM 2,0 detecta a versão do cliente existente e executa as etapas necessárias para atualizar para o cliente 2,0.

    Depois de atualizar a infraestrutura de servidor do MBAM 2,0, os clientes do MBAM 1,0 continuam a se comunicar com o servidor do MBAM 2,0 com êxito, dados de recuperação posteriores, mas a conformidade será baseada nas políticas do MBAM 1,0. Você deve atualizar os clientes para o MBAM 2,0 para que os computadores cliente relatem precisamente a conformidade com as políticas do MBAM 2,0. Você pode atualizar os clientes para o cliente do MBAM 2,0 sem desinstalar o cliente anterior e o cliente começará a aplicar e relatar as políticas do MBAM 2,0.

    Se estiver usando o MBAM com o Configuration Manager, você deve atualizar os clientes do MBAM 1,0 para MBAM 2,0.

## Atualizando o MBAM a partir de uma arquitetura de dois servidores


Use as instruções a seguir para atualizar de uma versão anterior do MBAM quando você estiver usando uma arquitetura de dois servidores, onde um servidor está hospedando os componentes do Microsoft SQL Server, e o outro servidor está hospedando os sites e serviços.

**Para atualizar o MBAM a partir de uma arquitetura de dois servidores**

1.  No servidor com os recursos do SQL Server, no painel de controle, selecione **programas e recursos**e, em seguida, desinstalar **o Microsoft BitLocker Administration and Monitoring**. O banco de dados de recuperação e a conformidade e o banco de dados de auditoria permanecem inalterados.

2.  Execute **MBAMSetup.exe** para a versão MBAM 2,0, selecione opcionalmente o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , **Selecione a topologia autônoma ou** de **integração do System Center Configuration Manager** e clique em **Avançar**.

5.  Na página **selecionar recursos para instalar** , desmarque os recursos **servidor de autoatendimento** e **Administração e monitoramento e** clique em **Avançar**.

6.  Aguarde até que as verificações de pré-requisitos sejam concluídas e clique em **Avançar**. Se um pré-requisito ausente for detectado, resolva os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.

7.  Na página **fornecer conta usada para acessar a página bancos de dados do MBAM** , forneça o nome do computador para o servidor que hospedará os sites e serviços e clique em **Avançar**.

8.  Na página **Configurar o banco** de dados de recuperação, especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação. Você também deve especificar onde os arquivos do banco de dados e as informações do log serão localizados.

9.  Clique em **Avançar** para continuar.

10. Na página **Configurar o banco de dados de conformidade e auditoria** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade.

11. Clique em **Avançar** para continuar.

12. Na página **Configurar a conformidade e os relatórios de auditoria** , especifique a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados e forneça uma conta de usuário e uma senha de domínio para acessar o banco de dados de conformidade e auditoria. Configure a senha desta conta para nunca expirar. A conta de usuário pode acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.

13. Clique em **Avançar** para continuar.

14. Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**. Isso não ativa as atualizações automáticas no Windows. Se você anteriormente optou por usar o Microsoft Update para este produto ou outro produto, a página Microsoft Update não será exibida.

15. Na página **Resumo da instalação** , examine os recursos que serão instalados e clique em **instalar** para iniciar a instalação.

**Para desinstalar os recursos do servidor de administração e monitoramento e concluir a atualização**

1.  No computador que hospeda os recursos do servidor de administração e monitoramento, no painel de controle, selecione **programas e recursos**e, em seguida, desinstale o MBAM para remover os sites e serviços instalados anteriormente.

2.  Execute o **MBAMSetup.exe** para a versão 2,0, selecione opcionalmente o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , **Selecione a topologia autônoma ou** de **integração do System Center Configuration Manager** e clique em **Avançar**.

5.  Na página **selecionar recursos para instalar** , desmarque o banco de dados de **recuperação** e os recursos de **banco de dados de auditoria** e conformidade e relatórios de **auditoria** e, em seguida, clique em **Avançar**.

6.  Aguarde até que as verificações de pré-requisitos sejam concluídas e clique em **Avançar**. Se um pré-requisito ausente for detectado, resolva os pré-requisitos ausentes primeiro e clique em **verificar pré-requisitos novamente**.

7.  Na página **Configurar segurança de comunicação de rede** , escolha se deseja usar a criptografia SSL (Secure Socket Layer) para os sites e serviços. Se você decidir criptografar a comunicação, selecione o certificado de autoridade de certificação (CA) a ser usado para criptografia.

    **Observação**  O certificado deve ser criado antes desta etapa para permitir que você o selecione nessa página.

     

8.  Na página **Configurar o local do banco de dados de status de conformidade** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazena os dados de conformidade e auditoria. Você também deve especificar onde os arquivos do banco de dados e as informações do log serão localizados.

9.  Clique em **Avançar** para continuar.

10. Na página **Configurar o local do banco de dados de recuperação** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazena os dados de recuperação.

11. Clique em **Avançar** para continuar.

12. Na página **Configurar a conformidade e os relatórios de auditoria** , insira a URL da instância de relatório que você configurou no outro servidor. Use o botão **testar** para verificar se você pode acessar o site.

13. Clique em **Avançar** para continuar.

14. Na página **Configurar o portal de autoatendimento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do portal de autoatendimento.

    **Observação**  O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.

     

15. Na página **Configurar o servidor de administração e monitoramento** , especifique o diretório virtual desejado para o site de suporte técnico.

16. Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**. Esta etapa não ativa as atualizações automáticas no Windows. Se você anteriormente optou por usar o Microsoft Update para este produto ou outro produto, a página Microsoft Update não será exibida.

17. Na página **Resumo da instalação** , examine os recursos que serão instalados e clique em **instalar** para iniciar a instalação.

18. Para validar que a atualização foi bem-sucedida, verifique se você pode entrar em contato com cada site de outro computador do domínio.

## Atualizando o cliente MBAM em computadores de usuários finais


Para atualizar os computadores de usuários finais para o cliente do MBAM 2,0, execute **MbamClientSetup.exe** em cada computador cliente. O instalador atualiza automaticamente o cliente para o cliente do MBAM 2,0. Você pode instalar o cliente do MBAM por meio de um sistema de distribuição de software eletrônico, ferramentas como os serviços de domínio do Active Directory ou o System Center Configuration Manager.

Para validar a atualização do cliente, faça o seguinte:

1.  Aguarde até que o ciclo de relatório configurado seja concluído e, em seguida, inicie o **SQL Server Management Studio** no computador do SQL Server.

2.  No computador do SQL Server, inicie o **SQL Server Management Studio**.

3.  Verifique se a tabela **RecoveryAndHardwareCore. Machines** contém uma linha que mostra o nome do computador do usuário final.

## Tópicos relacionados


[Implantando o MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





