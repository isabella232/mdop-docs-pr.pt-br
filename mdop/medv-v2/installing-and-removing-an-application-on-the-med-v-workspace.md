---
title: Instalação e remoção de um aplicativo no espaço de trabalho da MED-V
description: Instalação e remoção de um aplicativo no espaço de trabalho da MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800028"
---
# Instalação e remoção de um aplicativo no espaço de trabalho da MED-V


Os aplicativos que são incompatíveis com o sistema operacional do host podem ser executados no espaço de trabalho do MED-V e abertos no espaço de trabalho do MED-V da mesma maneira que eles são abertos a partir do computador host, no menu **Iniciar** ou usando um atalho de localhost.

Depois de implantar um espaço de trabalho do MED-V, você tem várias opções diferentes disponíveis para instalar e remover aplicativos no espaço de trabalho do MED-V. Essas opções incluem o seguinte:

-   [Usar a política de grupo](#bkmk-grouppolicy)

-   [Usando um sistema de distribuição de software eletrônico](#bkmk-esd)

-   [Usando a virtualização de aplicativos (APP-V)](#bkmk-appv)

-   [Atualizando a imagem principal](#bkmk-coreimage)

**Importante**  Para garantir que um aplicativo instalado seja automaticamente publicado no host, instale o aplicativo na máquina virtual para **todos os usuários**. Para obter mais informações sobre a publicação de aplicativos, consulte [como publicar e cancelar a publicação de um aplicativo no espaço de trabalho do MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).

 

**Dica**  O MED-V não é compatível com o redirecionamento de convidado para host para manipulação de conteúdo, como clicar duas vezes em um documento do Microsoft Word no Internet Explorer no espaço de trabalho do MED-V. Portanto, os aplicativos necessários, como o Microsoft Word, devem ser instalados no espaço de trabalho do MED-V para fornecer a funcionalidade padrão de manipulação de conteúdo que um usuário final pode esperar.

 

## <a href="" id="bkmk-grouppolicy"></a> Adicionando e removendo aplicativos usando a política de grupo


Você pode usar a política de grupo e os objetos de política de grupo para atribuir ou publicar aplicativos em todos ou alguns espaços de trabalho do MED-V na sua empresa. Para aplicativos atribuídos, quando um usuário final faz logon em seu computador, o aplicativo é exibido no menu **Iniciar** . Quando eles selecionarem o novo aplicativo pela primeira vez, o aplicativo será instalado e estará pronto para uso. Para aplicativos publicados, o aplicativo não é exibido no menu **Iniciar** . Ele só está disponível para o usuário final instalar usando **Adicionar ou remover programas** no painel de **controle** ou abrindo um arquivo associado ao aplicativo.

Você também pode usar a política de grupo e objetos de política de grupo da mesma maneira para remover aplicativos do espaço de trabalho do MED-V.

Para obter mais informações sobre como adicionar e remover aplicativos usando a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> Adicionar e remover aplicativos usando um sistema ESD


Um sistema ESD (Electronic Software Distribution) foi projetado para a implantação eficiente de software e outras informações para vários computadores diferentes em conexões de rede. Se a sua organização usa um sistema ESD para implantar o software, você pode usá-lo para adicionar e remover aplicativos em espaços de trabalho do MED-V da mesma forma que adiciona e remove aplicativos em computadores físicos.

## <a href="" id="bkmk-appv"></a> Adicionando e removendo aplicativos usando o APP-V


O Microsoft Application Virtualization (App-V) fornece a funcionalidade administrativa para disponibilizar aplicativos para os computadores de usuários finais sem precisar instalar os aplicativos diretamente nesses computadores. Você pode querer usar o MED-V e o App-V juntos, se, por exemplo, a sua organização tiver aplicativos que você tenha sequenciado com o App-V no Windows XP, e resequenciar os mesmos atrasaria a migração para o Windows 7.

Você pode usar o MED-V em conjunto com o App-V para adicionar e remover aplicativos virtuais em um espaço de trabalho do MED-V implantado. Para gerenciar aplicativos dessa maneira, primeiro você deve instalar o agente do App-V no sistema operacional de convidado do MED-V. Em seguida, você pode usar o App-V no espaço de trabalho do MED-V para adicionar e remover os aplicativos virtuais.

Para obter informações sobre como instalar e usar o App-V, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

**Importante**  Os aplicativos do App-V que você publica no espaço de trabalho do MED-V têm associações de tipo de arquivo que não podem ser redirecionadas do computador host para a máquina virtual convidada. No entanto, o usuário final ainda pode acessar esses tipos de arquivo clicando em **arquivo**e, em seguida, clicando em **abrir** no aplicativo publicado do App-V.

Para forçar o redirecionamento dessas associações de tipo de arquivo, consulte App-V para associações de tipo de arquivo mapeado digitando o seguinte em um prompt de comando na máquina virtual convidada: **SFTMIME/QUERY OBJ: Type**. Em seguida, mapeie essas associações de tipo de arquivo no computador host.

 

## <a href="" id="bkmk-coreimage"></a> Adicionar e remover aplicativos na imagem principal


Embora não seja considerada uma prática recomendada do MED-V, você pode adicionar e remover aplicativos diretamente na imagem principal. Depois de adicionar ou remover um aplicativo, você pode reimplantar o espaço de trabalho do MED-V novamente em sua empresa da mesma forma que o implantou originalmente.

Para obter mais informações sobre como adicionar ou remover aplicativos na imagem principal, consulte [Instalando aplicativos em uma imagem do Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).

**Importante**  Não recomendamos esse método de gerenciamento de aplicativos. Se você adicionar ou remover aplicativos da imagem principal e reimplantar o espaço de trabalho do MED-V novamente em sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.

 

**Observação**  Embora um aplicativo seja instalado em um espaço de trabalho do MED-V, você também pode ter que publicar o aplicativo antes que ele fique disponível para o usuário final. Por exemplo, talvez seja necessário publicar um aplicativo instalado se a instalação não criar automaticamente um atalho no menu **Iniciar** . Da mesma forma, para cancelar a publicação de um aplicativo, talvez seja necessário remover manualmente um atalho do menu **Iniciar** .

Por padrão, a maioria dos aplicativos é publicada no momento em que eles são instalados, quando os atalhos são automaticamente criados e habilitados.

 

## Tópicos relacionados


[Como testar a publicação de aplicativos](how-to-test-application-publishing.md)

[Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





