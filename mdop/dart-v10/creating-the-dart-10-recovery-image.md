---
title: Criação da imagem de recuperação do DaRT 10
description: Criação da imagem de recuperação do DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796192"
---
# Criação da imagem de recuperação do DaRT 10


Depois de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 10, você cria uma imagem de recuperação do DaRT 10. A imagem de recuperação inicia o Windows RE, no qual você pode iniciar as ferramentas do DaRT. Você pode gerar arquivos ISO (International Organization for Standardization) e imagens WIM (Windows Imaging Format). Além disso, você pode usar o PowerShell para gerar scripts que usam as configurações selecionadas no assistente de imagem de recuperação do DaRT. Você pode usar o script mais tarde para reconstruir imagens de recuperação usando as mesmas configurações. A imagem de recuperação fornece uma variedade de ferramentas de recuperação. Para obter uma descrição das ferramentas, consulte [visão geral das ferramentas no DART 10](overview-of-the-tools-in-dart-10.md).

Após inicializar o computador no DaRT, você pode executar as diferentes ferramentas do DaRT para tentar diagnosticar e reparar o computador. Esta seção apresenta o processo de criação da imagem de recuperação DaRT e permite selecionar as ferramentas e os recursos que você deseja incluir como parte da imagem.

Você pode criar a imagem de recuperação do DaRT usando um destes dois métodos:

-   Use o assistente de imagem de recuperação DaRT, que é executado em um ambiente do Windows.

-   Modifique um exemplo de script do PowerShell com os valores desejados. Para obter mais informações, consulte [como usar um script do PowerShell para criar a imagem de recuperação](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).

Você pode escrever o ISO em um CD ou DVD gravável, salvá-lo em uma unidade flash USB ou salvá-lo em um formato que você pode usar para inicializar o DaRT a partir de uma partição remota ou de uma partição de recuperação.

Depois de criar a imagem ISO, você pode gravá-la em um CD ou DVD em branco (se o computador tiver uma unidade de CD ou DVD). Se o seu computador não tiver uma unidade para essa finalidade, você pode usar os programas mais genéricos que são usados para gravar CDs ou DVDs.

## Selecione a arquitetura da imagem e especifique o caminho


Na página mídia do Windows 10, selecione se deseja criar uma imagem de recuperação do DaRT de 32 bits ou 64 bits. Use o Windows de 32 bits para compilar as imagens de recuperação do DaRT de 32 bits e o Windows de 64 bits para criar imagens de recuperação de 64 bits do DaRT. Você pode usar um único computador para criar imagens de recuperação para os dois tipos de arquitetura, mas não pode criar uma imagem que funcione nas arquiteturas de 32 bits e de 64 bits. Você também pode indicar o caminho da mídia de instalação do Windows 10. Escolha a arquitetura que corresponde a uma das imagens de recuperação que você está criando.

**Para selecionar a arquitetura da imagem e especificar o caminho**

1.  Na página **mídia do Windows 10** , selecione uma das seguintes opções:

    -   Se você estiver criando uma imagem de recuperação para computadores de 64 bits, selecione **criar uma imagem do DART x64 (64 bits)**.

    -   Se você estiver criando uma imagem de recuperação para computadores de 32 bits, selecione **criar uma imagem do DART x86 (32 bits)**.

2.  Na caixa **especificar o caminho raiz da mídia de instalação do Windows 10 &lt; 64 bits ou do 32-bit &gt; install** , digite o caminho dos arquivos de instalação do Windows 10. Use um caminho que corresponda à arquitetura da imagem de recuperação que você está criando.

3.  Clique em **Avançar**.

## Selecionar as ferramentas a serem incluídas na imagem de recuperação


Na página ferramentas, você pode selecionar várias ferramentas para incluir na imagem de recuperação. Essas ferramentas estarão disponíveis para os usuários finais quando forem inicializadas na imagem do DaRT. No entanto, se você habilitar a conectividade remota ao criar a imagem DaRT, todas as ferramentas estarão disponíveis quando um trabalho de suporte técnico se conectar ao computador do usuário final, independentemente de quais ferramentas você escolheu incluir na imagem.

