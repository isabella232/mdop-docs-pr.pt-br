---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft
author: dansimp
ms.assetid: 79a36c77-fa0c-4651-8028-4a79763a2fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0677dda93f2c2dc60ec627ae0c3f4bd8c199db6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799640"
---
# Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft


Para pesquisar as notas de versão do Microsoft User Experience Virtualization (UE-V) 2,0, pressione Ctrl + F.

Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V. As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto. Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Fornecendo comentários


Diga-nos o que você acha da nossa documentação do MDOP, enviando-nos seus comentários e comentários. Envie seus comentários sobre a documentação para [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemas conhecidos do UE-V


Esta seção contém notas de versão para a virtualização da experiência do usuário.

### Modelos de local das configurações do UE-V para o Skype causa falha no Skype

Quando um usuário gera um modelo de local de configurações válido para o aplicativo da área de trabalho do Skype, registra-o e, em seguida, inicia o aplicativo da área de trabalho do Skype, o Skype falha. Um _VIOLATION de acesso é registrado no log de eventos do aplicativo.

SOLUÇÃO alternativa: remova ou cancele o registro do modelo do Skype para permitir que o Skype funcione novamente.

### Scripts existentes para instalações silenciosas do UE-V podem falhar

Duas alterações feitas no instalador do UE-V podem fazer com que scripts de instalação silenciosa que funcionaram para versões anteriores do UE-V falhem ao instalar o UE-V 2,1. O primeiro é um novo requisito para que os usuários aceitem os termos de licença e concordem ou recusem a participação no programa de aperfeiçoamento da experiência do usuário (CEIP), mesmo durante uma instalação silenciosa. Usar o parâmetro/q não é mais suficiente para indicar a aceitação dos termos e do contrato de licença para participar do CEIP.

Em segundo lugar, o instalador agora força uma reinicialização do computador após a instalação do UE-V Agent. Isso pode causar uma falha em um script de instalação se ele não estiver esperando a reinicialização (por exemplo, instalar primeiro o UE-V Agent e, em seguida, instalar imediatamente o gerador).

SOLUÇÃO alternativa: o UE-V Installer (. msi) tem dois novos parâmetros de linha de comando que dão suporte a instalações silenciosas.

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
<td align="left"><p><strong>/ACCEPTLICENSETERMS = true</strong></p></td>
<td align="left"><p>Defina esse parâmetro como <strong> true </strong> para instalar o UE-V silenciosamente. Adicionar esse parâmetro implica que o usuário aceite os termos de licença do UE-V, que são encontrados (por padrão) aqui:%ProgramFiles%\Microsoft User Experience Virtualization\Agent</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/NORESTART</strong></p></td>
<td align="left"><p>Esse parâmetro impede o reinício obrigatório após a instalação do UE-V Agent. Um código de retorno de 3010 indica que uma reinicialização é necessária antes de usar o UE-V.</p></td>
</tr>
</tbody>
</table>

 

### As configurações do registro não são sincronizadas entre aplicativos nativos e App-V no mesmo computador

Quando um computador tem um aplicativo instalado por meio da virtualização de aplicativos (App-V) e localmente com um arquivo do Windows Installer (. msi), as configurações baseadas em registro não são sincronizadas entre as tecnologias.

SOLUÇÃO alternativa: para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.

### Resultados imprevisíveis com o Office 2010 e o Office 2013 instalados

Quando um usuário tem o Office 2010 e o Office 2013 instalados, todas as configurações comuns entre as duas versões do Office são móveis pela UE-V. Isso pode fazer com que o tamanho do pacote do Office 2010 seja muito grande ou resulte em conflitos imprevisíveis com o 2013, principalmente se o Office 365 for usado.

SOLUÇÃO alternativa: Instale apenas uma versão do Office ou limite quais configurações serão sincronizadas por UE-V.

### Desinstalar e reinstalar o aplicativo Windows 8 reverte as configurações para o estado inicial

Ao usar a sincronização de configurações do UE-V para um aplicativo do Windows 8, se o usuário desinstalar o aplicativo e reinstalar o aplicativo, as configurações do aplicativo retornarão aos valores padrão.Isso acontece porque a desinstalação remove a cópia local (em cache) das configurações do aplicativo, mas não remove o pacote de configurações local do UE-V.Quando o aplicativo é reinstalado e iniciado, o UE-V coleta as configurações do aplicativo que foram redefinidas para os padrões do aplicativo e, em seguida, carrega as configurações padrão para o local de armazenamento central.Outros computadores executando o aplicativo e, em seguida, baixar as configurações padrão.Esse comportamento é idêntico ao comportamento dos aplicativos da área de trabalho.

SOLUÇÃO alternativa: nenhum.

### O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office

Recomendamos que você instale a versão de 32 bits do Microsoft Office para sistemas operacionais de 32 bits e 64 bits. Para escolher a versão do Microsoft Office que você precisa, clique aqui. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office. Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits. O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.

SOLUÇÃO alternativa: nenhum

### <a href="" id="msi-s-are-not-localized"></a>Os MSI não estão localizados

O UE-V 2,0 inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator. Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês. Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.

SOLUÇÃO alternativa: nenhum

### Favicons associados ao Internet Explorer 9 favoritos não fazem roaming

Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.

SOLUÇÃO alternativa: o favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado no navegador do Internet Explorer 9.

### Caminhos de configurações de arquivo são armazenados no registro

Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro. Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.

SOLUÇÃO alternativa: Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.

### Caminhos de armazenamento de configurações longos podem causar um erro

Mantenha as configurações dos caminhos de armazenamento o mais breve possível. Caminhos longos podem impedir a resolução ou a sincronização. O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações. Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo) +. pkgx. Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.

