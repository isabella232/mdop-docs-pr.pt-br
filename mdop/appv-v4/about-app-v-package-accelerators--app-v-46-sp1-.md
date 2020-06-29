---
title: Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)
description: Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797656"
---
# Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)


Você pode usar aceleradores de pacotes do App-V para sequenciar automaticamente aplicativos grandes e complexos. Além disso, ao aplicar um acelerador de pacote App-V, você nem sempre é obrigado a instalar manualmente um aplicativo para criar o pacote de aplicativo virtual.

**Observação**  Em alguns casos, você será solicitado a instalar um aplicativo localmente no computador que está executando o sequenciador do App-V antes de poder usar o acelerador de pacote. Se você precisar instalar um aplicativo, deverá instalar o aplicativo para o local padrão do aplicativo. Esta instalação não é monitorada pelo App-V Sequencer. Quando o acelerador do pacote do App-V é criado, o autor do acelerador de pacote determina se o aplicativo deve ser instalado localmente é necessário.

 

O sequenciador do App-V extrai os arquivos necessários do acelerador de pacotes do App-V e a mídia de instalação associada para criar um pacote virtual sem ter que monitorar a instalação do aplicativo.

**Importante**  Aviso de isenção de responsabilidade: o Microsoft Application Virtualization Sequencer não lhe concede nenhum direito de licença para o aplicativo de software que você está usando para criar um acelerador de pacote. Você deve obedecer a todos os termos de licença de usuário final para tal aplicativo. É sua responsabilidade certificar-se de que os termos de licença do aplicativo de software permitam criar um acelerador de pacote usando o Application Virtualization Sequencer.

 

Os aceleradores de pacotes do App-V e os modelos de projeto diferem uns dos outros. Aceleradores de pacote são específicas do aplicativo. Os modelos de projeto permitem que os usuários salvem as configurações mais comuns específicas de uma organização e as apliquem a vários aplicativos. Você também pode criar modelos de projeto no prompt de comando, enquanto em contraste, você deve usar o console do App-V Sequencer para criar aceleradores de pacote. Além disso, não há suporte para a criação de um pacote usando um acelerador de pacote e a aplicação de um modelo de projeto.

## Compartilhando aceleradores de pacotes do App-V


Esta seção fornece informações de práticas recomendadas sobre como compartilhar aceleradores de pacote. Se você planeja compartilhar aceleradores de pacote, informações como nomes de computador, informações da conta do usuário e informações sobre os aplicativos associados podem estar incluídas nos aceleradores de pacote. a lista a seguir descreve os métodos que você deve considerar ao criar aceleradores de pacote:

-   **Nome de usuário**. Ao fazer logon no computador que executa o App-V Sequencer, você deve usar uma conta de usuário genérica, como a conta de **administrador** interna para administrar o computador/domínio. Você não deve usar uma conta com base em um nome de usuário existente.

-   **Nome do computador**. Especifique um nome geral e não identificado para o computador que está executando o sequenciador.

-   **URL do servidor**. No console do sequenciador, na guia **implantação** , use as configurações padrão para as informações de configuração da URL do servidor.

-   **Aplicativos**. Se você não deseja compartilhar a lista de aplicativos que foram instalados no computador que executa o sequenciador quando você criou o acelerador de pacote, você deve excluir o arquivo **appv\_manifest.xml** . Esse arquivo está localizado no diretório raiz do pacote do pacote de aplicativo virtual.

Você também deve analisar quaisquer configurações ou arquivos de configuração associados ao pacote de aplicativo virtual para garantir que os aplicativos não contenham informações pessoais.

## Proteger aceleradores de pacotes do App-V


Sempre salve os aceleradores de pacotes do App-V e qualquer mídia de instalação associada em um local seguro na rede para proteger os aceleradores de pacotes do App-V e os arquivos de instalação contra violações ou se tornarem corrompidos. Como os aceleradores de pacote também podem conter informações específicas de senha e usuário, você deve salvar aceleradores de pacotes do App-V em um local seguro, e você deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o editor possa ser verificado quando o acelerador de pacote for aplicado. Para obter mais informações sobre assinaturas digitais, consulte [diretrizes de aplicativos sobre práticas de assinatura digital para segurança do Common Criteria](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .

## Tópicos relacionados


[Como criar aceleradores de pacote do App-V (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[Como aplicar um acelerador de pacote para criar um pacote de aplicativo virtual (App-V 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





