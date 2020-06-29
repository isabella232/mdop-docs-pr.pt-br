---
title: Criar um pacote de espaço de trabalho da MED-V
description: Criar um pacote de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799237"
---
# <span data-ttu-id="e5354-103">Criar um pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="e5354-104">Um espaço de trabalho do MED-V é o ambiente de área de trabalho do Windows XP em que os usuários finais interagem com a máquina virtual fornecida pelo MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="e5354-105">O administrador cria e personaliza o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="e5354-106">O espaço de trabalho consiste em uma imagem e a política de grupo que define as regras e a funcionalidade do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="e5354-107">Você pode criar vários espaços de trabalho do MED-V, cada um personalizado com sua própria configuração, configurações e regras.</span><span class="sxs-lookup"><span data-stu-id="e5354-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="e5354-108">Um usuário, grupo ou vários usuários ou grupos podem ser associados a cada espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="e5354-109">A personalização torna o espaço de trabalho do MED-V disponível apenas para esse usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="e5354-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="e5354-110">Use o **pacote do espaço de trabalho do MED-v** para criar espaços de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="e5354-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="e5354-111">O **pacote do espaço de trabalho do MED-V** é dividido em duas seções principais:</span><span class="sxs-lookup"><span data-stu-id="e5354-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="e5354-112">Um painel principal que inclui três botões que você usa para criar e gerenciar espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="e5354-113">O botão **criar um pacote do espaço de trabalho do MED-v** abre o **Assistente Criar pacote de espaço de trabalho do MED-v** que você usa para criar seus espaços de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="e5354-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="e5354-114">Uma **central de ajuda** à direita da janela que fornece informações e orientação para ajudá-lo a criar, testar e gerenciar seus espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="e5354-115">Importante</span><span class="sxs-lookup"><span data-stu-id="e5354-115">Important</span></span>**  
<span data-ttu-id="e5354-116">Antes de poder usar o **pacote do espaço de trabalho do MED-V**, você deve primeiro verificar se a política de execução do Windows PowerShell está definida como Irrestrito.</span><span class="sxs-lookup"><span data-stu-id="e5354-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="e5354-117">Além disso, a política de SAN do computador em que o **pacote do espaço de trabalho do MED-V** é executado deve ser definida como "Online All".</span><span class="sxs-lookup"><span data-stu-id="e5354-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="e5354-118">Para verificar a configuração da política de SAN, execute os seguintes comandos em um prompt de comando com credenciais administrativas:</span><span class="sxs-lookup"><span data-stu-id="e5354-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="e5354-119">Se for necessário, altere a política de SAN para "tudo online" digitando os seguintes comandos no prompt de comando com credenciais administrativas:</span><span class="sxs-lookup"><span data-stu-id="e5354-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="e5354-120">Importante</span><span class="sxs-lookup"><span data-stu-id="e5354-120">Important</span></span>**  
<span data-ttu-id="e5354-121">Se o software de criptografia de disco automático estiver instalado no computador que você usa para montar o disco rígido virtual e compilar o pacote do espaço de trabalho do MED-V, você deve desabilitar o software antes de começar.</span><span class="sxs-lookup"><span data-stu-id="e5354-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="e5354-122">Caso contrário, você não pode usar o espaço de trabalho do MED-V em qualquer outro computador.</span><span class="sxs-lookup"><span data-stu-id="e5354-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="e5354-123">As informações fornecidas aqui podem ajudá-lo a criar seu pacote de implantação do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="e5354-124">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e5354-124">Prerequisites</span></span>


