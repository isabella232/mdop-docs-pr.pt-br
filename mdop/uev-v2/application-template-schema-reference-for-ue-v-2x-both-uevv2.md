---
title: Referência de esquema de modelo de aplicativo para UE-V 2. x
description: Referência de esquema de modelo de aplicativo para UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800066"
---
# Referência de esquema de modelo de aplicativo para UE-V 2. x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usam modelos de localização de configurações XML para definir as configurações do aplicativo da área de trabalho e as configurações do Windows que são capturadas e aplicadas pela UE-V. O UE-V inclui um conjunto de modelos de local de configurações padrão. Você também pode criar modelos de local de configurações personalizadas com o UE-V Generator.

Um usuário avançado pode personalizar o arquivo XML de um modelo de local de configurações. Este tópico detalha a estrutura XML dos modelos de localização de configurações do UE-V 2,1 (SP1) e do 2,0 e fornece orientação para a edição desses arquivos.

## Referência de esquema de modelo de aplicativo do UE-V 2,1 e do 2,1 SP1


Esta seção detalha a estrutura XML do modelo de local de configurações do UE-V 2,1 e do 2,1 SP1 e fornece orientação para a edição desse arquivo.

### Nesta seção

-   [Atributo XML de declaração e codificação](#xml21)

-   [Namespace e elemento raiz](#namespace21)

-   [Tipos de dados](#data21)

-   [Elemento Name](#name21)

-   [Elemento ID](#id21)

-   [Elemento Version](#version21)

-   [Elemento Author](#author21)

-   [Elemento processos e processo](#processes21)

-   [Elemento de aplicativo](#application21)

-   [Elemento comum](#common21)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate21)

-   [Apêndice: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>Atributo XML de declaração e codificação

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

A declaração XML deve especificar o atributo XML versão 1,0 ( &lt; ? XML Version = "1.0" &gt; ). Os modelos de local de configurações criados pelo UE-V Generator são salvos na codificação UTF-8, embora a codificação não seja especificada explicitamente. Recomendamos que você inclua o atributo encoding = "UTF-8" nesse elemento como prática recomendada. Todos os modelos incluídos com o produto também especificam essa marca (veja os documentos na experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\Templates para fins de referência). Por exemplo:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Namespace e elemento raiz

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

O UE-V usa o https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace para todos os aplicativos. SettingsLocationTemplate é o elemento raiz e contém todos os outros elementos. Referência SettingsLocationTemplate em todos os modelos usando esta marca:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Tipos de dados

Estes são os tipos de dados do esquema de modelo de aplicativo do UE-V.

<a href="" id="guid"></a>**GUID** GUID descreve uma expressão regular de identificador global exclusivo padrão no formulário "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Isso é usado no elemento Filesetting\\Root\\KnownFolder para verificar a formatação de pastas bem conhecidas.

<a href="" id="filenamestring"></a>**Filenamestring** Filenamestring refere-se ao nome de arquivo de um processo a ser monitorado. Seus valores são restritos pelo Regex \ [^ \ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, (ou seja, eles podem não conter caracteres de barra invertida, asterisco ou ponto de interrogação caracteres curinga, o caractere de pipe, o sinal de maior ou menor que, barra de encaminhamento ou caracteres de dois pontos).

<a href="" id="idstring"></a>**IDString** IDString refere-se ao valor ID dos elementos do aplicativo, SettingsLocationTemplate e dos elementos comuns (usados para descrever os pacotes de aplicativos que compartilham configurações comuns). Ele é restrito pelo mesmo Regex como filenamestring (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion é um valor inteiro usado para descrever a revisão do modelo de local de configurações. Seu valor pode variar de 0 a 2147483647.

<a href="" id="empty"></a>Em **branco** Vazio refere-se a um valor nulo. Isso é usado no Process\\ShellProcess para indicar que não há processo para monitorar. Esse valor não deve ser usado em nenhum modelo de aplicativo.

<a href="" id="author"></a>**Criar** O tipo de dados autor é um tipo complexo que identifica o autor de um modelo. Ele contém dois elementos filho: **Name** e **email**. Dentro do tipo de dados autor, o elemento Name é obrigatório enquanto o elemento de email é opcional. Esse tipo é descrito em mais detalhes sob o elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervalo** de Range define uma classe Integer que consiste em dois elementos filho: **mínimo** e **máximo**. Esse tipo de dados é implementado no tipo de dados ProcessVersion. Se especificado, os valores mínimo e máximo devem ser incluídos.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion define um tipo com quatro elementos filho: **Major**, **Minor**, **Build**e **patch**. Esse tipo de dados é usado pelo elemento processo para preencher seus valores ProductVersion e FileVersion. Os dados desse tipo são um valor de intervalo. O principal elemento filho é obrigatório e os outros são opcionais.

<a href="" id="architecture"></a>**Arquitetura** do A arquitetura enumera dois valores possíveis: **Win32** e **Win64**. Esses valores são usados para especificar a arquitetura do processo.

<a href="" id="process"></a>**Processo** O tipo de dados processo é um contêiner usado para descrever os processos a serem monitorados pela UE-V. Ele contém seis elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**. Esta tabela detalha os respectivos tipos de dados de cada elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Tipo de Dados</strong></p></td>
<td align="left"><p><strong>Obrigatório</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Arq</p></td>
<td align="left"><p>Filenamestring</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquitetura</p></td>
<td align="left"><p>Arquitetura</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processar** O tipo de dados Processes representa um contêiner para uma coleção de um ou mais elementos de processo. Dois elementos filho são compatíveis com o tipo de sequência Processes: **process** e **ShellProcess**. Processo é um elemento do tipo processo e ShellProcess é do tipo de dados vazio. Pelo menos um item deve ser identificado na sequência.

<a href="" id="path"></a>**Caminho** Path é consumido pela configuração RegistrySetting e filepara se referir a caminhos de arquivo e registro. Esse elemento dá suporte a dois atributos opcionais: **recursive** e **DeleteIfNotFound**. Ambos os valores são definidos como default = "false".

Recursiva indica que o caminho e todas as subpastas estão incluídos para configurações de arquivo ou que todas as chaves do registro filho estão incluídas para as configurações do registro. Em ambos os casos, todos os itens no nível atual são incluídos nos dados capturados. Para um objeto filesettings, todos os arquivos na pasta especificada são incluídos nos dados capturados pela UE-V, mas as pastas não estão incluídas. Para caminhos de registro, todos os valores no caminho atual são capturados, mas as chaves do registro filho não são capturadas. Em ambos os casos, deve-se tomar cuidado para evitar a captura de grandes conjuntos de dados ou grandes números de itens.

O atributo DeleteIfNotFound remove a configuração dos dados do caminho de armazenamento das configurações do usuário. Isso pode ser desejável em casos em que a remoção dessas configurações do pacote irá salvar uma grande quantidade de espaço em disco no servidor de arquivos do caminho de armazenamento de configurações.

<a href="" id="filemask"></a>**Máscara** de Filemask especifica apenas determinados tipos de arquivo para a pasta que é definida por path. Por exemplo, o caminho pode ser `C:\users\username\files` e filemask poderia ser `*.txt` apenas incluir arquivos de texto.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting representa um contêiner para chaves do registro e valores e o comportamento desejado associado na parte do UE-V Agent. Quatro elementos filho são definidos neste tipo: **Path**, **Name**, **Exclude**e uma sequência do **caminho** e **nome**do valor.

<a href="" id="filesetting"></a>**Configuração** do Filesetting contém parâmetros associados a arquivos e caminhos de arquivos. Quatro elementos filho são definidos: **root**, **Path**, **filemask**e **Exclude**. A raiz é obrigatória e as outras são opcionais.

<a href="" id="settings"></a>**Configurações** de Configurações é um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction descritas anteriormente. Além disso, ele também pode conter os seguintes elementos filho com comportamentos descritos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Assíncrono</p></td>
<td align="left"><p>Os pacotes de configurações assíncronas são aplicados sem bloquear a inicialização do aplicativo para que o início do aplicativo continue enquanto as configurações ainda estiverem sendo aplicadas. Isso é útil para configurações que podem ser aplicadas de forma assíncrona, como aquelas <code>get/set</code> por meio de uma API, como SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Por padrão, o UE-V salva apenas as configurações de um aplicativo quando a última instância de um aplicativo que usa o modelo é fechada. Quando esse elemento é definido como ' false ', o UE-V exporta as configurações mesmo se outras instâncias de um aplicativo estiverem em execução. Modelos adequados – aqueles que incluem uma seção de elementos comuns – que são fornecidos com o UE-V usam esse sinalizador para habilitar as configurações compartilhadas para sempre exportar no aplicativo e, ao mesmo tempo, impedir que as configurações específicas do aplicativo sejam exportadas até que a última instância seja fechada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(apresentado em 2,1)</p>
<p>Esse parâmetro obriga um pacote de configurações importada a ser aplicado mesmo se não houver nenhuma diferença entre o pacote e o estado atual do aplicativo. Esse parâmetro deve ser usado apenas em casos especiais, pois ele pode retardar a importação das configurações.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Elemento Name

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

Nome especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Em geral, evite fazer referência a informações de versão, pois isso pode ser objeto do elemento ProductVersion. Por exemplo, especifique `<Name>My Application</Name>` em vez de `<Name>My Application 1.1</Name>` .

**Observação**  O UE-V não faz referência a DTDs externos, portanto, não é possível usar entidades nomeadas em um modelo de local de configurações. Por exemplo, não use &reg; para se referir ao símbolo de marca comercial registrado®. Em vez disso, use referências numeradas canônicas para incluir esses tipos de caracteres especiais, por exemplo, & \ #174 para o caractere®. Esta regra se aplica a todos os valores de cadeias de caracteres neste documento.

Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obter uma lista completa de entidades de caractere. Os documentos codificados em UTF-8 podem incluir os caracteres Unicode diretamente. Salvar modelos pelo UE-V Generator converte as entidades de caracteres em representações Unicode automaticamente.

 

### <a href="" id="id21"></a>Elemento ID

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

ID preenche um identificador exclusivo para um modelo específico. Essa marca se tornará o identificador primário que o agente do UE-V usa para fazer referência ao modelo no tempo de execução (por exemplo, veja a saída dos cmdlets Get-UevTemplate e Get-UevTemplateProgram do PowerShell). Por convenção, essa marca não deve conter espaços, o que simplifica o script. Os números de versão de aplicativos devem ser especificados nesse elemento para permitir a fácil identificação do modelo, como `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Elemento Version

**Obrigatório: verdadeiro**

**Tipo: inteiro**

**Valor mínimo: 0**

**Valor máximo: 2147483647**

A versão identifica a versão do modelo de local de configurações para o controle administrativo de alterações. O UE-V Generator automaticamente incrementa esse número a cada vez que o modelo é salvo. Observe que esse campo deve ser um inteiro de número inteiro; valores fracionários, como `<Version>2.5</Version>` não são permitidos.

**Dica:** Você pode salvar anotações sobre alterações de versão usando marcas de comentário XML `<!-- -->` , por exemplo:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Importante**  Esse valor é consultado para determinar se uma nova versão de um modelo deve ser aplicada a um modelo existente nestes casos:

-   Quando a tarefa de atualização automática do modelo agendado é executada

-   Quando o cmdlet Update-UevTemplate do PowerShell é executado

-   Quando o método de atualização microsoft\\uev: SettingsLocationTemplate é chamado por meio do WMI

 

### <a href="" id="author21"></a>Elemento Author

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

O autor identifica o criador do modelo de local de configurações. Há suporte para dois elementos filho opcionais: **nome** e **email**. Os dois atributos são opcionais, mas, se o elemento filho do email for especificado, ele deve ser acompanhado pelo elemento Name. O autor se refere ao nome completo do contato do modelo de local de configurações e o email deve se referir a um endereço de email para o autor. Recomendamos que você inclua essas informações nos modelos publicados publicamente, por exemplo, na [Galeria de modelos do UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes21"></a>Elemento processos e processo

**Obrigatório: verdadeiro**

**Tipo: Element**

Os processos contêm pelo menos `<Process>` um elemento, que, por sua vez, contém os seguintes elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**. O elemento filho filename é obrigatório e os outros são opcionais. Um elemento totalmente preenchido contém marcas semelhantes a este exemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Arq

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

O nome do arquivo refere-se ao nome de arquivo real do executável exibido no sistema de arquivos. Esse elemento Especifica o critério principal que o UE-V usa para avaliar se um modelo se aplica a um processo ou não. Esse elemento deve ser especificado no modelo de local de configurações XML.

Nomes de fileválidas não devem coincidir com a expressão regular \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, ou seja, eles podem não conter caracteres de barra invertida, asterisco ou interrogação de caracteres curinga, o caractere de tubo, o sinal de maior ou menor que, barra ou dois pontos (o \ \? \* | &lt; &gt; /ou: caracteres.).

**Dica:** Para testar uma cadeia de caracteres nesse Regex, use uma janela de comando do PowerShell e substitua o nome do seu executável para **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Um valor **true** indica que a cadeia de caracteres contém caracteres ilegais. Veja alguns exemplos de valores ilegais:

-   \\\\server\\share\\program.exe

-   Programa \ *. exe

-   Pro? ram.exe

-   Programa &lt; 1 &gt; . exe

**Observação**  O gerador do UE-V codifica o maior que e menor que os caracteres como &gt; e &lt; respectivamente.

 

Em circunstâncias raras, o valor FileName não inclui necessariamente a extensão. exe, mas ele deve ser especificado como parte do valor. Por exemplo, `<Filename>MyApplictication.exe</Filename>` deve ser especificado em vez de `<Filename>MyApplictication</Filename>` . O segundo exemplo não aplicará o modelo ao processo, se o nome real do arquivo executável for "MyApplication.exe".

### Arquitetura

**Obrigatório: falso**

**Tipo: Architecture (cadeia)**

Arquitetura refere-se à arquitetura do processador para a qual o executável de destino foi compilado. Os valores válidos são Win32 para aplicativos de 32 bits ou Win64 para aplicativos de 64 bits. Se presente, essa marca limita a aplicabilidade do modelo de local de configurações a uma arquitetura de aplicativo específica. Para obter um exemplo disso, compare a experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e arquivos de MicrosoftOffice2010Win64.xml incluídos na UE-V. Isso é útil quando caminhos relativos mudam entre versões diferentes de um executável ou se as configurações foram adicionadas ou removidas ao passar de uma arquitetura de processador para outra.

Se esse elemento estiver ausente, o modelo de local de configurações ignorará a arquitetura do processo e se aplicará aos processos do 32 e do 64-bit se o nome do arquivo e outros atributos se aplicarem.

**Observação**  A UE-V não oferece suporte a processadores ARM nesta versão.

 

### ProductName

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

O NomeDoProduto é um elemento opcional usado para identificar um produto para fins administrativos ou relatórios. O NomeDoProduto é diferente do nome do arquivo, pois não há restrições de expressão regular em seu valor. Isso permite descrições mais facilmente compreendidas de um processo em que o nome do executável pode não ser óbvio. Por exemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

FileDescription é uma marca opcional que permite uma descrição administrativa do arquivo executável. Esse é um campo de texto gratuito e pode ser útil para distinguir vários executáveis dentro de um pacote de software onde há necessidade de identificar a função do executável.

Por exemplo, em um aplicativo adequado, pode ser útil fornecer lembretes sobre a função de dois executáveis (MyApplication.exe e MyApplicationHelper.exe), como mostrado aqui:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

ProductVersion refere-se às versões de produto principais e secundárias de um arquivo, bem como um nível de compilação e patch. ProductVersion é um elemento opcional, mas, se especificado, ele deve conter pelo menos o elemento filho Major. O valor deve expressar um intervalo no formato Minimum = "X" Maximum = "Y", em que X e Y são inteiros. Os valores mínimo e máximo podem ser idênticos.

Os elementos da versão do produto e do arquivo podem não ser especificados. Fazer isso torna o modelo "versão independente", o que significa que o modelo será aplicado a todas as versões do executável especificado.

**Exemplo 1:**

Versão do produto: 1,0 especificado no UE-V Generator produz o seguinte XML:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Exemplo 2:**

Versão do arquivo: 5.0.2.1000 especificado no UE-V Generator produz o seguinte XML:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Exemplo 1 incorreto – intervalo incompleto:**

Somente o atributo mínimo está presente. O máximo também deve ser incluído em um intervalo.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Exemplo 2 incorreto – especificado secundário sem elemento principal:**

Somente o elemento secundário está presente. Importante também deve ser incluído.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

FileVersion diferencia a versão de lançamento de um aplicativo publicado e os detalhes de compilação interna de um executável de componente. Para a maioria dos aplicativos comerciais, esses números são idênticos. Onde elas variam, a versão do produto de um arquivo indica uma identificação genérica de versão de um arquivo, enquanto a versão do arquivo indica uma compilação específica de um arquivo (como no caso de um hotfix ou atualização). Isso identifica arquivos com exclusividade sem interromper a lógica de detecção.

Para determinar a versão do produto e o arquivo de um determinado executável, clique com o botão direito do mouse no arquivo no Windows Explorer, selecione Propriedades e, em seguida, clique na guia detalhes.

Incluir um elemento FileVersion para um aplicativo permite uma lógica de detecção de ajuste de precisão mais granular, mas não é necessário para a maioria dos aplicativos. As configurações do elemento ProductVersion são verificadas primeiro e, em seguida, FileVersion está marcada. A configuração mais restritiva será aplicada.

Os elementos filho e as regras de sintaxe para FileVersion são idênticos aos do ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Elemento de aplicativo

Aplicativo é um contêiner para configurações que se aplicam a um aplicativo específico. Ele é uma coleção dos seguintes campos/tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versão</p></td>
<td align="left"><p>Identifica a versão do modelo de local de configurações para o controle administrativo de alterações. Para obter mais informações, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versão </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não. Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365. Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (apresentado em 2,1)</p></td>
<td align="left"><p>Especifica que este modelo só pode ser associado ao perfil especificado dentro desse elemento e não pode ser alterado via WMI ou PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processos</p></td>
<td align="left"><p>Um contêiner para uma coleção de um ou mais elementos de processo. Para obter mais informações, consulte <a href="#processes21" data-raw-source="[Processes](#processes21)"> processos </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações</p></td>
<td align="left"><p>Um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction. Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de dados </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Elemento comum

Comum é semelhante a um elemento de aplicativo, mas ele sempre é associado a dois ou mais elementos de aplicativo. A seção comum representa o conjunto de configurações compartilhadas entre essas instâncias de aplicativo. Ele é uma coleção dos seguintes campos/tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versão</p></td>
<td align="left"><p>Identifica a versão do modelo de local de configurações para o controle administrativo de alterações. Para obter mais informações, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versão </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não. Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365. Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (apresentado em 2,1)</p></td>
<td align="left"><p>Especifica que este modelo só pode ser associado ao perfil especificado dentro desse elemento e não pode ser alterado via WMI ou PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações</p></td>
<td align="left"><p>Um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction. Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de dados </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>Elemento SettingsLocationTemplate

Esse elemento define as configurações para um único aplicativo ou um pacote de aplicativos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Apêndice: SettingsLocationTemplate. xsd

Aqui está o arquivo SettingsLocationTemplate. xsd que mostra seus elementos, elementos filho, atributos e parâmetros:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## Referência de esquema de modelo de aplicativo do UE-V 2,0


Esta seção detalha a estrutura XML do modelo de local de configurações do UE-V 2,0 e fornece orientação para a edição desse arquivo.

### Nesta seção

-   [Atributo XML de declaração e codificação](#xml)

-   [Namespace e elemento raiz](#namespace)

-   [Tipos de dados](#data)

-   [Elemento Name](#name)

-   [Elemento ID](#id)

-   [Elemento Version](#version)

-   [Elemento Author](#author)

-   [Elemento processos e processo](#processes)

-   [Elemento de aplicativo](#application)

-   [Elemento comum](#common)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate)

-   [Apêndice: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>Atributo XML de declaração e codificação

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

A declaração XML deve especificar o atributo XML versão 1,0 ( &lt; ? XML Version = "1.0" &gt; ). Os modelos de local de configurações criados pelo UE-V Generator são salvos na codificação UTF-8, embora a codificação não seja especificada explicitamente. Recomendamos que você inclua o atributo encoding = "UTF-8" nesse elemento como prática recomendada. Todos os modelos incluídos com o produto também especificam essa marca (veja os documentos na experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\Templates para fins de referência). Por exemplo:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Namespace e elemento raiz

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

O UE-V usa o https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace para todos os aplicativos. SettingsLocationTemplate é o elemento raiz e contém todos os outros elementos. Referência SettingsLocationTemplate em todos os modelos usando esta marca:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Tipos de dados

Estes são os tipos de dados do esquema de modelo de aplicativo do UE-V.

<a href="" id="guid"></a>**GUID** GUID descreve uma expressão regular de identificador global exclusivo padrão no formulário "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Isso é usado no elemento Filesetting\\Root\\KnownFolder para verificar a formatação de pastas bem conhecidas.

<a href="" id="filenamestring"></a>**Filenamestring** Filenamestring refere-se ao nome de arquivo de um processo a ser monitorado. Seus valores são restritos pelo Regex \ [^ \ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, (ou seja, eles podem não conter caracteres de barra invertida, asterisco ou ponto de interrogação caracteres curinga, o caractere de pipe, o sinal de maior ou menor que, barra de encaminhamento ou caracteres de dois pontos).

<a href="" id="idstring"></a>**IDString** IDString refere-se ao valor ID dos elementos do aplicativo, SettingsLocationTemplate e dos elementos comuns (usados para descrever os pacotes de aplicativos que compartilham configurações comuns). Ele é restrito pelo mesmo Regex como filenamestring (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion é um valor inteiro usado para descrever a revisão do modelo de local de configurações. Seu valor pode variar de 0 a 2147483647.

<a href="" id="empty"></a>Em **branco** Vazio refere-se a um valor nulo. Isso é usado no Process\\ShellProcess para indicar que não há processo para monitorar. Esse valor não deve ser usado em nenhum modelo de aplicativo.

<a href="" id="author"></a>**Criar** O tipo de dados autor é um tipo complexo que identifica o autor de um modelo. Ele contém dois elementos filho: **Name** e **email**. Dentro do tipo de dados autor, o elemento Name é obrigatório enquanto o elemento de email é opcional. Esse tipo é descrito em mais detalhes sob o elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervalo** de Range define uma classe Integer que consiste em dois elementos filho: **mínimo** e **máximo**. Esse tipo de dados é implementado no tipo de dados ProcessVersion. Se especificado, os valores mínimo e máximo devem ser incluídos.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion define um tipo com quatro elementos filho: **Major**, **Minor**, **Build**e **patch**. Esse tipo de dados é usado pelo elemento processo para preencher seus valores ProductVersion e FileVersion. Os dados desse tipo são um valor de intervalo. O principal elemento filho é obrigatório e os outros são opcionais.

<a href="" id="architecture"></a>**Arquitetura** do A arquitetura enumera dois valores possíveis: **Win32** e **Win64**. Esses valores são usados para especificar a arquitetura do processo.

<a href="" id="process"></a>**Processo** O tipo de dados processo é um contêiner usado para descrever os processos a serem monitorados pela UE-V. Ele contém seis elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**. Esta tabela detalha os respectivos tipos de dados de cada elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Tipo de Dados</th>
<th align="left">Obrigatório</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Arq</p></td>
<td align="left"><p>Filenamestring</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arquitetura</p></td>
<td align="left"><p>Arquitetura</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processar** O tipo de dados Processes representa um contêiner para uma coleção de um ou mais elementos de processo. Dois elementos filho são compatíveis com o tipo de sequência Processes: **process** e **ShellProcess**. Processo é um elemento do tipo processo e ShellProcess é do tipo de dados vazio. Pelo menos um item deve ser identificado na sequência.

<a href="" id="path"></a>**Caminho** Path é consumido pela configuração RegistrySetting e filepara se referir a caminhos de arquivo e registro. Esse elemento dá suporte a dois atributos opcionais: **recursive** e **DeleteIfNotFound**. Ambos os valores são definidos como default = "false".

Recursiva indica que o caminho e todas as subpastas estão incluídos para configurações de arquivo ou que todas as chaves do registro filho estão incluídas para as configurações do registro. Em ambos os casos, todos os itens no nível atual são incluídos nos dados capturados. Para um objeto filesettings, todos os arquivos na pasta especificada são incluídos nos dados capturados pela UE-V, mas as pastas não estão incluídas. Para caminhos de registro, todos os valores no caminho atual são capturados, mas as chaves do registro filho não são capturadas. Em ambos os casos, deve-se tomar cuidado para evitar a captura de grandes conjuntos de dados ou grandes números de itens.

O atributo DeleteIfNotFound remove a configuração dos dados do caminho de armazenamento das configurações do usuário. Isso pode ser desejável em casos em que a remoção dessas configurações do pacote irá salvar uma grande quantidade de espaço em disco no servidor de arquivos do caminho de armazenamento de configurações.

<a href="" id="filemask"></a>**Máscara** de Filemask especifica apenas determinados tipos de arquivo para a pasta que é definida por path. Por exemplo, o caminho pode ser `C:\users\username\files` e filemask poderia ser `*.txt` apenas incluir arquivos de texto.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting representa um contêiner para chaves do registro e valores e o comportamento desejado associado na parte do UE-V Agent. Quatro elementos filho são definidos neste tipo: **Path**, **Name**, **Exclude**e uma sequência do **caminho** e **nome**do valor.

<a href="" id="filesetting"></a>**Configuração** do Filesetting contém parâmetros associados a arquivos e caminhos de arquivos. Quatro elementos filho são definidos: **root**, **Path**, **filemask**e **Exclude**. A raiz é obrigatória e as outras são opcionais.

<a href="" id="settings"></a>**Configurações** de Configurações é um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction descritas anteriormente. Além disso, ele também pode conter os seguintes elementos filho com comportamentos descritos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Assíncrono</p></td>
<td align="left"><p>Os pacotes de configurações assíncronas são aplicados sem bloquear a inicialização do aplicativo para que o início do aplicativo continue enquanto as configurações ainda estiverem sendo aplicadas. Isso é útil para configurações que podem ser aplicadas de forma assíncrona, como aquelas <code>get/set</code> por meio de uma API, como SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Por padrão, o UE-V salva apenas as configurações de um aplicativo quando a última instância de um aplicativo que usa o modelo é fechada. Quando esse elemento é definido como ' false ', o UE-V exporta as configurações mesmo se outras instâncias de um aplicativo estiverem em execução. Modelos adequados – aqueles que incluem uma seção de elementos comuns – que são fornecidos com o UE-V usam esse sinalizador para habilitar as configurações compartilhadas para sempre exportar no aplicativo e, ao mesmo tempo, impedir que as configurações específicas do aplicativo sejam exportadas até que a última instância seja fechada.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Elemento Name

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

Nome especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Em geral, evite fazer referência a informações de versão, pois isso pode ser objeto do elemento ProductVersion. Por exemplo, especifique `<Name>My Application</Name>` em vez de `<Name>My Application 1.1</Name>` .

**Observação**  O UE-V não faz referência a DTDs externos, portanto, não é possível usar entidades nomeadas em um modelo de local de configurações. Por exemplo, não use &reg; para se referir ao símbolo de marca comercial registrado®. Em vez disso, use referências numeradas canônicas para incluir esses tipos de caracteres especiais, por exemplo, & \ #174 para o caractere®. Esta regra se aplica a todos os valores de cadeias de caracteres neste documento.

Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obter uma lista completa de entidades de caractere. Os documentos codificados em UTF-8 podem incluir os caracteres Unicode diretamente. Salvar modelos pelo UE-V Generator converte as entidades de caracteres em representações Unicode automaticamente.

 

### <a href="" id="id"></a>Elemento ID

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

ID preenche um identificador exclusivo para um modelo específico. Essa marca se tornará o identificador primário que o agente do UE-V usa para fazer referência ao modelo no tempo de execução (por exemplo, veja a saída dos cmdlets Get-UevTemplate e Get-UevTemplateProgram do PowerShell). Por convenção, essa marca não deve conter espaços, o que simplifica o script. Os números de versão de aplicativos devem ser especificados nesse elemento para permitir a fácil identificação do modelo, como `<ID>MicrosoftCalculator6</ID>` ou `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Elemento Version

**Obrigatório: verdadeiro**

**Tipo: inteiro**

**Valor mínimo: 0**

**Valor máximo: 2147483647**

A versão identifica a versão do modelo de local de configurações para o controle administrativo de alterações. O UE-V Generator automaticamente incrementa esse número a cada vez que o modelo é salvo. Observe que esse campo deve ser um inteiro de número inteiro; valores fracionários, como `<Version>2.5</Version>` não são permitidos.

**Dica:** Você pode salvar anotações sobre alterações de versão usando marcas de comentário XML `<!-- -->` , por exemplo:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Importante**  Esse valor é consultado para determinar se uma nova versão de um modelo deve ser aplicada a um modelo existente nestes casos:

-   Quando a tarefa de atualização automática do modelo agendado é executada

-   Quando o cmdlet Update-UevTemplate do PowerShell é executado

-   Quando o método de atualização microsoft\\uev: SettingsLocationTemplate é chamado por meio do WMI

 

### <a href="" id="author"></a>Elemento Author

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

O autor identifica o criador do modelo de local de configurações. Há suporte para dois elementos filho opcionais: **nome** e **email**. Os dois atributos são opcionais, mas, se o elemento filho do email for especificado, ele deve ser acompanhado pelo elemento Name. O autor se refere ao nome completo do contato do modelo de local de configurações e o email deve se referir a um endereço de email para o autor. Recomendamos que você inclua essas informações nos modelos publicados publicamente, por exemplo, na [Galeria de modelos do UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes"></a>Elemento processos e processo

**Obrigatório: verdadeiro**

**Tipo: Element**

Os processos contêm pelo menos `<Process>` um elemento, que, por sua vez, contém os seguintes elementos filho: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **FileVersion**. O elemento filho filename é obrigatório e os outros são opcionais. Um elemento totalmente preenchido contém marcas semelhantes a este exemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Arq

**Obrigatório: verdadeiro**

**Tipo: cadeia de caracteres**

O nome do arquivo refere-se ao nome de arquivo real do executável exibido no sistema de arquivos. Esse elemento Especifica o critério principal que o UE-V usa para avaliar se um modelo se aplica a um processo ou não. Esse elemento deve ser especificado no modelo de local de configurações XML.

Nomes de fileválidas não devem coincidir com a expressão regular \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, ou seja, eles podem não conter caracteres de barra invertida, asterisco ou interrogação de caracteres curinga, o caractere de tubo, o sinal de maior ou menor que, barra ou dois pontos (o \ \? \* | &lt; &gt; /ou: caracteres.).

**Dica:** Para testar uma cadeia de caracteres nesse Regex, use uma janela de comando do PowerShell e substitua o nome do seu executável para **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Um valor **true** indica que a cadeia de caracteres contém caracteres ilegais. Veja alguns exemplos de valores ilegais:

-   \\\\server\\share\\program.exe

-   Programa \ *. exe

-   Pro? ram.exe

-   Programa &lt; 1 &gt; . exe

**Observação**  O gerador do UE-V codifica o maior que e menor que os caracteres como &gt; e &lt; respectivamente.

 

Em circunstâncias raras, o valor FileName não inclui necessariamente a extensão. exe, mas ele deve ser especificado como parte do valor. Por exemplo, `<Filename>MyApplictication.exe</Filename>` deve ser especificado em vez de `<Filename>MyApplictication</Filename>` . O segundo exemplo não aplicará o modelo ao processo, se o nome real do arquivo executável for "MyApplication.exe".

### Arquitetura

**Obrigatório: falso**

**Tipo: Architecture (cadeia)**

Arquitetura refere-se à arquitetura do processador para a qual o executável de destino foi compilado. Os valores válidos são Win32 para aplicativos de 32 bits ou Win64 para aplicativos de 64 bits. Se presente, essa marca limita a aplicabilidade do modelo de local de configurações a uma arquitetura de aplicativo específica. Para obter um exemplo disso, compare a experiência do usuário do%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e arquivos de MicrosoftOffice2010Win64.xml incluídos na UE-V. Isso é útil quando caminhos relativos mudam entre versões diferentes de um executável ou se as configurações foram adicionadas ou removidas ao passar de uma arquitetura de processador para outra.

Se esse elemento estiver ausente, o modelo de local de configurações ignorará a arquitetura do processo e se aplicará aos processos do 32 e do 64-bit se o nome do arquivo e outros atributos se aplicarem.

**Observação**  A UE-V não oferece suporte a processadores ARM nesta versão.

 

### ProductName

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

O NomeDoProduto é um elemento opcional usado para identificar um produto para fins administrativos ou relatórios. O NomeDoProduto é diferente do nome do arquivo, pois não há restrições de expressão regular em seu valor. Isso permite descrições mais facilmente compreendidas de um processo em que o nome do executável pode não ser óbvio. Por exemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

FileDescription é uma marca opcional que permite uma descrição administrativa do arquivo executável. Esse é um campo de texto gratuito e pode ser útil para distinguir vários executáveis dentro de um pacote de software onde há necessidade de identificar a função do executável.

Por exemplo, em um aplicativo adequado, pode ser útil fornecer lembretes sobre a função de dois executáveis (MyApplication.exe e MyApplicationHelper.exe), como mostrado aqui:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

ProductVersion refere-se às versões de produto principais e secundárias de um arquivo, bem como um nível de compilação e patch. ProductVersion é um elemento opcional, mas, se especificado, ele deve conter pelo menos o elemento filho Major. O valor deve expressar um intervalo no formato Minimum = "X" Maximum = "Y", em que X e Y são inteiros. Os valores mínimo e máximo podem ser idênticos.

Os elementos da versão do produto e do arquivo podem não ser especificados. Fazer isso torna o modelo "versão independente", o que significa que o modelo será aplicado a todas as versões do executável especificado.

**Exemplo 1:**

Versão do produto: 1,0 especificado no UE-V Generator produz o seguinte XML:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Exemplo 2:**

Versão do arquivo: 5.0.2.1000 especificado no UE-V Generator produz o seguinte XML:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Exemplo 1 incorreto – intervalo incompleto:**

Somente o atributo mínimo está presente. O máximo também deve ser incluído em um intervalo.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Exemplo 2 incorreto – especificado secundário sem elemento principal:**

Somente o elemento secundário está presente. Importante também deve ser incluído.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obrigatório: falso**

**Tipo: cadeia de caracteres**

FileVersion diferencia a versão de lançamento de um aplicativo publicado e os detalhes de compilação interna de um executável de componente. Para a maioria dos aplicativos comerciais, esses números são idênticos. Onde elas variam, a versão do produto de um arquivo indica uma identificação genérica de versão de um arquivo, enquanto a versão do arquivo indica uma compilação específica de um arquivo (como no caso de um hotfix ou atualização). Isso identifica arquivos com exclusividade sem interromper a lógica de detecção.

Para determinar a versão do produto e o arquivo de um determinado executável, clique com o botão direito do mouse no arquivo no Windows Explorer, selecione Propriedades e, em seguida, clique na guia detalhes.

Incluir um elemento FileVersion para um aplicativo permite uma lógica de detecção de ajuste de precisão mais granular, mas não é necessário para a maioria dos aplicativos. As configurações do elemento ProductVersion são verificadas primeiro e, em seguida, FileVersion está marcada. A configuração mais restritiva será aplicada.

Os elementos filho e as regras de sintaxe para FileVersion são idênticos aos do ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Elemento de aplicativo

Aplicativo é um contêiner para configurações que se aplicam a um aplicativo específico. Ele é uma coleção dos seguintes campos/tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão</p></td>
<td align="left"><p>Identifica a versão do modelo de local de configurações para o controle administrativo de alterações. Para obter mais informações, consulte <a href="#version" data-raw-source="[Version](#version)"> versão </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não. Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365. Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processos</p></td>
<td align="left"><p>Um contêiner para uma coleção de um ou mais elementos de processo. Para obter mais informações, consulte <a href="#processes" data-raw-source="[Processes](#processes)"> processos </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações</p></td>
<td align="left"><p>Um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction. Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data" data-raw-source="[Data types](#data)"> tipos de dados </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Elemento comum

Comum é semelhante a um elemento de aplicativo, mas ele sempre é associado a dois ou mais elementos de aplicativo. A seção comum representa o conjunto de configurações compartilhadas entre essas instâncias de aplicativo. Ele é uma coleção dos seguintes campos/tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão</p></td>
<td align="left"><p>Identifica a versão do modelo de local de configurações para o controle administrativo de alterações. Para obter mais informações, consulte <a href="#version" data-raw-source="[Version](#version)"> versão </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla se este modelo está habilitado em conjunto com uma conta da Microsoft ou não. Se a sincronização do MSA estiver habilitada para um usuário em um computador, esse modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Semelhante ao MSA, isso controla se esse modelo está habilitado em conjunto com o office365. Se o Office 365 estiver sendo usado para sincronizar as configurações, este modelo será automaticamente desabilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações</p></td>
<td align="left"><p>Um contêiner para todas as configurações que se aplicam a um modelo específico. Ele contém instâncias das configurações de registro, arquivo, SystemParameter e CustomAction. Para obter mais informações, consulte <strong> configurações </strong> em <a href="#data" data-raw-source="[Data types](#data)"> tipos de dados </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>Elemento SettingsLocationTemplate

Esse elemento define as configurações para um único aplicativo ou um pacote de aplicativos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica um nome exclusivo para o modelo de local de configurações. Isso é usado para fins de exibição ao fazer referência ao modelo em WMI, PowerShell, visualizador de eventos e logs de depuração. Para obter mais informações, consulte <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Preenche um identificador exclusivo para um modelo específico. Essa marca se torna o identificador primário que o UE-V Agent usa para fazer referência ao modelo em tempo de execução. Para obter mais informações, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição opcional do modelo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Localizadores</p></td>
<td align="left"><p>Um nome opcional exibido na interface do usuário, localizado por uma localidade de idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Uma descrição de modelo opcional localizada por uma localidade de idioma.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Apêndice: SettingsLocationTemplate. xsd

Aqui está o arquivo SettingsLocationTemplate. xsd que mostra seus elementos, elementos filho, atributos e parâmetros:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Tópicos relacionados


[Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





