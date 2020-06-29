---
title: Visão geral das ferramentas do DaRT 7.0
description: Visão geral das ferramentas do DaRT 7.0
author: dansimp
ms.assetid: 67c5991e-cbe6-4ce9-9fe5-f1761369d1fe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d327e14fd1851f0e0d82e1c3ad692bcf7842a835
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799273"
---
# Visão geral das ferramentas do DaRT 7.0


Na janela **diagnóstico e recuperação do conjunto** de ferramentas de diagnóstico e recuperação do Microsoft (DART) 7, você pode iniciar qualquer uma das ferramentas individuais que foram incluídas quando a imagem de recuperação do DART foi criada. Para obter informações sobre como acessar a janela **diagnóstico e conjunto de ferramentas de recuperação** , consulte [como recuperar computadores locais usando a imagem de recuperação do DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

Se ele estiver disponível, você pode usar o **Assistente de soluções** na janela **diagnóstico e recuperação de conjunto de ferramentas** para selecionar a ferramenta que melhor atende a seu problema específico, com base em uma breve entrevista.

## Explorando as ferramentas do DaRT


Esta seção descreve as diversas ferramentas que fazem parte do DaRT.

### Editor do registro

Você pode usar o **Editor do registro** para acessar e alterar o registro do sistema operacional Windows que você está analisando ou reparando. Isso inclui a adição, a remoção e a edição de chaves e valores e a importação de arquivos do registro (. reg).

**Cuidado**  Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.

 

### Locksmith

O **Assistente locksmith** permite definir ou alterar a senha de qualquer conta local no sistema operacional Windows que você está analisando ou reparando. Você não precisa saber a senha atual. No entanto, a senha definida deve ser compatível com os requisitos definidos por um objeto de política de grupo local. Isso inclui o tamanho e a complexidade da senha.

Você pode usar **locksmith** quando a senha de uma conta local, como a conta de administrador local, for desconhecida. Você não pode usar **locksmith** para definir senhas para contas de domínio.

### Crash Analyzer

Use o **Assistente do Crash Analyzer** para determinar rapidamente a causa de uma falha no computador analisando o arquivo de despejo de memória no sistema operacional do Windows que você está reparando. O **Crash Analyzer** examina o arquivo de despejo de falha para o driver que causou a falha do computador. Em seguida, você pode desabilitar o driver de dispositivo com problema usando o nó **serviços e drivers** na ferramenta de **Gerenciamento do computador** .

O **Assistente do Crash Analyzer** requer as ferramentas de depuração para Windows e arquivos de símbolo para o sistema operacional que você está reparando. Você pode incluir ambos os requisitos ao criar a imagem de recuperação do DaRT. Se não estiverem incluídos na imagem de recuperação e você não tiver acesso a elas no computador que está reparando, você pode copiar o arquivo de despejo de memória para outro computador e usar a versão autônoma do **Crash Analyzer** para diagnosticar o problema.

Executar o **Crash Analyzer** é uma boa ideia, mesmo que você planeje a nova imagem do computador. A imagem pode ter um driver defeituoso que está causando problemas em seu ambiente. Ao executar o **Crash Analyzer**, você pode identificar os drivers dos problemas e melhorar a estabilidade da imagem.

Para obter mais informações sobre o **Crash Analyzer**, consulte [Diagnosticando falhas do sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

### Restauração de arquivos

A **restauração de arquivos** permite que você tente restaurar arquivos que foram excluídos acidentalmente ou que eram muito grandes para caber na lixeira. A **restauração de arquivos** não está limitada a volumes de disco regulares, mas pode localizar e restaurar arquivos em volumes perdidos ou em volumes criptografados pelo BitLocker.

### Disk Commander

O **Disk Commander** permite recuperar e reparar partições de disco ou volumes usando um dos seguintes processos de recuperação:

-   Restaurar o registro mestre de inicialização (MBR)

-   Recuperar um ou mais volumes perdidos

-   Restaurar tabelas de partição do backup do **Disk Commander**

-   Salvar tabelas de partição no backup do **Disk Commander**

**Aviso**  Recomendamos que você faça backup de um disco antes de usar o **Disk Commander** para repará-lo. Usando o **Disk Commander**, você pode danificar volumes e torná-los inacessíveis. Além disso, as alterações em um volume podem afetar outros volumes porque volumes em um disco compartilham uma tabela de partição.

 

### Apagamento de disco

Você pode usar **apagamento de disco** para excluir todos os dados de um disco ou volume, até mesmo os dados que são deixados para trás após a reformatação de uma unidade de disco rígido. O **apagamento de disco** permite que você selecione entre uma substituição de passagem única ou uma substituição de quatro passagens, que atende aos padrões atuais do departamento de defesa dos EUA.

**Aviso**  Após limpar um disco ou volume, você não pode recuperar os dados. Verifique o tamanho e o rótulo de um volume antes de apagá-lo.

 

### Gerenciamento do computador

**Gerenciamento de computador** é uma coleção de ferramentas administrativas do Windows que ajudam você a solucionar um problema de computador. Você pode usar as ferramentas de **Gerenciamento do computador** no DART para ver as informações do sistema e os logs de eventos, gerenciar discos, listar Autoruns e gerenciar serviços e drivers. O console de **Gerenciamento do computador** é personalizado para ajudar você a diagnosticar e reparar problemas que possam impedir a inicialização do sistema operacional Windows.

### Explorador

A ferramenta do **Explorer** permite que você navegue no sistema de arquivos do computador e em compartilhamentos de rede para que você possa remover dados importantes que o usuário armazenou na unidade local antes de tentar reparar ou refazer a imagem do computador. E, como você pode mapear letras de unidade para compartilhamentos de rede, é fácil copiar e mover arquivos do computador para a rede para que ele possa ser restaurado ou da rede para o computador.

### Assistente de solução

O **Assistente de solução** apresenta uma série de perguntas e, em seguida, recomenda a melhor ferramenta para a situação, com base nas suas respostas. Este assistente ajuda você a determinar qual ferramenta usar quando você não estiver familiarizado com as ferramentas do DaRT.

### Configuração de TCP/IP

Quando você inicializa um computador com problema no DaRT, ele é definido para obter automaticamente a sua configuração de TCP/IP (endereço IP e servidor DNS) do protocolo DHCP (protocolo de configuração dinâmica de hosts). Se o DHCP estiver indisponível, você poderá configurar manualmente o TCP/IP usando a ferramenta de **configuração TCP/IP** . Primeiro, selecione um adaptador de rede e, em seguida, configure o endereço IP e o servidor DNS para esse adaptador.

### Desinstalação de hotfix

O **Assistente de desinstalação de hotfix** permite que você remova hotfixes ou Service Packs do sistema operacional Windows no computador que está reparando. Use essa ferramenta quando um hotfix ou Service Pack for suspeito para impedir que o sistema operacional seja iniciado.

Recomendamos que você desinstale apenas um hotfix de cada vez, mesmo que a ferramenta permita que você desinstale mais de um.

**Importante**  Os programas que foram instalados ou atualizados após a instalação de um hotfix podem não funcionar corretamente após a desinstalação de um hotfix.

 

### Verificação de SFC

A ferramenta de **verificação Sfc** inicia o **Assistente de reparo de arquivos do sistema** e permite reparar arquivos do sistema que impedem o início do sistema operacional Windows instalado. O **Assistente de reparo de arquivos do sistema** pode reparar automaticamente os arquivos de sistema corrompidos ou ausentes, ou pode notificá-lo antes que ele realize qualquer reparo.

### Pesquisar

Antes de recriar uma cópia de um computador, recuperar arquivos do disco rígido local é importante, especialmente quando o usuário pode não ter feito backup ou armazenado os arquivos em outro lugar.

A ferramenta de **pesquisa** abre uma janela de **pesquisa de arquivos** que você pode usar para localizar documentos quando você não conhece o caminho do arquivo ou para Pesquisar tipos gerais de arquivos em todos os discos rígidos locais. Você pode procurar padrões de nome de arquivo específicos em caminhos específicos. Você também pode limitar os resultados a um intervalo de datas ou intervalo de tamanho.

### Limpeza autônoma do sistema

**Importante**  Ambientes com o Standalone System Sweeper implantado devem, em vez disso, usar a imagem de proteção do Microsoft defender offline (WDO) para detecção de malware. Por causa de como a ferramenta standalone System Sweeper se integra ao DaRT, todas as implantações de versão do DaRT com suporte não podem aplicar essas atualizações Antimalware às imagens do DaRT.

 

O **standalone System Sweeper** pode ajudar a detectar malware e software indesejado e avisá-lo sobre riscos de segurança. Você pode usar essa ferramenta para examinar um computador e remover malware mesmo quando o sistema operacional do Windows instalado não está em execução. Quando o **standalone System Sweeper** detecta software mal-intencionado ou indesejado, ele solicita que você remova, deixe em quarentena ou permita a cada item.

Malware que usa rootkits podem se mascarar do sistema operacional em execução. Se um vírus ou spyware habilitado para rootkit estiver em um computador, a maioria das ferramentas de digitalização e remoção em tempo real não poderá mais vê-la ou removê-la. Como você inicializa o computador com problema no DaRT e o sistema operacional instalado está offline, você pode detectar o rootkit sem ser capaz de se mascarar.

### Conexão remota

A ferramenta **conexão remota** no DART permite que você execute remotamente as ferramentas DART em um computador de usuário final. Depois que algumas informações específicas forem fornecidas pelo usuário final (ou por um profissional de assistência técnica em funcionamento no computador do usuário final), o administrador de ti poderá assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.

**Importante**  Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.

 

## Tópicos relacionados


[Introdução ao DaRT 7.0](getting-started-with-dart-70-new-ia.md)

 

 





