---
title: Sobre o MBAM 2.0 SP1
description: Sobre o MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799295"
---
# Sobre o MBAM 2.0 SP1

Este tópico descreve as alterações no Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1). Para obter uma descrição geral do MBAM, consulte [introdução ao MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>O que há de novo no MBAM 2,0 SP1

Esta versão do MBAM fornece os novos recursos e funcionalidades a seguir.

### Suporte para o Gerenciador de configuração do Windows 8,1, Windows Server 2012 R2 e System Center 2012 R2

O Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) adiciona suporte para o Windows 8,1, o Windows Server 2012 R2 e o System Center 2012 R2 Configuration Manager.

### Suporte para Microsoft SQL Server 2008 R2 SP2

O Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) adiciona suporte ao Microsoft SQL Server 2008 R2 SP2. Você deve usar o Microsoft SQL Server 2008 R2 ou superior se estiver executando o Microsoft System Center Configuration Manager 2007 R2.

### Acúmulo de comentários do cliente

O MBAM 2,0 SP1 inclui um pacote cumulativo de correções para solucionar problemas que foram encontrados desde a versão do Microsoft BitLocker Administration and Monitoring (MBAM) 2,0. Como parte dessas alterações, o campo nome do computador agora aparece nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker, quando você executa o MBAM com o Microsoft System Center Configuration Manager 2007.

### A exceção do firewall deve ser definida em portas para o portal de autoatendimento e o site de administração e monitoramento

Ao configurar o portal de autoatendimento e o site de administração e monitoramento, você deve definir uma exceção de firewall para permitir a comunicação por meio das portas especificadas. Anteriormente, a instalação do servidor do MBAM abriu as portas automaticamente no firewall do Windows.

### O local dos relatórios do MBAM foi alterado no Configuration Manager

Os relatórios do MBAM para a topologia integrada do Configuration Manager agora estão disponíveis em subpastas dentro do nó MBAM. Os nomes de subpastas representam o idioma dos relatórios dentro da subpasta.

### Capacidade de instalar o MBAM em um servidor de site primário quando você instala o MBAM com o Configuration Manager

Você pode instalar o MBAM em um servidor de site primário ou um servidor de site de administração central quando instalar o MBAM com a topologia integrada do Configuration Manager. Antes, era necessário instalar o MBAM em um servidor de site de administração central.

**Importante**  
O servidor no qual você instala o MBAM deve ser o servidor de nível superior na sua hierarquia.



A instalação do MBAM funciona de maneira diferente para o Microsoft System Center Configuration Manager 2007 e o Microsoft System Center 2012 Configuration Manager da seguinte forma:

-   **Configuration manager 2007** : se você instalar o MBAM em um servidor de site primário que faz parte de uma hierarquia do Configuration Manager maior e tiver um servidor pai do site central, o MBAM resolverá o servidor pai do site central e executará todas as ações de instalação nesse servidor pai. As ações de instalação incluem verificação de pré-requisitos e instalação dos objetos e relatórios do Configuration Manager. Por exemplo, se você instalar o MBAM em um servidor de site primário que seja filho de um servidor pai de site central, o MBAM instalará todos os objetos e relatórios do Configuration Manager no servidor pai. Se você instalar o MBAM no servidor pai, o MBAM executará todas as ações de instalação nesse servidor pai.

-   **Gerenciador de configuração do System Center 2012** : se você instalar o MBAM em um servidor de site primário ou em um servidor de administração central, o MBAM executará todas as ações de instalação nesse servidor de site.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> O console do Configuration Manager deve estar instalado no computador no qual você instala o servidor MBAM

Ao instalar o MBAM com a topologia integrada do Configuration Manager, você deve instalar o console do Configuration Manager no mesmo computador em que o MBAM será instalado. Se você usar a arquitetura recomendada, que é descrita em [introdução-usando MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), você instalaria o MBAM no servidor de site primário do Configuration Manager.

