---
title: Como gerenciar a compatibilidade de hardware
description: Como gerenciar a compatibilidade de hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796136"
---
# <span data-ttu-id="835f8-103">Como gerenciar a compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="835f8-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="835f8-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) podem coletar informações sobre o fabricante e o modelo de computadores cliente após a implantação da política de grupo permitir verificação de compatibilidade de hardware.</span><span class="sxs-lookup"><span data-stu-id="835f8-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="835f8-105">Se você configurar essa política, o agente MBAM relata as informações do modelo e do modelo do computador ao servidor MBAM quando o cliente MBAM é implantado em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="835f8-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="835f8-106">O recurso de compatibilidade de hardware é útil quando sua organização tem hardware de computador ou computadores mais antigos que não dão suporte a chips do Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="835f8-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="835f8-107">Nesses casos, você pode usar o recurso de compatibilidade de hardware para garantir que a criptografia do BitLocker seja aplicada somente a modelos de computador que o dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="835f8-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="835f8-108">Se todos os computadores da sua organização forem compatíveis com o BitLocker, você não precisará usar o recurso de compatibilidade de hardware.</span><span class="sxs-lookup"><span data-stu-id="835f8-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="835f8-109">**Observação**  Por padrão, o recurso de compatibilidade de hardware do MBAM não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="835f8-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="835f8-110">Para habilitá-lo, selecione o recurso de **compatibilidade de hardware** no recurso do **servidor de administração e monitoramento** durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="835f8-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="835f8-111">Para obter mais informações sobre como configurar e configurar a compatibilidade de hardware, consulte [implantando a infraestrutura de servidor do MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="835f8-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="835f8-112">O recurso de compatibilidade de hardware funciona da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="835f8-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="835f8-113">O agente cliente do MBAM descobre informações básicas do computador, como fabricante, modelo, fabricante do BIOS, versão do BIOS, criador do TPM e versão do TPM e, em seguida, passa essas informações para o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="835f8-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="835f8-114">O MBAM Server gera uma lista de componentes e modelos de computador cliente para permitir que você Diferencie entre aqueles que podem ou não dar suporte ao BitLocker</span><span class="sxs-lookup"><span data-stu-id="835f8-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="835f8-115">Os agentes do cliente MBAM implantados na empresa atualizam automaticamente essa lista com todos os novos computadores e modelos que são descobertos com um estado **desconhecido**.</span><span class="sxs-lookup"><span data-stu-id="835f8-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="835f8-116">Em seguida, um administrador pode usar o site de administração do MBAM para alterar as entradas de lista para especificar uma marca e um modelo de computador específico como **compatível** ou **incompatível**.</span><span class="sxs-lookup"><span data-stu-id="835f8-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="835f8-117">Antes de o agente do cliente MBAM começar a criptografar uma unidade, o agente verifica primeiro a compatibilidade de criptografia do BitLocker do hardware em que ele está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="835f8-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="835f8-118">Se o hardware estiver marcado como compatível, o processo de criptografia do BitLocker será iniciado.</span><span class="sxs-lookup"><span data-stu-id="835f8-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="835f8-119">O MBAM também verificará novamente o status de compatibilidade de hardware do computador uma vez por dia.</span><span class="sxs-lookup"><span data-stu-id="835f8-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="835f8-120">Se o hardware estiver marcado como incompatível, o agente registrará um evento e passará um estado de "hardware isento" como parte do relatório de conformidade.</span><span class="sxs-lookup"><span data-stu-id="835f8-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="835f8-121">O agente verifica a cada sete dias para ver se o estado mudou para "compatível".</span><span class="sxs-lookup"><span data-stu-id="835f8-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="835f8-122">Se o hardware estiver marcado como desconhecido, o processo de criptografia do BitLocker não será iniciado.</span><span class="sxs-lookup"><span data-stu-id="835f8-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="835f8-123">O agente cliente do MBAM verificará novamente o status de compatibilidade de hardware do computador uma vez por dia.</span><span class="sxs-lookup"><span data-stu-id="835f8-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="835f8-124">**Aviso**  Se o agente cliente do MBAM tentar criptografar um computador que não dá suporte à criptografia de unidade de disco BitLocker, há uma possibilidade de que o computador seja corrompido.</span><span class="sxs-lookup"><span data-stu-id="835f8-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="835f8-125">Verifique se o recurso de compatibilidade de hardware está configurado corretamente quando a sua organização tiver hardware mais antigo que não dê suporte ao BitLocker.</span><span class="sxs-lookup"><span data-stu-id="835f8-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="835f8-126">Para gerenciar a compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="835f8-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="835f8-127">Abra um navegador da Web e navegue até o site de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="835f8-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="835f8-128">Selecione **hardware** na barra de menus à esquerda.</span><span class="sxs-lookup"><span data-stu-id="835f8-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="835f8-129">No painel direito, clique em **pesquisa avançada**e, em seguida, em filtrar para exibir uma lista de todos os modelos de computador que têm um status de **funcionalidade** **desconhecido**.</span><span class="sxs-lookup"><span data-stu-id="835f8-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="835f8-130">Uma lista de modelos de computador que correspondem aos critérios de pesquisa será exibida.</span><span class="sxs-lookup"><span data-stu-id="835f8-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="835f8-131">Os administradores podem adicionar, editar ou remover novos tipos de computador desta página.</span><span class="sxs-lookup"><span data-stu-id="835f8-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="835f8-132">Examine cada configuração de hardware desconhecida para determinar se a configuração deve ser definida como **compatível** ou **incompatível**.</span><span class="sxs-lookup"><span data-stu-id="835f8-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="835f8-133">Selecione uma ou mais linhas e, em seguida, clique em **definir como compatível** ou **definir incompatível** para definir a compatibilidade do BitLocker, conforme apropriado, para os modelos de computador selecionados.</span><span class="sxs-lookup"><span data-stu-id="835f8-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="835f8-134">Se definido como **compatível**, o BitLocker tenta impor uma política de criptografia de unidade em computadores que correspondam ao modelo com suporte.</span><span class="sxs-lookup"><span data-stu-id="835f8-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="835f8-135">Se definido como **incompatível**, o BitLocker não impedirá a política de criptografia de unidade nesses computadores.</span><span class="sxs-lookup"><span data-stu-id="835f8-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="835f8-136">**Observação**  Depois de definir um modelo de computador como compatível, ele pode levar mais de vinte a quatro horas para o cliente MBAM iniciar a criptografia do BitLocker nos computadores que correspondem ao modelo de hardware.</span><span class="sxs-lookup"><span data-stu-id="835f8-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="835f8-137">Os administradores devem monitorar regularmente a lista de compatibilidade de hardware para examinar os novos modelos descobertos pelo agente do MBAM e, em seguida, atualizar sua configuração de compatibilidade para **compatível** ou **incompatível** conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="835f8-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="835f8-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="835f8-138">Related topics</span></span>


[<span data-ttu-id="835f8-139">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="835f8-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





