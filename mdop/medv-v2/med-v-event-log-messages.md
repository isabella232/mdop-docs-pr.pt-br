---
title: Mensagens do log de eventos da MED-V
description: Mensagens do log de eventos da MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799200"
---
# Mensagens do log de eventos da MED-V


Os arquivos de log para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fornecem informações detalhadas sobre como implantar e gerenciar o MED-V na sua empresa e ajudar a verificar a funcionalidade ou ajudar a solucionar problemas.

## IDs de evento


Veja a seguir uma lista de IDs de eventos do MED-V para ajudar a solucionar problemas que podem ocorrer ao implantar ou gerenciar o MED-V.

### Fts

Mostra as identificações de eventos da primeira configuração de hora.

### IDENTIFICAÇÃO do evento 3066

Falha na operação iniciar máquina virtual.

<a href="" id="description"></a>**Descrição**  
Há um problema potencial com o disco rígido virtual (VHD) que você está usando para criar um espaço de trabalho do MED-V.

<a href="" id="solution"></a>**Solução**  
Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ela possa ser iniciada.

### IDENTIFICAÇÃO do evento 3071

Falha na preparação da máquina virtual.

<a href="" id="description"></a>**Descrição**  
Ocorreu um problema com uma configuração de primeira vez que pode ter sido causada por muitos problemas diferentes. Isso inclui problemas com a conectividade de rede.

<a href="" id="solution"></a>**Solução**  
Reinicie o agente do host do MED-V para executar a instalação novamente pela primeira vez.

### IDENTIFICAÇÃO do evento 3078

Falha na preparação da máquina virtual.

<a href="" id="description"></a>**Descrição**  
Há um problema potencial com o VHD que você está usando para criar um espaço de trabalho do MED-V.

<a href="" id="solution"></a>**Solução**  
Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ela possa ser iniciada.

### IDENTIFICAÇÃO do evento 3079

Tentando preparar a máquina virtual.

<a href="" id="description"></a>**Descrição**  
O MED-V está tentando preparar a máquina virtual.

<a href="" id="solution"></a>**Solução**  
Nenhuma ação é necessária. Na primeira vez que a configuração é concluída.

### IDENTIFICAÇÃO do evento 3080

O cliente foi interrompido ao preparar a máquina virtual.

<a href="" id="description"></a>**Descrição**  
O MED-V é interrompido inesperadamente quando ele tenta preparar a máquina virtual.

<a href="" id="solution"></a>**Solução**  
Iniciar o agente de host do MED-V e concluir a configuração da primeira vez

### IDENTIFICAÇÃO do evento 3084

A máquina virtual não é válida. Na primeira vez que a instalação precisa ser executada novamente.

<a href="" id="description"></a>**Descrição**  
O agente de host do MED-V detectou um problema com a máquina virtual.

<a href="" id="solution"></a>**Solução**  
Nenhuma ação é necessária. Na primeira vez que a configuração é concluída.

### IDENTIFICAÇÃO do evento 3099

Falha na chamada para iniciar a máquina virtual.

<a href="" id="description"></a>**Descrição**  
Há um problema potencial com o VHD que você está usando para criar um espaço de trabalho do MED-V.

<a href="" id="solution"></a>**Solução**  
Verifique se você pode criar uma máquina virtual com o VHD do MED-V e que ele possa ser aberto.

### Gerenciamento de VM

### IDENTIFICAÇÃO do evento 4022

VMManagerException erro fatal durante a emissão do comando para a VM.

<a href="" id="description"></a>**Descrição**  
O usuário final tentou sair do MED-V fazendo logoff ou desligando o host do MED-V, e a configuração de configuração do VMTaskTimeout foi excedida.

<a href="" id="solution"></a>**Solução**  
Reinicie o MED-V.

### IDENTIFICAÇÃO do evento 4028

Tempo limite da operação da VM.

<a href="" id="description"></a>**Descrição**  
O usuário final tentou sair do MED-V fazendo logoff ou desligando o host e a configuração de configuração do VMTaskTimeout foi excedida.

