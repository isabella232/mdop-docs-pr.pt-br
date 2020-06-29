---
title: Gerenciamento de configurações do espaço de trabalho da MED-V usando um WMI
description: Gerenciamento de configurações do espaço de trabalho da MED-V usando um WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799811"
---
# Gerenciamento de configurações do espaço de trabalho da MED-V usando um WMI


Você pode usar a instrumentação de gerenciamento do Windows (WMI) na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 para gerenciar suas configurações atuais.

## Para gerenciar as configurações do espaço de trabalho do MED-V com um WMI


Uma ferramenta de navegação WMI permite que você exiba e edite as configurações em um espaço de trabalho do MED-V. O provedor WMI é implementado usando a estrutura de extensão do provedor WMI do Microsoft .NET Framework 3,5.

O provedor WMI é implementado no namespace **root\\microsoft\\medv** e implementa a **configuração**de classe. A **configuração** de classe contém propriedades que correspondem às configurações no registro do sistema sob a chave HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv do registro.

**Cuidado**  As ferramentas de navegação WMI podem ser usadas para excluir ou modificar classes e instâncias. Excluir ou modificar determinadas classes e instâncias pode resultar na perda de dados valiosos e fazer com que o MED-V funcione de forma imprevisível.

 

Você pode usar sua ferramenta de navegação WMI preferida para exibir e editar as configurações de configuração do MED-V seguindo estas etapas.

1.  Abra sua ferramenta de navegação WMI preferida com permissões de administrador.

2.  Conecte-se ao namespace **root\\microsoft\\medv**.

3.  Enumere as instâncias para se conectar à instância em execução. Você deseja se conectar à instância da **configuração**de classe.

    Uma janela do **Editor de objeto** é aberta. As configurações de configuração do MED-V são listadas como **Propriedades**.

Execute as etapas a seguir para editar uma configuração de configuração do MED-V no WMI.

1.  Na lista de **Propriedades** na janela do **Editor de objetos** , clique duas vezes no nome da configuração que você deseja editar. Por exemplo, para editar informações sobre o redirecionamento de URL do MED-V, clique duas vezes na propriedade **UxRedirectUrls**.

    Uma janela do **Editor de propriedades** é aberta.

2.  Edite o valor para atualizar as informações de configuração. Por exemplo, para editar informações sobre o redirecionamento de URL do MED-V, adicione ou remova um endereço da Web na lista.

3.  Salve as configurações de propriedades atualizadas.

Depois de terminar de exibir ou editar as configurações de configuração do MED-V, feche a ferramenta de navegação WMI.

**Importante**  Em alguns casos, é necessária uma reinicialização do espaço de trabalho do MED-V para que as alterações nas configurações de configuração do MED-V entrem em vigor.

 

O código a seguir mostra o arquivo MOF (Managed Object Format) que define a classe **Setting** .

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

A classe **Setting** é herdada da classe **ConfigValueProvider** . O código a seguir mostra o arquivo MOF (Managed Object Format) que define a classe **ConfigValueProvider** .

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## Tópicos relacionados


[Gerenciamento de configurações do espaço de trabalho da MED-V](managing-med-v-workspace-configuration-settings.md)

[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)

 

 





