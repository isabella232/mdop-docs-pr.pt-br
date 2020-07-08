---
title: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
description: Como recuperar computadores remotos usando a imagem de recuperação do DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799143"
---
# Como recuperar computadores remotos usando a imagem de recuperação do DaRT


O recurso de conexão remota no Microsoft Diagnostics and Recovery Toolset (DaRT) 7 permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final. Depois que determinadas informações forem fornecidas pelo usuário final (ou por um profissional de assistência técnica em funcionamento no computador do usuário final), o administrador de ti ou o agente de helpdesk poderá assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.

**Importante**  
Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.



**Para recuperar um computador remoto usando o DaRT**

1.  Inicialize um computador de usuário final usando a imagem de recuperação do DaRT.

    Você geralmente usará um dos seguintes métodos para inicializar o DaRT para recuperar um computador remoto, dependendo de como você implanta a imagem de recuperação do DaRT. Para obter mais informações sobre a implantação da imagem de recuperação do DaRT, consulte [implantando a imagem de recuperação do dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

    -   Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.

    -   Inicialize no DaRT a partir de uma partição remota na rede.

    Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

    Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.

    **Observação**  
    A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.



2.  Quando o computador estiver sendo inicializado na imagem de recuperação do DaRT, a caixa de diálogo **netstart** será exibida. Você será perguntado se deseja inicializar serviços de rede. Se você clicar em **Sim**, presume-se que um servidor DHCP esteja presente na rede e uma tentativa seja feita para obter um endereço IP do servidor. Se a rede usar endereços IP estáticos em vez de DHCP, você poderá usar posteriormente a ferramenta de **configuração TCP/IP** no DART para especificar um endereço IP estático.

    Para ignorar o processo de inicialização de rede, clique em **não**.

3.  Após a caixa de diálogo inicialização de rede, será perguntado se você deseja remapear as letras da unidade. Quando você executa o Windows online, o volume do sistema geralmente é mapeado para a unidade C. No entanto, quando você executa o Windows offline em WinRE, o volume do sistema original pode ser mapeado para outra unidade, e isso pode causar confusão. Se você decidir remapear, o DaRT tenta mapear as letras da unidade offline para corresponder às letras da unidade online. O remapeamento será executado apenas se um sistema operacional offline for selecionado posteriormente no processo de inicialização.

4.  Após a caixa de diálogo remapeamento, uma caixa de diálogo **Opções de recuperação do sistema** é exibida e solicita que você selecione um layout de teclado. Em seguida, ele exibe o diretório raiz do sistema, o tipo de sistema operacional instalado e o tamanho da partição. Se você não vir o sistema operacional listado e suspeitar que a falta de drivers seja uma possível causa da falha, clique em **carregar drivers** para carregar os drivers suspeitos. Isso solicitará que você insira a mídia de instalação para o dispositivo e selecione o driver. Selecione a instalação que você deseja reparar ou diagnosticar e, em seguida, clique em **Avançar**.

    **Observação**  
    Se o ambiente de recuperação do Windows (WinRE) detectar ou suspeitar que o Windows 7 não iniciou corretamente na última vez em que foi tentado, o **reparo de inicialização** pode começar a ser executado automaticamente. Para obter informações sobre essa situação, incluindo como resolvê-la, consulte [solução de problemas do DaRT 7,0](troubleshooting-dart-70-new-ia.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. Na janela **Opções de recuperação do sistema** , selecione **diagnósticos e conjunto de ferramentas de recuperação da Microsoft** para abrir a janela **diagnóstico e conjunto de ferramentas de recuperação** .

6. Na janela **diagnóstico e recuperação de conjunto de ferramentas** , clique em **conexão remota** para abrir a janela **conexão remota DART** . Se você for solicitado a fornecer o acesso remoto do suporte técnico, clique em **OK**.

   A janela conexão remota DaRT abre e exibe um número de tíquete, um endereço IP e informações de porta.

7. No computador do agente da assistência técnica, abra o **Visualizador de conexão remota do DART**.

   Clique em **Iniciar**, em **todos os programas**, em **Microsoft DART 7**e, em seguida, clique em **Visualizador de conexão remota do DART**.

8. Na janela **conexão remota DART** , insira a permissão necessária, o endereço IP e as informações sobre a porta.

   **Observação**  
   Essas informações são criadas no computador do usuário final e devem ser fornecidas pelo usuário final. Pode haver vários endereços IP a serem escolhidos, dependendo de quantos estão disponíveis no computador do usuário final.



9. Clique em **Conectar**.

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

**Para executar o Visualizador de conexão remota no prompt de comando**

1.  Você pode executar o **Visualizador de conexão remota do DART** no prompt de comando especificando o comando **DartRemoteViewer.exe** e usando os seguintes parâmetros:

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


[Recuperar computadores usando o DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









