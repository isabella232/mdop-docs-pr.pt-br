---
title: Como instalar a atualização de idioma do MBAM em servidores distribuídos
description: Como instalar a atualização de idioma do MBAM em servidores distribuídos
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799724"
---
# <span data-ttu-id="d8d5f-103">Como instalar a atualização de idioma do MBAM em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="d8d5f-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="d8d5f-104">O monitoramento e administração do Microsoft BitLocker (MBAM) inclui quatro funções de servidor que podem ser executadas em um ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="d8d5f-105">No entanto, somente dois recursos do MBAM Server exigem a atualização para dar suporte à instalação da versão de idioma do MBAM 1,0 e do modelo de política de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="d8d5f-106">Em configurações com os recursos do MBAM Server instalados em vários computadores, somente os seguintes recursos do servidor precisam ser atualizados:</span><span class="sxs-lookup"><span data-stu-id="d8d5f-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="d8d5f-107">A conformidade e os relatórios de auditoria do MBAM</span><span class="sxs-lookup"><span data-stu-id="d8d5f-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="d8d5f-108">O servidor de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="d8d5f-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="d8d5f-109">**Importante**  Os recursos do servidor do MBAM devem ser atualizados nesta ordem: primeiro os relatórios de conformidade e auditoria e, em seguida, o servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="d8d5f-110">Os modelos de política de grupo do MBAM podem ser atualizados a qualquer momento, sem preocupação com a sequência.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="d8d5f-111">Para instalar a atualização de idioma do MBAM no recurso servidor de relatório de auditoria e conformidade do MBAM</span><span class="sxs-lookup"><span data-stu-id="d8d5f-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="d8d5f-112">No computador que executa o recurso de relatório conformidade e auditoria do MBAM, localize e execute o assistente de configuração de atualização de idioma do MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="d8d5f-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="d8d5f-113">Conclua o assistente para os relatórios de conformidade e auditoria e, em seguida, feche o assistente.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="d8d5f-114">Para instalar a atualização de idioma do MBAM no recurso de servidor administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="d8d5f-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="d8d5f-115">No computador que está executando o recurso de administração e monitoramento do MBAM, abra o console de gerenciamento dos serviços de informações da Internet (IIS), vá para **sites**e, em seguida, desligue o site de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="d8d5f-116">Escolha Editar as associações para o site do MBAM e modifique as associações do site.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="d8d5f-117">Por exemplo, altere a porta de 443 para 9443.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="d8d5f-118">Localize e execute o assistente de configuração de atualização de idioma do MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="d8d5f-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="d8d5f-119">Conclua o assistente para o recurso de administração e monitoramento do servidor e, em seguida, feche o assistente.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="d8d5f-120">Após atualizar o banco de dados do servidor, abra o console de gerenciamento do IIS e examine as associações do site de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="d8d5f-121">Exclua a associação antiga e certifique-se de que a associação restante tenha o nome de host, certificado e número de porta corretos para a configuração empresarial do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="d8d5f-122">Reinicie o site da MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="d8d5f-123">Teste a funcionalidade do site da Web do MBAM:</span><span class="sxs-lookup"><span data-stu-id="d8d5f-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="d8d5f-124">Abra a interface da Web do MBAM e certifique-se de que você possa obter uma chave de recuperação para um cliente.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="d8d5f-125">Impor a criptografia de um computador cliente novo ou manualmente descriptografado.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="d8d5f-126">**Observação**  O cliente MBAM será aberto apenas se puder se comunicar com o banco de dados de recuperação e de hardware.</span><span class="sxs-lookup"><span data-stu-id="d8d5f-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="d8d5f-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8d5f-127">Related topics</span></span>


[<span data-ttu-id="d8d5f-128">Implantação da Atualização da Versão de Idioma do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d8d5f-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





