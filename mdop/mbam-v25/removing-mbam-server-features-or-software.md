---
title: Removendo os recursos de servidor ou o software do MBAM
description: Removendo os recursos de servidor ou o software do MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799580"
---
# Removendo os recursos de servidor ou o software do MBAM


Estas instruções explicam como remover software e recursos do Microsoft BitLocker Administration and Monitoring (MBAM). Se você remover os recursos do MBAM Server, apenas os recursos configurados serão removidos do servidor, e não do software do servidor do MBAM. Se você remover o software MBAM Server, o software e todos os recursos do MBAM Server que você configurou nesse servidor serão removidos.

**Observação**  Para impedir a remoção acidental de dados, o MBAM não fornece nenhum mecanismo para remover os bancos de dados; Você deve fazer isso manualmente.

 

## <a href="" id="bkmk-removeserverfeatures"></a>Removendo recursos do MBAM Server


Você pode usar qualquer um dos seguintes métodos para remover os recursos do MBAM Server que você configurou:

-   Assistente de configuração do servidor do MBAM

-   Cmdlets do Windows PowerShell

### Usar o assistente de configuração do servidor do MBAM para remover recursos

Siga estas instruções para usar o assistente de configuração do servidor do MBAM para remover os recursos de servidor MBAM configurados de um servidor.

**Para remover os recursos do MBAM usando o assistente**

1.  No servidor em que você deseja remover recursos, selecione **configuração do servidor do MBAM** para abrir o assistente de configuração.

2.  Clique em **remover recursos**, selecione os recursos a serem removidos e clique em **Avançar**. Uma página de **Resumo** exibe os recursos que você selecionou para remoção.

3.  Clique em **remover** para começar a remover os recursos e, em seguida, clique em **fechar**.

### Usando o Windows PowerShell para remover recursos

Use as etapas a seguir como um guia geral para remover os recursos do MBAM Server usando cmdlets do Windows PowerShell.

**Para remover os recursos do MBAM usando o Windows PowerShell**

1.  Antes de remover qualquer recurso, consulte [configurando recursos do MBAM 2,5 Server usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para examinar os pré-requisitos para usar o Windows PowerShell.

2.  Use os seguintes cmdlets para remover os recursos do MBAM Server:

    -   Disable-MbamReport

    -   Disable-MbamWebApplication

    -   Disable-MbamCMIntegration

    Para obter ajuda com os cmdlets do Windows PowerShell, digite cmdlet **Get-Help** &lt; *cmdlet* &gt; ou consulte a [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) para os cmdlets do Windows PowerShell MBAM.

## Removendo o software MBAM Server


Use as etapas a seguir para remover o software do servidor MBAM e todos os recursos do MBAM Server que você configurou nesse servidor.

**Para remover o software do servidor MBAM**

1.  No servidor em que você deseja desinstalar o software MBAM Server, execute **MBAMserversetup.exe** para iniciar o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

2.  Selecione **desinstalar**e siga os prompts restantes para concluir o processo de desinstalação do software MBAM Server.



## Tópicos relacionados


[Implantando o MBAM 2.5](deploying-mbam-25.md)

 

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



