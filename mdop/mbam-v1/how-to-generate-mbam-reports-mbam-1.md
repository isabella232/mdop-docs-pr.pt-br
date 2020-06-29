---
title: Como gerar relatórios do MBAM
description: Como gerar relatórios do MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799490"
---
# Como gerar relatórios do MBAM


O monitoramento e a administração do Microsoft BitLocker (MBAM) geram vários relatórios para monitorar o uso e a conformidade de criptografia do BitLocker. Este tópico descreve como abrir o site de administração do MBAM e como gerar relatórios do MBAM sobre conformidade empresarial, computadores individuais, compatibilidade de hardware e atividade de recuperação de chave. Para obter mais informações sobre os relatórios do MBAM, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-1.md).

**Observação**  Para executar os relatórios, você deve ser membro da função de **usuários de relatório** nos computadores em que você instalou os recursos de servidor de administração e monitoramento, banco de dados de auditoria e conformidade e relatórios de conformidade e auditoria.

 

**Para abrir o site de administração do MBAM**

1.  Abra um navegador da Web e navegue até o site do MBAM. A URL padrão do site é *http:// &lt; NomeDoComputador &gt; * do servidor de administração e monitoramento do Microsoft BitLocker.

    **Observação**  Se o site do MBAMadministration foi instalado em uma porta que não seja a porta 80, você deve especificar o número da porta na URL. Por exemplo, *http:// &lt; NomeDoComputador &gt; : &lt; Port &gt; *. Se você especificou um nome de host para o site do MBAMadministration durante a instalação, a URL seria *http:// &lt; hostname &gt; *.

     

2.  No painel de navegação, clique em **relatórios**. No painel principal, clique na guia do tipo de relatório: **relatório de conformidade empresarial**, **relatório de conformidade do computador**, relatório de auditoria de **hardware**ou relatório de **auditoria de recuperação**.

    **Observação**  Os dados do cliente MBAM históricos são mantidos no banco de dados de conformidade. Esses dados retidos podem ser necessários caso um computador seja perdido ou roubado. Ao executar relatórios corporativos, você deve usar as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.

     

**Para gerar um relatório de conformidade empresarial**

1.  No site do MBAMadministration, clique em **relatórios** no painel de navegação e, em seguida, clique na guia **relatório de conformidade empresarial** e selecione os filtros apropriados para o seu relatório. Para o relatório de conformidade empresarial, você pode definir os filtros a seguir.

    -   **Status de conformidade**. Use esse filtro para especificar os tipos de status de conformidade (por exemplo, compatíveis ou não conformes) a serem incluídos no relatório.

    -   **Estado do erro**. Use esse filtro para especificar os tipos de estado de erro, como nenhum erro ou erro, a ser incluído no relatório.

2.  Clique em **Exibir relatório** para exibir o relatório especificado.

    Os resultados do relatório podem ser salvos em qualquer um dos vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.

    **Observação**  O relatório de conformidade empresarial é gerado por um trabalho do SQL que é executado a cada seis horas. Portanto, na primeira vez que você tentar exibir o relatório, verá que alguns dados estão ausentes.

     

3.  Para exibir informações sobre um computador no relatório de conformidade do computador, selecione o nome do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

**Para gerar o relatório de conformidade do computador**

1.  No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e selecione o **relatório de conformidade do computador**. Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.

2.  Clique em **Exibir relatório** para ver o relatório do computador.

    Os resultados podem ser salvos em qualquer um dos vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.

3.  Para exibir mais informações sobre um computador no relatório de conformidade do computador, selecione o nome do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

    **Observação**  Um computador cliente MBAM é considerado compatível se o computador atender aos requisitos das configurações da política do MBAM ou se o modelo de hardware do computador estiver definido como incompatível. Portanto, quando você estiver exibindo informações detalhadas sobre os volumes de disco associados ao computador, os computadores isentos da criptografia do BitLocker devido à compatibilidade de hardware poderão ser exibidos como compatíveis, mesmo que o status da criptografia do volume da unidade seja exibido como não compatível.

     

**Para gerar o relatório de auditoria de compatibilidade de hardware**

1.  No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e selecione o **relatório de auditoria de hardware**. Selecione os filtros apropriados para o seu relatório de auditoria de hardware. O relatório de auditoria de hardware oferece os seguintes filtros disponíveis:

    -   **Usuário (Domain\\User)**. Especifica o nome do usuário que fez uma alteração.

    -   **Tipo de alteração**. Especifica o tipo de alterações que você está procurando.

    -   **Data de início**. Especifica a parte de data de início do intervalo de datas que você deseja relatar.

    -   **Data de término**. Especifica a parte de data de término do intervalo de datas que você deseja relatar.

2.  Clique em **Exibir relatório** para exibir o relatório.

    Os resultados podem ser salvos em vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.

**Para gerar o relatório de auditoria de chave de recuperação**

1.  No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e, em seguida, selecione o **relatório de auditoria de recuperação**. Selecione os filtros para o relatório de auditoria de chave de recuperação. Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:

    -   **Solicitante**. Especifica o nome de usuário do solicitante. O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário.

    -   **Solicitante**. Especifica o nome de usuário do solicitante. O solicitante é a pessoa que chamou o suporte técnico para obter uma chave de recuperação.

    -   **Resultado da solicitação** Especifica os tipos de resultado de solicitação, como: sucesso ou falha. Por exemplo, você pode querer ver as tentativas de acesso à chave que falharam.

    -   **Tipo de chave**. Especifica o tipo de chave, como: senha da chave de recuperação ou hash de senha do TPM.

    -   **Data de início**. Especifica a parte de data de início do intervalo de datas.

    -   **Data de término**. Especifica a parte de data de término do intervalo de datas.

2.  Clique em **Exibir relatório** para exibir o relatório.

    Os resultados podem ser salvos em vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.

## Tópicos relacionados


[Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





