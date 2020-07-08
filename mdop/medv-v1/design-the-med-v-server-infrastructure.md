---
title: Projetar a infraestrutura de servidor do MED-V
description: Projetar a infraestrutura de servidor do MED-V
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799421"
---
# Projetar a infraestrutura de servidor do MED-V


Neste tópico, você criará a infraestrutura do servidor para cada instância do MED-V. Isso inclui determinar se a instância do SQL Server existirá no servidor MED-V ou em um servidor remoto, bem como o tamanho do banco de dados do SQL Server. Você também irá determinar a localização do console de gerenciamento.

## Projetar e colocar o servidor para cada instância do MED-V


O servidor MED-V implementa políticas e armazena dados do estado e do histórico de seus clientes.

### Fator forma

O MED-V recomenda o uso de um servidor de CPU dual core de 2,8 GHz com 2 GB de RAM. Essa recomendação se baseia na pressuposição de que o servidor MED-V será executado em uma máquina dedicada e que o SQL Server e o console de gerenciamento do MED-V serão executados em máquinas separadas.

Dada essa carga de trabalho, o servidor MED-V deve ser relativamente levemente carregado. Na ausência de orientação arquitetônica específica no fator forma do servidor, projete o servidor usando a recomendação do MED-V, com memória que corresponde ao fator forma padrão da organização. O servidor MED-V pode ser executado em uma máquina virtual (VM) no Windows Server2008 o Hyper-V. Se uma VM for usada, verifique se ela tem acesso aos recursos de memória e CPU equivalentes aos especificados para um computador físico.

A capacidade de disco que o servidor MED-V exige deve ser suficiente para armazenar os arquivos de configuração do espaço de trabalho do MED-V. Um espaço de trabalho do MED-V só pode usar uma VM e uma política para um ou mais usuários. Portanto, o número de espaços de trabalho do MED-V que devem ser armazenados depende do grau em que políticas diferentes são necessárias para usuários diferentes da mesma VM, bem como o número de VMs que serão usadas. Os arquivos XML do espaço de trabalho do MED-V têm cerca de 30KB em tamanho para um espaço de trabalho do MED-V típico. Para determinar a capacidade de disco necessária, multiplique 30 KB pelo número de espaços de trabalho do MED-V que o servidor MED-V irá armazenar.

As conexões de rede mais importantes do servidor MED-V são os links para seus clientes, portanto, coloque o servidor em um local de rede que forneça a largura de banda mais disponível e os links mais robustos para seus clientes.

### Tolerância a falhas

Só pode haver um servidor ativo do MED-V em uma instância do MED-V, e o MED-V não inclui recursos padrão para colocar o servidor em um cluster do Microsoft Cluster Server (MSCS) para fornecer tolerância a falhas. Um servidor de backup passivo pode ser configurado manualmente.

Para decidir se um servidor de backup passivo deve ser configurado manualmente para a instância do MED-V, determine se os usuários terão permissão para usar as imagens do MED-V no modo offline. Para saber mais sobre o modo offline, confira [como configurar um usuário ou grupo de domínio](how-to-configure-a-domain-user-or-groupmedvv2.md). Se os usuários não têm permissão para trabalhar offline, eles não poderão continuar a trabalhar no caso de uma falha do servidor MED-V, mesmo se o espaço de trabalho do MED-V já tiver sido iniciado no cliente. Se o trabalho offline for permitido, para cada espaço de trabalho do MED-V, determine por quanto tempo o cliente tem permissão para trabalhar offline antes de ser autenticado. Esta é a quantidade máxima de tempo que o servidor pode ficar indisponível.

## Criar e colocar o banco de dados do SQL Server


O servidor MED-V usa o banco de dados do SQL Server para armazenar o status e os eventos do cliente. Você pode instalar o banco de dados do SQL Server no mesmo computador que o servidor do MED-V ou pode colocá-lo em um servidor separado que executa o SQL Server, que pode ser opcionalmente remoto. Você pode compartilhar o banco de dados com outras instâncias do MED-V, e, nesse caso, os eventos e alertas dessas instâncias serão armazenados no mesmo banco de dados, e os relatórios incluirão eventos de todas as instâncias. Você pode instalar o banco de dados em uma instância existente do SQL Server, e os bancos de dados de outros servidores MED-V podem residir na mesma instância.

Se você colocar o servidor de banco de dados em um local remoto do servidor MED-V, entre links de redes que não têm largura de banda suficiente disponível, os relatórios podem ser lentos para carregar no console e podem não exibir os dados mais recentes dos clientes. Consulte as expectativas de nível de serviço da organização que você especificou em [definir o escopo do projeto](define-the-project-scope.md) e use essas informações para decidir onde colocar o banco de dados do SQL Server.

