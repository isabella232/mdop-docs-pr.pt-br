---
title: Sobre licenciamento de aplicativos
description: Sobre licenciamento de aplicativos
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797657"
---
# Sobre licenciamento de aplicativos


Você pode gerenciar licenças de aplicativos diretamente do console de gerenciamento do servidor do Application Virtualization.

## Tipos de licença


No momento, o sistema do System Center Application Virtualization oferece suporte aos seguintes tipos de licença:

-   **Licença ilimitada**— permite o acesso ao aplicativo por qualquer número de usuários simultâneos. Esse método de licenciamento é apropriado quando você deseja associar uma licença de toda a empresa a um aplicativo.

-   **Licença simultânea**— permite que você defina o número máximo de usuários simultâneos que têm permissão para usar o aplicativo.

-   **Licença nomeada**— permite atribuir uma licença a um usuário individual. Uma licença nomeada pode ser usada para garantir que um usuário em particular sempre será capaz de executar o aplicativo.

Você pode combinar licenças simultâneas e nomeadas para o mesmo aplicativo.

O licenciamento está desabilitado por padrão, mas você pode habilitá-lo na guia **pipeline do provedor** da caixa de diálogo **Propriedades do provedor** . Para obter detalhes sobre como habilitar e desabilitar o licenciamento, consulte [como configurar ou desabilitar o licenciamento de aplicativos](how-to-set-up-or-disable-application-licensing.md).

## Políticas de provedor


Políticas de provedor foram desenvolvidas para o modelo de provedor de serviços de aplicativo (ASP). Nesse modelo, um único ASP pode hospedar um sistema de virtualização de aplicativo único para vários clientes, em que cada cliente precisa permanecer isolado. Os clientes podem ter requisitos drasticamente diferentes — por exemplo, um cliente pode exigir autenticação enquanto outro não. Você pode usar políticas de provedor para associar permissões a clientes para que somente os usuários aprovados possam acessar cada aplicativo virtual ou pacote de aplicativo virtual.

Para o cliente empresarial, você pode usar esse recurso quando tiver requisitos de licenciamento estritos para um ou mais aplicativos. Nessa situação, o componente de licenciamento está desabilitado na guia **pipeline do provedor** da caixa de diálogo **Propriedades do provedor** .

A guia **pipeline do provedor** também tem caixas de seleção para habilitar autenticação, autorização (**reforçar as configurações de permissão de acesso**) e medição (**registrar informações de uso**). Se a sua configuração tiver requisitos especiais, você poderá escrever seus próprios componentes de pipeline e adicioná-los ao sistema clicando no botão **avançado** .

## Autoridades da conta


A autoridade da conta é o domínio no qual o servidor do Application Virtualization está instalado. Ao passar pela instalação do servidor, você será solicitado a fornecer um nome de domínio; o domínio no qual o computador está instalado é detectado e usado por padrão. Quando os usuários tentam entrar no sistema, eles são solicitados a fornecer suas credenciais antes de poderem acessar o domínio.

O sistema de virtualização de aplicativos dá suporte a vários domínios. Você pode conceder acesso a aplicativos a grupos de usuários em outros domínios se uma relação de confiança for estabelecida entre domínios. Os usuários devem fornecer credenciais que são reconhecidas por cada domínio.

No console de gerenciamento do servidor do Application Virtualization, você pode alterar o domínio primário (autoridade da conta) e as credenciais que são usadas para acessá-lo.

## Autenticação


Autenticação é o mecanismo usado para confirmar a identidade do usuário. Qualquer usuário com um nome de usuário e senha reconhecidos tem acesso.

No sistema de virtualização de aplicativos, você pode habilitar ou desabilitar a autenticação por meio de uma caixa de seleção na guia **pipeline do provedor** . Por padrão, a autenticação do Windows está habilitada.

## Autorização


Autorização é o processo usado para confirmar a identidade do usuário. Depois de confirmar a identidade do usuário, o sistema determina se o usuário recebeu acesso ao sistema e para quais aplicativos o usuário recebeu acesso. O console de gerenciamento de servidor do Application Virtualization tem uma caixa de seleção **impor configurações de permissão de acesso** na guia **pipeline do provedor** para habilitar ou desabilitar a autorização.

No sistema de virtualização de aplicativos, o acesso é concedido apenas a um grupo de usuários, e não a usuários individuais.

## Tópicos relacionados


[Como gerenciar licenças de aplicativos no Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Como configurar ou desabilitar o licenciamento de aplicativo](how-to-set-up-or-disable-application-licensing.md)

[Server Management Console: nó Políticas de Provedor](server-management-console-provider-policies-node.md)

 

 





