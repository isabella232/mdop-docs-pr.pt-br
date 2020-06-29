---
ms.reviewer: ''
title: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0
description: Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796301"
---
# Como usar um aplicativo App-V 4,6 a partir de um aplicativo App-V 5,0

*Observação:** App-V 4,6 saiu do suporte básico. O seguinte se aplica a um pacote App-V 4,6 SP3.

Use o procedimento a seguir para executar um aplicativo App-V 4.6 com aplicativos do App-V 5,0 em um cliente autônomo.

**Para executar aplicativos em um cliente autônomo**

1.  Selecione dois aplicativos em seu ambiente que podem ser abertos uns dos outros. Por exemplo, Microsoft Outlook e Adobe Acrobat Reader. Você pode acessar um anexo de email criado usando o Adobe Acrobat.

2.  Converta os pacotes ou crie um novo pacote para qualquer um dos aplicativos usando o formato App-V 5,0. Para obter mais informações sobre como converter pacotes, consulte [como migrar pontos de extensão de um pacote app-v 4,6 para um pacote app-v 5,0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) ou [como migrar pontos de extensão de um pacote app-v 4,6 para o app-v 5,0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).

3.  Adicione e provisione o pacote usando o console de gerenciamento do App-V 5,0. Para obter mais informações sobre como adicionar e provisionar pacotes, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [como configurar o acesso aos pacotes usando o console de gerenciamento](how-to-configure-access-to-packages-by-using-the-management-console-50.md).

4.  O aplicativo convertido agora é executado usando o App-V 5,0 e você pode abrir um aplicativo da outra. Por exemplo, se você converteu um pacote do Microsoft Office em um pacote do App-V 5,0 e o Adobe Acrobat ainda está sendo executado como um pacote App-V 4.6, você pode abrir um anexo do Adobe Acrobat Reader usando o Microsoft Outlook.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 








