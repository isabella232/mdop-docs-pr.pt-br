---
title: Como instalar manualmente o Application Virtualization Client
description: Como instalar manualmente o Application Virtualization Client
author: dansimp
ms.assetid: bb67f70b-d525-4317-b254-e4f084c717ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cb41b5e51bd33c377b17c088e97cb54f1a57685
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797054"
---
# Como instalar manualmente o Application Virtualization Client

Há dois tipos de componentes de cliente de virtualização de aplicativos: o cliente de desktop de virtualização de aplicativos, que foi projetado para instalação em computadores de mesa e o cliente de virtualização de aplicativos para serviços de área de trabalho remota (anteriormente serviços de terminal), que podem ser instalados em servidores de sessão de área de trabalho remota (host da Sessão RD). Embora os dois programas do Client Installer sejam diferentes, você pode usar o procedimento a seguir para instalar manualmente o cliente da área de trabalho do Application Virtualization em um único computador desktop ou o cliente do Application Virtualization para serviços de área de trabalho remota em um único servidor host da sessão da área de trabalho remota. Em um ambiente de produção, você provavelmente instalará o cliente de desktop do Application Virtualization em vários computadores desktop com um processo de instalação automatizado com script. Para obter informações sobre como instalar vários clientes usando um processo de instalação com script, consulte [como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md).

**Observação**  
1. Se você estiver instalando o aplicativo cliente do Application Virtualization para serviços de área de trabalho remota em um servidor de host de sessão de área de trabalho remota, avise os usuários que têm uma sessão de cliente RDP ou ICA aberta com o servidor host da sessão da área de trabalho remota em que devem salvar o trabalho e fechar as sessões deles. Em uma sessão de área de trabalho remota, você pode instalar o cliente manualmente. Para obter mais informações sobre como atualizar o cliente, consulte [como atualizar o cliente do Application Virtualization](how-to-upgrade-the-application-virtualization-client.md).

2. Se você tiver qualquer configuração no computador do usuário que dependa do caminho de instalação do cliente, observe que o cliente do Application Virtualization (App-V) 4,5 usa uma pasta de instalação diferente das versões anteriores. Por padrão, uma nova instalação do cliente do Application Virtualization (App-V) 4,5 será instalada na pasta do cliente \\Program Files\\Microsoft Application Virtualization. Se uma versão anterior do cliente já estiver instalada, a instalação do cliente App-V executará uma atualização para a pasta de instalação existente.

**Observação**  
Para o App-V versão 4,6 e posterior, quando o cliente App-V está instalado, o SFTLDR.DLL é instalado no diretório Windows\\system32. Se o cliente App-V estiver instalado em um sistema de 64 bits, o SFTLDR\_WOW64.DLL será instalado no diretório Windows\\SysWOW64

**Para instalar manualmente o cliente da área de trabalho do Application Virtualization**

1. Depois de obter o arquivo morto correto do instalador e salvá-lo em seu computador, verifique se você está conectado com uma conta com direitos de administrador no computador e clique duas vezes no arquivo para expandir o arquivo.

2. Escolha a pasta na qual deseja salvar os arquivos e, em seguida, abra a pasta após a cópia dos arquivos.

3. Revise as notas de versão, se apropriado.

4. Navegue até localizar o arquivo setup.exe e clique duas vezes setup.exe para iniciar a instalação.

