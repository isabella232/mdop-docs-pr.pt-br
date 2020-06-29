---
title: Como gerenciar a compatibilidade de hardware
description: Como gerenciar a compatibilidade de hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796136"
---
# Como gerenciar a compatibilidade de hardware


O monitoramento e a administração do Microsoft BitLocker (MBAM) podem coletar informações sobre o fabricante e o modelo de computadores cliente após a implantação da política de grupo permitir verificação de compatibilidade de hardware. Se você configurar essa política, o agente MBAM relata as informações do modelo e do modelo do computador ao servidor MBAM quando o cliente MBAM é implantado em um computador cliente.

O recurso de compatibilidade de hardware é útil quando sua organização tem hardware de computador ou computadores mais antigos que não dão suporte a chips do Trusted Platform Module (TPM). Nesses casos, você pode usar o recurso de compatibilidade de hardware para garantir que a criptografia do BitLocker seja aplicada somente a modelos de computador que o dão suporte a ele. Se todos os computadores da sua organização forem compatíveis com o BitLocker, você não precisará usar o recurso de compatibilidade de hardware.

**Observação**  Por padrão, o recurso de compatibilidade de hardware do MBAM não está habilitado. Para habilitá-lo, selecione o recurso de **compatibilidade de hardware** no recurso do **servidor de administração e monitoramento** durante a instalação. Para obter mais informações sobre como configurar e configurar a compatibilidade de hardware, consulte [implantando a infraestrutura de servidor do MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

O recurso de compatibilidade de hardware funciona da seguinte maneira.

****

1.  O agente cliente do MBAM descobre informações básicas do computador, como fabricante, modelo, fabricante do BIOS, versão do BIOS, criador do TPM e versão do TPM e, em seguida, passa essas informações para o servidor MBAM.

2.  O MBAM Server gera uma lista de componentes e modelos de computador cliente para permitir que você Diferencie entre aqueles que podem ou não dar suporte ao BitLocker

3.  Os agentes do cliente MBAM implantados na empresa atualizam automaticamente essa lista com todos os novos computadores e modelos que são descobertos com um estado **desconhecido**. Em seguida, um administrador pode usar o site de administração do MBAM para alterar as entradas de lista para especificar uma marca e um modelo de computador específico como **compatível** ou **incompatível**.

4.  Antes de o agente do cliente MBAM começar a criptografar uma unidade, o agente verifica primeiro a compatibilidade de criptografia do BitLocker do hardware em que ele está sendo executado.

    -   Se o hardware estiver marcado como compatível, o processo de criptografia do BitLocker será iniciado. O MBAM também verificará novamente o status de compatibilidade de hardware do computador uma vez por dia.

    -   Se o hardware estiver marcado como incompatível, o agente registrará um evento e passará um estado de "hardware isento" como parte do relatório de conformidade. O agente verifica a cada sete dias para ver se o estado mudou para "compatível".

    -   Se o hardware estiver marcado como desconhecido, o processo de criptografia do BitLocker não será iniciado. O agente cliente do MBAM verificará novamente o status de compatibilidade de hardware do computador uma vez por dia.

**Aviso**  Se o agente cliente do MBAM tentar criptografar um computador que não dá suporte à criptografia de unidade de disco BitLocker, há uma possibilidade de que o computador seja corrompido. Verifique se o recurso de compatibilidade de hardware está configurado corretamente quando a sua organização tiver hardware mais antigo que não dê suporte ao BitLocker.

 

**Para gerenciar a compatibilidade de hardware**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento do Microsoft BitLocker. Selecione **hardware** na barra de menus à esquerda.

2.  No painel direito, clique em **pesquisa avançada**e, em seguida, em filtrar para exibir uma lista de todos os modelos de computador que têm um status de **funcionalidade** **desconhecido**. Uma lista de modelos de computador que correspondem aos critérios de pesquisa será exibida. Os administradores podem adicionar, editar ou remover novos tipos de computador desta página.

3.  Examine cada configuração de hardware desconhecida para determinar se a configuração deve ser definida como **compatível** ou **incompatível**.

4.  Selecione uma ou mais linhas e, em seguida, clique em **definir como compatível** ou **definir incompatível** para definir a compatibilidade do BitLocker, conforme apropriado, para os modelos de computador selecionados. Se definido como **compatível**, o BitLocker tenta impor uma política de criptografia de unidade em computadores que correspondam ao modelo com suporte. Se definido como **incompatível**, o BitLocker não impedirá a política de criptografia de unidade nesses computadores.

    **Observação**  Depois de definir um modelo de computador como compatível, ele pode levar mais de vinte a quatro horas para o cliente MBAM iniciar a criptografia do BitLocker nos computadores que correspondem ao modelo de hardware.

     

5.  Os administradores devem monitorar regularmente a lista de compatibilidade de hardware para examinar os novos modelos descobertos pelo agente do MBAM e, em seguida, atualizar sua configuração de compatibilidade para **compatível** ou **incompatível** conforme apropriado.

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)

 

 





