---
title: Solução de problemas da MED-V
description: Solução de problemas da MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799757"
---
# Solução de problemas da MED-V


Esta seção fornece informações para ajudar a solucionar problemas gerais com a virtualização de área de trabalho do Microsoft Enterprise (MED-V).

## Alterar a resolução do host e, em seguida, maximizar o espaço de trabalho do MED-V faz com que a área de trabalho apareça em preto


Ao trabalhar no modo de área de trabalho completo, se você alterar a resolução do host e, em seguida, maximizar a janela do espaço de trabalho do MED-V, a área de trabalho aparecerá em preto e o espaço de trabalho do MED-V pode não

### Solução

Pare e, em seguida, inicie o espaço de trabalho do MED-V.

## Iniciando um espaço de trabalho do MED-V com um adaptador de rede desabilitado e, posteriormente, habilitar o adaptador não restaura a conectividade de rede


Se você configurar um espaço de trabalho do MED-V no modo de ponte e, em seguida, iniciar o espaço de trabalho do MED-V enquanto um adaptador de rede estiver desabilitado, se o adaptador for habilitado posteriormente, a conectividade de rede por meio desse adaptador não será restaurada.

### Solução

Pare e, em seguida, inicie o espaço de trabalho do MED-V.

## Uma imagem pode ser usada por apenas um usuário do Windows por computador


Uma imagem do espaço de trabalho do MED-V pode ser usada somente pelo usuário do Windows que baixou ou importou a imagem. Esse usuário é o único usuário além dos administradores que têm permissões para a pasta onde as imagens baixadas estão localizadas.

### Solução

Altere manualmente a ACL (lista de controle de acesso) no repositório de imagens.

## Ao instalar o MED-V usando o Configuration Manager com direitos de usuários habilitados, a desinstalação falha


Se o MED-V estiver instalado usando o Microsoft System Center Configuration Manager e o modo de execução do pacote for definido como direitos de usuário, a desinstalação falhará com uma mensagem de erro que diz que somente os usuários administrativos podem desinstalar o MED-V.

### Solução

Ao criar um pacote do Configuration Manager para MED-V, defina o modo de execução como direitos administrativos.

## Ao instalar o MED-V usando um sistema de implantação corporativa, no qual a instalação está configurada para executar o cliente após a instalação, não é possível executar o cliente


Se o MED-V estiver instalado usando um sistema de implantação corporativo e o pacote de instalação estiver configurado para executar o cliente MED-V após a instalação, após a execução do cliente na conta do sistema, você não poderá ver que o cliente está em execução (exceto na área de notificação) e não pode interagir com ele.

### Solução

Ao instalar o MED-V usando um sistema de implantação corporativo, use o parâmetro *Start \ _MEDV = 0* . msi.

## A imagem de teste do MED-V falha ao iniciar


Se uma imagem de teste do MED-V não for iniciada, ela nunca será recuperada e todas as futuras inicializações falharão com a mensagem de erro "GINA falha ao carregar".

### Solução

Exclua a imagem de teste existente e crie-a novamente.

## Depois de tentar ingressar em um domínio com as credenciais erradas, a imagem nunca é bem-sucedida ao ingressar no domínio


Se houver um erro de configuração no bloco de construção de domínio ingressar, que faz parte do script de configuração da máquina virtual pela primeira vez, isso causará falha no espaço de trabalho do MED-V ao tentar ingressar em um domínio. Depois que o erro de configuração for reparado, a imagem incluída no espaço de trabalho do MED-V não poderá ingressar no domínio.

### Solução

Se a imagem foi implantada, redistribua a imagem. Se a imagem for uma imagem de teste, recrie a imagem.

## O MED-V não oferece suporte a vários monitores


O MED-V não é compatível com a exibição de aplicativos publicados em vários monitores. Aplicativos publicados e outras janelas de cliente podem ser exibidas na tela errada e, às vezes, quando uma tela é desconectada, o MED-V tenta enviar a tela para o monitor para que o monitor conectado apareça em branco.

### Solução

Desconecte a tela adicional e reinicie o cliente.