### Novos parâmetros de linha de comando de configuração para a topologia integrada do Configuration Manager

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro de linha de comando</th>
<th align="left">Descrição</th>
<th align="left">Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Permite que você instale os relatórios do Configuration Manager em um servidor remoto do SQL Server Reporting Services (SSRS) que faz parte do mesmo site do Configuration Manager para o qual o MBAM está instalado. Você pode definir o valor para o nome de domínio totalmente qualificado do servidor de função do ponto do SSRS remoto.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Permite que você instale somente os relatórios do Configuration Manager, sem outros objetos do Configuration Manager, como a linha de base, a coleção e os itens de configuração.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você deve combinar esse parâmetro com o parâmetro CM_REPORTS_COLLECTION_ID.</p>
</div>
<div>

</div>
<p>Valores de parâmetros válidos:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul>
<p>Você pode combinar esse parâmetro com o parâmetro CM_SSRS_REMOTE_SERVER_NAME se quiser instalar os relatórios apenas em um servidor remoto de função do ponto do SSRS.</p>
<p>Se você não definir o parâmetro ou se defini-lo como false, a instalação do MBAM instalará todos os objetos do Configuration Manager, incluindo os relatórios.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = verdadeiro</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>Uma ID de coleção existente que identifica a coleção para a qual os dados de conformidade de relatório serão exibidos. Você pode especificar qualquer ID de coleção. Você não precisa usar a ID da coleção "computadores com suporte MBAM".</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = verdadeiro</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Capacidade de ativar ou desativar o texto do aviso do portal de autoatendimento

O MBAM 2,0 SP1 permite que você desative o texto de aviso no portal de autoatendimento. Anteriormente, o texto do aviso é exibido por padrão e você não pôde desativá-lo.

**Para desativar o texto de aviso**

1.  No servidor em que você instalou o portal de autoatendimento, abra serviços de informações da Internet (IIS) e navegue até **sites &gt; Administração e monitoramento do Microsoft BitLocker &gt; SelfService &gt; configurações do aplicativo**.

2.  Na coluna **Name** , selecione **DisplayNotice**e defina o valor como **false**.

### Capacidade de localizar a instrução HelpdeskText que aponta os usuários para obter informações mais Autoatendimento do portal

Você pode configurar uma versão localizada da instrução "HelpdeskText" do portal de autoatendimento, que informa aos usuários finais como obter ajuda adicional quando estiverem usando o portal de autoatendimento. Se você configurar o texto localizado para a instrução, conforme descrito nas instruções a seguir, o MBAM exibirá a versão localizada. Se MBAM não encontrar a versão localizada, ele exibirá o valor que está no parâmetro **HelpdeskText** .

**Para exibir uma versão localizada da instrução HelpdeskText**

1.  No servidor em que você instalou o portal de autoatendimento, abra o IIS e navegue para **sites &gt; Administração e administração do Microsoft BitLocker &gt; SelfService configurações do &gt; aplicativo**.

2.  No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .

3.  No campo **nome** , digite **HelpdeskText**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para o texto. Por exemplo, para criar uma instrução HelpdeskText localizada em espanhol, você deve nomear o parâmetro HelpdeskText \ _es-es. Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  No campo **valor** , digite o texto localizado que você deseja exibir para os usuários finais.

### Capacidade de localizar o portal de autoatendimento HelpdeskURL

Você pode configurar uma versão localizada do portal de autoatendimento HelpdeskURL para exibir aos usuários finais por padrão. Se você criar uma versão localizada, conforme descrito nas instruções a seguir, o MBAM encontrará e exibirá a versão localizada. Se o MBAM não encontrar uma versão localizada, ele exibirá a URL que está configurada para o parâmetro HelpDeskURL.

**Para exibir um HelpdeskURL localizado**

1.  No servidor em que você instalou o portal de autoatendimento, abra o IIS e navegue para **sites &gt; Administração e administração do Microsoft BitLocker &gt; SelfService configurações do &gt; aplicativo**.

2.  No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .

