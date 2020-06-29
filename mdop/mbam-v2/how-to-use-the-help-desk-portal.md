---
title: Como usar o Portal de Assistência Técnica
description: Como usar o Portal de Assistência Técnica
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799850"
---
# Como usar o Portal de Assistência Técnica


O site de administração e monitoramento do MBAM, também chamado de portal de suporte técnico, é uma interface administrativa para a criptografia de unidade de disco BitLocker instalada como parte da infraestrutura de servidor de administração e monitoramento do Microsoft BitLocker (MBAM). As seções a seguir descrevem como você pode usar este site para analisar relatórios, recuperar unidades de usuários finais e gerenciar os usuários finais TPMs.

## <a href="" id="bkmk-reports"></a>Relatórios


O MBAM coleta informações dos computadores do Active Directory e do cliente, o que permite que você execute relatórios diferentes para monitorar o uso e a conformidade do BitLocker. Usando a seção **relatórios** do site Administração e monitoramento, você pode gerar relatórios sobre conformidade empresarial, computadores individuais e atividades de recuperação de chave. Para obter uma descrição de cada relatório, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).

**Para acessar relatórios**

1.  Abra um navegador da Web e navegue até o site de administração e monitoramento do MBAM.

2.  Selecione **relatórios** no painel esquerdo.

3.  Na barra de menus superior, selecione o tipo de relatório que deseja gerar. Para salvar relatórios, clique no botão **Exportar** na barra de menus relatórios.

Para obter informações adicionais sobre como executar relatórios do MBAM, consulte [como gerar relatórios do MBAM](how-to-generate-mbam-reports-mbam-2.md).

## <a href="" id="bkmk-drirec"></a>Recuperação de unidade


O recurso de **recuperação de unidade** do site de administração e monitoramento permite aos usuários com funções específicas de administrador (por exemplo, usuários de suporte técnico) para acessar dados de chave de recuperação coletados pelo cliente MBAM. Esses dados podem ser usados para acessar uma unidade protegida pelo BitLocker quando o BitLocker entra no modo de recuperação. Para obter instruções sobre como recuperar uma unidade que está no modo de recuperação, consulte [como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).

Você também pode recuperar unidades que foram movidas ou que estão corrompidas:

-   [Como recuperar uma unidade movida](how-to-recover-a-moved-drive-mbam-2.md)

-   [Como recuperar uma unidade corrompida](how-to-recover-a-corrupted-drive-mbam-2.md)

Para obter informações adicionais sobre como recuperar uma unidade protegida pelo BitLocker, consulte [executando o gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).

## <a href="" id="bkmk-manatpm"></a>Gerenciar TPM


O recurso gerenciar TPM do site de administração e monitoramento oferece aos usuários certas funções de administrador (por exemplo, "usuários da assistência técnica MBAM") acessados com dados do TPM que foram coletados pelo cliente MBAM. Em um bloqueio de TPM, um administrador pode usar o site de administração e monitoramento para recuperar o arquivo de senha necessário para desbloquear o TPM. Para obter instruções sobre como redefinir um TPM após um bloqueio de TPM, consulte [como redefinir um bloqueio de TPM](how-to-reset-a-tpm-lockout-mbam-2.md).

## <a href="" id="bkmk-helpdesk"></a> Tarefas do suporte técnico do MBAM


Você pode usar o site de administração e monitoramento para várias tarefas administrativas, como o gerenciamento de hardware protegido pelo BitLocker, a recuperação de unidades e a execução de relatórios. Por padrão, a URL para o site de administração e monitoramento é http:// &lt; *MBAMAdministrationServername* &gt; , embora você possa personalizá-lo durante o processo de instalação.

**Observação**  Para acessar os vários recursos oferecidos pelo site de administração e monitoramento, você deve ter as funções adequadas associadas à sua conta de usuário. Para obter mais informações sobre noções básicas sobre funções de usuário, consulte [como gerenciar funções de administrador MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

 

Use os links a seguir para encontrar informações sobre as tarefas que você pode executar usando o site Administração e monitoramento:

-   [Como redefinir um bloqueio de TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [Como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [Como recuperar uma unidade movida](how-to-recover-a-moved-drive-mbam-2.md)

-   [Como recuperar uma unidade corrompida](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [Como determinar o estado de criptografia BitLocker de computadores perdidos](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





