---
title: Restaurar o arquivo morto de um backup
description: Restaurar o arquivo morto de um backup
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797317"
---
# Restaurar o arquivo morto de um backup


Se ocorrer um desastre e o arquivo para o gerenciamento avançado de política de grupo (AGPM) estiver danificado ou destruído, um administrador do AGPM (controle total) pode restaurar o arquivo de uma cópia de backup preparada antecipadamente e, em seguida, importar do ambiente de produção do domínio qualquer objeto de política de grupo (GPOs) que não esteja no arquivo morto Para obter informações sobre como restaurar um backup de arquivo morto para um servidor diferente, consulte [mover o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive-agpm40.md).

Uma conta de usuário que tenha acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) e à pasta que contém o arquivo morto será necessária para concluir esse procedimento.

**Para restaurar o arquivo de um backup**

1.  Interrompa o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).

2.  Remova o arquivo morto existente. Por padrão, a pasta arquivo morto é%ProgramData%\\Microsoft\\AGPM, no entanto, o administrador do AGPM que instalou o gerenciamento avançado de política de grupo da Microsoft – o servidor pode ter entrado um local diferente durante a instalação.

3.  Recrie a pasta arquivo morto Configurando o caminho do arquivo, a conta do serviço do AGPM, o proprietário do arquivo e a porta de escuta. Não é necessário usar os mesmos valores usados durante a instalação original. Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).

4.  Copie o conteúdo do arquivo morto backup para a pasta de arquivo morto, copiando as subpastas e arquivos para garantir que cada subpasta e arquivo herdem as permissões da pasta arquivo morto. Tome cuidado para não substituir a pasta de arquivo morto.

5.  Se você não tiver certeza sobre se um GPO no backup do arquivo morto é mais recente do que a cópia daquele GPO na produção, gere um relatório de diferença e compare as configurações. Para obter mais informações, consulte [identificar diferenças entre GPOs, versões de GPO ou modelos](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).

6.  Reinicie o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).

### Referências adicionais

-   [Fazer backup do arquivo morto](back-up-the-archive-agpm40.md)

-   [Mover o servidor e o arquivo morto do AGPM](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Gerenciamento do arquivo morto](managing-the-archive-agpm40.md)

 

 





