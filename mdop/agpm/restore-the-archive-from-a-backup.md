---
title: Restaurar o arquivo morto de um backup
description: Restaurar o arquivo morto de um backup
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797310"
---
# Restaurar o arquivo morto de um backup


Se ocorrer um desastre e o arquivo para o gerenciamento avançado de política de grupo (AGPM) estiver danificado ou destruído, um administrador do AGPM (controle total) pode restaurar o arquivo de uma cópia de backup preparada antecipadamente e, em seguida, importar do ambiente de produção qualquer objeto de política de grupo (GPOs) que não esteja no arquivo morto Para obter informações sobre como restaurar um backup de arquivo morto para um servidor diferente, consulte [mover o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive.md).

Uma conta de usuário que tenha acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) e à pasta que contém o arquivo morto será necessária para concluir esse procedimento.

**Para restaurar o arquivo de um backup**

1.  Interrompa o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Remova o arquivo morto existente. Por padrão, a pasta arquivo morto é%ProgramData%\\Microsoft\\AGPM, no entanto, o administrador do AGPM que instalou o gerenciamento avançado de política de grupo da Microsoft – o servidor pode ter entrado um local diferente durante a instalação.

3.  Recrie a pasta arquivo morto Configurando o caminho do arquivo, a conta do serviço do AGPM, o proprietário do arquivo e a porta de escuta. Não é necessário usar os mesmos valores usados durante a instalação original. Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm30ops.md).

4.  Copie o conteúdo do arquivo morto backup para a pasta de arquivo morto, copiando as subpastas e arquivos para garantir que cada subpasta e arquivo herdem as permissões da pasta arquivo morto. Tome cuidado para não substituir a pasta de arquivo morto.

5.  Se você não tiver certeza sobre se um GPO no backup do arquivo morto é mais recente do que a cópia daquele GPO na produção, gere um relatório de diferença e compare as configurações. Para obter mais informações, consulte [identificar diferenças entre GPOs, versões de GPO ou modelos](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).

6.  Reinicie o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

### Referências adicionais

-   [Fazer backup do arquivo morto](back-up-the-archive.md)

-   [Mover o servidor e o arquivo morto do AGPM](move-the-agpm-server-and-the-archive.md)

-   [Gerenciamento do arquivo morto](managing-the-archive.md)

 

 





