---
title: Como localizar o "HelpdeskURL" do Portal de Autoatendimento
description: Como localizar o "HelpdeskURL" do Portal de Autoatendimento
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799926"
---
# Como localizar o "HelpdeskURL" do Portal de Autoatendimento


Você pode configurar uma versão localizada da URL do portal de autoatendimento para exibir aos usuários finais por padrão. A URL do portal de autoatendimento é representada pelo parâmetro **HelpdeskURL**.

Se você criar uma versão localizada, conforme descrito nas instruções a seguir, a administração e o monitoramento do Microsoft BitLocker (MBAM) localiza e exibe a versão localizada. Se o MBAM não encontrar uma versão localizada, ele exibirá a URL configurada para o parâmetro **HelpDeskURL**.

**Observação**  Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento. Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.

 

**Para localizar a URL do portal de autoatendimento**

1.  No servidor em que você configurou o portal de autoatendimento, navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.

2.  No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .

3.  No campo **nome** , digite **HelpdeskURL**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para a URL.

    Por exemplo, para criar uma versão localizada do `HelpdeskURL` valor em espanhol, nomeie o parâmetro **HelpdeskURL \ _es-es**.

    O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**. Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão. Esse fallback recursivo imita as regras de carregamento de recursos do .NET.

    Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  No campo **valor** , digite a versão localizada do `HelpdeskURL` valor que você deseja exibir para os usuários finais.



## Tópicos relacionados


[Personalizando o Portal de Autoatendimento para sua organização](customizing-the-self-service-portal-for-your-organization.md)

 

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




