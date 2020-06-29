---
title: Como instalar a atualização de idiomas do MBAM em um servidor único
description: Como instalar a atualização de idiomas do MBAM em um servidor único
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799535"
---
# Como instalar a atualização de idiomas do MBAM em um servidor único


O monitoramento e administração do Microsoft BitLocker (MBAM) inclui quatro funções de servidor que podem ser executadas em um ou mais computadores. No entanto, somente dois recursos do MBAM Server exigem a atualização para suportar a instalação da versão de idioma do MBAM 1,0 e o modelo de política de MBAM. Para atualizar todos os três recursos de MBAM necessários a serem instalados em um computador, execute as etapas descritas neste tópico.

**Para instalar a atualização de idioma do MBAM em um único servidor**

1.  Abra o console de gerenciamento dos serviços de informações da Internet (IIS), vá para **sites**e, em seguida, desligue o site de administração e monitoramento do Microsoft BitLocker.

2.  Edite as associações do site do MBAM e modifique temporariamente as associações do site. Por exemplo, altere a porta de 443 para 9443.

3.  Localize e execute o assistente de configuração do MBAM (MBAMsetup.exe) e selecione os três recursos a seguir:

    1.  Relatórios de conformidade e auditoria

    2.  Servidor de administração e monitoramento

    3.  Modelos de política de grupo

    **Importante**  Os recursos do servidor do MBAM devem ser atualizados na seguinte ordem: relatórios de conformidade e auditoria primeiro, administração e monitoramento do servidor. Os modelos de política de grupo podem ser atualizados a qualquer momento, sem preocupação com a sequência.

     

4.  Após atualizar o banco de dados do servidor, abra o console de gerenciamento do IIS e examine as associações do site de administração e monitoramento do Microsoft BitLocker.

5.  Exclua uma das associações e certifique-se de que a associação restante tenha o nome de host, certificado e número de porta corretos para a configuração empresarial do MBAM.

6.  Reinicie o site do MBAM.

7.  Teste a funcionalidade do site do MBAM:

    -   Abra a interface da Web do MBAM e verifique se é possível buscar uma chave de recuperação para um cliente.

    -   Impor a criptografia de um computador cliente novo ou manualmente descriptografado.

        **Observação**  O cliente MBAM será aberto apenas se puder se comunicar com o banco de dados de recuperação e de hardware.

         

## Tópicos relacionados


[Implantação da Atualização da Versão de Idioma do MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