3.  No campo **nome** , digite **HelpdeskURL**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para a URL. Por exemplo, para criar um HelpdeskURL localizado em espanhol, você deve nomear o parâmetro HelpdeskURL \ _es-es. Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  No campo **valor** , digite o HelpdeskURL localizado que você deseja exibir para os usuários finais.

### Capacidade de localizar o texto de aviso do portal de autoatendimento

Você pode configurar o texto de aviso localizado para exibir aos usuários finais por padrão no portal de autoatendimento. O arquivo notice.txt, que exibe o texto do aviso, está localizado no seguinte diretório raiz:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

Para exibir o texto de aviso localizado, crie um arquivo notice.txt localizado e salve-o em uma pasta de idioma específico no seguinte diretório:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

O MBAM exibe o texto do aviso com base nas seguintes regras:

-   Se você criar um arquivo notice.txt localizado na pasta de idiomas apropriada, o MBAM exibirá o texto de aviso localizado.

-   Se o MBAM não encontrar uma versão localizada do arquivo notice.txt, ele exibirá o texto no arquivo de notice.txt padrão.

-   Se o MBAM não encontrar um arquivo de notice.txt padrão, ele exibirá o texto padrão no portal de autoatendimento.

**Observação**  
Se o navegador de um usuário final estiver definido como um idioma que não tenha uma subpasta ou notice.txt de idioma correspondente, o texto que estiver no arquivo notice.txt do diretório raiz a seguir será exibido:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self



**Para criar um arquivo notice.txt localizado**

1.  No servidor em que você instalou o portal de autoatendimento, crie uma &lt; *language* &gt; pasta de idiomas no seguinte diretório, onde &lt; *idioma* &gt; representa o nome do idioma localizado:

    &lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

    **Observação**  
    Algumas pastas de idioma já existem, portanto, talvez você não precise criar uma. Se você precisar criar uma pasta de idiomas, consulte [referência da API do NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947) para obter uma lista dos nomes válidos que você pode usar para a pasta de &lt; *idiomas* &gt; .



2.  Crie um arquivo notice.txt que contenha o texto de aviso localizado.

3.  Salve o arquivo notice.txt na pasta de &lt; *idiomas* &gt; . Por exemplo, para criar um arquivo notice.txt localizado em espanhol, salve o arquivo notice.txt localizado na seguinte pasta:

    &lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\es-es do serviço \\Self

## Atualizando para o MBAM 2,0 SP1


Você pode atualizar para o MBAM 2,0 SP1 a partir de qualquer versão anterior do MBAM.

### Atualizando a infraestrutura do MBAM

Você pode atualizar a infraestrutura do MBAM Server para o MBAM 2,0 SP1 da seguinte maneira:

**Substituição manual do servidor in-loco**: você deve desinstalar manualmente a infraestrutura do servidor do MBAM existente e instalar a infraestrutura de servidor do MBAM 2,0 SP1. Você não precisa remover os bancos de dados para fazer a atualização. Em vez disso, selecione os bancos de dados existentes, que a versão anterior do MBAM criou. A instalação da atualização do MBAM 2,0 SP1 migra os bancos de dados existentes para o MBAM 2,0 SP1.

**Atualização do cliente distribuído**: se você estiver usando a topologia MBAM autônoma, poderá atualizar os clientes do MBAM gradualmente após a instalação da infraestrutura de servidor MBAM do 2,0 SP1.

Depois de atualizar a infraestrutura do MBAM Server, os clientes do MBAM 1,0 ou do 2,0 serão reportados para o servidor do MBAM 2,0 SP1 e armazenarão os dados de recuperação, mas a conformidade será baseada nas políticas disponíveis para a versão do MBAM cliente que está instalada atualmente. Para habilitar o relatório de políticas do MBAM 2,0 SP1, você deve atualizar os computadores cliente para o MBAM 2,0 SP1. Você pode atualizar os computadores cliente para o cliente do MBAM 2,0 SP1 sem desinstalar o cliente anterior, e o cliente começará a se aplicar e gerar relatórios com base nas políticas do MBAM 2,0 SP1.

