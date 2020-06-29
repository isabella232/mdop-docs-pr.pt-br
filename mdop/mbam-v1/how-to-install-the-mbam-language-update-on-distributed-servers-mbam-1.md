---
title: Como instalar a atualização de idioma do MBAM em servidores distribuídos
description: Como instalar a atualização de idioma do MBAM em servidores distribuídos
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799724"
---
# Como instalar a atualização de idioma do MBAM em servidores distribuídos


O monitoramento e administração do Microsoft BitLocker (MBAM) inclui quatro funções de servidor que podem ser executadas em um ou mais computadores. No entanto, somente dois recursos do MBAM Server exigem a atualização para dar suporte à instalação da versão de idioma do MBAM 1,0 e do modelo de política de MBAM. Em configurações com os recursos do MBAM Server instalados em vários computadores, somente os seguintes recursos do servidor precisam ser atualizados:

-   A conformidade e os relatórios de auditoria do MBAM

-   O servidor de administração e monitoramento do MBAM

**Importante**  Os recursos do servidor do MBAM devem ser atualizados nesta ordem: primeiro os relatórios de conformidade e auditoria e, em seguida, o servidor de administração e monitoramento. Os modelos de política de grupo do MBAM podem ser atualizados a qualquer momento, sem preocupação com a sequência.

 

**Para instalar a atualização de idioma do MBAM no recurso servidor de relatório de auditoria e conformidade do MBAM**

1.  No computador que executa o recurso de relatório conformidade e auditoria do MBAM, localize e execute o assistente de configuração de atualização de idioma do MBAM (MBAMsetup.exe).

2.  Conclua o assistente para os relatórios de conformidade e auditoria e, em seguida, feche o assistente.

**Para instalar a atualização de idioma do MBAM no recurso de servidor administração e monitoramento do MBAM**

1.  No computador que está executando o recurso de administração e monitoramento do MBAM, abra o console de gerenciamento dos serviços de informações da Internet (IIS), vá para **sites**e, em seguida, desligue o site de administração e monitoramento do Microsoft BitLocker.

2.  Escolha Editar as associações para o site do MBAM e modifique as associações do site. Por exemplo, altere a porta de 443 para 9443.

3.  Localize e execute o assistente de configuração de atualização de idioma do MBAM (MBAMsetup.exe). Conclua o assistente para o recurso de administração e monitoramento do servidor e, em seguida, feche o assistente.

4.  Após atualizar o banco de dados do servidor, abra o console de gerenciamento do IIS e examine as associações do site de administração e monitoramento do Microsoft BitLocker.

5.  Exclua a associação antiga e certifique-se de que a associação restante tenha o nome de host, certificado e número de porta corretos para a configuração empresarial do MBAM.

6.  Reinicie o site da MBAM.

7.  Teste a funcionalidade do site da Web do MBAM:

    -   Abra a interface da Web do MBAM e certifique-se de que você possa obter uma chave de recuperação para um cliente.

    -   Impor a criptografia de um computador cliente novo ou manualmente descriptografado.

        **Observação**  O cliente MBAM será aberto apenas se puder se comunicar com o banco de dados de recuperação e de hardware.

         

## Tópicos relacionados


[Implantação da Atualização da Versão de Idioma do MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





