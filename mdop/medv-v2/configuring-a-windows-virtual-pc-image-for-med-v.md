---
title: Como configurar uma imagem do Windows Virtual PC para a MED-V
description: Como configurar uma imagem do Windows Virtual PC para a MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799948"
---
# <span data-ttu-id="adf28-103">Como configurar uma imagem do Windows Virtual PC para a MED-V</span><span class="sxs-lookup"><span data-stu-id="adf28-103">Configuring a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="adf28-104">Depois de instalar tudo o que você deseja incluir em sua imagem do MED-V, você pode configurar a imagem para usar na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="adf28-104">After you have installed everything that you want to include in your MED-V image, you can configure the image for use in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="adf28-105">Os tópicos desta seção fornecem orientação para configurar sua imagem do MED-V para ser executada primeiro antes de criar seu pacote de espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="adf28-105">The topics in this section provide guidance for configuring your MED-V image to run first time setup before you create your MED-V workspace package.</span></span>

<span data-ttu-id="adf28-106">Primeira vez que o programa de instalação prepara o espaço de trabalho do MED-V para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="adf28-106">First time setup prepares the MED-V workspace for an end user.</span></span> <span data-ttu-id="adf28-107">O processo cria uma máquina virtual a partir da imagem empacotada no espaço de trabalho do MED-V e executa a mini-configuração do Windows na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="adf28-107">The process creates a virtual machine from the image packaged in the MED-V workspace and then runs Windows Mini-Setup on the virtual machine.</span></span> <span data-ttu-id="adf28-108">Isso inclui a execução de ambos os scripts de instalação personalizados e o aplicativo de conclusão configuração da primeira vez, FtsCompletion.exe.</span><span class="sxs-lookup"><span data-stu-id="adf28-108">This includes the running of both custom setup scripts and the first time setup completion application, FtsCompletion.exe.</span></span>

<span data-ttu-id="adf28-109">Siga estas etapas para configurar sua imagem do MED-V para executar a configuração do primeiro horário:</span><span class="sxs-lookup"><span data-stu-id="adf28-109">Follow these steps to configure your MED-V image for running first time setup:</span></span>

