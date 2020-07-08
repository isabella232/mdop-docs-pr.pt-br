---
title: Visão geral do Gerenciamento Avançado de Política de Grupo
description: Visão geral do Gerenciamento Avançado de Política de Grupo
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799082"
---
# Visão geral do Gerenciamento Avançado de Política de Grupo


Você pode usar o gerenciamento de política de grupo avançado (AGPM) para estender os recursos do console de gerenciamento de política de grupo (GPMC) para fornecer controle de alterações abrangente e gerenciamento aprimorado para objetos de política de grupo (GPOs).

## Desenvolvimento de objetos de política de grupo com controle de alterações


Com o AGPM, você pode armazenar uma cópia de cada GPO em um arquivo morto central para que os administradores de política de grupo possam exibir e alterá-lo offline sem afetar imediatamente a versão implantada do GPO. Além disso, o AGPM armazena uma cópia de cada versão de cada GPO controlado no arquivo para que você possa reverter para uma versão anterior, se necessário.

Os termos "check-in" e "check-out" são usados apenas como em uma biblioteca (ou em aplicativos que fornecem controle de alterações, controle de versão ou controle de origem para o desenvolvimento de programação). Para usar um livro que esteja em uma biblioteca, verifique-o na biblioteca. Ninguém mais pode usá-lo enquanto você estiver com check-out. Quando terminar o livro, verifique-o novamente na biblioteca para que outras pessoas possam usá-lo.

Para usar esses recursos de controle de GPO, clique em um nó de controle de alterações no editor de gerenciamento de política de grupo. O nó de controle de alterações só aparecerá se você tiver instalado o cliente do AGPM.

Ao desenvolver GPOs usando o AGPM:

1.  Crie um novo GPO controlado ou controle um GPO previamente controlado.

2.  Confira o GPO para que você e somente você possa alterá-lo.

3.  Edite o GPO.

4.  Faça o check-in do GPO editado para que outras pessoas possam alterá-lo, ou para que ele possa ser implantado.

5.  Revise as alterações.

6.  Implante o GPO no ambiente de produção.

## Delegação baseada em função


O AGPM oferece delegação completa e fácil de usar com base em funções para o gerenciamento do acesso a GPOs no arquivo. As permissões no nível do domínio permitem que os administradores do AGPM forneçam acesso a domínios individuais sem fornecer acesso a outros domínios. A delegação baseada em GPO permite que os administradores do AGPM forneçam acesso a GPOs específicos sem fornecer acesso em todo o domínio.

No AGPM, há funções especificamente definidas: administrador do AGPM (controle total), Aprovador, editor e revisor. A função de administrador do AGPM inclui as permissões para todas as outras funções. Por padrão, somente os aprovadores têm a capacidade de implantar GPOs no ambiente de produção de um domínio, protegendo o ambiente contra erros de editores menos experientes. Além disso, por padrão, todas as funções incluem a função de revisor e, portanto, a capacidade de visualizar as configurações de GPO em relatórios. No entanto, o AGPM fornece um administrador do AGPM com a flexibilidade de personalizar o acesso ao GPO para atender às necessidades da sua organização.

## Delegação em um ambiente de administrador de política de grupo múltiplo


Em um ambiente onde várias pessoas alteram os GPOs, um administrador do AGPM delega a permissão para editores, Aprovadores e revisores, como grupos ou indivíduos. Para um processo de desenvolvimento de GPO típico para um editor e um aprovador, consulte [lista de verificação: criar, editar e implantar um GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).

### Referências adicionais

-   [Gerenciamento Avançado de Política de Grupo 4.0](advanced-group-policy-management-40.md)

 

 





