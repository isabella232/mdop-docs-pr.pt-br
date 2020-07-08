---
title: Como configurar um pacote de implantação
description: Como configurar um pacote de implantação
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799774"
---
# Como configurar um pacote de implantação


O assistente de empacotamento percorre a criação de um pacote criando uma pasta em seu computador local e transferindo todos os arquivos de instalação necessários para a pasta única. O conteúdo da pasta pode ser movido para várias unidades de mídia removível para distribuição.

**Observação**  
Um único pacote não pode conter arquivos de instalação para sistemas x86 e x64.



## Como criar um pacote de implantação


**Para criar um pacote de implantação**

1. Verifique no módulo **imagens** que você criou pelo menos uma imagem empacotada local.

2. No menu **ferramentas** , selecione **Assistente de empacotamento**.

3. Na página Bem-vindo ao **Assistente de empacotamento** , clique em **Avançar**.

4. Na página **imagem do espaço de trabalho** , marque a caixa de seleção **incluir imagem no pacote** para incluir uma imagem no pacote.

   O campo de **imagem** está habilitado.

   **Observação**  
   Uma imagem não é necessária em um pacote do MED-V; o pacote pode ser criado sem uma imagem. Nesse caso, a imagem deve ser carregada no servidor para que possa ser descarregada posteriormente pela rede para o cliente ou enviada para uma pasta pré-estágio de imagem.



5. Clique na lista de **imagens** para ver todas as imagens disponíveis. Selecione a imagem a ser copiada para o pacote. Clique em **Atualizar** para atualizar a lista de imagens disponíveis.

6. Clique em **Avançar**.

7. Na página **configurações de instalação do MED-v** , selecione o arquivo de instalação do MED-v seguindo um destes procedimentos:

   -   No campo **arquivo de instalação do MED-V** , digite o caminho completo do diretório onde o arquivo de instalação está localizado.

   -   Clique em **..** . para navegar até o diretório onde o arquivo de instalação está localizado.

   **Observação**  
   Este campo é obrigatório, e o assistente não continuará sem um nome de arquivo válido.



8. No campo **endereço do servidor** , digite o nome ou o endereço IP do servidor.

9. No campo **porta do servidor** , digite a porta do servidor.

10. Selecione a caixa de seleção o **servidor é acessado usando HTTPS** para exigir uma conexão HTTPS para se conectar ao servidor.

11. Siga um destes procedimentos:

    -   Clique em **configurações de instalação padrão**e, em seguida, clique em **Avançar** para continuar e deixar as configurações padrão.

    -   Clique em **configurações de instalação personalizadas**e, em seguida, clique em **Avançar** para personalizar as configurações de instalação.

        1.  Na página **configurações personalizadas da instalação do MED-V** , no campo **pasta de instalação** , digite o caminho da pasta na qual os arquivos MED-V serão instalados no computador host.

            **Observação**  
            É recomendável usar variáveis no caminho, em vez de constantes, que podem variar de um computador para o computador.

            Por exemplo, use *%ProgramFiles%\\MED-V* em vez de *c:\\MED-V*.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. Na página **instalações adicionais** , marque a caixa de seleção **incluir a instalação da software de virtualização** para incluir a instalação do Virtual PC no pacote.

    O campo **arquivo de instalação** está habilitado. Digite o caminho completo do arquivo de instalação do software de virtualização ou clique em **...** para navegar até o diretório.

13. Marque a caixa de seleção **incluir a instalação do Virtual PC QFE** para incluir a instalação da atualização do Virtual PC no pacote.

    O campo **arquivo de instalação** está habilitado. Digite o caminho completo do arquivo de instalação da atualização do Virtual PC ou clique em **..** . para navegar até o diretório.

14. Marque a caixa de seleção **incluir a instalação do Microsoft .NET framework 2,0** para incluir a instalação do Microsoft .net Framework 2,0 no pacote.

    O campo **arquivo de instalação** está habilitado. Digite o caminho completo do arquivo de instalação do Microsoft .NET Framework 2,0 ou clique em **...** para navegar até o diretório.

15. Clique em **Avançar**.

16. Na página **finalizar** , selecione o local onde o pacote deve ser salvo seguindo um destes procedimentos:

    -   No campo **destino do pacote** , digite o caminho completo do diretório em que o pacote deve ser salvo.

    -   Clique em **..** . para navegar até o diretório em que os arquivos de instalação devem ser salvos.

    **Observação**  
    A criação do pacote pode consumir mais espaço do que o tamanho real do pacote. Portanto, é recomendável construir o pacote no disco rígido. Após a criação do pacote, ele pode ser copiado para o USB.



17. No campo **nome do pacote** , insira um nome para o pacote.

18. Clique em **concluir** para criar o pacote.

    O pacote será criado. Isso pode levar alguns minutos.

    Após a criação do pacote, será exibida uma mensagem informando que ele foi concluído com êxito.

**Observação**  
Se você salvou todos os arquivos localmente, e não diretamente na mídia removível, certifique-se de copiar somente o conteúdo da pasta e não a própria pasta para a mídia removível.



**Observação**  
A mídia removível deve ser grande o suficiente para que o conteúdo do pacote consuma um máximo de apenas três trimestres da memória da mídia removível.



**Observação**  
Ao criar o pacote, até o dobro do tamanho do pacote real pode ser necessário quando a compilação é concluída.



## Tópicos relacionados


[Criando uma imagem do MED-V](creating-a-med-v-image.md)









