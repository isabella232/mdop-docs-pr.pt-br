---
title: Gerenciamento de atualizações de software para espaços de trabalho da MED-V
description: Gerenciamento de atualizações de software para espaços de trabalho da MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799547"
---
# Gerenciamento de atualizações de software para espaços de trabalho da MED-V


Você tem várias opções diferentes disponíveis para fornecer atualizações de software para os aplicativos no espaço de trabalho do MED-V implantado.

**Observação**  Para obter informações sobre como especificar as configurações de configuração que definem como o MED-V recebe atualizações automáticas, consulte [gerenciando atualizações automáticas para os espaços de trabalho do MED-v](managing-automatic-updates-for-med-v-workspaces.md).

 

**Atualizando o software em um espaço de trabalho do MED-V**

1.  **Usando um sistema de distribuição de software eletrônico**

    Se a sua organização usa um sistema ESD (sistema de distribuição de software eletrônico) para implantar um software, você pode usá-lo para fornecer atualizações de software para aplicativos em espaços de trabalho do MED-V, da mesma forma que fornece atualizações para aplicativos em computadores físicos.

2.  **Usar a política de grupo**

    Se a sua organização implantar o software usando a política de grupo, você poderá usá-lo para fornecer atualizações de software para aplicativos em espaços de trabalho do MED-V da mesma forma que fornece atualizações para aplicativos em computadores físicos.

3.  **Usando a virtualização de aplicativos (APP-V)**

    Se você usa MED-V juntamente com o App-V, é possível fornecer atualizações de software para aplicativos no espaço de trabalho do MED-V seguindo as etapas exigidas pela App-V para a atualização do software. Para obter mais informações, consulte [virtualização de aplicativo](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

4.  **Atualização do software na imagem principal**

    Embora não seja considerada uma prática recomendada do MED-V, você pode instalar atualizações de software para aplicativos na imagem principal. Depois de instalar as atualizações, você pode reimplantar o espaço de trabalho do MED-V novamente em sua empresa da mesma forma que o implantou originalmente.

    **Importante**  Não recomendamos esse método de gerenciamento de atualizações de software. Além disso, se você atualizar o software na imagem principal e reimplantar o espaço de trabalho do MED-V novamente em sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.

     

## Tópicos relacionados


[Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V](managing-automatic-updates-for-med-v-workspaces.md)

[Como testar a publicação de aplicativos](how-to-test-application-publishing.md)

[Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





