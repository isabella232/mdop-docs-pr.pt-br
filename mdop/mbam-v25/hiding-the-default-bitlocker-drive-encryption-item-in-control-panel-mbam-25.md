---
title: Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle
description: Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799204"
---
# Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle


Este tópico descreve como ocultar o item do painel de controle de **criptografia de unidade de disco BitLocker** , que é exibido por padrão no painel de controle como parte do sistema operacional Windows.

**Observação**  O Microsoft BitLocker Administration and Monitoring (MBAM) cria um item de painel de controle adicional personalizado, chamado **Opções de criptografia do BitLocker**, que permite que os usuários finais gerenciem o PIN e a senha, ativem o BitLocker para uma unidade e marquem a criptografia.

 

Consulte [compreendendo as opções de criptografia BitLocker e os itens de criptografia de unidade de disco BitLocker no painel de controle](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) para ler sobre:

-   Diferenças entre o MBAM e os itens padrão do painel de controle

-   Menu de atalho **gerenciar o BitLocker** que aparece quando você clica com o botão direito do mouse em uma unidade no Windows Explorer

**Importante**  Não altere as configurações de política de grupo no nó **criptografia de unidade de disco BitLocker** . Se fizer isso, o MBAM não funcionará corretamente. Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.

 

**Para ocultar o item de criptografia de unidade de disco BitLocker padrão no painel de controle**

1.  No console de gerenciamento de política de grupo (GPMC) ou no gerenciamento avançado de política de grupo, navegue até políticas de **configuração do usuário** &gt; **Policies** &gt; painel de controle de **modelos administrativos** &gt; **Control Panel**.

2.  No painel **detalhes** , clique duas vezes em **ocultar itens do painel de controle especificado**e, em seguida, clique em **habilitado**.

3.  Clique em **Mostrar**, clique em **Adicionar**e, em seguida, digite **Microsoft. BitLockerDriveEncryption**.



## Tópicos relacionados


[Noções básicas sobre as opções de criptografia BitLocker e itens de Criptografia de Unidade de Disco BitLocker no Painel de Controle](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Implantando objetos de Política de Grupo do MBAM 2.5](deploying-mbam-25-group-policy-objects.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





