---
title: Como recuperar computadores locais usando a imagem de recuperação do DaRT
description: Como recuperar computadores locais usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799337"
---
# Como recuperar computadores locais usando a imagem de recuperação do DaRT


Para recuperar um computador local usando o Microsoft Diagnostic and Recovery Toolset (DaRT) 7, você deve estar fisicamente presente no computador do usuário final que está apresentando problemas que exigem o DaRT. Você também pode executar o DaRT remotamente seguindo as instruções em [como recuperar computadores remotos usando a imagem de recuperação do DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

**Para recuperar um computador local usando o DaRT**

1.  Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT, a caixa de diálogo **netstart** será exibida. Você será perguntado se deseja inicializar serviços de rede. Se você clicar em **Sim**, presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor. Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.

    Para ignorar o processo de inicialização de rede, clique em **não**.

2.  Após a caixa de diálogo inicialização de rede, será perguntado se você deseja remapear as letras da unidade. Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão. Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online. O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.

3.  Após a caixa de diálogo remapeamento, uma caixa de diálogo **Opções de recuperação do sistema** é exibida e solicita que você selecione um layout de teclado. Em seguida, ele exibe o diretório raiz do sistema, o tipo de sistema operacional instalado e o tamanho da partição. Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos. Isso solicitará que você insira a mídia de instalação para o dispositivo e selecione o driver. Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.

    **Observação**  
    Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 7 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft**.

   A janela **diagnóstico e Recovery Toolset** é aberta. Agora você pode executar qualquer uma das ferramentas ou assistentes individuais que foram incluídos quando a imagem de recuperação do DaRT foi criada.

Você pode clicar em **ajuda** na janela do **conjunto de ferramentas de diagnóstico e recuperação** para abrir o arquivo de ajuda do cliente que fornece instruções e informações detalhadas necessárias para executar as ferramentas individuais do DART. Você também pode clicar no **Assistente de solução** na janela **diagnóstico e recuperação de conjunto de ferramentas** para escolher a melhor ferramenta para a situação, com base em uma breve entrevista que o assistente fornece.

Para obter informações gerais sobre qualquer uma das ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

**Para executar o DaRT no prompt de comando**

1. Você pode executar o DaRT no prompt de comando especificando o comando **netstart.exe** e usando qualquer um dos seguintes parâmetros:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parâmetro</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>-rede</p></td>
   <td align="left"><p>Inicializa os serviços de rede.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-remontar</p></td>
   <td align="left"><p>Remapeia as letras de unidade.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-aviso</p></td>
   <td align="left"><p>Exibe mensagens solicitando que o usuário final especifique se deseja inicializar a rede e remapear as unidades.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>A resposta do usuário final às solicitações substitui as opções-Network e-Remount.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Você pode personalizar o DaRT para que um computador inicializado pelo DaRT abra automaticamente a ferramenta **conexão remota** que é usada para estabelecer uma conexão remota com o suporte técnico.

## Tópicos relacionados


[Recuperar computadores usando o DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









