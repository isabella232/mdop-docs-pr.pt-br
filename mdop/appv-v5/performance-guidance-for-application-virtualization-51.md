---
title: Guia de desempenho do Application Virtualization 5.1
description: Guia de desempenho do Application Virtualization 5.1
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796270"
---
# Guia de desempenho do Application Virtualization 5.1


Saiba como configurar o App-V 5,1 para obter ótimo desempenho, otimizar pacotes de aplicativos virtuais e oferecer uma experiência de usuário melhor com o RDS e o VDI.

A implementação de vários métodos pode ajudá-lo a melhorar a experiência do usuário final. No entanto, seu ambiente pode não dar suporte a todos os métodos.

Você deve ler e compreender as informações a seguir antes de ler este documento.

-   [Guia do administrador do Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Publicação de aplicativos e interação do cliente do App-V 5 SP2](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Guia de sequenciamento do Microsoft Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=269953)

**Observação**  
Alguns termos usados neste documento podem ter significados diferentes dependendo da fonte externa e do contexto. Para obter mais informações sobre os termos usados neste documento seguidos de um asterisco **\\** *, consulte a seção [terminologia de orientação do desempenho do Application Virtualization](#bkmk-terms1) deste documento.



Por fim, este documento fornecerá as informações para configurar o computador que está executando o cliente do App-V 5,1 e o ambiente para obter ótimo desempenho. Otimize seus pacotes de aplicativos virtuais para desempenho usando o sequenciador e saiba como usar a virtualização de experiência do usuário (UE-V) ou outras tecnologias de gerenciamento do ambiente do usuário para fornecer a melhor experiência do usuário com o App-V 5,1 nos serviços de área de trabalho remota (RDS) e infraestrutura de área de trabalho virtual (VDI) não persistente.

Para ajudar a determinar quais informações são relevantes para o seu ambiente, examine a breve visão geral e a lista de verificação de aplicabilidade de cada seção.

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> App-V 5,1 em implantações de estado \ * não persistentes


Esta seção fornece informações sobre uma abordagem que ajuda a garantir que um usuário terá acesso a todos os aplicativos virtuais em segundos após o logon. Isso é conseguido com o endereçamento exclusivo da atualização de publicação do App-V 5,1 de longa execução. Como você descobrirá a base da abordagem, a atualização de publicação mais rápida é aquela que não precisa realmente fazer nada. Uma série de condições deve ser satisfeita e etapas seguidas para fornecer a melhor experiência do usuário.

Use as informações na seção a seguir para obter mais informações:

[Cenários de uso](#bkmk-us) – conforme você revisa os dois cenários, lembre-se de que esses são os métodos extremos. Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de pacotes de aplicativos virtuais e/ou usuários.

-   Otimizado para desempenho – para fornecer a experiência ideal, você pode esperar que a imagem base inclua alguns dos pacotes de aplicativo virtual do App-V. Esse e outros requisitos são discutidos.

-   Otimizado para armazenamento – se você estiver preocupado com o impacto do armazenamento, seguir este cenário irá ajudá-lo a solucionar esses problemas.

[Preparando seu ambiente](#bkmk-pe)

-   Etapas para preparar a imagem base – seja em um ambiente de VDI ou RDSH não persistente, apenas algumas etapas devem ser concluídas na imagem base para habilitar essa abordagem.

-   Use o UE-V 2,1 como a solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V – a base dessa abordagem é a capacidade de uma solução UEM de persistir o conteúdo de apenas alguns locais de registro e de arquivo. Esses locais constituem as integrações do usuário \ *. Certifique-se de analisar os requisitos específicos para a solução UPM.

[Orientação de experiência do usuário](#bkmk-uewt)

-   Acompanhamento-passo-a-passo é uma orientação passo a passo das operações do App-V e do UE-V e das expectativas que os usuários devem ter.

-   Resultado – descreve os resultados esperados.

[Impacto no ciclo de vida do pacote](#bkmk-plc)

[Aprimorar a experiência com VDI por meio da otimização/ajuste de desempenho](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>Lista de verificação de aplicabilidade

Ambiente de implantação

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>VDI ou RDSH não persistentes.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>User Experience Virtualization (UE-V), outras soluções UPM ou discos de perfil de usuário (UPD).</p></td>
</tr>
</tbody>
</table>



Configuração esperada

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>User Experience Virtualization (UE-V) com o modelo de estado de usuário do App-V habilitado ou o software de gerenciamento de perfil do usuário (UPM). O software UPM não-UE-V deve ser capaz de disparar no início e no logoff de logon ou processo/aplicativo.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>O SCS (repositório de conteúdo compartilhado) do App-V está configurado ou pode ser configurado.</p></td>
</tr>
</tbody>
</table>



Administração de ti

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>O administrador pode precisar atualizar a imagem base da VM regularmente para garantir o desempenho ideal ou o administrador pode precisar gerenciar várias imagens para diferentes grupos de usuários.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>Cenário de uso

Ao revisar os dois cenários, lembre-se de que esses métodos são extremos. Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de usuários, pacotes de aplicativos virtuais ou ambos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Otimizado para desempenho</th>
<th align="left">Otimizado para armazenamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Para fornecer a melhor experiência do usuário, essa abordagem aproveita os recursos de uma solução UPM e requer uma preparação adicional da imagem e pode causar uma sobrecarga adicional de gerenciamento de imagens.</p>
<p>A seguir está a descrição de vários aprimoramentos de desempenho em implantações não persistentes de estado. Para obter mais informações, consulte as <strong> etapas de sequenciamento para otimizar pacotes para a publicação de desempenho </strong> e referência para <strong> o guia de sequenciamento do App-V </strong> na <strong> seção Consulte também deste documento </strong> .</p></td>
<td align="left"><p>As expectativas gerais do cenário anterior ainda se aplicam aqui. No entanto, lembre-se de que as imagens da VM são geralmente armazenadas em arrays dispendiosos; uma ligeira alteração foi feita na abordagem. Não configure previamente pacotes de aplicativos virtuais direcionados pelo usuário na imagem base.</p>
<p>O impacto dessas alterações é detalhado na seção do guia de experiência do usuário deste documento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>Preparando seu ambiente

A tabela a seguir mostra as etapas necessárias para preparar a imagem base e o UE-V ou outra solução UPM para a abordagem.

**Preparar a imagem base**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Otimizado para desempenho</th>
<th align="left">Otimizado para armazenamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Instale a versão do cliente do App-V 5,1 do cliente.</p></li>
<li><p>Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</p></li>
<li><p>Configurar para o modo SCS (repositório de conteúdo compartilhado). Para obter mais informações, consulte <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,1 para o modo de repositório de conteúdo compartilhado </a> .</p></li>
<li><p>Configurar preservar integrações de usuário na DWORD do registro de logon.</p></li>
<li><p>Pré-configure todos os pacotes de usuário e de destino global, por exemplo, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Pré-configure todos os grupos de conexões direcionadas a usuário e global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Pré-publique todos os pacotes direcionados globalmente.</p>
<p></p>
<p>Como alternativa</p>
<ul>
<li><p>Executar uma publicação/atualização global.</p></li>
<li><p>Executar uma publicação/atualização de usuário.</p></li>
<li><p>Cancele a publicação de todos os pacotes direcionados pelo usuário.</p></li>
<li><p>Exclua as seguintes entradas de User-virtual File System (VFS).</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Instale a versão do cliente do App-V 5,1 do cliente.</p></li>
<li><p>Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</p></li>
<li><p>Configurar para o modo SCS (repositório de conteúdo compartilhado). Para obter mais informações, consulte <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,1 para o modo de repositório de conteúdo compartilhado </a> .</p></li>
<li><p>Configurar preservar integrações de usuário na DWORD do registro de logon.</p></li>
<li><p>Pré-configure todos os pacotes direcionados global por exemplo, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Pré-configure todos os grupos de conexão de direcionamento global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Pré-publique todos os pacotes direcionados globalmente.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**Configurações** -para configurações essenciais do cliente App-V e para obter um pouco mais de contexto e instruções, Confira as seguintes informações:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração</th>
<th align="left">O que isso faz?</th>
<th align="left">Como devo usá-lo?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Modo SCS (Shared Content Store)</p>
<ul>
<li><p>Configurável no PowerShell usando <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</p></li>
<li><p>Durante a instalação do cliente App-V.</p></li>
</ul></td>
<td align="left"><p>Ao executar o repositório de conteúdo compartilhado, somente os dados de publicação são mantidos no disco rígido; outros ativos de aplicativo virtual são mantidos na memória (RAM).</p>
<p>Isso ajuda a conservar o armazenamento local e a minimizar a e/s de disco por segundo (IOPS).</p></td>
<td align="left"><p>Isso é recomendado quando conexões de baixa latência são disponibilizadas entre o ponto de extremidade do cliente App-V e o servidor de conteúdo do SCS, SAN.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p>Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> software </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> Client </strong>  \  <strong> Integration </strong> .</p></li>
<li><p>Crie o valor DWORD <strong> PreserveUserIntegrationsOnLogin </strong> com um valor de <strong> 1 </strong> .</p></li>
<li><p>Reinicie o serviço App-V Client ou reinicie o computador que executa o cliente App-V.</p></li>
</ul></td>
<td align="left"><p>Se você não tiver pré-configurado ( <strong> Add-AppvClientPackage </strong> ) um pacote específico e essa configuração não for definida, o cliente App-V desintegrará * as integrações de usuário persistentes e, em seguida, se reintegrará *.</p>
<p>Para cada pacote que atenda às condições acima, o dobro do trabalho será realizado durante a publicação/atualização.</p></td>
<td align="left"><p>Se você não planeja pré-configurar previamente cada pacote de usuário disponível na imagem base, use essa configuração.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p>Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong> &lt; forte &gt; software </strong>  \  <strong> publicação de </strong>  \  <strong> </strong> &lt; cliente forte do Microsoft AppV &gt; </strong>  \  <strong> </strong> .</p></li>
<li><p>Crie o valor DWORD <strong> MaxConcurrentPublishingrefresh </strong> com o número máximo de atualizações de publicação simultâneas desejadas.</p></li>
<li><p>O serviço e o computador do cliente App-V não precisam ser reiniciados.</p></li>
</ul></td>
<td align="left"><p>Essa configuração determina o número de usuários que podem realizar uma atualização/sincronização de publicação ao mesmo tempo. A configuração padrão é sem limite.</p></td>
<td align="left"><p>Limitar o número de atualizações de publicação simultâneas impede o uso excessivo da CPU que pode afetar o desempenho do computador. Esse limite é recomendado em um ambiente RDS, no qual vários usuários podem entrar no mesmo computador ao mesmo tempo e executar uma sincronização de atualização de publicação.</p>
<p>Se o limite de atualização de publicação simultânea for atingido, o tempo necessário para publicar novos aplicativos e disponibilizá-los para os usuários finais após o login poderá demorar um período indeterminado.</p></td>
</tr>
</tbody>
</table>



### Configurar o método de solução UE-V para App-V

Recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico. Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI). A UE-V é otimizada para cenários de RDS e VDI.

Para obter mais informações, consulte [introdução ao User Experience Virtualization 2,0](https://technet.microsoft.com/library/dn458926.aspx)

Em essência, tudo o que é necessário é instalar o UE-V Client e baixar o modelo de configurações do aplicativo Microsoft autod App-V da [Galeria de modelos do Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33). Registre o modelo. Para obter mais informações sobre os modelos do UE-V, consulte [o recurso específico do UE-v para adquirir e registrar o modelo](https://technet.microsoft.com/library/dn458926.aspx).

**Observação**  
Sem realizar uma etapa de configuração adicional, a virtualização de ambiente de usuário da Microsoft (UE-V) não poderá sincronizar os atalhos do menu iniciar (arquivos. lnk) no computador de destino. O tipo de arquivo. lnk é excluído por padrão.

O UE-V só dará suporte à remoção do tipo de arquivo. lnk da lista de exclusão nos cenários de RDS e VDI, em que cada dispositivo de usuário terá o mesmo conjunto de aplicativos instalados no mesmo local e cada arquivo. lnk será válido para todos os dispositivos dos usuários. Por exemplo, o UE-V não oferece suporte aos dois cenários a seguir, porque o resultado da rede será que o atalho será válido em um, mas não em todos os dispositivos.

-   Se um usuário tiver um aplicativo instalado em um dispositivo com arquivos. lnk habilitados e o mesmo aplicativo nativo instalado em outro dispositivo em uma raiz de instalação diferente com arquivos. lnk habilitados.

-   Se um usuário tiver um aplicativo instalado em um dispositivo, mas não outro com arquivos. lnk habilitados.



**Importante**  
Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.



Usando o editor de registro da Microsoft (regedit.exe), navegue até **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** e remova **. lnk** dos tipos de arquivo excluídos.

**Configurar outra solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V**

A expectativa em um ambiente stateful é que uma solução UPM é implementada e pode dar suporte à persistência de dados de usuário entre sessões e entre logons.

Os requisitos para a solução UPM são os seguintes.

Para habilitar uma experiência de logon otimizada, por exemplo, a abordagem App-V 5,1 para o usuário, a solução deve ser capaz de:

-   Persistir as integrações de usuário abaixo, como parte do perfil do usuário/pessoa.

-   Disparar uma sincronização de perfil de usuário no logon (ou início do aplicativo), que pode garantir que todas as integrações de usuário sejam aplicadas antes de iniciar a publicação/atualização ou,

-   Anexar e desanexar um disco de perfil de usuário (UPD) ou uma tecnologia semelhante que contém as integrações do usuário.

    **Observação**  
    O App-V tem suporte ao usar a UPD somente quando o perfil inteiro é armazenado no disco de perfil do usuário.

    Não há suporte para pacotes do App-V ao usar a UPD com pastas selecionadas armazenadas no disco de perfil do usuário. O driver copiar no write não manipula as pastas selecionadas UPD.



-   Captura de alterações nos locais, que constituem as integrações do usuário antes do logoff da sessão.

Com o App-V 5,1 ao adicionar um servidor de publicação (**Add-AppvPublishingServer**), você pode configurar a sincronização, por exemplo, atualizar durante o logon e/ou depois de um intervalo de atualização especificado. Em ambos os casos, uma tarefa agendada é criada.

Em versões anteriores do App-V 5,1, ambas as tarefas agendadas eram configuradas usando um VBScript que iniciaria o usuário e a atualização global. Com o pacote de hotfix 4 para Application Virtualization 5,0 SP2, a atualização do usuário durante o logon foi iniciada por **SyncAppvPublishingServer.exe**. Essa alteração foi introduzida para fornecer um processo de gatilho às soluções do UPM. Esse processo atrasa a publicação/Refresh para permitir que a solução UPM aplique as integrações do usuário. Ele será encerrado quando a publicação/atualização for concluída.

**Integrações do usuário**

Registro – HKEY \ _CURRENT \ _USER

-   Caminho-Software\\Classes

    Exclude: configurações locais, ActivatableClasses, AppX \ *

-   Caminho-Software\\Microsoft\\AppV

-   Caminhos de caminho Software\\Microsoft\\Windows\\CurrentVersion\\App

**Locais de arquivos**

-   Root – "variável de ambiente" APPDATA

    Caminho – Microsoft\\AppV\\Client\\Catalog

-   Root – "variável de ambiente" APPDATA

    Caminho – Microsoft\\AppV\\Client\\Integration

-   Root – "variável de ambiente" APPDATA

    Path-Microsoft\\Windows\\Start Menu\\Programs

-   (Para manter todos os atalhos da área de trabalho, virtuais e não virtuais)

    Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} filemask-\ *. lnk

**Microsoft User Experience Virtualization (UE-V)**

Além disso, recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico. Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI).

Para obter mais informações, consulte [introdução ao User Experience Virtualization 1,0](https://technet.microsoft.com/library/jj680015.aspx) e [compartilhamento de configurações modelos de local com a Galeria de modelos UE-V](https://technet.microsoft.com/library/jj679972.aspx).

### <a href="" id="bkmk-uewt"></a>Orientação de experiência do usuário

Veja a seguir uma orientação passo a passo sobre as operações do App-V e do UPM e as expectativas que os usuários devem esperar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Otimizado para desempenho</th>
<th align="left">Otimizado para armazenamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</p>
<ul>
<li><p>Opera Uma publicação/atualização do usuário é iniciada. Gestão Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</p></li>
<li><p>Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário. Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff. Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário.</p></li>
</ul>
<p>Em logons subsequentes:</p>
<ul>
<li><p>Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</p>
<p>Gestão Haverá atalhos presentes na área de trabalho ou no menu Iniciar, que funcionam imediatamente. Quando a publicação/atualização é concluída (ou seja, as titularidades do pacote são alteradas), alguns podem ficar ausentes.</p></li>
<li><p>Opera A publicação/atualização processará operações de cancelamento e publicação de alterações nos direitos do pacote do usuário. Gestão Se não houver nenhuma alteração de direito, o publishing1 será concluído em segundos. Caso contrário, a publicação/atualização será aumentada em relação ao número e à complexidade * dos aplicativos virtuais</p></li>
<li><p>Opera A solução UPM capturará as integrações do usuário novamente no logoff. Gestão Mesmo que a seção anterior.</p></li>
</ul>
<p>¹ a operação de publicação ( <strong> publicar-AppVClientPackage </strong> ) adiciona entradas ao catálogo do usuário, mapeia a qualificação ao usuário, identifica o repositório local e termina ao completar qualquer etapa de integração.</p></td>
<td align="left"><p>Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</p>
<ul>
<li><p>Opera Uma publicação/atualização do usuário é iniciada. Gestão</p>
<ul>
<li><p>Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</p></li>
<li><p>Os logins iniciais e subseqüentes serão afetados pela pré-configuração dos pacotes (adicionar/atualizar).</p>
<p></p></li>
</ul></li>
<li><p>Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário. Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff. Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário</p></li>
</ul>
<p>Em logons subsequentes:</p>
<ul>
<li><p>Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</p></li>
<li><p>Opera Adicionar/atualizar deve pré-configurar todos os aplicativos direcionados ao usuário. Gestão</p>
<ul>
<li><p>Isso pode aumentar o tempo para a disponibilidade do aplicativo significativamente (na ordem de 10 de segundos).</p></li>
<li><p>Isso aumentará o tempo de atualização de publicação em relação ao número e à complexidade * dos aplicativos virtuais.</p>
<p></p></li>
</ul></li>
<li><p>Opera A publicação/atualização processará operações de cancelamento e publicação para alterações nos direitos do pacote de usuários.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Resultado</th>
<th align="left">Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Como as integrações do usuário são completamente preservadas, não haverá nenhum trabalho por exemplo, integração para a publicação/atualização a ser concluída. Todos os aplicativos virtuais estarão disponíveis em segundos de login.</p></li>
<li><p>A publicação/atualização processará as alterações dos aplicativos virtuais intitulados aos usuários, que impactam a experiência.</p></li>
</ul></td>
<td align="left"><p>Como o Adicionar/atualizar deve reconfigurar todos os aplicativos virtuais para a VM, o tempo de atualização de publicação em todos os logins será estendido.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>Impacto no ciclo de vida do pacote

Atualizar um pacote é um aspecto crucial do ciclo de vida do pacote. Para ajudar a garantir que os usuários tenham acesso aos pacotes de aplicativos virtuais atualizados (publicados) ou rebaixados (não publicados), é recomendável atualizar a imagem base para refletir essas alterações. Para entender por que examine a seção a seguir:

App-V 5,0 SP2 introduziu o conceito de Estados pendentes. No passado,

-   Se um administrador tiver alterado direitos ou criado uma nova versão de um pacote (atualizado) e durante uma publicação/atualização que o pacote estava em uso, a operação de cancelamento ou publicação, respectivamente, falharia.

-   Agora, se um pacote estiver em-uso, a operação será pendente. As operações de cancelamento de publicação e publicação pendente serão processadas na reinicialização do serviço, ou se outro comando de publicação ou cancelamento de publicação for emitido. Nesse caso, se o aplicativo virtual estiver sendo usado de outra forma, o aplicativo virtual permanecerá em um estado pendente. Para pacotes publicados globalmente, uma reinicialização (ou reinicialização do serviço) geralmente necessária.

Em um ambiente não persistente, é improvável que estas operações pendentes sejam processadas. As operações pendentes, por exemplo, as tarefas são capturadas em **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**. Embora esse local seja mantido pela solução UPM, se não for aplicado ao ambiente antes do logon, ele não será processado.

### <a href="" id="bkmk-evdi"></a>Aprimorar a experiência com VDI por meio do ajuste de otimização de desempenho

A seção a seguir contém listas com informações sobre documentação e downloads da Microsoft que podem ser úteis ao otimizar seu ambiente para desempenho.

**Blog e script do .NET NGEN (altamente recomendado)**

Sobre a tecnologia NGEN

-   [Como acelerar a otimização do NGEN](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [Script](https://aka.ms/DrainNGenQueue)

**Funções do servidor e do servidor do Windows**

Diretrizes de ajuste de desempenho do servidor para

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**Funções de servidor**

-   [Host de virtualização de área de trabalho remota](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [Host da sessão da área de trabalho remota](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [Relevância do IIS: gerenciamento de App-V, publicação, serviços Web de relatório](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [Relevância de servidor de arquivos (SMB): se usado para armazenamento e entrega de conteúdo do App-V no modo SCS](https://technet.microsoft.com/library/jj134210.aspx)

**Orientação de ajuste de desempenho do cliente Windows (SO convidado)**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [Script de otimização: (fornecido pelo suporte da Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [Script de otimização: (fornecido pelo suporte da Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## Etapas de sequenciamento para otimizar pacotes para o desempenho de publicação


Vários recursos do App-V facilitam novos cenários ou permitem novos cenários de implantação de cliente. Esses recursos seguintes podem afetar o desempenho das operações de publicação e inicialização.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Consideração</th>
<th align="left">Benefícios</th>
<th align="left">Compensações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nenhum bloco de recursos 1 (FB1, também conhecido como principal FB)</p></td>
<td align="left"><p>Nenhuma FB1 significa que o aplicativo será iniciado imediatamente e a falha de fluxo (o aplicativo exige arquivo, DLL e deve ser puxado pela rede) durante a inicialização. Se houver limitações de rede, o FB1 irá:</p>
<ul>
<li><p>Reduza o número de falhas de fluxo e largura de banda de rede usada quando você inicia um aplicativo pela primeira vez.</p></li>
<li><p>Atrasar o lançamento até que todo o FB1 tenha sido transmitido.</p></li>
</ul></td>
<td align="left"><p>A falha do fluxo diminui o tempo de inicialização.</p></td>
<td align="left"><p>Os pacotes de aplicativos virtuais com o FB1 configurado precisarão ser novamente sequenciados.</p></td>
</tr>
</tbody>
</table>



### Removendo FB1

Remover o FB1 não exige o instalador do aplicativo original. Depois de concluir as etapas a seguir, é recomendável que você reverta o computador que executa o sequenciador para um instantâneo limpo.

**Interface do usuário do sequenciador** -crie um novo pacote de aplicativo virtual.

1.  Conclua as etapas de sequenciamento para personalizar- &gt; streaming.

2.  Na etapa de streaming, não selecione **otimizar o pacote para implantação em redes lentas ou não confiáveis**.

3.  Se desejar, vá para o **sistema operacional de destino**.

**Modificar um pacote de aplicativo virtual existente**

1.  Conclua as etapas de sequenciamento para transmitir.

2.  Não selecione **otimizar o pacote para implantação em uma rede lenta ou não confiável**.

3.  Mover para **criar pacote**.

**PowerShell** -atualize um pacote de aplicativo virtual existente.

1.  Abra uma sessão do PowerShell com privilégios elevados.

2.  Import-Module **appvsequencer**.

3.  **Update-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.appv"-instalador

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **Observação**  
    Esse cmdlet requer um arquivo executável (. exe) ou um arquivo em lotes (. bat). Você deve fornecer um arquivo executável ou arquivo em lotes vazio (não há nada).



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Conhecer</th>
<th align="left">Benefícios</th>
<th align="left">Compensações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nenhuma instalação do SXS na publicação (pré-instalação assemblies SxS)</p></td>
<td align="left"><p>Os pacotes de aplicativos virtuais não precisam ser seqüenciados novamente. Os assemblies SxS podem permanecer no pacote de aplicativo virtual.</p></td>
<td align="left"><p>As dependências do assembly SxS não serão instaladas no momento da publicação.</p></td>
<td align="left"><p>As dependências de assembly SxS devem ser pré-instaladas.</p></td>
</tr>
</tbody>
</table>



### Criando um novo pacote de aplicativo virtual no sequenciador

Se, durante o monitoramento do sequenciador, um assembly SxS (como um VC + + Runtime) for instalado como parte da instalação de um aplicativo, o assembly SxS será detectado e incluído no pacote automaticamente. O administrador será notificado e terá a opção de excluir o assembly SxS.

**Lado do cliente**:

Ao publicar um pacote de aplicativo virtual, o cliente App-V detectará se uma dependência SxS obrigatória já está instalada. Se a dependência não estiver disponível no computador e estiver incluída no pacote, um programa tradicional do Windows Installer (.** MSI**) a instalação do assembly SxS será iniciada. Conforme documentado anteriormente, basta instalar a dependência no computador que está executando o cliente para garantir que a instalação do Windows Installer (. msi) não ocorra.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Conhecer</th>
<th align="left">Benefícios</th>
<th align="left">Compensações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Empregar arquivos de configuração dinâmicos de forma seletiva</p></td>
<td align="left"><p>O cliente App-V 5,1 deve analisar e processar esses arquivos de configuração dinâmica.</p>
<p>Fique atento ao tamanho e à complexidade (execução de script, inclusões de VREG/exclusões) do arquivo.</p>
<p>Muitos pacotes de aplicativos virtuais podem já ter arquivos de configurações dinâmicas específicos do computador ou do computador.</p></td>
<td align="left"><p>Os tempos de publicação serão aprimorados se esses arquivos forem usados seletivamente ou não.</p></td>
<td align="left"><p>Os pacotes de aplicativos virtuais precisariam ser reconfigurados individualmente ou por meio do console de gerenciamento do App-V Server para remover arquivos de configuração dinâmico associados.</p></td>
</tr>
</tbody>
</table>



### Desativando uma configuração dinâmica usando o PowerShell

-   Para pacotes já publicados, você pode usar `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sem

    Parâmetro **-DynamicDeploymentConfiguration**

-   Da mesma forma, ao adicionar novos pacotes usando `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , não use o

    **-Parâmetro DynamicDeploymentConfiguration** .

Para obter a documentação sobre como aplicar uma configuração dinâmica, consulte:

-   [Como aplicar o arquivo de configuração do usuário usando o PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [Como aplicar o arquivo de configuração da implantação usando o PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Conhecer</th>
<th align="left">Benefícios</th>
<th align="left">Compensações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Conta para a execução de script síncrono durante o ciclo de vida do pacote.</p></td>
<td align="left"><p>Se o material de apoio do script estiver incorporado no pacote, o Add (PowerShell) pode ser significativamente mais lento.</p>
<p>A execução de scripts durante a inicialização do aplicativo virtual (StartVirtualEnvironment, StartProcess) e/ou adicionar + publicar afetará o desempenho percebido durante uma ou mais dessas operações do ciclo de vida.</p></td>
<td align="left"><p>O uso de scripts assíncronos (não bloqueados) garantirá que as operações do ciclo de vida sejam concluídas com eficiência.</p></td>
<td align="left"><p>Esta etapa requer o conhecimento funcional de todos os pacotes de aplicativos virtuais com o material de script incorporado, que tem arquivos de configurações dinâmicos associados e a referência e execução de scripts de forma síncrona.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remover fontes virtuais estranhas do pacote.</p></td>
<td align="left"><p>A maioria dos aplicativos investigados pela equipe do produto App-V continha um pequeno número de fontes, geralmente menor que 20.</p></td>
<td align="left"><p>As fontes virtuais afetam o desempenho da atualização da publicação.</p></td>
<td align="left"><p>As fontes desejadas deverão ser habilitadas/instaladas nativamente. Para obter instruções, confira instalar ou desinstalar fontes.</p></td>
</tr>
</tbody>
</table>



### Determinar quais fontes virtuais existem no pacote

-   Faça uma cópia do pacote.

-   Renomear o pacote \ _copy. AppV para Package\_copy.zip

-   Abra AppxManifest.xml e localize o seguinte:

    &lt;AppV: categoria de extensão = "AppV. fonts"&gt;

    &lt;AppV: fontes&gt;

    &lt;AppV: caminho da fonte = "\ [{fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: Font&gt;

    **Observação**  
    Se houver fontes marcadas como **DELAYLOAD**, elas não terão impacto na primeira inicialização.



~~~
&lt;/appv:Fonts&gt;
~~~

### Excluindo fontes virtuais do pacote

Use o arquivo de configuração dinâmica que melhor se adapta ao escopo do usuário – configuração de implantação para todos os usuários no computador, configuração de usuário para usuários específicos ou usuários.

-   Desative as fontes com a implantação ou a configuração do usuário.

Fontes

--&gt;

&lt;Fonts Enabled = "false"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> Terminologia de diretrizes de desempenho do App-V 5,1


Os termos a seguir são usados para descrever os conceitos e ações relacionados à otimização de desempenho do App-V 5,1.

-   **Complexidade** – refere-se a uma ou mais características do pacote que podem afetar o desempenho durante a pré-configuração (**Add-AppvClientPackage**) ou integração (**Publish-AppvClientPackage**). Alguns exemplos de características são: tamanho do manifesto, número de fontes virtuais, número de arquivos.

-   **Desintegrar** – remove as integrações do usuário

-   **Integrar novamente** – aplica as integrações do usuário.

-   **Não persistente, poold** – cria um computador que executa um ambiente virtual cada vez que eles fazem logon.

-   **Persistente, pessoal** – um computador que executa um ambiente virtual que permanece igual para cada logon.

-   **Stateful** – para este documento, sugere que as integrações do usuário são mantidas entre sessões e uma tecnologia de gerenciamento do ambiente do usuário é usada em conjunto com RDSH não persistente ou VDI.

-   **Sem monitoração** de estado – representa um cenário quando nenhum estado do usuário é mantido entre as sessões.

-   **Gatilho** – (ou gatilhos de ação nativa). O UPM usa esses tipos de gatilhos para iniciar operações de monitoramento ou sincronização.

-   **Experiência do usuário** -no contexto do App-V 5,1, a experiência do usuário, quantitativomente, é a soma das seguintes partes:

    -   Do ponto em que os usuários iniciam um logon quando podem manipular a área de trabalho.

    -   A partir do ponto em que a área de trabalho pode ser interagindo ao ponto em que uma atualização de publicação começa (em termos do PowerShell, sincronizar) ao usar a infraestrutura de servidor completo do App-V 5,1. Em instâncias autônomas, é quando os comandos do PowerShell **Add-AppVClientPackage** e **Publish-AppVClientPackage** são iniciados.

    -   Do início ao término da atualização da publicação. Em instâncias autônomas, este é o primeiro a último aplicativo virtual publicado.

    -   A partir do ponto em que o aplicativo virtual está disponível para ser iniciado a partir de um atalho. Como alternativa, ele é do ponto em que a associação de tipo de arquivo está registrada e iniciará um aplicativo virtual especificado.

-   **Gerenciamento de perfil de usuário** – a abordagem controlada e estruturada para gerenciar componentes do usuário associados ao ambiente. Por exemplo, perfis de usuário, gerenciamento de preferências e políticas, controle de aplicativos e implantação de aplicativos. Você pode usar scripts ou soluções de terceiros para configurar o ambiente conforme necessário.






## Tópicos relacionados


[Guia do administrador do Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)









