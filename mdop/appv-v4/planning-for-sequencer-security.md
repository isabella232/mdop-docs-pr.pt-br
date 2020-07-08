---
title: Planejamento da segurança do Sequencer
description: Planejamento da segurança do Sequencer
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796820"
---
# Planejamento da segurança do Sequencer


Incorpore as práticas de implementação recomendadas o mais cedo possível ao configurar o Application Virtualization (App-V) para que a implementação do sequenciador seja funcional e mais segura. Se você já configurou o sequenciador, use as seguintes diretrizes de práticas recomendadas para revisitar as decisões de design e analisá-las de uma perspectiva de segurança.

**Importante**  
O sequenciador do App-V coleta e implanta todas as informações do aplicativo gravadas no computador que executa o sequenciador. Você deve garantir que todos os usuários que acessarem o computador executando o sequenciador tenham credenciais administrativas. Os usuários com credenciais de conta de usuário não devem ter acesso para controlar o conteúdo e os arquivos de pacote do pacote. Se você estiver sequenciando em um computador que esteja executando serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal), verifique se ele é um computador dedicado ao sequenciamento e se os usuários com credenciais de conta de usuário não estão conectados a ele durante o sequenciamento.



## Práticas recomendadas de segurança do sequenciador


Considere os cenários a seguir e as práticas recomendadas associadas ao implementar e usar o sequenciador do Application Virtualization (App-V):

-   **Verificação de vírus no computador que executa o sequenciador**— é recomendável que você verifique o computador que executa o sequenciador em busca de vírus e desabilite o software de detecção de malware e malware no computador que executa o sequenciador durante o processo de sequenciamento. Isso irá acelerar o processo de sequenciamento e impedir que os componentes do software antivírus e anti-malware interfiram no processo de sequenciamento. Em seguida, instale o pacote sequenciado em um computador que não esteja executando o sequenciador e, após a instalação bem-sucedida, verifique se há vírus no computador. Se forem encontrados vírus, o fabricante do software deve ser contatado para informá-los dos arquivos de origem infectados e solicitar uma fonte de instalação atualizada sem vírus. Opcionalmente, o sequenciador pode ser verificado após a fase de instalação e, se um vírus for encontrado, o fabricante do software deve ser contatado conforme mencionado acima.

    **Observação**  
    Se um vírus for detectado em um aplicativo, o aplicativo não deve ser implantado nos computadores de destino.



-   A **captura de listas de controle de acesso (ACLs) em arquivos NTFS**— o sequenciador do App-V captura permissões do sistema de arquivos NTFS para os arquivos monitorados durante a instalação do produto. Esse recurso permite que você duplique com mais precisão o comportamento pretendido do aplicativo, como se tivesse sido instalado localmente e não virtualizado. Em alguns cenários, um aplicativo pode armazenar informações que os usuários não se destinam a acessar nos arquivos do aplicativo. Por exemplo, um aplicativo pode armazenar informações de credenciais em um arquivo dentro do aplicativo. Se as ACLs não forem impostas no pacote, um usuário poderá visualizar e usar essas informações fora do aplicativo.

    **Observação**  
    Você não deve sequenciar aplicativos que armazenam informações específicas de segurança não criptografadas, como senhas e assim por diante.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   O **sequenciador não captura ACLs do registro**— embora o sequenciador Capture as ACLs do sistema de arquivos NTFS durante a fase de instalação do sequenciamento, ele não captura as ACLs para o registro. Os usuários terão acesso total a todas as chaves do registro para aplicativos virtuais, exceto para serviços. No entanto, se um usuário modificar o registro de um aplicativo virtual, a alteração será armazenada em uma loja específica (**uservol \ _sftfs \ _v1. pkg**) e não afetará outros usuários.

-   **Serviços de aplicativo**– App-V fornece suporte para serviços de aplicativo que fazem parte de um aplicativo virtualizado. No entanto, no ambiente virtual, o contexto de segurança em que ele será executado será limitado. Os únicos contextos de segurança com suporte em um ambiente virtual são sistema local, serviço local e serviço de rede. Durante o sequenciamento, se um contexto de segurança for especificado para um serviço de aplicativo diferente dos três suportados, o contexto de segurança do sistema local será aplicado no ambiente virtual. Se o serviço de aplicativo estiver configurado para usar o serviço local ou o serviço de rede, ele será respeitado no ambiente virtual. Configurar a conta de serviço pode ser feita durante o processo de sequenciamento usando esses três contextos de segurança.

-   **Informações de segurança persistentes**— ao sequenciar aplicativos, você pode instalar o aplicativo como um usuário ou pode desenvolver um método automatizado para a instalação do aplicativo durante a monitoração. Tudo que não está sendo excluído do pacote será capturado como parte desse pacote para que o aplicativo tenha os ativos necessários para serem executados em um ambiente virtualizado. Alguns aplicativos armazenam informações de segurança confidenciais (como senhas) durante a instalação; se persistentes não protegidos, essas informações de segurança poderão ser acessadas por outros usuários com acesso ao pacote. Durante a instalação, se uma instalação de aplicativo solicitar uma senha ou outras informações confidenciais de segurança, verifique com a documentação se ela não é persistente (removida após a instalação) ou, se persistiu, se ela está protegida (criptografada).

-   **Proteger pacotes de aplicativos virtuais**— sempre salve pacotes de aplicativos virtuais em um local seguro na rede para impedir que o pacote seja adulterado ou corrompido.

## Tópicos relacionados


[Planejamento de segurança e proteção](planning-for-security-and-protection.md)









