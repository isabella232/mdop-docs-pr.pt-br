---
title: Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7
description: Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800041"
---
# Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7


Você pode instalar todos os componentes do MED-V em uma imagem do Windows 7 que você distribui em toda a sua empresa da mesma forma que faria com qualquer nova instalação do Windows 7. Em seguida, o usuário final conclui a instalação do espaço de trabalho do MED-V clicando em um atalho do menu **Iniciar** que você configura para iniciar o MED-v. Primeira vez que a configuração iniciar e o usuário final seguir as instruções para concluir a configuração.

A seção a seguir fornece informações e instruções para ajudá-lo a implantar o espaço de trabalho do MED-V em toda a sua empresa usando uma imagem do Windows 7.

**Para implantar um espaço de trabalho do MED-V em uma imagem do Windows 7**

1.  Crie uma imagem padrão do Windows 7. Para obter mais informações, consulte [criando uma imagem padrão do Windows 7: guia](https://go.microsoft.com/fwlink/?LinkId=204843) passo a passo ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  Na imagem do Windows 7, instale o PC virtual do Windows e as atualizações do Windows Virtual PC. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

3.  Instale o agente de host do MED-V usando o arquivo de instalação do MED-V \ _HostAgent \ _Setup. Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).

    **Aviso**  O Internet Explorer deve ser fechado antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL. Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.

     

4.  Copie os arquivos de pacote do espaço de trabalho do MED-V para a imagem do Windows 7. Os arquivos de pacote do espaço de trabalho do MED-V são o arquivo de espaço de trabalho do MED-V, o arquivo. medv e o arquivo de setup.exe que você criou usando o **pacote do espaço de trabalho do MED-v**.

    **Importante**  O arquivo. medv e setup.exe deve estar na mesma pasta que o instalador do espaço de trabalho do MED-V. Em seguida, instale o espaço de trabalho do MED-V executando setup.exe.

     

5.  Configurar um atalho no menu **Iniciar** para abrir a instalação do pacote do espaço de trabalho do MED-V.

    Crie um atalho do menu **Iniciar** para o arquivo setup.exe que permite ao usuário final iniciar uma instalação do MED-V conforme necessário.

6.  Usando o processo de implantação de imagens padrão da sua empresa, distribua a imagem do Windows 7 para os computadores da sua empresa que exigem o MED-V.

Quando o usuário final precisa acessar um aplicativo publicado no espaço de trabalho do MED-V, ele pode clicar no atalho do menu **Iniciar** para instalar o espaço de trabalho do MED-v. Isso iniciará automaticamente a instalação da primeira vez e concluirá a configuração do MED-V. Depois que a configuração for concluída pela primeira vez, o usuário final poderá acessar os aplicativos MED-V no menu **Iniciar** .

## Tópicos relacionados


[Visão geral da implantação da MED-V 2.0](med-v-20-deployment-overview.md)

[Como implantar um espaço de trabalho da MED-V por meio de um sistema de distribuição eletrônica de software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





