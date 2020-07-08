---
title: Notas de versão do MED-V 1.0
description: Notas de versão do MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799903"
---
# Notas de versão do MED-V 1.0


## Problemas conhecidos com o MED-V


Esta seção fornece as informações mais atualizadas sobre problemas gerais com a plataforma da virtualização de área de trabalho do Microsoft Enterprise (MED-V). Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Sempre que possível, esses problemas serão resolvidos em versões posteriores.

### Downloads de arquivos não seguem regras de redirecionamento da Web

Downloads de arquivos não seguem regras de redirecionamento da Web definidas em uma política do espaço de trabalho do MED-V.

### Ao expandir uma janela do aplicativo publicado pelo console para tela inteira, ele desaparece

Se você expandir uma janela de aplicativo publicado no console (como cmd.exe) para tela inteira dentro de um espaço de trabalho do MED-V configurado no modo de integração sem falhas, a janela do aplicativo poderá desaparecer ou não responder.

### Ao trabalhar no modo de área de trabalho completo, os locais dos ícones na área de trabalho não são salvos

Ao trabalhar no modo de área de trabalho completo, as alterações de localização manual dos ícones na área de trabalho não são salvas entre sessões do espaço de trabalho do MED-V.

### Uma imagem local e uma imagem de teste com o mesmo nome não podem existir no mesmo domínio

Se uma imagem local estiver incluída no domínio e o administrador criar uma nova versão da mesma imagem com o mesmo nome de computador que uma imagem de teste, quando a imagem de teste entrar no domínio, a ação de ingresso no domínio falhará ou será bem-sucedida e a imagem local será removida do domínio.

### O MED-V não oferece suporte aos recursos do Windows Aero

O MED-V não oferece suporte aos recursos do Windows Aero (como o Aero Flip 3D).

### O console de gerenciamento pode ser usado por apenas um usuário do Windows por computador

O console de gerenciamento do MED-V pode ser usado apenas por administradores e pelo usuário do Windows que instalou o aplicativo de gerenciamento.

### O utilitário de configuração do servidor MED-V testa a conectividade do Microsoft SQL Server em contexto do usuário, em vez do contexto do serviço do servidor MED-V

O MED-V usa o contexto do serviço do servidor MED-V para coletar relatórios do banco de dados relatórios do Microsoft SQL Server. O utilitário de configuração do MED-V Server verifica o banco de dados e testa a cadeia de conexão do banco de dados. Ele não valida o acesso do serviço do servidor MED-V ao banco de dados.

 

 





