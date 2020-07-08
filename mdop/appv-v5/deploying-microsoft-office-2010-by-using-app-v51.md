---
title: Implantando o Microsoft Office 2010 usando o App-V
description: Implantando o Microsoft Office 2010 usando o App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796546"
---
# Implantando o Microsoft Office 2010 usando o App-V


Você pode criar pacotes do Office 2010 para o Microsoft Application Virtualization (App-V) 5,1 usando um dos seguintes métodos:

-   Sequenciador do Application Virtualization (App-V)

-   Acelerador de pacote do Application Virtualization (App-V)

## Suporte do App-V para o Office 2010


A tabela a seguir mostra as versões do App-V, os métodos de criação de pacotes do Office, o licenciamento com suporte e as implantações com suporte para o Office 2010.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item com suporte</th>
<th align="left">Nível de suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versões do App-V com suporte</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
<li><p>5,1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Criação de pacote</p></td>
<td align="left"><ul>
<li><p>Sequenciamento</p></li>
<li><p>Acelerador de pacote</p></li>
<li><p>Kit de implantação do Office</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Licenciamento compatível</p></td>
<td align="left"><p>Licenciamento por volume</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implantações com suporte</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>VDI pessoal</p></li>
<li><p>AOS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Criando o Office 2010 App-V 5,1 usando o sequenciador


O sequenciamento do Office 2010 é um dos principais métodos para criar um pacote do Office 2010 no App-V 5,1. A Microsoft forneceu uma receita detalhada por meio de um artigo da base de dados de conhecimento. Para criar um pacote do Office 2010 no App-V 5,1, consulte o link a seguir para obter instruções detalhadas:

[Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Criando pacotes do Office 2010 App-V 5,1 usando aceleradores de pacote


Os pacotes do Office 2010 App-V 5,1 podem ser criados por meio de aceleradores de pacote. A Microsoft fornece aceleradores de pacote para a criação do Office 2010 no Windows 10, no Windows 8 e no Windows 7. Para criar pacotes do Office 2010 no App-V usando aceleradores de pacote, consulte as seguintes páginas para acessar o acelerador de pacote apropriado:

-   [Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 8](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Para obter instruções detalhadas sobre como criar pacotes de aplicativos virtuais usando aceleradores de pacotes do App-V, consulte [como criar um pacote de aplicativo virtual usando um acelerador de pacote app-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).

## Implantando o pacote do Microsoft Office para o App-V 5,1


Você pode implantar pacotes do Office 2010 usando qualquer um dos seguintes métodos de implantação do App-V:

-   System Center Configuration Manager

-   Servidor do App-V

-   Autônomos por meio de comandos do PowerShell

## Gerenciamento e personalização do Office App-V Package


Os pacotes do Office 2010 podem ser gerenciados como qualquer outro pacote do App-V 5,1 por meio de mecanismos de gerenciamento de pacotes conhecidos. Nenhuma instrução especial é necessária, por exemplo, para adicionar, publicar, cancelar a publicação ou remover pacotes do Office.

## Integração do Microsoft Office com o Windows


A tabela a seguir fornece uma lista completa de pontos de integração com suporte para o Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ponto de extensão</th>
<th align="left">Descrição</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in de junção de reunião do Lync para Firefox e Chrome</p></td>
<td align="left"><p>O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviado para o driver de impressão do OneNote</p></td>
<td align="left"><p>O usuário pode imprimir no OneNote</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Anotações vinculadas do OneNote</p></td>
<td align="left"><p>Anotações vinculadas do OneNote</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviar para o suplemento do OneNote para Internet Explorer</p></td>
<td align="left"><p>O usuário pode enviar para o OneNote do IE</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exceção de firewall para o Lync e o Outlook</p></td>
<td align="left"><p>Exceção de firewall para o Lync e o Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente MAPI</p></td>
<td align="left"><p>Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in do SharePoint para Firefox</p></td>
<td align="left"><p>O usuário pode usar os recursos do SharePoint no Firefox</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet do painel de controle de email</p></td>
<td align="left"><p>O usuário Obtém o applet do painel de controle de email no Outlook</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assemblies de interoperabilidade primária</p></td>
<td align="left"><p>Suporte a suplementos gerenciados</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador do cache de documentos do Office</p></td>
<td align="left"><p>Permite o cache de documentos para aplicativos do Office</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de pesquisa de protocolo do Outlook</p></td>
<td align="left"><p>O usuário pode pesquisar no Outlook</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controles ActiveX:</p></td>
<td align="left"><p>Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharpoint.OpenXMLDocuments</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx. Joinmanager</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Controle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Auxiliar do navegador do OneDrive pro</p></td>
<td align="left"><p>Controle ActiveX]</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sobreposições de ícones do OneDrive pro</p></td>
<td align="left"><p>O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Recursos adicionais


**Recursos adicionais dos pacotes do Office 2013 App-V**

[Cenários suportados para a implantação do Microsoft Office como um pacote App-V sequenciado](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Pacotes do Office 2010 App-V**

[Kit de sequenciamento do Microsoft Office 2010 para Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Problemas conhecidos ao criar ou usar um pacote do App-V 5,0 do Office 2010](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Grupos de conexão**

[Implantando grupos de conexão no Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Gerenciando grupos de conexão](managing-connection-groups51.md)

**Configuração dinâmica**

[Sobre a configuração dinâmica do App-V 5.1](about-app-v-51-dynamic-configuration.md)






 

 





