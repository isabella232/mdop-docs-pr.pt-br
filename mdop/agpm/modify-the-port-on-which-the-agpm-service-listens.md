---
title: Modificar a porta na qual o serviço do AGPM escuta
description: Modificar a porta na qual o serviço do AGPM escuta
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797735"
---
# Modificar a porta na qual o serviço do AGPM escuta


O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção. Por padrão, o serviço do AGPM escuta na porta 4600. Você pode alterar essa porta modificando o arquivo de índice de arquivo de gerenciamento avançado de política de grupo (AGPM) para cada arquivo morto.

**Observação**  Antes de modificar a porta na qual o serviço do AGPM escuta, é recomendável que você faça backup do arquivo de índice do arquivamento do AGPM (gpostate.xml). Esse arquivo está localizado na pasta inserida como o caminho do arquivo morto durante a instalação do gerenciamento avançado de política de grupo-servidor. Por padrão, esse local desse arquivo é% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml no servidor do AGPM. Se você não souber qual computador hospeda o arquivo, poderá seguir o procedimento para modificar o caminho do arquivo morto para exibir o caminho de arquivo morto atual. Para obter mais informações, consulte [Modificar o caminho do arquivo morto](modify-the-archive-path.md).

 

Uma conta de usuário com acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) e o arquivo de índice do arquivo morto é necessário para concluir este procedimento.

**Para modificar a porta na qual o serviço do AGPM escuta**

1.  No computador que hospeda o arquivo morto, abra o arquivo de índice de arquivo (gpostate.xml) em um editor de texto.

2.  No arquivo, procure **AGPM: Port = "4600"**.

3.  Substitua **4600** pela porta na qual o serviço do AGPM deve escutar; em seguida, salve e feche o arquivo.

4.  No servidor do AGPM, reinicie o serviço do AGPM. (Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service.md).)

5.  Modifique a porta na conexão do servidor do AGPM para cada administrador de política de grupo. (Para obter mais informações, consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).)

6.  Repita para cada servidor de arquivamento e AGPM.

### Referências adicionais

-   [Gerenciamento do serviço AGPM](managing-the-agpm-service.md)

 

 





