---
title: Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V
description: Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799548"
---
# Como gerenciar o redirecionamento da URL usando o empacotador de espaço de trabalho da MED-V


Você pode usar o pacote do espaço de trabalho do MED-V para gerenciar o redirecionamento de URL no espaço de trabalho do MED-V.

**Para gerenciar o redirecionamento de endereço Web em um espaço de trabalho do MED-V**

1.  Para abrir o **pacote do espaço de trabalho do MED-V**, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-v**.

2.  No painel principal do **pacote de espaço de trabalho do MED-V** , clique em **gerenciar redirecionamento da Web**.

3.  Na janela **gerenciar redirecionamento da Web** , você pode digitar, colar ou importar uma lista das URLs redirecionadas para o Internet Explorer no espaço de trabalho do MED-V.

    **Observação**  
    O redirecionamento de URL no MED-V só oferece suporte aos protocolos HTTP e HTTPS. O MED-V não oferece suporte para FTP ou outros protocolos.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Clique em **salvar como...** para salvar os arquivos de redirecionamento de URL atualizados na pasta especificada. O MED-V cria um arquivo de registro que contém as informações atualizadas de redirecionamento de URL. Implante a chave do registro atualizada usando a política de grupo. Para obter mais informações sobre como usar a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   O MED-V também cria um script do Windows PowerShell na pasta especificada que você pode usar para recriar o pacote do espaço de trabalho do MED-V atualizado.

## Tópicos relacionados


[Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Gerenciar o redirecionamento da URL da MED-V](manage-med-v-url-redirection.md)









