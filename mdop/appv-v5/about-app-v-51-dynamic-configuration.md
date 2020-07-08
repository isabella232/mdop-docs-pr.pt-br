---
title: Sobre a configuração dinâmica do App-V 5,1
description: Você pode usar a configuração dinâmica para personalizar um pacote App-V 5,1 para um usuário. Use as informações a seguir para criar ou editar um arquivo de configuração dinâmica existente.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796630"
---
# Sobre a configuração dinâmica do App-V 5,1 
Com a configuração dinâmica, você pode editar o arquivo de configuração dinâmica para personalizar como um pacote do App-V 5,1 é executado para um usuário ou grupo. A personalização do pacote remove a necessidade de resequenciar pacotes usando as configurações desejadas.  Ele também fornece uma maneira de manter o conteúdo do pacote e as configurações personalizadas de forma independente.

Os pacotes de aplicativos virtuais contêm um manifesto que fornece todas as informações básicas do pacote. Essas informações incluem os padrões para as configurações do pacote e determina as configurações na forma mais básica (sem personalização adicional). 

Quando um pacote é criado, o sequenciador gera a implantação padrão e os arquivos. XML automaticamente usando os dados do manifesto do pacote. Portanto, esses arquivos gerados refletem as configurações padrão configuradas durante o sequenciamento. Se você aplicar esses arquivos a um pacote no formato gerado pelo sequenciador, os pacotes terão as mesmas configurações padrão que vieram do manifesto. 

Use esses arquivos gerados para fazer alterações, se necessário, o que não afeta diretamente o pacote. Se você quiser adicionar, excluir ou atualizar os arquivos de configuração, faça as alterações sobre os valores padrão nas informações do manifesto.

>[!TIP]
>A ordem em que os arquivos são lidos são:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Manifesto</li></ul><p>A primeira entrada representa o que é lido por último. Portanto, o conteúdo tem precedência e todos os pacotes contêm inerentemente e fornecem configurações padrão do manifesto do pacote.<ol><li> Se personalizar o arquivo de DeploymentConfig.xml e aplicar as configurações personalizadas, as configurações padrão no manifesto do pacote serão substituídas. </li><li> Se personalizar o UserConfig.xml e aplicar as configurações personalizadas, as configurações padrão para a configuração de implantação e o manifesto de pacote serão substituídas. </li></ol>

## Conteúdo do arquivo de configuração do usuário (UserConfig.xml)
O arquivo userconfig fornece configurações que são aplicadas para um usuário específico ao implantar o pacote em um computador executando o cliente App-V 5,1.  Essas configurações não afetam outros usuários do cliente.

Use o arquivo userconfig para especificar ou modificar as configurações personalizadas de um pacote:

-   Extensões integradas ao sistema nativo por usuário: atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM
-   Subsistemas virtuais: objetos do aplicativo, variáveis de ambiente, modificações do registro, serviços e fontes
-   Scripts (somente contexto do usuário)
-   Gerenciando autoridade (para controlar a coexistência do pacote com o App-V 4,6)

### Cabeçalho

O cabeçalho de um arquivo de configuração de usuário dinâmico é semelhante ao seguinte:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

O **PackageID** é o mesmo valor que existe no arquivo de manifesto.


### Body

O corpo do arquivo de configuração de usuário dinâmico pode incluir todos os pontos de extensão do aplicativo definidos no arquivo de manifesto, bem como as informações para configurar aplicativos virtuais. Há quatro subseções permitidas no corpo:

1.  **[Aplicativos](#applications)** 
2.  **[Subsistemas](#subsystems)**
3.  **[Userscript](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Aplicativos

Todas as extensões de aplicativo contidas no arquivo de manifesto dentro de um pacote têm uma ID de aplicativo atribuída, que você encontra no arquivo de manifesto. A ID do aplicativo permite habilitar ou desabilitar todas as extensões para um determinado aplicativo em um pacote. A ID do aplicativo deve existir no arquivo de manifesto ou é ignorada.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Subsistemas

AppExtensions e outros subsistemas organizados como subnós.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Você pode habilitar ou desabilitar cada subsistema usando o atributo **Enabled** .

**Extensões** 

Alguns subsistemas (subsistemas de extensão) extensões de controle. Esses subsistemas são atalhos, associações de tipo de arquivo, protocolos de URL, AppPaths, clientes de software e COM.

Subsistemas de extensão podem ser habilitados e desabilitados independentemente do conteúdo. Por exemplo, se você habilitar atalhos, o cliente usará os atalhos contidos no manifesto por padrão. Cada subsistema de extensão pode conter um \<Extensions\> nó. Se esse elemento filho estiver presente, o cliente ignora o conteúdo do arquivo de manifesto desse subsistema e só usa o conteúdo do arquivo de configuração. 

_**Exemplos:**_ 

- Se você definir isso no arquivo de configuração de usuário ou de implantação, o conteúdo do manifesto será ignorado.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Se você definir somente o seguinte, o conteúdo do manifesto será integrado durante a publicação.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Se você definir o seguinte, todos os atalhos dentro do manifesto ainda serão ignorados. Em outras palavras, nenhum atalho fica integrado.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Subsistemas de extensão com suporte:**_ 

Subsistema de extensão de **atalhos** controla quais atalhos são integrados ao sistema local.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

O subsistema de extensão do **tipo de arquivo** associa os tipos de arquivo aos programas para abrir por padrão, bem como configurar o menu de contexto. 

>[!TIP]
>Você pode configurar o subsistema com tipos MIME.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

Subsistema de extensão de **protocolos de URL** controla os protocolos de URL integrados ao registro local da máquina do cliente, por exemplo, _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

O subsistema de extensão de **clientes de software** permite que o aplicativo se registre como um cliente de email, leitor de notícias, Media Player e torna o aplicativo visível na interface do usuário definir acesso do programa e padrões do computador. Na maioria dos casos, você só precisa habilitá-lo e desabilitá-lo. Também há um controle para habilitar e desabilitar o cliente de email especificamente se você quiser que os outros clientes ainda estejam habilitados, exceto para esse cliente.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

Subsistema de extensão **AppPaths** abre aplicativos registrados com um caminho de aplicativo. Por exemplo, se contoso.exe tem um nome AppPath de _MyApp_, os usuários podem digitar _MyApp_ no menu executar, abrindo contoso.exe.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

O subsistema de extensões **com** permite um aplicativo registrado em servidores com locais. O modo pode ser:

-   Integração
-   Isola 
-   Desativada

```XML

<COM Mode="Isolated"/>
```

**Objetos de núcleo virtual**

```XML

<Objects Enabled="false" />
```

O **registro virtual** define um registro no registro virtual dentro de HKCU.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Sistema de arquivos virtual**

```XML

    <FileSystem Enabled="true" />
```

**Fontes virtuais**

```XML

      <Fonts Enabled="false" />
```

**Variáveis de ambiente virtual**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Serviços virtuais**

```XML

      <Services Enabled="false" />
```

#### Userscript

Use userscripttes para configurar ou alterar o ambiente virtual.  Você também pode executar scripts no momento da implantação ou para limpar o ambiente após o encerramento do aplicativo. Para ver um exemplo de script, consulte o arquivo de configuração do usuário gerado pelo sequenciador. A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados.

#### ManagingAuthority

Use o ManagingAuthority quando duas versões do pacote estiverem em coexistência na mesma máquina, uma implantada para o App-V 4,6 e outra implantada no App-V 5,0. Para permitir que o App-V vNext assuma os pontos de extensão do App-V 4,6 para o pacote nomeado, digite o seguinte no arquivo userconfig (em que PackageName é o GUID do pacote no App-V 4,6:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## Arquivo de configuração de implantação (DeploymentConfig.xml)

O arquivo DeploymentConfig fornece configurações para contexto de máquina e contexto de usuário, fornecendo os mesmos recursos listados no arquivo userconfig. A configuração é aplicada durante a implantação do pacote em um computador que executa o cliente App-V 5,1.

Use o arquivo DeploymentConfig para especificar ou modificar as configurações personalizadas de um pacote:

- Todas as configurações de userconfig
- Extensões que só podem ser aplicadas globalmente para todos os usuários
- Subsistemas virtuais para locais de máquinas globais, por exemplo, o registro
- URL da fonte do produto
- Scripts (somente contexto da máquina)
- Controles para encerrar processos filho

### Cabeçalho

O cabeçalho de um arquivo de configuração de implantação dinâmica é semelhante ao seguinte:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

O **PackageID** é o mesmo valor que existe no arquivo de manifesto.

### Body

O corpo do arquivo de configuração de implantação dinâmica inclui duas seções:

- **Userconfiguration:** permite o mesmo conteúdo que o arquivo de configuração do usuário descrito na seção anterior.  Durante a publicação do pacote para um usuário, qualquer configuração de appextensions nesta seção substituirá as configurações correspondentes no manifesto dentro do pacote, a menos que você forneça um arquivo de configuração do usuário. Se também fornecer um arquivo userconfig, ele será usado em vez das configurações de usuário no arquivo de configuração de implantação. Ao publicar o pacote globalmente, somente o conteúdo do arquivo de configuração de implantação é usado em combinação com o manifesto. Para obter mais detalhes, consulte [conteúdo do arquivo de configuração do usuário (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** contém informações que podem ser configuradas somente para uma máquina inteira, não para um usuário específico na máquina. Por exemplo, HKEY_LOCAL_MACHINE chaves do registro no VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### Userconfiguration

Confira o [conteúdo do arquivo de configuração do usuário (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) para obter informações sobre as configurações fornecidas para esta seção. 

### MachineConfiguration

Use a seção MachineConfiguration para configurar informações para uma máquina inteira; Não para um usuário específico no computador. Por exemplo, HKEY_LOCAL_MACHINE chaves do registro no registro virtual. Há quatro subseções permitidas nesse elemento:

1.  **[Subsistemas](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Subsistemas

AppExtensions e outros subsistemas organizados como subnós.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Você pode habilitar ou desabilitar cada subsistema usando o atributo **Enabled** .

**Extensões** 

Alguns subsistemas (subsistemas de extensão) extensões de controle. O subsistema é um recurso de aplicativos que os programas padrão usam. Para esse tipo de extensão, o pacote deve ser publicado globalmente para integração com o sistema local. As mesmas regras para controles e configurações que se aplicam às extensões na configuração do usuário também se aplicam aos usuários na seção MachineConfiguration.

**Recursos do aplicativo**: usado por programas padrão que permitem que um aplicativo se registre como:

- Capacidade de abrir extensões de arquivo específicas
- Um Contender para o menu iniciar slot do navegador da Internet
- Capacidade de abrir tipos específicos de MIME do Windows

Essa extensão também torna o aplicativo virtual visível na interface do usuário definir programas padrão.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Subsistemas de extensão com suporte:**_ 

Subsistema de extensão **do registro virtual de máquina** define uma chave do registro no registro virtual em HKEY_LOCAL_MACHINE.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Objetos de núcleo virtual em toda a máquina**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

Use ProductSourceURLOptOut para indicar que a URL do pacote pode ser modificada globalmente por meio do _PackageSourceRoot_ (para dar suporte a cenários de filial do escritório). As alterações entram em vigor na próxima inicialização. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

O pacote pode ser configurado para executar scripts no momento da implantação, publicação ou remoção. Para ver um exemplo de script, consulte o arquivo de configuração de implantação gerado pelo sequenciador. 

A seção scripts abaixo fornece mais informações sobre os vários gatilhos que podem ser usados.

#### TerminateChildProcess

Um executável de aplicativo pode ser especificado, cujos processos filho são encerrados quando o processo exe do aplicativo é encerrado.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Scripts

A tabela a seguir descreve os vários eventos de script e o contexto em que eles podem ser executados.

| Tempo de execução do script       | Pode ser especificado na configuração de implantação | Pode ser especificado na configuração do usuário | Pode ser executado no ambiente virtual do pacote | Pode ser executado no contexto de um aplicativo específico | Executado no contexto do sistema/usuário: (configuração da implantação, configuração do usuário) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/D)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (Sistema, usuário)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (Sistema, usuário)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/D)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (Usuário, usuário)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Usuário, usuário)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Usuário, usuário)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Usuário, usuário)                                                                |

### Usar vários scripts em um único gatilho de evento

O App-V 5,1 oferece suporte ao uso de vários scripts em um único gatilho de evento para pacotes do App-V, incluindo pacotes que você converte do App-V 4,6 para o App-V 5,0 ou posterior. Para habilitar o uso de vários scripts, o App-V 5,1 usa um aplicativo inicializador de scripts, chamado ScriptRunner.exe, que é instalado como parte da instalação do App-V Client.

### Como usar vários scripts em um único gatilho de evento

Para cada script que você deseja executar, passe esse script como um argumento para o aplicativo ScriptRunner.exe. Em seguida, o aplicativo executa cada script separadamente, juntamente com os argumentos que você especificar para cada script. Use apenas um script (ScriptRunner.exe) por disparador.

> [!NOTE]
> 
> Recomendamos que você execute a linha de multiscript em um prompt de comando primeiro para garantir que todos os argumentos sejam compilados corretamente antes de adicioná-los ao arquivo de configuração de implantação.

### Descrições de script e parâmetro de exemplo

Usando o arquivo e a tabela de exemplo a seguir, modifique o arquivo de implantação ou configuração do usuário para adicionar os scripts que você deseja executar.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**Os parâmetros no arquivo de exemplo incluem:**

#### \<AddPackage\>

Nome do gatilho de evento para o qual você está executando um script, como adicionar um pacote ou publicar um pacote.

#### \<Path\>ScriptRunner.exe\</Path\>

O aplicativo inicializador de scripts que é instalado como parte da instalação do aplicativo App-V Client.

> [!NOTE]
> 
> Embora ScriptRunner.exe seja instalado como parte do cliente App-V, a localização do cliente App-V deve estar em% path% ou ScriptRunner não será executado. ScriptRunner.exe geralmente está localizado no Virtualizationfolder C:FilesApplication.

#### \<Arguments\>

`-appvscript` -Token que representa o script real que você deseja executar.

`script1.exe` – Nome do script que você deseja executar.

`arg1 arg2` – Argumentos para o script que você deseja executar.

`-appvscriptrunnerparameters` – Token que representa as opções de execução para script1.exe.

`-wait` – Token que informa ao ScriptRunner para esperar a execução de script1.exe para concluir antes de prosseguir para o próximo script.

`-timeout=x` – Token que informa ScriptRunner para parar de executar o script atual após x número de segundos. Todos os outros scripts especificados ainda são executados.

`-rollbackonerror` – Token que informa ao ScriptRunner para parar de executar todos os scripts que ainda não foram executados e reverter um erro para o cliente App-V.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Aguarda a conclusão geral do ScriptRunner.exe.

Defina o valor de tempo limite do executor geral para ser maior ou igual à soma dos valores de tempo limite dos scripts individuais.

Se algum script individual relatou um erro e rollbackonerror foi definido como true, então ScriptRunner reportaria o erro para o cliente App-V.

O ScriptRunner executa qualquer script cujo tipo de arquivo esteja associado a um aplicativo instalado no computador. Se o aplicativo associado estiver ausente ou o tipo de arquivo do script não estiver associado a nenhum aplicativo no computador, o script não será executado.

### Criar um arquivo de configuração dinâmico usando um arquivo de manifesto do App-V 5,1

Você pode criar o arquivo de configuração dinâmica usando um dos três métodos: manualmente, usando o console de gerenciamento do App-V 5,1 ou sequenciando um pacote, que gera dois arquivos de exemplo. Para obter mais informações sobre como criar o arquivo usando o console de gerenciamento do App-V 5,1, consulte [como criar um arquivo de configuração personalizado usando o console de gerenciamento do App-v 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Para criar o arquivo manualmente, as informações acima nas seções anteriores podem ser combinadas em um único arquivo. Recomendamos que você use arquivos gerados pelo sequenciador.



- Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).
- Para problemas com o App-V, use o [Fórum do TechNet do App-v](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados

- [Como aplicar o arquivo de configuração da implantação usando o PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [Como aplicar o arquivo de configuração do usuário usando o PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Operações para o App-V 5.1](operations-for-app-v-51.md)

---
