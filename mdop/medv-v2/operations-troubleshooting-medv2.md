---
title: Solução de problemas de operações
description: Solução de problemas de operações
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796075"
---
# Solução de problemas de operações


Este tópico inclui informações que você pode usar para ajudar a solucionar problemas operacionais gerais na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.

## Solucionando problemas em operações do MED-V


Veja a seguir alguns problemas que os usuários finais podem encontrar quando executarem o MED-V e soluções para ajudar a solucionar esses problemas:

**Falha no redirecionamento da documentação**. Geralmente, esse problema ocorre quando a pasta meus documentos de um usuário final aponta para um local de rede. O Windows não dá suporte à criação de um compartilhamento de outra pasta compartilhada. Quando uma unidade ou pasta é redirecionada para o convidado, o RDP\\Windows Virtual PC cria um compartilhamento para essa pasta. Portanto, se a pasta meus documentos do host já estiver apontando para um compartilhamento, o RDP\\Windows Virtual PC não poderá criar um compartilhamento de um compartilhamento.

Outra causa possível desse problema é que as credenciais necessárias para se conectar ao recurso de rede podem ser diferentes das credenciais de domínio do usuário. O MED-V pode estar detectando que os documentos são redirecionados no host, envie essas informações para o convidado e, em seguida, tente reconectar o recurso de rede. Se as credenciais do usuário não forem autenticadas, o MED-V pode parar de tentar autenticar.

**Solução**

Para solucionar esse problema, tente um dos seguintes procedimentos:

-   Defina o diretório raiz do usuário dentro do Active Directory. O convidado e o host devem, então, se conectar ao mesmo recurso de rede.

-   Em vez de redirecionar a pasta meus documentos para um caminho UNC, mapeie-a para uma letra de unidade (no host, mapeie uma unidade que aponte para o recurso de rede). A pasta meus documentos pode ser definida para usar a letra da unidade em vez do caminho UNC. O convidado será redirecionado para essa mesma unidade mapeada conforme esperado.

-   Crie um script de inicialização no convidado que redireciona a pasta meus documentos para o recurso de rede e fornece credenciais adicionais conforme necessário.

**Falha no redirecionamento de URL**. Uma URL que você especificou para o redirecionamento do host para o convidado não é redirecionada conforme o esperado ou está retornando uma mensagem de erro indicando que o site não existe.

**Solução**

Esse erro pode ocorrer quando há um uso incorreto de caracteres, como asterisco (\ *), nas informações de redirecionamento de URL. Verifique o valor do registro para redirecionamento de URL e corrija os erros.

A chave do registro é chamada `RedirectUrls` e geralmente está localizada em:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

**Ícone na barra de tarefas enganosa**. Por padrão, o ícone que aparece na barra de tarefas de um usuário final para aplicativos publicados e URLs redirecionadas é o ícone do Windows Virtual PC. Se um usuário final não reconhece esse comportamento padrão, ele pode ficar confuso ao olhar na barra de tarefas para localizar o aplicativo.

**Solução**

A única maneira de evitar esse comportamento padrão é alterar as configurações do usuário para as propriedades da barra de tarefas da seguinte maneira:

1.  Clique com o botão direito do mouse na barra de tarefas e clique em **Propriedades**.

2.  Na caixa de diálogo **Propriedades da barra de tarefas e do menu iniciar** , clique na guia **barra de tarefas** .

3.  Na barra suspensa da caixa de botões da **barra de tarefas** , selecione **nunca combinar**.

4.  Clique em **OK**.

Os ícones esperados para aplicativos publicados e URLs redirecionadas são exibidos.

**Aviso emitido se o segundo usuário tentar fazer logon ou se a máquina virtual estiver em uso**. Uma mensagem de aviso é emitida quando um segundo usuário se conecta a um espaço de trabalho do MED-V enquanto um primeiro usuário ainda está executando o MED-V. O aviso também será emitido se MED-V for iniciado enquanto a máquina virtual estiver sendo usada, por exemplo, se a máquina virtual tiver sido iniciada por meio do PC virtual do Windows no menu **Iniciar** . Quando o usuário final aceita a mensagem de aviso, o MED-V é desligado.

**Solução**

Um usuário final deve verificar se todos os outros usuários fazem logoff do MED-V antes de tentarem fazer logon. Isso garante que nenhuma outra instância do MED-V esteja em execução e que o computador virtual do Windows não esteja no controle da máquina virtual.

