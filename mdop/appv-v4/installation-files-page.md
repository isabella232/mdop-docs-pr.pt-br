---
title: Página Arquivos de Instalação
description: Página Arquivos de Instalação
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796906"
---
# Página Arquivos de Instalação


Use a página **arquivos de instalação** para especificar os arquivos de instalação que foram usados para criar o pacote de aplicativo virtual especificado na página **selecionar pacote** deste assistente. Se você criou um pacote de aplicativo virtual que contém vários aplicativos, copie todos os arquivos de instalação necessários para uma única pasta no computador executando o Microsoft Application Virtualization Sequencer.

Esta página contém os seguintes elementos:

<a href="" id="original-installation-files"></a>**Arquivos de instalação originais**  
Clique em **procurar** para especificar os arquivos de instalação que foram usados originalmente para criar o pacote de aplicativo virtual. O diretório pai que você especificar deve ser salvo localmente no computador que executa o sequenciador e deve conter todos os arquivos de instalação ou subpastas necessários que contenham os arquivos de instalação. Os arquivos de instalação podem estar contidos na pasta pai ou em qualquer uma das subpastas da pasta pai especificada.

<a href="" id="files-installed-on-local-system"></a>**Arquivos instalados no sistema local**  
Clique em **procurar** para especificar os arquivos de instalação que foram instalados localmente no computador que está executando o sequenciador. Você só pode selecionar essa opção se os arquivos de instalação do aplicativo tiverem sido instalados no local padrão do aplicativo.

**Observação**  O local de instalação padrão fornecido depende das seguintes condições:

 

-   A raiz do pacote especificada quando o pacote foi originalmente criado.

-   O local de instalação especificado no Windows Installer quando o pacote foi originalmente criado.

-   O caminho de instalação do aplicativo padrão.

Por exemplo, se a raiz do pacote especificada for **Q:\\Office12** e durante a instalação, o local de instalação padrão será alterado de **c:\\Arquivos de Files\\Office12** para **Q:\\Office12**, o caminho especificado durante DEHYDRATION deve ser **c:\\Arquivos de Files\\Office 12**.

Se a raiz do pacote especificada for **Q:\\Microsoft** e durante a instalação, o local de instalação padrão será alterado de **c:\\Arquivos de Files\\Office12** para **Q:\\Microsoft\\Office12**, o caminho especificado durante DEHYDRATION deve ser c:\\Arquivos de **programas**.

Quando você cria um pacote usando um acelerador de pacote, cada arquivo no pacote, por exemplo **Q:\\Office12\\file.txt** é encontrado no computador local, substituindo o **Q:\\Office12** raiz do pacote pelo local padrão especificado quando o acelerador do pacote foi criado, por exemplo, **c:\\Arquivos de Files\\Office12**. No exemplo anterior, o arquivo deve estar localizado em **c:\\Arquivos de Files\\Office12\\file.txt**.

## Tópicos relacionados


[Assistente para Criar Acelerador de Pacote (App-V 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