5. O assistente verifica o sistema para garantir que todos os pré-requisitos de software estejam instalados e, se qualquer uma das seguintes opções estiverem ausentes, o assistente solicitará automaticamente que você instale-os:

    - Pacote redistribuível do Microsoft Visual C++ 2005 SP1 (x86)

    - Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)

    - Relatório de erros do aplicativo Microsoft

    **Observação**  
    Para o App-V versão 4,6 e posterior, o assistente também instalará o pacote redistribuível do Microsoft Visual C++ 2008 SP1 (x86).

    Para obter mais informações sobre como instalar o Microsoft Visual C++ 2008 SP1 Redistributable Package (x86), consulte [https://go.microsoft.com/fwlink/?LinkId=150700](https://go.microsoft.com/fwlink/?LinkId=150700) .

    Se solicitado, clique em **instalar**. O progresso da instalação é exibido, e o status muda de **pendente** para **instalação**. O status de instalação muda para **bem-sucedida** à medida que cada etapa é concluída com êxito.

6. Quando o **Assistente do cliente de desktop do Microsoft Application Virtualization – InstallShield** for exibido, clique em **Avançar**.

7. A tela **contrato de licença** será exibida. Leia o contrato de licença e, se concordar, clique em **aceito os termos do contrato de licença** e, em seguida, clique em **Avançar**.

   Opcionalmente, você pode clicar no botão para ler a política de privacidade. Você deve estar conectado à Internet para acessar a declaração de privacidade.

8. Na tela **tipo de configuração** , selecione o tipo de configuração. Clique em **típico** para usar os valores de programa padrão ou clique em **personalizado** se desejar definir as configurações do programa durante a instalação.

9. Se você escolher **normal**, a próxima tela exibirá **pronto para instalar o programa**. Clique em **instalar** para começar a instalação.

10. Se você escolher **personalizado**, a tela de **pasta de destino** será exibida.

11. Na tela de **pasta de destino** , clique em **Avançar** para aceitar a pasta padrão ou clique em **alterar** para exibir a tela alterar a **pasta de destino atual** . Navegue até ou, no campo **nome da pasta** , insira a pasta de destino, clique em **OK**e clique em **Avançar**.

12. Na tela **local de dados do Application Virtualization** , clique em **Avançar** para aceitar os locais de dados padrão ou conclua as seguintes ações para alterar o local em que os dados são armazenados:

    1. Clique em **alterar**e, em seguida, navegue até ou, no campo **local dos dados globais** , insira a pasta de destino do local de dados globais e clique em **OK**. O diretório de dados globais é onde o cliente da área de trabalho do Application Virtualization armazena em cache os dados compartilhados por todos os usuários do computador, como arquivos OSD e dados de arquivo SFT.

    2. Se você quiser alterar a letra da unidade a ser usada, selecione a letra da unidade preferida na lista suspensa.

    3. Insira um novo caminho para armazenar os dados específicos do usuário no campo **local de dados específicos do usuário,** se você quiser alterar o local dos dados. O diretório de dados do usuário é onde o cliente da área de trabalho do Application Virtualization armazena informações específicas do usuário, como configurações pessoais para aplicativos virtualizados.

       **Observação**  
       Esse caminho deve ser diferente para cada usuário, portanto, deve incluir uma variável de ambiente específica do usuário ou uma unidade mapeada ou outra coisa que será resolvida para um caminho exclusivo para cada usuário.

    4. Quando terminar de fazer as alterações, clique em **Avançar**.

13. Na tela **configurações de tamanho do cache** , você pode aceitar ou alterar o tamanho padrão do cache. Clique em um dos seguintes botões de opção para escolher como gerenciar o espaço do cache:

    1. **Use o tamanho máximo do cache**. Insira um valor numérico de 100 a 1048576 (1 TB) no campo **tamanho máximo (MB)** para especificar o tamanho máximo do cache.

    2. **Use o limite de espaço livre em disco**. Insira um valor numérico para especificar a quantidade de espaço livre em disco, em MB, que o cliente do Application Virtualization deve deixar disponível no disco. Isso permite que o cache cresça até que a quantidade de espaço livre em disco atinja esse limite. O valor mostrado em **espaço livre em disco restante** indica o quanto espaço em disco não está sendo usado no momento.

    **Importante**  
    Para garantir que o cache tem espaço suficiente alocado para todos os pacotes que podem ser implantados, use a configuração **usar o limite de espaço em disco livre** ao configurar o cliente para que o cache possa crescer conforme necessário. Ou, se preferir, determine com antecedência quanto espaço em disco será necessário para o cache do App-V e, no momento da instalação, defina o tamanho do cache de acordo. Para obter mais informações sobre o recurso de gerenciamento de espaço de cache, no guia de operações do Microsoft Application Virtualization (App-V), consulte **como usar o recurso de gerenciamento de espaço em cache**.

    Clique em **Avançar** para continuar.

14. Nas seções a seguir da tela de **configuração de política do pacote de tempo de execução** , você pode alterar os parâmetros que afetam a forma como o cliente de virtualização do aplicativo se comporta durante o tempo de execução:

    1. **Raiz da fonte do aplicativo**. Especifica o local dos arquivos SFT. Se usado, substitui as partes de protocolo, servidor e porta da URL de CODEBASE HREF no arquivo OSD.

    2. **Autorização do aplicativo**. Quando **exigir a autorização do usuário, mesmo quando o cache** estiver marcado, os usuários deverão se conectar a um servidor e validar as credenciais pelo menos uma vez antes de permitirem o início de cada aplicativo virtual.

    3. **Permitir streaming de arquivo**. Indica se o streaming do arquivo será habilitado, independentemente de como o campo **raiz da fonte do aplicativo** será usado. Se não estiver marcada, o streaming de arquivos estará desabilitado. Isso deve ser verificado se a **raiz da fonte do aplicativo** contiver um caminho UNC na forma \\\\server\\share.

    4. **Carregar aplicativo automaticamente**. Controla quando e como ocorre a carga de fundo automática dos aplicativos.

       **Observação**  
       Quando você instala o cliente App-V para usar com um cache somente leitura, por exemplo, com uma implementação de servidor VDI, defina **quais aplicativos serão carregados** automaticamente para não **carregar aplicativos automaticamente** para impedir que o cliente tente atualizar aplicativos no cache somente leitura.

    Clique em **Avançar** para continuar.

15. Na tela do **Publishing Server** , marque a caixa de seleção **configurar um servidor de publicação agora** se você quiser definir um servidor de publicação ou clique em **Avançar** se quiser concluir isso mais tarde. Para definir um servidor de publicação, especifique as seguintes informações:

    1. **Nome para exibição**— Insira o nome que você deseja exibir para o servidor.

    2. **Tipo**— selecione o tipo de servidor na lista suspensa de tipos de servidor.

    3. **Nome** e **porta**do host — Insira o nome do host e a porta nos campos correspondentes. Quando você selecionar um tipo de servidor na lista suspensa, o campo porta será automaticamente preenchido com os números de porta padrão. Para alterar um número de porta, clique no tipo de servidor na lista e altere o número da porta de acordo com as suas necessidades.

    4. **Caminho**— se você tiver selecionado **servidor http padrão** ou **servidor http de segurança avançada**, será necessário inserir o caminho completo do arquivo XML que contém dados de publicação neste campo. Se você selecionar o **aplicativo do Application Virtualization** ou o **servidor de virtualização de segurança avançada**, esse campo não estará ativo.

    5. **Entre em contato com este servidor automaticamente para atualizar as configurações quando um usuário faz logon**: Marque esta caixa de seleção se desejar que esse servidor seja consultado automaticamente quando os usuários entrarem na conta do cliente do Application Virtualization.

    6. Quando terminar com as etapas de configuração, clique em **Avançar**.

16. Na tela **pronto para instalar o programa** , clique em **instalar**. Será exibida uma tela que mostra o progresso da instalação.

17. Na tela **Assistente para instalação concluída** , clique em **concluir**.

    **Observação**  
    Se a instalação falhar por algum motivo, talvez seja necessário reiniciar o computador antes de tentar a instalação novamente.

## Tópicos relacionados

[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Visão geral de cenário de entrega autônoma](stand-alone-delivery-scenario-overview.md)
