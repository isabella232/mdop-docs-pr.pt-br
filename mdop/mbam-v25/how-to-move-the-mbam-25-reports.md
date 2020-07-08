---
title: Como mover os relatórios do MBAM 2.5
description: Como mover os relatórios do MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795988"
---
# Como mover os relatórios do MBAM 2.5


Use estes procedimentos para mover o recurso relatórios de um computador para outro, ou seja, para mover o recurso relatórios do servidor a para o servidor B.

As etapas de alto nível para mover o recurso relatórios são:

1.  Interrompa todas as instâncias do site de administração e monitoramento do MBAM.

2.  Instale o software de servidor MBAM 2,5 no servidor B e configure o recurso relatórios no servidor B.

3.  Atualize os dados de conexão dos relatórios nos servidores de administração e monitoramento do MBAM.

4.  Retome a instância do site de administração e monitoramento do MBAM.

**Observação**  Para executar os scripts de exemplo do Windows PowerShell neste tópico, você deve atualizar a política de execução do Windows PowerShell para permitir que os scripts sejam executados. Consulte [executando scripts do Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obter instruções.

 

**Parar o site de administração e monitoramento do MBAM**

-   No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.

    Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B**

1.  Instale o software MBAM Server no servidor B. Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso **relatórios** .

    Você também pode usar o cmdlet **Enable-MbamReport** do Windows PowerShell para configurar os relatórios.

    Para obter instruções sobre como configurar os relatórios, consulte [como configurar os relatórios do MBAM 2,5](how-to-configure-the-mbam-25-reports.md).

**Atualizar os dados de conexão dos relatórios no servidor de administração e monitoramento**

1.  No servidor que está executando o recurso relatórios, use o console do Gerenciador dos serviços de informações da Internet (IIS) para atualizar a URL dos relatórios.

2.  Expanda **Administração e monitoramento do Microsoft BitLocker**e selecione o nó da **assistência técnica** .

3.  Na seção **Gerenciamento** do modo de **exibição recursos**, selecione **Editor de configuração**.

4.  No campo **seção** , selecione **appSettings**.

5.  Selecione a linha de **coleção** e, em seguida, clique no botão "reticências" **(...)** na extremidade direita do painel para abrir o **Editor de coleção**.

6.  No **Editor de coleção**, selecione a linha que contém **Microsoft. MBAM. Reports. URL**e atualize o valor de **Microsoft. MBAM. Reports. URL** para refletir o nome do servidor para o servidor B.

    Se você configurou anteriormente o recurso relatórios em uma instância nomeada do SQL Server Reporting Services, adicione ou atualize o nome da instância para a URL, por exemplo:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando no servidor de administração e monitoramento semelhante ao exemplo de código a seguir.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    Usando as descrições na tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parâmetro</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>Nome do servidor para o qual os relatórios foram movidos.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Nome da instância do SQL Server Reporting Services para a qual os relatórios foram movidos.</p></td>
    </tr>
    </tbody>
    </table>

     

**Retomar a instância do site de administração e monitoramento**

1.  No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.

2.  Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Observação**  Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.

     



## Tópicos relacionados


[Como configurar os relatórios do MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Movendo os recursos do MBAM 2.5 para outro servidor](moving-mbam-25-features-to-another-server.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





