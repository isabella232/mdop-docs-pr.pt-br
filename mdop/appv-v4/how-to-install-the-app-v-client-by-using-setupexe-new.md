---
title: Como instalar o cliente do App-V usando Setup.exe
description: Como instalar o cliente do App-V usando Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797105"
---
# <span data-ttu-id="f024a-103">Como instalar o cliente do App-V usando Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f024a-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="f024a-104">Este tópico descreve como instalar o cliente App-V usando o programa setup.exe.</span><span class="sxs-lookup"><span data-stu-id="f024a-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="f024a-105">Quando você instala o cliente App-V usando o programa setup.exe, o instalador determina qual software de pré-requisito é necessário e o instala automaticamente antes de instalar o cliente.</span><span class="sxs-lookup"><span data-stu-id="f024a-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="f024a-106">Para instalar o cliente do Application Virtualization usando o Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f024a-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="f024a-107">Verifique se você está conectado com uma conta que tem direitos de administrador no computador.</span><span class="sxs-lookup"><span data-stu-id="f024a-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="f024a-108">Abra uma janela do prompt de comando e, em seguida, altere o diretório para a pasta que contém os arquivos de instalação.</span><span class="sxs-lookup"><span data-stu-id="f024a-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="f024a-109">Ao instalar a versão 4.6 ou posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f024a-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="f024a-110">A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.</span><span class="sxs-lookup"><span data-stu-id="f024a-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="f024a-111">Digite a cadeia de caracteres do comando instalar no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="f024a-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="f024a-112">Você também pode criar um arquivo de comando e executá-lo a partir do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="f024a-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="f024a-113">Você também pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="f024a-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="f024a-114">O exemplo de linha de comando a seguir mostra como setup.exe pode ser usado com vários parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="f024a-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="f024a-115">Para obter mais informações sobre esses parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f024a-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="f024a-116">"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" produção System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="f024a-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="f024a-117">Importante</span><span class="sxs-lookup"><span data-stu-id="f024a-117">Important</span></span>**  
    -   <span data-ttu-id="f024a-118">As aspas que aparecem na seção "**/v**" devem ser tratadas como caracteres especiais e inseridas com um " **\\** " anterior.</span><span class="sxs-lookup"><span data-stu-id="f024a-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="f024a-119">As aspas são necessárias somente quando o valor contém um espaço; no entanto, para consistência, todas as instâncias no exemplo anterior são mostradas como tendo aspas.</span><span class="sxs-lookup"><span data-stu-id="f024a-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="f024a-120">Os **%** caracteres "" em "**% HomeDrive%**" devem ser precedidos pelo **^** caractere de escape "".</span><span class="sxs-lookup"><span data-stu-id="f024a-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="f024a-121">Caso contrário, o Shell de comando do Windows define o valor para aquele do usuário que está executando a instalação.</span><span class="sxs-lookup"><span data-stu-id="f024a-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="f024a-122">As opções do **InstallShield** **/s** e **/qn** são necessárias para fazer com que essa instalação seja silenciosa.</span><span class="sxs-lookup"><span data-stu-id="f024a-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="f024a-123">A opção **/qn** deve seguir a opção **/v** , separada por apenas um caractere de aspas sem espaços intervenientes.</span><span class="sxs-lookup"><span data-stu-id="f024a-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="f024a-124">A pasta especificada no valor **SWIGLOBALDATA** já deve existir.</span><span class="sxs-lookup"><span data-stu-id="f024a-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="f024a-125">Quando a instalação estiver concluída, recomendamos que você execute um exame do Microsoft Update para garantir que as atualizações mais recentes sejam instaladas.</span><span class="sxs-lookup"><span data-stu-id="f024a-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="f024a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f024a-126">Related topics</span></span>


[<span data-ttu-id="f024a-127">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="f024a-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





