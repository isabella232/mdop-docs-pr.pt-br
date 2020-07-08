---
title: Instalando o software de servidor do MBAM 2.5
description: Instalando o software de servidor do MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799263"
---
# Instalando o software de servidor do MBAM 2.5


Este tópico descreve como instalar o software de servidor Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando o assistente de configuração de administração e administração do Microsoft BitLocker ou usando parâmetros de linha de comando. Repita o processo de instalação do servidor para cada servidor no qual você está configurando os recursos do MBAM 2,5 Server. Após concluir a instalação, consulte [Configurando os recursos do servidor do MBAM 2,5](configuring-the-mbam-25-server-features.md) para ver as etapas sobre como configurar os recursos do servidor.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Antes de começar</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Examinar as informações de planejamento do MBAM 2,5</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurações com suporte no MBAM 2.5</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitetura de alto nível do MBAM 2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Leia como obter arquivos de log</p></td>
<td align="left"><p>Por padrão, os arquivos de log são criados na pasta% Temp% do computador local. Para gravar os arquivos de log em um local específico, em vez de na <strong> pasta% temp </strong> %, use o <strong> </strong> &lt; <em> argumento/log Location </em> &gt; .</p>
<p>Outros eventos podem ser registrados em Visualizador de eventos nos <strong> nós MBAM, Setup </strong> ou <strong> MBAM-Web </strong> em <strong> aplicativos e serviços registra o &gt; Microsoft &gt; Windows </strong> . Por exemplo, se você desinstalar o MBAM, o desinstalador também desinstalará os logs da MBAM-instalação e MBAM-no EventViewer.</p></td>
</tr>
</tbody>
</table>

 

## Instalar o software de servidor do MBAM 2,5 usando o assistente de configuração de monitoramento e administração do Microsoft BitLocker


Use estas etapas para instalar o software MBAM Server usando o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

**Para instalar o software de servidor MBAM 2,5 usando o assistente**

1.  No servidor em que você deseja instalar o MBAM, execute **MBAMserversetup.exe** para iniciar o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

2.  Na página de **boas-vindas** , clique em **Avançar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Escolha se deseja usar o Microsoft Update ao verificar se há atualizações e clique em **Avançar**.

5.  Escolha se deseja participar do programa de aperfeiçoamento da experiência do usuário e clique em **Avançar**.

6.  Para iniciar a instalação, clique em **instalar**.

7.  Para configurar os recursos de servidor após a instalação do software do servidor MBAM, marque a caixa de seleção **executar configuração do servidor do MBAM após o assistente se fechar** . Você também pode configurar o MBAM mais tarde usando o atalho de **configuração do servidor do MBAM** que a instalação do servidor cria no menu **Iniciar** .

8.  Clique em **concluir**.

## Instalar o software de servidor MBAM 2,5 usando uma janela do prompt de comando


Em um prompt de comando, digite um comando semelhante ao seguinte comando para instalar o software MBAM Server.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

A tabela a seguir descreve os parâmetros de linha de comando para a instalação do software de servidor MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valor do parâmetro</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>Verdadeiro falso</p></td>
<td align="left"><p>Verdadeiro – participe do programa experiência de aprimoramento do cliente, que ajuda a Microsoft a identificar quais recursos de MBAM para melhorar.</p>
<p>False – não participa do programa experiência de aprimoramento do cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>Verdadeiro falso</p></td>
<td align="left"><p>True – use o Microsoft Update para manter seu computador seguro e atualizado para Windows e outros produtos da Microsoft, incluindo o MBAM.</p>
<p>Falso – não usar o Microsoft Update</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Caminho&gt;</p></td>
<td align="left"><p>Local onde você deseja instalar o MBAM.</p>
<p>Exemplo:</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>Verdadeiro falso</p></td>
<td align="left"><p>True – continuar o processo de desinstalação do MBAM, mesmo se houver falha na remoção de qualquer recurso.</p>
<p>Falso (padrão) se a ação personalizada de desinstalação não conseguir remover um recurso do servidor MBAM adicionado, a desinstalação falha e o MBAM permanecerá instalado.</p>
<p>Em ambos os casos, todos os recursos que foram removidos com sucesso durante a tentativa de desinstalar o MBAM permanecem removidos.</p></td>
</tr>
</tbody>
</table>

 



## Tópicos relacionados


[Implantando o MBAM 2.5](deploying-mbam-25.md)

[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





