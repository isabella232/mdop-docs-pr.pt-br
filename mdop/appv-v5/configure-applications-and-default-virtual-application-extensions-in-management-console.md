---
title: Configurar aplicativos e extensões de aplicativo virtual padrão no console de gerenciamento
description: Como exibir e configurar aplicativos e extensões de aplicativos virtuais padrão usando o Console de Gerenciamento
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796566"
---
#   Configurar aplicativos e extensões de aplicativo virtual padrão no console de gerenciamento

Use o procedimento a seguir para *Exibir* e *Configurar* extensões de pacote padrão.

**Para exibir e configurar extensões de aplicativo virtual padrão**

1.  Para exibir o pacote que você deseja configurar, abra o console de gerenciamento do App-V 5,1. Selecione o pacote que você deseja configurar, clique com o botão direito do mouse no nome do pacote e selecione **Editar configuração padrão**.

2.  Para exibir os aplicativos contidos no pacote especificado, no painel **configuração padrão** , clique em **aplicativos**. Para exibir os atalhos do pacote, clique em **atalhos**. Para exibir as associações de tipo de arquivo para esse pacote, clique em **tipos de arquivo**.

3.  Para habilitar as extensões do aplicativo, selecione **habilitar**.

    Para habilitar atalhos, selecione **Habilitar atalhos**. Para adicionar um novo atalho para o aplicativo selecionado, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **Adicionar novo atalho**. Para remover um atalho, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **remover atalho**. Para editar um atalho existente, clique com o botão direito do mouse no aplicativo e selecione **Editar atalho**.

4.  Para exibir outras extensões de aplicativo, clique em **avançado** e em **Exportar configuração**. Digite um nome de arquivo e clique em **salvar**. Você pode exibir todas as extensões de aplicativo associadas ao pacote usando o arquivo de configuração.

5.  Para editar outras extensões de aplicativo, modifique o arquivo de configuração e clique em **importar e substitua essa configuração**. Selecione o arquivo modificado e clique em **abrir**. Na caixa de diálogo, clique em **substituir** para concluir o processo.

>**Observação** Se o upload falhar e o tamanho do arquivo de configuração for superior a 4 MB, será necessário aumentar o tamanho máximo de arquivo permitido pelo servidor. Isso pode ser feito adicionando o atributo maxRequestLength com um valor maior do que o tamanho do seu arquivo de configuração (em KB) ao elemento httpRuntime na linha 26 de `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .  
Por exemplo, alterar `<httpRuntime targetFramework="4.5"/>` para `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` aumentará o tamanho máximo para 8MB


**Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





