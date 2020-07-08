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
# Gerenciamento de atualizações automáticas para espaços de trabalho da MED-V


O espaço de trabalho do MED-V é uma máquina virtual que contém um sistema operacional separado, cujo processo de atualização automática de software deve ser gerenciado da mesma forma que os computadores físicos da sua empresa. Como o sistema operacional convidado nem sempre está sendo executado quando o sistema operacional do host está em execução, você deve garantir que a máquina virtual do MED-V esteja configurada de forma que as atualizações de software possam ser aplicadas ao sistema operacional convidado, conforme necessário. A solução Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fornece a funcionalidade que permite que você determine como as atualizações automáticas de software são processadas em um espaço de trabalho do MED-V.

## Gerenciando política de ativação do espaço de trabalho do MED-V


A política de ativação do espaço de trabalho do MED-V garante que a máquina virtual do MED-V seja disponibilizada para atualizações durante o tempo especificado nas configurações de configuração do MED-V. Isso se aplica a ambas as atualizações publicadas da Microsoft por meio do Windows Update e atualizações implantadas e controladas por soluções não-Microsoft, como aplicativos antivírus.

**Importante**  A política de ativação do espaço de trabalho do MED-V é otimizada para a infraestrutura do Microsoft Update. Se você estiver usando o Microsoft System Center Configuration Manager para implantar atualizações não Microsoft, recomendamos que você também use o System Center Updates Publisher, que aproveita a mesma infraestrutura que o Microsoft Update e, portanto, benefícios da política de ativação do espaço de trabalho do MED-V. Para obter mais informações, consulte o [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .

 

Quando você criou seu pacote de espaço de trabalho do MED-V, configurou quando e como ele é iniciado, quando o usuário final se conecta (**início rápido**) ou quando o usuário final abre primeiro um aplicativo publicado (**início normal**). Ou você define a opção para permitir que o usuário final controle essa configuração.

De qualquer forma, sempre que a opção de **início rápido** estiver selecionada, a máquina virtual continuará a ser executada, desde que o host do MED-V esteja conectado como usuário. Nesta configuração, como o MED-V está ativo quando o host está ativo, as atualizações automáticas são aplicadas sem a necessidade de processamento adicional do MED-V.

No entanto, para os casos em que o **início rápido** não for especificado ou a máquina virtual hibernar ou parar, o MED-v garante por meio da política de ativação do espaço de trabalho do MED-v que o sistema operacional convidado está sendo atualizado regularmente mesmo quando o MED-V não é usado regularmente. O MED-V executa essa função com a ativação regular da máquina virtual com base nas definições de configuração que você especificar. Isso permite que os clientes de atualização automática na máquina virtual sejam executados com base nas configurações.Depois que o período definido pela configuração do MED-V expirar, o MED-V retornará a máquina virtual ao seu estado anterior.

**Observação**  Se o usuário final abrir um aplicativo publicado durante o período de atualização, as atualizações necessárias serão aplicadas, mas o MED-V não será automaticamente hibernado ou desligado após o término do período de atualização. Em vez disso, o MED-V continua sendo executado.

 

A política de ativação do espaço de trabalho do MED-V inclui três componentes principais:

**Gerenciador de atualizações de convidados**

De acordo com o host do MED-V, este programa executável autônomo é responsável por ativar a máquina virtual de acordo com uma agenda configurável e predefinida. Especifique as configurações para indicar em que horário o Gerenciador de atualizações deve ativar a máquina virtual todos os dias e por quanto tempo a máquina virtual deve ser mantida em dia (em minutos) para permitir que as atualizações sejam aplicadas. Após o número de minutos especificado ter sido atingido, o Gerenciador de atualizações de convidado coloca a máquina virtual em hibernação, preparada para o próximo uso. Você pode agendar a execução do programa executável por meio do Gerenciador de tarefas do Windows.

**Serviço de gerenciamento de reinicialização de convidado**

Que residem no host do MED-V, esse serviço tem três responsabilidades principais. Juntamente com o Gerenciador de atualizações de convidado, ele gerencia a reinicialização da máquina virtual ao fazer logon do usuário, se for necessário. Ele detecta quando a reinicialização da máquina virtual é necessária devido a atualizações instaladas. E garante que a tarefa para o Gerenciador de atualizações de convidados seja sempre agendada de acordo com a configuração.

**Serviço de atualização de convidado**

Que residem na máquina virtual do MED-V, este serviço do Windows tem a responsabilidade de monitorar quando as atualizações instaladas exigem uma reinicialização. Depois que o serviço se lembrar da necessidade de uma reinicialização, ele notificará o serviço de gerenciamento de reinicialização de convidado no host.

### Opções de configuração para a política de ativação do espaço de trabalho do MED-V

Você controla quando e por quanto tempo o computador virtual é ativado para receber atualizações automáticas definindo os dois valores de configuração a seguir no registro. Esses dois valores estão localizados na chave HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.

**GuestUpdateTime** – configura a hora e os minutos todos os dias em que o MED-V deve ativar a máquina virtual para atualização, com base no padrão de relógio de 24 horas. Especifique a hora no formato HH: MM. O valor padrão é 00:00 (meia-noite).

**GuestUpdateDuration** – configura o número de minutos que o MED-V deve manter a máquina virtual para atualização, começando no momento especificado na configuração GuestUpdateTime. O valor padrão é 240 (4 horas). Definir esse valor como zero (0) desabilita a política de ativação do espaço de trabalho do MED-V.

Para obter mais informações sobre como definir os valores de configuração do MED-V, consulte [Gerenciando as configurações do espaço de trabalho do MED-v](managing-med-v-workspace-configuration-settings.md).

**Observação**  Uma prática recomendada do MED-V é definir seu intervalo de ativação para corresponder ao tempo em que as máquinas virtuais do MED-V estão planejadas para serem atualizadas regularmente. Além disso, recomendamos que você defina essas configurações para se parecer com o comportamento do computador host.

 

### Reinicie a notificação usando o seu sistema ESD

Você pode configurar seu sistema ESD para notificar o MED-V sempre que uma reinicialização for necessária para o espaço de trabalho do MED-V após a aplicação das atualizações automáticas. Quando você aplica atualizações automáticas pelo seu sistema ESD que você sabe que exige uma reinicialização, deve escrever um script para sinalizar o seguinte evento global no espaço de trabalho do MED-V:

**Importante**  Você deve abrir o evento com direitos de modificação e, em seguida, sinalizá-lo. Se você não o abrir com as permissões corretas, isso não funcionará.

 

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

Quando você sinaliza esse evento, o MED-V o captura e informa à máquina virtual que é necessária uma reinicialização.

## Tópicos relacionados


[Gerenciamento de atualizações de software para espaços de trabalho da MED-V](managing-software-updates-for-med-v-workspaces.md)

 

 





