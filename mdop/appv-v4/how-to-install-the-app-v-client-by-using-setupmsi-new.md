---
title: Como instalar o cliente do App-V usando Setup.msi
description: Como instalar o cliente do App-V usando Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797104"
---
# Como instalar o cliente do App-V usando Setup.msi


Este tópico descreve como instalar o cliente App-V usando o programa setup.msi. Antes de instalar o cliente App-V usando o programa setup.msi, você deve primeiro determinar se um software de pré-requisito deve ser instalado e, em seguida, deve instalá-lo. Para instalar o software de pré-requisito, consulte a seção [instalando o software de pré-requisito](#prereq-sw) deste tópico. Para instalar o software cliente, confira o artigo [instalando o aplicativo App-V usando a seção de programas Setup.msi](#msi-setup) deste tópico.

## <a href="" id="prereq-sw"></a>Instalar software de pré-requisito


Você pode usar os procedimentos a seguir para instalar o software de pré-requisito. Você pode criar um arquivo de comando e executar os comandos a partir do prompt de comando ou pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar os comandos.

**Observação**  As versões x86 do seguinte software são necessárias para as versões x86 e x64 do cliente App-V.

 

**Para instalar o Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**

1. Baixe o pacote de software do [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) a partir do centro de download da Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ). \ [Valor de token de modelo \] da versão 4,5 SP2 e posterior do cliente App-V, baixar vcredist\_x86.exe do [pacote redistribuído do Microsoft Visual C++ 2005 Service Pack 1 atualização de segurança do ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valor de token do modelo \]

2. Para instalar silenciosamente, use a opção de linha de comando "/Q" com vcredist\_x86.exe — por exemplo, **vcredist\_x86.exe/q**.

3. Para instalar o software usando o arquivo vcredist\_x86.msi, use a opção de linha de comando "/C/T: &lt; fullpathtofolder &gt; " para extrair os arquivos vcredist.msi e vcredis1.cab de vcredist\_x86.exe para uma pasta temporária. Para instalar silenciosamente, use a opção de linha de comando/quiet — por exemplo, **msiexec/i vcredist.msi** /Quiet.

### Para instalar o Microsoft VisualC + + 2008SP1 Redistributable Package (x86)

**Importante**  Para a versão 4.6 e posterior do cliente App-V, você também deve instalar a atualização de segurança ATL do pacote Microsoft Visual C++ 2008 Service Pack 1.

 

****

1.  Baixe o pacote do software de [atualização de segurança do Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package](https://go.microsoft.com/fwlink/?LinkId=150700) do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Para instalar silenciosamente, use a opção de linha de comando "/Q" com vcredist\_x86.exe — por exemplo, **vcredist\_x86.exe/q**.

### Para instalar o Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Baixe o pacote de software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) a partir do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Para instalar silenciosamente, use a opção de linha de comando/quiet — por exemplo, **msiexec/i msxml6\_x86.msi/Quiet**.

### Para instalar o relatório de erros do aplicativo Microsoft

Ao instalar o relatório de erros do aplicativo Microsoft, você deve usar o parâmetro *APPGUID* para especificar o código do produto App-V. O código do produto é exclusivo para cada tipo e versão do cliente App-V. Selecione o código do produto correto na tabela a seguir.

**Importante**  Para o App-V 4.6 SP2 e posterior, você não precisa mais instalar o relatório de erros do aplicativo Microsoft (dw20shared.msi). O App-V agora usa o relatório de erros da Microsoft.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão</th>
<th align="left">Código do produto para o cliente da área de trabalho</th>
<th align="left">Código de produto do cliente para serviços de área de trabalho remota</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

versão do ¹ App-V "Languages".

**Observação**  Se precisar localizar o código do produto, você pode usar o editor de banco de dados Orca.exe ou uma ferramenta semelhante para examinar os arquivos do Windows Installer para localizar o valor da propriedade *ProductCode* . Para obter mais informações sobre como usar Orca.exe, consulte [ferramentas de desenvolvimento do Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Localize o programa de instalação do relatório de erros do aplicativo Microsoft, dw20shared.msi, que pode ser encontrado na pasta **Support\\Watson** na mídia de lançamento.

2.  Para instalar o software, execute o seguinte comando:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Instalando o cliente App-V usando o programa Setup.msi


Use o procedimento a seguir para instalar o cliente App-V. Verifique se todos os softwares de pré-requisito necessários foram instalados. \ [Valor de token de modelo \] para a versão 4.6 e posterior do cliente App-V, o programa setup.msi verifica o sistema e, se o software de pré-requisito não estiver instalado, ele gerará uma mensagem de erro indicando que a instalação não pode continuar. \ [Valor do token do modelo \]

**Para instalar o cliente do Application Virtualization usando o Setup.msi**

1.  Verifique se você está conectado com uma conta que tem direitos de administrador no computador.

2.  Abra uma janela do prompt de comando usando direitos elevados e altere o diretório para a pasta que contém os arquivos de instalação. Ao instalar a versão 4.6 ou posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits. A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.

3.  Digite a cadeia de caracteres do comando instalar no prompt de comando. Você também pode criar um arquivo de comando e executá-lo a partir do prompt de comando. Você também pode usar uma linguagem de script como VBScript ou Windows PowerShell para executar o comando.

4.  O exemplo de linha de comando a seguir mostra como setup.msi pode ser usado com vários parâmetros opcionais. Para obter mais informações sobre esses parâmetros, consulte [parâmetros de linha de comando do instalador do cliente do cliente de virtualização do aplicativo](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "sistema de produção" SWIPUBSVRTYPE = "HTTP/secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "appsntype.xml/AppVirt/" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client" SWIFSDRIVE = "=" S "/q**

    **Importante**  
    -   O comutador do Windows Installer "**/q**" é usado para fazer isso uma instalação silenciosa.

    -   Os **%** caracteres "" em "**% HomeDrive%**" devem ser precedidos pelo **^** caractere de escape "". Caso contrário, o Shell de comando do Windows define o valor para aquele do usuário que está executando a instalação.

    -   Para ativar o registro em log de instalação, use o msiexec switch **/l\ * v filename. log**.

     

## Tópicos relacionados


[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





