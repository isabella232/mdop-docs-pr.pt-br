---
title: Sobre o MBAM 2.5
description: Sobre o MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799427"
---
# Sobre o MBAM 2.5


O monitoramento e a administração do Microsoft BitLocker (MBAM) 2,5 fornecem uma interface administrativa simplificada para a criptografia de unidade de disco BitLocker. O BitLocker oferece proteção aprimorada contra roubo de dados ou exposição de dados para computadores perdidos ou roubados. O BitLocker criptografa todos os dados armazenados nos volumes e unidades de sistema operacional Windows e nas unidades de dados configurados.

## Visão geral do MBAM


O MBAM 2,5 tem os seguintes recursos:

-   Permite que os administradores automatizem o processo de criptografar volumes em computadores cliente em toda a empresa.

-   Permite que os agentes de segurança determinem rapidamente o estado de conformidade de computadores individuais ou até mesmo da empresa em si.

-   Fornece gerenciamento centralizado de relatório e de hardware com o Microsoft System Center Configuration Manager.

-   Reduz a carga de trabalho no suporte técnico para ajudar os usuários finais com o PIN do BitLocker e solicitações de chave de recuperação.

-   Permite aos usuários finais recuperar dispositivos criptografados de forma independente, usando o Portal de Autoatendimento.

-   Permite que os gerentes de segurança auditem facilmente o acesso para recuperar informações importantes.

-   Permite que os usuários do Windows Enterprise continuem a trabalhar em qualquer lugar com a garantia de que seus dados corporativos estão protegidos.

O MBAM impõe as opções de política de criptografia BitLocker definidas para a sua empresa, monitora a conformidade dos computadores cliente com essas políticas e relata sobre o status de criptografia dos computadores da empresa e do indivíduo. Além disso, o MBAM permite que você acesse as informações da chave de recuperação quando os usuários esquecem o PIN ou a senha, ou quando os registros de inicialização ou do BIOS são alterados.

Os seguintes grupos podem estar interessados em usar o MBAM para gerenciar o BitLocker:

-   Administradores, profissionais de segurança de ti e responsáveis pela conformidade responsáveis por garantir que os dados confidenciais não sejam divulgados sem autorização

-   Administradores que são responsáveis por segurança de computador em escritórios remotos ou filiais

-   Administradores responsáveis pelos computadores cliente que executam o Windows

