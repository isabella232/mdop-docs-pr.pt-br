---
title: Planejando o uso do App-V com o Office
description: Planejando o uso do App-V com o Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796243"
---
# Planejando o uso do App-V com o Office


Use as informações a seguir para planejar como implantar o Office usando o Microsoft Application Virtualization (App-V) 5,1. Este artigo inclui:

-   [Suporte do App-V para pacotes de idiomas](#bkmk-lang-pack)

-   [Versões com suporte do Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Planejando o uso do App-V com versões coexistentes do Office](#bkmk-plan-coexisting)

-   [Como o Office se integra ao Windows ao implantar usar o App-V para implantar o Office](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>Suporte do App-V para pacotes de idiomas


Você pode usar o sequenciador do App-V 5,1 para criar pacotes de plug-in para pacotes de idiomas, pacotes de interface de idioma, revisores de ferramenta e idiomas de dica de ferramenta. Em seguida, você pode incluir os pacotes de plug-in em um grupo de conexão, juntamente com o pacote do Office 2013 que você cria usando o kit de ferramentas de implantação do Office. Os pacotes de idiomas do plug-in e os aplicativos do Office interagem perfeitamente no mesmo grupo de conexão, assim como qualquer outro pacote agrupado em um grupo de conexão.

>**Observação**  O Microsoft Visio e o Microsoft Project não oferecem suporte para o pacote de idiomas do tailandês.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Versões com suporte do Microsoft Office

Consulte as [IDs de produto do Microsoft Office que o App-V suporta](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) para uma lista de produtos do Office com suporte.
>**Note** &nbsp; Observação &nbsp; Você deve usar a ferramenta de implantação do Office para criar pacotes do App-V para aplicativos do Microsoft 365 para empresas. Não há suporte para a criação de pacotes para versões de licença de volume do Office Professional Plus ou do Office Standard. Não é possível usar o sequenciador App-V.

 

## <a href="" id="bkmk-plan-coexisting"></a>Planejando o uso do App-V com versões coexistentes do Office


Você pode instalar mais de uma versão do Microsoft Office lado a lado no mesmo computador usando a "coexistência do Microsoft Office". Você pode implementar a coexistência do Office com as combinações de todas as versões principais do Office e com métodos de instalação, conforme aplicável, usando a versão do Office com base no Windows Installer (MSi) do Office, clique para executar e App-V 5,1. No entanto, o uso de coexistência do Office não é recomendado pela Microsoft.

A prática recomendada pela Microsoft é evitar a coexistência do Office completamente para evitar problemas de compatibilidade. No entanto, ao migrar para uma versão mais recente do Office, os problemas surgem ocasionalmente que não podem ser resolvidos imediatamente, portanto, você pode implementar a coexistência temporariamente para facilitar uma migração mais recente para a versão mais recente do produto. Usar a coexistência do Office em uma base de longo prazo nunca é recomendado, e sua organização deve ter um plano para fazer toda a transição no futuro imediato.

### Antes de implementar a coexistência do Office

Antes de implementar a coexistência do Office, examine a seguinte documentação do Office. Escolha o artigo que corresponde à versão mais recente do Office para a qual você planeja implementar a coexistência.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do Office</th>
<th align="left">Link para diretrizes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Informações sobre como usar os pacotes e programas do Office 2013 (implantação do MSI) em um computador que esteja executando outra versão do Office</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Informações sobre como usar os pacotes e programas do Office 2010 em um computador que esteja executando outra versão do Office</a></p></td>
</tr>
</tbody>
</table>

 

A documentação do Office fornece diretrizes abrangentes sobre a coexistência para instalações do Windows Installer (MSi) e com Clique para executar do Office. Este tópico do App-V na coexistência suplementa a orientação do Office com informações que são mais específicas para implantações do App-V.

### Cenários de coexistência do Office com suporte

As tabelas a seguir resumem os cenários de coexistência com suporte. Elas são organizadas de acordo com a versão e o método de implantação com o qual você está começando e o método de versão e implantação para o qual você está migrando. Certifique-se de testar completamente todas as soluções de coexistência antes de implantá-las em um público de produção.

>**Observação**  A Microsoft não oferece suporte ao uso de várias versões do Office em ambientes Windows Server com o serviço de função de host da sessão da área de trabalho remota habilitado. Para executar cenários de coexistência do Office, você deve desabilitar esse serviço de função.

 

### Integrações do Windows & a coexistência do Office

Os métodos de instalação do Office para Windows Installer e com Clique para executar integram-se com determinados pontos do sistema operacional Windows subjacente. Quando você usa a coexistência, as integrações comuns do sistema operacional entre duas versões do Office podem entrar em conflito, causando problemas de compatibilidade e experiência do usuário. Com o App-V, você pode sequenciar determinadas versões do Office para excluir as integrações, portanto "isolando"-as do sistema operacional.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Modo em que o App-V pode sequenciar esta versão do Office</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Sempre não integrado. O App-V não oferece integrações de sistema operacional com uma versão virtualizada do Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Modo integrado e não integrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Sempre integrado. Não é possível desabilitar as integrações do sistema operacional do Windows.</p></td>
</tr>
</tbody>
</table>

 

A Microsoft recomenda que você implante a coexistência do Office com apenas uma instância integrada do Office. Por exemplo, se você estiver usando o App-V para implantar o Office 2010 e o Office 2013, você deve sequenciar o Office 2010 no modo não integrado. Para obter mais informações sobre o sequenciamento do Office no modo não integração (isolado), consulte [como sequenciar o Microsoft office 2010 no Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Limitações conhecidas dos cenários de coexistência do Office

As seções a seguir descrevem alguns problemas que você pode encontrar ao usar o App-V para implementar a coexistência com o Office.

### Limitações comuns em cenários de coexistência do Office com base no Windows Installer/com Clique para executar e App-V

As seguintes limitações podem ocorrer quando você instala as seguintes versões do Office no mesmo computador:

-   O Office 2010 usando a versão baseada no Windows Installer

-   Office 2013 usando o App-V

Após a publicação do Office 2013 usando o App-V lado a lado com uma versão anterior do Office 2010 baseado no Windows Installer também pode fazer com que o Windows Installer seja iniciado. Isso ocorre porque a versão baseada no Windows Installer ou clique para executar do Office 2010 está tentando registrar-se automaticamente no computador.

Para ignorar a operação de registro automático do Word nativo do Word 2010, siga estas etapas:

1.  Saia do Word 2010.

2.  Inicie o editor do registro fazendo o seguinte:

    -   No Windows 7: clique em **Iniciar**, digite **regedit** na caixa Iniciar pesquisa e pressione Enter.

    -   No Windows 8,1 ou no Windows 10, digite **regedit** e pressione Enter na página inicial e, em seguida, pressione Enter.

    Se for solicitada uma senha de administrador ou uma confirmação, digite a senha ou clique em **continuar**.

3.  Localize e selecione a seguinte subchave do registro:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  No menu **Editar** , clique em **novo**e, em seguida, clique em **valor DWORD**.

5.  Digite **NoReReg**e pressione Enter.

6.  Clique com o botão direito do mouse em **NoReReg** e clique em **Modificar**.

7.  Na caixa **ValueData** , digite **1**e clique em **OK**.

8.  No menu arquivo, clique em **sair** para fechar o editor do registro.

## <a href="" id="bkmk-office-integration-win"></a>Como o Office se integra ao Windows quando você usa o App-V para implantar o Office


Ao implantar o Office 2013 usando o App-V, o Office é totalmente integrado ao sistema operacional, que fornece aos usuários finais os mesmos recursos e funcionalidades que o Office tem quando ele é implantado sem App-V.

O pacote do Office 2013 App-V é compatível com os seguintes pontos de integração com o sistema operacional Windows:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ponto de extensão</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in de junção de reunião do Lync para Firefox e Chrome</p></td>
<td align="left"><p>O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviado para o driver de impressão do OneNote</p></td>
<td align="left"><p>O usuário pode imprimir no OneNote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Anotações vinculadas do OneNote</p></td>
<td align="left"><p>Anotações vinculadas do OneNote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviar para o suplemento do OneNote para Internet Explorer</p></td>
<td align="left"><p>O usuário pode enviar para o OneNote do IE</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exceção de firewall para o Lync e o Outlook</p></td>
<td align="left"><p>Exceção de firewall para o Lync e o Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente MAPI</p></td>
<td align="left"><p>Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in do SharePoint para Firefox</p></td>
<td align="left"><p>O usuário pode usar os recursos do SharePoint no Firefox</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet do painel de controle de email</p></td>
<td align="left"><p>O usuário Obtém o applet do painel de controle de email no Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assemblies de interoperabilidade primária</p></td>
<td align="left"><p>Suporte a suplementos gerenciados</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador do cache de documentos do Office</p></td>
<td align="left"><p>Permite o cache de documentos para aplicativos do Office</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de pesquisa de protocolo do Outlook</p></td>
<td align="left"><p>O usuário pode pesquisar no Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controles ActiveX:</p></td>
<td align="left"><p>Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx. Joinmanager</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Controle ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Auxiliar do navegador do OneDrive pro</p></td>
<td align="left"><p>Controle ActiveX]</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sobreposições de ícones do OneDrive pro</p></td>
<td align="left"><p>O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensões de shell</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Teclado</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





