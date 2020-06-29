---
title: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
description: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796129"
---
# Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle


Um aplicativo do painel de controle de administração e monitoramento do Microsoft BitLocker (MBAM), chamado de opções de criptografia do BitLocker, estará disponível em **sistema e segurança** quando o cliente MBAM estiver instalado. Este painel de controle MBAM personalizado substitui o painel de controle padrão do Windows BitLocker. O painel de controle do MBAM permite desbloquear unidades criptografadas (fixas e removíveis) e também ajuda você a gerenciar seu PIN ou senha. Para obter mais informações sobre como habilitar o painel de controle do MBAM, consulte [como ocultar a criptografia do BitLocker padrão no painel de controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).

**Observação**  Para o cliente BitLocker, o administrador e os arquivos de log operacional estão localizados no Visualizador de eventos, em **logs de aplicativos e serviços**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.

 

**Para usar o painel de controle do cliente MBAM**

1.  Para abrir as opções de criptografia do BitLocker, clique em **Iniciar**e, em seguida, selecione **painel de controle**. Quando o **painel de controle** for aberto, selecione **sistema e segurança**.

2.  Clique duas vezes em **Opções de criptografia do BitLocker** para abrir o painel de controle MBAM personalizado. Você verá uma lista de todas as unidades de disco rígido no computador e seu status de criptografia. Você também poderá ver uma opção para gerenciar seu PIN ou senhas.

3.  Use a lista de unidades de disco rígido no computador para verificar o status de criptografia, desbloquear uma unidade ou solicitar uma isenção de proteção do BitLocker se as políticas de isenção de usuário e computador tiverem sido implantadas.

4.  Usuários que não são administradores podem usar o painel de controle opções de criptografia BitLocker para gerenciar PINs ou senhas. Um usuário pode selecionar **gerenciar PIN** e, em seguida, inserir um PIN atual e um novo PIN. Os usuários também podem confirmar o novo PIN. A função **Atualizar PIN** irá redefinir o pino para o novo que o usuário selecionar.

5.  Para gerenciar sua senha, selecione **desbloquear unidade** e insira sua senha atual. Assim que a unidade for desbloqueada, selecione **Redefinir senha** para alterar sua senha atual.

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)

 

 





