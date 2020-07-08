---
title: Como instalar o cliente usando a linha de comando
description: Como instalar o cliente usando a linha de comando
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797102"
---
# Como instalar o cliente usando a linha de comando


Os tópicos desta seção incluem procedimentos para instalar o cliente de desktop do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal) usando setup.exe ou setup.msi. É necessário ter direitos administrativos para executar o programa de instalação.

Você pode usar parâmetros de linha de comando opcionais para aplicar configurações específicas ao cliente App-V durante a instalação. Para obter mais informações sobre como usar parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md). Se você tiver aplicado configurações do registro a um computador antes de implantar um cliente — por exemplo, usando a política de grupo, essas configurações serão mantidas e todos os parâmetros de linha de comando adicionais serão aplicados. Os valores de parâmetro de linha de comando substituirão qualquer valor existente na mesma configuração.

**Observação**  Ao instalar o cliente App-V para usar com um cache somente leitura, por exemplo, com uma implementação de servidor VDI, você deve definir o parâmetro *AUTOLOADTARGET* como None para impedir que o cliente tente atualizar aplicativos quando o cache for somente leitura.

 

Para obter mais informações sobre como definir esses valores de parâmetro após a instalação, consulte [como definir as configurações do registro do cliente App-V usando a linha de comando](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) no guia de operações do Application Virtualization (App-V).

**Observação**  Se uma configuração no computador do usuário depende do caminho de instalação do cliente, observe que o aplicativo virtualização do aplicativo (App-V) 4.5 copia seus arquivos de instalação para uma pasta diferente das versões anteriores. Por padrão, uma nova instalação do aplicativo App-V 4.5 copiará seus arquivos de instalação para a pasta do cliente \\Program Files\\Microsoft Application Virtualization. Se uma versão anterior do cliente já estiver instalada, executar o instalador do cliente do App-V 4,5 executará uma atualização do cliente existente usando a pasta de instalação existente.

 

\ [Valor do token do modelo \]

**Observação**  Para o App-V versão 4.6 e posterior, quando o cliente App-V estiver instalado, o SFTLDR.DLL será copiado para o diretório Windows\\system32. Se o cliente App-V estiver instalado em um sistema de 64 bits, o SFTLDR\_WOW64.DLL será copiado para o diretório Windows\\SysWOW64.

 

\ [Valor do token do modelo \]

## Nesta seção


Os tópicos a seguir descrevem como instalar o cliente de desktop do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal) usando setup.exe ou setup.msi.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Como instalar o cliente do App-V usando Setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
Fornece um procedimento passo a passo para instalar o cliente App-V usando o programa setup.exe.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Como instalar o cliente do App-V usando Setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
Fornece procedimentos passo a passo para instalar qualquer software de pré-requisito e também o cliente App-V usando o programa setup.msi.

## Tópicos relacionados


[Parâmetros de linha de comando do instalador do Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Como desinstalar o cliente do App-V](how-to-uninstall-the-app-v-client.md)

 

 





