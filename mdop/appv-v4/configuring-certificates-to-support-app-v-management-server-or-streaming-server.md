---
title: Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V
description: Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798017"
---
# <span data-ttu-id="1f2b2-103">Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V</span><span class="sxs-lookup"><span data-stu-id="1f2b2-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="1f2b2-104">Depois de concluir o processo de provisionamento de certificado e alterar as permissões da chave privada para dar suporte à instalação do App-V, você pode iniciar a configuração do servidor de gerenciamento ou do servidor de transmissão.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="1f2b2-105">Durante a configuração, se um certificado for provisionado antes de executar o programa de instalação, o assistente exibirá o certificado na tela **modo de segurança de conexão** e, por padrão, a caixa de seleção **usar segurança aprimorada** estará marcada.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="1f2b2-106">**Observação**  Selecione o certificado que foi configurado para o App-V se houver mais de um certificado provisionado para este servidor.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="1f2b2-107">**Importante**  Durante a atualização da versão 4,2 para a versão 4,5, a configuração tem uma opção para **usar a segurança aprimorada**; no entanto, a seleção dessa opção não desabilitará o streaming em RTSP.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="1f2b2-108">Você deve usar o console de gerenciamento para desabilitar o RTSP após a instalação.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="1f2b2-109">Selecione a porta TCP que o serviço vai usar para comunicações de cliente.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="1f2b2-110">A porta padrão é TCP 322; no entanto, você pode mudar a porta para uma porta personalizada do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="1f2b2-111">As etapas restantes do assistente são as mesmas que se você estivesse implantando um servidor de gerenciamento ou de streaming do App-V sem usar o recurso de **segurança aprimorado** .</span><span class="sxs-lookup"><span data-stu-id="1f2b2-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="1f2b2-112">Configurar certificados para ambientes NLB</span><span class="sxs-lookup"><span data-stu-id="1f2b2-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="1f2b2-113">Para dar suporte a grandes empresas, muitas vezes o servidor de gerenciamento é colocado em um cluster de balanceamento de carga de rede (NLB) para dar suporte ao grande número de conexões.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="1f2b2-114">Isso requer pelo menos dois servidores de gerenciamento que parecem ser um único servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="1f2b2-115">Quando o ambiente usa um cluster NLB com vários servidores de gerenciamento, você precisa de uma configuração avançada do certificado usado para o cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="1f2b2-116">O certificado App-V é enviado a uma autoridade de certificação (CA) configurada em um computador com o Windows Server2003.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="1f2b2-117">A SAN permite que você se conecte a um nome de host de cluster NLB específico do servidor de gerenciamento usando um nome de sistema de nomes de domínio (DNS) que pode ser diferente dos nomes de computador reais, porque pode haver até 32 servidores que compõem o cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="1f2b2-118">Essa configuração é necessária somente ao usar um cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="1f2b2-119">Quando o cliente se conecta ao servidor, ele se conecta usando o nome de domínio totalmente qualificado (FQDN) do cluster NLB e não o FQDN de um servidor individual.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="1f2b2-120">Se você não adicionar a propriedade SAN com o FQDN dos nós do servidor no cluster, todas as conexões do cliente serão recusadas porque o nome comum do certificado não corresponderá ao nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1f2b2-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="1f2b2-121">Para obter informações mais detalhadas sobre a configuração de certificados com o atributo SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="1f2b2-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="1f2b2-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f2b2-122">Related topics</span></span>


[<span data-ttu-id="1f2b2-123">Configuração de certificados para dar suporte ao streaming seguro</span><span class="sxs-lookup"><span data-stu-id="1f2b2-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="1f2b2-124">Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="1f2b2-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





