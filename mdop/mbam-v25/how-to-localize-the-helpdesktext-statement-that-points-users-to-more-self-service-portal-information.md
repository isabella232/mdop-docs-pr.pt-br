---
title: Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento
description: Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799269"
---
# Como localizar a instrução "HelpdeskText" que direciona os usuários a mais informações sobre o Portal Autoatendimento


Você pode configurar uma versão localizada da instrução "HelpdeskText" do portal de autoatendimento, que informa os usuários finais sobre como obter ajuda adicional quando estiverem usando o portal de autoatendimento. Se você configurar o texto localizado para a instrução, conforme descrito nas instruções a seguir, o MBAM exibirá a versão localizada. Se MBAM não encontrar a versão localizada, ele exibirá o valor que está no parâmetro **HelpdeskText** .

**Observação**  Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento. Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.

 

**Para exibir uma versão localizada da instrução HelpdeskText**

1.  No servidor em que você configurou o portal de autoatendimento, navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.

2.  No painel **ações** , clique em **Adicionar** para abrir a caixa de diálogo **Adicionar configuração de aplicativo** .

3.  No campo **nome** , digite **HelpdeskText**\ _ &lt; *Language* &gt; , onde &lt; *idioma* &gt; é o código de idioma apropriado para o texto.

    Por exemplo, para criar uma instrução HelpdeskText localizada em espanhol, nomeie o parâmetro **HelpdeskText \ _es-es**.

    O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**. Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão. Esse fallback recursivo imita as regras de carregamento de recursos do .NET.

    Para obter uma lista dos códigos de idioma válidos que você pode usar, consulte [referência da API NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  No campo **valor** , digite o texto localizado que você deseja exibir para os usuários finais.



## Tópicos relacionados


[Personalizando o Portal de Autoatendimento para sua organização](customizing-the-self-service-portal-for-your-organization.md)

 

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



