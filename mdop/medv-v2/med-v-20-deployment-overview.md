---
title: Visão geral da implantação da MED-V 2.0
description: Visão geral da implantação da MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799806"
---
# Visão geral da implantação da MED-V 2.0


Esta seção fornece informações gerais e instruções sobre como instalar e implantar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Visão geral


O MED-V 2,0 se baseia em um modelo de aplicativo, em que os mesmos métodos usados para implantar aplicativos podem ser usados para implantar e gerenciar o MED-V. Uma solução MED-V implantada inclui dois componentes: o agente de host e o agente de convidado do MED-V. O agente de host do MED-V está instalado na área de trabalho do Windows 7 e o agente de convidado do MED-V está instalado no Windows XP dentro do espaço de trabalho do MED-V. O MED-V também inclui um pacote do espaço de trabalho do MED-V que fornece as informações e as ferramentas necessárias para criar e configurar os espaços de trabalho do MED-V.

**Importante**  
O MED-V só oferece suporte à instalação do pacote do espaço de trabalho do MED-V, ao agente de host do MED-V e ao espaço de trabalho do MED-v para todos os usuários. A instalação do MED-V para o usuário atual somente selecionando **ALLUSERS = ""** causa falhas na instalação dos componentes e na configuração do espaço de trabalho do MED-V.



### Os arquivos de instalação do MED-V

O MED-V inclui os seguintes arquivos de instalação, necessários para executar o MED-V:

**O arquivo de instalação do MED-V Host Agent**

O arquivo de instalação do Host Agent é chamado de MED-V\_HostAgent\_Setup.exe. Esse arquivo é distribuído e instalado em cada computador de usuário final relevante como parte de sua implantação de toda a empresa do MED-V.

**O arquivo de instalação do pacote do espaço de trabalho do MED-V**

O arquivo de instalação do pacote do espaço de trabalho do MED-V é chamado MED-V\_WorkspacePackager\_Setup.exe. Use esse arquivo para instalar o pacote do espaço de trabalho do MED-V em um computador no qual você tenha direitos e permissões de administrador. O administrador da área de trabalho usa o pacote do espaço de trabalho do MED-V para criar e gerenciar os espaços de trabalho do MED-V.

**Observação**  
O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.



### O processo de implantação do MED-V

Veja a seguir uma visão geral de alto nível do processo de instalação e implantação do MED-V:

1.  Instale o pacote do espaço de trabalho do MED-V no computador em que você tem credenciais administrativas e que você usará para construir os pacotes do espaço de trabalho do MED-V. Para obter mais informações, consulte [como instalar o pacote do espaço de trabalho do MED-V](how-to-install-the-med-v-workspace-packager.md).

2.  Prepare sua imagem do MED-V e crie seus pacotes de espaço de trabalho do MED-V usando o pacote do espaço de trabalho do MED-V. Para obter mais informações, consulte [operações do MED-V](operations-for-med-v.md).

3.  Implante os componentes do MED-V necessários em toda a sua empresa. Os componentes obrigatórios do MED-V são do Windows Virtual PC, do MED-V Host Agent e do espaço de trabalho do MED-V.

**Importante**  
A instalação dos componentes do MED-V requer credenciais administrativas. Se um usuário final estiver instalando o MED-V, ele será solicitado a inserir credenciais administrativas. Como alternativa, as credenciais administrativas podem ser fornecidas no contexto se você estiver instalando usando um sistema ESD (Electronic Software Distribution).



### Componentes do MED-V

Os componentes do MED-V que você implanta em toda a sua empresa consistem nos seguintes itens:

**PC virtual do Windows**

Funções do MED-V nas imagens do PC virtual do Windows para sua solução de compatibilidade. O PC virtual do Windows e a atualização para Windows 7 (KB977206) são necessários. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

**O arquivo de instalação do MED-V Host Agent**

MED-V\_HostAgent\_Setup.exe.

**Os arquivos de instalação do espaço de trabalho do MED-V**

Os arquivos de instalação do espaço de trabalho do MED-V são criados quando você cria o pacote do espaço de trabalho do MED-v que consiste no seguinte:

Um programa executável setup.exe que executa a instalação do espaço de trabalho do MED-V

Um &lt; instalador do MED-V \ _workspace \ _name &gt; . msi

Um &lt; arquivo VHD \ _filename &gt; . medv, que é o disco rígido virtual compactado

Os arquivos para configurações de configuração ( &lt; espaço de trabalho \ _name &gt; . reg e &lt; espaço de trabalho \ _name &gt; . ps1)

Para implantar o MED-V, copie todos os arquivos de instalação necessários para o computador host ou para um compartilhamento que possa ser acessado pelo computador host. Execute os arquivos de instalação do componente para o PC virtual do Windows, o agente do host do MED-V e o espaço de trabalho do MED-V. Em seguida, inicie o agente do host do MED-V para concluir a configuração inicial do MED-V.

Você pode executar a instalação manualmente. No entanto, recomendamos que você use um método de distribuição de software eletrônico para automatizar a implantação dos componentes. Para obter mais informações, consulte [como implantar um espaço de trabalho do MED-V por meio de um sistema de distribuição de software eletrônico](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).

**Observação**  
Para obter informações sobre argumentos de linha de comando disponíveis para controlar as opções de instalação, consulte [Opções de linha de comando para arquivos de instalação do MED-V](command-line-options-for-med-v-installation-files.md).



