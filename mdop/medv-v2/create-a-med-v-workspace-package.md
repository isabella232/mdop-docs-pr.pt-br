---
title: Criar um pacote de espaço de trabalho da MED-V
description: Criar um pacote de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799237"
---
# Criar um pacote de espaço de trabalho da MED-V


Um espaço de trabalho do MED-V é o ambiente de área de trabalho do Windows XP em que os usuários finais interagem com a máquina virtual fornecida pelo MED-V. O administrador cria e personaliza o espaço de trabalho do MED-V. O espaço de trabalho consiste em uma imagem e a política de grupo que define as regras e a funcionalidade do espaço de trabalho do MED-V.

Você pode criar vários espaços de trabalho do MED-V, cada um personalizado com sua própria configuração, configurações e regras. Um usuário, grupo ou vários usuários ou grupos podem ser associados a cada espaço de trabalho do MED-V. A personalização torna o espaço de trabalho do MED-V disponível apenas para esse usuário ou grupo.

Use o **pacote do espaço de trabalho do MED-v** para criar espaços de trabalho do MED-v. O **pacote do espaço de trabalho do MED-V** é dividido em duas seções principais:

-   Um painel principal que inclui três botões que você usa para criar e gerenciar espaços de trabalho do MED-V. O botão **criar um pacote do espaço de trabalho do MED-v** abre o **Assistente Criar pacote de espaço de trabalho do MED-v** que você usa para criar seus espaços de trabalho do MED-v.

-   Uma **central de ajuda** à direita da janela que fornece informações e orientação para ajudá-lo a criar, testar e gerenciar seus espaços de trabalho do MED-V.

**Importante**  
Antes de poder usar o **pacote do espaço de trabalho do MED-V**, você deve primeiro verificar se a política de execução do Windows PowerShell está definida como Irrestrito.

`Set-ExecutionPolicy Unrestricted`

Além disso, a política de SAN do computador em que o **pacote do espaço de trabalho do MED-V** é executado deve ser definida como "Online All". Para verificar a configuração da política de SAN, execute os seguintes comandos em um prompt de comando com credenciais administrativas:

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

Se for necessário, altere a política de SAN para "tudo online" digitando os seguintes comandos no prompt de comando com credenciais administrativas:

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Importante**  
Se o software de criptografia de disco automático estiver instalado no computador que você usa para montar o disco rígido virtual e compilar o pacote do espaço de trabalho do MED-V, você deve desabilitar o software antes de começar. Caso contrário, você não pode usar o espaço de trabalho do MED-V em qualquer outro computador.



As informações fornecidas aqui podem ajudá-lo a criar seu pacote de implantação do espaço de trabalho do MED-V.

## <a href="" id="bkmk-prereq"></a>Pré-requisitos


Antes de começar a criar seu pacote de implantação do espaço de trabalho do MED-V, verifique se você tem acesso aos seguintes itens:

-   **Uma imagem do Windows XP preparada**

    Para obter mais informações sobre como criar uma imagem do Windows XP para usar com o MED-V, consulte [preparar uma imagem do MED-v](prepare-a-med-v-image.md).

-   **Um arquivo de texto ou lista que contém informações de redirecionamento de URL**

    Seu arquivo de texto ou lista de redirecionamento de URL contém as URLs que você deseja que sejam redirecionadas do computador host para o Internet Explorer no espaço de trabalho do MED-V. Quando você estiver usando o assistente de empacotamento para criar seu espaço de trabalho do MED-V, importe, digite ou copie e cole essas informações de redirecionamento como uma das etapas no processo de criação do pacote.

    **Observação**  
    O redirecionamento de URL no MED-V só oferece suporte aos protocolos HTTP e HTTPS. O MED-V não oferece suporte para FTP ou outros protocolos.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Empacotando um espaço de trabalho do MED-V para um idioma diferente do idioma do pacote do espaço de trabalho do MED-V


