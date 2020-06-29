---
title: Práticas recomendadas da MED-V 2.0
description: Práticas recomendadas da MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799807"
---
# Práticas recomendadas da MED-V 2.0


Quando estiver planejando, implantando e gerenciando o MED-V na sua empresa, você poderá encontrar as recomendações de práticas recomendadas para ser útil.

### Configurar a primeira vez a instalação para ser executada de forma autônoma

Embora você possa especificar as configurações de sua preferência, uma prática recomendada do MED-V é criar o arquivo Sysprep. inf para que a configuração inicial possa ser executada no modo **autônomo** . Isso exige que você forneça todas as informações de configurações necessárias ao continuar usando o assistente do **Gerenciador de instalação** . Para obter mais informações sobre como configurar a imagem do MED-V, consulte [Configurando uma imagem do Windows Virtual PC para med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Desabilitar pontos de restauração na máquina virtual

Antes de criar o pacote do espaço de trabalho do MED-V, recomendamos que você desabilite os pontos de restauração na máquina virtual para impedir que o disco diferencial aumente não associado. Para obter mais informações, consulte [como desativar e ativar a restauração do sistema no Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

### Configurar a imagem do MED-V para usar perfis locais

Recomendamos que você aplique apenas as políticas que fazem sentido em um ambiente de compatibilidade do aplicativo para Windows XP. Por exemplo, as políticas de personalização da área de trabalho geralmente não precisam ser aplicadas e devem ser desabilitadas. Para obter mais informações sobre como permitir somente perfis locais, consulte [configurações de política de grupo para perfis de usuário móvel](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

### Configurar uma atualização de desempenho da política de grupo

Por padrão, a política de grupo é baixada para um computador, um byte de cada vez. Isso causa atrasos quando o MED-V está sendo associado ao domínio. Para aumentar o desempenho da política de grupo, recomendamos que você defina o seguinte valor da chave do registro para o registro:

Subchave do registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrada: BufferPolicyReads

Tipo: DWORD

Valor: 1

### Distribuir aviso legal por meio da política de grupo em vez de na imagem do MED-V

Se você quiser que os usuários finais vejam um contrato de nível de serviço (SLA) antes de acessarem o MED-V, recomendamos que você aplique o SLA por meio da política de grupo para que o SLA seja exibido para o usuário final após a primeira vez que a instalação for concluída.

**Cuidado**  Embora seja possível executar a primeira prática durante a configuração no modo **autônomo** , se você decidir definir a política local ou a entrada do registro para incluir um SLA na sua imagem (disco rígido virtual), também deverá especificar a primeira vez que a configuração da instalação será executada no modo **assistido** ou que a configuração da primeira vez poderá falhar.

 

### Compactar o disco rígido virtual

Recomendamos que você compacte seu disco rígido virtual para recuperar espaço em disco vazio e reduzir o tamanho do disco rígido virtual. Para obter mais informações sobre como compactar seu disco rígido virtual, consulte [compactando o disco rígido virtual do MED-V](compacting-the-med-v-virtual-hard-disk.md).

### Configurar a máquina virtual para reiniciar em uma falha de tela azul

Recomendamos que você configure a máquina virtual do espaço de trabalho do MED-V para reiniciar automaticamente quando encontrar uma falha de tela azul. Para definir essa configuração no convidado, defina o valor de reinicialização na chave hKey \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\crashcontrol como "1".

Você também pode definir essa configuração clicando em **Iniciar**, em **painel de controle**e, em seguida, em **sistema**. Em seguida, na área **inicialização e recuperação** da guia **avançado** , clique em **configurações**. Marque a caixa de seleção **reinicialização automática** e clique em **OK**.

### Fazer backup da imagem do MED-V antes de lacra-la

Recomendamos que você crie uma cópia de backup da imagem do MED-V antes de lacra-la. Para obter mais informações sobre como lacrar sua imagem do MED-V, consulte [Configurando uma imagem do Windows Virtual PC para med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Instalar o Windows Virtual PC por último ao instalar a partir de um arquivo em lote

Ao instalar os componentes do MED-V usando um arquivo em lotes, especifique que o Windows Virtual PC e o hotfix do Windows Virtual PC são instalados após o agente do host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V. Isso garante que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.

### Instalar o espaço de trabalho do MED-V na pasta local

Devido a problemas que podem ocorrer ao instalar o MED-V a partir de um local de rede, recomendamos que você copie os arquivos de configuração do espaço de trabalho do MED-V localmente e, em seguida, execute setup.exe.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>Gerenciar o redirecionamento de impressoras somente de uma maneira

Se uma impressora é instalada manualmente na máquina virtual de convidado do MED-V, e a mesma impressora é instalada posteriormente no computador host, o resultado é que ela é instalada duas vezes no convidado. Para evitar essa situação, recomendamos que você gerencie o redirecionamento de impressora apenas de uma maneira: desabilite o redirecionamento e instale as impressoras manualmente no convidado ou habilite o redirecionamento e não instale impressoras manualmente no convidado.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>Definir configurações para patch de convidado do MED-V

Você pode controlar quando e por quanto tempo a máquina virtual do MED-V pode receber atualizações automáticas definindo os valores de configuração relevantes no registro. Uma prática recomendada do MED-V é definir seu intervalo de ativação para corresponder ao tempo em que você agendou atualizações regulares para máquinas virtuais do MED-V. Além disso, recomendamos que você defina essas configurações para se parecer com o comportamento do computador host.

Para obter mais informações sobre como definir as configurações para o patch de convidado do MED-V, consulte [gerenciando atualizações automáticas para espaços de trabalho do MED-v](managing-automatic-updates-for-med-v-workspaces.md).

### Configurar antivírus/software de backup

Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, recomendamos que, quando possível, você exclua os seguintes tipos de arquivo de máquina virtual de qualquer processo de antivírus ou backup em execução no computador host do MED-V:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. Wim

## Tópicos relacionados


[Segurança e proteção para a MED-V](security-and-protection-for-med-v.md)

 

 





