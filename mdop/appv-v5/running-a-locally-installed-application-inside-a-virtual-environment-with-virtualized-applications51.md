---
title: Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados
description: Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados
author: dansimp
ms.assetid: 71baf193-a9e8-4ffa-aa7f-e0bffed2e4b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 384a1325b2f363595971f70f25fe0a25cade448d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796214"
---
# <span data-ttu-id="b57a9-103">Executando de um aplicativo instalado localmente em um ambiente virtual com aplicativos virtualizados</span><span class="sxs-lookup"><span data-stu-id="b57a9-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="b57a9-104">Você pode executar um aplicativo instalado localmente em um ambiente virtual, juntamente com aplicativos que foram virtualizados usando o Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="b57a9-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="b57a9-105">Você pode querer fazer isso se:</span><span class="sxs-lookup"><span data-stu-id="b57a9-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="b57a9-106">Deseja instalar e executar um aplicativo localmente em computadores cliente, mas deseja virtualizar e executar plug-ins específicos que funcionem com esse aplicativo local.</span><span class="sxs-lookup"><span data-stu-id="b57a9-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="b57a9-107">Está Solucionando problemas em um pacote do cliente App-V e deseja abrir um aplicativo local dentro do ambiente virtual do App-V.</span><span class="sxs-lookup"><span data-stu-id="b57a9-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="b57a9-108">Use qualquer um dos seguintes métodos para abrir um aplicativo local dentro do ambiente virtual do App-V:</span><span class="sxs-lookup"><span data-stu-id="b57a9-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="b57a9-109">Chave do registro RunVirtual</span><span class="sxs-lookup"><span data-stu-id="b57a9-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="b57a9-110">Cmdlet Get-AppvClientPackage do PowerShell</span><span class="sxs-lookup"><span data-stu-id="b57a9-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="b57a9-111">Opções de linha de comando/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="b57a9-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="b57a9-112">Chave do gancho de linha de/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="b57a9-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="b57a9-113">Cada método realiza essencialmente a mesma tarefa, mas alguns métodos podem ser mais adequados para alguns aplicativos do que outros, dependendo se o aplicativo virtualizado já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b57a9-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="b57a9-114">Chave do registro RunVirtual</span><span class="sxs-lookup"><span data-stu-id="b57a9-114">RunVirtual registry key</span></span>


