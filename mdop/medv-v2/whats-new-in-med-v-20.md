---
title: Novidades da MED-V 2.0
description: Novidades da MED-V 2.0
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799325"
---
# Novidades da MED-V 2.0


A virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 evoluiu o suporte de compatibilidade do aplicativo para o Windows 7 e removeu a funcionalidade que não é necessária para esse cenário. Por exemplo, recursos como criptografia do espaço de trabalho do MED-V, o servidor do MED-V centralizado e a transferência de corte do espaço de trabalho do MED-V foram removidos.

## Alterações na funcionalidade padrão


Esta seção discute as principais áreas nas quais a funcionalidade do MED-V 2,0 mudou.

### Criação do espaço de trabalho do MED-V

O disco rígido virtual usado para o espaço de trabalho do MED-V agora é criado no PC virtual do Windows. Os métodos que são usados para criar o espaço de trabalho do MED-V incluem a instalação do Windows XP SP3, a atualização do sistema operacional e a preparação dele para serem gerenciados por meio da infraestrutura de gerenciamento de software.

As funcionalidades de gerenciamento offline e transferência de corte foram removidas, além da funcionalidade de compactação e compactação do espaço de trabalho do MED-V proprietário. Quando você cria um espaço de trabalho do MED-V, um administrador deve preparar e configurar aplicativos e ferramentas de gerenciamento apropriados na imagem em vez de usar a ferramenta de preparação da máquina virtual fornecida no MED-V 1,0.

A execução do Sysprep na imagem do MED-V agora é necessária e validada durante a embalagem do espaço de trabalho do MED-V. O pacote do espaço de trabalho do MED-V fornece uma interface gráfica do usuário (GUI) que orienta o administrador por meio do processo de empacotamento. O console do MED-V 1,0 foi removido junto com a funcionalidade de gerenciamento de imagens, o gerenciamento de perfis do espaço de trabalho do MED-V e a necessidade de testar e criptografar os espaços de trabalho do MED-V.

### Implantação do espaço de trabalho do MED-V

Para implantar um espaço de trabalho do MED-V, um administrador pode tirar proveito de suas ferramentas eletrônicas de distribuição de software. O método de recebimento de cliente disponível no MED-V 1,0 foi removido e o espaço de trabalho do MED-V agora é fornecido usando métodos fora do MED-V. Os administradores podem tratar os espaços de trabalho do MED-V como fariam com qualquer outro pacote de aplicativos e podem agendar implantações e instalações do MED-V usando suas ferramentas e processos existentes. As instalações do MED-V podem ser implantadas silenciosamente e podem ser facilmente gerenciadas dentro de uma infra-estrutura existente de distribuição de software.

### Gerenciamento do espaço de trabalho do MED-V

O espaço de trabalho do MED-V no MED-V 2,0 se baseia em um disco rígido virtual do Windows Virtual PC. O MED-V ampliou os recursos que o Windows Virtual PC oferece ao melhorar a experiência perfeita sem exigir criptografia ou ferramentas especiais para acessar o espaço de trabalho do MED-V.

Após a implantação do MED-V em uma estação de trabalho, o espaço de trabalho do MED-V pode ser aberto em modo de tela inteira usando o PC virtual do Windows. Essa nova funcionalidade removeu a necessidade de políticas que definem uma preferência para modos de tela inteira ou contínua e também removemos a necessidade de forçar o diagnóstico e a solução de problemas em tela cheia.

A publicação de aplicativos no espaço de trabalho do MED-V não é mais realizada com perfis e digitando manualmente o caminho para os aplicativos. Em vez disso, ocorre automaticamente à medida que os aplicativos são instalados no convidado. O repositório de imagens central que incluiu versões das imagens que foram entregues por meio da transferência de corte foi removida. Em vez disso, o MED-V permite que os administradores gerenciem o espaço de trabalho do MED-V da mesma forma que seriam um computador físico, permitindo que aplicativos e atualizações sejam distribuídos sem a complexidade de uma infraestrutura MED-V dedicada.

## Alterações em recursos do MED-V


Diversas áreas importantes do MED-V 2,0 refletem melhorias ou adições aos recursos a seguir.

### Criação do espaço de trabalho do MED-V

