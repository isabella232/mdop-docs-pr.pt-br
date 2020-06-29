---
title: Planejamento da implementação do Application Virtualization Sequencer
description: Planejamento da implementação do Application Virtualization Sequencer
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796816"
---
# Planejamento da implementação do Application Virtualization Sequencer


O uso do sequenciamento, o processo usado pela virtualização de aplicativos para criar aplicativos virtuais e pacotes de aplicativos, requer o uso de um computador com o software sequenciador do Application Virtualization instalado.

Durante o processo de sequenciamento, o sequenciador é colocado no modo de monitor, e o aplicativo a ser sequenciado é instalado no computador de sequenciamento. Em seguida, o aplicativo sequenciado é iniciado, e suas funções mais importantes e comumente usadas são exercidas para que o processo de monitoramento possa configurar o bloco de recursos principal, que contém o conteúdo mínimo em um pacote de aplicativo necessário para a execução de um aplicativo. Quando essas etapas forem concluídas, o modo de monitoramento será interrompido e o aplicativo sequenciado será salvo e testado para verificar a operação correta.

Ao decidir quais aplicativos escolher para o sequenciamento, lembre-se de que determinados aplicativos não podem ser sequenciados. Isso inclui certas partes do sistema operacional Windows, como Internet Explorer, drivers de dispositivo e aplicativos que iniciam serviços no momento da inicialização.

Para obter informações passo a passo sobre como instalar o sequenciador, consulte [como instalar o Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).

**Importante**  O plano de processo de sequenciamento completo deve ser revisado e aprovado pela equipe de segurança da sua empresa. As operações do sequenciador geralmente são mantidas separadas do ambiente de produção em um laboratório. Isso pode ser tão simples ou tão abrangente quanto necessário, de acordo com suas necessidades de negócios. Os computadores de sequenciamento precisarão de conectividade com a rede corporativa para copiar pacotes concluídos para os servidores de produção. No entanto, como elas são geralmente operadas sem proteção antivírus, elas não devem estar desprotegidas da rede corporativa, por exemplo, você pode ser capaz de operar atrás de um firewall ou de um segmento de rede isolado. O uso de máquinas virtuais configuradas para compartilhar uma rede virtual isolada também pode ser uma abordagem aceitável. Siga as políticas de segurança da sua empresa para solucionar essa situação com segurança.

 

As etapas principais para planejar o processo de sequenciamento incluem o seguinte:

-   Considere o número de aplicativos que você espera processar todos os meses, o tamanho desses aplicativos e adicionar uma bonificação para o sequenciamento de atualizações futuras. Os pacotes podem ter até 4 GB de tamanho, compactados ou descompactados.

-   Prepare e documente um processo repetível e repetível para sua organização acompanhar ao sequenciar cada aplicativo. Isso deve incluir o uso de uma lista de verificação para cada execução, bem como um processo de controle de versão. O uso de um log de rastreamento para cada aplicativo sequenciado também é muito útil ao investigar possíveis problemas técnicos com um pacote.

-   Para aplicativos de sequenciamento, use computadores de alto desempenho que são otimizados para o processamento de throughput, com pelo menos 4 GB de RAM e uma CPU rápida (3 GHz ou mais). Discos rígidos rápidos e o uso de volumes de disco separados também podem melhorar o desempenho. Máquinas virtuais são ideais para o sequenciamento porque podem ser facilmente redefinidas ou você pode usar um computador físico com uma imagem limpa em uma partição local para habilitar a criação rápida de uma nova geração de imagens após a conclusão de cada operação de sequenciamento do pacote.

    **Importante**  Não há suporte para a execução do sequenciador App-V no modo de segurança.

     

-   Verifique se você compreende o ambiente operacional do aplicativo sequenciado, incluindo elementos de integração, como o Microsoft Office ou o Java Runtime Environment, pois isso geralmente determinará se algo deve ser instalado no computador de sequenciamento antes de sequenciar o aplicativo.

-   Certifique-se de que cada nova operação de sequenciamento sempre comece com uma imagem base limpa. Certifique-se de que o computador de sequenciamento foi redefinido, restaurando a imagem salva em um computador físico ou reiniciando uma máquina virtual após descartar todas as alterações. A imagem base deve ter as atualizações mais recentes aplicadas do Windows Update antes de salvar.

-   Desative qualquer coisa no computador de sequenciamento que possa interferir no processo de monitoramento de instalação, tais scanners de antivírus e Windows Update, pois ter uma plataforma estável durante o processo de sequenciamento é essencial. Como essa etapa provoca sérios riscos de segurança, certifique-se de que as precauções corretas sejam tomadas para proteger o computador e a rede, bem como o pacote de aplicativo sequenciado. Recomendamos que você faça uma verificação antivírus dos pacotes de aplicativos antes de sequenciará-los.

-   Inclua um processo detalhado para testar cada aplicativo após o sequenciamento. Testar o aplicativo sequenciado determinará se ele funciona corretamente e é uma parte essencial do processo antes de implantar o aplicativo virtualizado para usuários finais. Como a etapa final do teste antes da implantação em larga escala para usuários finais, você também deve planejar uma implantação piloto para um grupo de teste.

-   Ao testar aplicativos sequenciados, escolha equipamento de computador do mesmo tipo e executando os mesmos sistemas operacionais que estão em uso no ambiente de produção da empresa. Desde que estejam configurados corretamente, é possível usar máquinas virtuais ou computadores físicos.

## Tópicos relacionados


[Requisitos de Hardware e Software do Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Como instalar o Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Como fazer upgrade do Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Visão geral de segurança e proteção](security-and-protection-overview.md)

 

 





