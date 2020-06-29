---
title: Como definir a pré-configuração de imagens
description: Como definir a pré-configuração de imagens
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799866"
---
# Como definir a pré-configuração de imagens


**Observação**  Pré-preparação de imagem é útil somente para o download inicial da imagem. Não há suporte para a atualização de imagem.

 

## Como definir a pré-configuração de imagens


**Para configurar o pré-teste de imagem**

1.  No computador cliente, no diretório de armazenamento de imagens, crie uma pasta para a imagem de pré-teste e nomeie-a em *imagens do MED-V*.

    **Observação**  Essa pasta deve ser chamada *de imagens do MED-V*.

     

2.  Na pasta de imagens do MED-V, crie uma subpasta e nomeie-a *PrestagedImages*.

    **Observação**  Essa pasta deve ser chamada de *PrestagedImages*.

     

3.  Para aplicar a segurança da ACL (listas de controle de acesso) à pasta de *imagens do MED-V* , defina a seguinte ACL:

    **Usuários do NT AUTHORITY\\Authenticated: (OI) (CI) (acesso especial:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 ARQUIVO \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Observação**  É recomendável aplicar a segurança de ACL à pasta de *imagens do MED-V* .

     

4.  Para aplicar a segurança de ACL à pasta *PrestagedImages* , defina a seguinte ACL:

    **Usuários do NT AUTHORITY\\Authenticated: (OI) (CI) (acesso especial:)**

    **LEIA \ _CONTROL**

    **SINCRONIZAR**

    **ARQUIVO \ _GENERIC \ _READ**

    **ARQUIVO \ _READ \ _DATA**

    **ARQUIVO \ _READ \ _EA**

    **ARQUIVO \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Observação**  É recomendável aplicar a segurança de ACL à pasta *PrestagedImages* .

     

5.  Empurre os arquivos de imagem (CKM e INDEX Files) para a pasta *PrestagedImages* .

    **Observação**  Depois que os arquivos de imagem forem enviados para a pasta de pré-teste, é recomendável executar uma verificação de integridade de dados e marcá-los como somente leitura.

     

6.  Inclua o seguinte parâmetro na instalação do cliente MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V images"*.

## Como atualizar o local de pré-teste


**Para atualizar o local de pré-teste**

1.  A chave do registro, *PrestagedImagesPath*, aponta para o local da imagem padrão. Ele está localizado no seguinte diretório:

    -   Em x86- `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   Em um x64- `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Se a imagem estiver em um local diferente, altere o caminho.

 

 





