---
title: Notas de versão do DaRT 7.0
description: Notas de versão do DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799137"
---
# Notas de versão do DaRT 7.0


**Para pesquisar essas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Sobre o diagnóstico e o conjunto de ferramentas de recuperação da Microsoft 7,0


Estas notas da versão contêm informações que são necessárias para instalar com êxito o DaRT7 e contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outra documentação da plataforma DaRT, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo incluído neste produto.

## Sobre a documentação do produto


A documentação do Microsoft Diagnostics e do conjunto de ferramentas de recuperação (DaRT) 7 é distribuída com o produto e no site de conexão.

Para obter ajuda detalhada sobre como usar as ferramentas no DaRT7, consulte o arquivo de ajuda disponível no menu **diagnóstico e recuperação do conjunto de ferramentas** .

## Fornecendo comentários


Estamos interessados em seus comentários sobre o DaRT7. Você pode enviar seus comentários para o dart7feedback@microsoft.com. Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras dessas ferramentas para torná-las mais úteis no futuro.

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, recomendamos que você instale as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conhecidos com o DaRT 7,0


### A verificação de SFC não pode iniciar se a limpeza do sistema autônomo estiver aberta

Se a limpeza do sistema autônomo estiver em execução, a verificação de SFC não poderá ser iniciada ou executada devido a um conflito de recursos entre as duas ferramentas.

**Solução alternativa:** Feche a ferramenta de limpeza do sistema autônomo antes de tentar abrir ou executar a ferramenta de verificação SFC.

### Caracteres Unicode podem não ser exibidos em nomes de arquivo

Se você excluir um arquivo que tem caracteres Unicode em seu nome de arquivo e tentar restaurar o arquivo usando a ferramenta restauração de arquivo, o arquivo não será encontrado. Isso só ocorre quando você usa caracteres de um idioma diferente do idioma do DVD do Windows que foi usado para criar a imagem de recuperação.

**Solução alternativa:** Certifique-se de que o idioma usado pelo DaRT corresponda ao idioma usado pelo sistema operacional do qual ele está tentando restaurar arquivos.

### A instalação de linha de comando do DaRT pode falhar silenciosamente

A instalação de linha de comando do DaRT falha silenciosamente se executada com a opção modo silencioso, a menos que seja executada usando permissões de administrador elevadas.

**Solução alternativa:** Execute a instalação de linha de comando usando permissões elevadas de administrador. A instalação do DaRT suporta as opções típicas do Windows Installer para instalação por linha de comando. Consulte [as opções de linha de comando](https://go.microsoft.com/fwlink/?LinkId=160689) do Windows Installer para obter mais informações sobre as várias opções disponíveis.

### A pesquisa de arquivos não pode mover uma pasta para um volume diferente

Não há suporte para a movimentação de pastas entre volumes pelo aplicativo de pesquisa de arquivos. Se você tentar mover uma pasta para um volume diferente na pesquisa de arquivos, o seguinte erro será retornado: "ocorreu um erro ao gravar o * &lt; nome &gt; *do arquivo do arquivo. Verifique se a unidade tem espaço suficiente e se o caminho de destino está acessível. "

**Solução alternativa:** Use o Explorer para mover uma pasta para um volume diferente.

### Alguns dados podem não estar disponíveis em computadores em que as letras de unidade são remapeadas

Esse problema pode ocorrer em computadores habilitados para BitLocker e em computadores multi-inicializador. Isso ocorre porque algumas informações no registro offline têm letras de drive embutidas e o DaRT usa letras diferentes para os mesmos volumes. Os efeitos típicos incluem não ter acesso a determinadas contas de usuário locais no editor do registro. Além disso, algumas ferramentas podem não conseguir obter as propriedades que dependem da resolução de caminhos de arquivo.

**Solução alternativa:** Use a opção para remapear as letras da unidade ao iniciar o DaRT. Isso geralmente alinha as letras de unidade típicas ao esperado.

### A desinstalação do hotfix pode não desinstalar determinadas atualizações

Algumas atualizações e service packs não podem ser desinstaladas porque são marcadas como não instaláveis ou porque elas precisam ser desinstaladas dentro do Windows 7. Nesses casos, a ferramenta de desinstalação de hotfix pode indicar que essas atualizações foram desinstaladas, mesmo que não tenham sido.

**Solução alternativa:** Desinstale essas atualizações problemáticas do Windows 7.

### Apagamento de disco: discos com volumes estendidos, volumes distribuídos ou volumes espelhados não podem ser excluídos

O apagamento de disco não dá suporte à exclusão de discos estendidos, espelhados ou distribuídos em um ou mais volumes.

**Solução alternativa:** Selecione e exclua cada disco no volume separadamente.

## Informações de direitos autorais da versão


Este documento é fornecido "como está". As informações e os modos de exibição expressos neste documento, incluindo URL e outras referências de site da Internet, podem mudar sem aviso prévio. Você assume o risco de usá-lo.

Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios.Nenhuma associação ou conexão real é intencional ou deve ser inferida.

Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft. Este documento é confidencial e proprietário da Microsoft. Ele é divulgado e pode ser usado somente mediante um contrato de não divulgação.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.

Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.

## Tópicos relacionados


[Sobre o DaRT 7.0](about-dart-70-new-ia.md)

 

 





