---
title: Gerando relatórios autônomos do MBAM 2.5
description: Gerando relatórios autônomos do MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799209"
---
# Gerando relatórios autônomos do MBAM 2.5


Ao configurar o Microsoft BitLocker Administration and Monitoring (MBAM) with the autônomo Topology, você pode gerar relatórios para monitorar o uso e a conformidade de criptografia de unidade de disco BitLocker. Este tópico contém os seguintes procedimentos:

-   [Para abrir o site de administração e monitoramento](#bkmk-openadmin)

-   [Para gerar um relatório de conformidade empresarial](#bkmk-enterprise)

-   [Para gerar um relatório de conformidade do computador](#bkmk-computercomp)

-   [Para gerar um relatório de auditoria de chave de recuperação](#bkmk-recoverykey)

Para obter descrições dos relatórios autônomos, consulte [compreendendo os relatórios](understanding-mbam-25-stand-alone-reports.md)autônomos do MBAM 2,5.

**Observação**  Para executar os relatórios, você deve ser membro do grupo **usuários de relatório do MBAM** , que você pode configurar nos serviços de domínio Active Directory. Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

 

<a href="" id="bkmk-openadmin"></a>**Para abrir o site de administração e monitoramento**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento. A URL padrão para o site de administração e monitoramento é:

    *http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; porta &gt; /helpdesk*

2.  No painel esquerdo, clique em **relatórios**. Na barra de menus superior, selecione o relatório que você deseja executar.

    Os dados do cliente MBAM são mantidos no banco de dados de conformidade e auditoria para referência histórica, caso um computador seja perdido ou roubado. Ao executar relatórios corporativos, recomendamos que você use as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.

    Depois de gerar um relatório, você pode salvar os resultados em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.

    **Observação**  Configure o SQL Server Reporting Services (SSRS) para usar SSL (Secure Sockets Layer) antes de configurar o site de administração e monitoramento. Se, por algum motivo, o SSRS não estiver configurado para usar SSL, a URL dos relatórios será definida como HTTP em vez de HTTPS quando você configurar o site de administração e monitoramento. Se, em seguida, você acessar o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido". Para mostrar o relatório, clique em **mostrar todo o conteúdo**.

     

<a href="" id="bkmk-enterprise"></a>**Para gerar um relatório de conformidade empresarial**

1.  No site Administração e monitoramento, selecione o nó **relatórios** no painel de navegação à esquerda, selecione **relatório de conformidade empresarial**e selecione os filtros que você deseja usar. Os filtros disponíveis para o relatório de conformidade empresarial são:

    -   **Status de conformidade**. Use esse filtro para especificar os tipos de status de conformidade do relatório (por exemplo, compatível ou não conforme).

    -   **Estado do erro**. Use esse filtro para especificar os tipos de estado de erro do relatório (por exemplo, nenhum erro ou erro).

2.  Clique em **Exibir relatório** para exibir o relatório selecionado.

3.  Selecione um nome de computador para exibir informações sobre o computador no relatório de conformidade do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

<a href="" id="bkmk-computercomp"></a>**Para gerar um relatório de conformidade do computador**

1.  No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione **relatório de conformidade do computador**. Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.

2.  Clique em **Exibir relatório** para ver o relatório de conformidade do computador.

3.  Selecione um nome de computador para exibir mais informações sobre o computador no relatório de conformidade do computador.

4.  Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.

    **Observação**  Um computador cliente MBAM é considerado compatível se o computador corresponder ou exceder os requisitos das configurações da política de grupo do MBAM.

<a href="" id="bkmk-recoverykey"></a>**Para gerar um relatório de auditoria de chave de recuperação**

1.  No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione **relatório de auditoria de recuperação**. Selecione os filtros para o relatório de auditoria de chave de recuperação. Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:

    -   **Usuário da assistência técnica**. Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante. O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário final.

    -   **Usuário final**. Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante. O solicitante é o usuário final que chamou o suporte técnico para obter uma chave de recuperação.

    -   **Resultado da solicitação**. Esse filtro permite que os usuários especifiquem os tipos de resultados de solicitação (por exemplo, sucesso ou falha) em que desejam basear o relatório. Por exemplo, os usuários podem querer ver as tentativas de acesso à chave que falharam.

    -   **Tipo de chave**. Esse filtro permite que os usuários especifiquem o tipo de chave (por exemplo, a senha da chave de recuperação ou o hash de senha do TPM) em que desejam basear o relatório.

    -   **Data de início**. Esse filtro é usado para definir a parte de data de início do intervalo de datas que o usuário quer relatar.

    -   **Data de término**. Esse filtro é usado para definir a parte de data de término do intervalo de datas que os usuários desejam relatar.

2.  Clique em **Exibir relatório** para exibir o relatório.



## Tópicos relacionados


[Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Noções básicas sobre relatórios autônomos do MBAM 2.5](understanding-mbam-25-stand-alone-reports.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





