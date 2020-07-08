---
title: Como compartilhar pastas entre o host e o espaço de trabalho do MED-V
description: Como compartilhar pastas entre o host e o espaço de trabalho do MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799735"
---
# Como compartilhar pastas entre o host e o espaço de trabalho do MED-V


Você pode compartilhar pastas entre o host e o espaço de trabalho do MED-V. As pastas compartilhadas podem ser armazenadas no seguinte:

-   Um computador externo na rede

-   O computador host

Os procedimentos a seguir demonstram como compartilhar pastas entre o host e o espaço de trabalho do MED-V.

**Para compartilhar pastas localizadas na rede**

1.  Configure o MED-V no modo de área de trabalho completo.

2.  No gerenciamento do MED-V, na guia rede, clique em **usar um endereço IP diferente do host (ponte)**.

3.  Faça o seguinte no computador host:

    1.  No painel de controle, clique em **Exibir o status e as tarefas da rede**e defina **descoberta de rede** como **ativada**.

    2.  No menu Iniciar, clique com o botão direito do mouse em **computador**e clique em **Mapear unidade de rede**.

    3.  Na caixa de diálogo **Mapear unidade de rede** , no campo **unidade** , selecione uma unidade.

        **Observação**  Verifique se a mesma letra de unidade não está em uso em ambos os computadores.

         

    4.  Clique em **Procurar**.

    5.  Na caixa de diálogo **Procurar pasta** , navegue até a unidade compartilhada e clique em **OK**.

    6.  Clique em **concluir**.

4.  Repita a etapa 3 no espaço de trabalho do MED-V. Aponte para a mesma unidade do computador host.

**Para compartilhar pastas localizadas no host**

1.  Configure a pasta a ser compartilhada com as permissões apropriadas.

2.  No espaço de trabalho do MED-V, vá para **meus locais de rede** e localize a pasta compartilhada.

3.  No espaço de trabalho do MED-V, localize a pasta compartilhada.

**Observação**  Certifique-se de que os computadores do espaço de trabalho do host e do espaço de trabalho do MED-V estejam no mesmo domínio ou grupo de trabalho.

 

 

 