<a href="" id="solution"></a>**Solução**  
Reinicie o MED-V.

### IDENTIFICAÇÃO do evento 4038

Vmsal postou uma mensagem de erro para o usuário.

<a href="" id="description"></a>**Descrição**  
Uma mensagem de erro é exibida para o usuário final informando que o MED-V não pôde iniciar o aplicativo virtual.

<a href="" id="solution"></a>**Solução**  
Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC e tente iniciar o aplicativo em tela inteira.

### IDENTIFICAÇÃO do evento 4040

Recycling Additions porque TerminalServices não está inicializado no convidado.

<a href="" id="description"></a>**Descrição**  
O MED-V reinicializou a máquina virtual porque os serviços de área de trabalho remota não foram inicializados na máquina virtual.

<a href="" id="solution"></a>**Solução**  
Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC.

### IDENTIFICAÇÃO do evento 4042

Falha ao reciclar adições no convidado.

<a href="" id="description"></a>**Descrição**  
O MED-V não pôde reciclar adições de máquina virtual na máquina virtual.

<a href="" id="solution"></a>**Solução**  
Se o erro for registrado duas ou mais vezes em uma linha, interrompa o MED-V e conecte-se à máquina virtual usando o console do Windows Virtual PC.

### IDENTIFICAÇÃO do evento 4043

Falha ao redefinir a senha expirada na máquina virtual.

<a href="" id="description"></a>**Descrição**  
O usuário final não redefiniu a senha na máquina virtual antes de ela ter expirado. Como resultado, o usuário pode não conseguir acessar os recursos da rede nem salvar o trabalho.

<a href="" id="solution"></a>**Solução**  
Desligue o MED-V Guest e reinicie-o.

### Redirecionamento de URL

### IDENTIFICAÇÃO do evento 5005

Não foi possível obter o nome da VM da configuração; Não é possível iniciar o navegador convidado.

<a href="" id="description"></a>**Descrição**  
O redirecionamento de URL não pôde obter o nome do espaço de trabalho do MED-V na configuração. Como resultado, ele não pode informar ao PC virtual do Windows para abrir a URL redirecionada no navegador de espaço de trabalho do MED-V.

<a href="" id="solution"></a>**Solução**  
Certifique-se de que o nome do espaço de trabalho do MED-V esteja definido e que ele corresponda a um nome de máquina virtual no &lt; *user* &gt; diretório de computadores \\Virtual usuários do C:\\Users\\. O nome do espaço de trabalho do MED-V está localizado em HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Por exemplo, se o usuário for "Matt" e o nome do espaço de trabalho for "mattsworkspace", o valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve ser "mattsworkspace", e deve haver um arquivo chamado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### IDENTIFICAÇÃO do evento 5006

Falha ao criar servidor de pipe.

<a href="" id="description"></a>**Descrição**  
O serviço de redirecionamento de URL não pôde criar o servidor de pipe para se comunicar com o Internet Explorer.

<a href="" id="solution"></a>**Solução**  
Verifique os logs de eventos do sistema para tentar criar um arquivo ou um recurso cujo caminho comece semelhante ao seguinte: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" e termina com o nome de usuário e o nome de domínio do usuário. Se isso não estiver presente no log de eventos, reinicie o computador.

### ConfigMgr (convidado)

### IDENTIFICAÇÃO do evento 7001

Os dados de configuração de rede do host não estão formatados corretamente.

<a href="" id="description"></a>**Descrição**  
A configuração de rede recebida do host é uma cadeia de caracteres XML formatada incorretamente ou as informações de rede retornadas do host não podem ser gravadas em um documento XML.

<a href="" id="solution"></a>**Solução**  
Reinicie o computador host e a máquina virtual.

### IDENTIFICAÇÃO do evento 7005

Uma alteração na configuração de rede do host foi detectada, mas não pôde ser aplicada porque os dados de configuração de rede do host não estavam formatados corretamente.

