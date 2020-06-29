---
title: Criar ou editar o arquivo SMS \ _def. mof
description: Criar ou editar o arquivo SMS \ _def. mof
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799224"
---
# <span data-ttu-id="1b019-103">Criar ou editar o arquivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="1b019-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="1b019-104">Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa criar ou editar o arquivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="1b019-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="1b019-105">Se estiver usando o SystemCenter2012 ConfigurationManager, você deve criar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b019-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="1b019-106">Crie o arquivo no site de camada superior.</span><span class="sxs-lookup"><span data-stu-id="1b019-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="1b019-107">As alterações serão replicadas para os outros sites em sua infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1b019-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="1b019-108">No Configuration Manager 2007, o arquivo já existe, portanto você só precisa editá-lo.</span><span class="sxs-lookup"><span data-stu-id="1b019-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="1b019-109">Não substitua o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="1b019-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="1b019-110">Nas seções a seguir, preencha as instruções correspondentes à versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="1b019-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="1b019-111">Para criar o arquivo SMS \ _def. MOF para SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="1b019-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="1b019-112">No servidor do Configuration Manager, navegue até o local onde você precisa criar o arquivo SMS \ _def. MOF, por exemplo, a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b019-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="1b019-113">Crie um arquivo de texto chamado **SMS \ _def. mof** e copie o código a seguir para popular o arquivo com as seguintes classes Sms \ _def. mof MBAM:</span><span class="sxs-lookup"><span data-stu-id="1b019-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="1b019-114">Importe o arquivo **SMS \ _def. mof** fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b019-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="1b019-115">Abra o **console SystemCenter2012 ConfigurationManager** e selecione a guia **Administração** .</span><span class="sxs-lookup"><span data-stu-id="1b019-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="1b019-116">Na guia **Administração** , selecione **configurações do cliente**.</span><span class="sxs-lookup"><span data-stu-id="1b019-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="1b019-117">Clique com o botão direito do mouse em **configurações padrão do cliente**e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="1b019-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="1b019-118">Na janela **configurações padrão** , selecione **inventário de hardware**.</span><span class="sxs-lookup"><span data-stu-id="1b019-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="1b019-119">Clique em **definir classes**e, em seguida, clique em **importar**.</span><span class="sxs-lookup"><span data-stu-id="1b019-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="1b019-120">No navegador que é aberto, selecione seu arquivo **. mof** e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="1b019-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="1b019-121">A janela de **Resumo da importação** será aberta.</span><span class="sxs-lookup"><span data-stu-id="1b019-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="1b019-122">Na janela **Resumo da importação** , verifique se a opção para importar classes de inventário de hardware e configurações de classe está selecionada e clique em **importar**.</span><span class="sxs-lookup"><span data-stu-id="1b019-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="1b019-123">Na janela **classes de inventário de hardware** e na janela **configurações padrão** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b019-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="1b019-124">Habilite a classe **Win32 \ _Tpm** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1b019-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="1b019-125">Abra o **console SystemCenter2012 ConfigurationManager** e selecione a guia **Administração** .</span><span class="sxs-lookup"><span data-stu-id="1b019-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="1b019-126">Na guia **Administração** , selecione **configurações do cliente**.</span><span class="sxs-lookup"><span data-stu-id="1b019-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="1b019-127">Clique com o botão direito do mouse em **configurações padrão do cliente**e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="1b019-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="1b019-128">Na janela **configurações padrão** , selecione **inventário de hardware**.</span><span class="sxs-lookup"><span data-stu-id="1b019-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="1b019-129">Clique em **definir classes**.</span><span class="sxs-lookup"><span data-stu-id="1b019-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="1b019-130">Na janela principal, role para baixo e selecione a classe **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="1b019-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="1b019-131">Em **TPM**, verifique se a propriedade **SpecVersion** está selecionada.</span><span class="sxs-lookup"><span data-stu-id="1b019-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="1b019-132">Na janela **classes de inventário de hardware** e na janela **configurações padrão** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b019-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="1b019-133">Para editar o arquivo SMS \ _def. mof do Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="1b019-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="1b019-134">No servidor do Configuration Manager, navegue até o local do arquivo **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="1b019-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="1b019-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="1b019-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="1b019-136">Em uma instalação padrão, o local de instalação é% systemdrive% \\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1b019-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="1b019-137">Copie o código a seguir e, em seguida, adicione-o ao arquivo **SMS \ _def. mof** para adicionar as seguintes classes MBAM necessárias ao arquivo:</span><span class="sxs-lookup"><span data-stu-id="1b019-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="1b019-138">Modifique a classe **Win32 \ _Tpm** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1b019-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="1b019-139">Defina **SMS \ _REPORT** como **verdadeiro** nos atributos de classe.</span><span class="sxs-lookup"><span data-stu-id="1b019-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="1b019-140">Defina **SMS \ _REPORT** como **true** no atributo da propriedade **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="1b019-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="1b019-141">**Tem uma sugestão para o MBAM**?</span><span class="sxs-lookup"><span data-stu-id="1b019-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="1b019-142">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1b019-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="1b019-143">**Tem um problema com o MBAM**?</span><span class="sxs-lookup"><span data-stu-id="1b019-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="1b019-144">Use o [Fórum do TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1b019-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="1b019-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b019-145">Related topics</span></span>


[<span data-ttu-id="1b019-146">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1b019-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="1b019-147">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="1b019-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="1b019-148">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1b019-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="1b019-149">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="1b019-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1b019-150">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1b019-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1b019-151">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1b019-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




