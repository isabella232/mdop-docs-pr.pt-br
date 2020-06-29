---
title: Notas de versão do DaRT 7.0
description: Notas de versão do DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799137"
---
# <span data-ttu-id="ae35f-103">Notas de versão do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ae35f-103">Release Notes for DaRT 7.0</span></span>


**<span data-ttu-id="ae35f-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="ae35f-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="ae35f-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="ae35f-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span>

## <span data-ttu-id="ae35f-106">Sobre o diagnóstico e o conjunto de ferramentas de recuperação da Microsoft 7,0</span><span class="sxs-lookup"><span data-stu-id="ae35f-106">About Microsoft Diagnostics and Recovery Toolset 7.0</span></span>


<span data-ttu-id="ae35f-107">Estas notas da versão contêm informações que são necessárias para instalar com êxito o DaRT7 e contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="ae35f-107">These release notes contain information that is required to successfully install DaRT7 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="ae35f-108">Se houver uma diferença entre essas notas de versão e outra documentação da plataforma DaRT, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="ae35f-108">If there is a difference between these release notes and other DaRT platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ae35f-109">Estas notas de versão substituem o conteúdo incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="ae35f-109">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="ae35f-110">Sobre a documentação do produto</span><span class="sxs-lookup"><span data-stu-id="ae35f-110">About the Product Documentation</span></span>


<span data-ttu-id="ae35f-111">A documentação do Microsoft Diagnostics e do conjunto de ferramentas de recuperação (DaRT) 7 é distribuída com o produto e no site de conexão.</span><span class="sxs-lookup"><span data-stu-id="ae35f-111">Documentation for Microsoft Diagnostics and Recovery Toolset (DaRT)7 is distributed with the product and on the Connect site.</span></span>

<span data-ttu-id="ae35f-112">Para obter ajuda detalhada sobre como usar as ferramentas no DaRT7, consulte o arquivo de ajuda disponível no menu **diagnóstico e recuperação do conjunto de ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="ae35f-112">For detailed help about how to use the tools in DaRT7, see the Help file available on the **Diagnostics and Recovery Toolset** menu.</span></span>

## <span data-ttu-id="ae35f-113">Fornecendo comentários</span><span class="sxs-lookup"><span data-stu-id="ae35f-113">Providing feedback</span></span>


<span data-ttu-id="ae35f-114">Estamos interessados em seus comentários sobre o DaRT7.</span><span class="sxs-lookup"><span data-stu-id="ae35f-114">We are interested in your feedback on DaRT7.</span></span> <span data-ttu-id="ae35f-115">Você pode enviar seus comentários para o dart7feedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ae35f-115">You can send your feedback to dart7feedback@microsoft.com.</span></span> <span data-ttu-id="ae35f-116">Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras dessas ferramentas para torná-las mais úteis no futuro.</span><span class="sxs-lookup"><span data-stu-id="ae35f-116">This email address is not a support channel, but your feedback will help us to plan future changes for these tools to make them more useful to you in the future.</span></span>

## <span data-ttu-id="ae35f-117">Proteger contra vulnerabilidades e vírus de segurança</span><span class="sxs-lookup"><span data-stu-id="ae35f-117">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="ae35f-118">Para ajudar a proteger contra vulnerabilidades e vírus de segurança, recomendamos que você instale as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="ae35f-118">To help protect against security vulnerabilities and viruses, we recommend that you install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="ae35f-119">Para obter mais informações, consulte [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="ae35f-119">For more information, see [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="ae35f-120">Problemas conhecidos com o DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="ae35f-120">Known Issues with DaRT 7.0</span></span>


### <span data-ttu-id="ae35f-121">A verificação de SFC não pode iniciar se a limpeza do sistema autônomo estiver aberta</span><span class="sxs-lookup"><span data-stu-id="ae35f-121">SFC Scan cannot start if Standalone System Sweeper is open</span></span>

<span data-ttu-id="ae35f-122">Se a limpeza do sistema autônomo estiver em execução, a verificação de SFC não poderá ser iniciada ou executada devido a um conflito de recursos entre as duas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ae35f-122">If the Standalone System Sweeper is running, SFC Scan cannot start or run because of a resource conflict between the two tools.</span></span>

<span data-ttu-id="ae35f-123">**Solução alternativa:** Feche a ferramenta de limpeza do sistema autônomo antes de tentar abrir ou executar a ferramenta de verificação SFC.</span><span class="sxs-lookup"><span data-stu-id="ae35f-123">**Workaround:** Close the Standalone System Sweeper before you try to open or run the SFC Scan tool.</span></span>

### <span data-ttu-id="ae35f-124">Caracteres Unicode podem não ser exibidos em nomes de arquivo</span><span class="sxs-lookup"><span data-stu-id="ae35f-124">Unicode characters may not be displayed in file names</span></span>