## O espaço de trabalho do MED-V pode falhar ao iniciar quando o host falha durante a inicialização do espaço de trabalho do MED-V


Se o host falha durante o processo de inicialização do espaço de trabalho do MED-V e uma mensagem de erro é exibida dizendo que "o elemento raiz está ausente," o espaço de trabalho do MED-V pode adicionar dados a um arquivo de configuração de máquina virtual (VMC) vazio, o que fará com que o processo de inicialização falhe.

### Solução

Substitua o arquivo VMC vazio por um arquivo VMC da imagem base.

## O teclado não responde nas janelas de aplicativos publicados


Em um espaço de trabalho do MED-V, se você pressionar a tecla do logotipo do Windows quando um aplicativo publicado estiver em foco, o teclado não responderá mais nas janelas de aplicativos publicadas.

### Solução

Pressione a tecla do logotipo do Windows enquanto um aplicativo publicado estiver em foco.

## Um espaço de trabalho do domínio MED-V não atualiza as credenciais do domínio


Ao usar um espaço de trabalho do MED-V persistente em um ambiente de domínio, se você alterar a senha do domínio, o cliente MED-V não atualizará as credenciais de domínio do espaço de trabalho do MED-V. Quando um aplicativo publicado tenta acessar um recurso de rede, você receberá uma mensagem de erro informando que suas credenciais venceram.

### Solução

Reinicie o sistema operacional do espaço de trabalho do MED-V.

## Aplicativo de publicação maximizada Windows cover The host Taskbar


Se você maximizar uma janela de aplicativo publicada para tela inteira, talvez ela cubra a barra de tarefas do host.

### Solução

Siga um destes procedimentos:

Minimize a janela do aplicativo publicado para obter acesso à área de notificação e reinicie o espaço de trabalho do MED-V.

Minimize a janela do aplicativo publicado e restaure a janela ao seu estado maximizado.

## A adição de usuários ou grupos no Gerenciador de configuração do MED-V Server não funciona


Ao adicionar usuários ou grupos na caixa de diálogo **Selecionar usuários ou grupos** , os usuários ou grupos selecionados não são adicionados à lista de controle de acesso no Gerenciador de configuração do MED-V Server.

### Solução

Adicionar usuários ou grupos usando a caixa de diálogo **Inserir nomes de usuários ou grupos** . Para obter informações detalhadas, consulte [como instalar e configurar o componente do servidor MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).

## O MED-V não funciona em computadores com o Windows Virtual PC para Windows 7 instalado


O MED-V requer o PC2007 virtual do Windows. O Windows Virtual PC para Windows e o virtual PC2007 SP1 não podem ser instalados no mesmo computador.

### Solução

Desinstale o Virtual PC para o Windows7 antes de instalar o PC2007 virtual SP1 e o MED-V.

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a>O MED-V não é compatível com imagens do modo Virtual PC e WindowsXP


O MED-V 1.0 SP1 não oferece suporte a imagens criadas pelo PC virtual do Windows para o Windows7. Se um PC virtual para a imagem do Windows7 for usado, o cliente falhará durante a inicialização.

### Solução

Criar imagens do MED-V usando o virtual PC2007 SP1.

## O Firewall do Windows bloqueia a atividade de rede do PC2007 SP1 virtual


Por padrão, o Firewall do Windows bloqueia a atividade de rede do PC2007 SP1 virtual e, quando o virtual PC2007 SP1 é iniciado no computador cliente, há uma mensagem de firewall que bloqueia a sequência de inicialização e todo o acesso à rede.

### Solução

Atualize a exceção do firewall usando a política de grupo antes de o MED-V ser usado pelo usuário final.

## A mensagem de erro ao atualizar o cliente é exibida


Durante a atualização do cliente do MED-V 1.0 para o MED-V 1.0 SP1, uma mensagem poderá ser exibida informando que não há um espaço de trabalho do MED-V definido.

### Solução

Feche o cliente e reinicie-o.

## Tópicos relacionados


[Notas de versão do MED-V 1.0](med-v-10-release-notesmedv-10.md)

[Notas de versão do MED-V 1.0 SP1 e SP2](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





