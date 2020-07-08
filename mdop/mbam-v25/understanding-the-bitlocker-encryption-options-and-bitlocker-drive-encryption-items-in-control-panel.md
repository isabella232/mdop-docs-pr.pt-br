---
title: Noções básicas sobre as opções de criptografia BitLocker e itens de Criptografia de Unidade de Disco BitLocker no Painel de Controle
description: Noções básicas sobre as opções de criptografia BitLocker e itens de Criptografia de Unidade de Disco BitLocker no Painel de Controle
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796083"
---
# Noções básicas sobre as opções de criptografia BitLocker e itens de Criptografia de Unidade de Disco BitLocker no Painel de Controle


Este tópico descreve as **Opções de criptografia BitLocker** e os itens do painel de controle da **criptografia de unidade de disco BitLocker** e explica o seguinte:

-   Como esses itens são criados

-   Tarefas que eles permitem executar

-   **Gerenciar o BitLocker** Clique com o botão direito do mouse no menu de atalho, quando estiver visível versus oculto, e como configurá-lo para ser visto por padrão

## Opções de criptografia do BitLocker e itens do painel de controle da criptografia de unidade de disco BitLocker


A tabela a seguir lista as tarefas que você pode executar em cada item do painel de controle e descreve como esses itens são criados.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Opções de criptografia do BitLocker (MBAM)</th>
<th align="left">Criptografia de unidade de disco BitLocker (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefas que você pode fazer</p></td>
<td align="left"><ul>
<li><p>Alterar seu PIN ou senha</p></li>
<li><p>Verificar o status de criptografia para uma unidade</p></li>
<li><p>Abrir o console de gerenciamento do TPM</p></li>
<li><p>Ative o BitLocker</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Suspender proteção para uma unidade</p></li>
<li><p>Fazer backup da chave de recuperação</p></li>
<li><p>Alterar seu PIN</p></li>
<li><p>Desativar o BitLocker para uma unidade</p></li>
<li><p>Ativar o BitLocker para uma unidade</p></li>
<li><p>Abrir o console de gerenciamento do TPM</p></li>
<li><p>Descriptografar uma unidade (aparece apenas se o cliente do MBAM não estiver instalado)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Como o item do painel de controle é criado</p></td>
<td align="left"><p>Criado no painel de controle quando você instala o cliente MBAM. Este item não pode ser ocultado.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Este item é exibido em adição a, mas não substitui o item padrão do painel de controle de criptografia de unidade de disco BitLocker.</p>
</div>
<div>

</div></td>
<td align="left"><p>É exibido por padrão no painel de controle como parte do sistema operacional Windows, mas você pode ocultá-lo.</p>
<p>Para ocultá-la, confira <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> ocultação do item padrão de criptografia de unidade de disco BitLocker no painel de controle </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Menu de atalho "gerenciar BitLocker"


A tabela a seguir descreve como o menu de atalho **gerenciar o BitLocker** é diferente, dependendo se o cliente MBAM está instalado. O termo "menu de atalho" refere-se às opções exibidas quando você clica com o botão direito do mouse em uma unidade no Windows Explorer.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Quando o cliente MBAM é instalado</th>
<th align="left">Quando o cliente MBAM não está instalado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visibilidade do menu de atalho</p></td>
<td align="left"><p>A opção gerenciar BitLocker está oculta.</p>
<p>Para deixar a opção gerenciar BitLocker visível no menu de atalho, que exibe a opção para descriptografar uma unidade, exclua a seguinte chave do registro:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>A opção gerenciar o BitLocker é exibida no menu de atalho.</p></td>
</tr>
<tr class="even">
<td align="left"><p>O que os usuários podem fazer</p></td>
<td align="left"><p>Com o atalho oculto, os usuários podem abrir o item do painel de controle de criptografia de unidade de disco BitLocker, mas a opção para descriptografar uma unidade não está disponível.</p></td>
<td align="left"><p>Com o atalho visível, selecionar a <strong> opção gerenciar BitLocker </strong> abre o item do painel de controle de criptografia de unidade de disco BitLocker, que exibe a opção para descriptografar uma unidade.</p></td>
</tr>
</tbody>
</table>




## Tópicos relacionados


[Administrando os recursos do MBAM 2.5](administering-mbam-25-features.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