<span data-ttu-id="ae35f-125">Se você excluir um arquivo que tem caracteres Unicode em seu nome de arquivo e tentar restaurar o arquivo usando a ferramenta restauração de arquivo, o arquivo não será encontrado.</span><span class="sxs-lookup"><span data-stu-id="ae35f-125">If you delete a file that has Unicode characters in its file name and try to restore the file by using the File Restore tool, the file is not found.</span></span> <span data-ttu-id="ae35f-126">Isso só ocorre quando você usa caracteres de um idioma diferente do idioma do DVD do Windows que foi usado para criar a imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ae35f-126">This only occurs when you use characters from a language other than the language of the Windows DVD that was used to create the recovery image.</span></span>

<span data-ttu-id="ae35f-127">**Solução alternativa:** Certifique-se de que o idioma usado pelo DaRT corresponda ao idioma usado pelo sistema operacional do qual ele está tentando restaurar arquivos.</span><span class="sxs-lookup"><span data-stu-id="ae35f-127">**Workaround:** Make sure that the language that is used by DaRT matches the language that is used by the operating system from which it is trying to restore files.</span></span>

### <span data-ttu-id="ae35f-128">A instalação de linha de comando do DaRT pode falhar silenciosamente</span><span class="sxs-lookup"><span data-stu-id="ae35f-128">DaRT command-line installation may fail silently</span></span>

<span data-ttu-id="ae35f-129">A instalação de linha de comando do DaRT falha silenciosamente se executada com a opção modo silencioso, a menos que seja executada usando permissões de administrador elevadas.</span><span class="sxs-lookup"><span data-stu-id="ae35f-129">DaRT command-line installation fails silently if run with the quiet mode option unless it is run by using elevated administrator permissions.</span></span>

