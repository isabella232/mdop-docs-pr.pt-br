---
title: Considerações sobre segurança para o DaRT 10
description: Considerações sobre segurança para o DaRT 10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799195"
---
# Considerações sobre segurança para o DaRT 10


Este tópico contém uma breve visão geral sobre as contas e grupos, arquivos de log e outras considerações relacionadas à segurança do Microsoft Diagnostics e do conjunto de ferramentas de recuperação (DaRT) 10. Para obter mais informações, siga os links neste artigo.

## Considerações gerais sobre segurança


**Compreender os riscos de segurança**. O DaRT 10 inclui funcionalidade que permite que um administrador ou um trabalho de suporte técnico execute as ferramentas do DaRT remotamente para resolver problemas em um computador de usuário final. Além disso, você pode salvar a imagem ISO (International Organization for Standardization) em uma unidade flash USB ou colocar a imagem ISO em uma rede para incluir seu conteúdo como uma partição de recuperação no disco rígido de um computador. Esses recursos oferecem flexibilidade, mas também podem criar possíveis riscos de segurança que você deve considerar ao configurar o DaRT.

**Proteja seus computadores fisicamente**. Quando os administradores e os funcionários do suporte técnico não estão fisicamente em seus computadores, eles devem bloquear seus computadores e usar um protetor de tela seguro.

**Aplicar as atualizações de segurança mais recentes a todos os computadores**. Mantenha-se informado sobre novas atualizações para sistemas operacionais assinando o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

## Limitar o acesso do usuário final às ferramentas do DaRT


Ao criar a imagem de recuperação do DaRT, você pode selecionar as ferramentas que deseja incluir. Por motivos de segurança, talvez você queira restringir o acesso do usuário final às ferramentas do DaRT mais poderosas, como apagamento de disco e locksmith. No DaRT 10, você pode desabilitar determinadas ferramentas durante a configuração e ainda disponibilizá-las para trabalhadores do suporte técnico quando o usuário final iniciar o recurso de conexão remota.

Você pode até mesmo configurar a imagem DaRT para que a opção de iniciar uma sessão de conexão remota seja a única ferramenta disponível para um usuário final.

**Importante**  Depois que a conexão remota for estabelecida, todas as ferramentas que você incluiu na imagem de recuperação, incluindo aquelas que não estão disponíveis para o usuário final, ficarão disponíveis para qualquer trabalho de suporte técnico que esteja trabalhando no computador do usuário final.

 

Para obter mais informações sobre como incluir ferramentas na imagem de recuperação do DaRT, consulte [visão geral das ferramentas no DART 10](overview-of-the-tools-in-dart-10.md).

## Proteger a imagem de recuperação do DaRT


Se você implantar a imagem de recuperação do DaRT salvando-a em uma unidade flash USB ou criando uma partição remota ou uma partição de recuperação, talvez queira incluir o método preferido de criptografia de unidade da sua empresa no ISO. A criptografia da ISO ajuda a garantir que os usuários finais não possam usar a funcionalidade do DaRT se tivessem acesso à imagem de recuperação e garante que os usuários não autorizados não possam inicializar o DaRT em computadores que pertençam a outra pessoa. Se você usar um método de criptografia, certifique-se de implantá-lo e habilitá-lo em todos os computadores.

**Observação**  O DaRT 10 é compatível com o BitLocker nativamente.

 

Para incluir a criptografia de unidade, adicione os arquivos de solução de criptografia ao criar a imagem de recuperação. Sua solução de criptografia deve ser capaz de ser executada no WinPE. Os usuários finais que inicializam a partir da ISO poderão acessar a solução de criptografia e desbloquear a unidade.

## Manter a segurança entre dois computadores quando você usa a conexão remota


Por padrão, a comunicação entre dois computadores que estabeleceram uma sessão de **conexão remota** pode não ser criptografada. Portanto, para ajudar a manter a segurança entre os dois computadores, recomendamos que ambos os computadores façam parte da mesma rede.

## Tópicos relacionados


[Segurança e privacidade do DaRT 10](security-and-privacy-for-dart-10.md)

 

 





