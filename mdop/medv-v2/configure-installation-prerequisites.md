---
title: Configurar os pré-requisitos de instalação
description: Configurar os pré-requisitos de instalação
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797499"
---
# Configurar os pré-requisitos de instalação


As instruções a seguir são pré-requisitos para instalar e usar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

[PC virtual do Windows](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Atualização do Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Antivirus/configuração do software de backup](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Como instalar e configurar o Windows Virtual PC


**Importante**  Se já existir uma versão do Virtual PC para Windows no computador host, você deverá desinstalá-la antes de instalar o Windows Virtual PC.

 

**Para instalar o Windows Virtual PC**

1.  Baixe o [computador virtual do Windows](https://go.microsoft.com/fwlink/?LinkId=195918) a partir do centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Execute o arquivo de instalação no computador host e siga as etapas no assistente.

**Importante**  O Windows Virtual PC inclui o pacote de componentes de integração, que fornece recursos que melhoram a interação entre o ambiente virtual e o computador físico. Por exemplo, ele permite que o mouse se movimente entre o host e os computadores convidados. O MED-V requer a instalação do pacote de componentes de integração.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Como instalar e configurar a atualização do Windows Virtual PC


A atualização da Microsoft associada ao artigo KB977206 habilita o modo Windows XP para computadores sem a tecnologia de virtualização assistida por hardware (HAV). Recomendamos que você instale esta atualização porque alguns recursos de integração podem não funcionar corretamente se o pacote de componentes de integração no sistema operacional convidado não corresponderem à versão do computador virtual do Windows instalada no computador host.

**Importante**  Você não precisa instalar esta atualização ao instalar o MED-V em computadores host que executam o Windows 7 com Service Pack 1.

 

**Dica**  Além da atualização listada aqui, recomendamos que você examine todas as atualizações disponíveis do Windows Virtual PC e aplique essas atualizações adequadas ou necessárias para o seu ambiente.

 

**Para instalar a atualização do Windows Virtual PC**

1.  Baixe a atualização necessária do Windows Virtual PC no centro de download da Microsoft.

    [atualização de 32 bits](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [atualização de 64 bits](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Execute o arquivo de instalação no computador host no modo elevado e siga as etapas no assistente.

    Para obter mais informações sobre o pacote de hotfix para o PC virtual do Windows, consulte o [artigo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Como configurar antivírus/software de backup


Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, recomendamos que você possa excluir os seguintes tipos de arquivo de máquina virtual de qualquer processo de antivírus ou backup em execução no computador host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. Wim

## Tópicos relacionados


[Configurar os pré-requisitos do ambiente](configure-environment-prerequisites.md)

[Arquitetura de alto nível](high-level-architecturemedv2.md)

[Configurações com suporte na MED-V 2.0](med-v-20-supported-configurations.md)

 

 





