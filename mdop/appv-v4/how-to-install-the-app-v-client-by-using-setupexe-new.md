---
title: Como instalar o cliente do App-V usando Setup.exe
description: Como instalar o cliente do App-V usando Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797105"
---
# Como instalar o cliente do App-V usando Setup.exe


Este tópico descreve como instalar o cliente App-V usando o programa setup.exe. Quando você instala o cliente App-V usando o programa setup.exe, o instalador determina qual software de pré-requisito é necessário e o instala automaticamente antes de instalar o cliente.

**Para instalar o cliente do Application Virtualization usando o Setup.exe**

1.  Verifique se você está conectado com uma conta que tem direitos de administrador no computador.

2.  Abra uma janela do prompt de comando e, em seguida, altere o diretório para a pasta que contém os arquivos de instalação. Ao instalar a versão 4.6 ou posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits. A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.

3.  Digite a cadeia de caracteres do comando instalar no prompt de comando. Você também pode criar um arquivo de comando e executá-lo a partir do prompt de comando. Você também pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar o comando.

4.  O exemplo de linha de comando a seguir mostra como setup.exe pode ser usado com vários parâmetros opcionais. Para obter mais informações sobre esses parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).

    **"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" produção System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **Importante**  
    -   As aspas que aparecem na seção "**/v**" devem ser tratadas como caracteres especiais e inseridas com um " **\\** " anterior. As aspas são necessárias somente quando o valor contém um espaço; no entanto, para consistência, todas as instâncias no exemplo anterior são mostradas como tendo aspas.

    -   Os **%** caracteres "" em "**% HomeDrive%**" devem ser precedidos pelo **^** caractere de escape "". Caso contrário, o Shell de comando do Windows define o valor para aquele do usuário que está executando a instalação.

    -   As opções do **InstallShield** **/s** e **/qn** são necessárias para fazer com que essa instalação seja silenciosa. A opção **/qn** deve seguir a opção **/v** , separada por apenas um caractere de aspas sem espaços intervenientes.

    -   A pasta especificada no valor **SWIGLOBALDATA** já deve existir.

     

5.  Quando a instalação estiver concluída, recomendamos que você execute um exame do Microsoft Update para garantir que as atualizações mais recentes sejam instaladas.

## Tópicos relacionados


[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





