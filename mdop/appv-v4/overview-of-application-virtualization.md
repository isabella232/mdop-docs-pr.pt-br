---
title: Visão geral do Application Virtualization
description: Visão geral do Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796850"
---
# Visão geral do Application Virtualization


O Microsoft Application Virtualization (App-V) pode disponibilizar aplicativos para os computadores dos usuários finais sem precisar instalar os aplicativos diretamente nesses computadores. Isso se tornou possível por meio de um processo conhecido como *sequenciamento do aplicativo, o*que permite que cada aplicativo seja executado em seu próprio ambiente virtual autocontido no computador cliente. Os aplicativos sequenciados são isolados uns dos outros. Isso elimina conflitos de aplicativos, mas os aplicativos ainda podem interagir com o computador cliente.

O cliente App-V é o recurso que permite que o usuário final interaja com os aplicativos após eles terem sido publicados no computador. O cliente gerencia o ambiente virtual no qual os aplicativos virtualizados são executados em cada computador. Após a instalação do cliente em um computador, os aplicativos devem ser disponibilizados para o computador por meio de um processo conhecido como *publicação*, o que permite que o usuário final execute os aplicativos virtuais. O processo de publicação copia os ícones do aplicativo virtual e os atalhos para o computador, geralmente na área de trabalho do Windows ou no menu **Iniciar** , e também copia as informações de definição do pacote e Associação de tipo de arquivo para o computador. A publicação também torna o conteúdo do pacote do aplicativo disponível para o computador do usuário final.

O conteúdo do pacote do aplicativo virtual pode ser copiado para um ou mais servidores de virtualização de aplicativos para que ele possa ser transmitido para os clientes sob demanda e armazenado localmente em cache. Os servidores de arquivos e os servidores Web também podem ser usados como servidores de streaming ou o conteúdo pode ser copiado diretamente para o computador do usuário final, por exemplo, se você estiver usando um sistema de distribuição de software eletrônico, como o Microsoft Endpoint Configuration Manager. Em uma implementação de vários servidores, manter o conteúdo do pacote e mantê-lo atualizado em todos os servidores de streaming requer uma solução de gerenciamento de pacotes abrangente. Dependendo do tamanho da sua organização, talvez seja necessário ter muitos aplicativos virtuais disponíveis para os usuários finais localizados em todo o mundo. Gerenciar os pacotes para garantir que os aplicativos apropriados estejam disponíveis para todos os usuários onde e quando precisarem acessá-los é, portanto, um requisito importante.

## Recursos do sistema do Microsoft Application Virtualization


A tabela a seguir descreve os principais recursos do sistema de gerenciamento do Microsoft Application Virtualization.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Recurso</th>
<th align="left">Função</th>
<th align="left">Informações adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de gerenciamento do Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsável por transmitir o conteúdo do pacote e publicar os atalhos e associações de tipo de arquivo para o cliente do Application Virtualization.</p></td>
<td align="left"><p>O servidor de gerenciamento do Application Virtualization dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pasta de conteúdo </strong></p></td>
<td align="left"><p>Indica o local dos pacotes do Application Virtualization para streaming.</p></td>
<td align="left"><p>Essa pasta pode ser localizada em um compartilhamento ou em um servidor de gerenciamento do Application Virtualization.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Console de gerenciamento do Microsoft Application Virtualization</p></td>
<td align="left"><p>Este console é uma ferramenta de gerenciamento de snap-in do MMC 3,0 usada para administração do Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Essa ferramenta pode ser instalada no servidor do Microsoft Application Virtualization ou em uma estação de trabalho separada que tenha o Microsoft Management Console (MMC) 3.0 e a Microsoft. NETFramework 2,0 instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsável por comunicar qualquer solicitação de leitura e gravação ao repositório de dados do Application Virtualization.</p></td>
<td align="left"><p>O serviço Web de gerenciamento pode ser instalado no servidor de gerenciamento do Microsoft Application Virtualization ou em um computador separado que tenha o Microsoft ISS (serviços de informações da Internet) instalado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Repositório de dados do Microsoft Application Virtualization</p></td>
<td align="left"><p>O banco de dados do aplicativo do SQL Server do App-V responsável por armazenar todas as informações relacionadas à infraestrutura de virtualização do aplicativo.</p></td>
<td align="left"><p>Essas informações incluem todos os registros de aplicativos, atribuições de aplicativos e quais grupos têm responsabilidade por gerenciar o ambiente de virtualização de aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming do Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsável pela hospedagem dos pacotes do Application Virtualization para transmitir para clientes em uma filial, em que o link de volta para o servidor de gerenciamento do Application Virtualization é considerado uma conexão de rede de longa distância.</p></td>
<td align="left"><p>Esse servidor contém somente a funcionalidade de streaming e não fornece o console de gerenciamento do Application Virtualization nem o serviço Web de gerenciamento da virtualização de aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciador do Microsoft Application Virtualization</p></td>
<td align="left"><p>O sequenciador é usado para monitorar e capturar a instalação de aplicativos para criar pacotes de aplicativos virtuais.</p></td>
<td align="left"><p>A saída consiste nos ícones do aplicativo, um arquivo. OSD que contém informações de definição do pacote, um arquivo de manifesto do pacote e o arquivo. sft que contém os arquivos de conteúdo do programa aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente do Microsoft Application Virtualization</p></td>
<td align="left"><p>O cliente da área de trabalho do Application Virtualization e o cliente do Application Virtualization para serviços de área de trabalho remota fornecem e gerenciam o ambiente virtual para aplicativos virtualizados.</p></td>
<td align="left"><p>O cliente do Microsoft Application Virtualization gerencia o fluxo de pacote no cache, a atualização de publicação, o transporte e todas as interações com os servidores do Application Virtualization.</p></td>
</tr>
</tbody>
</table>

 

 

 





