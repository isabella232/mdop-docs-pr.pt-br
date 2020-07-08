---
title: Como instalar o Application Virtualization Streaming Server
description: Como instalar o Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797103"
---
# Como instalar o Application Virtualization Streaming Server


O servidor de streaming do Application Virtualization publica seus aplicativos para os clientes. Em um ambiente de carga balanceada, que é típico de implantações grandes, todos os servidores em um grupo de servidores devem transmitir os mesmos aplicativos. Se os servidores de streaming do Application Virtualization forem para transmitir diferentes aplicativos, atribua-os a grupos de servidores diferentes. Nesse caso, você também pode ter que aumentar a capacidade de um grupo de servidor.

Se você tiver designado um computador de destino na rede, com uma conta de logon com privilégios administrativos locais, poderá usar o procedimento a seguir para instalar o servidor de streaming do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.

**Observação**  O assistente de instalação pode criar um registro de grupo do servidor, se ele não existir, e um registro da associação do servidor de transmissão do Application Virtualization nesse grupo.

 

Depois de concluir o processo de instalação, reinicie o servidor.

**Para instalar um servidor de streaming do Application Virtualization**

1.  Verifique se nenhuma versão anterior do servidor de streaming do Application Virtualization está instalada em seu computador de destino.

    **Importante**  Verifique se o servidor de gerenciamento do App-V não está instalado neste computador. Os dois produtos não podem ser instalados no mesmo computador.

     

2.  Navegue até o local do programa de configuração do sistema virtualização do aplicativo na rede, execute esse programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo **Setup.exe** .

3.  Na página de **boas-vindas** , clique em **Avançar**.

4.  Na página **contrato de licença** , para aceitar os termos de licença, selecione **aceito os termos e as condições de licenciamento**e, em seguida, clique em **Avançar**.

5.  Na página **informações do cliente** , especifique o **nome de usuário** e a organização e clique em **Avançar**.

6.  Na página **caminho de instalação** , clique em **procurar**, especifique o local onde você deseja instalar o servidor de streaming e clique em **Avançar**.

7.  Na página **modo de segurança de conexão** , selecione o certificado desejado na lista suspensa e clique em **Avançar**.

    **Observação**  A configuração do **modo de conexão segura** exige que o servidor tenha um certificado do servidor provisionado para ele de uma infraestrutura de chave pública. Se um certificado do servidor não estiver instalado no servidor, essa opção não estará disponível e não poderá ser selecionada. Você deve conceder acesso de leitura à conta de serviço de rede para o certificado que está sendo usado.

     

8.  Na página **configuração de porta TCP** , para usar a porta padrão (554), selecione **usar porta padrão (554)**. Para especificar uma porta personalizada, selecione **usar porta personalizada**, especifique o número da porta no campo fornecido e clique em **Avançar**.

    **Observação**  Ao instalar o servidor em um cenário não seguro, você pode usar a porta padrão (554) ou pode definir uma porta personalizada.

     

9.  Na página **raiz do conteúdo** , especifique o local no computador de destino onde os arquivos do SFT serão salvos e clique em **Avançar**.

    **Observação**  Se a porta HTTP ou RTSP do servidor de streaming de aplicativo virtual já estiver alocada, você será solicitado a selecionar uma nova porta. Especifique a porta desejada e clique em **Avançar**.

     

10. Na tela **Configurações avançadas** , insira as seguintes informações:

    1.  **Máximo de conexões de cliente**

    2.  **Tempo limite de conexão (s)**

    3.  **Tamanho do pool de thread RTSP**

    4.  **Tempo limite RTSP (s)**

    5.  **Número de processos básicos**

    6.  **Tempo limite do núcleo (s)**

    7.  **Habilitar a autenticação do usuário**

    8.  **Habilitar a autorização do usuário**

    9.  **Tamanho do bloco do cache (KB)**

    10. **Tamanho máximo de cache (MB)**

    **Observação**  O servidor de streaming App-V usa permissões do sistema de arquivos NTFS para controlar o acesso aos aplicativos no compartilhamento de conteúdo. Use **habilitar a autenticação do usuário** e **habilitar a autorização do usuário** para controlar se o servidor verifica e impõe essas listas de controle de acesso (ACLs) ou não.

     

11. Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.

12. Na tela **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.

    **Importante**  A instalação pode demorar vários minutos para ser concluída. Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando que a instalação foi bem-sucedida.

    Não é necessário reiniciar o computador quando solicitado. No entanto, para otimizar o desempenho do sistema, recomendamos uma reinicialização.

     

13. Repita as etapas de 1 a 12 para cada servidor de aplicativos virtual que você precisa instalar.

## Tópicos relacionados


[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

 

 





