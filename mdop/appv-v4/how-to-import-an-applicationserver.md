---
title: Como importar um aplicativo
description: Como importar um aplicativo
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797118"
---
# Como importar um aplicativo


Normalmente, você importa aplicativos para disponibilizá-los para o fluxo de um servidor de gerenciamento do Application Virtualization. Você também pode adicionar um aplicativo manualmente, mas deve fornecer informações precisas e detalhadas sobre o aplicativo para fazer isso. Para obter mais informações, consulte [como adicionar um aplicativo manualmente](how-to-manually-add-an-application.md).

**Observação**  Para importar um aplicativo, você deve ter o arquivo Open Software Descriptor (OSD) em seqüência ou o arquivo de projeto do sequenciador (SPRJ) disponível no servidor.

 

Ao importar um aplicativo, você deve certificar-se de que o servidor está configurado com um valor no campo **caminho de conteúdo padrão** na guia **geral** da caixa de diálogo **Opções do sistema** (acessível, clicando com o botão direito do mouse no nó do **sistema** App-V do App-V Server). O valor padrão de caminho de conteúdo define onde os aplicativos serão importados e durante o processo de importação, esse valor é usado para modificar os caminhos definidos no arquivo OSD para o arquivo SFT e para os atalhos de ícone. No arquivo OSD, o caminho para o arquivo SFT é especificado na entrada HREF de CODEBASE e o caminho para os ícones é especificado na entrada atalhos.

Durante o processo de importação, o protocolo, o servidor e, se estiverem presentes, a porta especificada nesses dois caminhos no arquivo OSD serão substituídas pelo valor do caminho de conteúdo padrão. A tabela a seguir fornece um exemplo de como o caminho de importação será afetado.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Caminho de conteúdo padrão</th>
<th align="left">BASE de código do arquivo OSD HREF</th>
<th align="left">Valor resultante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**Para importar um aplicativo**

1.  Clique com o botão direito do mouse no nó **aplicativos** no painel esquerdo e escolha **importar aplicativos**.

2.  Na caixa de diálogo **abrir** , navegue até o arquivo SPRJ ou OSD do aplicativo. Realce o arquivo e clique em **abrir**.

3.  No **Assistente para novo aplicativo**, certifique-se de que a caixa **habilitado** esteja selecionada para os aplicativos que você deseja transmitir. Você também pode inserir uma descrição e verificar os caminhos do servidor e do arquivo. Além disso, se você tiver configurado licenças e grupos de servidores, poderá selecionar esses grupos.

4.  Clique em **Avançar**.

5.  Na tela **atalhos publicados** , marque as caixas dos locais onde você gostaria que os atalhos do aplicativo aparecessem nos computadores cliente.

6.  Clique em **Avançar**.

7.  Na tela **associações de arquivo** , você pode adicionar novas associações de arquivo a esse aplicativo. Para fazer isso, clique em **Adicionar**, insira a extensão (sem um ponto precedente), insira uma descrição e clique em **OK**.

    **Observação**  Aplicativos sequenciados com o sequenciador 4,0 preencha a caixa de diálogo **associações de arquivos** ao importar ou criá-las por meio do console de gerenciamento. Aplicativos com pacotes de versão do sequenciador anteriores não.

     

8.  Clique em **Avançar**.

9.  Na tela **permissões de acesso** , clique em **Adicionar**.

10. Preencha a caixa de diálogo **Selecionar grupos** . Quando terminar, clique em **OK**.

11. Clique em **Avançar**.

12. Na tela **Resumo** , você pode revisar as configurações de importação. Clique em **concluir**ou em **retornar** para alterar a importação ou clique em **Cancelar** para cancelar a importação.

## Tópicos relacionados


[Como gerenciar grupos de aplicativos no Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Como gerenciar aplicativos no Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

[Como adicionar um aplicativo manualmente](how-to-manually-add-an-application.md)

 

 