### Fator forma

Se você executar o SQL Server no mesmo servidor do MED-V, e se o SQL Server só será usado para armazenar dados para esse servidor, comece com a recomendação do MED-V e adicione recursos para a carga do SQL Server. Se o SQL Server armazenar eventos e alertas de mais de uma instância do MED-V, para obter informações sobre como redimensionar o fator forma do servidor, consulte o guia [planejamento e design da infraestrutura Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) (http://go.Microsoft.com/fwlink/?linkid=163302).

O tamanho do banco de dados depende do número de eventos do cliente que o banco de dados armazenará. Os eventos são criados pela operação normal do cliente, como quando um espaço de trabalho do MED-V é iniciado ou quando há um erro no espaço de trabalho do MED-V. O intervalo padrão no qual o cliente envia eventos é de 1 minuto.

Para estimar o tamanho do banco de dados, determine o seguinte:

-   Número de clientes na instância do MED-V. O máximo é 5.000.

-   Taxa de chegada de eventos típico. Essa taxa depende do comportamento de uso do cliente, mas é de aproximadamente 15 a 20 eventos por dia por cliente.

-   Tamanho do evento. O tamanho geralmente está em torno de 200 bytes.

-   Valor do armazenamento. O número de dias durante os quais os eventos serão armazenados.

Multiplique esses valores em conjunto para calcular o tamanho do armazenamento de dados necessário em bytes e, em seguida, adicionar um fator de segurança à conta para o seguinte:

-   Erros, que podem criar um grande número de eventos de um cliente em um curto período de tempo.

-   Tabela de banco de dados e espaço organizacional.

Para aproximar a necessidade de acordo com a otimização da infraestrutura por segundo (IOPs), use os valores acima, multiplicando a taxa de chegada do evento típico pelo número de clientes na instância. Isso gera o número de registros que podem ser gravados por dia. Divida esse número por 86.400 para derivar o número de registros gravados por segundo. Se as operações de gravação puderem ser equacionadas com uma única operação de otimização de infraestrutura (e/s), esse número será o IOPs de gravação necessário. Adicione um buffer para a atividade de relatório. Isso é difícil de determinar, mas depende do número de consoles em uso com a instância e a frequência com a qual elas são usadas para gerar relatórios.

### Tolerância a falhas

Quando o cliente MED-V estiver em execução, se o servidor não estiver disponível, o backup dos eventos será feito no cliente e os relatórios não estarão disponíveis no console de gerenciamento. Consulte as expectativas de nível de serviço da organização determinadas em [definir o escopo do projeto](define-the-project-scope.md) para decidir se o design de uma infraestrutura do SQL Server tolerante a falhas é necessário.

O MED-V não oferece suporte para a execução do SQL Server em um cluster do MSCS. Para fornecer espera passiva e evitar perda de dados em caso de falha, você pode colocar o SQL Server em uma configuração de envio de log. Para obter informações sobre o envio de logs, consulte o guia [planejamento e design de infraestrutura do Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) ( https://go.microsoft.com/fwlink/?LinkId=163302) .

## Projetar o console de gerenciamento


Parte da funcionalidade do console de gerenciamento do MED-V é testar as VMs antes de serem empacotadas para distribuição para clientes MED-V. Portanto, o console de gerenciamento deve ser projetado com um fator forma semelhante ao mais próximo possível, o fator forma de um computador cliente médio-V típico.

O aplicativo console de gerenciamento é instalado em conjunto com o cliente MED-V e usa o Microsoft Virtual PC2007 SP1 com o hotfix descrito no artigo 974918 da base de dados de conhecimento da Microsoft. Um sistema operacional cliente deve ser usado; o console de gerenciamento do MED-V não pode ser executado no mesmo sistema do servidor MED-V.

Você não pode compartilhar um console de gerenciamento com várias instâncias do servidor MED-V. O endereço do servidor MED-V é especificado durante a instalação do cliente MED-V do console de gerenciamento; Isso pode ser alterado após a instalação, mas, a qualquer momento, o console de gerenciamento só pode funcionar com um único servidor MED-V.

Você pode usar vários consoles de gerenciamento com um único servidor MED-V. Para evitar conflitos, um mecanismo está disponível que notifique outros usuários do console quando um console tiver feito alterações em um espaço de trabalho do MED-V.

Para cada instância do MED-V, determine quantos consoles de gerenciamento serão necessários e onde serão colocados. Selecione um fator de forma de cliente MED-V típico para ser usado para o console de gerenciamento.

## Tópicos relacionados


[Configurações com suporte no MED-V 1.0 SP1](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[Configurando o servidor do MED-V para o modo de cluster](configuring-med-v-server-for-cluster-mode.md)

[Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

 

 





