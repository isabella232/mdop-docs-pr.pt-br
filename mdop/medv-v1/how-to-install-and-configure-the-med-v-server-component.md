---
title: Como instalar e configurar o componente de servidor do MED-V
description: Como instalar e configurar o componente de servidor do MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799980"
---
# Como instalar e configurar o componente de servidor do MED-V


Esta seção explica como [instalar](#bkmk-howtoinstallthemedvserver) e [Configurar](#bkmk-howtoconfigurethemedvserver) o servidor MED-V.

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>Como instalar o servidor MED-V


**Para instalar o servidor MED-V**

1.  Instale o pacote MED-V Server. msi.

    O pacote MED-V Server. msi é chamado *MED-V\_Server\_x.msi*, em que x é o número da versão.

    Por exemplo, *MED-V\_Server\_1.0.65.msi*.

2.  Quando a tela de **boas-vindas do Assistente InstallShield** for exibida, clique em **Avançar**.

3.  Na tela **contrato de licença** , leia o contrato de licença, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.

    A tela de **pasta de destino** será exibida, com a pasta de instalação padrão exibida.

    A pasta de instalação padrão é *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.

    -   Para alterar a pasta em que o MED-V deve ser instalado, clique em **alterar** e navegue até uma pasta existente.

4.  Clique em **Avançar**.

5.  Na tela **pronto para instalar o programa** , clique em **instalar**.

    A instalação do servidor MED-V é iniciada. Isso pode levar alguns minutos, e a tela pode não exibir texto. Durante a instalação, várias telas de progresso são exibidas. Se aparecer uma mensagem, siga as instruções fornecidas.

6.  Quando a tela **Assistente InstallShield concluído** for exibida, clique em **concluir** para concluir o assistente.

**Observação**  
Se você estiver instalando o servidor MED-V pela área de trabalho remota da Microsoft, use a seguinte sintaxe: **mstsc/administrador**. Certifique-se de que sua sessão RDP seja direcionada ao console.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>Como configurar o servidor MED-V


As seguintes configurações do servidor podem ser configuradas:

-   [Connections](#bkmk-configuringconnections)

-   [Images](#bkmk-configuringimages)

-   [Permissões](#bkmk-configuringpermissions)

-   [Relatórios](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>Configurar conexões

**Para configurar conexões**

1.  No menu Iniciar do Windows, selecione **todos os programas &gt; med-v &gt; med-v Server Configuration Manager**.

    **Observação**  
    Observação: se você tiver marcado a caixa de seleção **iniciar o Gerenciador de configuração do MED-v Server** durante a instalação do servidor, o Gerenciador de configuração do MED-v Server será iniciado automaticamente após a conclusão da instalação do servidor.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. Na guia **conexões** , defina as seguintes configurações de conexões de cliente:

   -   **Habilitar conexões não criptografadas (http), usando a porta**— Marque esta caixa de seleção para habilitar conexões não criptografadas usando uma porta especificada. Na caixa porta, insira a porta do servidor na qual aceitar conexões não criptografadas (http).

   -   **Habilitar conexões criptografadas (https), usando porta**— Marque esta caixa de seleção para habilitar conexões criptografadas usando uma porta especificada. Na caixa porta, insira a porta do servidor na qual aceitar conexões criptografadas (https).

       HTTPS é uma configuração opcional que pode ser definida para garantir transações seguras entre o servidor MED-V e os clientes do MED-V. Para configurar o HTTPS, você deve executar os seguintes procedimentos:

       -   Configurar um certificado no servidor.

       -   Associe o certificado do servidor à porta especificada usando Netsh. Para obter informações, consulte os seguintes artigos:

           -   [Comandos netsh para HTTP (Hypertext Transfer Protocol)](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [Como: configurar uma porta com um certificado SSL](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [Como: configurar uma porta com um certificado SSL](https://msdn.microsoft.com/library/ms733791.aspx)

3. Clique em **OK**.

### <a href="" id="bkmk-configuringimages"></a>Configurando imagens

**Para configurar imagens**

1.  Clique na guia **imagens** .

2.  Defina as seguintes configurações de gerenciamento de imagens:

    -   **Diretório VMs**— diretório da máquina virtual (o diretório onde as imagens estão armazenadas). Este campo contém um caminho UNC para o diretório de imagens no servidor de distribuição de imagens que deve ser acessado do servidor MED-V.

    -   **URL de VMs**— o local do servidor onde as imagens estão armazenadas.

3.  Clique em **OK**.

### <a href="" id="bkmk-configuringpermissions"></a>Configurando permissões

**Para configurar permissões**

1.  Clique na guia **permissões** .

2.  Uma lista de todos os usuários que podem fazer logon é fornecida. Para aplicar as permissões de leitura e gravação a um usuário, marque a caixa de seleção ao lado do usuário. Para aplicar permissões somente leitura a um usuário, desmarque a caixa de seleção.

3.  Para adicionar usuários ou grupos de domínio, clique em **Adicionar**.

    A caixa de diálogo **Inserir nomes de usuário ou grupo** é exibida.

    1.  Selecione usuários ou grupos do domínio seguindo um destes procedimentos:

        -   No campo **Inserir nomes de usuário ou grupo** , digite um usuário ou grupo que exista no domínio ou exista como um usuário ou grupo local no computador. Em seguida, clique em **verificar nomes** para resolvê-lo para o nome completo existente.

        -   Clique em **Localizar** para abrir a caixa de diálogo **Selecionar usuários ou grupos** padrão. Em seguida, selecione usuários ou grupos do domínio.

    2.  Clique em **OK**.

4.  Para remover usuários ou grupos de domínio, selecione um usuário ou grupo e clique em **remover**.

5.  Clique em **OK**.

### <a href="" id="bkmk-configuringreports"></a>Configurando relatórios

**Para configurar relatórios**

1.  Clique na guia **relatórios** .

2.  Para dar suporte a relatórios, selecione **habilitar relatórios**.

3.  Na caixa **cadeia de conexão** , insira uma cadeia de conexão para o banco de dados MSSQL.

    -   Quando o SQL Server estiver instalado em um servidor remoto, use a seguinte cadeia de conexão:

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **Observação**  
        Observação: para se conectar ao SQL Express, use: `Data Source=<ServerName>\sqlexpress.`



4.  Para criar o banco de dados, clique em **criar banco de dados**.

5.  Para testar a conexão, clique em **testar conexão**.

6.  Para configurar as opções de compensação do banco de dados, clique em **limpar opções**.

    A caixa de diálogo **limpar opções de banco de dados** é exibida.

    1.  Escolha uma das seguintes opções:

        -   **Limpar dados mais antigos do que**: limpar todos os dados anteriores ao número de dias especificado; na caixa número, insira um número de dias.

        -   **Limpar todos os dados do banco de**dados — limpar todos os dados existentes no banco de dados.

        -   **Remover banco de dados**— excluir o banco de dados.

    2.  Clique em **OK** para aplicar as alterações e fechar a caixa de diálogo.

7.  Clique em **OK** para salvar as alterações ou clique em **Cancelar** para fechar a caixa de diálogo sem salvar as alterações.

8.  Se solicitado, reinicie o serviço do servidor MED-V para aplicar as alterações nas configurações de rede.

## Tópicos relacionados


[Configurações com suporte](supported-configurationsmedv-orientation.md)

[Projetar a infraestrutura de servidor do MED-V](design-the-med-v-server-infrastructure.md)