SOLUÇÃO alternativa: nenhum.

### Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional

As configurações do sistema operacional para o narrador e caracteres monetários específicos para o local (por exemplo, configurações de idioma e regionais) só serão transferidas para versões de sistema operacional do Windows. Por exemplo, os caracteres monetários não serão movidos entre o Windows 7 e o Windows 8.

SOLUÇÃO alternativa: nenhum

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>O agente do UE-V 1 gera erros ao executar modelos do UE-V 2

Se um modelo de local de configurações do UE-V 2 for distribuído para um computador instalado com um agente UE-V 1, algumas configurações falharão na sincronização entre computadores e o agente reportará erros no log de eventos.

SOLUÇÃO alternativa: ao migrar do UE-V 1 para o UE-V 2, é provável que você tenha computadores executando a versão anterior do agente, crie um catálogo do UE-V 2,0 separado para dar suporte ao UE-V 2,0 Agent e modelos.

## Hotfixes e artigos da base de dados de conhecimento para UE-V 2,1


Esta seção contém hotfixes e artigos da KB para o UE-V 2,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artigo do KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>3018608</p></td>
<td align="left"><p>UE-V 2,1-TemplateConsole.exe falha quando as classes do UE-V WMI estão ausentes</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)">support.microsoft.com/kb/3018608/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-V: compatibilidade com o User Experience Virtualization (UE-V) com perfis de usuário</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>Configurações do UE-V Registry</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Configurações do UE-V replicadas pelo Internet Explorer</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Como reparar uma instalação corrompida do UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Não há suporte para a migração de perfis MAPI com o Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769586</p></td>
<td align="left"><p>O UE-V transfere pastas vazias e chaves do registro</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Como habilitar o log de depuração na Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769570</p></td>
<td align="left"><p>O UE-V não atualiza o tema nas sessões do RDS ou da VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Como usar a virtualização da experiência do usuário da Microsoft com aplicativos App-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Versões de arquivo atuais para a virtualização da experiência do usuário da Microsoft</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Informações sobre a virtualização da experiência do usuário e alta disponibilidade</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 






 

 





