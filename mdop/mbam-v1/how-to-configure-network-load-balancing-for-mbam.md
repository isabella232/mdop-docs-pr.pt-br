---
title: Como configurar os Balanceamento de Carga de Rede para o MBAM
description: Como configurar os Balanceamento de Carga de Rede para o MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799687"
---
# Como configurar os Balanceamento de Carga de Rede para o MBAM


Para verificar se você atendeu os pré-requisitos e requisitos de hardware e software para instalar o recurso de servidor de administração e monitoramento, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).

**Observação**  Para obter os arquivos de log de instalação, você deve instalar o Microsoft BitLocker Administration and Monitoring (MBAM) usando o pacote **msiexec** e a opção de localização **/l** &lt; &gt; . Os arquivos de log são criados no local que você especificar.

Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que instala o MBAM.

 

Os clusters de balanceamento de carga de rede (NLB) do recurso de servidor de administração e monitoramento fornecem escalabilidade no MBAM e devem oferecer suporte a mais de 55.000 computadores cliente do MBAM.

**Observação**  O balanceamento de carga de rede do Windows Server distribui solicitações de cliente em um conjunto de servidores que são configurados em um cluster de servidor único. Quando o balanceamento de carga de rede é instalado em cada um dos servidores (hosts) em um cluster, o cluster apresenta um endereço IP virtual ou FQDN (nome de domínio totalmente qualificado) para solicitações do cliente. As solicitações iniciais do cliente vão para todos os hosts do cluster, mas apenas um host aceita e manipula a solicitação.

Todos os computadores que farão parte de um cluster NLB terão os seguintes requisitos:

-   Todos os computadores no cluster NLB devem estar no mesmo domínio.

-   Cada computador no cluster NLB deve usar um endereço IP estático.

-   Cada computador do cluster NLB deve ter o balanceamento de carga de rede habilitado.

-   O cluster NLB requer um endereço IP estático, e um registro de host deve ser criado manualmente no sistema de nomes de domínio (DNS).

 

## Configurando o balanceamento de carga de rede para servidores de administração e monitoramento MBAM


As etapas a seguir descrevem como configurar um nome virtual e um endereço IP do cluster NLB para dois servidores de administração e monitoramento do MBAM e como configurar clientes do MBAM para usar o cluster NLB.

Antes de começar os procedimentos descritos neste tópico, você deve ter o recurso de servidor de monitoramento e administração do MBAM instalado com êxito usando a mesma associação de porta do IIS em dois computadores de servidor separados que atendam aos pré-requisitos para a instalação de recursos do MBAM Server e a configuração de cluster de NLB.

**Observação**  Este tópico descreve o processo básico de uso do Gerenciador de balanceamento de carga de rede para criar um cluster NLB. As etapas exatas para configurar um servidor Windows como parte de um cluster NLB dependem da versão do Windows Server em uso... Para obter mais informações sobre como criar NLBs em WindowsServer2008, consulte [criando clusters de balanceamento de carga de rede](https://go.microsoft.com/fwlink/?LinkId=197176) na biblioteca do Windows Server2008 technet.

 

**Para configurar um nome virtual e um endereço IP do cluster NLB para dois servidores de administração e monitoramento do MBAM**

1.  Clique em **Iniciar**, em **todos os programas**, em **Ferramentas administrativas**e, em seguida, clique em **Gerenciador de balanceamento de carga de rede**.

    **Observação**  Se o Gerenciador de NLB não estiver presente, você poderá instalá-lo como um recurso do WindowsServer. Você deve instalar esse recurso em servidores de administração e monitoramento do MBAM se quiser configurá-lo para o cluster NLB.

     

2.  Na barra de menus, clique em **cluster**e, em seguida, clique em **novo** para abrir a caixa de diálogo **parâmetros de cluster** .

3.  Na caixa de diálogo **parâmetros de cluster** , insira as informações para a configuração de IP do cluster NLB:

    -   **Endereço IP:** Endereço IP do cluster NLB registrado no DNS

    -   **Máscara de sub-rede:** Máscara de sub-rede do endereço IP do cluster NLB registrada no DNS

    -   **Nome de Internet completo:** FQDN do nome do cluster NLB registrado no DNS

4.  Verifique se **a difusão ponto a ponto** está selecionada no **modo de operação do cluster**e clique em **Avançar**.

5.  Na página **endereços IP do cluster** , clique em **Avançar**.

6.  Na página **regras de porta** , clique em **Editar** para definir as portas para as quais o cluster NLB responderá e configurar as portas usadas para a comunicação de sistema de cliente para site conforme elas são definidas para o site ou clique em **Avançar** para habilitar o endereço IP do cluster NLB para responder a todas as portas TCP/IP.

    **Observação**  Assegure-se de que a **afinidade** esteja definida como **single**.

     

7.  Na página **conectar** , insira um nome de host da instância do MBAM Administration and Monitoring Server que fará parte do cluster NLB no **host**e, em seguida, clique em **conectar**.

8.  Em **interfaces disponíveis para configurar um novo cluster**, selecione a interface de rede que será configurada para responder à comunicação do cluster NLB e clique em **Avançar**.

9.  Na página **parâmetros do host** , revise as informações exibidas para garantir que as configurações de **configuração de IP dedicado** exibam a configuração de IP de host dedicada para o host de cluster NLB correto, verifique se o estado inicial do host do estado **padrão:** é **iniciado**e clique em **concluir**.

    **Observação**  A página **parâmetros do host** também exibe a prioridade do host do cluster NLB, que é de 1 a 32. À medida que novos hosts são adicionados ao cluster NLB, a prioridade do host deve ser diferente dos hosts adicionados anteriormente. A prioridade é incrementada automaticamente quando você usa o Gerenciador de balanceamento de carga de rede.

     

10. Clique em ** &lt; &gt; nome do cluster NLB** e certifique-se de que o **status** da interface do host NLB seja exibido **convergido** antes de continuar. Esta etapa pode exigir que você atualize a exibição do cluster NLB como a configuração de TCP/IP do host que está sendo modificada pelo Gerenciador de NLB.

11. Para adicionar mais hosts ao cluster NLB, clique com o botão direito do mouse em ** &lt; nome &gt; do cluster NLB**, clique em **Adicionar host ao cluster** e repita as etapas 7 a 10 para cada sistema de site que fará parte do cluster NLB.

12. Em um computador que tenha o modelo de política de grupo do MBAM instalado, modifique as configurações da política de grupo do MBAM para configurar os pontos de extremidade dos serviços do MBAM para usar o nome do cluster NLB e a associação de porta do IIS apropriada para acessar os recursos do MBAM de administração e do servidor de monitoramento instalados nos computadores do cluster NLB. Para obter mais informações sobre como editar configurações do GPO MBAM, consulte [como editar configurações de GPO do MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md). Se os servidores de administração e administração do MBAM são novos no seu ambiente, verifique se as associações de grupo de segurança local necessárias foram configuradas corretamente. Para obter mais informações sobre os requisitos de grupo de segurança, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

13. Quando a configuração do cluster NLB estiver concluída, recomendamos que você valide se a administração do MBAM e o monitoramento do cluster NLB funcionam. Para fazer isso, abra um navegador da Web em um computador que não seja o servidor que está configurado no NLB e certifique-se de que você possa acessar o site de administração e monitoramento do MBAM usando o FQDN do NLB.

## Tópicos relacionados


[Implantando a infraestrutura do Servidor do MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