Para restringir o acesso do usuário final a essas ferramentas, mas ainda manter o acesso completo às ferramentas por meio do Visualizador de conexão remota, não selecione essas ferramentas na página ferramentas. Os usuários finais poderão usar somente a conexão remota e poderão ver, mas não poderão, acessar qualquer ferramenta que você excluir da imagem de recuperação.

**Para selecionar as ferramentas a serem incluídas na imagem de recuperação**

1.  Na página **ferramentas** , marque a caixa de seleção ao lado de cada ferramenta que você deseja incluir na imagem.

2.  Clique em **Avançar**.

## Escolha se deseja permitir a conectividade remota por um suporte técnico


Na página conexão remota, você pode optar por habilitar um trabalhador de suporte técnico para conectar-se remotamente e executar as ferramentas DaRT no computador de um usuário final. A opção conectividade remota é exibida como uma opção disponível na janela diagnóstico e recuperação do conjunto de ferramentas. Depois que os funcionários do suporte técnico estabelecerem uma conexão remota, eles poderão executar as ferramentas DaRT no computador do usuário final a partir de um local remoto.

**Para escolher se a conectividade remota será permitida por profissionais de suporte técnico**

1.  Na página **conexão remota** , marque a caixa de seleção **permitir conexões remotas** para permitir conexões remotas ou desmarque a caixa de seleção para impedir conexões remotas.

2.  Se você desmarcou a caixa de seleção **permitir conexões remotas** , clique em **Avançar**. Caso contrário, vá para a próxima etapa para continuar a configuração da conectividade remota.

3.  Selecione uma destas opções:

    -   Deixe o Windows escolher um número de porta aberto.

    -   Especifique o número da porta. Se você selecionar essa opção, insira um número de porta entre 1 e 65535 no campo abaixo da opção. Este número de porta será usado ao estabelecer uma conexão remota. Recomendamos que o número da porta seja 1024 ou superior para minimizar a possibilidade de um conflito.

4.  (Opcional) na caixa de mensagem de **boas-vindas conexão remota** , crie uma mensagem personalizada que os usuários finais recebem quando estabelecem uma conexão remota. A mensagem pode ter no máximo 2048 caracteres.

5.  Clique em **Avançar**.

    Para obter mais informações sobre como executar as ferramentas do DaRT remotamente, consulte [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).

## Adicionar drivers à imagem de recuperação


Na guia Drivers da página de opções avançadas, você pode adicionar outros drivers de dispositivo que talvez sejam necessários ao reparar um computador. Geralmente, eles podem incluir armazenamento ou controladores de rede que o Windows 10 não fornece. Os drivers são instalados quando a imagem é criada.

**Importante**  Quando você selecionar os drivers a serem incluídos, lembre-se de que a conectividade sem fio (como Bluetooth ou 802.11 a/b/g/n) não é compatível com o DaRT.

 

**Para adicionar drivers à imagem de recuperação**

1.  Na página **Opções avançadas** , clique na guia **drivers** .

2.  Clique em **Adicionar**.

3.  Navegue até o arquivo a ser adicionado ao driver e clique em **abrir**.

    **Observação**  O arquivo de driver é fornecido pelo fabricante do controlador de armazenamento ou de rede.

     

4.  Repita as etapas 2 e 3 para cada driver que você deseja incluir.

5.  Clique em **Avançar**.

## Adicionar pacotes opcionais do WinPE à imagem de recuperação


Na guia WinPE da página de opções avançadas, você pode adicionar pacotes opcionais do WinPE à imagem do DaRT. Esses pacotes fazem parte do Windows ADK, que é um pré-requisito para a instalação do assistente de imagem de recuperação do DaRT. As ferramentas que você pode selecionar são todas opcionais. Todos os pacotes obrigatórios são adicionados automaticamente, com base nas ferramentas que você selecionou na página ferramentas.

Você também pode especificar o tamanho do espaço de trabalho. Espaço transitório é a quantidade de espaço em disco RAM que é reservada para que o DaRT seja executado. O espaço transitório é útil para o caso de o disco rígido do usuário final não estar disponível. Se você estiver executando ferramentas e drivers adicionais, talvez queira aumentar o espaço transitório.