Por padrão, o espaço de trabalho do MED-V dá suporte a caracteres no idioma do computador e em inglês. Para criar um espaço de trabalho do MED-V para um idioma diferente daquele instalado no computador, especifique **-Loc \ [locale \]** no script do PowerShell (. ps1) após o nome do espaço de trabalho do MED-V.

Para criar um pacote de espaço de trabalho do MED-V em um idioma diferente do padrão do computador do empacotador do espaço de trabalho do MED-v, gere um script no idioma padrão executando o pacote do espaço de trabalho do MED-v e modificando o script de saída conforme necessário para a sua localidade. O script está localizado no diretório de saída do espaço de trabalho do MED-V especificado durante a compactação. Os nomes das configurações de localidade estão em. WXL arquivos no seguinte diretório:

C:\\Arquivos de Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## Criando um pacote do espaço de trabalho do MED-V


Para criar um pacote de espaço de trabalho do MED-V, siga estas etapas:

****

1.  Para abrir o **pacote do espaço de trabalho do MED-V**, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-v**.

2.  No painel principal do **pacote de espaço de trabalho do MED-v** , clique em **criar um pacote de espaço de trabalho do MED-v**.

    O **Assistente para criação do pacote do espaço de trabalho** do MED-v Create-v é exibido. O assistente consiste nas seguintes páginas:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Informações do pacote</strong></p></td>
    <td align="left"><p>Especifique um nome para o espaço de trabalho do MED-V e selecione uma pasta onde os arquivos do pacote do espaço de trabalho do MED-V serão salvos.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Selecionar imagem do Windows XP</strong></p></td>
    <td align="left"><p>Especifique a imagem do computador virtual do Windows XP preparado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Configuração da primeira vez</strong></p></td>
    <td align="left"><p>Especifique o processo de configuração que o MED-V segue durante a primeira configuração.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Mensagens do MED-V</strong></p></td>
    <td align="left"><p>Especifique as mensagens e a URL opcional para as informações de ajuda que o usuário final vê durante a primeira configuração.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nomeando computadores</strong></p></td>
    <td align="left"><p>Especifique como a máquina virtual MED-V é nomeada.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Copiar configurações do host</strong></p></td>
    <td align="left"><p>Especifique como as configurações para o espaço de trabalho do MED-V são definidas.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Inicialização e rede</strong></p></td>
    <td align="left"><p>Especifique as configurações para iniciar o espaço de trabalho do MED-V, a rede e as credenciais do usuário.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Redirecionamento da Web</strong></p></td>
    <td align="left"><p>Especifique um arquivo de texto ou uma lista de URLs que você deseja que sejam redirecionados para o Internet Explorer no espaço de trabalho do MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Resumo</strong></p></td>
    <td align="left"><p>Verifique as configurações do espaço de trabalho do MED-V e comece a criar seu pacote de implantação do espaço de trabalho do MED-V.</p></td>
    </tr>
    </tbody>
    </table>



3.  Na página **informações do pacote** , insira um nome para o espaço de trabalho do MED-v e selecione uma pasta onde os arquivos do pacote do espaço de trabalho do MED-v serão salvos.

    **Aviso**  
    Você deve nomear o espaço de trabalho do MED-V e especificar uma pasta para continuar.



~~~
After you have finished, click **Next**.
~~~

4. Na página **selecionar imagem do Windows XP** , especifique o local da imagem do seu computador virtual do MED-V do Windows XP preparado (arquivo. vhd).

   **Aviso**  
   Você deve especificar uma imagem de VHD do Windows XP para continuar.



~~~
After you have finished, click **Next**.
~~~

