---
title: Tecnologia Trim Transfer do MED-V
description: Tecnologia Trim Transfer do MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799822"
---
# Tecnologia Trim Transfer do MED-V


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


A tecnologia de eliminação de duplicação avançada da transferência de corte do MED-V acelera o download de imagens de máquinas virtuais iniciais e atualizadas na LAN ou WAN, reduzindo assim a largura de banda de rede necessária para transportar uma máquina virtual de espaço de trabalho do MED-V para vários usuários finais.

Essa tecnologia inovadora usa dados locais existentes para criar a imagem da máquina virtual, aproveitando o fato de que, em muitos casos, grande parte da máquina virtual (por exemplo, arquivos do sistema e do aplicativo) já existe no disco do usuário final. Por exemplo, se uma máquina virtual que contém o WindowsXP for entregue a um cliente executando uma cópia local do WindowsXP, o MED-V removerá automaticamente os elementos WindowsXP redundantes da transferência. Para garantir um espaço de trabalho válido e funcional, o cliente MED-V Verifica criptograficamente a integridade dos dados locais antes de usá-los, garantindo que os blocos de dados locais sejam absolutamente idênticos aos da imagem da máquina virtual desejada. Blocos que não correspondem não são usados.

O processo é eficiente na largura de banda e é transparente, e as transferências são executadas em segundo plano, utilizando recursos de CPU e CPU não utilizados.

Ao atualizar para uma nova versão de imagem (por exemplo, quando os administradores querem distribuir um novo aplicativo ou patch), somente os elementos que foram alterados ("deltas") são baixados, e não toda a máquina virtual, reduzindo significativamente a largura de banda e o tempo de entrega necessários para a rede.

Você pode configurar quais pastas serão indexadas no host como parte do protocolo de transferência de corte, com base no sistema operacional do host. Essas configurações são definidas no arquivo *ClientSettings.xml* , que pode ser encontrado na pasta **Servers\\Configuration Server\\** .

Durante a aplicação de novas configurações, o serviço deve ser reiniciado.

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





