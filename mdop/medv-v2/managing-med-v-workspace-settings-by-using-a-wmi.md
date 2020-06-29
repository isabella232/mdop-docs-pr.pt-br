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
# <span data-ttu-id="9f700-103">Gerenciamento de configurações do espaço de trabalho da MED-V usando um WMI</span><span class="sxs-lookup"><span data-stu-id="9f700-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="9f700-104">Você pode usar a instrumentação de gerenciamento do Windows (WMI) na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 para gerenciar suas configurações atuais.</span><span class="sxs-lookup"><span data-stu-id="9f700-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="9f700-105">Para gerenciar as configurações do espaço de trabalho do MED-V com um WMI</span><span class="sxs-lookup"><span data-stu-id="9f700-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="9f700-106">Uma ferramenta de navegação WMI permite que você exiba e edite as configurações em um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f700-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="9f700-107">O provedor WMI é implementado usando a estrutura de extensão do provedor WMI do Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="9f700-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="9f700-108">O provedor WMI é implementado no namespace **root\\microsoft\\medv** e implementa a **configuração**de classe.</span><span class="sxs-lookup"><span data-stu-id="9f700-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="9f700-109">A **configuração** de classe contém propriedades que correspondem às configurações no registro do sistema sob a chave HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv do registro.</span><span class="sxs-lookup"><span data-stu-id="9f700-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="9f700-110">**Cuidado**  As ferramentas de navegação WMI podem ser usadas para excluir ou modificar classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="9f700-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="9f700-111">Excluir ou modificar determinadas classes e instâncias pode resultar na perda de dados valiosos e fazer com que o MED-V funcione de forma imprevisível.</span><span class="sxs-lookup"><span data-stu-id="9f700-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="9f700-112">Você pode usar sua ferramenta de navegação WMI preferida para exibir e editar as configurações de configuração do MED-V seguindo estas etapas.</span><span class="sxs-lookup"><span data-stu-id="9f700-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="9f700-113">Abra sua ferramenta de navegação WMI preferida com permissões de administrador.</span><span class="sxs-lookup"><span data-stu-id="9f700-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="9f700-114">Conecte-se ao namespace **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="9f700-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="9f700-115">Enumere as instâncias para se conectar à instância em execução.</span><span class="sxs-lookup"><span data-stu-id="9f700-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="9f700-116">Você deseja se conectar à instância da **configuração**de classe.</span><span class="sxs-lookup"><span data-stu-id="9f700-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="9f700-117">Uma janela do **Editor de objeto** é aberta.</span><span class="sxs-lookup"><span data-stu-id="9f700-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="9f700-118">As configurações de configuração do MED-V são listadas como **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="9f700-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="9f700-119">Execute as etapas a seguir para editar uma configuração de configuração do MED-V no WMI.</span><span class="sxs-lookup"><span data-stu-id="9f700-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="9f700-120">Na lista de **Propriedades** na janela do **Editor de objetos** , clique duas vezes no nome da configuração que você deseja editar.</span><span class="sxs-lookup"><span data-stu-id="9f700-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="9f700-121">Por exemplo, para editar informações sobre o redirecionamento de URL do MED-V, clique duas vezes na propriedade **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="9f700-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="9f700-122">Uma janela do **Editor de propriedades** é aberta.</span><span class="sxs-lookup"><span data-stu-id="9f700-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="9f700-123">Edite o valor para atualizar as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="9f700-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="9f700-124">Por exemplo, para editar informações sobre o redirecionamento de URL do MED-V, adicione ou remova um endereço da Web na lista.</span><span class="sxs-lookup"><span data-stu-id="9f700-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="9f700-125">Salve as configurações de propriedades atualizadas.</span><span class="sxs-lookup"><span data-stu-id="9f700-125">Save the updated property settings.</span></span>

<span data-ttu-id="9f700-126">Depois de terminar de exibir ou editar as configurações de configuração do MED-V, feche a ferramenta de navegação WMI.</span><span class="sxs-lookup"><span data-stu-id="9f700-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="9f700-127">**Importante**  Em alguns casos, é necessária uma reinicialização do espaço de trabalho do MED-V para que as alterações nas configurações de configuração do MED-V entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="9f700-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="9f700-128">O código a seguir mostra o arquivo MOF (Managed Object Format) que define a classe **Setting** .</span><span class="sxs-lookup"><span data-stu-id="9f700-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="9f700-129">A classe **Setting** é herdada da classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="9f700-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="9f700-130">O código a seguir mostra o arquivo MOF (Managed Object Format) que define a classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="9f700-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

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

## <span data-ttu-id="9f700-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f700-131">Related topics</span></span>


[<span data-ttu-id="9f700-132">Gerenciamento de configurações do espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="9f700-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="9f700-133">Gerenciar configurações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="9f700-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