<a href="" id="description"></a>**Descrição**  
Uma alteração na configuração de rede do host foi comunicada à máquina virtual, mas não foi possível processá-la na máquina virtual devido a um erro. Esse erro pode ser causado por dados formatados incorretamente ou pela incapacidade de definir as informações na instância CCMNetworkAdapter da instrumentação de gerenciamento do Windows (WMI).

<a href="" id="solution"></a>**Solução**  
Reinicie o host e a máquina virtual.

### ConfigMgr (host)

### IDENTIFICAÇÃO do evento 8006

Não é possível encontrar a máquina virtual.

<a href="" id="description"></a>**Descrição**  
O Windows Virtual PC 7 não consegue localizar a máquina virtual. A máquina virtual pode ter sido excluída, movida, removida ou o acesso foi negado.

<a href="" id="solution"></a>**Solução**  
Reinstale a máquina virtual.

### IDENTIFICAÇÃO do evento 8008

As informações de configuração de rede da estação de trabalho não puderam ser recuperadas.

<a href="" id="description"></a>**Descrição**  
As informações de configuração de rede não puderam ser coletadas do host do MED-V, provavelmente devido a uma falha na chamada do sistema no .NET Framework. Essa falha também pode ocorrer se as informações de rede retornadas do host MED-V não puderem ser gravadas em um documento XML.

<a href="" id="solution"></a>**Solução**  
Reinicie a estação de trabalho host.

### IDENTIFICAÇÃO do evento 8010

Os dados de configuração de rede não puderam ser definidos na máquina virtual.

<a href="" id="description"></a>**Descrição**  
A conversão de endereços (NAT) do MED-V hostnetwork (NAT) não pôde ser comunicada à máquina virtual, provavelmente porque a máquina virtual está em um estado incorreto ou o Windows Virtual PC Additions não foi instalado ou habilitado.

<a href="" id="solution"></a>**Solução**  
Desligue e reinicie a máquina virtual. Além disso, talvez seja necessário reinstalar a máquina virtual.

### IDENTIFICAÇÃO do evento 8011

Não foi possível redefinir os dados de configuração de rede na máquina virtual.

<a href="" id="description"></a>**Descrição**  
A configuração hostnetwork do MED-V (com ponte) não pôde ser comunicada à máquina virtual, provavelmente porque a máquina virtual está em um estado incorreto ou o Windows Virtual PC Additions não foi instalado ou habilitado.

<a href="" id="solution"></a>**Solução**  
Desligue e reinicie a máquina virtual. Além disso, talvez seja necessário reinstalar a máquina virtual.

### Redirecionamento de impressora

### IDENTIFICAÇÃO do evento 9001

Erro de permissão de arquivo.

<a href="" id="description"></a>**Descrição**  
O usuário final não está autorizado a acessar a pasta necessária para abrir ou criar o arquivo da impressora MED-V para leitura.

<a href="" id="solution"></a>**Solução**  
Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para ler e gravar nele. Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\, e todos os arquivos contidos deverão ter permissões de leitura e gravação. E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.

### IDENTIFICAÇÃO do evento 9002

Erro de permissão de arquivo.

<a href="" id="description"></a>**Descrição**  
O usuário final não está autorizado a acessar a pasta necessária para abrir ou criar o arquivo da impressora MED-V para gravação.

<a href="" id="solution"></a>**Solução**  
Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para lê-lo e escrevê-lo. Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação. E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.

### IDENTIFICAÇÃO do evento 9004

Não foi possível criar o caminho para armazenar arquivos de impressora MEDV.

<a href="" id="description"></a>**Descrição**  
O serviço de redirecionamento de impressora não pôde acessar arquivos ou criar diretórios necessários para armazenar as informações da impressora.

<a href="" id="solution"></a>**Solução**  
Verifique se o caminho User\\AppData\\ pode ser acessado e se o usuário tem permissão para ler e gravar nele. Por exemplo, se o usuário for "Matt", o caminho C:\\Users\\Matt\\AppData\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação. E, se existir, o caminho C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ e todos os arquivos contidos deverão ter permissões de leitura e gravação.

### IDENTIFICAÇÃO do evento 9005

