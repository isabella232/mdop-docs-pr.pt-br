---
title: Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming
description: Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797043"
---
# <span data-ttu-id="c2a6b-103">Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="c2a6b-103">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>


<span data-ttu-id="c2a6b-104">Para dar suporte a uma instalação mais segura do App-V, você pode usar os procedimentos a seguir para modificar as chaves privadas no Windows Server2003 ou no Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-104">To support a more secure App-V installation, you can use the following procedures to modify private keys in either Windows Server2003 or Windows Server2008.</span></span> <span data-ttu-id="c2a6b-105">Para modificar as permissões da chave privada, você pode usar a ferramenta Windows Server2003 Resource Kit `WinHttpCertCfg.exe` .</span><span class="sxs-lookup"><span data-stu-id="c2a6b-105">To modify the permissions of the private key, you can use the Windows Server2003 Resource Kit tool `WinHttpCertCfg.exe`.</span></span>

<span data-ttu-id="c2a6b-106">Para o Windows Server2003, o procedimento requer que um certificado que atenda aos pré-requisitos listados neste documento seja instalado no computador ou nos computadores nos quais você vai instalar o gerenciamento do App-V ou o Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-106">For Windows Server2003, the procedure requires that a certificate that meets the prerequisites listed in this document is installed on the computer or computers on which you will install the App-V Management or Streaming Server.</span></span> <span data-ttu-id="c2a6b-107">Informações adicionais sobre como usar a `WinHttpCertCfg.exe` ferramenta estão disponíveis em <https://go.microsoft.com/fwlink/?LinkId=151981> .</span><span class="sxs-lookup"><span data-stu-id="c2a6b-107">Additional information about using the `WinHttpCertCfg.exe` tool is available at <https://go.microsoft.com/fwlink/?LinkId=151981>.</span></span>

<span data-ttu-id="c2a6b-108">No Windows Server2008, o processo de alteração das ACLs na chave privada é muito mais simples.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-108">In Windows Server2008, the process of changing the ACLs on the private key is much simpler.</span></span> <span data-ttu-id="c2a6b-109">A interface do usuário do certificado pode ser usada para gerenciar permissões de chave privada.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-109">The certificate’s user interface can be used to manage private key permissions.</span></span>

<span data-ttu-id="c2a6b-110">**Observação**  O contexto de segurança padrão é serviço de rede; no entanto, uma conta de domínio pode ser usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-110">**Note** The default security context is Network Service; however, a domain account can be used instead.</span></span>

 

**<span data-ttu-id="c2a6b-111">Para gerenciar chaves privadas no Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="c2a6b-111">To manage private keys in Windows Server2003</span></span>**

1.  <span data-ttu-id="c2a6b-112">No computador que se tornará o servidor de gerenciamento ou de streaming do App-V, digite o seguinte comando em um prompt de comando para listar as permissões atuais atribuídas a um certificado específico:</span><span class="sxs-lookup"><span data-stu-id="c2a6b-112">On the computer that will become the App-V Management or Streaming Server, type the following command in a command prompt to list the current permissions assigned to a specific certificate:</span></span>

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  <span data-ttu-id="c2a6b-113">Se necessário, modifique as permissões do certificado para fornecer acesso de leitura ao contexto de segurança que será usado para o serviço de gerenciamento ou streaming:</span><span class="sxs-lookup"><span data-stu-id="c2a6b-113">If necessary, modify the permissions of the certificate to provide read access to the security context that will be used for Management or Streaming Service:</span></span>

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  <span data-ttu-id="c2a6b-114">Verifique se o contexto de segurança foi adicionado corretamente listando as permissões no certificado:</span><span class="sxs-lookup"><span data-stu-id="c2a6b-114">Verify that the security context was properly added by listing the permissions on the certificate:</span></span>

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**<span data-ttu-id="c2a6b-115">Para gerenciar chaves privadas no Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="c2a6b-115">To manage private keys in Windows Server2008</span></span>**

1.  <span data-ttu-id="c2a6b-116">Crie um MMC (console de gerenciamento Microsoft) com o snap-in de *certificados* que direciona o repositório de certificados do *computador local* .</span><span class="sxs-lookup"><span data-stu-id="c2a6b-116">Create a Microsoft Management Console (MMC) with the *Certificates* snap-in that targets the *Local Machine* certificate store.</span></span>

2.  <span data-ttu-id="c2a6b-117">Expanda o MMC e selecione **gerenciar chaves privadas**.</span><span class="sxs-lookup"><span data-stu-id="c2a6b-117">Expand the MMC and select **Manage Private Keys**.</span></span>

3.  <span data-ttu-id="c2a6b-118">Na guia **segurança** , adicione a conta de **serviço de rede** com acesso de **leitura** .</span><span class="sxs-lookup"><span data-stu-id="c2a6b-118">On the **Security** tab, add the **Network Service** account with **Read** access.</span></span>

## <span data-ttu-id="c2a6b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2a6b-119">Related topics</span></span>


[<span data-ttu-id="c2a6b-120">Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V</span><span class="sxs-lookup"><span data-stu-id="c2a6b-120">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[<span data-ttu-id="c2a6b-121">Configuração de certificados para dar suporte ao streaming seguro</span><span class="sxs-lookup"><span data-stu-id="c2a6b-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

 

 





