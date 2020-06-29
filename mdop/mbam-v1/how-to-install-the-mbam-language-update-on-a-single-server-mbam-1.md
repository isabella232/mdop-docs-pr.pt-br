---
title: Como instalar a atualização de idiomas do MBAM em um servidor único
description: Como instalar a atualização de idiomas do MBAM em um servidor único
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799535"
---
# <span data-ttu-id="2a0fe-103">Como instalar a atualização de idiomas do MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="2a0fe-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="2a0fe-104">O monitoramento e administração do Microsoft BitLocker (MBAM) inclui quatro funções de servidor que podem ser executadas em um ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="2a0fe-105">No entanto, somente dois recursos do MBAM Server exigem a atualização para suportar a instalação da versão de idioma do MBAM 1,0 e o modelo de política de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="2a0fe-106">Para atualizar todos os três recursos de MBAM necessários a serem instalados em um computador, execute as etapas descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="2a0fe-107">Para instalar a atualização de idioma do MBAM em um único servidor</span><span class="sxs-lookup"><span data-stu-id="2a0fe-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="2a0fe-108">Abra o console de gerenciamento dos serviços de informações da Internet (IIS), vá para **sites**e, em seguida, desligue o site de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="2a0fe-109">Edite as associações do site do MBAM e modifique temporariamente as associações do site.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="2a0fe-110">Por exemplo, altere a porta de 443 para 9443.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="2a0fe-111">Localize e execute o assistente de configuração do MBAM (MBAMsetup.exe) e selecione os três recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2a0fe-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="2a0fe-112">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="2a0fe-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="2a0fe-113">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="2a0fe-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="2a0fe-114">Modelos de política de grupo</span><span class="sxs-lookup"><span data-stu-id="2a0fe-114">Group Policy Templates</span></span>

    <span data-ttu-id="2a0fe-115">**Importante**  Os recursos do servidor do MBAM devem ser atualizados na seguinte ordem: relatórios de conformidade e auditoria primeiro, administração e monitoramento do servidor.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="2a0fe-116">Os modelos de política de grupo podem ser atualizados a qualquer momento, sem preocupação com a sequência.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="2a0fe-117">Após atualizar o banco de dados do servidor, abra o console de gerenciamento do IIS e examine as associações do site de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="2a0fe-118">Exclua uma das associações e certifique-se de que a associação restante tenha o nome de host, certificado e número de porta corretos para a configuração empresarial do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="2a0fe-119">Reinicie o site do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="2a0fe-120">Teste a funcionalidade do site do MBAM:</span><span class="sxs-lookup"><span data-stu-id="2a0fe-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="2a0fe-121">Abra a interface da Web do MBAM e verifique se é possível buscar uma chave de recuperação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="2a0fe-122">Impor a criptografia de um computador cliente novo ou manualmente descriptografado.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="2a0fe-123">**Observação**  O cliente MBAM será aberto apenas se puder se comunicar com o banco de dados de recuperação e de hardware.</span><span class="sxs-lookup"><span data-stu-id="2a0fe-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="2a0fe-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a0fe-124">Related topics</span></span>


[<span data-ttu-id="2a0fe-125">Implantação da Atualização da Versão de Idioma do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2a0fe-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





