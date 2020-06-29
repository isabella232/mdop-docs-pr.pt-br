---
title: Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V
description: Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799643"
---
# <span data-ttu-id="2e5c1-103">Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="2e5c1-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="2e5c1-104">O espaço de trabalho do MED-V é uma máquina virtual que contém um sistema operacional separado, cujo processo de atualização automática de software deve ser gerenciado da mesma forma que os computadores físicos da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="2e5c1-105">Como o sistema operacional convidado nem sempre está sendo executado quando o sistema operacional do host está em execução, você deve garantir que a máquina virtual do MED-V esteja configurada de forma que as atualizações de software possam ser aplicadas ao sistema operacional convidado, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="2e5c1-106">A solução Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fornece a funcionalidade que permite que você determine como as atualizações automáticas de software são processadas em um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="2e5c1-107">Gerenciando política de ativação do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="2e5c1-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="2e5c1-108">A política de ativação do espaço de trabalho do MED-V garante que a máquina virtual do MED-V seja disponibilizada para atualizações durante o tempo especificado nas configurações de configuração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="2e5c1-109">Isso se aplica a ambas as atualizações publicadas da Microsoft por meio do Windows Update e atualizações implantadas e controladas por soluções não-Microsoft, como aplicativos antivírus.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="2e5c1-110">**Importante**  A política de ativação do espaço de trabalho do MED-V é otimizada para a infraestrutura do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="2e5c1-111">Se você estiver usando o Microsoft System Center Configuration Manager para implantar atualizações não Microsoft, recomendamos que você também use o System Center Updates Publisher, que aproveita a mesma infraestrutura que o Microsoft Update e, portanto, benefícios da política de ativação do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="2e5c1-112">Para obter mais informações, consulte o [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="2e5c1-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="2e5c1-113">Quando você criou seu pacote de espaço de trabalho do MED-V, configurou quando e como ele é iniciado, quando o usuário final se conecta (**início rápido**) ou quando o usuário final abre primeiro um aplicativo publicado (**início normal**).</span><span class="sxs-lookup"><span data-stu-id="2e5c1-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="2e5c1-114">Ou você define a opção para permitir que o usuário final controle essa configuração.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="2e5c1-115">De qualquer forma, sempre que a opção de **início rápido** estiver selecionada, a máquina virtual continuará a ser executada, desde que o host do MED-V esteja conectado como usuário.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="2e5c1-116">Nesta configuração, como o MED-V está ativo quando o host está ativo, as atualizações automáticas são aplicadas sem a necessidade de processamento adicional do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="2e5c1-117">No entanto, para os casos em que o **início rápido** não for especificado ou a máquina virtual hibernar ou parar, o MED-v garante por meio da política de ativação do espaço de trabalho do MED-v que o sistema operacional convidado está sendo atualizado regularmente mesmo quando o MED-V não é usado regularmente.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="2e5c1-118">O MED-V executa essa função com a ativação regular da máquina virtual com base nas definições de configuração que você especificar.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="2e5c1-119">Isso permite que os clientes de atualização automática na máquina virtual sejam executados com base nas configurações.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="2e5c1-120">Depois que o período definido pela configuração do MED-V expirar, o MED-V retornará a máquina virtual ao seu estado anterior.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="2e5c1-121">**Observação**  Se o usuário final abrir um aplicativo publicado durante o período de atualização, as atualizações necessárias serão aplicadas, mas o MED-V não será automaticamente hibernado ou desligado após o término do período de atualização.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="2e5c1-122">Em vez disso, o MED-V continua sendo executado.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="2e5c1-123">A política de ativação do espaço de trabalho do MED-V inclui três componentes principais:</span><span class="sxs-lookup"><span data-stu-id="2e5c1-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="2e5c1-124">Gerenciador de atualizações de convidados</span><span class="sxs-lookup"><span data-stu-id="2e5c1-124">Guest Update Manager</span></span>**