Para obter mais informações sobre como atualizar os servidores do MBAM, consulte [atualizando de versões anteriores do MBAM](upgrading-from-previous-versions-of-mbam.md).

### Atualizando o cliente do MBAM para o MBAM 2,0 SP1

Para atualizar os computadores de usuários finais para o cliente do MBAM 2,0 SP1, execute **MbamClientSetup.exe** em cada computador cliente. O instalador atualiza automaticamente o cliente para o cliente do MBAM 2,0 SP1. Após a instalação, os computadores cliente não precisam ser reinicializados, e o cliente do MBAM 2,0 SP1 começa a se aplicar e se comunicar com as políticas do MBAM 2,0 SP1.

Se estiver usando o MBAM com o Configuration Manager, você deve atualizar os computadores cliente MBAM para o MBAM 2,0 SP1.

Para obter mais informações sobre como atualizar os computadores cliente do MBAM, confira o guia [de atualização de versões anteriores do MBAM](upgrading-from-previous-versions-of-mbam.md).

## Instalar ou atualizar para o MBAM 2,0 SP1 com o Configuration Manager


Esta seção descreve os requisitos durante a instalação do MBAM 2,0 SP1 como uma nova instalação ou atualização para uma instalação anterior do MBAM 2,0 SP1.

### Arquivos necessários para instalar o MBAM 2,0 SP1 se você estiver usando o MBAM com o Configuration Manager

Se você estiver instalando o MBAM pela primeira vez e estiver usando o MBAM 2,0 SP1 com o System Center Configuration Manager, será necessário criar ou editar arquivos MOF para permitir que o MBAM funcione corretamente com o Configuration Manager.

-   **arquivo de configuração. mof**

    -   Se você estiver usando o Configuration Manager 2007, será necessário editar o arquivo Configuration. mof completando a etapa 3 do item **atualizar o arquivo Configuration. mof se você atualizar para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007**, que segue este item.

    -   Se você estiver usando o Gerenciador de configuração do System Center 2012, edite o arquivo Configuration. mof seguindo as instruções em [Editar o arquivo Configuration. mof](edit-the-configurationmof-file.md).

-   **arquivo SMS \ _def. mof** – siga as instruções em [criar ou editar o arquivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).

### Atualize o arquivo Configuration. mof se você atualizar para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007

Se estiver atualizando para o MBAM 2,0 SP1 e estiver usando o MBAM com o Configuration Manager 2007, você deve atualizar o arquivo Configuration. MOF para garantir que o MBAM 2,0 SP1 funcione corretamente.

**Para atualizar o arquivo Configuration. mof:**

1.  No servidor do Configuration Manager, navegue até o local do arquivo de configuração. mof:

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    Em uma instalação padrão, o local de instalação é%systemdrive%\\Program Files (x86) \\Microsoft Configuration Manager.

2.  Examine o bloco de código que você acrescentou ao arquivo Configuration. mof e exclua-o. O bloco de código será semelhante ao mostrado na etapa a seguir.

3.  Copie o bloco de código a seguir e, em seguida, adicione-o ao arquivo Configuration. MOF para adicionar as seguintes classes MBAM necessárias ao arquivo:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Tradução do MBAM 2,0 SP1

O MBAM 2,0 SP1 agora está disponível nos seguintes idiomas:

-   Inglês (Estados Unidos) en-US
-   Francês (França) fr-FR
-   Italiano (Itália) it-IT
-   Alemão (Alemanha) de-DE
-   Espanhol, classificação internacional (Espanha) es-ES
-   Coreano (Coréia) ko-KR
-   Japonês (Japão) ja-JP
-   Português (Brasil) pt-BR
-   Russo (Rússia) ru-RU
-   Chinês tradicional zh-TW
-   Chinês simplificado zh-CN

## Como obter tecnologias do MDOP

O MBAM 2,0 SP1 faz parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Tópicos relacionados

[Notas de versão do MBAM 2.0 SP1](release-notes-for-mbam-20-sp1.md)









