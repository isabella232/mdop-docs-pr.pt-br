---
title: Planejamento da compatibilidade do sistema operacional para aplicativos
description: Planejamento da compatibilidade do sistema operacional para aplicativos
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799678"
---
# Planejamento da compatibilidade do sistema operacional para aplicativos


Este tópico ajuda a determinar como resolver problemas de compatibilidade do sistema operacional do aplicativo e discute como a virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 funciona como uma solução para a sua organização.

Este tópico discute os requisitos comerciais do MED-V e compara o MED-V ao modo Windows XP e ao Microsoft Application Virtualization (App-V):

-   [Requisitos comerciais para o MED-V](#bkmk-whenmedv)

-   [Benefícios do MED-V em relação ao modo Windows XP](#bkmk-medvvsxp)

-   [Benefícios do MED-V versus App-V](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a>Requisitos comerciais para o MED-V


Quando o departamento de ti da sua empresa está determinando se deseja atualizar para o Windows 7, ele deve prestar atenção aos seus aplicativos de linha de negócios e aplicativos de linha de negócios baseados na Web para garantir que eles possam ser executados no novo sistema operacional. Geralmente, esses aplicativos e URLs foram criados para funcionar especificamente com uma versão mais antiga do Windows ou Internet Explorer, e podem ocorrer problemas quando você tenta usá-los no novo sistema operacional. A Microsoft oferece muitos métodos diferentes para manipular os vários problemas de compatibilidade que podem ocorrer quando você atualiza, como o Application Compatibility Toolkit (ACT) e o assistente de compatibilidade de programas do Windows 7. Mas mesmo depois que todos os aplicativos tiverem sido testados quanto à compatibilidade e correções forem determinados, alguns aplicativos ainda não funcionarão corretamente no Windows 7 ou são muito dispendiosos para serem resolvidos.

Ao usar o MED-V, você pode executar esses aplicativos herdados por meio de um ambiente de PC virtual do Windows executando o Windows XP. Como você não precisa mais testar e validar esses aplicativos de problemas no novo sistema operacional antes da atualização, a migração para o Windows 7 é muito mais fácil e rápida.

### Usando a lista de verificação do MED-V

Considere o MED-V se qualquer um dos seguintes cenários se aplicarem a você:

-   Você é uma organização de grande porte (por exemplo, 500 usuários e mais), ter um contrato empresarial com a Microsoft e planejar a atualização para o Windows 7.

-   Você testou seus aplicativos de linha de negócios e encontrou alguns que são incompatíveis com o Windows 7.

-   Você resolveu os problemas de compatibilidade para alguns desses aplicativos problemáticos atualizando o aplicativo ou usando um Shim fornecido pela Microsoft, como o kit de ferramentas de compatibilidade de aplicativos (ACT), mas os problemas de compatibilidade permanecem para alguns aplicativos.

-   Você considerou o App-V como uma opção para fornecer os aplicativos incompatíveis e concluiu que, mesmo depois de implementar o App-V, você ainda tem problemas de compatibilidade do sistema operacional do aplicativo que você deve resolver.

-   Você considerou o modo Windows XP como uma solução e determinou que essa não é uma opção eficiente porque:

    -   Você deseja poder implantar imagens virtuais que contenham os aplicativos de problemas para todos os usuários finais ao mesmo tempo, em vez de individualmente e ter as imagens virtuais automaticamente associadas ao domínio.

    -   Você decidiu que é muito mais econômico gerenciar esses aplicativos herdados (que são entregues virtualmente) e controlar as configurações do Windows Virtual PC de um local centralizado, em vez de cada área de trabalho do usuário final.

    -   Você deseja poder atualizar e dar suporte a máquinas virtuais em escala em vez de por área de trabalho.

    -   Você deseja a capacidade de redirecionar URLs executadas melhor em uma versão mais antiga do Internet Explorer para as máquinas virtuais e gerenciar facilmente o redirecionamento de URL mais tarde.

-   Você determinou que seria mais econômico e útil fazer a atualização para o Windows 7 o mais breve possível e decidiu adiar a solução de problemas de compatibilidade de aplicativos restantes até uma data posterior, sabendo que você tem uma solução disponível no MED-V.

## <a href="" id="bkmk-medvvsxp"></a> Benefícios do MED-V em relação ao modo Windows XP


O Windows Virtual PC para Windows 7 permite que você execute versões diferentes de um sistema operacional ao mesmo tempo em um único dispositivo e está incluído no Windows 7 Professional Edition e versões mais recentes.

A funcionalidade do modo do Windows XP aproveita o PC virtual do Windows fornecendo uma imagem pré-configurada do Windows XP que permite criar um ambiente virtual do Windows XP. Nesse ambiente virtual, você pode instalar manualmente os aplicativos que são incompatíveis com o Windows 7 e que sejam executados diretamente de sua área de trabalho por meio do PC virtual do Windows.

**Usando o modo Windows XP, você pode fazer o seguinte:**

-   Executar aplicativos compatíveis com o Windows XP dentro de uma máquina virtual que é executada no PC virtual do Windows.

-   Publicar esses aplicativos no menu da área de trabalho ou do programa do host.

Quando quiser fornecer essas máquinas virtuais em uma escala grande, como parte de uma migração empresarial para o Windows 7, você deve ser capaz de implantar as máquinas virtuais rapidamente, provisionar e personalizá-las com eficiência, controlar suas configurações e dar suporte a elas com facilidade.

O MED-V se baseia no modo Windows XP para oferecer compatibilidade de aplicativos em toda a empresa. Enquanto o modo Windows XP está limitado a fornecer funcionalidade de aplicativo virtual para indivíduos e pequenas empresas, o MED-V permite implantações em larga escala de imagens pré-configuradas do Windows XP em toda a sua rede corporativa. Ele oferece uma solução de gerenciamento pronto para empresas para a configuração, a implantação e a manutenção desses espaços de trabalho virtuais do MED-V. O MED-V também oferece ao enterpriseadministrators um conjunto de políticas para controlar o uso da imagem. Isso inclui quais usuários terão acesso a quais aplicativos específicos nessas imagens.

**Ao usar o MED-V, você pode fazer o seguinte:**

-   Atualize para seu novo sistema operacional sem precisar testar e resolver cada aplicativo e URL incompatíveis.

-   Implante imagens virtuais do Windows XP que sejam automaticamente integradas ao domínio e personalizadas por cada usuário.

-   Provisionar aplicativos e informações de redirecionamento de URL para os usuários.

-   Controlar as configurações do Windows Virtual PC.

-   Mantenha e dê suporte a pontos de extremidade por meio de monitoramento e solução de problemas.

-   Certifique-se de que os computadores convidados sejam corrigidos, mesmo se estiverem em um estado suspenso.

-   Automatizar a criação de máquinas virtuais por usuário e a inicialização de Sysprep.

-   Diagnostique problemas no host e nos computadores convidados facilmente.

-   Gerencie perfeitamente computadores convidados conectados por meio do modo NAT do Windows Virtual PC.

## <a href="" id="bkmk-medvvsappv"></a>Benefícios do MED-V versus App-V


O MED-V e o App-V são duas tecnologias muito diferentes que podem facilmente trabalhar em conjunto para resolver problemas de compatibilidade do sistema operacional do aplicativo. Ao usar o App-V, você cria um pacote individual para cada aplicativo, e cada um deles é mantido separadamente dos outros. Cada aplicativo virtual pode ser entregue imediatamente ao usuário final, o que é muito útil para uma estratégia de implantação do Windows 7.

O MED-V não manipula aplicativos individualmente. Em vez disso, ele cria uma instância adicional do Windows XP na mesma área de trabalho que está executando o Windows 7. Você pode instalar quantos aplicativos forem necessários para esta imagem virtual e gerenciar a imagem da mesma forma que faria com qualquer outro computador da sua organização.

Além disso, você pode usar o MED-V em conjunto com o App-V para que os aplicativos virtuais que são sequenciados por meio do App-V sejam instalados, publicados e gerenciados usando o MED-V.

## Tópicos relacionados


[Definir e planejar sua implantação da MED-V](define-and-plan-your-med-v-deployment.md)

 

 