1. <span data-ttu-id="adf28-110">Como opção, você pode compactar o disco rígido virtual (VHD) para recuperar espaço em disco vazio e reduzir o tamanho do VHD antes de prosseguir com a configuração da imagem do PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="adf28-110">As an option, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you continue with configuring the Windows Virtual PC image.</span></span> <span data-ttu-id="adf28-111">Para obter mais informações, consulte [compactando o disco rígido virtual do MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="adf28-111">For more information, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

2. <span data-ttu-id="adf28-112">Personalize o processo de configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="adf28-112">Customize the virtual machine setup process.</span></span>

3. <span data-ttu-id="adf28-113">Lacre a imagem do MED-V usando Sysprep.</span><span class="sxs-lookup"><span data-stu-id="adf28-113">Seal the MED-V image by using Sysprep.</span></span>

   **<span data-ttu-id="adf28-114">Personalizando o processo de configuração da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="adf28-114">Customizing the Virtual Machine Setup Process</span></span>**

4. <span data-ttu-id="adf28-115">Como parte da preparação da imagem para usar com o MED-V, você pode definir várias configurações na máquina virtual, como especificar as configurações para executar o Windows Update.</span><span class="sxs-lookup"><span data-stu-id="adf28-115">As part of preparing your image for use with MED-V, you can configure various settings on the virtual machine, such as specifying the settings for running Windows Update.</span></span> <span data-ttu-id="adf28-116">Especifique todas as configurações da máquina virtual necessárias antes de criar o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="adf28-116">Specify all the necessary virtual machine settings before you create the MED-V workspace package.</span></span>

5. <span data-ttu-id="adf28-117">Antes de criar o pacote do espaço de trabalho do MED-V, recomendamos que você desabilite os pontos de restauração na máquina virtual para impedir que o disco diferencial aumente não associado.</span><span class="sxs-lookup"><span data-stu-id="adf28-117">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="adf28-118">Para obter mais informações, consulte [como desativar e ativar a restauração do sistema no Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="adf28-118">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

   **<span data-ttu-id="adf28-119">Observação</span><span class="sxs-lookup"><span data-stu-id="adf28-119">Note</span></span>**  
   <span data-ttu-id="adf28-120">Você pode configurar seu arquivo Sysprep. inf para desabilitar pontos de restauração quando a configuração da primeira vez for executada.</span><span class="sxs-lookup"><span data-stu-id="adf28-120">You can set up your Sysprep.inf file to disable restore points when first time setup is run.</span></span> <span data-ttu-id="adf28-121">Para obter um exemplo de como definir essa chave GuiRunOnce, consulte o arquivo Sysprep. inf de exemplo mais adiante nesta seção.</span><span class="sxs-lookup"><span data-stu-id="adf28-121">For an example of setting this GuiRunOnce key, see the sample Sysprep.inf file later in this section.</span></span>



6. <span data-ttu-id="adf28-122">Configure o processo de configuração para executar a mini-instalação em vez da tela de boas-vindas padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="adf28-122">Configure the setup process to run Mini-Setup instead of the default Windows Welcome.</span></span> <span data-ttu-id="adf28-123">Você deve executar a ferramenta Sysprep usando a opção **-Mini** , ou marcar a caixa de seleção **MiniSetup** na interface gráfica do usuário.</span><span class="sxs-lookup"><span data-stu-id="adf28-123">You must either run the Sysprep tool by using the **-mini** switch, or select the **MiniSetup** check box in the graphical user interface.</span></span> <span data-ttu-id="adf28-124">Para obter mais informações, consulte [como lacrar a imagem com Sysprep](#bkmk-seal).</span><span class="sxs-lookup"><span data-stu-id="adf28-124">For more information, see [How to Seal the Image with Sysprep](#bkmk-seal).</span></span>

   **<span data-ttu-id="adf28-125">Chamando o arquivo de conclusão de configuração da primeira vez</span><span class="sxs-lookup"><span data-stu-id="adf28-125">Calling the First time setup Completion File</span></span>**

   1.  <span data-ttu-id="adf28-126">Um executável chamado FtsCompletion.exe está incluído como parte da instalação do agente de convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="adf28-126">An executable called FtsCompletion.exe is included as part of the installation of the MED-V Guest Agent.</span></span> <span data-ttu-id="adf28-127">Por padrão, ele está localizado na unidade do sistema da sua imagem do MED-V em **arquivos de programas – virtualização de área de trabalho do Microsoft Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="adf28-127">By default, it is located in the system drive of your MED-V image under **Program Files – Microsoft Enterprise Desktop Virtualization**.</span></span>

       **<span data-ttu-id="adf28-128">Importante</span><span class="sxs-lookup"><span data-stu-id="adf28-128">Important</span></span>**  
       <span data-ttu-id="adf28-129">Como a etapa final do processo de configuração inicial, você deve executar este programa executável.</span><span class="sxs-lookup"><span data-stu-id="adf28-129">As the final step in the first time setup process, you must run this executable program.</span></span> <span data-ttu-id="adf28-130">O usuário para o qual o programa executável está sendo chamado deve ser um membro do grupo de Administradores local do convidado.</span><span class="sxs-lookup"><span data-stu-id="adf28-130">The user for whom the executable program is being called must be a member of the guest’s local administrator group.</span></span>



   2.  <span data-ttu-id="adf28-131">Você pode decidir como deseja chamar este programa executável, por exemplo, por meio de um script que é implantado com o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="adf28-131">You can decide how you want to call this executable program, for example, through a script that is deployed with the MED-V workspace.</span></span> <span data-ttu-id="adf28-132">Você pode chamar esse executável como a última linha do seu arquivo Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="adf28-132">You can call this executable as the last line of your Sysprep.inf file.</span></span> <span data-ttu-id="adf28-133">Para obter um exemplo de como chamar esse programa executável no seu arquivo Sysprep. inf, consulte o arquivo de exemplo mais adiante nesta seção.</span><span class="sxs-lookup"><span data-stu-id="adf28-133">For an example of how to call this executable program in your Sysprep.inf file, see the sample file later in this section.</span></span>

<span data-ttu-id="adf28-134">Depois de concluir a personalização da sua imagem do MED-V, você estará pronto para lacrar a imagem usando Sysprep.</span><span class="sxs-lookup"><span data-stu-id="adf28-134">After you have completed customization of your MED-V image, you are ready to seal the image by using Sysprep.</span></span>

<a href="" id="bkmk-seal"></a>**<span data-ttu-id="adf28-135">Lacrando a imagem do MED-V usando Sysprep</span><span class="sxs-lookup"><span data-stu-id="adf28-135">Sealing the MED-V Image by Using Sysprep</span></span>**

1.  <span data-ttu-id="adf28-136">A ferramenta de preparação do sistema (Sysprep) é uma tecnologia que você pode usar para realizar instalações baseadas em imagens em toda a rede com intervenção mínima de um administrador ou profissional.</span><span class="sxs-lookup"><span data-stu-id="adf28-136">The System Preparation tool (Sysprep) is a technology that you can use to perform image-based installations throughout the network with minimal intervention by an administrator or IT-Professional.</span></span>

2.  <span data-ttu-id="adf28-137">Em um ambiente do MED-V, você pode usar o Sysprep para atribuir identificadores de segurança exclusivos (SID) e outras configurações a cada espaço de trabalho do MED-V na primeira vez que eles forem iniciados.</span><span class="sxs-lookup"><span data-stu-id="adf28-137">In a MED-V environment, you can use Sysprep to assign unique security IDs (SID) and other settings to each MED-V workspace the first time that they are started.</span></span>

    **<span data-ttu-id="adf28-138">Observação</span><span class="sxs-lookup"><span data-stu-id="adf28-138">Note</span></span>**  
    <span data-ttu-id="adf28-139">Para obter mais informações sobre como usar o Sysprep, consulte [referência técnica do Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .</span><span class="sxs-lookup"><span data-stu-id="adf28-139">For more information about how to use Sysprep, see [Sysprep Technical Reference](https://go.microsoft.com/fwlink/?LinkId=195930) (https://go.microsoft.com/fwlink/?LinkId=195930).</span></span>



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## <span data-ttu-id="adf28-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="adf28-140">Example</span></span>


<span data-ttu-id="adf28-141">Aqui está um exemplo de um arquivo Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="adf28-141">Here is an example of a Sysprep.inf file.</span></span>

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## <span data-ttu-id="adf28-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adf28-142">Related topics</span></span>


[<span data-ttu-id="adf28-143">Criar um pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="adf28-143">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

[<span data-ttu-id="adf28-144">Preparar uma imagem da MED-V</span><span class="sxs-lookup"><span data-stu-id="adf28-144">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









