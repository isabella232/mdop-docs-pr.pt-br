---
title: Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software
description: Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799555"
---
# Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software


Um sistema de distribuição de software eletrônico pode ajudá-lo a migrar com eficiência software para muitos computadores por meio de conexões de rede rápidas ou lentas. A seção a seguir fornece informações e instruções para ajudá-lo a implantar os componentes do MED-V (virtualização de área de trabalho do Microsoft Enterprise) 2,0 em toda a sua empresa usando um sistema de distribuição de software.

**Observação**  
Seja qual for a solução de distribuição de software que você usa, você deve estar familiarizado com os requisitos de sua solução específica. Se você estiver usando o System Center Configuration Manager 2007 R2 ou uma versão posterior, consulte a [biblioteca de documentação do Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) na biblioteca técnica da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .



**Importante**  
Se você estiver usando o System Center Configuration Manager 2007 SP2 e seus espaços de trabalho do MED-V estiverem configurados para operar no modo **NAT** , as máquinas virtuais serão classificadas como clientes baseados na Internet e não poderão encontrar os pontos de distribuição mais próximos a partir dos quais baixar conteúdo.

O [hotfix para melhorar a funcionalidade para VMs gerenciadas pelo med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) adiciona Nova funcionalidade a máquinas virtuais que são gerenciadas pelo med-v e que são configuradas para operar no modo **NAT** . A nova funcionalidade permite às máquinas virtuais acessar os pontos de distribuição mais próximos. Portanto, o administrador pode gerenciar a máquina virtual e o computador host da mesma maneira. Esse hotfix deve ser instalado primeiro no servidor do site e, em seguida, no cliente.

A atualização está disponível publicamente. No entanto, você pode ser solicitado a aceitar um contrato de serviços da Microsoft. Siga os prompts nas páginas da Web sucessivas para recuperar este hotfix.



**Observação**  
Você deve instalar o pacote do espaço de trabalho do MED-V e compilar seus espaços de trabalho do MED-V antes de poder implantar os componentes do MED-v por meio do sistema de distribuição de software. Para obter mais informações sobre como preparar uma imagem e criar seus espaços de trabalho do MED-V, consulte [operações do MED-v](operations-for-med-v.md).



**Para implantar os componentes do MED-V usando um sistema de distribuição de software**

1.  Defina um grupo de computadores e usuários no sistema de distribuição de software eletrônico como o conjunto de destino de computadores/usuários.

2.  Crie pacotes para cada arquivo de instalação da Microsoft que precisa ser distribuído. Estes são os arquivos necessários e a ordem em que devem ser instalados:

    1.  **PC virtual do Windows** – se ainda não estiver instalado (é preciso reiniciar o computador). Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    2.  **Inclusões e atualizações do Windows Virtual PC** – se ainda não estiverem instaladas. Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).

    3.  **Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação). Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).

        **Aviso**  
        Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL. Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.   

    4.  **Instalador do espaço de trabalho do MED-v, VHD e executável de configuração** – criado no **pacote do espaço de trabalho do MED-v**. Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).

        **Importante**  
        O arquivo de disco rígido virtual compactado (. medv) e o programa de instalação executável (setup.exe) devem estar na mesma pasta que o instalador do espaço de trabalho do MED-V. Em seguida, instale o instalador do espaço de trabalho do MED-V executando setup.exe.

        **Dica**  
        Como os problemas que podem ocorrer ao instalar o MED-V a partir de um local de rede, recomendamos que você copie os arquivos de instalação do espaço de trabalho do MED-V localmente e, em seguida, execute setup.exe.       

