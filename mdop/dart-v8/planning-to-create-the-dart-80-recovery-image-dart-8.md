---
title: Planejamento para criar a imagem de recuperação do DaRT 8.0
description: Planejamento para criar a imagem de recuperação do DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799546"
---
# Planejamento para criar a imagem de recuperação do DaRT 8.0


Use as informações desta seção quando estiver planejando criar a imagem de recuperação do Microsoft (Microsoft Diagnostics and Recovery Toolset) 8,0.

## Planejando criar a imagem de recuperação do DaRT 8,0


Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem. Para tomar a decisão, considere que os usuários finais podem ter acesso a essas ferramentas. Se os engenheiros de suporte adotarem a mídia de recuperação de imagem para os computadores dos usuários finais para diagnosticar problemas, talvez você queira instalar todas as ferramentas na imagem de recuperação. Se você planeja diagnosticar os computadores dos usuários finais remotamente, talvez queira desativar algumas das ferramentas, como apagamento de disco e editor do registro, e, em seguida, habilitar outras ferramentas, incluindo conexão remota.

Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais. Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.

Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md). Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DaRT 8,0](security-considerations-for-dart-80--dart-8.md).

## Pré-requisitos para a imagem de recuperação


Os seguintes itens são necessários ou recomendados para criar a imagem de recuperação do DaRT:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Pré-requisito</strong></p></td>
<td align="left"><p><strong>Detalhes</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivos de origem do Windows 8</p></td>
<td align="left"><p>Obrigatório para criar a imagem de recuperação do DaRT. Fornecer o caminho de um DVD do Windows 8 ou dos arquivos de origem do Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas de depuração do Windows para a sua plataforma</p></td>
<td align="left"><p>Obrigatório ao executar o <strong> Crash Analyzer </strong> para determinar a causa de uma falha no computador. Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT. Você pode baixar as ferramentas de depuração do Windows aqui: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> baixar e instalar as ferramentas de depuração para Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opcional: <strong> definições do defender </strong></p></td>
<td align="left"><p>As definições mais recentes para o <strong> defender </strong> são necessárias ao executar o <strong> defender </strong> . Embora você possa baixar as definições ao executar o <strong> defender </strong> , recomendamos baixar as definições mais recentes no momento em que cria a imagem de recuperação do DART para que você ainda possa executar a ferramenta com as definições mais recentes mesmo que o computador com problema não tenha conectividade de rede.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional: Arquivos de símbolos do Windows para uso com o <strong> Crash Analyzer</strong></p></td>
<td align="left"><p>Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do programa. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele parou de funcionar. Para obter mais informações, consulte <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnosticar falhas do sistema com o Crash Analyzer </a> .</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejamento da implantação do DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