## Etapas de implantação


Ao implantar o MED-V em toda a sua empresa, há duas considerações principais: instalação e configuração da primeira vez.

### Instalação

1.  **PC virtual do Windows** -durante a instalação, o MED-V verifica o computador virtual do Windows e a atualização necessária para o Windows 7 (KB977206). Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    Você pode instalá-los como parte das instalações do Windows 7 antes de instalar o MED-V ou pode instalá-los como parte da distribuição do MED-V. No entanto, o MED-V não inclui um mecanismo para a implantação; Elas devem ser implantadas usando um sistema ESD (Electronic Software Distribution) ou parte da imagem do Windows 7.

    **Importante**  
    Ao instalar os componentes do MED-V usando um arquivo em lotes, uma prática recomendada é especificar que o Windows Virtual PC e o hotfix do Windows Virtual PC são instalados após o pacote de host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V. Isso significa que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Agente de host do MED-v** – instale o agente de host do MED-v no computador com Windows 7 em que o MED-v será executado. Isso deve ser instalado antes da instalação do espaço de trabalho do MED-V e verifica se o computador virtual do Windows está instalado.

3. **Espaço de trabalho do MED-v** – você cria os arquivos necessários nesta instalação usando o pacote do espaço de trabalho do MED-v: os arquivos setup.exe,. medv e. msi. Para instalar o espaço de trabalho do MED-V, execute setup.exe; Isso aciona os outros arquivos conforme necessário. A instalação coloca uma entrada no registro sob a chave de execução do computador local para iniciar o agente de host do MED-V, que sempre executa o MED-V quando o Windows for iniciado.

   **Importante**  
   A instalação do espaço de trabalho do MED-V pode ser executada interativamente pelo usuário final ou silenciosamente por meio de um sistema de distribuição de software eletrônico. A instalação do espaço de trabalho do MED-V requer credenciais administrativas, portanto, os usuários finais devem ser administradores de seus computadores para instalar o espaço de trabalho do MED-V. Como alternativa, um sistema de distribuição de software eletrônico geralmente é executado no contexto do sistema e tem permissões suficientes.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### Configuração da primeira vez

Após a instalação do MED-V e dos componentes obrigatórios, o MED-V deve ser configurado. A configuração do MED-V é conhecida como configuração pela primeira vez. Usando o **pacote do espaço de trabalho do MED-V**, você pode configurar a primeira vez que a configuração seja executada silenciosa ou interativamente. A configuração da primeira vez do MED-V exige que os usuários finais insiram a senha para se autenticarem no espaço de trabalho do MED-V, mas, caso contrário, podem ser praticamente invisíveis ao usuário. As notificações são mostradas na área de notificação, como quando a instalação é concluída pela primeira vez e os aplicativos estão prontos. Veja a seguir as ações que ocorrem durante a configuração do MED-V na primeira vez:

1.  O disco rígido virtual deve ser configurado. A mini-instalação é executada e expande a imagem do Windows XP. Geralmente, isso ocorre em uma janela oculta, mas o MED-V pode ser configurado para ser exibido durante essa configuração.

2.  Após a conclusão da mini-instalação, você pode executar comandos que devem ter para configuração adicional, como a instalação do software ESD ou de outros aplicativos ou a configuração da imagem. Elas podem ser chamadas no arquivo Sysprep. inf, mas não são necessárias. Para obter mais informações, consulte [Configurando uma imagem do Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

3.  Ftscompletion.exe é executado como a última etapa na configuração. Esse processo conclui a configuração do MED-V, adiciona o usuário ao grupo RDP para permitir que eles acessem o espaço de trabalho do MED-V, copie os logs, sinalizem o MED-V de que o espaço de trabalho do MED-V está pronto e, em seguida, reinicia o espaço de trabalho do MED-V. Esse processo também pode adicionar o usuário como administrador do espaço de trabalho do MED-V se ele tiver sido configurado quando o espaço de trabalho do MED-V foi criado. Ftscompletion.exe geralmente é chamado pelo arquivo Sysprep, inf, mas também pode ser executado por meio de outro método, como um script. No entanto, Ftscompletion.exe deve ser a última ação que é executada quando a estação de trabalho está configurada. Para obter mais informações, consulte [Configurando uma imagem do Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

4.  Após a reinicialização do espaço de trabalho do MED-V pela Ftscompletion.exe, o usuário final está conectado. Se ele não tiver salvo a senha durante a primeira instalação, ele será solicitado a fazê-lo novamente. O espaço de trabalho do MED-V é iniciado e configurado para o usuário. A configuração inclui a aplicação da política de grupo.

    Recomendamos que você aplique apenas as políticas que fazem sentido em um ambiente de compatibilidade do aplicativo para Windows XP. Por exemplo, as políticas de personalização da área de trabalho normalmente não precisam ser aplicadas e devem ser desabilitadas. Para obter mais informações sobre como permitir somente perfis locais, consulte [configurações de política de grupo para perfis de usuário móvel](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

Depois que a configuração for concluída pela primeira vez, o usuário final será notificado de que os aplicativos publicados estão prontos. Eles poderão, então, acessar os aplicativos instalados no espaço de trabalho do MED-V a partir do menu **Iniciar** .

## Tópicos relacionados


[Preparar o ambiente de implantação para a MED-V](prepare-the-deployment-environment-for-med-v.md)

[Implantação da MED-V](deployment-of-med-v.md)









