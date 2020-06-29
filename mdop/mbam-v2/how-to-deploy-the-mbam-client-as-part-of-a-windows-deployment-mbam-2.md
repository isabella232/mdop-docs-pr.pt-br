---
title: Como implantar o cliente do MBAM como parte de uma implantação do Windows
description: Como implantar o cliente do MBAM como parte de uma implantação do Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799509"
---
# Como implantar o cliente do MBAM como parte de uma implantação do Windows


O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. Se computadores que têm um chip TPM (Trusted Platform Module), o cliente BitLocker pode ser integrado a uma organização habilitando o gerenciamento e a criptografia de BitLocker em computadores cliente como parte do processo de implantação e implantação de imagens do Windows.

**Observação**  
Para verificar os requisitos do sistema do cliente de administração e administração do Microsoft BitLocker, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



A criptografia de computadores cliente com o BitLocker durante o estágio inicial da criação de imagens de uma implantação do Windows pode reduzir a sobrecarga administrativa necessária para implementar o MBAM em uma organização. Ele também garante que todos os computadores implantados já tenham o BitLocker em execução e estejam configurados corretamente.

**Observação**  
O procedimento neste tópico descreve como modificar o registro do Windows. Usar o editor do registro incorretamente pode causar sérios problemas que podem exigir a reinstalação do Windows. A Microsoft não pode garantir que os problemas resultantes do uso incorreto do editor do registro possam ser resolvidos. Use o editor do registro por sua conta e risco.



**Para criptografar um computador como parte da implantação do Windows**

1.  Se sua organização planeja usar o protetor TPM (Trusted Platform Module) ou as opções de protetor TPM + PIN no BitLocker, você deve ativar o chip TPM antes da implantação inicial do MBAM. Ao ativar o chip TPM, você evita uma reinicialização mais tarde no processo e garante que os chips do TPM sejam configurados corretamente de acordo com os requisitos da sua organização. Você deve ativar o chip TPM manualmente no BIOS do computador.

    **Observação**  
    Alguns fornecedores fornecem ferramentas para ativar e ativar o chip TPM no BIOS de dentro do sistema operacional. Consulte a documentação do fabricante para obter mais detalhes sobre como configurar o chip TPM.



2.  Instale o agente cliente de administração e administração do Microsoft BitLocker.

3.  Ingressar no computador em um domínio (recomendado).

    -   Se o computador não estiver associado ao domínio, a senha de recuperação não será armazenada no serviço de recuperação de chave MBAM. Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.

    -   Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no servidor do MBAM, o computador precisará ser renovado. Nenhum método de recuperação está disponível.

4.  Execute o prompt de comando como administrador, interrompa o serviço do MBAM e, em seguida, defina o serviço como **manual** ou por **demanda**e, em seguida, comece digitando os seguintes comandos:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Defina as configurações do registro para o agente MBAM para ignorar a política de grupo e executar o TPM para **apenas a criptografia do sistema operacional** executando o **regedit**e, em seguida, importando o modelo de chave do registro de c:\\Arquivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  Em regedit, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e defina as configurações listadas na tabela a seguir.

    Entrada do registro

    Definições de configuração

    Deploymenttime

    0 = DESATIVADO

    1 = usar configurações de política de tempo de implantação (padrão)

    UseKeyRecoveryService

    0 = não usar a caução de chave (as próximas duas entradas do registro não são necessárias nesse caso)

    1 = usar a caução chave no sistema de recuperação de chave (padrão)

    Recomendado: o computador deve ser capaz de se comunicar com o serviço de recuperação de chave. Verifique se o computador pode se comunicar com o serviço antes de prosseguir.

    Keyrecoveryoptions

    0 = carregar apenas a chave de recuperação

    1 = carregar chave de recuperação e pacote de recuperação de chave (padrão)

    KeyRecoveryServiceEndPoint

    Defina esse valor como a URL para o servidor Web de recuperação de chave, por exemplo, http://de &lt; nome de computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. O agente MBAM reinicia o sistema durante a implantação do cliente do MBAM. Quando estiver pronto para esta reinicialização, execute o seguinte comando em um prompt de comando como administrador:

   **net start mbamagent**

8. Quando o computador for reiniciado e o BIOS solicitar que você aceite uma alteração no TPM, aceite a alteração.

9. Durante o processo de criação de imagens do sistema operacional cliente Windows, quando você estiver pronto para iniciar a criptografia, reinicie o serviço do agente do MBAM e defina iniciar como **automático** executando um prompt de comando como administrador e digitando os seguintes comandos:

   **SC config mbamagent Start = auto**

   **net start mbamagent**

10. Remova os valores do registro bypass executando regedit e indo para a entrada do registro HKLM\\SOFTWARE\\Microsoft. Para excluir o nó **MBAM** , clique com o botão direito do mouse no nó e clique em **excluir**.

## Tópicos relacionados


[Implantando o Cliente do MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)