Não foi possível obter o nome da VM da configuração; Não é possível iniciar o instalador convidado. Não é possível atualizar o MED-V – nenhuma rede de host detectada.

<a href="" id="description"></a>**Descrição**  
O serviço de redirecionamento de impressora não pôde obter o nome do espaço de trabalho do MED-V na configuração do MED-V e não pode informar ao PC virtual do Windows para iniciar o instalador no MED-V Guest.

<a href="" id="solution"></a>**Solução**  
Certifique-se de que o nome do espaço de trabalho do MED-V esteja definido e que ele corresponda a um nome de máquina virtual no &lt; *user* &gt; diretório de computadores \\Virtual usuários do C:\\Users\\. O nome do espaço de trabalho do MED-V está localizado em HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.

Por exemplo, se o usuário for "Matt" e o nome do espaço de trabalho for "mattsworkspace", o valor de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name deve ser "mattsworkspace" e deve haver um arquivo chamado C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.

### Publicação de aplicativos

### IDENTIFICAÇÃO do evento 10015

Ocorreu um erro no sistema de arquivos durante o processo de reconciliação. O processo de reconciliação não processará o &lt; *nome* do arquivo &gt; , mas continuará processando outras alterações.

<a href="" id="description"></a>**Descrição**  
Ocorreu um erro de acesso não autorizado ou de e/s ao criar ou excluir um atalho.

<a href="" id="solution"></a>**Solução**  
Verifique se o caminho do arquivo pode ser acessado e se o usuário tem permissões para criar ou excluir o arquivo especificado.

### IDENTIFICAÇÃO do evento 10021

&lt; *Erro de erro \ _information* &gt; para operação de operação de arquivo &lt; *\ _name* &gt; no arquivo de nome do arquivo &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrição**  
Ocorreu um erro de acesso não autorizado ou de e/s ao criar ou excluir um atalho.

<a href="" id="solution"></a>**Solução**  
Verifique se o caminho do arquivo pode ser acessado e se o usuário tem permissões para criar ou excluir o arquivo especificado.

### Correção de convidado

### IDENTIFICAÇÃO do evento 11001

Mensagem de uso da tarefa de ativação de convidado.

<a href="" id="description"></a>**Descrição**  
MedvHost.exe com a opção/GuestWakeup foi executada incorretamente, ou o comando está formatado incorretamente.

<a href="" id="solution"></a>**Solução**  
Certifique-se de que o comando seja executado com o seguinte formato:

Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *Workspace \ _name* &gt; " onde

&lt;*Duration \ _in \ _minutes* &gt; é o número de minutos em que a máquina virtual deve ficar em dia (o padrão é 240) e

&lt;*espaço de trabalho \ _name* &gt; é o nome da máquina virtual que deve ser ativado.

### IDENTIFICAÇÃO do evento 11002

Não é possível atualizar o MED-V – nenhuma rede de host detectada.

<a href="" id="description"></a>**Descrição**  
O patch de convidado não pôde ser concluído porque nenhuma conexão de rede de host foi detectada.

<a href="" id="solution"></a>**Solução**  
Conecte o host do MED-V a uma conexão de rede ativa antes de executar o patch de convidado.

### IDENTIFICAÇÃO do evento 11003

Não é possível atualizar o MED-V – o host não está em execução em A/C powerFailed para criar um servidor de pipe.

<a href="" id="description"></a>**Descrição**  
O patch de convidado não pôde ser concluído porque o host parece estar em execução na energia da bateria, em vez de em um fio de alimentação.

<a href="" id="solution"></a>**Solução**  
Conecte o computador host a um cabo de alimentação antes de executar o patch de convidado.

### UX do cliente

### IDENTIFICAÇÃO do evento 14003

A mensagem de status da bandeja a seguir era muito longa e não pôde ser exibida: &lt; *tray \ _status \ _message*&gt;

<a href="" id="description"></a>**Descrição**  
O MED-V criou uma cadeia de caracteres não esperada muito longa para a dica de ferramenta de bandeja ou a mensagem de balão. Como resultado, a mensagem exibida foi truncada.

