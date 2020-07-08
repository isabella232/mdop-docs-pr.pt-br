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
# Como configurar uma imagem do Windows Virtual PC para a MED-V


Depois de instalar tudo o que você deseja incluir em sua imagem do MED-V, você pode configurar a imagem para usar na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0. Os tópicos desta seção fornecem orientação para configurar sua imagem do MED-V para ser executada primeiro antes de criar seu pacote de espaço de trabalho do MED-V.

Primeira vez que o programa de instalação prepara o espaço de trabalho do MED-V para um usuário final. O processo cria uma máquina virtual a partir da imagem empacotada no espaço de trabalho do MED-V e executa a mini-configuração do Windows na máquina virtual. Isso inclui a execução de ambos os scripts de instalação personalizados e o aplicativo de conclusão configuração da primeira vez, FtsCompletion.exe.

Siga estas etapas para configurar sua imagem do MED-V para executar a configuração do primeiro horário:

1. Como opção, você pode compactar o disco rígido virtual (VHD) para recuperar espaço em disco vazio e reduzir o tamanho do VHD antes de prosseguir com a configuração da imagem do PC virtual do Windows. Para obter mais informações, consulte [compactando o disco rígido virtual do MED-V](compacting-the-med-v-virtual-hard-disk.md).

2. Personalize o processo de configuração da máquina virtual.

3. Lacre a imagem do MED-V usando Sysprep.

   **Personalizando o processo de configuração da máquina virtual**

4. Como parte da preparação da imagem para usar com o MED-V, você pode definir várias configurações na máquina virtual, como especificar as configurações para executar o Windows Update. Especifique todas as configurações da máquina virtual necessárias antes de criar o pacote do espaço de trabalho do MED-V.

5. Antes de criar o pacote do espaço de trabalho do MED-V, recomendamos que você desabilite os pontos de restauração na máquina virtual para impedir que o disco diferencial aumente não associado. Para obter mais informações, consulte [como desativar e ativar a restauração do sistema no Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Observação**  
   Você pode configurar seu arquivo Sysprep. inf para desabilitar pontos de restauração quando a configuração da primeira vez for executada. Para obter um exemplo de como definir essa chave GuiRunOnce, consulte o arquivo Sysprep. inf de exemplo mais adiante nesta seção.



6. Configure o processo de configuração para executar a mini-instalação em vez da tela de boas-vindas padrão do Windows. Você deve executar a ferramenta Sysprep usando a opção **-Mini** , ou marcar a caixa de seleção **MiniSetup** na interface gráfica do usuário. Para obter mais informações, consulte [como lacrar a imagem com Sysprep](#bkmk-seal).

   **Chamando o arquivo de conclusão de configuração da primeira vez**

   1.  Um executável chamado FtsCompletion.exe está incluído como parte da instalação do agente de convidado do MED-V. Por padrão, ele está localizado na unidade do sistema da sua imagem do MED-V em **arquivos de programas – virtualização de área de trabalho do Microsoft Enterprise**.

       **Importante**  
       Como a etapa final do processo de configuração inicial, você deve executar este programa executável. O usuário para o qual o programa executável está sendo chamado deve ser um membro do grupo de Administradores local do convidado.



   2.  Você pode decidir como deseja chamar este programa executável, por exemplo, por meio de um script que é implantado com o espaço de trabalho do MED-V. Você pode chamar esse executável como a última linha do seu arquivo Sysprep. inf. Para obter um exemplo de como chamar esse programa executável no seu arquivo Sysprep. inf, consulte o arquivo de exemplo mais adiante nesta seção.

Depois de concluir a personalização da sua imagem do MED-V, você estará pronto para lacrar a imagem usando Sysprep.

<a href="" id="bkmk-seal"></a>**Lacrando a imagem do MED-V usando Sysprep**

1.  A ferramenta de preparação do sistema (Sysprep) é uma tecnologia que você pode usar para realizar instalações baseadas em imagens em toda a rede com intervenção mínima de um administrador ou profissional.

2.  Em um ambiente do MED-V, você pode usar o Sysprep para atribuir identificadores de segurança exclusivos (SID) e outras configurações a cada espaço de trabalho do MED-V na primeira vez que eles forem iniciados.

    **Observação**  
    Para obter mais informações sobre como usar o Sysprep, consulte [referência técnica do Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



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

## Exemplo


Aqui está um exemplo de um arquivo Sysprep. inf.

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

## Tópicos relacionados


[Criar um pacote de espaço de trabalho da MED-V](create-a-med-v-workspace-package.md)

[Preparar uma imagem da MED-V](prepare-a-med-v-image.md)









