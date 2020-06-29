---
title: Como instalar o Application Virtualization Streaming Server
description: Como instalar o Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797103"
---
# <span data-ttu-id="48c65-103">Como instalar o Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="48c65-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="48c65-104">O servidor de streaming do Application Virtualization publica seus aplicativos para os clientes.</span><span class="sxs-lookup"><span data-stu-id="48c65-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="48c65-105">Em um ambiente de carga balanceada, que é típico de implantações grandes, todos os servidores em um grupo de servidores devem transmitir os mesmos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="48c65-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="48c65-106">Se os servidores de streaming do Application Virtualization forem para transmitir diferentes aplicativos, atribua-os a grupos de servidores diferentes.</span><span class="sxs-lookup"><span data-stu-id="48c65-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="48c65-107">Nesse caso, você também pode ter que aumentar a capacidade de um grupo de servidor.</span><span class="sxs-lookup"><span data-stu-id="48c65-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="48c65-108">Se você tiver designado um computador de destino na rede, com uma conta de logon com privilégios administrativos locais, poderá usar o procedimento a seguir para instalar o servidor de streaming do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.</span><span class="sxs-lookup"><span data-stu-id="48c65-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="48c65-109">**Observação**  O assistente de instalação pode criar um registro de grupo do servidor, se ele não existir, e um registro da associação do servidor de transmissão do Application Virtualization nesse grupo.</span><span class="sxs-lookup"><span data-stu-id="48c65-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="48c65-110">Depois de concluir o processo de instalação, reinicie o servidor.</span><span class="sxs-lookup"><span data-stu-id="48c65-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="48c65-111">Para instalar um servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="48c65-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="48c65-112">Verifique se nenhuma versão anterior do servidor de streaming do Application Virtualization está instalada em seu computador de destino.</span><span class="sxs-lookup"><span data-stu-id="48c65-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="48c65-113">**Importante**  Verifique se o servidor de gerenciamento do App-V não está instalado neste computador.</span><span class="sxs-lookup"><span data-stu-id="48c65-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="48c65-114">Os dois produtos não podem ser instalados no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="48c65-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="48c65-115">Navegue até o local do programa de configuração do sistema virtualização do aplicativo na rede, execute esse programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="48c65-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="48c65-116">Na página de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="48c65-117">Na página **contrato de licença** , para aceitar os termos de licença, selecione **aceito os termos e as condições de licenciamento**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="48c65-118">Na página **informações do cliente** , especifique o **nome de usuário** e a organização e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="48c65-119">Na página **caminho de instalação** , clique em **procurar**, especifique o local onde você deseja instalar o servidor de streaming e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="48c65-120">Na página **modo de segurança de conexão** , selecione o certificado desejado na lista suspensa e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="48c65-121">**Observação**  A configuração do **modo de conexão segura** exige que o servidor tenha um certificado do servidor provisionado para ele de uma infraestrutura de chave pública.</span><span class="sxs-lookup"><span data-stu-id="48c65-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="48c65-122">Se um certificado do servidor não estiver instalado no servidor, essa opção não estará disponível e não poderá ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="48c65-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="48c65-123">Você deve conceder acesso de leitura à conta de serviço de rede para o certificado que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="48c65-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="48c65-124">Na página **configuração de porta TCP** , para usar a porta padrão (554), selecione **usar porta padrão (554)**.</span><span class="sxs-lookup"><span data-stu-id="48c65-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="48c65-125">Para especificar uma porta personalizada, selecione **usar porta personalizada**, especifique o número da porta no campo fornecido e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="48c65-126">**Observação**  Ao instalar o servidor em um cenário não seguro, você pode usar a porta padrão (554) ou pode definir uma porta personalizada.</span><span class="sxs-lookup"><span data-stu-id="48c65-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="48c65-127">Na página **raiz do conteúdo** , especifique o local no computador de destino onde os arquivos do SFT serão salvos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="48c65-128">**Observação**  Se a porta HTTP ou RTSP do servidor de streaming de aplicativo virtual já estiver alocada, você será solicitado a selecionar uma nova porta.</span><span class="sxs-lookup"><span data-stu-id="48c65-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="48c65-129">Especifique a porta desejada e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="48c65-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="48c65-130">Na tela **Configurações avançadas** , insira as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="48c65-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="48c65-131">Máximo de conexões de cliente</span><span class="sxs-lookup"><span data-stu-id="48c65-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="48c65-132">Tempo limite de conexão (s)</span><span class="sxs-lookup"><span data-stu-id="48c65-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="48c65-133">Tamanho do pool de thread RTSP</span><span class="sxs-lookup"><span data-stu-id="48c65-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="48c65-134">Tempo limite RTSP (s)</span><span class="sxs-lookup"><span data-stu-id="48c65-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="48c65-135">Número de processos básicos</span><span class="sxs-lookup"><span data-stu-id="48c65-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="48c65-136">Tempo limite do núcleo (s)</span><span class="sxs-lookup"><span data-stu-id="48c65-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="48c65-137">Habilitar a autenticação do usuário</span><span class="sxs-lookup"><span data-stu-id="48c65-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="48c65-138">Habilitar a autorização do usuário</span><span class="sxs-lookup"><span data-stu-id="48c65-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="48c65-139">Tamanho do bloco do cache (KB)</span><span class="sxs-lookup"><span data-stu-id="48c65-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="48c65-140">Tamanho máximo de cache (MB)</span><span class="sxs-lookup"><span data-stu-id="48c65-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="48c65-141">**Observação**  O servidor de streaming App-V usa permissões do sistema de arquivos NTFS para controlar o acesso aos aplicativos no compartilhamento de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="48c65-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="48c65-142">Use **habilitar a autenticação do usuário** e **habilitar a autorização do usuário** para controlar se o servidor verifica e impõe essas listas de controle de acesso (ACLs) ou não.</span><span class="sxs-lookup"><span data-stu-id="48c65-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="48c65-143">Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="48c65-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="48c65-144">Na tela **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="48c65-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="48c65-145">**Importante**  A instalação pode demorar vários minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="48c65-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="48c65-146">Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando que a instalação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="48c65-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="48c65-147">Não é necessário reiniciar o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="48c65-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="48c65-148">No entanto, para otimizar o desempenho do sistema, recomendamos uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="48c65-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="48c65-149">Repita as etapas de 1 a 12 para cada servidor de aplicativos virtual que você precisa instalar.</span><span class="sxs-lookup"><span data-stu-id="48c65-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="48c65-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48c65-150">Related topics</span></span>


[<span data-ttu-id="48c65-151">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="48c65-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





