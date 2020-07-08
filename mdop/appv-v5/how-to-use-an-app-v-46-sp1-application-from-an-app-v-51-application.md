---
title: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,1
description: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,1
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796299"
---
# Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,1

*Observação:** App-V 4,6 saiu do suporte básico. O seguinte se aplica a um pacote App-V 4,6 SP3.

Use o procedimento a seguir para executar um aplicativo App-V 4.6 com aplicativos do App-V 5,1 em um cliente autônomo.

**Observação**  Este procedimento pressupõe que você esteja executando a versão mais recente do App-V 4,6.

**Para executar aplicativos em um cliente autônomo**

1.  Selecione dois aplicativos em seu ambiente que podem ser abertos uns dos outros. Por exemplo, Microsoft Outlook e Adobe Acrobat Reader. Você pode acessar um anexo de email criado usando o Adobe Acrobat.

2.  Converta os pacotes ou crie um novo pacote para qualquer um dos aplicativos usando o formato App-V 5,1. Para obter mais informações sobre como converter pacotes, consulte [como migrar pontos de extensão de um pacote app-v 4,6 para um pacote app-v 5,1 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) ou [como migrar pontos de extensão de um pacote app-v 4,6 para o app-v 5,1 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

3.  Adicione e provisione o pacote usando o console de gerenciamento do App-V 5,1. Para obter mais informações sobre como adicionar e provisionar pacotes, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) e [como configurar o acesso aos pacotes usando o console de gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-51.md).

4.  O aplicativo convertido agora é executado usando o App-V 5,1 e você pode abrir um aplicativo da outra. Por exemplo, se você converteu um pacote do Microsoft Office em um pacote do App-V 5,1 e o Adobe Acrobat ainda está sendo executado como um pacote App-V 4.6, você pode abrir um anexo do Adobe Acrobat Reader usando o Microsoft Outlook.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





