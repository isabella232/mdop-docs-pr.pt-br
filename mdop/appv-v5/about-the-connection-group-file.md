---
title: Sobre o arquivo do grupo de conexão
description: Sobre o arquivo do grupo de conexão
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796623"
---
# Sobre o arquivo do grupo de conexão


**Neste tópico:**

-   [Finalidade e local do arquivo de grupo de conexão](#bkmk-cg-purpose-loc)

-   [Estrutura do arquivo XML do grupo de conexões](#bkmk-define-cg-5-0sp3)

-   [Configurar a prioridade dos pacotes em um grupo de conexão](#bkmk-config-pkg-priority-incg)

-   [Configurações de conexão de aplicativo virtual com suporte](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Finalidade e local do arquivo de grupo de conexão


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Finalidade do grupo de conexão</p></td>
<td align="left"><p>Um grupo de conexão é um recurso App-V que permite agrupar pacotes para criar um ambiente virtual no qual os aplicativos desses pacotes podem interagir uns com os outros.</p>
<p>Exemplo: você deseja usar plug-ins com o Microsoft Office. Você pode criar um pacote que contém os plug-ins e criar outro pacote que contém o Office e, em seguida, adicionar os dois pacotes a um grupo de conexão para permitir que o Office Use esses plug-ins.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Como funciona o arquivo de grupo de conexão</p></td>
<td align="left"><p>Quando você aplica um arquivo de grupo de conexão do Application Virtualization 5,0, os pacotes enumerados no arquivo serão combinados em tempo de execução em um único ambiente virtual. Use o arquivo de grupo de conexão do 5,0 do Microsoft Application Virtualization (App-V) para configurar grupos de conexão do aplicativo virtual 5,0 existentes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caminho de arquivo de exemplo</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Estrutura do arquivo XML do grupo de conexões


**Nesta seção:**

-   [Parâmetros que definem o grupo de conexão](#bkmk-params-define-cg)

-   [Parâmetros que definem os pacotes no grupo de conexões](#bkmk-params-define-pkgs-incg)

-   [App-V 5,0 SP3 exemplo de arquivo XML do grupo de conexões](#bkmk-50sp3-exp-cg-xml)

-   [Exemplo do App-V 5,0 a App-V 5,0 SP2-arquivo XML do grupo de conexões](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Parâmetros que definem o grupo de conexão

A tabela a seguir descreve os parâmetros no arquivo XML que definem o grupo de conexão propriamente dito, e não os pacotes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome do esquema</p></td>
<td align="left"><p>Nome do esquema.</p>
<p><strong>Aplicável a partir do App-V 5,0 SP3 </strong> : se você quiser usar os novos recursos "pacotes opcionais" e "usar qualquer versão" descritos nesta tabela, você deve especificar o seguinte esquema no arquivo XML:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Identificador de GUID exclusivo para esse grupo de conexão. O estado do grupo de conexão é associado a esse identificador. Especifique esse identificador somente quando criar o grupo de conexão.</p>
<p>Você pode criar um novo GUID digitando: <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificador de GUID de versão para esta versão do grupo de conexão.</p>
<p>Ao atualizar um grupo de conexão (por exemplo, ao adicionar ou atualizar um novo pacote), você deve atualizar o GUID de versão para refletir a nova versão.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Nome para exibição do grupo de conexão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Prioridade</p></td>
<td align="left"><p>Campo prioridade opcional para o grupo conexão.</p>
<p><strong>"0" </strong> - indica a prioridade mais alta.</p>
<p>Se for necessária uma prioridade, mas não tiver sido configurada, o pacote falhará porque o grupo de conexões correto a ser usado não pode ser determinado.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Parâmetros que definem os pacotes no grupo de conexões

Na &lt; seção pacotes &gt; do arquivo XML do grupo de conexão, você lista os pacotes de membros no grupo conexão especificando cada identificador de pacote exclusivo e identificador de versão do pacote, conforme descrito na tabela a seguir. O primeiro pacote na lista tem a precedência mais alta.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageID</p></td>
<td align="left"><p>Identificador de GUID exclusivo para este pacote. Esse GUID não é alterado quando novas versões do pacote são publicadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificador de GUID exclusivo para a versão do pacote.</p>
<p><strong>Aplicável a partir do App-V 5,0 SP3 </strong> : se você especificar <strong> "*" </strong> para a versão do pacote, o GUID da versão do pacote mais recente disponível será inserido dinamicamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>Aplicável a partir do App-V 5,0 SP3 </strong> : parâmetro que permite que você crie um pacote opcional dentro do grupo de conexão. As entradas válidas são:</p>
<ul>
<li><p><strong>"verdadeiro" </strong> – o pacote é opcional no grupo de conexão</p></li>
<li><p><strong>"falso" </strong> – o pacote é necessário no grupo de conexão</p></li>
</ul>
<p>Veja <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)"> como usar pacotes opcionais em grupos de conexão </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>App-V 5,0 SP3 exemplo de arquivo XML do grupo de conexões

O exemplo de arquivo XML do grupo de conexão a seguir mostra exemplos dos campos nas tabelas anteriores e realça os itens que são novos para o App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>Exemplo do App-V 5,0 a App-V 5,0 SP2-arquivo XML do grupo de conexões

O exemplo de arquivo XML do grupo de conexão de exemplo a seguir aplica-se ao App-V 5,0 a App-V 5,0 SP2. Ele mostra exemplos dos campos na tabela anterior, mas exclui as alterações descritas acima para o App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Configurar a prioridade dos pacotes em um grupo de conexão


A precedência do pacote é configurada usando a ordem da lista do pacote. O primeiro pacote no documento tem a precedência mais alta. Os pacotes subsequentes na lista têm prioridade decrescente.

A precedência do pacote é a resolução para colisões de recursos inevitávels durante a inicialização do ambiente virtual. Por exemplo, se dois pacotes que estão sendo abertos no mesmo ambiente virtual definirem o mesmo valor DWORD do registro, o pacote com a precedência mais alta determinará o valor definido.

Você pode usar o arquivo de grupo de conexão para configurar cada grupo de conexão usando os seguintes métodos:

-   Especifique as prioridades do tempo de execução para grupos de conexão.

    **Observação**  A prioridade só será necessária se o pacote estiver associado a mais de um grupo de conexão.

     

-   Especifique a precedência do pacote dentro do grupo de conexão.

O campo Priority é necessário quando um aplicativo virtual em execução é iniciado a partir de uma solicitação de aplicativo nativo, por exemplo, o Microsoft Windows Explorer. O cliente App-V usa a prioridade para determinar em qual ambiente virtual de grupo de conexão o aplicativo deve ser executado. Essa situação ocorre se um aplicativo virtual fizer parte de vários grupos de conexão.

Se um aplicativo virtual for aberto usando outro aplicativo virtual, o ambiente virtual do aplicativo virtual original será usado. Nesse caso, o campo Priority não é usado.

**Exemplo:**

O aplicativo virtual que o Microsoft Outlook está em execução no ambiente virtual **XYZ**. Quando você abre um documento do Microsoft Word anexado, uma versão virtualizada do Microsoft Word abre no ambiente virtual **XYZ**, independentemente dos grupos de conexão associados do Microsoft Word ou das prioridades do tempo de execução da máquina virtual.

## <a href="" id="bkmk-va-conn-configs"></a>Configurações de conexão de aplicativo virtual com suporte


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração</th>
<th align="left">Cenário de exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>A. plug-in e arquivo exe (. dll)</p></td>
<td align="left"><ul>
<li><p>Você deseja distribuir o Microsoft Office para todos os usuários, mas distribuir um plug-in do Microsoft Excel para apenas um subconjunto de usuários.</p></li>
<li><p>Habilite o grupo de conexão para os usuários apropriados.</p></li>
<li><p>Atualize cada pacote individualmente, conforme necessário.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>A. arquivo exe e um aplicativo de middleware</p></td>
<td align="left"><ul>
<li><p>Você tem um aplicativo exige um aplicativo de middleware ou vários aplicativos que dependem da mesma versão de tempo de execução de middleware.</p></li>
<li><p>Todos os computadores que exigem um ou mais aplicativos recebem os grupos de conexão com o aplicativo de tempo de execução do aplicativo e middleware.</p></li>
<li><p>Opcionalmente, você pode combinar vários aplicativos middleware em um único grupo de conexão.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Exemplo</th>
<th align="left">Exemplo de descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Grupo de conexão de aplicativo virtual para a divisão financeira</p></td>
<td align="left"><ul>
<li><p>Aplicativo middleware 1</p></li>
<li><p>Aplicativo Middleware 2</p></li>
<li><p>Aplicativo middleware 3</p></li>
<li><p>Tempo de execução do aplicativo middleware</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de conexão de aplicativo virtual para divisão de RH</p></td>
<td align="left"><ul>
<li><p>Aplicativo middleware 5</p></li>
<li><p>Aplicativo middleware 6</p></li>
<li><p>Tempo de execução do aplicativo middleware</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>A. arquivo exe e um arquivo. exe</p></td>
<td align="left"><p>Você tem um aplicativo que depende de outro aplicativo e deseja manter os pacotes separados para desempenho operacional, restrições de licenciamento ou linhas do tempo de distribuição.</p>
<p><strong>Exemplo:</strong></p>
<p>Se você estiver implantando o Microsoft Lync 2010, poderá usar três pacotes:</p>
<ul>
<li><p>Microsoft office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>Você pode gerenciar a implantação usando os seguintes grupos de conexão:</p>
<ul>
<li><p>Microsoft office2010 e Microsoft Communicator2007</p></li>
<li><p>Microsoft office2010 e Microsoft Lync2010</p></li>
</ul>
<p>Quando a implantação for concluída, você poderá criar um único novo pacote Microsoft office2010 + Microsoft Lync2010 ou mantê-los e mantê-los como pacotes separados e implantá-los usando um grupo de conexão.</p></td>
</tr>
</tbody>
</table>

 






## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups.md)

 

 





