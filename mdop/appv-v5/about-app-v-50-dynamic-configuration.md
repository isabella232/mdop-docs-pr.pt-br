---
title: Sobre a configuração dinâmica do App-V 5.0
description: Sobre a configuração dinâmica do App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796644"
---
# Sobre a configuração dinâmica do App-V 5.0


Você pode usar a configuração dinâmica para personalizar um pacote App-V 5,0 para um usuário. Use as informações a seguir para criar ou editar um arquivo de configuração dinâmica existente.

Quando você edita o arquivo de configuração dinâmica, ele personaliza como um pacote do App-V 5,0 será executado para um usuário ou grupo. Isso ajuda a fornecer um método mais conveniente para a personalização do pacote, removendo a necessidade de resequenciar os pacotes usando as configurações desejadas e fornece uma maneira de manter o conteúdo do pacote e as configurações personalizadas de forma independente.

## Avançado: configuração dinâmica


Os pacotes de aplicativos virtuais contêm um manifesto que fornece todas as informações básicas do pacote. Essas informações incluem os padrões para as configurações do pacote e determina as configurações na forma mais básica (sem personalização adicional). Se desejar ajustar esses padrões para um usuário ou grupo específico, você pode criar e editar os seguintes arquivos:

-   Arquivo de configuração do usuário

-   Arquivo de configuração de implantação

Os arquivos. XML anteriores especificam as configurações do pacote e permitem que os pacotes sejam personalizados sem afetar diretamente os pacotes. Quando um pacote é criado, o sequenciador gera automaticamente a implantação padrão e os arquivos user. xml usando os dados do manifesto do pacote. Portanto, esses arquivos de configuração gerados simplesmente refletem as configurações padrão que o pacote innateu de como as coisas foram configuradas durante o sequenciamento. Se você aplicar esses arquivos de configuração a um pacote no formato gerado pelo sequenciador, os pacotes terão as mesmas configurações padrão que vieram do manifesto. Isso fornece um modelo específico do pacote para começar se qualquer um dos padrões deve ser alterado.

**Observação**  As informações a seguir só podem ser usadas para modificar arquivos de configuração gerados do sequenciador para personalizar pacotes para atender a requisitos específicos de um usuário ou grupo.

 

### Conteúdo do arquivo de configuração dinâmica

Todas as adições, exclusões e atualizações nos arquivos de configuração precisam ser feitas em relação aos valores padrão especificados pelas informações de manifesto do pacote. Revise a seguinte tabela:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Arquivo de configuração do usuário. xml</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivo de implantação de configuração. xml</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manifesto do pacote</p></td>
</tr>
</tbody>
</table>

 

A tabela anterior representa como os arquivos serão lidos. A primeira entrada representa o que será lido por último, portanto, o conteúdo terá precedência. Portanto, todos os pacotes contêm inerentemente e fornecem configurações padrão do manifesto do pacote. Se um arquivo Configuration. XML de implantação com configurações personalizadas for aplicado, ele substituirá os padrões de manifesto do pacote. Se um arquivo de configuração de usuário. XML com configurações personalizadas for aplicado antes disso, ele substituirá a configuração de implantação e os padrões de manifesto do pacote.

A lista a seguir exibe mais informações sobre os dois tipos de arquivo:

-   **Arquivo de configuração do usuário (userconfig)** – permite que você especifique ou modifique configurações personalizadas para um pacote. Essas configurações serão aplicadas para um usuário específico quando o pacote for implantado em um computador que esteja executando o cliente App-V 5,0.

-   **Arquivo de configuração de implantação (deploymentconfig)** – permite que você especifique ou modifique as configurações padrão para um pacote. Essas configurações serão aplicadas a todos os usuários quando um pacote for implantado em um computador que esteja executando o cliente App-V 5,0.

Para personalizar as configurações de um pacote para um conjunto específico de usuários em um computador ou para fazer alterações que serão aplicadas a locais de usuários locais, como o HKCU, o arquivo userconfig deve ser usado. Para modificar as configurações padrão de um pacote para todos os usuários em um computador ou para fazer alterações que serão aplicadas a locais globais, como HKEY \ _LOCAL \ _MACHINE e a pasta All Users, o arquivo DeploymentConfig deve ser usado.

O arquivo userconfig fornece configurações que podem ser aplicadas a um único usuário sem afetar outros usuários em um cliente:

-   Extensões que serão integradas ao sistema nativo por usuário:-atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM

-   Subsistemas virtuais:-objetos do aplicativo, variáveis de ambiente, modificações do registro, serviços e fontes

