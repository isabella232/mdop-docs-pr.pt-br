---
title: Introdução ao App-V 5.0
description: Introdução ao App-V 5.0
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796528"
---
# Introdução ao App-V 5.0


O App-V 5,0 permite aos administradores implantar, atualizar e dar suporte a aplicativos como serviços em tempo real, de acordo com a necessidade. Os aplicativos individuais são transformados de produtos instalados localmente em serviços de gerenciamento centralizado e estão disponíveis onde você precisar, sem a necessidade de pré-configurar computadores ou alterar as configurações do sistema operacional.

O App-V consiste nos seguintes elementos:

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
<td align="left"><p>Servidor de gerenciamento do App-V</p></td>
<td align="left"><ul>
<li><p>Fornece um local central para o gerenciamento da infraestrutura do App-V, que fornece aplicativos virtuais para o cliente da área de trabalho do App-V e para os serviços de área de trabalho remota (antigo Terminal Services).</p></li>
<li><p>Usa o Microsoft SQL Server® para seu armazenamento de dados, em que um ou mais servidores de gerenciamento do App-V podem compartilhar um único repositório de dados do SQL Server.</p></li>
<li><p>Autentica solicitações e fornece segurança, medição, monitoramento e coleta de dados. O servidor usa o Active Directory e ferramentas de suporte para gerenciar usuários e aplicativos.</p></li>
<li><p>Tem um site de gerenciamento baseado em® do Silverlight, que permite que você configure a infraestrutura do App-V em qualquer computador. Você pode adicionar e remover aplicativos, manipular atalhos, atribuir permissões de acesso a usuários e grupos e criar grupos de conexão.</p></li>
<li><p>Permite a comunicação entre o console de gerenciamento da Web do App-V e o repositório de dados do SQL Server. Esses componentes podem ser instalados em um único computador servidor ou em um ou mais computadores separados, dependendo da arquitetura do sistema necessária.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de publicação do App-V</p></td>
<td align="left"><ul>
<li><p>Fornece clientes App-V com aplicativos qualificados para o usuário específico</p></li>
<li><p>Hospeda o pacote de aplicativo virtual para streaming.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de Desktop App-V</p></td>
<td align="left"><ul>
<li><p>Recupera aplicativos virtuais</p></li>
<li><p>Publica os aplicativos nos clientes</p></li>
<li><p>Configura e gerencia automaticamente ambientes virtuais em tempo de extremidade do Windows.</p></li>
<li><p>Armazena configurações de aplicativo virtual específicas do usuário, como alterações de registro e arquivo, em cada perfil de usuário&#39;s.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de serviços de área de trabalho remota do App-V (RDS)</p></td>
<td align="left"><p>Permite que servidores host da sessão da área de trabalho remota usem os recursos do cliente da área de trabalho do App-V para sessões de área de trabalho compartilhadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciador App-V</p></td>
<td align="left"><ul>
<li><p>É uma ferramenta baseada em assistente que você usa para transformar aplicativos tradicionais em aplicativos virtuais.</p></li>
<li><p>Produz o aplicativo "pacote", que consiste em:</p>
<ol>
<li><p>um arquivo do aplicativo sequenciado (APPV)</p></li>
<li><p>um arquivo do Windows Installer (MSI) que pode ser implantado para clientes configurados para operação autônoma</p></li>
<li><p>Vários arquivos XML, incluindo Report.XML, PackageName_DeploymentConfig.XML e PackageName_UserConfig.XML. Os arquivos userconfig e DeploymentConfig XML são usados para configurar as alterações personalizadas no comportamento padrão do pacote.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre esses elementos, consulte [arquitetura de alto nível para o App-V 5,0](high-level-architecture-for-app-v-50.md).

Se você for novo para este produto, recomendamos que leia a documentação completamente. Antes de implantá-lo em um ambiente de produção, também recomendamos que você valide seu plano de implantação em um ambiente de rede de teste. Você também pode considerar a criação de uma classe sobre tecnologias pertinentes. Para obter mais informações sobre oportunidades de treinamento da Microsoft, consulte a visão geral de treinamento da Microsoft em <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Observação**  Uma versão que pode ser baixada do guia deste administrador não está disponível. No entanto, você pode aprender sobre um modo especial da biblioteca do TechNet que permite a você selecionar artigos, agrupá-los em uma coleção e imprimi-los ou exportá-los para um arquivo em <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Esta seção do guia do administrador do App-V 5,0 inclui informações de alto nível sobre o App-V 5,0 para fornecer a você uma compreensão básica do produto antes de iniciar o planejamento de implantação.

## Introdução ao App-V 5,0


-   [Sobre o App-V 5.0](about-app-v-50.md)

    Fornece uma visão geral de alto nível do App-V 5,0 e como ele pode ser usado em sua organização.

-   [Sobre o App-V 5.0 SP1](about-app-v-50-sp1.md)

    Fornece uma visão geral de alto nível do App-V 5.0 SP1 e como ele pode ser usado em sua organização.

-   [Sobre o App-V 5.0 SP2](about-app-v-50-sp2.md)

    Fornece uma visão geral de alto nível do App-V 5.0 SP2 e como ele pode ser usado em sua organização.

-   [Sobre o App-V 5.0 SP3](about-app-v-50-sp3.md)

    Fornece uma visão geral de alto nível do App-V 5.0 SP2 e como ele pode ser usado em sua organização.

-   [Avaliação do App-V 5.0](evaluating-app-v-50.md)

    Fornece informações sobre como você pode avaliar melhor o App-V 5,0 para uso em sua organização.

-   [Arquitetura de alto nível para o App-V 5.0](high-level-architecture-for-app-v-50.md)

    Fornece uma descrição dos recursos do App-V 5,0 e como eles funcionam juntos.

-   [Acessibilidade para o App-V 5.0](accessibility-for-app-v-50.md)

    Fornece informações sobre recursos e serviços que tornam esse produto e sua documentação correspondente mais acessível para pessoas com deficiências.

## <a href="" id="other-resources-for-this-product-"></a>Outros recursos para este produto


-   [Guia do administrador do Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Planejamento para o App-V 5.0](planning-for-app-v-50-rc.md)

-   [Implantação do App-V 5.0](deploying-app-v-50.md)

-   [Operações para o App-V 5.0](operations-for-app-v-50.md)

-   [Solução de problemas do App-V 5.0](troubleshooting-app-v-50.md)






 

 





