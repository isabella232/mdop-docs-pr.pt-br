---
title: Como implantar o cliente do MBAM como parte de uma implantação do Windows
description: Como implantar o cliente do MBAM como parte de uma implantação do Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799567"
---
# Como implantar o cliente do MBAM como parte de uma implantação do Windows


O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização habilitando o gerenciamento e a criptografia de BitLocker em computadores cliente durante o processo de criação de imagens do computador e implantação do Windows.

**Observação**  
Para verificar os requisitos do sistema do cliente do MBAM, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).



A criptografia de computadores cliente com o BitLocker durante o estágio inicial da imagem de uma implantação do Windows pode reduzir a sobrecarga administrativa da implementação do MBAM. Essa abordagem também garante que todos os computadores implantados já tenham o BitLocker em execução e estejam configurados corretamente.

**Aviso**  
Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.



**Para criptografar um computador como parte da implantação do Windows**

1.  Se sua organização planeja usar o protetor TPM (Trusted Platform Module) ou as opções de protetor TPM + PIN no BitLocker, você deve ativar o chip TPM antes da implantação inicial do MBAM. Ao ativar o chip TPM, você evita uma reinicialização mais tarde no processo e garante que os chips do TPM sejam configurados corretamente de acordo com os requisitos da sua organização. Você deve ativar o chip TPM manualmente na BIOS do computador. Consulte a documentação do fabricante para obter mais detalhes sobre como configurar o chip TPM.

2.  Instale o agente do cliente MBAM.

3.  Recomendamos que você ingresse no computador em um domínio...

    -   Se o computador não estiver associado a um domínio, a senha de recuperação não será armazenada no serviço de recuperação de chave MBAM. Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.

    -   Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no servidor do MBAM, o computador precisará ser renovado. Nenhum método de recuperação está disponível.

4.  Abra um prompt de comando como administrador, interrompa o serviço do MBAM e, em seguida, defina o serviço como **manual** ou por **demanda**. Em seguida, execute os seguintes comandos:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Defina as configurações do registro para que o agente MBAM ignore a política de grupo e execute o TPM para que o **sistema operacional somente** execute a criptografia para fazer isso, execute o **regedit**e, em seguida, importe o modelo de chave do registro de c:\\Arquivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  Em regedit, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e defina as configurações listadas na tabela a seguir.

    Entrada do registro

    Definições de configuração

    Deploymenttime

    0 = DESATIVADO

    1 = usar configurações de política de tempo de implantação (padrão)

    UseKeyRecoveryService

    0 = não usar a caução de chave (as próximas duas entradas do registro não são necessárias nesse caso).

    1 = usar a caução chave no sistema de recuperação de chave (padrão)

    Recomendado: o computador deve ser capaz de se comunicar com o serviço de recuperação de chave. Verifique se o computador pode se comunicar com o serviço antes de prosseguir.

    Keyrecoveryoptions

    0 = somente chave de recuperação para carregar

    1 = carregar chave de recuperação e pacote de recuperação de chave (padrão)

    KeyRecoveryServiceEndPoint

    Defina esse valor como a URL para o servidor Web de recuperação de chave.

    Exemplo: http://de &lt; nome do computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. O agente MBAM reinicia o sistema durante a implantação do cliente do MBAM. Quando estiver pronto para esta reinicialização, execute o seguinte comando em um prompt de comando como administrador:

   **net start mbamagent**

8. Quando o computador for reiniciado e o BIOS solicitar que você aceite uma alteração no TPM, aceite a alteração.

9. Durante o processo de criação de imagens do sistema operacional cliente Windows, quando você estiver pronto para iniciar a criptografia, reinicie o serviço do agente MBAM. Em seguida, para definir start to **Automatic**, abra um prompt de comando como administrador e execute os seguintes comandos:

   **SC config mbamagent Start = auto**

   **net start mbamagent**

10. Remova os valores do registro de bypass. Para fazer isso, execute regedit, navegue até a entrada do registro HKLM\\SOFTWARE\\Microsoft, clique com o botão direito do mouse no nó **MBAM** e, em seguida, clique em **excluir**.

## Tópicos relacionados


[Implantando o Cliente do MBAM 1.0](deploying-the-mbam-10-client.md)









