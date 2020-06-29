---
title: Implantando o Microsoft Office 2016 usando o App-V
description: Implantando o Microsoft Office 2016 usando o App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796545"
---
# Implantando o Microsoft Office 2016 usando o App-V


Use as informações neste artigo para usar o Microsoft Application Virtualization 5,0 ou versões posteriores para fornecer o Microsoft Office 2016 como um aplicativo virtualizado para computadores em sua organização. Para obter informações sobre como usar o App-V para fornecer o Office 2013, consulte [implantando o Microsoft Office 2013 usando o app-v](deploying-microsoft-office-2013-by-using-app-v.md). Para obter informações sobre como usar o App-V para fornecer o Office 2010, consulte [implantando o Microsoft Office 2010 usando o app-v](deploying-microsoft-office-2010-by-using-app-v.md).

Este tópico contém as seguintes seções:

-   [O que saber antes de começar](#bkmk-before-you-start)

-   [Criando um pacote do Office 2016 para o App-V com a ferramenta de implantação do Office](#bkmk-create-office-pkg)

-   [Publicando o pacote do Office para o App-V 5,0](#bkmk-pub-pkg-office)

-   [Personalizando e gerenciando pacotes do Office App-V](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>O que saber antes de começar


Antes de implantar o Office 2016 usando o App-V, examine as informações de planejamento a seguir.

### <a href="" id="bkmk-supp-vers-coexist"></a>Versões do Office com suporte e coexistência do Office

Use a tabela a seguir para obter informações sobre as versões compatíveis do Office e sobre como executar versões coexistentes do Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informações a serem revisadas</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">Versões com suporte do Microsoft Office</a></p></td>
<td align="left"><ul>
<li><p>Versões com suporte do Office</p></li>
<li><p>Tipos de implantação com suporte (por exemplo, área de trabalho, infraestrutura de área de trabalho virtual pessoal (VDI), VDI em pool)</p></li>
<li><p>Opções de licenciamento do Office</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">Planejando o uso do App-V com versões coexistentes do Office</a></p></td>
<td align="left"><p>Considerações para a instalação de diferentes versões do Office no mesmo computador</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>Requisitos de empacotamento, publicação e implantação

Antes de implantar o Office usando o App-V, examine os seguintes requisitos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Embalagem</p></td>
<td align="left">
<ul>
<li><p>Todos os aplicativos do Office que você deseja implantar para os usuários devem estar em um único pacote.</p></li>
<li><p>No App-V 5,0 e posterior, você deve usar a ferramenta de implantação do Office para criar pacotes. Não é possível usar o sequenciador.</p></li>
<li><p>Se você estiver implantando o Microsoft Visio 2016 e o Microsoft Project 2016 juntamente com o Office, deverá incluí-los no mesmo pacote com o Office. Para obter mais informações, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> implantação do Visio 2016 e do Project 2016 com o Office </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Publicação</p></td>
<td align="left"><ul>
<li><p>Você pode publicar apenas um pacote do Office em cada computador cliente.</p></li>
<li><p>Você deve publicar o pacote do Office globalmente. Você não pode publicar para o usuário.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Implantando qualquer um dos seguintes produtos em um computador compartilhado, por exemplo, usando serviços de área de trabalho remota:</p>
<ul>
<li><p>Aplicativos do Microsoft 365 para empresas</p></li>
<li><p>Visio pro para Office 365</p></li>
<li><p>Project pro para Office 365</p></li>
</ul></td>
<td align="left"><p>Você deve habilitar a <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> ativação de computador compartilhado </a> .</p>
</td>
</tr>
</tbody>
</table>



### Excluindo aplicativos do Office de um pacote

A tabela a seguir descreve os métodos recomendados para excluir aplicativos específicos do Office de um pacote.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Use a <strong> </strong> configuração ExcludeApp quando você cria o pacote usando a ferramenta de implantação do Office.</p></td>
<td align="left"><ul>
<li><p>Permite que você exclua aplicativos específicos do Office do pacote quando a ferramenta de implantação do Office cria o pacote. Por exemplo, você pode usar essa configuração para criar um pacote que contenha apenas o Microsoft Word.</p></li>
<li><p>Para obter mais informações, consulte o <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Modificar o arquivo DeploymentConfig.xml</p></td>
<td align="left"><ul>
<li><p>Modifique o arquivo DeploymentConfig.xml após a criação do pacote. Esse arquivo contém as configurações padrão do pacote para todos os usuários em um computador que esteja executando o cliente App-V.</p></li>
<li><p>Para obter mais informações, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> desabilitando aplicativos do Office 2016 </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Criando um pacote do Office 2016 para o App-V com a ferramenta de implantação do Office


Conclua as etapas a seguir para criar um pacote do Office 2016 para o App-V 5,0 ou posterior.

>**Important** &nbsp; Importante &nbsp; No App-V 5,0 e posterior, você deve usar a ferramenta de implantação do Office para criar um pacote. Você não pode usar o sequenciador para criar pacotes.

### Revisar os pré-requisitos para usar a ferramenta de implantação do Office

O computador no qual você está instalando a ferramenta de implantação do Office deve ter:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Software de pré-requisito</p></td>
<td align="left"><p>.NET Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistemas operacionais compatíveis</p></td>
<td align="left"><ul>
<li><p>versão de 64 bits do Windows 10</p></li>
<li><p>versão de 64 bits do Windows 8 ou 8,1</p></li>
<li><p>versão de 64 bits do Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


>**Observação**  Neste tópico, o termo "Office 2016 App-V Package" refere-se ao licenciamento de assinatura.


### Criar pacotes do Office 2016 App-V usando a ferramenta de implantação do Office

Você cria pacotes do Office 2016 App-V usando a ferramenta de implantação do Office. As instruções a seguir explicam como criar um pacote do Office 2016 App-V com licenciamento de assinatura.

Crie pacotes do Office 2016 App-V em computadores com Windows de 64 bits. Uma vez criado, o pacote do Office 2016 App-V será executado em computadores com o Windows 7, o Windows 8,1 e o Windows 10 com 32 bits e 64 bits.

### Baixar a ferramenta de implantação do Office

Os pacotes do Office 2016 App-V são criados usando a ferramenta de implantação do Office, que gera um pacote do Office 2016 App-V. O pacote não pode ser criado ou modificado por meio do sequenciador App-V. Para começar a criação de pacotes:

1.  Baixe a [ferramenta de implantação do Office 2016 para clique para executar](https://www.microsoft.com/download/details.aspx?id=49117).

> **Importante** Você deve usar a ferramenta de implantação do Office 2016 para criar pacotes do Office 2016 App-V.
> 2. Execute o arquivo. exe e extraia seus recursos para o local desejado. Para facilitar esse processo, você pode criar uma pasta de rede compartilhada na qual os recursos serão salvos.

    Example: \\\\Server\\Office2016

3. Verifique se há um setup.exe e um arquivo configuration.xml e se estão no local especificado.

### Baixar aplicativos do Office 2016

Depois de baixar a ferramenta de implantação do Office, você pode usá-la para obter os aplicativos mais recentes do Office 2016. Depois de obter os aplicativos do Office, crie o pacote do Office 2016 App-V.

O arquivo XML que está incluído na ferramenta de implantação do Office especifica os detalhes do produto, como os idiomas e os aplicativos do Office incluídos.

1. **Personalize o arquivo de configuração XML de exemplo:** Use o arquivo de configuração XML de exemplo que você baixou com a ferramenta de implantação do Office para personalizar os aplicativos do Office:

   1. Abra o arquivo XML de exemplo no bloco de notas ou no seu editor de texto favorito.

   2. Com o exemplo configuration.xml arquivo aberto e pronto para edição, você pode especificar produtos, idiomas e o caminho para o qual você salva os aplicativos do Office 2016. Veja a seguir um exemplo básico do arquivo configuration.xml:

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      >**Observação**  O XML de configuração é um arquivo XML de exemplo. O arquivo inclui linhas que foram comentadas. Você pode "remover o comentário" dessas linhas para personalizar as configurações adicionais com o arquivo. Para "remover o comentário" dessas linhas, remova a "<! --"do início da linha e"--> "do final da linha.

      O arquivo de configuração XML acima Especifica que o Office 2016 ProPlus 32-bit Edition, incluindo o Visio ProPlus, será baixado em inglês para o \\\\server\\Office 2016, que é o local onde os aplicativos do Office serão salvos. Observe que a ID do produto dos aplicativos não afetará o licenciamento final do Office. Os pacotes do Office 2016 App-V com várias licenças podem ser criados a partir dos mesmos aplicativos por meio da especificação de licenciamento em um estágio posterior. A tabela a seguir resume os atributos e elementos personalizáveis do arquivo XML:

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">Entrada</th>
      <th align="left">Descrição</th>
      <th align="left">Exemplo</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>Adicionar elemento</p></td>
      <td align="left"><p>Especifica os produtos e idiomas a serem incluídos no pacote.</p></td>
      <td align="left"><p>N/A</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (atributo do elemento add)</p></td>
      <td align="left"><p>Especifica a edição do produto do Office 2016 a ser usado: 32 bits ou 64 bits. A operação falhará se <strong> OfficeClientEdition </strong> não estiver definido como um valor válido.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Elemento Product</p></td>
      <td align="left"><p>Especifica o aplicativo. O Project 2016 e o Visio 2016 devem ser especificados aqui como um produto adicionado a ser incluído nos aplicativos.

      Para obter mais informações sobre os IDs de produto, consulte <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> IDs de produto que são suportados pela ferramenta de implantação do Office para clique para executar</a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p>Elemento de linguagem</p></td>
      <td align="left"><p>Especifica o idioma com suporte nos aplicativos</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Versão (atributo do elemento add)</p></td>
      <td align="left"><p>Opcional. Especifica uma compilação a ser usada para o pacote</p>
      <p>O padrão é a compilação anunciada mais recente (conforme definido no v32.CAB na origem do Office).</p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Caminho_de_origem (atributo do elemento add)</p></td>
      <td align="left"><p>Especifica o local em que os aplicativos serão salvos.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Canal (atributo do elemento add)</p></td>
      <td align="left"><p>Opcional. Especifica o canal de atualização do produto que você deseja baixar ou instalar. </p><p>Para obter mais informações sobre os canais de atualização, consulte Visão geral de canais de atualização para aplicativos do Microsoft 365 para empresas.</p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      Depois de editar o arquivo configuration.xml para especificar o produto desejado, os idiomas e também o local em que os aplicativos do Office 2016 serão salvos, você poderá salvar o arquivo de configuração, por exemplo, como Customconfig.xml.

2. **Baixe os aplicativos para o local especificado:** Use um prompt de comando elevado e um sistema operacional de 64 bits para baixar os aplicativos do Office 2016 que serão convertidos posteriormente em um pacote do App-V. Veja a seguir um exemplo de comando com uma descrição de detalhes:

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   No exemplo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>é a ferramenta de implantação do Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/Download</strong></p></td>
   <td align="left"><p>baixa os aplicativos do Office 2016 que você especificar no arquivo customConfig.xml. Esses bits podem ser convertidos posteriormente em um pacote do Office 2016 App-V com licenciamento por volume.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>passa o arquivo de configuração XML necessário para concluir o processo de download, neste exemplo, customconfig.xml. Depois de usar o comando download, os aplicativos do Office devem ser encontrados no local especificado no arquivo XML de configuração, neste exemplo \Server\Office2016.</p></td>
   </tr>
   </tbody>
   </table>



### Converter os aplicativos do Office em um pacote do App-V

Depois de baixar os aplicativos do Office 2016 por meio da ferramenta de implantação do Office, use a ferramenta de implantação do Office para convertê-los em um pacote do Office 2016 App-V. Conclua as etapas que correspondem ao seu modelo de licenciamento.

**Resumo do que você precisará fazer:**

-   Crie os pacotes do Office 2016 App-V em computadores com Windows de 64 bits. No entanto, o pacote será executado em computadores de 32 bits 64 e no Windows 7, no Windows 8 ou 8,1 e no Windows 10.

-   Crie um pacote do Office App-V para pacote de licenciamento de assinatura usando a ferramenta de implantação do Office e modifique o arquivo de configuração do CustomConfig.xml.

    A tabela a seguir resume os valores que você precisa inserir no arquivo CustomConfig.xml para o modelo de licenciamento que você está usando. As etapas nas seções que seguem a tabela especificarão as entradas exatas que você precisa fazer.

>**Note** &nbsp; Observação &nbsp; Você pode usar a ferramenta de implantação do Office para criar pacotes do App-V para aplicativos do Microsoft 365 para empresas. Não há suporte para a criação de pacotes para versões de licença de volume do Office Professional Plus ou do Office Standard.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID do Produto (Product ID)</th>
<th align="left">Licenciamento de assinatura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2016 com Visio 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2016 com Visio 2016 e Project 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Como converter os aplicativos do Office em um pacote do App-V**

1. No bloco de notas, abra novamente o arquivo CustomConfig.xml e faça as seguintes alterações no arquivo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parâmetro</th>
   <th align="left">O que alterar o valor para</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>SourcePath</p></td>
   <td align="left"><p>Aponte para os aplicativos do Office baixados anteriormente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>Especifique o licenciamento de assinatura, conforme mostrado no exemplo a seguir:</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento de assinatura:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SourcePath</strong></p></td>
   <td align="left"><p>é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>ID do Produto (Product ID)</strong></p></td>
   <td align="left"><p>para o Office foi alterado para <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>ID do Produto (Product ID)</strong></p></td>
   <td align="left"><p>para o Visio foi alterado para <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (opcional)</p></td>
   <td align="left"><p>Permite especificar os programas do Office que você não deseja incluir no pacote do App-V que a ferramenta de implantação do Office cria. Por exemplo, você pode excluir o Access e o InfoPath.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (opcional)</p></td>
   <td align="left"><p>Por padrão, todos os pacotes do App-V criados pela ferramenta de implantação do Office compartilham a mesma ID de pacote do App-V. Você pode usar PACKAGEGUID para especificar uma ID de pacote diferente para cada pacote, que permite publicar vários pacotes do App-V, criados pela ferramenta de implantação do Office e gerenciá-los usando o servidor App-V.</p>
   <p>Um exemplo de quando usar esse parâmetro é se você cria pacotes diferentes para usuários diferentes. Por exemplo, você pode criar um pacote com apenas o Office 2016 para alguns usuários e criar outro pacote com o Office 2016 e o Visio 2016 para outro conjunto de usuários.</p>
&gt;<strong>Observação </strong> mesmo que você use IDs de pacote exclusivas, ainda é possível implantar apenas um pacote do App-V para um único dispositivo.
   </td>
   </tr>
   </tbody>
   </table>



2. Use o comando/Packager para converter os aplicativos do Office em um pacote do Office 2016 App-V.

   Por exemplo:

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   No exemplo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>é a ferramenta de implantação do Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>cria o pacote App-V do Office 2016 com o tipo de licenciamento especificado no arquivo customConfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>passa o arquivo XML de configuração (neste caso, customConfig) que foi preparado para o estágio de empacotamento.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2016AppV</strong></p></td>
   <td align="left"><p>Especifica o local do pacote do Office App-V recém-criado.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Verifique se o pacote do Office 2016 App-V funciona corretamente:

   1.  Publique o pacote do Office 2016 App-V, que você criou globalmente, em um computador de teste e verifique se os atalhos do Office 2016 são exibidos.

   2.  Inicie alguns aplicativos do Office 2016, como o Excel ou o Word, para garantir que o pacote esteja funcionando conforme o esperado.

## <a href="" id="bkmk-pub-pkg-office"></a>Publicando o pacote do Office para App-V


Use as informações a seguir para publicar um pacote do Office.

### Métodos para publicar pacotes do Office App-V

Implante o pacote do App-V para o Office 2016 usando os mesmos métodos que você usa para qualquer outro pacote:

-   System Center Configuration Manager

-   Servidor do App-V

-   Autônomos por meio de comandos do PowerShell

### Como publicar pré-requisitos e requisitos

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito ou requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitar o script do PowerShell nos clientes do App-V</p></td>
<td align="left"><p>Para publicar pacotes do Office 2016, você deve executar um script.</p>
<p>Os scripts de pacote são desativados por padrão em clientes App-V. Para habilitar o script, execute o seguinte comando do PowerShell:</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar o pacote do Office 2016 globalmente</p></td>
<td align="left"><p>Os pontos de extensão no pacote App-V do Office exigem instalação no nível do computador.</p>
<p>Quando você publica no nível do computador, não são necessárias ações de pré-requisito ou redistribuíveis, e o pacote do Office 2016 permite que seus aplicativos funcionem como o Office instalado nativamente, eliminando a necessidade de os administradores personalizarem pacotes.</p></td>
</tr>
</tbody>
</table>



### Como publicar um pacote do Office

Execute o seguinte comando para publicar um pacote do Office globalmente:

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   No console de gerenciamento da Web no App-V Server, você pode adicionar permissões a um grupo de computadores em vez de a um grupo de usuários para permitir que os pacotes sejam publicados globalmente nos computadores do grupo correspondente.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Personalizando e gerenciando pacotes do Office App-V


Para gerenciar seus pacotes do Office App-V, use as mesmas operações que faria para qualquer outro pacote, mas há algumas exceções, como descrito nas seções a seguir.

-   [Habilitando plug-ins do Office usando grupos de conexão](#bkmk-enable-office-plugins)

-   [Desativando aplicativos do Office 2016](#bkmk-disable-office-apps)

-   [Desativando atalhos do Office 2016](#bkmk-disable-shortcuts)

-   [Gerenciando atualizações de pacote do Office 2016](#bkmk-manage-office-pkg-upgrd)

-   [Implantação do Visio 2016 e do Project 2016 com o Office](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>Habilitando plug-ins do Office usando grupos de conexão

Use as etapas desta seção para habilitar os plug-ins do Office com o pacote do Office. Para usar os plug-ins do Office, você deve usar o sequenciador do App-V para criar um pacote separado que contenha apenas os plug-ins. Não é possível usar a ferramenta de implantação do Office para criar o pacote de plug-ins. Em seguida, crie um grupo de conexão que contenha o pacote de plug-ins e o pacote do Office, conforme descrito nas etapas a seguir.

**Para habilitar plug-ins para pacotes do Office App-V**

1.  Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.

2.  Sequenciar seus plug-ins usando o sequenciador do App-V. Verifique se o Office 2016 está instalado no computador que está sendo usado para sequenciar o plug-in. É recomendável usar os aplicativos do Microsoft 365 para empresas (não virtuais) no computador de sequenciamento quando você sequenciar plug-ins do Office 2016.

3.  Crie um pacote do App-V que inclua os plug-ins desejados.

4.  Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.

5.  Adicione o pacote do Office 2016 App-V e o pacote de plug-ins que você sequenciaou ao grupo de conexão que você criou.

    >**Importante** A ordem dos pacotes no grupo de conexão determina a ordem em que o conteúdo do pacote é mesclado. No arquivo do descritor de grupo de conexão, adicione o pacote do Office 2016 App-V primeiro e, em seguida, adicione o pacote do plug-in App-V.



6.  Certifique-se de que os dois pacotes sejam publicados no computador de destino e que o pacote de plug-in seja publicado globalmente para corresponder às configurações globais do pacote do Office 2016 App-V publicado.

7.  Verifique se o arquivo de configuração de implantação do pacote de plug-in tem as mesmas configurações que o pacote do Office 2016 App-V tem.

    Como o pacote do Office 2016 App-V está integrado ao sistema operacional, as configurações do pacote de plug-in devem coincidir. Você pode pesquisar o arquivo de configuração de implantação para "modo COM" e garantir que o pacote de plug-ins tenha esse valor definido como "integrado" e que "InProcessEnabled" e "OutOfProcessEnabled" correspondam às configurações do pacote do Office 2016 App-V que você publicou.

8.  Abra o arquivo de configuração de implantação e defina o valor de **objetos habilitados** como **falso**.

9.  Se você fez qualquer alteração no arquivo de configuração de implantação após o sequenciamento, verifique se o pacote de plug-in é publicado com o arquivo.

10. Verifique se o grupo de conexão que você criou está habilitado no computador desejado. O grupo de conexão criado provavelmente será "pendente" se o pacote do Office 2016 App-V estiver em uso quando o grupo de conexão estiver habilitado. Se isso acontecer, será necessário reinicializar para habilitar o grupo de conexão com êxito.

11. Depois de publicar com êxito os dois pacotes e habilitar o grupo de conexão, inicie o aplicativo de destino do Office 2016 e verifique se o plug-in que você publicou e adicionado ao grupo de conexão funciona como esperado.

### <a href="" id="bkmk-disable-office-apps"></a>Desativando aplicativos do Office 2016

Você pode querer desabilitar aplicativos específicos em seu pacote do Office App-V. Por exemplo, você pode desabilitar o Access, mas deixar todos os outros aplicativos principais do Office disponíveis. Quando você desabilitar um aplicativo, o usuário final não verá mais o atalho para esse aplicativo. Não é necessário sequenciar novamente o aplicativo. Quando você altera o arquivo de configuração de implantação após a publicação do pacote do Office 2016 App-V, você salvará as alterações, adicionará o pacote do Office 2016 app-v e a publicará novamente com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do Office 2016 App-V.

>**Observação** Para excluir aplicativos específicos do Office (por exemplo, o Access e o InfoPath) quando você cria o pacote do App-V com a ferramenta de implantação do Office, use a configuração **ExcludeApp** .


**Para desabilitar um aplicativo do Office 2016**

1.  Abra um arquivo de configuração de implantação com um editor de texto, como o **bloco de notas** , e procure por "aplicativos".

2.  Procure o aplicativo do Office que você deseja desabilitar, por exemplo, Access 2016.

3.  Altere o valor de "Enabled" de "true" para "false".

4.  Salve o arquivo de configuração de implantação.

5.  Adicione o pacote do Office 2016 App-V com o novo arquivo de configuração de implantação.

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Adicione novamente o pacote do Office 2016 App-V e Republique-o com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do App-V do Office 2016.

### <a href="" id="bkmk-disable-shortcuts"></a>Desativando atalhos do Office 2016

Você pode querer desativar atalhos para determinados aplicativos do Office em vez de cancelar a publicação ou remoção do pacote. O exemplo a seguir mostra como desabilitar atalhos para o Microsoft Access.

**Para desativar atalhos para aplicativos do Office 2016**

1.  Abra um arquivo de configuração de implantação no bloco de notas e procure por "atalhos".

2.  Para desabilitar certos atalhos, exclua ou comente os atalhos específicos que você não quer. Você deve manter o subsistema presente e habilitado. Por exemplo, no exemplo a seguir, exclua os atalhos do Microsoft Access, enquanto mantém os subsistemas de &lt; atalho &gt; &lt; /Shortcut &gt; intactos para desabilitar o atalho do Microsoft Access.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  Salve o arquivo de configuração de implantação.

4.  Republicar o pacote do Office 2016 App-V com novo arquivo de configuração de implantação.

Muitas configurações adicionais podem ser alteradas por meio da modificação da configuração de implantação para pacotes do App-V, por exemplo, associações de tipo de arquivo, sistema de arquivos virtual e muito mais. Para obter informações adicionais sobre como usar arquivos de configuração de implantação para alterar as configurações do pacote do App-V, consulte a seção recursos adicionais no final deste documento.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Gerenciando atualizações de pacote do Office 2016

Para atualizar um pacote do Office 2016, use a ferramenta de implantação do Office. Para atualizar um pacote do Office 2016 implantado anteriormente, siga as etapas a seguir.

**Como atualizar um pacote do Office 2016 implantado anteriormente**

1. Crie um novo pacote do Office 2016 por meio da ferramenta de implantação do Office que usa o software aplicativo mais recente do Office 2016. Os bits mais recentes do Office 2016 sempre podem ser obtidos por meio do estágio de download da criação de um pacote do Office 2016 App-V. O pacote do Office 2016 recém-criado terá as atualizações mais recentes e uma nova ID de versão. Todos os pacotes criados usando a ferramenta de implantação do Office têm a mesma linhagem.

   > **Observação** Os pacotes do Office App-V têm duas IDs de versão:
   > <ul>
   > <li>Uma ID de versão do pacote do Office 2016 App-V que é exclusiva em todos os pacotes criados usando a ferramenta de implantação do Office.</li>
   > <li>Uma segunda ID de versão do pacote do App-V, x. x. x. x por exemplo, no manifesto AppX que só será alterado se houver uma nova versão do Office. Por exemplo, se uma nova versão do Office 2016 com atualizações estiver disponível e um pacote for criado por meio da ferramenta de implantação do Office para incorporar essas atualizações, a ID da versão X. x. x. X será alterada para refletir que a própria versão do Office mudou. O servidor App-V usará a ID da versão x. x. x para diferenciar esse pacote e reconhecer que ele contém novas atualizações para o pacote publicado anteriormente e, como resultado, publicá-lo como uma atualização para o pacote existente do Office 2016.</li>
   > </ul>


2. Publique globalmente os pacotes do Office 2016 App-V recém-criados em computadores onde você deseja aplicar as novas atualizações. Como o novo pacote tem a mesma linhagem do pacote mais antigo do Office 2016 App-V, publicar o novo pacote com as atualizações só aplicará as novas alterações ao pacote antigo e, portanto, será rápido.

3. As atualizações serão aplicadas da mesma maneira em qualquer pacote App-V publicado globalmente. Como os aplicativos provavelmente estarão em uso, as atualizações podem ser adiadas até que o computador seja reiniciado.


### <a href="" id="bkmk-deploy-visio-project"></a>Implantação do Visio 2016 e do Project 2016 com o Office

A tabela a seguir descreve os requisitos e as opções para a implantação do Visio 2016 e do Project 2016 com o Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Como faço para empacotar e publicar o Visio 2016 e o Project 2016 com o Office?</p></td>
<td align="left"><p>Você deve incluir o Visio 2016 e o Project 2016 no mesmo pacote com o Office.</p>
<p>Se você não estiver implantando o Office, poderá criar um pacote que contenha o Visio e/ou o Project, desde que siga os requisitos de empacotamento, publicação e implantação descritos neste tópico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Como eu posso implantar o Visio 2016 e o Project 2016 para usuários específicos?</p></td>
<td align="left"><p>Use um dos seguintes métodos:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Se quiser...</th>
<th align="left">... em seguida, use esse método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crie dois pacotes diferentes e implante cada um deles em um grupo diferente de usuários</p></td>
<td align="left"><p>Crie e implante os seguintes pacotes:</p>
<ul>
<li><p>Um pacote que contém apenas o Office-implantação em computadores cujos usuários precisam apenas do Office.</p></li>
<li><p>Um pacote que contém o Office, o Visio e o Project-implantação para computadores cujos usuários precisam de todos os três aplicativos.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Se você quiser apenas um pacote para a organização inteira, ou se tiver usuários que compartilham computadores:</p></td>
<td align="left"><p>Siga estas etapas:</p>
<ol>
<li><p>Crie um pacote que contenha o Office, o Visio e o Project.</p></li>
<li><p>Implante o pacote para todos os usuários.</p></li>
<li><p>Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> o Microsoft AppLocker </a> para impedir que usuários específicos usem o Visio e o Project.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## Recursos adicionais


[Implantando o Microsoft Office 2013 usando o App-V](deploying-microsoft-office-2013-by-using-app-v.md)

[Implantando o Microsoft Office 2010 usando o App-V](deploying-microsoft-office-2010-by-using-app-v.md)

[Ferramenta de implantação do Office 2016 para clique para executar](https://www.microsoft.com/download/details.aspx?id=49117)

**Grupos de conexão**

[Implantando grupos de conexão no Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Gerenciando grupos de conexão](managing-connection-groups.md)

**Configuração dinâmica**

[Sobre a configuração dinâmica do App-V 5.1](about-app-v-51-dynamic-configuration.md)





