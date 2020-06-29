---
title: Como instalar o servidor de publicação em um computador remoto
description: Como instalar o servidor de publicação em um computador remoto
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796385"
---
# Como instalar o servidor de publicação em um computador remoto


Use o procedimento a seguir para instalar o Publishing Server em um computador separado. Antes de executar o procedimento a seguir, verifique se o banco de dados e o servidor de gerenciamento estão disponíveis.

**Para instalar o Publishing Server em um computador separado**

1. Copie os arquivos de instalação do App-V 5,1 Server para o computador no qual você deseja instalá-lo. Para iniciar a instalação do App-V 5,1 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador. Clique em **Instalar**.

2. Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.

3. Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**. Clique em **Avançar**.

4. Na página **seleção de recursos** , marque a caixa de seleção **servidor de publicação** e clique em **Avançar**.

5. Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.

6. Na página **Configurar o Publishing Server Configuration** , especifique os seguintes itens:

   -   A URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado. Por exemplo, **http://ManagementServerName:12345** .

   -   Especifique o nome do site que você deseja usar para o serviço de publicação. Aceite o padrão se você não tiver um nome personalizado.

   -   Para a **Associação de portabilidade**, especifique um número de porta exclusivo que será usado pelo App-V 5,1, por exemplo, **54321**.

7. Na página **pronto para instalar** , clique em **instalar**.

8. Após a conclusão da instalação, o servidor de publicação deve ser registrado com o servidor de gerenciamento. No console de gerenciamento do App-V 5,1, use as etapas a seguir para registrar o servidor:

   1.  Abra o console do servidor de gerenciamento do App-V 5,1.

   2.  No painel esquerdo, selecione **servidores**e, em seguida, selecione **registrar novo servidor**.

   3.  Digite o nome do servidor e uma descrição (se necessário) e clique em **Adicionar**.

9. Para verificar se o servidor de publicação está funcionando corretamente, você deve importar um pacote para o servidor de gerenciamento, entitle o pacote a um grupo de anúncios e publicar o pacote. Usando um navegador da Internet, abra a seguinte URL: <strong> http://publishingserver:pubport </strong> . Se o servidor estiver executando corretamente, as informações semelhantes às seguintes serão exibidas:

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.1](deploying-app-v-51.md)

 

 





