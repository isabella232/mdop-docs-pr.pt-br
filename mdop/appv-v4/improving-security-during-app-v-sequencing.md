---
title: Como melhorar a segurança durante o sequenciamento do App-V
description: Como melhorar a segurança durante o sequenciamento do App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796909"
---
# Como melhorar a segurança durante o sequenciamento do App-V


Os aplicativos de empacotamento para sequenciamento são a maior tarefa em andamento em uma infraestrutura do App-V. Como essa tarefa está em andamento, você deve considerar com cuidado a criação de políticas e procedimentos a serem seguidos durante a sequenciamento de aplicativos. No App-V 4.5, durante o sequenciamento, você pode capturar listas de controle de acesso (ACLs) nos ativos de arquivo do aplicativo virtualizado.

## Verificação de vírus no sequenciador


É uma prática recomendada instalar o software de digitalização no computador de sequenciamento e, em seguida, verificar o computador em busca de vírus e malware. Depois que o computador de sequenciamento é examinado e gratuito de qualquer vírus ou malware, desabilite o software de digitalização, incluindo todo o antivírus e software de detecção de malware, no computador de sequenciamento antes de sequenciar qualquer aplicativo. Isso acelera o processo de sequenciamento e impede que os componentes do software de digitalização sejam detectados durante o sequenciamento e incluídos no pacote de aplicativo virtual.

## Capturando ACLs em arquivos (NTFS)


O sequenciador captura as permissões de NTFS (as ACLs) dos arquivos que são monitorados durante a fase de instalação de sequenciamento. (Antes do lançamento do App-V 4.5, as ACLs não eram capturadas como parte do processo de sequenciamento.) Este novo recurso permite que determinados aplicativos sejam executados para usuários com um nível baixo de permissão que normalmente exigiria privilégios administrativos.

Esse recurso também permite que o engenheiro de sequenciamento Capture as configurações de segurança identificadas pelo fornecedor. A falha na aplicação das configurações recomendadas pelo fornecedor pode deixar o aplicativo aberto para atacar ou usar indevido para os usuários. Para obter informações sobre se você deve ou não implantar um aplicativo com ACLs abertas, consulte o grupo de suporte do aplicativo ou o fornecedor do software.

**Importante**  Embora o sequenciador Capture as ACLs de NTFS ao monitorar a fase de instalação do sequenciamento, ele não captura as ACLs para o registro. Os usuários têm acesso total a todas as chaves do registro para aplicativos virtuais, exceto para serviços. No entanto, se um usuário modificar o registro de um aplicativo virtual, essa alteração será armazenada em um local específico ( `uservol_sftfs_v1.pkg` ) e não afetará outros usuários.

 

Durante a fase de instalação, um engenheiro de sequenciamento pode modificar as permissões padrão dos arquivos, se necessário. Depois que o processo de sequenciamento estiver concluído, mas antes de salvar o pacote, o engenheiro de sequenciamento poderá optar por impor descritores de segurança que foram capturados durante a fase de instalação. É uma prática recomendada forçar descritores de segurança se nenhuma outra solução permitir que o aplicativo seja executado corretamente quando virtualizado.

 

 





