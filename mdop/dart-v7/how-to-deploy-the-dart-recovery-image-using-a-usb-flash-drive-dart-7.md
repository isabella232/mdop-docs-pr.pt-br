---
title: Como implantar a imagem de recuperação do DaRT usando um pen drive
description: Como implantar a imagem de recuperação do DaRT usando um pen drive
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799318"
---
# Como implantar a imagem de recuperação do DaRT usando um pen drive


Após concluir a execução do **Assistente de imagem de recuperação DART**, você pode usar a ferramenta em <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar o arquivo de imagem ISO para uma unidade flash USB (UFD).

Você também pode copiar manualmente o arquivo de imagem ISO para um UFD seguindo as etapas fornecidas nesta seção.

**Para salvar a imagem de recuperação do DaRT em uma unidade flash USB**

1.  Formate a unidade flash USB.

    1.  Em um sistema operacional válido ou uma sessão do WindowsPE válida, insira seu UFD.

    2.  No prompt de comando com permissões de administrador, digite **DiskPart** e digite **list disk**.

        A janela do prompt de comando exibe o número do disco do UFD, por exemplo, o **disco 1**.

    3.  Insira os comandos a seguir, um por vez, no prompt de comando.

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        **Observação**  O exemplo de código anterior pressupõe DISK1 é o UFD. Se for necessário, substitua o disco 1 pelo número do seu disco.

         

2.  Usando o método preferido da sua empresa para montar uma imagem, monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** do **Assistente de imagem de recuperação do DART**. Isso requer que você tenha um método disponível para montar um arquivo de imagem.

3.  Abra o arquivo de imagem ISO montado e copie todo o seu conteúdo para a unidade flash USB formatada.

    **Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o conteúdo para o UFD. Isso permite que você ignore a necessidade de montar a imagem.

     

## Tópicos relacionados


[Implantação da imagem de recuperação do DaRT 7.0](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