<a href="" id="solution"></a>**Solução**  
Esse é um erro raro que pode ocorrer quando o MED-V cria aleatoriamente o texto da dica de ferramenta. Não há solução.

### IDENTIFICAÇÃO do evento 14004

O MED-V parou devido a uma exceção não tratada.

<a href="" id="description"></a>**Descrição**  
Uma exceção não tratada fez o MED-V parar inesperadamente.

<a href="" id="solution"></a>**Solução**  
Reinicie o MED-V.

### IDENTIFICAÇÃO do evento 14005

O servidor tentou criar o mutex, mas já existia.

<a href="" id="description"></a>**Descrição**  
Uma segunda instância do MedvHost.exe está presa na memória.

<a href="" id="solution"></a>**Solução**  
Abra o taskmanager e encerre todos os processos de MedvHost.exe.

### IDENTIFICAÇÃO do evento 14006

Erro ao modificar ou excluir o registro de valor do registro &lt; *\ _value* &gt; .

<a href="" id="description"></a>**Descrição**  
O MED-V não pode modificar a entrada especificada no registro.

<a href="" id="solution"></a>**Solução**  
Verifique se você instalou ou desinstalou o MED-V com credenciais administrativas.

### IDENTIFICAÇÃO do evento 14007

O arquivo especificado ( &lt; *filename* &gt; ) não é válido.

<a href="" id="description"></a>**Descrição**  
Durante a instalação ou desinstalação, um arquivo temporário corrompido foi passado para o host do MED-V.

<a href="" id="solution"></a>**Solução**  
Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.

### IDENTIFICAÇÃO do evento 14008

Arquivo não encontrado: &lt; *nome_do_arquivo* &gt; .

<a href="" id="description"></a>**Descrição**  
Durante a instalação ou desinstalação, um caminho de um arquivo temporário obrigatório não foi encontrado.

<a href="" id="solution"></a>**Solução**  
Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V.

### IDENTIFICAÇÃO do evento 14009

Não é possível ler o nome do arquivo do arquivo de parâmetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrição**  
Durante o processo de instalação ou desinstalação, o MED-V não pôde ler um arquivo temporário.

<a href="" id="solution"></a>**Solução**  
Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V. Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.

### IDENTIFICAÇÃO do evento 14010

Erro ao desserializar o nome do arquivo de parâmetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrição**  
Durante o processo de instalação ou desinstalação, o MED-V encontrou um arquivo temporário corrompido.

<a href="" id="solution"></a>**Solução**  
Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V. Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.

### IDENTIFICAÇÃO do evento 14011

Erro inesperado ao desserializar o nome do arquivo de parâmetro &lt; *filename* &gt; .

<a href="" id="description"></a>**Descrição**  
Durante o processo de instalação ou desinstalação, o MED-V encontrou um arquivo temporário corrompido.

<a href="" id="solution"></a>**Solução**  
Exclua todos os arquivos da pasta Temp e reinstale ou desinstale o MED-V. Além disso, verifique se o usuário tem as permissões e os direitos necessários para a pasta Temp.

### IDENTIFICAÇÃO do evento 14012

Erro inesperado quando as configurações direitos na &lt; *pasta da pasta \ _name* &gt; para nome de usuário do usuário &lt; *username* &gt; .

<a href="" id="description"></a>**Descrição**  
Um erro ocorre quando o MED-V não consegue definir direitos e permissões em determinadas pastas durante a instalação.

<a href="" id="solution"></a>**Solução**  
Verifique as seguintes permissões de administrador nas seguintes pastas:

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### IDENTIFICAÇÃO do evento 14013

Erro inesperado ao criar um arquivo de bloqueio.

<a href="" id="description"></a>**Descrição**  
Um erro ocorre quando o MED-V não pode criar um arquivo na pasta @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" durante a instalação.

<a href="" id="solution"></a>**Solução**  
Verifique os direitos de administrador para a pasta MedvLock.

## Tópicos relacionados


[Solução de problemas da MED-V](troubleshooting-med-vmedv2.md)

 

 





