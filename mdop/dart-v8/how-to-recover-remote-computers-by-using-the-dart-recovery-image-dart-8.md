---
title: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
description: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799464"
---
# Como recuperar computadores remotos usando a imagem de recuperação do DaRT


Use o recurso conexão remota no Microsoft Diagnostic and Recovery Toolset (DaRT) 8,0 para executar as ferramentas do DaRT remotamente em um computador de usuário final. Depois que o usuário final fornece o trabalho de administrador ou de suporte técnico com determinadas informações, o administrador de ti ou o trabalhador de suporte técnico pode assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.

Se você desativou as ferramentas DaRT ao criar a imagem de recuperação, ainda tem acesso a todas as ferramentas. Todas as ferramentas, exceto conexão remota, não estão disponíveis para os usuários finais.

**Para recuperar um computador remoto usando a imagem de recuperação do DaRT**

1.  Inicialize um computador de usuário final usando a imagem de recuperação do DaRT.

    Você geralmente usará um dos seguintes métodos para inicializar o DaRT para recuperar um computador remoto, dependendo de como você implanta a imagem de recuperação do DaRT. Para obter mais informações sobre a implantação da imagem de recuperação do DaRT, consulte [implantando o DaRT 8,0](deploying-dart-80-dart-8.md).

    -   Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.

    -   Inicialize no DaRT a partir de uma partição remota na rede.

    Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

    Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.

    **Observação**  
    A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. Quando for perguntado se você deseja inicializar serviços de rede, selecione uma das seguintes opções:

   **Sim** -presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor. Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.

   **Não** -ignore o processo de inicialização de rede.

3. Indique se deseja remapear as letras da unidade. Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão. Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online. O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.

4. Na caixa de diálogo **Opções de recuperação do sistema** , selecione um layout de teclado.

5. Verifique o diretório raiz do sistema exibido, o tipo de sistema operacional instalado e o tamanho da partição. Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos e, em seguida, insira a mídia de instalação para o dispositivo e selecione o driver.

6. Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.

   **Observação**  
   Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 8 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente. Para obter informações sobre como resolver esse problema, consulte [solução de problemas do DaRT 8,0](troubleshooting-dart-80-dart-8.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Na janela **Opções de recuperação do sistema** , clique em **conjunto de ferramentas de diagnóstico e recuperação da Microsoft** para abrir o conjunto de **ferramentas diagnóstico e recuperação**.

8. Na janela **diagnóstico e recuperação de conjunto de ferramentas** , clique em **conexão remota** para abrir a janela **conexão remota DART** . Se você for solicitado a fornecer o acesso remoto do suporte técnico, clique em **OK**.

   A janela conexão remota DaRT abre e exibe um número de tíquete, um endereço IP e informações de porta.

9. No computador de suporte técnico, abra o **Visualizador de conexão remota do DART**.

10. Clique em **Iniciar**, em **todos os programas**, em **Microsoft DART 8,0**e, em seguida, clique em **Visualizador de conexão remota do DART**.

11. Na janela **conexão remota DART** , insira a permissão necessária, o endereço IP e as informações sobre a porta.

   **Observação**  
   Essas informações são criadas no computador do usuário final e devem ser fornecidas pelo usuário final. Pode haver vários endereços IP a serem escolhidos, dependendo de quantos estão disponíveis no computador do usuário final.



12. Clique em **Conectar**.

O administrador de ti agora assume o controle do computador do usuário final e pode executar as ferramentas do DaRT remotamente.

**Observação**  
É fornecido um arquivo chamado inv32.xml e contém informações de conexão remota, como o número da porta e o endereço IP. Por padrão, o arquivo está localizado geralmente em%windir%\\System32.



**Para personalizar o processo de conexão remota**

1. Você pode personalizar o processo de conexão remota editando o arquivo winpeshl.ini. Para obter mais informações sobre como editar o arquivo winpeshl.ini, consulte [Winpeshl.ini arquivos](https://go.microsoft.com/fwlink/?LinkId=219413).

   Especifique os seguintes comandos e parâmetros para personalizar a forma como uma conexão remota é estabelecida com um computador de usuário final:

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Comando</th>
   <th align="left">Parâmetro</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RemoteRecovery.exe</strong></p></td>
   <td align="left"><p>-nomessage</p></td>
   <td align="left"><p>Especifica que o prompt de confirmação não será exibido. <strong>A conexão remota </strong> continua da mesma forma que se o usuário final tiver respondido &quot; Sim &quot; à solicitação de confirmação.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>WaitForConnection.exe</strong></p></td>
   <td align="left"><p>nenhum(a)</p></td>
   <td align="left"><p>Impede que um script personalizado continue até que a <strong> conexão remota </strong> não esteja em execução ou uma conexão válida seja estabelecida com o computador do usuário final.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Esse comando não serve nenhuma função se for especificado independentemente. Ele deve ser especificado em um script para funcionar corretamente.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Veja a seguir um exemplo de um arquivo winpeshl.ini que é personalizado para abrir a ferramenta **conexão remota** assim que uma tentativa é feita para inicializar o DART:

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

Quando o DaRT é iniciado, ele cria o arquivo inv32.xml em \\Windows\\System32\\ no disco de RAM. Este arquivo contém informações de conexão: endereço IP, porta e número do tíquete. Você pode copiar esse arquivo em um compartilhamento de rede para disparar um fluxo de trabalho de suporte técnico. Por exemplo, um programa personalizado pode verificar o compartilhamento de rede para arquivos de conexão e, em seguida, criar um tíquete de suporte ou enviar notificações por email.

**Para executar o Visualizador de conexão remota no prompt de comando**

1.  Para executar o **Visualizador de conexão remota do DART** no prompt de comando, especifique o comando **DartRemoteViewer.exe** e use os seguintes parâmetros:

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
    <td align="left"><p>-bilhete = &lt; <em> TicketNumber</em>&gt;</p></td>
    <td align="left"><p>Onde &lt; <em> TicketNumber </em> &gt; é o número do bilhete, incluindo os traços, que é gerado pela conexão remota.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>-IPAddress = &lt; <em> IPAddress</em>&gt;</p></td>
    <td align="left"><p>Onde &lt; <em> IPAddress </em> &gt; é o endereço IP gerado pela conexão remota.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>-Port = &lt; <em> porta</em>&gt;</p></td>
    <td align="left"><p>Em que &lt; <em> porta </em> &gt; é a porta correspondente ao endereço IP especificado.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. Se todos os três parâmetros forem especificados e os dados forem válidos, uma conexão será imediatamente tentada quando o programa for iniciado. Se algum parâmetro não for válido, o programa será iniciado como se não houvesse parâmetros especificados.

## Tópicos relacionados


[Operações do DaRT 8.0](operations-for-dart-80-dart-8.md)

[Recuperar computadores usando o DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