<span data-ttu-id="ae35f-130">**Solução alternativa:** Execute a instalação de linha de comando usando permissões elevadas de administrador.</span><span class="sxs-lookup"><span data-stu-id="ae35f-130">**Workaround:** Run the command-line installation by using elevated administrator permissions.</span></span> <span data-ttu-id="ae35f-131">A instalação do DaRT suporta as opções típicas do Windows Installer para instalação por linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ae35f-131">DaRT installation supports the typical Windows Installer options for command-line installation.</span></span> <span data-ttu-id="ae35f-132">Consulte [as opções de linha de comando](https://go.microsoft.com/fwlink/?LinkId=160689) do Windows Installer para obter mais informações sobre as várias opções disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ae35f-132">Please see [Command-Line Options](https://go.microsoft.com/fwlink/?LinkId=160689) for Windows Installer for more information about the several available switches.</span></span>

### <span data-ttu-id="ae35f-133">A pesquisa de arquivos não pode mover uma pasta para um volume diferente</span><span class="sxs-lookup"><span data-stu-id="ae35f-133">File Search cannot move a folder to a different volume</span></span>

<span data-ttu-id="ae35f-134">Não há suporte para a movimentação de pastas entre volumes pelo aplicativo de pesquisa de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ae35f-134">Moving folders between volumes is not supported by the File Search application.</span></span> <span data-ttu-id="ae35f-135">Se você tentar mover uma pasta para um volume diferente na pesquisa de arquivos, o seguinte erro será retornado: "ocorreu um erro ao gravar o \* &lt; nome &gt; \*do arquivo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae35f-135">If you try to move a folder to a different volume in File Search, the following error is returned: "An error occurred while writing the file *&lt;filename&gt;*.</span></span> <span data-ttu-id="ae35f-136">Verifique se a unidade tem espaço suficiente e se o caminho de destino está acessível. "</span><span class="sxs-lookup"><span data-stu-id="ae35f-136">Make sure that the drive has sufficient space and the destination path is accessible."</span></span>

<span data-ttu-id="ae35f-137">**Solução alternativa:** Use o Explorer para mover uma pasta para um volume diferente.</span><span class="sxs-lookup"><span data-stu-id="ae35f-137">**Workaround:** Use the Explorer to move a folder to a different volume.</span></span>

### <span data-ttu-id="ae35f-138">Alguns dados podem não estar disponíveis em computadores em que as letras de unidade são remapeadas</span><span class="sxs-lookup"><span data-stu-id="ae35f-138">Some data may not be available on computers where the drive letters are remapped</span></span>

<span data-ttu-id="ae35f-139">Esse problema pode ocorrer em computadores habilitados para BitLocker e em computadores multi-inicializador.</span><span class="sxs-lookup"><span data-stu-id="ae35f-139">This problem can occur on BitLocker-enabled computers and multiboot computers.</span></span> <span data-ttu-id="ae35f-140">Isso ocorre porque algumas informações no registro offline têm letras de drive embutidas e o DaRT usa letras diferentes para os mesmos volumes.</span><span class="sxs-lookup"><span data-stu-id="ae35f-140">This occurs because some information in the offline registry has hard-coded drive letters, and DaRT uses different letters for the same volumes.</span></span> <span data-ttu-id="ae35f-141">Os efeitos típicos incluem não ter acesso a determinadas contas de usuário locais no editor do registro.</span><span class="sxs-lookup"><span data-stu-id="ae35f-141">The typical effects include not having access to certain local user accounts in Registry Editor.</span></span> <span data-ttu-id="ae35f-142">Além disso, algumas ferramentas podem não conseguir obter as propriedades que dependem da resolução de caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae35f-142">Additionally, some tools may be unable to obtain properties that rely on resolving file paths.</span></span>

<span data-ttu-id="ae35f-143">**Solução alternativa:** Use a opção para remapear as letras da unidade ao iniciar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="ae35f-143">**Workaround:** Use the option to remap the drive letters as DaRT starts.</span></span> <span data-ttu-id="ae35f-144">Isso geralmente alinha as letras de unidade típicas ao esperado.</span><span class="sxs-lookup"><span data-stu-id="ae35f-144">This usually aligns the typical drive letters to what is expected.</span></span>

### <span data-ttu-id="ae35f-145">A desinstalação do hotfix pode não desinstalar determinadas atualizações</span><span class="sxs-lookup"><span data-stu-id="ae35f-145">Hotfix Uninstall might not uninstall certain updates</span></span>

<span data-ttu-id="ae35f-146">Algumas atualizações e service packs não podem ser desinstaladas porque são marcadas como não instaláveis ou porque elas precisam ser desinstaladas dentro do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae35f-146">Some updates and service packs cannot be uninstalled because they are marked as un-installable or because they need to be uninstalled from within Windows 7.</span></span> <span data-ttu-id="ae35f-147">Nesses casos, a ferramenta de desinstalação de hotfix pode indicar que essas atualizações foram desinstaladas, mesmo que não tenham sido.</span><span class="sxs-lookup"><span data-stu-id="ae35f-147">In these instances, the Hotfix Uninstall tool may indicate that these updates have been uninstalled even though they have not been.</span></span>

<span data-ttu-id="ae35f-148">**Solução alternativa:** Desinstale essas atualizações problemáticas do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae35f-148">**Workaround:** Uninstall these problematic updates from Windows 7.</span></span>

### <span data-ttu-id="ae35f-149">Apagamento de disco: discos com volumes estendidos, volumes distribuídos ou volumes espelhados não podem ser excluídos</span><span class="sxs-lookup"><span data-stu-id="ae35f-149">Disk Wipe: Disks with spanned volumes, striped volumes, or mirrored volumes cannot be deleted</span></span>

<span data-ttu-id="ae35f-150">O apagamento de disco não dá suporte à exclusão de discos estendidos, espelhados ou distribuídos em um ou mais volumes.</span><span class="sxs-lookup"><span data-stu-id="ae35f-150">Disk Wipe does not support deleting disks that are spanned, mirrored, or striped across one or more volumes.</span></span>

<span data-ttu-id="ae35f-151">**Solução alternativa:** Selecione e exclua cada disco no volume separadamente.</span><span class="sxs-lookup"><span data-stu-id="ae35f-151">**Workaround:** Select and delete each disk in the volume separately.</span></span>

## <span data-ttu-id="ae35f-152">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="ae35f-152">Release Notes Copyright Information</span></span>


<span data-ttu-id="ae35f-153">Este documento é fornecido "como está".</span><span class="sxs-lookup"><span data-stu-id="ae35f-153">This document is provided “as-is”.</span></span> <span data-ttu-id="ae35f-154">As informações e os modos de exibição expressos neste documento, incluindo URL e outras referências de site da Internet, podem mudar sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="ae35f-154">Information and views expressed in this document, including URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="ae35f-155">Você assume o risco de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ae35f-155">You bear the risk of using it.</span></span>

<span data-ttu-id="ae35f-156">Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios.</span><span class="sxs-lookup"><span data-stu-id="ae35f-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span><span data-ttu-id="ae35f-157">Nenhuma associação ou conexão real é intencional ou deve ser inferida.</span><span class="sxs-lookup"><span data-stu-id="ae35f-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="ae35f-158">Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae35f-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="ae35f-159">Este documento é confidencial e proprietário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae35f-159">This document is confidential and proprietary to Microsoft.</span></span> <span data-ttu-id="ae35f-160">Ele é divulgado e pode ser usado somente mediante um contrato de não divulgação.</span><span class="sxs-lookup"><span data-stu-id="ae35f-160">It is disclosed and can be used only pursuant to a nondisclosure agreement.</span></span>



<span data-ttu-id="ae35f-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae35f-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="ae35f-162">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="ae35f-162">All other trademarks are property of their respective owners.</span></span>

## <span data-ttu-id="ae35f-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae35f-163">Related topics</span></span>


[<span data-ttu-id="ae35f-164">Sobre o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ae35f-164">About DaRT 7.0</span></span>](about-dart-70-new-ia.md)

 

 





