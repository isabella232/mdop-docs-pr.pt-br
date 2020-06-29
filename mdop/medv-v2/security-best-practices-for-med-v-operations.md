---
title: Práticas recomendadas de segurança para operações da MED-V
description: Práticas recomendadas de segurança para operações da MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799664"
---
# Práticas recomendadas de segurança para operações da MED-V


Como um administrador autorizado, você é responsável por proteger as informações dos usuários e manter a segurança da sua organização durante e após a implantação de espaços de trabalho do MED-V. Em particular, considere os seguintes problemas.

**Personalizando o Internet Explorer no espaço de trabalho do MED-V**. Versões anteriores do sistema operacional Windows e do Internet Explorer não são tão seguras quanto as versões atuais. Portanto, o Internet Explorer no espaço de trabalho do MED-V está configurado para impedir a navegação e outras atividades que possam representar riscos de segurança. Além disso, a configuração de zona de segurança da Internet para o Internet Explorer no espaço de trabalho do MED-V é definida como o nível mais alto. Por padrão, ambas as configurações são definidas no pacote do espaço de trabalho do MED-V quando você cria seu pacote de espaço de trabalho do MED-V.

Usando o kit de administração do Internet Explorer (IEAK) ou alterando os padrões no pacote de espaço de trabalho do MED-V, você pode personalizar o Internet Explorer no espaço de trabalho do MED-V. No entanto, observe que, se você personalizar o Internet Explorer no espaço de trabalho do MED-V de forma a torná-lo menos seguro, você poderá expor sua organização a esses riscos de segurança que estão presentes em versões mais antigas do Internet Explorer.

De uma perspectiva de segurança, as práticas recomendadas para o gerenciamento do Internet Explorer no espaço de trabalho do MED-V são as seguintes:

-   Ao criar seu pacote de espaço de trabalho do MED-V, deixe os padrões definidos para que o Internet Explorer no espaço de trabalho do MED-V seja configurado para impedir a navegação e outras atividades que possam representar riscos de segurança.

-   Ao criar seu pacote de espaço de trabalho do MED-V, deixe os padrões definidos para que a configuração de segurança da zona de segurança da Internet permaneça no nível mais alto.

-   Configure seu proxy corporativo ou o supervisor de conteúdo do Internet Explorer para bloquear domínios fora da intranet da sua empresa.

**Configurar um espaço de trabalho do MED-V para todos os usuários em um computador compartilhado.** Ao configurar um espaço de trabalho do MED-V para que ele possa ser acessado por todos os usuários em um computador compartilhado, perceba que a máquina virtual convidada (VHD) é inserida em um local que concede acesso de leitura e gravação a todos os usuários desse sistema.

**Configurando uma conta proxy para ingressar no domínio.** Ao configurar uma conta proxy para ingressar em máquinas virtuais no domínio, você deve saber que é possível que um usuário final obtenha as credenciais da conta proxy. Portanto, devem ser tomadas precauções necessárias, como a limitação de direitos de usuário da conta, para impedir que um usuário final use as credenciais para causar danos.

**Configuração de Sysprep.** Embora o arquivo Sysprep. inf seja criptografado por padrão, seu conteúdo pode ser descriptografado e lido por qualquer usuário final determinado que pode fazer logon com êxito na máquina virtual. Isso gera problemas de segurança porque o arquivo Sysprep. inf pode conter credenciais, além de uma chave de produto do Windows.

Você pode diminuir esse risco Configurando uma conta limitada para ingressar em máquinas virtuais no domínio e especificando as credenciais dessa conta ao configurar o Sysprep. Como alternativa, você também pode configurar o Sysprep e a primeira vez que o programa de instalação seja executado no modo **assistido** e exigir que os usuários finais forneçam suas credenciais para ingressar na máquina virtual no domínio.

Uma prática recomendada do MED-V é especificar que o FtsCompletion.exe seja executado em uma conta que conceda aos direitos de usuário final para se conectar ao convidado por meio do cliente de conexão de área de trabalho remota (RDC).

**Autenticação de usuário final.** Habilitar o armazenamento em cache de credenciais de usuário final proporciona a melhor experiência do usuário do MED-V, mas cria o potencial que alguém pode ter acesso às credenciais do usuário final. A única maneira de diminuir esse risco é especificando no pacote do **espaço de trabalho do MED-V** que as credenciais do usuário final não são armazenadas. Para obter mais informações sobre autenticação de usuários finais, confira [autenticação de usuários finais do MED-V](authentication-of-med-v-end-users.md).

## Tópicos relacionados


[Solução de problemas de operações](operations-troubleshooting-medv2.md)

[Microsoft Enterprise Desktop Virtualization 2,0](index.md)

 

 





