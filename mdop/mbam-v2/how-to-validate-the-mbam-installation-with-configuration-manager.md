---
title: Como validar a instalação do MBAM com o Configuration Manager
description: Como validar a instalação do MBAM com o Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799112"
---
# <span data-ttu-id="6de11-103">Como validar a instalação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6de11-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="6de11-104">Depois de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) com o Configuration Manager, valide se a instalação configurou com êxito todos os recursos necessários para o MBAM completando as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6de11-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="6de11-105">Para validar a instalação do recurso do servidor MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6de11-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="6de11-106">No servidor em que o System Center Configuration Manager está implantado, abra o **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="6de11-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="6de11-107">Selecione o programa que é usado para desinstalar ou alterar um programa.</span><span class="sxs-lookup"><span data-stu-id="6de11-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="6de11-108">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos na lista de programas e recursos.</span><span class="sxs-lookup"><span data-stu-id="6de11-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="6de11-109">**Observação**  Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="6de11-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="6de11-110">Use o console do Configuration Manager para confirmar se uma nova coleção, chamada "computadores com suporte para MBAM", é exibida.</span><span class="sxs-lookup"><span data-stu-id="6de11-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="6de11-111">Para exibir a coleção com o Configuration Manager 2007: clique em **banco de dados do site** ( &lt; **Sitecom** &gt;  -  &lt; **nome_do_servidor** &gt; , &lt; **SiteName** &gt; ), gerenciamento do **computador**.</span><span class="sxs-lookup"><span data-stu-id="6de11-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="6de11-112">Para exibir a coleção com SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **conjuntos de dispositivos**.</span><span class="sxs-lookup"><span data-stu-id="6de11-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="6de11-113">Use o console do Configuration Manager para verificar se os seguintes relatórios estão listados na pasta **MBAM** :</span><span class="sxs-lookup"><span data-stu-id="6de11-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="6de11-114">Conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="6de11-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="6de11-115">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="6de11-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="6de11-116">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="6de11-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="6de11-117">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="6de11-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="6de11-118">Para exibir os relatórios com o Configuration Manager 2007: clique em **relatórios**, **serviços de relatório**, \ \ \ \ &lt; **nomedoservidor** &gt; , **pastas de relatório**</span><span class="sxs-lookup"><span data-stu-id="6de11-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="6de11-119">Para exibir os relatórios com o SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **monitoramento** , **relatórios**e **relatórios**.</span><span class="sxs-lookup"><span data-stu-id="6de11-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="6de11-120">Use o console do Configuration Manager para confirmar se a linha de base de configuração "proteção BitLocker" está listada.</span><span class="sxs-lookup"><span data-stu-id="6de11-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="6de11-121">Para exibir as linhas de base de configuração com o Configuration Manager 2007: clique em **Gerenciamento de configuração desejado**, em **linhas de base de configuração**.</span><span class="sxs-lookup"><span data-stu-id="6de11-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="6de11-122">Para exibir as linhas de base de configuração com o SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **configurações de conformidade**, **linhas de base de configuração**.</span><span class="sxs-lookup"><span data-stu-id="6de11-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="6de11-123">Use o console do Configuration Manager para confirmar se os seguintes itens de configuração novos são exibidos:</span><span class="sxs-lookup"><span data-stu-id="6de11-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="6de11-124">Proteção de unidades de dados fixas do BitLocker</span><span class="sxs-lookup"><span data-stu-id="6de11-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="6de11-125">Proteção de unidade do sistema operacional BitLocker</span><span class="sxs-lookup"><span data-stu-id="6de11-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="6de11-126">Para exibir os itens de configuração com o Configuration Manager 2007: clique em **Gerenciamento de configuração desejado**, **itens de configuração**.</span><span class="sxs-lookup"><span data-stu-id="6de11-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="6de11-127">Para exibir os itens de configuração com SystemCenter2012 ConfigurationManager: clique no espaço de trabalho **ativos e conformidade** , **configurações de conformidade**, **itens de configuração**.</span><span class="sxs-lookup"><span data-stu-id="6de11-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="6de11-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6de11-128">Related topics</span></span>


[<span data-ttu-id="6de11-129">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6de11-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





