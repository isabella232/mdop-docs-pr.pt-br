---
title: Informações para solução de problemas do Application Virtualization Client
description: Informações para solução de problemas do Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796676"
---
# Informações para solução de problemas do Application Virtualization Client


Este tópico inclui informações que você pode usar para solucionar vários problemas no cliente do Application Virtualization (App-V).

## A atualização de publicação está muito lenta


Se a atualização de publicação em um computador específico demorar muito mais do que o esperado e se o cliente estiver configurado para usar a configuração **IconSourceRoot** , determine se **IconSourceRoot** contém uma URL inválida. Uma URL inválida causará atrasos muito longos durante A atualização da publicação.

## Os usuários não conseguem se conectar ao servidor e vão para o modo de operações desconectadas


Quando você estiver usando um servidor de gerenciamento App-V configurado com o protocolo RTSPs, se os usuários não conseguirem se conectar e entrarem no modo operações desconectadas, determine se o certificado que está sendo usado no servidor é válido. Um certificado inválido impedirá que os usuários se conectem e farão com que eles entrem no modo operações desconectadas.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Os usuários experimentam desempenho lento quando os aplicativos não são totalmente armazenados em cache


Quando os aplicativos não são totalmente armazenados em cache, os usuários podem ocasionalmente sofrer um desempenho temporário lento ou intermitente ao iniciar ou usar o aplicativo. Há vários possíveis motivos pelos quais isso pode ocorrer — por exemplo, quando o cliente App-V está em processo de carregamento automático de um aplicativo ou quando uma solicitação fora da sequência está sendo processada. Quando os aplicativos estiverem totalmente armazenados em cache, esses problemas não ocorrerão mais.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>Erro exibido após a remoção de uma atualização


Você deve usar o formato de comando correto do Windows Installer 3,1 para remover uma atualização do cliente App-V da seguinte maneira:

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

Usar o formato de comando antigo causará o `msiexec /package <GUID> /uninstall <GUID>` erro 6003 "não foi possível iniciar o cliente do Application Virtualization".

## Código de erro 0A-0000E01E ocorre quando você tenta iniciar um aplicativo


O código de erro 0A-0000E01E indica que o pacote do aplicativo sequenciado pode estar corrompido. A solução é resequenciar o pacote.

## Os usuários não podem acessar arquivos que eles criaram na unidade p:


Se os usuários salvarem arquivos na unidade **p:** , eles não poderão recuperá-los porque não têm direitos de leitura na unidade. Os usuários não devem salvar arquivos na unidade **p:** .

## O usuário é solicitado com um erro de 1D1


Quando a URL de streaming de arquivo está definida incorretamente no arquivo Open Software Descriptor (OSD), o cliente App-V retorna um erro 1D1 em vez de um erro "arquivo não encontrado". Esse erro indica que o início do aplicativo falhou e o usuário foi forçado para o modo de operações desconectadas. Corrija a URL de streaming de arquivo.

## Ícones incorretos associados a alguns aplicativos


Quando um ícone deve ser usado em uma operação de publicação, o cliente App-V primeiro determina se ele já tem uma cópia em cache do ícone, olhando o cache de ícone para um item cujo caminho de origem original corresponde ao caminho do ícone fornecido para a operação de publicação. Se o cliente App-V encontrar uma correspondência, ele usará o ícone já em cache; caso contrário, ele fará o download do novo ícone no cache. Se o caminho para o ícone for um diretório de rascunho ou se for reutilizado para novos ícones ou pacotes, a pesquisa no cache pode selecionar o ícone errado de uma operação anterior.

## Os usuários são solicitados a fornecer credenciais ao iniciar um aplicativo


Se um usuário tentar iniciar um aplicativo virtual ao qual o administrador do sistema restringiu o acesso, o usuário pode ser solicitado a inserir as credenciais. O usuário deve digitar o nome de usuário e a senha de uma conta que tenha permissão para iniciar o aplicativo e, em seguida, pressionar ENTER.

## Atualização de publicação falha após a atualização do cliente App-V para a versão 4,5


Se o diretório de dados do usuário era colocado anteriormente em um local não padrão (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nome_do_usuário*%), os usuários que não têm privilégios de administrador no computador descobrirão que a atualização de publicação falha após a atualização do cliente App-V. Durante a atualização, o diretório de dados global do aplicativo App-V do cliente e todos os seus subdiretórios são configurados com direitos de acesso restritos somente para administradores. Você pode evitar esse problema alterando o diretório de dados do usuário antes da atualização para que ele não seja um subdiretório do diretório de dados globais.

## Reinicialização necessária após falha na instalação


Se a instalação do cliente falhar por qualquer motivo e se as tentativas subsequentes de instalar o cliente também falharem, verifique o log do Windows Installer para ver se ele mostra um erro "sftplay Failed, Error = 1072". Em caso afirmativo, reinicie o computador antes de tentar instalar o cliente novamente.

## Reparar um aplicativo virtual corrompido


Se, por qualquer motivo, um pacote de aplicativo virtual instalado usando um arquivo MSI (pacote do Windows Installer) for corrompido, reinstale o pacote. A função de reparo disponível no Windows Installer não atualizará os volumes do usuário.

## Tópicos relacionados


[Referência do Application Virtualization Client](application-virtualization-client-reference.md)

 

 





