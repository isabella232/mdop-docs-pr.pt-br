---
title: Migrando para o App-V 5.1 de uma versão anterior
description: Migrando para o App-V 5.1 de uma versão anterior
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796278"
---
# Migrando para o App-V 5.1 de uma versão anterior


Com o Microsoft Application Virtualization (App-V) 5,1, você pode migrar sua infraestrutura existente do App-V 4,6 ou App-V 5,0 para a infraestrutura mais flexível, integrada e mais fácil de gerenciar do App-V 5,1.
No entanto, não é possível migrar diretamente do App-V 4. x para o App-V 5,1, você deve migrar para o App-V 5,0 primeiro. Para obter mais informações sobre como migrar do App-V 4. x para o App-V 5,0, confira [migrar de uma versão anterior](migrating-from-a-previous-version-app-v-50.md)  

**Observação**  Os pacotes do App-V 5,1 são exatamente iguais aos pacotes do App-V 5,0. Não houve nenhuma alteração no formato do pacote entre as versões e, portanto, não há necessidade de converter pacotes do App-V 5,0 para pacotes do App-V 5,1.

Para obter mais informações sobre as diferenças entre o App-V 4,6 e o App-V 5,1, consulte a **seção diferenças entre o app-v 4,6 e o app-v 5,0** de [sobre o app-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Melhorias no conversor de pacotes do App-V 5,1


Agora você pode usar o conversor de pacote para converter pacotes do App-V 4,6 que contêm scripts e informações do registro e scripts dos arquivos Source. OSD agora estão incluídos na saída do conversor de pacote.

Você também pode usar o `–OSDsToIncludeInPackage` parâmetro com o `ConvertFrom-AppvLegacyPackage` cmdlet para especificar quais informações de arquivos. OSD são convertidas e colocadas dentro do novo pacote.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Novo no App-V 5,1</th>
<th align="left">Antes do App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Os novos arquivos. XML são criados correspondentes aos arquivos. OSD associados a um pacote; esses arquivos incluem as seguintes informações:</p>
<ul>
<li><p>variáveis de ambiente</p></li>
<li><p>teclado</p></li>
<li><p>associações de tipo de arquivo</p></li>
<li><p>informações do registro</p></li>
<li><p>escritas</p></li>
</ul>
<p>Agora você pode optar por adicionar informações de um subconjunto de arquivos. OSD no diretório de origem ao pacote usando o <code>-OSDsToIncludeInPackage</code> parâmetro.</p></td>
<td align="left"><p>As informações do registro e os scripts incluídos nos arquivos. OSD associados a um pacote não foram incluídos na saída do conversor de pacote.</p>
<p>O conversor de pacote preencheria o novo pacote com informações de todos os arquivos. OSD no diretório de origem.</p></td>
</tr>
</tbody>
</table>

 

### Exemplo de instrução de conversão

Para entender o novo processo, examine a seguinte instrução do conversor de pacote de exemplo `ConvertFrom-AppvLegacyPackage` .

**Se o diretório de origem (\\\\OldPkgStore\\ContosoApp) incluir o seguinte:**

-   ContosoApp. SFT

-   ContosoApp.msi

-   ContosoApp.sprj

-   ContosoApp\_manifest.xml

-   X. OSD

-   S. OSD

-   Z. OSD

**E executar este comando:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**O seguinte é criado no diretório de destino (\\\\NewPkgStore\\ContosoApp):**

-   ContosoApp. AppV

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**No exemplo acima:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estes arquivos de diretório de origem...</th>
<th align="left">... são convertidos nestes arquivos de diretório de destino...</th>
<th align="left">... e conterá esses itens</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>S. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variáveis de ambiente</p></li>
<li><p>Teclado</p></li>
<li><p>Associações de tipo de arquivo</p></li>
<li><p>Informações do registro</p></li>
<li><p>Scripts</p></li>
</ul></td>
<td align="left"><p>Cada arquivo. OSD é convertido em um arquivo. xml separado e correspondente que contém os itens listados aqui no formato de configuração de implantação do App-V 5,1. Esses itens podem ser copiados desses arquivos. xml e colocados na configuração de implantação ou arquivos de configuração do usuário, conforme desejado.</p>
<p>Neste exemplo, há três arquivos. xml, correspondentes aos três arquivos. OSD no diretório de origem. Cada arquivo. xml contém as variáveis de ambiente, atalhos, associações de tipo de arquivo, informações do registro e scripts em seu arquivo. OSD correspondente.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>S. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. AppV</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variáveis de ambiente</p></li>
<li><p>Teclado</p></li>
<li><p>Associações de tipo de arquivo</p></li>
</ul></td>
<td align="left"><p>As informações dos arquivos. OSD especificadas no <code>-OSDsToIncludeInPackage</code> parâmetro são convertidas e colocadas dentro do pacote. Em seguida, o conversor preenche o arquivo de configuração de implantação e o arquivo de configuração do usuário com o conteúdo do pacote, da mesma forma que o sequenciador do App-V faz ao sequenciar um novo pacote.</p>
<p>Neste exemplo, as variáveis de ambiente, atalhos e associações de tipo de arquivo incluídas em X. OSD e Y. OSD foram convertidos e colocados no pacote App-V, e algumas dessas informações também foram incluídas nos arquivos de configuração de implantação e configuração do usuário. X. OSD e Y. OSD foram usados porque foram incluídos como argumentos para o <code>-OSDsToIncludeInPackage</code> parâmetro. Nenhuma informação do Z. OSD foi incluída no pacote porque não foi incluída como um desses argumentos.</p></td>
</tr>
</tbody>
</table>

 

## Convertendo pacotes criados usando uma versão anterior do App-V


Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões do App-V antes do App-V 5,0. O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.

**Importante**  Depois de converter um pacote existente, você deve testar o pacote antes de implantar o pacote para garantir que o processo de conversão foi bem-sucedido.

 

**O que saber antes de converter pacotes existentes**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problema</th>
<th align="left">Solução alternativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Os pacotes virtuais que usam o DSC não são vinculados após a conversão.</p></td>
<td align="left"><p>Vincule os pacotes usando grupos de conexão. Consulte <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Gerenciando grupos de conexão </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conflitos de variáveis de ambiente são detectados durante a conversão.</p></td>
<td align="left"><p>Resolva os conflitos no <strong> arquivo. OSD associado </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caminhos de código fixo são detectados durante a conversão.</p></td>
<td align="left"><p>Os caminhos embutidos em código são difíceis de serem convertidos corretamente. O conversor de pacote detecta e retorna pacotes com arquivos que contêm caminhos embutidos em código. Exiba o arquivo com o caminho embutido e determine se o pacote requer o arquivo. Em caso afirmativo, é recomendável resequenciar o pacote.</p></td>
</tr>
</tbody>
</table>

 

Ao converter um pacote, verifique se há arquivos ou atalhos com falha. Localize o item no pacote App-V 4,6. Pode ser um caminho embutido em código. Converter o caminho.

**Observação**  É recomendável que você use o sequenciador do App-V 5,1 para converter aplicativos críticos ou aplicativos que precisam tirar proveito dos recursos. Veja [como sequenciar um novo aplicativo com o App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).

Se um pacote convertido não abrir após você convertê-lo, também é recomendável que você reaplique a sequência do aplicativo usando o sequenciador do App-V 5,1.

 

[Como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## Migrando clientes


A tabela a seguir exibe o método recomendado para a atualização de clientes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualize seu ambiente para a versão mais recente do App-V 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerações de atualização e implantação do Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instale o cliente do App-V 5,1 com coexistência habilitada.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciar e distribuir pacotes do App-V 5,1. Conforme necessário, cancele a publicação de pacotes do App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">Como sequenciar um novo aplicativo com o App-V 5,1 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  Você deve estar executando a versão mais recente do App-V 4.6 para usar o modo de coexistência. Além disso, quando você sequenciar um pacote, você deve definir a configuração de **autoridade de gerenciamento** , que está localizada na seção **configuração do usuário** .

 

## Migrando a infraestrutura completa do App-V 5,1 Server


Não há um método direto para atualizar para uma infraestrutura completa do App-V 5,1. Use as informações na seção a seguir para obter informações sobre como atualizar o servidor App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualize seu ambiente para a versão mais recente do App-V 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Considerações de atualização e implantação do Application Virtualization </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implante a versão do App-V 5,1 do cliente.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Como implantar o cliente App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale o App-V 5,1 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Como implantar o servidor do App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrar pacotes existentes.</p></td>
<td align="left"><p>Veja a <strong> seção convertendo pacotes criados usando uma versão anterior do App-V </strong> deste artigo.</p></td>
</tr>
</tbody>
</table>

 

## Tarefas de migração adicionais


Você também pode executar tarefas de migração adicionais, como reconfiguração de pontos de extremidade, bem como abrir um pacote criado usando uma versão anterior em um computador que executa o cliente App-V 5,1. Os links a seguir fornecem mais informações sobre como executar essas tarefas.

[Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para todos os usuários em um computador específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Outros recursos para executar tarefas de migração do App-V


[Operações para o App-V 5.1](operations-for-app-v-51.md)

[Um procedimento simplificado de atualização do servidor de gerenciamento do Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