-   Scripts (somente contexto do usuário)

-   Gerenciando autoridade (para controlar a coexistência do pacote com o App-V 4,6)

O arquivo DeploymentConfig fornece configurações em duas seções, uma em relação ao contexto da máquina e uma em relação ao contexto do usuário fornecendo as mesmas funcionalidades listadas na lista userconfig acima:

-   Todas as configurações de userconfig acima

-   Extensões que só podem ser aplicadas globalmente para todos os usuários

-   Subsistemas virtuais que podem ser configurados para locais de máquinas globais, por exemplo, registro

-   URL da fonte do produto

-   Scripts (somente contexto da máquina)

-   Controles para encerrar processos filho

### Estrutura de arquivos

A estrutura do arquivo de configuração dinâmica do App-V 5,0 é explicada na seção a seguir.

### Arquivo de configuração de usuário dinâmico

**Header** -o cabeçalho de um arquivo de configuração de usuário dinâmico é o seguinte:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

O **PackageID** é o mesmo valor que existe no arquivo de manifesto.

**Corpo** -o corpo do arquivo de configuração de usuário dinâmico pode incluir todos os pontos de extensão do aplicativo definidos no arquivo de manifesto, bem como informações para configurar aplicativos virtuais. Há quatro subseções permitidas no corpo:

1. **Aplicativos** – todas as extensões de aplicativo que estão contidas no arquivo de manifesto dentro de um pacote são atribuídas com uma ID de aplicativo, que também é definida no arquivo de manifesto. Isso permite que você habilite ou desabilite todas as extensões para um determinado aplicativo em um pacote. A **ID do aplicativo** deve existir no arquivo de manifesto ou será ignorada.

   &lt;Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Aplicativos&gt;

   &lt;!--Nenhum novo aplicativo pode ser definido na política. O cliente AppV ignorará qualquer ID de aplicativo que não esteja também no arquivo de manifesto--&gt;

   &lt;ID do aplicativo = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. **Subsistemas** -AppExtensions e outros subsistemas são organizados como subnós nos &lt; subsistemas &gt; :

   &lt;Userconfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Subsistemas&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Cada subsistema pode ser habilitado/desabilitado usando o atributo "**Enabled**". Veja a seguir vários subsistemas e exemplos de uso.

   **Extensions**

   Alguns subsistemas (subsistemas de extensão) extensões de controle. Esses subsistemas são:-atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM

   Subsistemas de extensão podem ser habilitados e desabilitados independentemente do conteúdo.  Portanto, se os atalhos estiverem habilitados, o cliente usará os atalhos contidos no manifesto por padrão. Cada subsistema de extensão pode conter &lt; um &gt; nó de extensões. Se esse elemento filho estiver presente, o cliente ignorará o conteúdo do arquivo de manifesto desse subsistema e somente usará o conteúdo do arquivo de configuração.

   Exemplo usando o subsistema de atalhos:

   1.  Se o usuário definiu isso no arquivo de configuração dinâmica ou de implantação:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Se o usuário tiver definido somente o seguinte:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Se o usuário definir o seguinte

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   Então, todos os atalhos dentro do manifesto ainda serão ignorados. Não haverá nenhum atalho integrado.

   Os subsistemas de extensão suportados são:

   **Atalhos:** Isso controla atalhos que serão integrados ao sistema local. Veja a seguir um exemplo com 2 atalhos:

   &lt;Subsistemas&gt;

   &lt;Atalhos habilitados = "verdadeiro"&gt;

     &lt;Extensões&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/Extension&gt;

     &lt;Categoria de extensão = "AppV. Shortcut"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Associações de tipo de arquivo:** Associa tipos de arquivos aos programas para abrir por padrão, bem como configurar o menu de contexto. (Os tipos MIME também podem ser configurados usando essa susbsystem). Exemplo de associação de tipo de arquivo está abaixo:

   &lt;FileTypeAssociations Enabled = "true"&gt;

   &lt;Extensões&gt;

     &lt;Extension category = "AppV. FileTypeAssociation"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **Protocolos de URL**: controla os protocolos de URL que são integrados ao registro local da máquina do cliente, por exemplo, "mailto:".

   &lt;URLProtocols Enabled = "true"&gt;

   &lt;Extensões&gt;

   &lt;Extension category = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Nome &gt; mailto &lt; /Name&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Descritivo&gt;

     &lt;AppUserModelId&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;InfoTip&gt;

   &lt;SourceFilter /&gt;

     &lt;ShellFolder /&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;CLSID&gt;

     &lt;ShellCommands&gt;

     &lt;Netcommand &gt; Open &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Nome &gt; aberto &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Observação/m "%1" &lt; /CommandLine&gt;

     &lt;DropTargetClassId /&gt;

     &lt;FriendlyName&gt;

     &lt;/Extended estendido &gt; 0 &lt;&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Aplicativos &gt; ContosoMail &lt; /Application&gt;

     &lt;Tópico &gt; ShellSystem &lt; /topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Clientes de software**: permite que o aplicativo se registre como um cliente de email, leitor de notícias, Media Player e torna o aplicativo visível na interface do usuário definir acesso do programa e padrões do computador. Na maioria dos casos, você só precisa habilitá-lo e desabilitá-lo. Também há um controle para habilitar e desabilitar o cliente de email especificamente se você quiser que os outros clientes ainda estejam habilitados, exceto para esse cliente.

   &lt;SoftwareClients Enabled = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "false"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths:-se um aplicativo por exemplo contoso.exe for registrado com um nome AppPath de "MyApp", ele permitirá que você digite "MyApp" no menu executar e ele será aberto contoso.exe.

   &lt;AppPaths Enabled = "true"&gt;

   &lt;Extensões&gt;

   &lt;Extension category = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Nome &gt;contosomail.exe&lt; /Name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; falsa &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl /&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: permite que um aplicativo registre servidores com locais. O Mode pode ser integração, isolado ou desligado. Quando ISOL.

   &lt;Modo COM = "isolado"/&gt;

   **Outras configurações**:

   Além das extensões, outros subsistemas podem ser habilitados/desabilitados e editados:

   **Objetos de núcleo virtual**:

   &lt;Objetos habilitados = "falso"/&gt;

   **Registro virtual**: usado se você deseja definir um registro no registro virtual dentro de HKCU

   &lt;Registro Enabled = "true"&gt;

   &lt;Conter&gt;

   &lt;Caminho da chave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Tipo de valor = "REG \ _SZ" Name = "bar" data = "NewValue"/&gt;

    &lt;/Key&gt;

     &lt;Caminho da chave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Remover&gt;

     &lt;/Registry&gt;

   **Sistema de arquivos virtual**

         &lt;FileSystem Enabled="true" /&gt;

   **Fontes virtuais**

         &lt;Fonts Enabled="false" /&gt;

   **Variáveis de ambiente virtual**

   &lt;EnvironmentVariables Enabled = "true"&gt;

   &lt;Conter&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Serviços virtuais**

         &lt;Services Enabled="false" /&gt;