5. Na página **configuração inicial** , selecione se você deseja que o programa de instalação inicial seja executado enquanto estiver participando ou desacompanhados e se quiser que o espaço de trabalho do MED-V seja usado separadamente ou usado por todos os usuários finais em um computador compartilhado.

   Se você selecionar **a instalação autônoma, sem notificação**, o usuário final não será informado antes da primeira instalação ser executada, e a máquina virtual não será mostrada para o usuário final durante a configuração do primeiro período. Além disso, a página **mensagens do MED-V** do assistente fica oculta porque nenhuma mensagem será necessária se a configuração da primeira vez for executada em um modo completamente autônomo.

   Se você selecionar **a instalação autônoma, mas notificar os usuários finais antes do início da configuração da primeira vez**, o usuário final será informado antes da execução da primeira vez que a configuração é executada. No entanto, a máquina virtual não é mostrada para o usuário final durante a primeira configuração.

   Selecione **configuração assistida** se o usuário final precisar inserir informações durante a primeira configuração.

   O comportamento padrão é **instalação autônoma, mas notifique os usuários finais antes do início da configuração do primeiro horário**.

   **Tenha**  
   Se você criou o arquivo Sysprep. inf para que a mini-instalação exija que a entrada do usuário seja concluída, você deve selecionar **configuração assistida** ou problemas podem ocorrer durante a primeira configuração.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. Na página **mensagens do MED-V** , especifique as seguintes mensagens que o usuário final vê durante a primeira configuração do tempo:

   -   A mensagem que o usuário final vê quando a configuração é iniciada pela primeira vez.

   -   A mensagem que o usuário final verá se a primeira configuração falhar ou ocorrer um erro.

   **Observação**  
   A página de **mensagens do MED-V** do assistente estará oculta se você tiver selecionado **a instalação autônoma, sem notificação** na página **configuração do primeiro uso** .



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. Na página **nomear computadores** , você pode especificar se o nome do computador é gerenciado pelo MED-V ou por uma ferramenta de gerenciamento do sistema, como Sysprep. O padrão é que o nome do computador seja gerenciado por uma ferramenta de gerenciamento do sistema.

   Se você especificar que o nome do computador é gerenciado pelo MED-V, selecione uma Convenção de nomenclatura de computador (máscara) predefinida na lista suspensa. Uma visualização de um nome de computador de exemplo é exibida com base no computador que você está usando para criar o pacote do espaço de trabalho do MED-V.

   Se você selecionar uma das convenções de nomenclatura personalizadas, os campos que você pode especificar serão limitados aos seguintes caracteres:

   -   Os campos prefixo e sufixo estão limitados aos caracteres A-Z, a-z, a 0-9 e aos caracteres especiais! @ \ # $% ^ & ()-\ _ ' {}. e ~.

   -   Os campos hostname e username estão limitados aos dígitos de 0 a 9.

   **Importante**  
   Os nomes de computador devem ser exclusivos e limitados a um máximo de 15 caracteres. Ao decidir sobre o método de nomenclatura do computador, considere os usuários finais que têm vários computadores ou que compartilham um computador e evite usar máscaras de nomes de computador que possam causar uma colisão na rede.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. Na página **copiar configurações do host** , você pode selecionar as seguintes configurações para especificar como o espaço de trabalho do MED-V é configurado:

   **Tenha**  
   As configurações que você especificar nesta página que são copiadas do computador host para o espaço de trabalho do MED-V substituem aquelas especificadas no arquivo de resposta Sysprep. inf.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. Na página **inicialização e rede** , você pode alterar o comportamento padrão para as seguintes configurações:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Iniciar o espaço de trabalho do MED-V</strong></p></td>
   <td align="left"><p>Escolha se deseja iniciar o espaço de trabalho do MED-V no logon do usuário, ao ser usado pela primeira vez ou para permitir que o usuário final decida quando o espaço de trabalho do MED-V é iniciado.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>O espaço de trabalho do MED-V é iniciado de duas maneiras: quando o usuário final faz logon ou quando ele inicia pela primeira vez uma ação que exige o MED-V, como abrir um aplicativo publicado ou inserir uma URL que exija redirecionamento.</p>
   <p>Você pode definir essa configuração para o usuário final ou permitir que o usuário final controle como o MED-V é iniciado.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Se você especificar que o usuário final decide, o comportamento padrão que ele perceberá é que o espaço de trabalho do MED-V é iniciado quando eles fazem logon. Eles podem alterar o padrão clicando com o botão direito do mouse no ícone do MED-V na área de notificação e selecionando <strong> as configurações do usuário do MED-v </strong> . Se você definir essa configuração para o usuário final, não será possível alterar a forma como o MED-V é iniciado.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Rede</strong></p></td>
   <td align="left"><p>Selecione <strong> compartilhado </strong> ou <strong> ponte </strong> para a configuração de rede. O padrão é <strong> compartilhado </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Compartilhado </strong> - o espaço de trabalho do MED-V usa a NAT (conversão de endereços de rede) para compartilhar o host&#39;s de IP para o tráfego de saída.</p>
   <p><strong>Em ponte </strong> - , o espaço de trabalho do MED-V tem seu próprio endereço de rede, normalmente obtido por meio de DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Credenciais da loja</strong></p></td>
   <td align="left"><p>Escolha se deseja armazenar as credenciais do usuário final.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>O comportamento padrão é que o armazenamento de credenciais está desabilitado para que o usuário final deva ser autenticado toda vez que fizer logon.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Embora o armazenamento em cache das credenciais do usuário final forneça a melhor experiência do usuário, você deve estar ciente dos riscos envolvidos.</p>
   <p>A credencial do domínio do usuário final é armazenada em um formato reversível no Gerenciador de credenciais do Windows. Como resultado, um invasor pode escrever um programa que recupere a senha e possa ter acesso às credenciais do usuário. Você só pode diminuir esse risco desabilitando o armazenamento de credenciais do usuário final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. Na página **redirecionamento da Web** , você pode inserir, colar ou importar uma lista das URLs redirecionadas para o Internet Explorer no espaço de trabalho do MED-V. Para obter mais informações sobre como configurar as informações de redirecionamento de URL, consulte [pré-requisitos](#bkmk-prereq).

   Você também pode especificar como o Internet Explorer no espaço de trabalho do MED-V está configurado para os usuários finais. Por padrão, o nível de segurança da zona da Internet é definido como alto. Além disso, certos recursos de navegação padrão, como a barra de endereços, são removidos. Essa configuração padrão do Internet Explorer no espaço de trabalho do MED-V fornece um ambiente de navegação mais seguro para usuários finais.

   **Tenha**  
   Ao alterar as configurações padrão, você pode personalizar o Internet Explorer no espaço de trabalho do MED-V. No entanto, observe que, se você alterar as configurações padrão para torná-las menos seguras, poderá expor sua organização a esses riscos de segurança que estão presentes em versões mais antigas do Internet Explorer. Para obter mais informações, consulte [práticas recomendadas de segurança para operações do MED-V](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. Na página **Resumo** , você pode revisar as configurações de empacotamento deste espaço de trabalho do MED-V. Se você quiser alterar as configurações, clique no botão **anterior** para retornar à página relevante. Quando terminar de revisar as configurações, clique em **criar**.

   A página de **conclusão** do **Assistente Criar pacote de espaço de trabalho do MED-V** abre para mostrar o progresso da criação do pacote.

   **Observação**  
   O processo de criação do pacote do espaço de trabalho do MED-V pode levar alguns minutos para ser concluído, dependendo do tamanho do VHD especificado.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Clique em **fechar** para fechar o Packaging Wizard e retornar ao **pacote do espaço de trabalho do MED-V**.

Seu pacote de espaço de trabalho do MED-V agora está pronto para teste antes da implantação.

## Tópicos relacionados


[Definição das configurações avançadas usando o Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Como testar o pacote de espaço de trabalho da MED-V](testing-the-med-v-workspace-package.md)

[Preparar uma imagem da MED-V](prepare-a-med-v-image.md)