Os espaços de trabalho do MED-V devem ser criados usando o PC virtual do Windows. As imagens do Virtual PC 2007 existentes devem ser migradas. A ferramenta de preparação da máquina virtual não está incluída no MED-V 2,0 e os administradores devem configurar, atualizar e otimizar suas imagens de acordo com o arquivo de ajuda do MED-V 2,0. A execução de Sysprep na imagem do MED-V é uma etapa obrigatória e deve ser realizada antes da compactação.

### Pacote de espaço de trabalho do MED-V

O Windows PowerShell é a base do pacote do espaço de trabalho do MED-V. Essa funcionalidade substitui algumas funcionalidades e funcionalidades de console antigas que gerenciaram funções centralizadas do MED-V. O pacote do espaço de trabalho do MED-V simplesmente empacota o disco rígido virtual com as configurações e a imagem adequadas para que ele possa ser facilmente implantado por administradores. Recursos avançados são fornecidos usando o Windows PowerShell.

### Distribuição do espaço de trabalho do MED-V

A infraestrutura de servidor dedicada não é mais necessária para o MED-V 2,0, e o método de recepção do cliente para implantar os espaços de trabalho do MED-V foi removido. Os espaços de trabalho do MED-V agora são implantados usando sua infraestrutura de distribuição de software eletrônico e podem ser armazenados em compartilhamentos comuns que são usados para outros pacotes de instalação.

### Configuração da primeira vez

O processo de configuração da primeira vez agora está integrado à Convenção de imagens padrão do Sysprep. O processo de configuração da primeira vez do espaço de trabalho do MED-V espaço de trabalho pode aplicar dinamicamente as configurações especificadas no pacote do espaço de trabalho do MED-V à imagem, pois ela começa com a mini-configuração. A ferramenta de script no console foi removida e a primeira vez que o processo de configuração agora se baseia nas opções configuradas no pacote do espaço de trabalho do MED-V pelo administrador.

### Publicação de aplicativos

Os administradores podem instalar aplicativos na imagem do MED-V antes da embalagem, após a implantação do espaço de trabalho do MED-V ou usando uma combinação de ambos. O MED-V não examina mais a política do espaço de trabalho do MED-V para publicar aplicativos, mas em vez disso, se refere ao que realmente está instalado no convidado. À medida que os aplicativos são instalados no convidado, eles são automaticamente detectados e publicados no menu **Iniciar** do host e estão prontos para serem iniciados pelo usuário final.

### Redirecionamento de URL

O MED-V 2,0 oferece o redirecionamento de endereço da Web do host para convidado sem problemas com base nas políticas configuradas e gerenciadas pelo administrador. Após a redirecionamento de uma URL para o navegador convidado, a experiência padrão é tentar limitar o usuário ao site redirecionado. Isso minimiza as atividades de navegação que um usuário pode executar que não são direcionadas ao administrador. O redirecionamento do navegador convidado para host foi removido.

### Solução de problemas

Agora, o MED-V aproveita os processos padrão baseados em host para solução de problemas. Como o espaço de trabalho do MED-V não está mais criptografado, ele pode ser aberto em modo de tela inteira dentro do console do Windows Virtual PC, onde ele pode ser visualizado e trabalhado com uma estação de trabalho padrão. Além disso, os logs não são mais criptografados localmente e registrados de forma centralizada. O MED-V agora faz uso extensivo dos logs de eventos locais, e o nível de log da saída, de informativas aos níveis de depuração, pode ser facilmente configurado. Por fim, um kit de ferramentas para solução de problemas agora é fornecido para que os administradores e a equipe de assistência técnica possam ter uma exibição gráfica e agregada de todas as opções de solução de problemas, e podem facilmente selecionar as atividades que mais atendam às suas necessidades.

O MED-V não é mais executado como um serviço do sistema. Em vez disso, ele é executado como processos de Propriedade do usuário e só é executado quando um usuário está conectado.A funcionalidade fornecida anteriormente pelo serviço de Propriedade do sistema agora é fornecida nos processos do lado do usuário.

## Tópicos relacionados


[Implantação da MED-V](deployment-of-med-v.md)

[Operações da MED-V](operations-for-med-v.md)

 

 





