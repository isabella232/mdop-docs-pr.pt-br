---
title: Considerações sobre segurança para o DaRT 7.0
description: Considerações sobre segurança para o DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799131"
---
# Considerações sobre segurança para o DaRT 7.0


O Microsoft Diagnostics and Recovery Toolset (DaRT) 7 inclui funcionalidade que permite que um administrador execute as ferramentas do DaRT remotamente para resolver problemas em um computador de usuário final. Em versões anteriores do DaRT, um técnico ou administrador do suporte técnico tinha que estar fisicamente em um computador de usuário final e inicializar o DaRT usando o CD ou DVD que incluiu a imagem de recuperação do DaRT. Agora, o técnico da assistência técnica ou o administrador podem executar os mesmos procedimentos remotamente.

Além disso, no DaRT7, além de gravar um CD ou DVD, agora você pode salvar a imagem ISO (organização internacional de normalização) em uma unidade flash USB. Você também pode colocar a imagem ISO em uma rede ou incluir seu conteúdo como uma partição de recuperação em um disco rígido do computador.

O recurso **conexão remota** no DaRT7 permite que os usuários finais acessem o DART usando um desses métodos de implantação novos. Portanto, eles podem iniciar o DaRT com facilidade e acessar as ferramentas DaRT.

As novas funcionalidades no DaRT7 fornecem muito mais flexibilidade em como usar o DaRT na sua empresa. No entanto, eles também criam seu próprio conjunto de problemas de segurança que devem ser resolvidos. Recomendamos que você considere as seguintes dicas de segurança ao configurar o DaRT.

## Para ajudar a manter a segurança ao criar a imagem de recuperação do DaRT


Ao criar a imagem de recuperação do DaRT, você pode selecionar as ferramentas que deseja incluir. Por motivos de segurança, talvez você queira restringir o acesso do usuário final às ferramentas do DaRT mais poderosas, como apagamento de disco e locksmith. No DaRT7, você pode desabilitar determinadas ferramentas durante a configuração e ainda disponibilizá-las aos agentes do helpdesk quando o usuário final iniciar o recurso de conexão remota.

Você pode até mesmo configurar a imagem DaRT para que a opção de iniciar uma sessão de conexão remota seja a única ferramenta disponível para um usuário final.

**Importante**  Depois que a conexão remota for estabelecida, todas as ferramentas que você incluiu na imagem de recuperação, incluindo aquelas que não estão disponíveis para o usuário final, ficarão disponíveis para o agente de helpdesk trabalhando no computador do usuário final.

 

Para obter mais informações sobre como incluir ferramentas na imagem de recuperação do DaRT, consulte [como usar o assistente de imagem de recuperação do DART para criar a imagem de recuperação](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).

## Para ajudar a manter a segurança criptografando a imagem de recuperação do DaRT


Se você usar uma das opções de implantação novas no DaRT7, por exemplo, salvar em uma unidade flash USB ou criar uma partição remota ou uma partição de recuperação, poderá incluir o método preferido de criptografia de unidade da sua empresa na ISO. Isso ajudará a garantir que um usuário final não possa usar a funcionalidade do DaRT caso ele tenha acesso à imagem de recuperação. Além disso, ele também garantirá que os usuários não autorizados não possam inicializar o DaRT em computadores que pertençam a outra pessoa.

O método de criptografia deve ser implantado e habilitado em todos os computadores.

**Observação**  O DaRT7 é compatível com o BitLocker nativamente.

 

## Para ajudar a manter a segurança entre dois computadores durante a conexão remota


Por padrão, a comunicação entre dois computadores que estabeleceram uma sessão de **conexão remota** pode não ser criptografada. Portanto, para ajudar a manter a segurança entre os dois computadores, recomendamos que ambos os computadores façam parte da mesma rede.

## Tópicos relacionados


[Operações do DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





