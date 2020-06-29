---
title: Planejamento para criar a imagem de recuperação do DaRT 10
description: Planejamento para criar a imagem de recuperação do DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799180"
---
# Planejamento para criar a imagem de recuperação do DaRT 10


Use as informações desta seção quando estiver planejando criar uma imagem de recuperação do Microsoft DaRT (Microsoft Diagnostics and Recovery Toolset) 10.

## Planejando criar a imagem de recuperação do DaRT 10


Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem. Para tomar a decisão, considere que os usuários finais podem ter acesso a essas ferramentas. Se os engenheiros de suporte adotarem a mídia de recuperação de imagem para os computadores dos usuários finais para diagnosticar problemas, talvez você queira instalar todas as ferramentas na imagem de recuperação. Se você planeja diagnosticar os computadores dos usuários finais remotamente, talvez queira desativar algumas das ferramentas, como apagamento de disco e editor do registro, e, em seguida, habilitar outras ferramentas, incluindo conexão remota.

Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais. Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.

Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DART 10](overview-of-the-tools-in-dart-10.md). Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DART 10](security-considerations-for-dart-10.md).

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
<td align="left"><p>Arquivos de origem do Windows 10</p></td>
<td align="left"><p>Obrigatório para criar a imagem de recuperação do DaRT. Forneça o caminho de um DVD do Windows 10 ou de arquivos de origem do Windows 10.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas de depuração do Windows para a sua plataforma</p></td>
<td align="left"><p>Obrigatório ao executar o <strong> Crash Analyzer </strong> para determinar a causa de uma falha no computador. Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT. Você pode baixar as ferramentas de depuração do Windows aqui: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> baixar e instalar as ferramentas de depuração para Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opcional: Arquivos de símbolos do Windows para uso com o <strong> Crash Analyzer</strong></p></td>
<td align="left"><p>Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do programa. Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele parou de funcionar. Para obter mais informações, consulte <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnosticar falhas do sistema com o Crash Analyzer </a> .</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados

[Planejamento da implantação do DaRT 10](planning-to-deploy-dart-10.md)

 

 