**Observação**  O BitLocker não é explicado em detalhes nesta documentação do MBAM. Para obter mais informações, consulte [visão geral da criptografia de unidade BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>O que há de novo no MBAM 2,5


Esta seção descreve os novos recursos do MBAM 2,5.

### Suporte para o Microsoft SQL Server 2014

O MBAM adiciona suporte ao Microsoft SQL Server 2014, além do mesmo software com suporte em versões anteriores do MBAM.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> MBAM de modelos de política de grupo baixados separadamente

Os modelos de política de grupo do MBAM devem ser baixados separadamente da instalação do MBAM. Em versões anteriores do MBAM, o instalador do MBAM incluiu um modelo de política de MBAM, que continha os objetos de política de grupo (GPOs) necessários do MBAM que definem as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker. Esses GPOs foram removidos do instalador do MBAM. Agora, você pode baixar os GPOs em [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou uma estação de trabalho antes de iniciar a instalação do cliente do MBAM. Você pode copiar os modelos de política de grupo para qualquer servidor ou estação de trabalho que esteja executando uma versão com suporte do Windows Server ou sistema operacional Windows.

**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente. Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de criptografia de unidade de disco BitLocker para você.

 

Os arquivos de modelo que você precisa copiar para um servidor ou estação de trabalho são:

-   BitLockerManagement. adml

-   BitLockerManagement. admx

-   BitLockerUserManagement. adml

-   BitLockerUserManagement. admx

Copie os arquivos de modelo para o local mais adequado às suas necessidades. Para os arquivos específicos do idioma, que devem ser copiados para uma pasta específica do idioma, o console de gerenciamento de política de grupo é necessário para exibir os arquivos.

- Para instalar os arquivos de modelo localmente em um servidor ou uma estação de trabalho, copie os arquivos para um dos locais a seguir.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo de arquivo</th>
  <th align="left">Local do arquivo</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>idioma neutro (. admx)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>específico do idioma (. adml)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (por exemplo, o arquivo específico do idioma inglês dos EUA será armazenado em <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

- Para disponibilizar os modelos para todos os administradores de política de grupo em um domínio, copie os arquivos para um dos locais a seguir em um controlador de domínio.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo de arquivo</th>
  <th align="left">Local do arquivo do controlador de domínio</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>Idioma neutro (. admx)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>Específico do idioma (. adml)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (por exemplo, o arquivo específico do idioma inglês dos EUA será armazenado em <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

Para obter mais informações sobre arquivos de modelo, consulte o [guia passo a passo sobre como gerenciar arquivos ADMX de política de grupo](https://go.microsoft.com/fwlink/?LinkId=392818).

### Capacidade de impor políticas de criptografia no sistema operacional e unidades de dados fixas

O MBAM 2.5 permite que você aplique políticas de criptografia no sistema operacional e unidades de dados fixas para computadores em sua organização e limite o número de dias que os usuários finais podem solicitar um adiamento da necessidade de atender às políticas de criptografia do MBAM.

Para permitir que você configure a aplicação de políticas de criptografia, uma nova configuração de política de grupo, chamada de política de aplicação de criptografia, foi adicionada para unidades do sistema operacional e unidades de dados fixas. Essa política é descrita na tabela a seguir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração da Política de Grupo</th>
<th align="left">Descrição</th>
<th align="left">Nó de política de grupo usado para definir essa configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações de imposição de política de criptografia (unidade do sistema operacional)</p></td>
<td align="left"><p>Para essa configuração, use a opção <strong> Configurar o número de dias do período de cortesia não compatível para unidades do sistema operacional </strong> para configurar um período de cortesia.</p>
<p>O período de carência especifica o número de dias pelos quais os usuários finais podem adiar a conformidade com as políticas do MBAM para a unidade do sistema operacional após a primeira detecção da unidade como não compatível.</p>
<p>Depois que o período de cortesia configurado expirar, os usuários não poderão adiar a ação necessária ou solicitar uma isenção a ele.</p>
<p>Se a interação do usuário for necessária (por exemplo, se você estiver usando o TPM (Trusted Platform Module) + PIN ou usando um protetor de senha, será exibida uma caixa de diálogo e os usuários não poderão fechá-lo até fornecer as informações necessárias. Se o protetor for somente TPM, a criptografia começará imediatamente em segundo plano sem a entrada do usuário.</p>
<p>Os usuários não podem solicitar isenções por meio do assistente de criptografia BitLocker. Em vez disso, eles devem entrar em contato com o suporte técnico ou usar qualquer processo que sua organização usa para solicitações de isenção.</p></td>
<td align="left"><p>Políticas de configuração do computador &gt; &gt; modelos administrativos &gt; componentes &gt; do Windows MDOP MBAM (gerenciamento de BitLocker) &gt; unidade do sistema operacional</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações de imposição de política de criptografia (unidades de dados fixas)</p></td>
<td align="left"><p>Para essa configuração, use a opção <strong> Configurar o número de dias do período de cortesia não compatível para unidades fixas </strong> para configurar um período de cortesia.</p>
<p>O período de carência especifica o número de dias pelos quais os usuários finais podem adiar a conformidade com as políticas MBAM para a unidade fixa após a primeira detecção da unidade como não compatível.</p>
<p>O período de cortesia começa quando a unidade fixa é determinada como não compatível. Se você estiver usando o desbloqueio automático, a política não será imposta até que a unidade do sistema operacional seja compatível. No entanto, se você não estiver usando o desbloqueio automático, a criptografia da unidade de dados fixa pode começar antes que a unidade do sistema operacional seja totalmente criptografada.</p>
<p>Depois que o período de cortesia configurado expirar, os usuários não poderão adiar a ação necessária ou solicitar uma isenção a ele. Se a interação do usuário for necessária, uma caixa de diálogo será exibida e os usuários não poderão fechá-la até fornecer as informações necessárias.</p></td>
<td align="left"><p>Políticas de configuração do computador &gt; &gt; modelos administrativos &gt; componentes &gt; do Windows MDOP MBAM (gerenciamento de BitLocker) &gt; unidade fixa</p></td>
</tr>
</tbody>
</table>

 

### Capacidade de fornecer uma URL no assistente de criptografia de unidade BitLocker para apontar para sua política de segurança

Uma nova configuração de política de grupo, **forneça a URL para o link de política de segurança**, permite que você configure uma URL que será apresentada aos usuários finais como um link chamado **política de segurança da empresa**. Esse link será exibido quando o MBAM solicitar que os usuários criptografem um volume.

Se você habilitar essa configuração de política, poderá configurar a URL para o link de **política de segurança da empresa** . Se você desabilitar ou não definir essa configuração de política, o link **política de segurança da empresa** não será exibido para os usuários.

A nova configuração de política de grupo está localizada no seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MDOP MBAM (gerenciamento de BitLocker) &gt; Gerenciamento de cliente**.

### Suporte para chaves de recuperação compatíveis com FIPS

O MBAM 2.5 é compatível com as chaves de recuperação do BitLocker compatíveis com o padrão FIPS (Federal Information Processing Standard) em dispositivos que executam o sistema operacional Windows 8.1. A chave de recuperação não é compatível com FIPS nas versões anteriores do Windows. Esse aperfeiçoamento aprimora o processo de recuperação de unidade em organizações que exigem conformidade com FIPS porque permite que os usuários finais usem o portal de autoatendimento ou o site de administração e monitoramento (Help Desk) para recuperar suas unidades se eles esquecerem do PIN ou da senha ou ficarão bloqueados em seus computadores. O novo recurso de conformidade com FIPS não se estende a protetores de senha.

Para habilitar a conformidade com FIPS em sua organização, você deve configurar as configurações de política de grupo do padrão FIPS (padrão de processamento de informações federais). Para obter instruções de configuração, consulte [configurações de política de grupo BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

Para computadores cliente que executam os sistemas operacionais Windows8 ou Windows7 sem o [hotfix do BitLocker instalado](https://support.microsoft.com/kb/3015477), os administradores de ti continuarão usando o protetor de Data Recovery Agents (Dra) em ambientes compatíveis com FIPS. Para obter informações sobre DRA, consulte [usando agentes de recuperação de dados com o BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

Consulte [pacote de hotfix 2 para administração e monitoramento do bitlocker 2,5](https://support.microsoft.com/kb/3015477) para baixar e instalar o hotfix do BitLocker para computadores com o Windows 7 e o Windows 8.

### Suporte para implantações de alta disponibilidade

O MBAM é compatível com os seguintes cenários de alta disponibilidade, além das topologias padrão de integração de dois servidores e do Configuration Manager:

-   Grupos de disponibilidade do SQL Server AlwaysOn

-   Clustering do SQL Server

-   Balanceamento de carga de rede (NLB)

-   Espelhamento do SQL Server

-   Backup do Volume Shadow Copy Service (VSS)

Para obter mais informações sobre esses recursos, confira [planejando a alta disponibilidade do MBAM 2,5](planning-for-mbam-25-high-availability.md).

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>Gerenciamento de funções para administração e monitoramento do site alterado

No MBAM 2.5, você deve criar grupos de segurança nos serviços de domínio Active Directory (ADDS) para gerenciar as funções que fornecem direitos de acesso ao site de administração e monitoramento. As funções permitem que os usuários de grupos de segurança específicos realizem tarefas diferentes no site, como a exibição de relatórios ou a ajuda de usuários finais a recuperarem unidades criptografadas. Em versões anteriores do MBAM, as funções eram gerenciadas por meio de grupos locais.

No MBAM 2.5, o termo "funções" substitui o termo "funções de administrador", que foi usado em versões anteriores do MBAM. Além disso, no MBAM 2.5, a função "administradores de sistema do MBAM" foi removida.

A tabela a seguir lista os grupos de segurança que você deve criar no AD DS. Você pode usar qualquer nome para os grupos de segurança.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Função</th>
<th align="left">Direitos de acesso para esta função no site de administração e monitoramento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Fornece acesso às áreas gerenciar TPM e recuperação de unidade do site de administração e monitoramento do MBAM. Os usuários que têm acesso a essas áreas devem preencher todos os campos quando usarem qualquer uma das áreas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Fornece acesso aos relatórios no site Administração e monitoramento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Fornece acesso a todas as áreas no site de administração e monitoramento. Os usuários neste grupo precisam inserir apenas a chave de recuperação, e não o domínio do usuário final e o nome de usuário, ao ajudar os usuários finais a recuperarem suas unidades. Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados da assistência técnica do MBAM, o MBAM permissões do grupo usuários da assistência avançada do MBAM substituirá as permissões do grupo usuários da assistência técnica do.</p></td>
</tr>
</tbody>
</table>

 

Depois de criar os grupos de segurança em Adicionar, atribua usuários e/ou grupos ao grupo de segurança apropriado para habilitar o nível de acesso correspondente ao site de administração e monitoramento. Para habilitar as pessoas com cada função para acessar o site de administração e monitoramento, você também deve especificar cada grupo de segurança quando estiver configurando o site de administração e monitoramento.

### Cmdlets do Windows PowerShell para configurar os recursos do MBAM Server

Os cmdlets do Windows PowerShell para MBAM 2.5 permitem que você configure e gerencie os recursos do servidor MBAM. Cada recurso tem um cmdlet do Windows PowerShell correspondente que você pode usar para habilitar ou desabilitar recursos ou para obter informações sobre o recurso.

Para pré-requisitos e pré-requisitos para usar o Windows PowerShell, consulte [configurando recursos do MBAM 2,5 Server usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

**Para carregar a ajuda do MBAM 2,5 para cmdlets do Windows PowerShell após instalar o software do MBAM Server**

1.  Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).

2.  Digite **Update-Help – módulo Microsoft. MBAM**.

A ajuda do Windows PowerShell para MBAM está disponível nos seguintes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ajuda do Windows PowerShell</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções na seção anterior sobre como carregar a ajuda do Windows PowerShell para MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>No TechNet como páginas da Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>No centro de download como um arquivo. docx do Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>No centro de download como um arquivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### Suporte para PINs de somente ASCII e aprimorados e capacidade para evitar caracteres sequenciais e de repetição

**Permitir PINs avançados para a configuração da política de grupo de inicialização**

A configuração de política de grupo, **permitir pinos aprimorados para inicialização**, permite que você configure se os Pins de inicialização avançados serão usados com o BitLocker. PINs de inicialização avançados permitem que os usuários insiram teclas em um teclado completo, incluindo letras maiúsculas e minúsculas, símbolos, números e espaços. Se você habilitar essa configuração de política, todos os novos PINs de inicialização do BitLocker definidos serão PINs aprimorados. Se você desabilitar ou não definir essa configuração de política, PINs avançados não poderão ser usados.

Nem todos os computadores dão suporte à entrada de pinos aprimorados no ambiente de execução antes da inicialização (PXE). Antes de habilitar essa configuração de política de grupo para sua organização, execute uma verificação do sistema durante o processo de configuração do BitLocker para garantir que o BIOS do computador seja compatível com o uso do teclado completo no PXE. Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

**Caixa de seleção exigir pinos somente ASCII**

A configuração **permitir pinos aprimorados para a política de grupo de inicialização** também contém a caixa de seleção **exigir Pins somente ASCII** . Se os computadores de sua organização não tiverem suporte para o uso do teclado completo em PXE, você poderá habilitar a caixa de seleção **permitir pinos aprimorados para** a configuração de política de grupo e, em seguida, marcar a caixa de seleção **exigir Pins somente ASCII** para exigir que os Pins aprimorados usem apenas caracteres ASCII imprimíveis.

**Uso imposto de caracteres não sequenciais e não repetitivos**

O MBAM 2.5 impede que os usuários finais criem PINs que consistem em números de repetição (como 1111) ou números sequenciais (como o 1234). Se os usuários finais tentarem inserir uma senha que contenha três ou mais números de repetição ou sequencial, o assistente de criptografia de unidade de disco BitLocker exibirá uma mensagem de erro e impedirá que os usuários insiram um PIN com os caracteres proibidos.

### Adição de certificado DRA ao relatório de conformidade do computador BitLocker

Um novo tipo de protetor, o certificado de agente de recuperação de dados (DRA), foi adicionado ao relatório de conformidade do computador BitLocker no Configuration Manager. Esse tipo de protetor aplica-se às unidades do sistema operacional, e ele aparece na seção **volume (s) do computador** na coluna **tipos de protetor** .

### Suporte para implantações de suporte de várias florestas

O MBAM 2,5 oferece suporte aos seguintes tipos de implantação de várias florestas:

-   Floresta única com um único domínio

-   Floresta única com uma única árvore e vários domínios

-   Floresta única com vários namespaces de árvores e disjunção

-   Várias florestas em uma topologia de floresta central

-   Várias florestas em uma topologia de floresta de recursos

Não há suporte para migração de floresta (indo de simples para vários, múltiplo para único, recurso para toda a floresta etc.) ou atualização ou downgrade.

Os pré-requisitos para a implantação do MBAM em implantações de várias florestas são:

-   A floresta deve estar em execução em versões compatíveis do Windows Server.

-   Uma relação de confiança bidirecional ou unidirecional é necessária. As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente. Em outras palavras, o domínio do servidor é apontado no domínio do cliente.

### Suporte do cliente MBAM para discos rígidos criptografados

O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667. Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada. Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .

## Como obter tecnologias do MDOP


O MBAM é parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do programa Microsoft Software Assurance. Para obter mais informações sobre o programa Microsoft Software Assurance e como adquirir o MDOP, consulte [como faço para obter o MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## <a href="" id="---------mbam-2-5-release-notes"></a> Notas de versão do MBAM 2,5


Para obter mais informações e últimas notícias que não estão incluídas nesta documentação, confira [notas de versão do MBAM 2,5](release-notes-for-mbam-25.md).

## Tem uma sugestão para o MBAM?
- Envie seus comentários [aqui](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Tópicos relacionados


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

 

 