<span data-ttu-id="e5354-125">Antes de começar a criar seu pacote de implantação do espaço de trabalho do MED-V, verifique se você tem acesso aos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="e5354-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="e5354-126">Uma imagem do Windows XP preparada</span><span class="sxs-lookup"><span data-stu-id="e5354-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="e5354-127">Para obter mais informações sobre como criar uma imagem do Windows XP para usar com o MED-V, consulte [preparar uma imagem do MED-v](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="e5354-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="e5354-128">Um arquivo de texto ou lista que contém informações de redirecionamento de URL</span><span class="sxs-lookup"><span data-stu-id="e5354-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="e5354-129">Seu arquivo de texto ou lista de redirecionamento de URL contém as URLs que você deseja que sejam redirecionadas do computador host para o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="e5354-130">Quando você estiver usando o assistente de empacotamento para criar seu espaço de trabalho do MED-V, importe, digite ou copie e cole essas informações de redirecionamento como uma das etapas no processo de criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="e5354-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="e5354-131">Observação</span><span class="sxs-lookup"><span data-stu-id="e5354-131">Note</span></span>**  
    <span data-ttu-id="e5354-132">O redirecionamento de URL no MED-V só oferece suporte aos protocolos HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5354-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="e5354-133">O MED-V não oferece suporte para FTP ou outros protocolos.</span><span class="sxs-lookup"><span data-stu-id="e5354-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="e5354-134">Empacotando um espaço de trabalho do MED-V para um idioma diferente do idioma do pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="e5354-135">Por padrão, o espaço de trabalho do MED-V dá suporte a caracteres no idioma do computador e em inglês.</span><span class="sxs-lookup"><span data-stu-id="e5354-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="e5354-136">Para criar um espaço de trabalho do MED-V para um idioma diferente daquele instalado no computador, especifique **-Loc \ [locale \]** no script do PowerShell (. ps1) após o nome do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="e5354-137">Para criar um pacote de espaço de trabalho do MED-V em um idioma diferente do padrão do computador do empacotador do espaço de trabalho do MED-v, gere um script no idioma padrão executando o pacote do espaço de trabalho do MED-v e modificando o script de saída conforme necessário para a sua localidade.</span><span class="sxs-lookup"><span data-stu-id="e5354-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="e5354-138">O script está localizado no diretório de saída do espaço de trabalho do MED-V especificado durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="e5354-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="e5354-139">Os nomes das configurações de localidade estão em. WXL arquivos no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="e5354-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="e5354-140">C:\\Arquivos de Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="e5354-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="e5354-141">Criando um pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="e5354-142">Para criar um pacote de espaço de trabalho do MED-V, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e5354-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="e5354-143">Para abrir o **pacote do espaço de trabalho do MED-V**, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="e5354-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="e5354-144">No painel principal do **pacote de espaço de trabalho do MED-v** , clique em **criar um pacote de espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="e5354-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="e5354-145">O **Assistente para criação do pacote do espaço de trabalho** do MED-v Create-v é exibido.</span><span class="sxs-lookup"><span data-stu-id="e5354-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="e5354-146">O assistente consiste nas seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="e5354-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="e5354-147">Informações do pacote</span><span class="sxs-lookup"><span data-stu-id="e5354-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-148">Especifique um nome para o espaço de trabalho do MED-V e selecione uma pasta onde os arquivos do pacote do espaço de trabalho do MED-V serão salvos.</span><span class="sxs-lookup"><span data-stu-id="e5354-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="e5354-149">Selecionar imagem do Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5354-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-150">Especifique a imagem do computador virtual do Windows XP preparado.</span><span class="sxs-lookup"><span data-stu-id="e5354-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="e5354-151">Configuração da primeira vez</span><span class="sxs-lookup"><span data-stu-id="e5354-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-152">Especifique o processo de configuração que o MED-V segue durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="e5354-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="e5354-153">Mensagens do MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-154">Especifique as mensagens e a URL opcional para as informações de ajuda que o usuário final vê durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="e5354-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="e5354-155">Nomeando computadores</span><span class="sxs-lookup"><span data-stu-id="e5354-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-156">Especifique como a máquina virtual MED-V é nomeada.</span><span class="sxs-lookup"><span data-stu-id="e5354-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="e5354-157">Copiar configurações do host</span><span class="sxs-lookup"><span data-stu-id="e5354-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-158">Especifique como as configurações para o espaço de trabalho do MED-V são definidas.</span><span class="sxs-lookup"><span data-stu-id="e5354-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="e5354-159">Inicialização e rede</span><span class="sxs-lookup"><span data-stu-id="e5354-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-160">Especifique as configurações para iniciar o espaço de trabalho do MED-V, a rede e as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="e5354-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="e5354-161">Redirecionamento da Web</span><span class="sxs-lookup"><span data-stu-id="e5354-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-162">Especifique um arquivo de texto ou uma lista de URLs que você deseja que sejam redirecionados para o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="e5354-163">Resumo</span><span class="sxs-lookup"><span data-stu-id="e5354-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="e5354-164">Verifique as configurações do espaço de trabalho do MED-V e comece a criar seu pacote de implantação do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="e5354-165">Na página **informações do pacote** , insira um nome para o espaço de trabalho do MED-v e selecione uma pasta onde os arquivos do pacote do espaço de trabalho do MED-v serão salvos.</span><span class="sxs-lookup"><span data-stu-id="e5354-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="e5354-166">Aviso</span><span class="sxs-lookup"><span data-stu-id="e5354-166">Warning</span></span>**  
    <span data-ttu-id="e5354-167">Você deve nomear o espaço de trabalho do MED-V e especificar uma pasta para continuar.</span><span class="sxs-lookup"><span data-stu-id="e5354-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="e5354-168">Na página **selecionar imagem do Windows XP** , especifique o local da imagem do seu computador virtual do MED-V do Windows XP preparado (arquivo. vhd).</span><span class="sxs-lookup"><span data-stu-id="e5354-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="e5354-169">Aviso</span><span class="sxs-lookup"><span data-stu-id="e5354-169">Warning</span></span>**  
   <span data-ttu-id="e5354-170">Você deve especificar uma imagem de VHD do Windows XP para continuar.</span><span class="sxs-lookup"><span data-stu-id="e5354-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="e5354-171">Na página **configuração inicial** , selecione se você deseja que o programa de instalação inicial seja executado enquanto estiver participando ou desacompanhados e se quiser que o espaço de trabalho do MED-V seja usado separadamente ou usado por todos os usuários finais em um computador compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e5354-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="e5354-172">Se você selecionar **a instalação autônoma, sem notificação**, o usuário final não será informado antes da primeira instalação ser executada, e a máquina virtual não será mostrada para o usuário final durante a configuração do primeiro período.</span><span class="sxs-lookup"><span data-stu-id="e5354-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="e5354-173">Além disso, a página **mensagens do MED-V** do assistente fica oculta porque nenhuma mensagem será necessária se a configuração da primeira vez for executada em um modo completamente autônomo.</span><span class="sxs-lookup"><span data-stu-id="e5354-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="e5354-174">Se você selecionar **a instalação autônoma, mas notificar os usuários finais antes do início da configuração da primeira vez**, o usuário final será informado antes da execução da primeira vez que a configuração é executada.</span><span class="sxs-lookup"><span data-stu-id="e5354-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="e5354-175">No entanto, a máquina virtual não é mostrada para o usuário final durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="e5354-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="e5354-176">Selecione **configuração assistida** se o usuário final precisar inserir informações durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="e5354-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="e5354-177">O comportamento padrão é **instalação autônoma, mas notifique os usuários finais antes do início da configuração do primeiro horário**.</span><span class="sxs-lookup"><span data-stu-id="e5354-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="e5354-178">Tenha</span><span class="sxs-lookup"><span data-stu-id="e5354-178">Caution</span></span>**  
   <span data-ttu-id="e5354-179">Se você criou o arquivo Sysprep. inf para que a mini-instalação exija que a entrada do usuário seja concluída, você deve selecionar **configuração assistida** ou problemas podem ocorrer durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="e5354-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="e5354-180">Na página **mensagens do MED-V** , especifique as seguintes mensagens que o usuário final vê durante a primeira configuração do tempo:</span><span class="sxs-lookup"><span data-stu-id="e5354-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="e5354-181">A mensagem que o usuário final vê quando a configuração é iniciada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e5354-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="e5354-182">A mensagem que o usuário final verá se a primeira configuração falhar ou ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="e5354-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="e5354-183">Observação</span><span class="sxs-lookup"><span data-stu-id="e5354-183">Note</span></span>**  
   <span data-ttu-id="e5354-184">A página de **mensagens do MED-V** do assistente estará oculta se você tiver selecionado **a instalação autônoma, sem notificação** na página **configuração do primeiro uso** .</span><span class="sxs-lookup"><span data-stu-id="e5354-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="e5354-185">Na página **nomear computadores** , você pode especificar se o nome do computador é gerenciado pelo MED-V ou por uma ferramenta de gerenciamento do sistema, como Sysprep.</span><span class="sxs-lookup"><span data-stu-id="e5354-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="e5354-186">O padrão é que o nome do computador seja gerenciado por uma ferramenta de gerenciamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="e5354-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="e5354-187">Se você especificar que o nome do computador é gerenciado pelo MED-V, selecione uma Convenção de nomenclatura de computador (máscara) predefinida na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="e5354-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="e5354-188">Uma visualização de um nome de computador de exemplo é exibida com base no computador que você está usando para criar o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="e5354-189">Se você selecionar uma das convenções de nomenclatura personalizadas, os campos que você pode especificar serão limitados aos seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="e5354-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="e5354-190">Os campos prefixo e sufixo estão limitados aos caracteres A-Z, a-z, a 0-9 e aos caracteres especiais!</span><span class="sxs-lookup"><span data-stu-id="e5354-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="e5354-191">@ \ # $% ^ & ()-\ _ ' {}.</span><span class="sxs-lookup"><span data-stu-id="e5354-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="e5354-192">e ~.</span><span class="sxs-lookup"><span data-stu-id="e5354-192">and ~.</span></span>

   -   <span data-ttu-id="e5354-193">Os campos hostname e username estão limitados aos dígitos de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="e5354-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="e5354-194">Importante</span><span class="sxs-lookup"><span data-stu-id="e5354-194">Important</span></span>**  
   <span data-ttu-id="e5354-195">Os nomes de computador devem ser exclusivos e limitados a um máximo de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e5354-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="e5354-196">Ao decidir sobre o método de nomenclatura do computador, considere os usuários finais que têm vários computadores ou que compartilham um computador e evite usar máscaras de nomes de computador que possam causar uma colisão na rede.</span><span class="sxs-lookup"><span data-stu-id="e5354-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="e5354-197">Na página **copiar configurações do host** , você pode selecionar as seguintes configurações para especificar como o espaço de trabalho do MED-V é configurado:</span><span class="sxs-lookup"><span data-stu-id="e5354-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="e5354-198">Tenha</span><span class="sxs-lookup"><span data-stu-id="e5354-198">Caution</span></span>**  
   <span data-ttu-id="e5354-199">As configurações que você especificar nesta página que são copiadas do computador host para o espaço de trabalho do MED-V substituem aquelas especificadas no arquivo de resposta Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="e5354-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="e5354-200">Na página **inicialização e rede** , você pode alterar o comportamento padrão para as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="e5354-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e5354-201">Iniciar o espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e5354-202">Escolha se deseja iniciar o espaço de trabalho do MED-V no logon do usuário, ao ser usado pela primeira vez ou para permitir que o usuário final decida quando o espaço de trabalho do MED-V é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e5354-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="e5354-203">O espaço de trabalho do MED-V é iniciado de duas maneiras: quando o usuário final faz logon ou quando ele inicia pela primeira vez uma ação que exige o MED-V, como abrir um aplicativo publicado ou inserir uma URL que exija redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="e5354-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="e5354-204">Você pode definir essa configuração para o usuário final ou permitir que o usuário final controle como o MED-V é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e5354-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="e5354-205">Observação</span><span class="sxs-lookup"><span data-stu-id="e5354-205">Note</span></span></strong><br/><p><span data-ttu-id="e5354-206">Se você especificar que o usuário final decide, o comportamento padrão que ele perceberá é que o espaço de trabalho do MED-V é iniciado quando eles fazem logon.</span><span class="sxs-lookup"><span data-stu-id="e5354-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="e5354-207">Eles podem alterar o padrão clicando com o botão direito do mouse no ícone do MED-V na área de notificação e selecionando <strong> as configurações do usuário do MED-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="e5354-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="e5354-208">Se você definir essa configuração para o usuário final, não será possível alterar a forma como o MED-V é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e5354-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e5354-209">Rede</span><span class="sxs-lookup"><span data-stu-id="e5354-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e5354-210">Selecione <strong> compartilhado </strong> ou <strong> ponte </strong> para a configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="e5354-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="e5354-211">O padrão é <strong> compartilhado </strong> .</span><span class="sxs-lookup"><span data-stu-id="e5354-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="e5354-212">Compartilhado </strong> - o espaço de trabalho do MED-V usa a NAT (conversão de endereços de rede) para compartilhar o host&#39;s de IP para o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="e5354-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="e5354-213">Em ponte </strong> - , o espaço de trabalho do MED-V tem seu próprio endereço de rede, normalmente obtido por meio de DHCP.</span><span class="sxs-lookup"><span data-stu-id="e5354-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e5354-214">Credenciais da loja</span><span class="sxs-lookup"><span data-stu-id="e5354-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e5354-215">Escolha se deseja armazenar as credenciais do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e5354-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="e5354-216">O comportamento padrão é que o armazenamento de credenciais está desabilitado para que o usuário final deva ser autenticado toda vez que fizer logon.</span><span class="sxs-lookup"><span data-stu-id="e5354-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="e5354-217">Importante</span><span class="sxs-lookup"><span data-stu-id="e5354-217">Important</span></span></strong><br/><p><span data-ttu-id="e5354-218">Embora o armazenamento em cache das credenciais do usuário final forneça a melhor experiência do usuário, você deve estar ciente dos riscos envolvidos.</span><span class="sxs-lookup"><span data-stu-id="e5354-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="e5354-219">A credencial do domínio do usuário final é armazenada em um formato reversível no Gerenciador de credenciais do Windows.</span><span class="sxs-lookup"><span data-stu-id="e5354-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="e5354-220">Como resultado, um invasor pode escrever um programa que recupere a senha e possa ter acesso às credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="e5354-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="e5354-221">Você só pode diminuir esse risco desabilitando o armazenamento de credenciais do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e5354-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="e5354-222">Na página **redirecionamento da Web** , você pode inserir, colar ou importar uma lista das URLs redirecionadas para o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="e5354-223">Para obter mais informações sobre como configurar as informações de redirecionamento de URL, consulte [pré-requisitos](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="e5354-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="e5354-224">Você também pode especificar como o Internet Explorer no espaço de trabalho do MED-V está configurado para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="e5354-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="e5354-225">Por padrão, o nível de segurança da zona da Internet é definido como alto.</span><span class="sxs-lookup"><span data-stu-id="e5354-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="e5354-226">Além disso, certos recursos de navegação padrão, como a barra de endereços, são removidos.</span><span class="sxs-lookup"><span data-stu-id="e5354-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="e5354-227">Essa configuração padrão do Internet Explorer no espaço de trabalho do MED-V fornece um ambiente de navegação mais seguro para usuários finais.</span><span class="sxs-lookup"><span data-stu-id="e5354-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="e5354-228">Tenha</span><span class="sxs-lookup"><span data-stu-id="e5354-228">Caution</span></span>**  
   <span data-ttu-id="e5354-229">Ao alterar as configurações padrão, você pode personalizar o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="e5354-230">No entanto, observe que, se você alterar as configurações padrão para torná-las menos seguras, poderá expor sua organização a esses riscos de segurança que estão presentes em versões mais antigas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e5354-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="e5354-231">Para obter mais informações, consulte [práticas recomendadas de segurança para operações do MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e5354-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="e5354-232">Na página **Resumo** , você pode revisar as configurações de empacotamento deste espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e5354-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="e5354-233">Se você quiser alterar as configurações, clique no botão **anterior** para retornar à página relevante.</span><span class="sxs-lookup"><span data-stu-id="e5354-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="e5354-234">Quando terminar de revisar as configurações, clique em **criar**.</span><span class="sxs-lookup"><span data-stu-id="e5354-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="e5354-235">A página de **conclusão** do **Assistente Criar pacote de espaço de trabalho do MED-V** abre para mostrar o progresso da criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="e5354-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="e5354-236">Observação</span><span class="sxs-lookup"><span data-stu-id="e5354-236">Note</span></span>**  
   <span data-ttu-id="e5354-237">O processo de criação do pacote do espaço de trabalho do MED-V pode levar alguns minutos para ser concluído, dependendo do tamanho do VHD especificado.</span><span class="sxs-lookup"><span data-stu-id="e5354-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="e5354-238">Clique em **fechar** para fechar o Packaging Wizard e retornar ao **pacote do espaço de trabalho do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="e5354-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="e5354-239">Seu pacote de espaço de trabalho do MED-V agora está pronto para teste antes da implantação.</span><span class="sxs-lookup"><span data-stu-id="e5354-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="e5354-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5354-240">Related topics</span></span>


[<span data-ttu-id="e5354-241">Definição das configurações avançadas usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5354-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="e5354-242">Como testar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="e5354-243">Preparar uma imagem da MED-V</span><span class="sxs-lookup"><span data-stu-id="e5354-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









