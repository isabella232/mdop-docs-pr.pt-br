---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799641"
---
# Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft


Para pesquisar as notas de versão do Microsoft User Experience Virtualization (UE-V) 2,0, pressione Ctrl + F.

Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V. As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto. Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Fornecendo comentários


Diga-nos o que você acha da nossa documentação do MDOP, enviando-nos seus comentários e comentários. Envie seus comentários sobre a documentação para [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemas conhecidos do UE-V


Esta seção contém notas de versão para a virtualização da experiência do usuário.

### As configurações do registro não são sincronizadas entre aplicativos nativos e App-V no mesmo computador

Quando um computador tem um aplicativo instalado por meio da virtualização de aplicativos (App-V) e um local com um arquivo do Windows Installer (. msi), as configurações baseadas em registro não são sincronizadas entre as tecnologias.

**Solução alternativa:** Para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a>As configurações não sincronizam quando o compartilhamento de rede está fora do domínio do usuário

Quando o Windows® 8 tenta a sincronização das configurações do sistema operacional, a sincronização falha com a seguinte mensagem de erro: **Boost:: FileSystem:: Exists:: nome de usuário ou senha incorreto**. Esse erro pode indicar que o compartilhamento de rede está fora do domínio do usuário ou um domínio com uma relação de confiança para esse domínio. Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**. Os compartilhamentos de rede usados para as configurações de UE-V armazenam locais de armazenamento devem residir no mesmo domínio do Active Directory que o usuário ou um domínio confiável do domínio do usuário.

**Solução alternativa:** Use compartilhamentos de rede do mesmo domínio do Active Directory que o usuário.

### Resultados imprevisíveis com o Office 2010 e o Office 2013 instalados

Quando um usuário tem o Office 2010 e o Office 2013 instalados, todas as configurações comuns entre as duas versões do Office são móveis pela UE-V. Isso pode fazer com que o tamanho do pacote do Office 2010 seja muito grande ou resulte em conflitos imprevisíveis com o 2013, principalmente se o Office 365 for usado.

**Solução alternativa:** Instale apenas uma versão do Office ou limite quais configurações são sincronizadas por UE-V.

### Desinstalar e reinstalar o aplicativo Windows 8 reverte as configurações para o estado inicial

Ao usar a sincronização de configurações do UE-V para um aplicativo do Windows 8, se o usuário desinstalar o aplicativo e reinstalar o aplicativo, as configurações do aplicativo retornarão aos valores padrão.Isso acontece porque a desinstalação remove a cópia local (em cache) das configurações do aplicativo, mas não remove o pacote de configurações local do UE-V.Quando o aplicativo é reinstalado e iniciado, o UE-V coleta as configurações do aplicativo que foram redefinidas para os padrões do aplicativo e, em seguida, carrega as configurações padrão para o local de armazenamento central.Outros computadores executando o aplicativo e, em seguida, baixar as configurações padrão.Esse comportamento é idêntico ao comportamento dos aplicativos da área de trabalho.

**Solução alternativa:** Nenhuma.

### Roaming de assinatura de email do Outlook 2010

O UE-V fará roaming dos arquivos de assinatura do Outlook 2010 entre dispositivos. No entanto, as opções de assinatura padrão para novas mensagens e respostas ou encaminhamentos não são sincronizadas. Essas duas configurações são armazenadas no perfil do Outlook, do qual a UE-V não faz roaming.

**Solução alternativa:** Nenhuma.

### O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office

Recomendamos que você instale a versão de 64 bits do Microsoft Office para computadores modernos. Para determinar qual versão você precisa, [clique aqui](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions). O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office. Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits. O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.

**Solução alternativa:** Nenhuma

### <a href="" id="msi-s-are-not-localized"></a>Os MSI não estão localizados

O UE-V 2,0 inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator. Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês. Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.

**Solução alternativa:** Nenhuma

### Favicons associados ao Internet Explorer 9 favoritos não fazem roaming

Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.

**Solução alternativa:** O favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado em cache no navegador Internet Explorer 9.

### Caminhos de configurações de arquivo são armazenados no registro

Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro. Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.

**Solução alternativa:** Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.

### Caminhos de armazenamento de configurações longos podem causar um erro

Mantenha as configurações dos caminhos de armazenamento o mais breve possível. Caminhos longos podem impedir a resolução ou a sincronização. O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações. Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo) +. pkgx. Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.

**Solução alternativa:** Nenhuma.

### Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional

As configurações do sistema operacional para o narrador e caracteres monetários específicos para o local (por exemplo, configurações de idioma e regionais) só serão transferidas para versões de sistema operacional do Windows. Por exemplo, os caracteres monetários não serão movidos entre o Windows 7 e o Windows 8.

**Solução alternativa:** Nenhuma

### Os aplicativos do Windows 8 não sincronizam as configurações quando o aplicativo é reiniciado após fechar inesperadamente

Se um aplicativo do Windows 8 for fechado inesperadamente logo após a inicialização, as configurações do aplicativo poderão não ser sincronizadas quando o aplicativo for reiniciado.

**Solução alternativa:** Feche o aplicativo do Windows 8, feche e reinicie o aplicativo UevAppMonitor.exe (pode usar o TaskManager) e reinicie o aplicativo do Windows 8.

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>O agente do UE-V 1 gera erros ao executar modelos do UE-V 2

Se um modelo de local de configurações do UE-V 2 for distribuído para um computador instalado com um agente UE-V 1, algumas configurações falharão na sincronização entre computadores e o agente reportará erros no log de eventos.

**Solução alternativa:** Ao migrar do UE-V 1 para o UE-V 2 e é provável que você tenha computadores executando a versão anterior do agente, crie um catálogo do UE-V 2,0 separado para dar suporte ao UE-V 2,0 Agent e aos modelos.

## Hotfixes e artigos da base de dados de conhecimento para UE-V 2,0


Esta seção contém hotfixes e artigos da KB para o UE-V 2,0.

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
<td align="left"><p>2927019</p></td>
<td align="left"><p>Pacote de hotfix 1 para Microsoft User Experience Virtualization 2,0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)">support.microsoft.com/kb/2927019</a></p></td>
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
<td align="left"><p>2930271</p></td>
<td align="left"><p>Noções básicas sobre as limitações de assinaturas do Outlook em roaming no Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)">support.microsoft.com/kb/2930271/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Como reparar uma instalação corrompida do UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Não há suporte para a migração de perfis MAPI com o Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769586</p></td>
<td align="left"><p>O UE-V transfere pastas vazias e chaves do registro</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Como habilitar o log de depuração na Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769570</p></td>
<td align="left"><p>O UE-V não atualiza o tema nas sessões do RDS ou da VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2901856</p></td>
<td align="left"><p>As configurações do aplicativo não sincronizam após você forçar uma reinicialização em um computador habilitado para UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)">support.microsoft.com/kb/2901856/EN-US</a></p></td>
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

 

 

 