3. **Userscript** – os scripts podem ser usados para configurar ou alterar o ambiente virtual, bem como executar scripts no momento da implantação ou remoção, antes do aplicativo ser executado ou podem ser usados para "limpar" o ambiente após o encerramento do aplicativo. Faça referência a um arquivo de configuração de usuário de exemplo que é exibido pelo sequenciador para ver um exemplo de script. A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados.

4. **ManagingAuthority** – pode ser usado quando duas versões do pacote são coexistentes na mesma máquina, uma implantada no app-v 4,6 e outras implantadas no app-v 5,0. Para permitir que o App-V vNext assuma os pontos de extensão do App-V 4,6 para o pacote nomeado, digite o seguinte no arquivo userconfig (em que PackageName é o GUID do pacote no App-V 4,6:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;

### Arquivo de configuração de implantação dinâmica

**Header** -o cabeçalho de um arquivo de configuração de implantação é o seguinte:

&lt;? XML Version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

O **PackageID** é o mesmo valor que existe no arquivo de manifesto.

**Corpo** -o corpo do arquivo de configuração de implantação inclui duas seções:

-   Seção de configuração do usuário – permite o mesmo conteúdo que o arquivo de configuração do usuário descrito na seção anterior. Quando o pacote for publicado para um usuário, as configurações de configuração do appextensions nesta seção substituirão as configurações correspondentes no manifesto dentro do pacote, a menos que um arquivo de configuração do usuário também seja fornecido. Se um arquivo userconfig também for fornecido, ele será usado em vez das configurações de usuário no arquivo de configuração de implantação. Se o pacote for publicado globalmente, somente o conteúdo do arquivo de configuração de implantação será usado em combinação com o manifesto.

-   Seção de configuração da máquina – contém informações que podem ser configuradas somente para uma máquina inteira, não para um usuário específico na máquina. Por exemplo, HKEY \ _LOCAL \ _MACHINE chaves do registro no VFS.

&lt;DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "reservado" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;Userconfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Configuração do usuário** – use a seção **arquivo de configuração do usuário dinâmico** anterior para obter informações sobre as configurações fornecidas na seção configuração do usuário do arquivo de configuração de implantação.

Configuração da máquina – a seção configuração da máquina do arquivo de configuração de implantação é usada para configurar informações que podem ser definidas somente para uma máquina inteira, não para um usuário específico no computador. Por exemplo, HKEY \ _LOCAL \ _MACHINE chaves do registro no registro virtual. Há quatro subseções permitidas nesse elemento

1.  **Subsistemas** -AppExtensions e outros subsistemas são organizados como subnós em &lt; subsistemas &gt; :

    &lt;MachineConfiguration&gt;

      &lt;Subsistemas&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    A seção a seguir exibe os vários subsistemas e exemplos de uso.

    **Extensões**:

    Alguns subsistemas (subsistemas de extensão) extensões de controle que só podem se aplicar a todos os usuários. O subsistema é recurso de aplicativo. Como isso só pode se aplicar a todos os usuários, o pacote deve ser publicado globalmente para que esse tipo de extensão seja integrado ao sistema local. As mesmas regras para controles e configurações que se aplicam às extensões na configuração do usuário também se aplicam aos usuários na seção MachineConfiguration.

    **Recursos do aplicativo**: usado por programas padrão na interface do sistema operacional Windows. Permite que um aplicativo se registre como capaz de abrir determinadas extensões de arquivo, como um Contender para o menu iniciar slot do navegador da Internet, como capaz de abrir certos tipos MIME do Windows.Essa extensão também torna o aplicativo virtual visível na interface do usuário definir programas padrão.:

    &lt;ApplicationCapabilities Enabled = "true"&gt;

      &lt;Extensões&gt;

       &lt;Extension category = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;Recurso&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Outras configurações**:

    Além das extensões, outros subsistemas podem ser editados:

    **Registro virtual em toda a máquina**: usado quando você deseja definir uma chave do registro no registro virtual em HKEY \ _Local \ _Machine

    &lt;Registro&gt;

    &lt;Conter&gt;

      &lt;Caminho da chave = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Caminho da chave = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Remover&gt;

    &lt;/Registry&gt;

    **Objetos de núcleo virtual em toda a máquina**

    &lt;Eles&gt;

    &lt;Não isolar&gt;

       &lt;Nome do objeto = "TestObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: indica se a URL do pacote pode ser modificada globalmente por meio do PackageSourceRoot (para dar suporte a cenários de filial do escritório). O padrão é falso e a alteração da configuração entra em vigor na próxima inicialização.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut Enabled = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** – o pacote pode ser configurado para executar scripts no momento da implantação, publicação ou remoção. Faça referência a um arquivo de configuração de implantação de exemplo gerado pelo sequenciador para ver um exemplo de script. A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados

4.  **TerminateChildProcess**:-um executável do aplicativo pode ser especificado, cujos processos filho serão encerrados quando o processo exe do aplicativo for finalizado.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Scripts

A tabela a seguir descreve os vários eventos de script e o contexto em que eles podem ser executados.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tempo de execução do script</th>
<th align="left">Pode ser especificado na configuração de implantação</th>
<th align="left">Pode ser especificado na configuração do usuário</th>
<th align="left">Pode ser executado no ambiente virtual do pacote</th>
<th align="left">Pode ser executado no contexto de um aplicativo específico</th>
<th align="left">Executado no contexto do sistema/usuário: (configuração da implantação, configuração do usuário)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/D)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema, usuário)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema, usuário)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/D)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Usuário, usuário)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Usuário, usuário)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Usuário, usuário)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Usuário, usuário)</p></td>
</tr>
</tbody>
</table>

 

### Criar um arquivo de configuração dinâmico usando um arquivo de manifesto do App-V 5,0

Você pode criar o arquivo de configuração dinâmica usando um dos três métodos: manualmente, usando o console de gerenciamento do App-V 5,0 ou sequenciando um pacote, que será gerado com dois arquivos de exemplo.

Para obter mais informações sobre como criar o arquivo usando o console de gerenciamento do App-V 5,0, consulte [como criar um arquivo de configuração personalizado usando o console de gerenciamento do App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Para criar o arquivo manualmente, as informações acima nas seções anteriores podem ser combinadas em um único arquivo. Recomendamos que você use arquivos gerados pelo sequenciador.






## Tópicos relacionados


[Como aplicar o arquivo de configuração da implantação usando o PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[Como aplicar o arquivo de configuração do usuário usando o PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





