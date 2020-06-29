---
title: Como definir as configurações de Registro do cliente do App-V usando a linha de comando
description: Como definir as configurações de Registro do cliente do App-V usando a linha de comando
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797217"
---
# Como definir as configurações de Registro do cliente do App-V usando a linha de comando


Após a implantação e configuração do cliente do Application Virtualization (App-V) durante a instalação usando a linha de comando, talvez seja necessário alterar uma ou mais configurações de cliente. Isso é feito editando-se as chaves do registro apropriadas usando um dos seguintes métodos:

-   Usar o editor de registro diretamente

-   Usando um arquivo. reg

-   Usando uma linguagem de script como VBScript ou Windows PowerShell

Também há um modelo ADM que você pode usar. Para obter mais informações sobre o modelo ADM, consulte <https://go.microsoft.com/fwlink/?LinkId=121835> .

**Cuidado**  Tome cuidado ao editar o registro porque os erros podem deixar o computador em um estado inutilizável. Certifique-se de seguir as práticas comerciais padrão relacionadas às edições do registro. Teste completamente todas as alterações propostas em um ambiente de teste antes de implantá-las nos computadores de produção.

 

## Nesta seção


**Importante**  Em um computador de 64 bits, as chaves e os valores descritos nas seções a seguir estarão em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[Como redefinir o cache do FileSystem](how-to-reset-the-filesystem-cache.md)  
Fornece as informações necessárias para redefinir o cache do sistema de arquivos.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[Como alterar o tamanho do cache do FileSystem](how-to-change-the-size-of-the-filesystem-cache.md)  
Explica como você pode alterar o tamanho do cache.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[Como Usar o Recurso de Gerenciamento de Espaço do Cache](how-to-use-the-cache-space-management-feature.md)  
Descreve como você pode configurar o recurso de gerenciamento de espaço em cache.

<a href="" id="how-to-configure-the-client-log-file"></a>[Como configurar o arquivo de log do cliente](how-to-configure-the-client-log-file.md)  
Descreve os vários valores da chave do registro que controlam o arquivo de log do cliente e como você pode alterá-los.

<a href="" id="how-to-configure-user-permissions"></a>[Como configurar permissões de usuário](how-to-configure-user-permissions.md)  
Identifica a chave do registro que controla as permissões do usuário e fornece exemplos de como você pode alterar algumas permissões.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[Como configurar o cliente para recuperação de pacote de aplicativo](how-to-configure-the-client-for-application-package-retrieval.md)  
Explica como configurar o cliente para recuperar conteúdo do pacote, ícones e associações de tipo de arquivo de fontes diferentes e fornece vários exemplos de formato de caminho correto.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[Como configurar o cliente para o Modo de Operação Desconectada](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Fornece informações sobre como definir as várias configurações associadas ao modo de operações desconectadas.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[Como configurar o comportamento de atalhos e de associações de tipo de arquivo](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
Descreve os valores da chave do registro que controlam atalhos e associações de tipo de arquivo no cliente App-V e fornece detalhes sobre como configurá-los.

## Tópicos relacionados


[Cliente do Application Virtualization](application-virtualization-client.md)

 

 