**Bipes ouvidos durante a primeira configuração**. Ocasionalmente, os bipes são ouvidos enquanto o MED-V estiver sendo executado pela primeira vez. Isso pode ser confuso para um usuário final. Os bipes estão originários da máquina virtual quando executam determinadas ações, como desligar.

**Solução**

Você pode interromper o serviço de bipe especificando o comando "net stop beep" no início de cada sequência de início de máquina virtual. Ou você pode desativar o serviço de bipe especificando o comando "sc config beep start = disabled". Você pode especificar esses comandos antes de lacrar a imagem ou como parte do Sysprep.

**Várias conexões de rede criadas para os espaços de trabalho do MED-V no modo de ponte**. Se a primeira configuração estiver criando um espaço de trabalho do MED-V configurado para o modo NAT, ele somente criará uma única conexão de rede no PC virtual do Windows. No entanto, se a primeira configuração estiver criando um espaço de trabalho do MED-V configurado para o modo de ponte, ele criará uma conexão de rede separada para cada adaptador de rede instalado no computador, pois o MED-V não pode determinar qual adaptador de rede está ativo. Isso também garante que os usuários móveis sempre tenham um adaptador de rede disponível para conexões com fio e sem fio.

**Solução**

Nenhuma.

O **aplicativo MED-V não responde por muito tempo durante o fechamento**. Em alguns casos, um aplicativo MED-V pára de responder quando está tentando fechar.

**Solução**

Você pode especificar o período de tempo que o MED-V aguarda para fechar aplicativos que não respondem definindo a chave do registro WaitToKillAppTimeout na máquina virtual convidada. Para obter mais informações, consulte [como aumentar o tempo de desligamento para que os processos possam ser encerrados corretamente no Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

A **renomeação de um atalho de aplicativo publicado na máquina virtual convidada não altera o nome publicado no host**. Quando você publica um aplicativo Criando um atalho e, em seguida, renomeia o atalho na máquina virtual convidada, o nome do aplicativo original permanece no menu de **início** do host. O programa continua a ser executado conforme o esperado, no entanto, o programa sempre manterá o nome original.

**Solução**

Nenhuma. Esse é um comportamento conhecido do PC virtual do Windows.

**Mover um atalho na máquina virtual convidada não atualiza o local no menu Iniciar do computador host**. Os atalhos do aplicativo MED-V publicados no menu **Iniciar** do computador host são catalogados no registro. Se você mover um atalho do aplicativo para uma subpasta, o registro não será atualizado para refletir a alteração.

**Solução**

Siga estas etapas para alterar o local de um atalho do aplicativo MED-V:

1.  Quando o MED-V estiver em execução, abra o Windows Explorer na máquina virtual de convidado do MED-V.

2.  Navegue até o diretório "%ALLUSERSPROFILE%\\Start Menu\\Programs".

3.  Mova os atalhos do aplicativo para fora das pastas StartMenu ou programas.

4.  Após cerca de 30 segundos, valide se os atalhos foram removidos do menu **Iniciar** do computador host.

5.  Mova os atalhos do aplicativo de volta para as novas pastas do programa no diretório inicial do Menu\\Programs.

6.  Após cerca de 30 segundos, valide se os atalhos são atualizados no menu **Iniciar** do computador host.

**Aplicativos publicados podem expirar após ficar ocioso**. Em alguns casos, os aplicativos publicados expirarão se ficarão inativos por algum tempo. Essa situação ocorre apenas se o IPsec estiver habilitado e o espaço de trabalho do MED-V estiver configurado para o modo NAT. Essa situação não ocorrerá se estiver em execução no modo de ponte.

**Solução**

Desative o IPsec quando você estiver executando o espaço de trabalho do MED-V no modo NAT.

**Fixar um aplicativo publicado na barra de tarefas ignora o MED-V**. Se um usuário final fixar um aplicativo publicado na barra de tarefas e, em seguida, fechar o aplicativo, o MED-V será ignorado na próxima vez que o aplicativo for aberto no ícone da barra de tarefas. Em vez disso, o aplicativo é aberto diretamente em uma janela do VMSAL.

**Solução**

Não fixe os aplicativos publicados no MED-V à barra de tarefas.

## Tópicos relacionados


[Práticas recomendadas de segurança para operações da MED-V](security-best-practices-for-med-v-operations.md)

[Solução de problemas de implantação](deployment-troubleshooting.md)

 

 





