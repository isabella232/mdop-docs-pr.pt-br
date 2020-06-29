---
title: Como recuperar computadores locais usando a imagem de recuperação do DaRT
description: Como recuperar computadores locais usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: f679d522-49ab-429c-93d0-294c3f3e5639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1b5faa0eb9ac24b33c66f1d5262a050b92e11e52
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799446"
---
# Como recuperar computadores locais usando a imagem de recuperação do DaRT


Use estas instruções para recuperar um computador quando você estiver fisicamente presente no computador do usuário final que está apresentando problemas.

**Como recuperar um computador local usando a imagem de recuperação do DaRT**

1.  Inicializar o computador do usuário final usando a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

    Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT 8,0, a caixa de diálogo **netstart** será exibida.

2.  Quando for perguntado se você deseja inicializar serviços de rede, selecione uma das seguintes opções:

    **Sim** -presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor. Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.

    **Não** -ignore o processo de inicialização de rede.

3.  Indique se deseja remapear as letras da unidade. Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão. Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online. O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.

4.  Na caixa de diálogo **Opções de recuperação do sistema** , selecione um layout de teclado.

5.  Verifique o diretório raiz do sistema exibido, o tipo de sistema operacional instalado e o tamanho da partição. Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos e, em seguida, insira a mídia de instalação para o dispositivo e selecione o driver.

6.  Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.

    **Observação**  
    Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 8 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft**.

   A janela **diagnóstico e Recovery Toolset** é aberta. Agora você pode executar qualquer uma das ferramentas ou assistentes individuais que foram incluídos quando a imagem de recuperação do DaRT foi criada.

Você pode clicar em **ajuda** na janela do **conjunto de ferramentas de diagnóstico e recuperação** para abrir o arquivo de ajuda do cliente que fornece instruções e informações detalhadas necessárias para executar as ferramentas individuais do DART. Você também pode clicar no **Assistente de solução** na janela **diagnóstico e recuperação de conjunto de ferramentas** para escolher a melhor ferramenta para a situação, com base em uma breve entrevista que o assistente fornece.

Para obter informações gerais sobre qualquer uma das ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).

**Como executar o DaRT no prompt de comando**

- Para executar o DaRT no prompt de comando, especifique o comando **netstart.exe** e use qualquer um dos seguintes parâmetros:

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>Parâmetro</strong></p></td>
  <td align="left"><p><strong>Descrição</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-rede</p></td>
  <td align="left"><p>Inicializa os serviços de rede.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-remontar</p></td>
  <td align="left"><p>Remapeia as letras de unidade.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-aviso</p></td>
  <td align="left"><p>Exibe mensagens que solicitam que o usuário final especifique se deseja inicializar a rede e remapear as unidades.</p>
  <div class="alert">
  <strong>Aviso</strong><br/><p>A resposta do usuário final para o prompt substitui as opções – Network e-Remount.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## Tópicos relacionados


[Operações do DaRT 8.0](operations-for-dart-80-dart-8.md)

[Recuperar computadores usando o DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