<span data-ttu-id="2e5c1-125">De acordo com o host do MED-V, este programa executável autônomo é responsável por ativar a máquina virtual de acordo com uma agenda configurável e predefinida.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="2e5c1-126">Especifique as configurações para indicar em que horário o Gerenciador de atualizações deve ativar a máquina virtual todos os dias e por quanto tempo a máquina virtual deve ser mantida em dia (em minutos) para permitir que as atualizações sejam aplicadas.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="2e5c1-127">Após o número de minutos especificado ter sido atingido, o Gerenciador de atualizações de convidado coloca a máquina virtual em hibernação, preparada para o próximo uso.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="2e5c1-128">Você pode agendar a execução do programa executável por meio do Gerenciador de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="2e5c1-129">Serviço de gerenciamento de reinicialização de convidado</span><span class="sxs-lookup"><span data-stu-id="2e5c1-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="2e5c1-130">Que residem no host do MED-V, esse serviço tem três responsabilidades principais.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="2e5c1-131">Juntamente com o Gerenciador de atualizações de convidado, ele gerencia a reinicialização da máquina virtual ao fazer logon do usuário, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="2e5c1-132">Ele detecta quando a reinicialização da máquina virtual é necessária devido a atualizações instaladas.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="2e5c1-133">E garante que a tarefa para o Gerenciador de atualizações de convidados seja sempre agendada de acordo com a configuração.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="2e5c1-134">Serviço de atualização de convidado</span><span class="sxs-lookup"><span data-stu-id="2e5c1-134">Guest Update Service</span></span>**

<span data-ttu-id="2e5c1-135">Que residem na máquina virtual do MED-V, este serviço do Windows tem a responsabilidade de monitorar quando as atualizações instaladas exigem uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="2e5c1-136">Depois que o serviço se lembrar da necessidade de uma reinicialização, ele notificará o serviço de gerenciamento de reinicialização de convidado no host.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="2e5c1-137">Opções de configuração para a política de ativação do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="2e5c1-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="2e5c1-138">Você controla quando e por quanto tempo o computador virtual é ativado para receber atualizações automáticas definindo os dois valores de configuração a seguir no registro.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="2e5c1-139">Esses dois valores estão localizados na chave HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="2e5c1-140">**GuestUpdateTime** – configura a hora e os minutos todos os dias em que o MED-V deve ativar a máquina virtual para atualização, com base no padrão de relógio de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="2e5c1-141">Especifique a hora no formato HH: MM.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="2e5c1-142">O valor padrão é 00:00 (meia-noite).</span><span class="sxs-lookup"><span data-stu-id="2e5c1-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="2e5c1-143">**GuestUpdateDuration** – configura o número de minutos que o MED-V deve manter a máquina virtual para atualização, começando no momento especificado na configuração GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="2e5c1-144">O valor padrão é 240 (4 horas).</span><span class="sxs-lookup"><span data-stu-id="2e5c1-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="2e5c1-145">Definir esse valor como zero (0) desabilita a política de ativação do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="2e5c1-146">Para obter mais informações sobre como definir os valores de configuração do MED-V, consulte [Gerenciando as configurações do espaço de trabalho do MED-v](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c1-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="2e5c1-147">**Observação**  Uma prática recomendada do MED-V é definir seu intervalo de ativação para corresponder ao tempo em que as máquinas virtuais do MED-V estão planejadas para serem atualizadas regularmente.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="2e5c1-148">Além disso, recomendamos que você defina essas configurações para se parecer com o comportamento do computador host.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="2e5c1-149">Reinicie a notificação usando o seu sistema ESD</span><span class="sxs-lookup"><span data-stu-id="2e5c1-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="2e5c1-150">Você pode configurar seu sistema ESD para notificar o MED-V sempre que uma reinicialização for necessária para o espaço de trabalho do MED-V após a aplicação das atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="2e5c1-151">Quando você aplica atualizações automáticas pelo seu sistema ESD que você sabe que exige uma reinicialização, deve escrever um script para sinalizar o seguinte evento global no espaço de trabalho do MED-V:</span><span class="sxs-lookup"><span data-stu-id="2e5c1-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="2e5c1-152">**Importante**  Você deve abrir o evento com direitos de modificação e, em seguida, sinalizá-lo.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="2e5c1-153">Se você não o abrir com as permissões corretas, isso não funcionará.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="2e5c1-154">Quando você sinaliza esse evento, o MED-V o captura e informa à máquina virtual que é necessária uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="2e5c1-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="2e5c1-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e5c1-155">Related topics</span></span>


[<span data-ttu-id="2e5c1-156">Gerenciamento de atualizações de software para espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="2e5c1-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





