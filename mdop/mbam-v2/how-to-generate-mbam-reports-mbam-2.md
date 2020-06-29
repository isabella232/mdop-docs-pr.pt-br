---
title: Como gerar relatórios do MBAM
description: Como gerar relatórios do MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799403"
---
# Como gerar relatórios do MBAM


Ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM) with the autônomo Topology, você pode gerar relatórios diferentes para monitorar o uso e a conformidade de criptografia do BitLocker. Os procedimentos neste tópico descrevem como abrir o site de administração e monitoramento e as etapas necessárias para gerar relatórios de administração e monitoramento do Microsoft BitLocker em conformidade com a empresa, computadores individuais e atividades de recuperação de chave. Para obter informações detalhadas sobre como entender os relatórios do MBAM, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).

**Observação**  Para executar os relatórios, você deve ser membro da função de **usuários de relatório** nos computadores em que os recursos de servidor de administração e monitoramento, o banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estão instalados.

 

**Para abrir o site de administração e monitoramento**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento. A URL padrão para o site de administração e monitoramento é *http:// &lt; ComputerName &gt; *.

    **Observação**  Se o site de administração e monitoramento tiver sido instalado em uma porta diferente da 80, você precisará especificar a porta na URL (por exemplo, *http:// &lt; ComputerName &gt; : &lt; Port &gt; *. Se você tiver especificado um nome de host para o site de administração e monitoramento durante a instalação, a URL será *http:// &lt; hostname &gt; *.

     

2.  No painel esquerdo, clique em **relatórios** e selecione o relatório que você deseja executar a partir da barra de menus superior.

    Os dados do cliente MBAM históricos são mantidos no banco de dados de conformidade para referência histórica, caso um computador seja perdido ou roubado. Ao executar relatórios corporativos, recomendamos que você use as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.

    **Observação**  Se o SSRS não tiver sido configurado para usar o Secure Socket Layer, a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM. Se, em seguida, você acessar o portal de suporte técnico e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido". Para mostrar o relatório, clique em **mostrar todo o conteúdo**.

     

**Para gerar um relatório de conformidade empresarial**

1.  No site Administração e monitoramento, selecione o nó **relatórios** no painel de navegação à esquerda, selecione **relatório de conformidade empresarial**e selecione os filtros que você deseja usar. Os filtros disponíveis para o relatório de conformidade empresarial são os seguintes:

    -   **Status de conformidade**. Use esse filtro para especificar os tipos de status de conformidade (por exemplo, em conformidade ou não conforme) do relatório.

    -   **Estado do erro**. Use esse filtro para especificar os tipos de estado de erro (por exemplo, nenhum erro ou erro) do relatório.

2.  Clique em **Exibir relatório** para exibir o relatório selecionado.

    Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.

    **Observação**  O relatório de conformidade empresarial é gerado por um trabalho do SQL que é executado a cada seis horas. Portanto, na primeira vez que você exibir o relatório, você pode descobrir que alguns dados estão ausentes. Você pode gerar dados de relatório atualizados manualmente usando o SQL Management Studio. Na janela **Gerenciador de objetos** , expanda **agente do SQL Server**, expanda **trabalhos**, clique com o botão direito do mouse no trabalho **CreateCache** e selecione **Iniciar trabalho na etapa..** ..

     

3.  Selecione um nome de computador para exibir informações sobre o computador no relatório de conformidade do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

**Para gerar o relatório de conformidade do computador**

1.  No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione o **relatório de conformidade do computador**. Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.

2.  Clique em **Exibir relatório** para ver o relatório do computador.

    Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.

3.  Selecione um nome de computador para exibir mais informações sobre o computador no relatório de conformidade do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

    **Observação**  Um computador cliente MBAM é considerado compatível se o computador atender aos requisitos das configurações da política do MBAM.

     

**Para gerar o relatório de auditoria de chave de recuperação**

1.  No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e, em seguida, selecione o **relatório de auditoria de recuperação**. Selecione os filtros para o relatório de auditoria de chave de recuperação. Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:

    -   **Solicitante**. Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante. O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário.

    -   **Solicitante**. Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante. O solicitante é a pessoa que chamou o suporte técnico para obter uma chave de recuperação.

    -   **Resultado da solicitação**. Esse filtro permite que os usuários especifiquem os tipos de resultados de solicitação (por exemplo, sucesso ou falha) em que desejam basear o relatório. Por exemplo, os usuários podem querer ver as tentativas de acesso à chave que falharam.

    -   **Tipo de chave**. Esse filtro permite que os usuários especifiquem o tipo de chave (por exemplo: senha da chave de recuperação ou hash de senha do TPM) em que desejam basear o relatório.

    -   **Data de início**. Esse filtro é usado para definir a parte de data de início do intervalo de datas que o usuário quer relatar.

    -   **Data de término**. Esse filtro é usado para definir a parte de data de término do intervalo de datas que os usuários desejam relatar.

2.  Clique em **Exibir relatório** para exibir o relatório.

    Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.

## Tópicos relacionados


[Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