**Para adicionar pacotes opcionais do WinPE à imagem de recuperação**

1.  Na página **Opções avançadas** , clique na guia **WinPE** .

2.  Marque a caixa de seleção ao lado de cada pacote que você deseja incluir na imagem ou clique na caixa de seleção **nome** para selecionar todos os pacotes.

3.  No campo **espaço transitório** , selecione a quantidade de espaço em disco RAM a ser alocada para executar o DART para o caso de o disco rígido do usuário final não estar disponível.

4.  Clique em **Avançar**.

## Adicionar as ferramentas de depuração do Crash Analyzer


Se você incluir a ferramenta Crash Analyzer na imagem ISO, também deverá incluir as ferramentas de depuração para Windows. Na guia Crash Analyzer da página de opções avançadas, você insere o caminho das ferramentas de depuração do Windows 10, que o analisador de falha usa para analisar os arquivos de despejo de memória. Você pode usar as ferramentas que estão no computador em que você está executando o assistente de imagem de recuperação DaRT ou pode usar as ferramentas que estão no computador do usuário final. Se você decidir usar as ferramentas no computador do usuário final, lembre-se de que cada computador que você diagnostica deve ter as ferramentas de depuração instaladas.

Se você tiver instalado o Microsoft Windows Software Development Kit (SDK) ou o Microsoft Windows Development Kit (WDK), as ferramentas de depuração do Windows 10 serão adicionadas à imagem de recuperação por padrão, e o caminho para as ferramentas de depuração será automaticamente preenchido. Você pode alterar o caminho das ferramentas de depuração do Windows 10 se os arquivos estiverem localizados em outro lugar além do local indicado pelo caminho de arquivo padrão. Um link no assistente permite baixar e instalar as ferramentas de depuração para Windows, caso ainda não estejam instaladas.

Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=266248). Instale as ferramentas de depuração para o local padrão.

**Observação**  O assistente do DaRT verifica as ferramentas na `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` chave do registro. Se o valor do registro não estiver lá, o assistente procurará em um dos seguintes locais, dependendo da arquitetura do sistema:

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**Para adicionar as ferramentas de depuração do Crash Analyzer**

1.  Na página **Opções avançadas** , clique na guia **analisador de falhas** .

2.  Adicionais Clique em **baixar as ferramentas de depuração** para baixar as ferramentas de depuração para Windows.

3.  Selecione uma das seguintes opções:

    -   **Inclua as ferramentas de depuração do Windows 10 &lt; 64 bits ou &gt; do 32-bit**. Se você selecionar essa opção, navegue até e selecione o local das ferramentas se o caminho ainda não estiver sendo exibido.

    -   **Use as ferramentas de depuração do sistema que está sendo depurado**. Se você selecionar essa opção, o Crash Analyzer não funcionará se as ferramentas de depuração para Windows não forem encontradas no computador com problema.

4.  Clique em **Avançar**.

## Selecionar os tipos de arquivos de imagem de recuperação a serem criados


Na página Criar imagem, escolha uma pasta de saída para a imagem de recuperação, insira um nome de imagem e selecione os tipos de arquivos de imagem de recuperação do DaRT a serem criados. Durante o processo de criação da imagem de recuperação, os arquivos de origem do Windows são descompactados, os arquivos DaRT são copiados para ele e a imagem é então "reempacotada" nos formatos de arquivo que você seleciona nesta página.

Os tipos de arquivos de imagem disponíveis são:

-   **Arquivo de imagem do Windows (WIM)** – usado para implantar o DART em um PXE (ambiente de execução de pré-inicialização) ou uma partição local).

-   **ISO (International Standards Organization)** – usada para implantação em CD ou DVD, ou para uso em máquinas virtuais (VM) s). O assistente requer que a imagem ISO tenha uma extensão de nome de arquivo. ISO porque a maioria dos programas que grava um CD ou DVD requer essa extensão. Se você não especificar um local diferente, a imagem ISO será criada na área de trabalho com o nome DaRT10. ISO.

