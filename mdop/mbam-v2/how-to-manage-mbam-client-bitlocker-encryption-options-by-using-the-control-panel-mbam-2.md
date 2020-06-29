---
title: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
description: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799606"
---
# Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle


Um aplicativo do painel de controle de administração e monitoramento do Microsoft BitLocker (MBAM), chamado de opções de criptografia do BitLocker, estará disponível em **sistema e segurança** quando o cliente de administração e monitoramento do Microsoft BitLocker estiver instalado. Este painel de controle do MBAM personalizado é um painel de controle adicional. Ele não substitui o painel de controle padrão do Windows BitLocker. O painel de controle do MBAM pode ser usado para desbloquear unidades fixas e removíveis criptografadas e também gerenciar seu PIN ou senha. Para obter mais informações sobre como habilitar o painel de controle do MBAM, consulte [como ocultar a criptografia do BitLocker padrão no painel de controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).

**Para usar o painel de controle do cliente MBAM**

1.  Para abrir as opções de criptografia do BitLocker, clique em **Iniciar** e, em seguida, selecione **painel de controle**. Quando o **painel de controle** for aberto, selecione **sistema e segurança**.

2.  Clique duas vezes em **Opções de criptografia do BitLocker** para abrir o painel de controle MBAM personalizado. Você verá uma lista de todas as unidades de disco rígido no computador e seu status de criptografia, além de uma opção para gerenciar seu PIN ou senhas.

    A lista de unidades de disco rígido no computador pode ser usada para verificar o status de criptografia, desbloquear uma unidade ou solicitar uma isenção de proteção do BitLocker se as políticas de isenção de usuário e computador tiverem sido implantadas.

    O painel de controle opções de criptografia do BitLocker também permite que os usuários que não são administradores gerenciem seu PIN ou senhas. Ao selecionar **gerenciar PIN**, os usuários são solicitados a digitar um PIN atual e um novo PIN (além de confirmar o novo PIN). Selecionar **Atualizar PIN** irá redefinir o pino para o novo que os usuários selecionaram.

    Para gerenciar sua senha, selecione **desbloquear unidade** e insira sua senha atual. Assim que a unidade for desbloqueada, selecione **Redefinir senha** para alterar sua senha atual.

## Tópicos relacionados


[Administrando os Recursos do MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





