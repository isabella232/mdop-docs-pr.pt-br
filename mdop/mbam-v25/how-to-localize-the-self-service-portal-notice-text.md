---
title: Como localizar o texto de aviso do Portal de Autoatendimento
description: Como localizar o texto de aviso do Portal de Autoatendimento
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799927"
---
# Como localizar o texto de aviso do Portal de Autoatendimento


Você pode configurar o texto de aviso localizado para exibir aos usuários finais por padrão no portal de autoatendimento. O arquivo Notice.txt que exibe o texto do aviso está no diretório raiz a seguir:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

Para exibir o texto de aviso localizado, crie um arquivo Notice.txt localizado e salve-o em uma pasta de idioma específico no seguinte diretório de exemplo:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

**Observação**  Você pode configurar o caminho usando o item **NoticeTextPath** nas **configurações do aplicativo**.

 

O MBAM exibe o texto do aviso com base nas seguintes regras:

-   Se você criar um arquivo **Notice.txt** localizado na pasta de idiomas apropriada, o MBAM exibirá o texto de aviso localizado se o arquivo de **Notice.txt** padrão existir. Se o arquivo **Notice.txt** padrão estiver ausente, será exibida uma mensagem indicando que o arquivo padrão está ausente.

-   Se o MBAM não encontrar uma versão localizada do arquivo Notice.txt, ele exibirá o texto no arquivo de Notice.txt padrão.

-   Se o MBAM não encontrar um arquivo de Notice.txt padrão, ele exibirá o texto padrão no portal de autoatendimento.

**Observação**  Se o navegador de um usuário final estiver definido como um idioma que não tenha uma subpasta ou Notice.txt de idioma correspondente, o texto no arquivo Notice.txt do diretório raiz a seguir será exibido:

&lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

 

**Para criar um arquivo Notice.txt localizado**

1.  No servidor em que você configurou o portal de autoatendimento, crie uma &lt; *Language* &gt; pasta de idiomas no seguinte diretório de exemplo, em que &lt; o *idioma* &gt; representa o nome do idioma localizado:

    &lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\ do serviço \\Self

    **Observação**  Algumas pastas de idioma já existem, portanto, talvez você não precise criar uma pasta. Se você precisar criar uma pasta de idiomas, consulte [referência da API do NLS (suporte ao idioma nacional)](https://go.microsoft.com/fwlink/?LinkId=317947) para obter uma lista dos nomes válidos que você pode usar para a pasta de &lt; *idiomas* &gt; .

     

2.  Crie um arquivo Notice.txt que contenha o texto de aviso localizado.

3.  Salve o arquivo Notice.txt na pasta de &lt; *idiomas* &gt; . Por exemplo, para criar um arquivo de Notice.txt localizado em espanhol, salve o arquivo Notice.txt localizado no seguinte exemplo de diretório:

    &lt;*Diretório de instalação de autoatendimento do MBAM* &gt; Website\\Es-es do serviço \\Self

    O nome da pasta de idioma também pode ser o nome de idioma neutro **es** em vez de **es-es**. Se o navegador do usuário final estiver definido como **es-es** e essa pasta não existir, a localidade pai (conforme definido no .net) será recuperada e verificada recursivamente, resolvendo para &lt; o diretório de instalação de autoatendimento MBAM &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de se tornar o arquivo de Notice.txt padrão. Esse fallback recursivo imita as regras de carregamento de recursos do .NET.



## Tópicos relacionados


[Personalizando o Portal de Autoatendimento para sua organização](customizing-the-self-service-portal-for-your-organization.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