-   **Script do PowerShell** – cria uma imagem de recuperação do DART com comandos que fornecem essencialmente as mesmas opções que você pode selecionar usando o assistente de imagem de recuperação do DART. O script também permite que você adicione ou altere arquivos na imagem de recuperação do DaRT.

Se você marcar a caixa de seleção Editar imagem nesta página, poderá personalizar a imagem de recuperação durante o processo de criação da imagem. Por exemplo, você pode alterar o arquivo "winpeshl.ini" para criar uma ordem de inicialização personalizada ou adicionar ferramentas de terceiros.

**Para selecionar os tipos de arquivos de imagem de recuperação a serem criados**

1.  Na página **criar imagem** , clique em **procurar** para escolher a pasta de saída para o arquivo de imagem.

    **Observação**  O tamanho da imagem vai variar, dependendo das ferramentas selecionadas e dos arquivos que você adicionar no assistente.

     

2.  Na caixa **nome da imagem** , insira um nome para a imagem de recuperação do DART ou aceite o nome padrão, que é DaRT10.

    O assistente cria uma subpasta no caminho de saída com esse nome.

3.  Selecione os tipos de arquivos de imagem que você deseja criar.

4.  Escolha uma das seguintes opções:

    -   Para alterar os arquivos na imagem de recuperação antes de criar os arquivos de imagem, marque a caixa de seleção **Editar imagem** e clique em **preparar**.

    -   Para criar a imagem de recuperação sem alterar os arquivos, clique em **criar**.

5.  

    Clique em **Avançar**.

## Editar os arquivos de imagem de recuperação


Você pode editar a imagem de recuperação somente se tiver marcado a caixa de seleção Editar imagem na página Criar imagem. Depois que a imagem de recuperação tiver sido preparada para edição, você poderá adicionar e modificar os arquivos de imagem de recuperação antes de criar a mídia inicializável. Por exemplo, você pode criar uma ordem personalizada para a inicialização, adicionar várias ferramentas de terceiros e assim por diante.

**Para editar os arquivos de imagem de recuperação**

1.  Na página **Editar imagem** , clique em **abrir** no Windows Explorer.

2.  Crie uma subpasta na pasta listada na caixa de diálogo.

3.  Copie os arquivos que você deseja para a nova subpasta ou remova os arquivos que não deseja.

4.  Clique em **criar** para começar a criar a imagem de recuperação.

## Gerar os arquivos de imagem de recuperação


Na página gerar arquivos, a imagem de recuperação do DaRT é gerada para os tipos de arquivo selecionados na página Criar imagem.

**Para gerar os arquivos de imagem de recuperação**

-   Na página **gerar arquivos** , clique em **Avançar** para gerar os arquivos de imagem de recuperação.

## Copiar a imagem de recuperação para um CD, DVD ou USB


Na página Criar mídia inicializável, você pode copiar opcionalmente o arquivo de imagem para um CD, DVD ou unidade flash USB (UFD). Você também pode criar mídia inicializável adicional desta página reiniciando o assistente.

**Observação**  O ambiente de execução de pré-inicialização (PXE) e a implantação de imagens locais não são suportados nativamente por essa ferramenta, pois exigem ferramentas empresariais adicionais, como o System Center Configuration Manager Server e o Microsoft Development Toolkit.

 

**Para copiar a imagem de recuperação para um CD, DVD ou USB**

1.  Na página **criar mídia inicializável** , selecione o arquivo ISO que você deseja copiar.

2.  Insira um CD, DVD ou USB e selecione a unidade.

    **Observação**  Se uma unidade não for reconhecida e você instalar uma nova unidade, você poderá clicar em **Atualizar** para forçar o assistente a atualizar a lista de unidades disponíveis.

     

3.  Clique no botão **criar mídia inicializável** .

4.  Para criar outra imagem de recuperação, clique em reiniciar ou clique em **fechar** se terminar de criar todas as mídias desejadas.

## Tópicos relacionados


[Visão geral das ferramentas do DaRT 10](overview-of-the-tools-in-dart-10.md)

[Implantação do DaRT 10](deploying-dart-10.md)

 

 





