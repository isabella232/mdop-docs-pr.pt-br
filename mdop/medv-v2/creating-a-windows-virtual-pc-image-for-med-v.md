---
title: Como criar uma imagem do Windows Virtual PC para a MED-V
description: Como criar uma imagem do Windows Virtual PC para a MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796061"
---
# Como criar uma imagem do Windows Virtual PC para a MED-V


Antes de poder entregar um espaço de trabalho do MED-V para os usuários, primeiro você precisa preparar um disco rígido virtual que você usa para criar o pacote de instalação do espaço de trabalho do MED-V para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Para preparar o disco rígido virtual necessário, você deve criar uma imagem do Windows Virtual PC que contenha o sistema operacional, as atualizações e o software necessários para que você implante posteriormente as informações de aplicativos e de redirecionamento de URL para os usuários. Esta seção fornece orientação sobre como criar o disco rígido virtual.

Para criar uma imagem virtual do MED-V, você deve seguir estas etapas.

1.  [Criar uma imagem do Windows Virtual PC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [Instalar o Windows XP na imagem](#bkmk-installingwindowsxpontovpc)

3.  [Instalar o .NET Framework na imagem](#bkmk-installingnet)

4.  [Aplicar atualizações à imagem](#bkmk-applypatchestovpc)

5.  [Instalar componentes de integração](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Criando uma imagem do Windows Virtual PC


Para criar uma imagem do Windows Virtual PC, consulte a documentação do PC virtual do Windows:

-   [Página inicial do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Ajuda do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Como alternativa, se você já tiver um arquivo de imagem do Windows (WIM) que deseja usar como base para a sua imagem virtual, é possível convertê-lo em um VHD que você usa para criar o espaço de trabalho do MED-V. Para obter mais informações sobre como converter um WIM em um disco rígido virtual, consulte [suporte a VHD nativo no Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .

**Importante**  O MED-V aceita apenas um disco rígido virtual por máquina virtual e apenas uma partição em cada disco virtual.

 

Depois de criar seu disco rígido virtual, instale o Windows XP na imagem.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Instalar o Windows XP em uma imagem do PC virtual do Windows


O MED-V exige que o Windows XP SP3 esteja instalado na imagem do PC virtual do Windows antes de criar o espaço de trabalho do MED-V.

Para obter mais informações sobre como instalar o Windows XP, consulte [criar uma máquina virtual e instalar um sistema operacional convidado](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Instalando o .NET Framework 3,5 SP1 em uma imagem do PC virtual do Windows


Você deve instalar manualmente o .NET Framework 3,5 SP1 e o Update KB959209 na imagem do PC virtual do Windows que você prepara para usar com o MED-V. A atualização [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) corrige vários problemas de compatibilidade de aplicativos conhecidos.

## <a href="" id="bkmk-applypatchestovpc"></a>Aplicando atualizações à imagem do PC virtual do Windows


Depois de instalar o Windows XP em sua máquina virtual, instale todas as atualizações necessárias do Windows XP na imagem, como SP3. Você também pode instalar algumas atualizações opcionais para melhorar o desempenho.

**Importante**  O MED-V exige que o Windows XP SP3 esteja em execução no sistema operacional convidado.

 

**Aviso**  Ao instalar atualizações do Windows XP, certifique-se de que você permaneça na versão do Internet Explorer no convidado que pretende usar no espaço de trabalho do MED-V. Por exemplo, se você pretende executar o Internet Explorer 6 no espaço de trabalho do MED-V, certifique-se de que todas as atualizações instaladas agora não incluam o Internet Explorer 7 ou o Internet Explorer 8. Além disso, recomendamos que você configure o registro para impedir que as atualizações automáticas atualizem o Internet Explorer.

 

### Instalar uma atualização de desempenho opcional

Embora seja opcional, recomendamos que você instale a seguinte atualização para o [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) . Esta atualização aumenta o desempenho das pastas compartilhadas em uma sessão de serviços de terminal:

**Observação**  A atualização está disponível publicamente. No entanto, você pode ser solicitado a aceitar um contrato de serviços da Microsoft. Siga os prompts nas páginas da Web sucessivas para recuperar este hotfix.

 

### Configurando uma atualização de desempenho de política de grupo

Por padrão, a política de grupo é baixada para um computador, um byte de cada vez. Isso causa atrasos enquanto o MED-V está sendo associado ao domínio. Para aumentar o desempenho da política de grupo, defina o seguinte valor da chave do registro para o registro:

Subchave do registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrada: BufferPolicyReads

Tipo: DWORD

Valor: 1

## <a href="" id="bkmk-installintegration"></a>Instalando componentes de integração


O Windows Virtual PC inclui o pacote de componentes de integração. Isso fornece recursos que melhoram a interação entre o ambiente virtual e o computador físico. Por exemplo, o pacote de componentes de integração permite que o mouse se movimente entre o host e os computadores convidados.

**Importante**  O MED-V requer a instalação do pacote de componentes de integração.

 

Ao configurar a imagem virtual para funcionar com o MED-V, você deve instalar manualmente o pacote de componentes de integração no sistema operacional convidado para disponibilizar os recursos de integração disponíveis.

Para obter mais informações sobre como instalar e usar o pacote de componentes de integração, consulte o seguinte:

-   [Instalar ou atualizar o pacote de componentes de integração](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [Sobre os recursos de integração](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### Instalando a atualização do RemoteApp

Depois de instalar o pacote de componentes de integração, você será solicitado a instalar a seguinte atualização: "atualização para Windows XP SP3 para habilitar o RemoteApp". Este é um componente obrigatório do MED-V.

**Importante**  Se você não for solicitado a instalar a atualização do RemoteApp, será necessário baixá-la e instalá-la manualmente. Para obter mais informações e instruções sobre como baixar essa atualização, consulte [atualização para Windows XP SP3 para habilitar o RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### Habilitando a área de trabalho remota

Por padrão, a área de trabalho remota é habilitada após a instalação do pacote de componentes de integração. Para que o MED-V seja operacional, verifique se a área de trabalho remota está habilitada e não distribua nenhuma política de grupo que desativasse.

Para obter informações sobre como habilitar a área de trabalho remota, consulte [habilitar ou desabilitar a área de trabalho remota](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .

## Personalizando o Internet Explorer usando o kit de administração do Internet Explorer


Se desejar, você pode usar o kit de administração do Internet Explorer para personalizar o Internet Explorer no sistema operacional convidado. Para obter mais informações, consulte o [Kit de administração e o guia de implantação do Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?linkid=200007).

**Aviso**  Você deve considerar as questões de segurança associadas à personalização do Internet Explorer no espaço de trabalho do MED-V. Para obter mais informações, consulte [práticas recomendadas de segurança para operações do MED-V](security-best-practices-for-med-v-operations.md).

 

Depois que o disco rígido virtual for instalado com um sistema operacional convidado atualizado, você poderá instalar aplicativos na imagem.

## Tópicos relacionados


[Instalar aplicativos em uma imagem do Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md)

[Como configurar uma imagem do Windows Virtual PC para a MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





