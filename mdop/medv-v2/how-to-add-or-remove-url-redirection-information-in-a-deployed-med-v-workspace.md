---
title: Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V
description: Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799873"
---
# Como adicionar ou remover as informações de redirecionamento de URL de um espaço de trabalho implantado da MED-V


Para editar informações de redirecionamento de URL em um espaço de trabalho do MED-V implantado, recomendamos que você atualize o registro do sistema usando a política de grupo. Embora não recomendemos isso, você também pode recriar e reimplantar o espaço de trabalho do MED-V com as informações atualizadas de redirecionamento de URL.

A chave do registro geralmente está localizada em:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

O seguinte valor de cadeia de caracteres múltipla deve estar presente: `RedirectUrls`

Os dados de valor para `RedirectUrls` são uma lista de todas as URLs que você especificou para redirecionamento quando criou o pacote do espaço de trabalho do MED-v usando o **pacote do espaço de trabalho do MED-v**. Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).

Você pode adicionar e remover informações de redirecionamento de URL executando uma das seguintes tarefas:

-   [Editar a chave do registro de redirecionamento de URL e implantar usando a política de grupo](#bkmk-editreg)

-   [Editar o arquivo de texto de redirecionamento de URL e recriar o espaço de trabalho do MED-V](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**Para atualizar as informações de redirecionamento de URL usando a política de grupo**

1.  Edite o valor da chave múltipla da chave do registro que é chamado `RedirectUrls` . Esse valor geralmente está localizado em:

    Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

    Se você estiver adicionando URLs à chave do registro, insira uma por linha, conforme necessário, quando criou o pacote do espaço de trabalho do MED-V. Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).

2.  Implante a chave do registro atualizada usando a política de grupo. Para obter mais informações sobre como usar a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

**Observação**  Esse método de edição de informações de redirecionamento de URL é uma prática recomendada do MED-V.

 

<a href="" id="bkmk-edittext"></a>**Para recriar o espaço de trabalho do MED-V usando um arquivo de texto de URL atualizado**

-   Outro método para adicionar e remover URLs da lista de redirecionamento é atualizar o arquivo de texto de redirecionamento de URL e usá-lo para criar um novo espaço de trabalho do MED-V. Em seguida, você pode reimplantar o espaço de trabalho do MED-V como antes, usando o processo padrão de implantação, como um sistema ESD.

    **Importante**  Não recomendamos esse método de edição de informações de redirecionamento de URL. Além disso, a qualquer momento em que você reimplantar o espaço de trabalho do MED-V para a sua empresa, a configuração deve ser executada novamente, e todos os dados salvos na máquina virtual serão perdidos.

     

## Tópicos relacionados


[Como testar o redirecionamento da URL](how-to-test-url-redirection.md)

[Gerenciamento de aplicativos implantados em espaços de trabalho da MED-V](managing-applications-deployed-to-med-v-workspaces.md)

[Criar um pacote de espaço de trabalho da MED-V](create-a-med-v-workspace-package.md)

 

 