3.  Configure os pacotes para serem executados em modo silencioso (não é necessária interação do usuário).

    Executar em modo silencioso elimina a solicitação para fechar o Internet Explorer se estiver em execução e a solicitação para iniciar o agente de host do MED-V. Ambas as ações são executadas quando o computador é reiniciado.

    **Observação**  
    A instalação do Windows Virtual PC exige que você reinicie o computador. Você pode criar um único processo de instalação e instalar todos os componentes ao mesmo tempo se suprimir a reinicialização e ignorar os pré-requisitos necessários para a instalação do MED-V. Você também pode fazer isso usando argumentos de linha de comando. Para obter um exemplo desses argumentos, consulte [para instalar os componentes do MED-V usando um arquivo em lotes](#bkmk-batch). O MED-V é iniciado automaticamente quando o computador é reiniciado.

4.  Instale o MED-V e seus componentes antes de instalar o Windows Virtual PC. Consulte o arquivo em lotes de exemplo mais adiante neste tópico.

    **Importante**  
    Selecione a opção **ignorar \ _PREREQUISITES** , conforme mostrado no arquivo em lotes de exemplo, de modo que os componentes do MED-V possam ser instalados antes dos componentes obrigatórios do VPC. Instale os componentes do MED-V nesta ordem para permitir a reinicialização única.

5.  Identifique outros requisitos necessários para a instalação e para o seu sistema de distribuição de software, como plataformas de destino e o espaço livre em disco.

6.  Atribua os pacotes ao conjunto de destino de computadores/usuários.

    À medida que os computadores estão em execução, o cliente do sistema de distribuição de software reconhece que novos pacotes estão disponíveis e começa a instalar os pacotes de acordo com a definição e os requisitos. As instalações devem funcionar sequencialmente no modo silencioso. Recomendamos que isso seja executado como um único processo que não exija uma reinicialização até que todos os pacotes sejam instalados.

7.  Depois que as instalações forem concluídas, reinicie os computadores atualizados.

    Dependendo do sistema de distribuição de software, você pode agendar uma reinicialização do computador ou os usuários finais podem reiniciar os computadores manualmente durante o trabalho normal. Depois que o computador for reiniciado, o MED-V iniciará automaticamente após o logon de um usuário final. Quando o MED-V é iniciado pela primeira vez, ele é executado na primeira vez em que está configurado.

A configuração inicial do programa será iniciada e poderá demorar vários minutos para ser concluída, dependendo do tamanho do disco rígido virtual especificado e do número de políticas aplicado ao espaço de trabalho do MED-V na inicialização. O usuário final pode acompanhar o progresso observando o ícone do MED-V na área de notificação. Para obter mais informações sobre a configuração da primeira vez, consulte [visão geral de implantação do MED-V 2,0](med-v-20-deployment-overview.md).

<a href="" id="bkmk-batch"></a>**Para instalar os componentes do MED-V usando um arquivo em lote**

1.  Execute a instalação em um prompt de comando com credenciais administrativas.

2.  Implantar cada componente em um único diretório. Se executado de um compartilhamento de rede, um tempo maior será necessário para descompactar o arquivo. medv.

3.  Como prática recomendada, especifique se o Windows Virtual PC e o hotfix do Windows Virtual PC estão instalados após o pacote do host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V. Isso significa que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.

4.  Reinicie o computador após o término do arquivo em lote.

Após a reinicialização, o usuário será solicitado a executar a configuração da primeira vez e concluir a configuração do MED-V.

O exemplo a seguir, com os argumentos especificados, mostra como instalar os componentes do 64 bits MED-V em um único processo:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Argumento</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Impede que a instalação do Windows Virtual PC e da atualização do Windows Virtual PC reinicie o computador host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p>Instala os componentes do MED-V no modo silencioso sem a interação do usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/qn</p></td>
<td align="left"><p>Instala os componentes do MED-V sem uma interface de usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Instala sem verificar o computador virtual do Windows.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Especifique esse argumento apenas se você estiver instalando o Windows Virtual PC como parte desta instalação.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>Força a instalação do espaço de trabalho do MED-V e impede que qualquer prompt seja gerado.</p></td>
</tr>
</tbody>
</table>



## Exemplo


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## Tópicos relacionados


[Visão geral da implantação da MED-V 2.0](med-v-20-deployment-overview.md)

[Implantar os componentes da MED-V](deploy-the-med-v-components.md)









