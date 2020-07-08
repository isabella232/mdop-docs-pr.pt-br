---
title: Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0
description: Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797886"
---
# Planejar como salvar e implantar a imagem de recuperação do DaRT 8.0


Você pode salvar e implantar a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 usando os métodos a seguir. Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um. Você também deve considerar sua infraestrutura e sua equipe de suporte. Se você tiver uma pequena infra-estrutura, talvez queira implantar o DaRT 8,0 usando mídia removível, pois a imagem de recuperação sempre estará disponível se você instalá-la no disco rígido local.

Se a sua organização usa os serviços de domínio Active Directory (AD DS), talvez você queira implantar imagens de recuperação como um serviço de rede usando o Windows DS. As imagens de recuperação sempre estão disponíveis para qualquer computador conectado. Você pode implantar várias imagens do Windows DS e mantê-las todas em um só lugar.

**Observação**  Talvez você queira usar mais de um método em sua organização. Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.

 

A tabela a seguir mostra algumas vantagens e desvantagens de cada método de usar o DaRT em sua organização.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método para inicializar o DaRT</th>
<th align="left">Vantagens</th>
<th align="left">Desvantagens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Mídia removível</strong></p>
<p>A imagem de recuperação é gravada em um CD, DVD ou unidade USB para permitir que a equipe de suporte leve as ferramentas de recuperação para o computador instável.</p></td>
<td align="left"><p>Dá suporte a cenários em que o registro de inicialização mestre (MBR) está corrompido e não é possível acessar o disco rígido e dá suporte a casos em que não há conexão de rede.</p>
<p>Permite que você crie várias imagens de recuperação com diferentes ferramentas para fornecer níveis diferentes de suporte.</p>
<p>Fornece uma ferramenta interna para gravar imagens de recuperação em mídias removíveis.</p></td>
<td align="left"><p>Requer que a equipe de suporte esteja fisicamente no computador do usuário final para inicializar o DaRT.</p>
<p>Requer tempo e manutenção para criar várias mídias com configurações diferentes para computadores de 32 bits e de 64 bits.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>De uma partição remota (rede)</strong></p>
<p>A imagem de recuperação está hospedada em um servidor de inicialização de rede, como os serviços de implantação do Windows (Windows DS), que permite que os usuários ou a equipe de suporte o transmitam para os computadores sob demanda.</p></td>
<td align="left"><p>Disponível para todos os computadores que têm acesso ao servidor de inicialização de rede.</p>
<p>As imagens de recuperação são hospedadas em um servidor central, o que permite atualizações centralizadas.</p>
<p>A equipe de suporte técnico centralizado pode fornecer reparos usando a conectividade remota.</p>
<p>Não há requisitos de armazenamento local nos clientes.</p>
<p>Capacidade de criar várias imagens de recuperação com diferentes ferramentas para níveis de suporte específicos.</p></td>
<td align="left"><p>A necessidade de proteger a infraestrutura do Windows DS para garantir que os usuários normais possam iniciar somente a imagem de recuperação do DaRT e não o processo completo de imagem do sistema operacional.</p>
<p></p>
<p></p>
<p>Requer que o computador do usuário final esteja conectado à rede em tempo de execução.</p>
<p>Requer que a imagem de recuperação seja trazida pela rede.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>De uma partição de recuperação na unidade de disco rígido local</strong></p>
<p>A imagem de recuperação é instalada em um disco rígido local manualmente ou por meio de sistemas de distribuição de software eletrônico, como o System Center Configuration Manager.</p></td>
<td align="left"><p>A imagem de recuperação está sempre disponível porque está em pré-teste no computador.</p>
<p>A equipe de suporte técnico centralizado pode oferecer suporte usando a conexão remota.</p>
<p>A imagem de recuperação é gerenciada de forma centralizada e implantada.</p>
<p>Outras solicitações de chave de recuperação em computadores protegidos por criptografia de unidade de disco BitLocker do Windows são eliminadas.</p></td>
<td align="left"><p>O armazenamento local é necessário.</p>
<p>Uma partição não criptografada e dedicada para posicionamento de imagens de recuperação é recomendada para reduzir o risco de uma partição de inicialização com falha.</p>
<p>Ao atualizar o DaRT, você deve atualizar todos os computadores na sua empresa, em vez de apenas uma partição (na rede) ou dispositivo removível.</p>
<p>Será necessária uma consideração adicional se você implantar a imagem de recuperação após o BitLocker ter sido habilitado.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejamento da implantação do DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