<span data-ttu-id="b57a9-115">Para adicionar um aplicativo instalado localmente a um pacote ou a um ambiente virtual do grupo de conexão, adicione uma subchave à `RunVirtual` chave do registro no editor do registro, conforme descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b57a9-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="b57a9-116">Não há nenhuma configuração de política de grupo disponível para gerenciar essa chave do registro, portanto, você precisa usar o System Center Configuration Manager ou outro sistema ESD (distribuição de software eletrônico) ou editar manualmente o registro.</span><span class="sxs-lookup"><span data-stu-id="b57a9-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="b57a9-117">Métodos com suporte de publicação de pacotes ao usar RunVirtual</span><span class="sxs-lookup"><span data-stu-id="b57a9-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b57a9-118">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="b57a9-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="b57a9-119">Métodos de publicação com suporte</span><span class="sxs-lookup"><span data-stu-id="b57a9-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b57a9-120">App-V 5,0 SP3 e App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b57a9-120">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b57a9-121">Publicado globalmente ou para o usuário</span><span class="sxs-lookup"><span data-stu-id="b57a9-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b57a9-122">App-V 5,0 até App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="b57a9-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b57a9-123">Publicado globalmente apenas</span><span class="sxs-lookup"><span data-stu-id="b57a9-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b57a9-124">Etapas para criar a subchave</span><span class="sxs-lookup"><span data-stu-id="b57a9-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="b57a9-125">Usando as informações da tabela a seguir, crie uma nova chave do registro usando o nome do arquivo executável, por exemplo, **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="b57a9-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b57a9-126">Método de publicação de pacote</span><span class="sxs-lookup"><span data-stu-id="b57a9-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="b57a9-127">Onde criar a chave do registro</span><span class="sxs-lookup"><span data-stu-id="b57a9-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b57a9-128">Publicado globalmente</span><span class="sxs-lookup"><span data-stu-id="b57a9-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b57a9-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="b57a9-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="b57a9-130">Exemplo </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="b57a9-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b57a9-131">Publicado para o usuário</span><span class="sxs-lookup"><span data-stu-id="b57a9-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b57a9-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="b57a9-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="b57a9-133">Exemplo </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="b57a9-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b57a9-134">O grupo conexão pode conter:</span><span class="sxs-lookup"><span data-stu-id="b57a9-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="b57a9-135">Pacotes que são publicados apenas globalmente ou apenas para o usuário</span><span class="sxs-lookup"><span data-stu-id="b57a9-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="b57a9-136">Pacotes publicados globalmente e para o usuário</span><span class="sxs-lookup"><span data-stu-id="b57a9-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="b57a9-137">A tecla HKEY_LOCAL_MACHINE ou HKEY_CURRENT_USER, mas todas as seguintes opções devem ser verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="b57a9-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="b57a9-138">Se quiser incluir vários pacotes no ambiente virtual, você deve incluí-los em um grupo de conexão habilitado.</span><span class="sxs-lookup"><span data-stu-id="b57a9-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="b57a9-139">Crie apenas uma subchave para um dos pacotes no grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="b57a9-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="b57a9-140">Se, por exemplo, você tiver um pacote publicado globalmente e outro pacote publicado para o usuário, crie uma subchave para qualquer um desses pacotes, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="b57a9-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="b57a9-141">Embora você crie uma subchave para apenas um dos pacotes, todos os pacotes no grupo de conexão, além do aplicativo local, estarão disponíveis no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="b57a9-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="b57a9-142">A chave na qual você cria a subchave deve corresponder ao método de publicação usado para o pacote.</span><span class="sxs-lookup"><span data-stu-id="b57a9-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="b57a9-143">Por exemplo, se você publicou o pacote para o usuário, deverá criar a subchave em <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="b57a9-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="b57a9-144">Defina o valor da nova subchave do registro como o PackageID e VersionId do pacote, separando os valores com um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="b57a9-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="b57a9-145">**Sintaxe**: &lt; PackageID &gt; \ _ &lt; VersionId&gt;</span><span class="sxs-lookup"><span data-stu-id="b57a9-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="b57a9-146">**Exemplo**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="b57a9-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="b57a9-147">O aplicativo no exemplo anterior produziria um arquivo de exportação do registro (arquivo. reg) como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b57a9-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="b57a9-148">Cmdlet Get-AppvClientPackage do PowerShell</span><span class="sxs-lookup"><span data-stu-id="b57a9-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="b57a9-149">Você pode usar o cmdlet **Start-AppVVirtualProcess** para recuperar o nome do pacote e iniciar um processo dentro do ambiente virtual do pacote especificado.</span><span class="sxs-lookup"><span data-stu-id="b57a9-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="b57a9-150">Esse método permite iniciar qualquer comando dentro do contexto de um pacote do App-V, independentemente de o pacote estar em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="b57a9-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="b57a9-151">Use a sintaxe de exemplo a seguir e substitua o nome do \*\* &lt; &gt; pacote do pacote:\*\*</span><span class="sxs-lookup"><span data-stu-id="b57a9-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="b57a9-152">Se não souber o nome exato do pacote, você pode usar a linha de comando **Get-AppvClientPackage \ \* executable\\** <em> , em que \*\*executável </em> \* é o nome do aplicativo, por exemplo: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="b57a9-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="b57a9-153">Opções de linha de comando/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="b57a9-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="b57a9-154">Você pode aplicar a opção **/appvpid &lt; : &gt; pid** a qualquer comando, que permite que esse comando seja executado em um processo virtual que você seleciona especificando a identificação do processo (PID).</span><span class="sxs-lookup"><span data-stu-id="b57a9-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="b57a9-155">Usar esse método inicia o novo executável no mesmo ambiente do App-V como um executável que já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b57a9-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="b57a9-156">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="b57a9-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="b57a9-157">Para localizar a ID do processo (PID) do seu processo App-V, execute o comando **tasklist.exe** de um prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="b57a9-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="b57a9-158">Chave do gancho de linha de/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="b57a9-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="b57a9-159">Essa opção permite executar um comando local dentro do ambiente virtual de um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="b57a9-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="b57a9-160">Ao contrário da opção **/appvid** , em que o ambiente virtual já deve estar em execução, essa opção permite que você inicie o ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="b57a9-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="b57a9-161">Syntax</span><span class="sxs-lookup"><span data-stu-id="b57a9-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="b57a9-162">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="b57a9-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="b57a9-163">Para obter o GUID do pacote e a versão do seu aplicativo, execute o cmdlet **Get-AppvClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="b57a9-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="b57a9-164">Concatene a opção **/appvve** com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b57a9-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="b57a9-165">Dois pontos</span><span class="sxs-lookup"><span data-stu-id="b57a9-165">A colon</span></span>

-   <span data-ttu-id="b57a9-166">GUID do pacote do pacote desejado</span><span class="sxs-lookup"><span data-stu-id="b57a9-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="b57a9-167">Um sublinhado</span><span class="sxs-lookup"><span data-stu-id="b57a9-167">An underscore</span></span>

-   <span data-ttu-id="b57a9-168">ID da versão do pacote desejado</span><span class="sxs-lookup"><span data-stu-id="b57a9-168">Version ID of the desired package</span></span>

<span data-ttu-id="b57a9-169">Se você não souber o nome exato do pacote, use a linha de comando **Get-AppvClientPackage \ \* executable\\** <em> , em que \*\* </em> executável\* é o nome do aplicativo, por exemplo: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="b57a9-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="b57a9-170">Esse método permite iniciar qualquer comando dentro do contexto de um pacote do App-V, independentemente de o pacote estar em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="b57a9-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="b57a9-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b57a9-171">Related topics</span></span>


[<span data-ttu-id="b57a9-172">Referência técnica para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b57a9-172">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)

 

 





