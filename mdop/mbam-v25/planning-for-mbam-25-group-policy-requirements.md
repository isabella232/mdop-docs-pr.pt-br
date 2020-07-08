---
title: Planejamento para os requisitos de Política de Grupo do MBAM 2.5
description: Planejamento para os requisitos de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799338"
---
# Planejamento para os requisitos de Política de Grupo do MBAM 2.5


Use as informações a seguir para determinar os tipos de protetores de BitLocker que você pode usar para gerenciar os computadores cliente do Microsoft BitLocker Administration and Monitoring (MBAM) na sua empresa.

## Tipos de protetores de BitLocker com suporte no MBAM


O MBAM dá suporte aos seguintes tipos de protetores de BitLocker.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de unidade ou volume</th>
<th align="left">Protetores de BitLocker compatíveis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Volumes do sistema operacional</p></td>
<td align="left"><ul>
<li><p><strong>Trusted Platform Module (TPM)</strong></p></li>
<li><p><strong>TPM + PIN</strong></p></li>
<li><p><strong>TPM + chave USB </strong> – compatível apenas quando o volume do sistema operacional é criptografado antes da instalação do MBAM</p></li>
<li><p><strong>A chave TPM + PIN + USB é </strong> - suportada somente quando o volume do sistema operacional é criptografado antes da instalação do MBAM</p></li>
<li><p><strong></strong> - Só há suporte para senha em dispositivos Windows to go, unidades de dados fixas e dispositivos Windows 8, Windows 8,1 e Windows 10 que não têm um TPM</p></li>
<li><p><strong>Senha numérica </strong> - aplicada automaticamente como parte da criptografia de volume e não precisa ser configurada, exceto no modo FIPS no Windows 7</p></li>
<li><p><strong>Agente de recuperação de dados (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Unidades de dados fixas</p></td>
<td align="left"><ul>
<li><p><strong>Senha</strong></p></li>
<li><p><strong>Desbloqueio automático</strong></p></li>
<li><p><strong>Senha numérica </strong> - aplicada automaticamente como parte da criptografia de volume e não precisa ser configurada, exceto no modo FIPS no Windows 7</p></li>
<li><p><strong>Agente de recuperação de dados (DRA)</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidades removíveis</p></td>
<td align="left"><ul>
<li><p><strong>Senha</strong></p></li>
<li><p><strong>Desbloqueio automático</strong></p></li>
<li><p><strong>Senha numérica </strong> - aplicada automaticamente como parte da criptografia de volume e não precisa ser configurada</p></li>
<li><p><strong>Agente de recuperação de dados (DRA)</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### Suporte para a política de criptografia do espaço usado do BitLocker

No MBAM 2,5 SP1, se você habilitar a criptografia de espaço usado via política de grupo do BitLocker, o cliente MBAM honrará-a.

Essa configuração de política de grupo é chamada **impor tipo de criptografia de unidade em unidades do sistema operacional** e está localizada no nó do GPO a seguir: modelos administrativos de **configuração de computador** &gt; **Administrative Templates** &gt; **componentes do Windows componentes** do &gt; **BitLocker Drive Encryption** &gt; **sistema operacional**da criptografia de unidade de disco rígido Se você habilitar essa política e selecionar o tipo de criptografia como **apenas criptografia de espaço usado**, o MBAM honrará a política e o BitLocker somente criptografará o espaço em disco usado no volume.

## Como obter os modelos de política de grupo do MBAM e editar as configurações


Quando estiver pronto para definir as configurações de política de grupo do MBAM desejadas, faça o seguinte:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapas para acompanhar</th>
<th align="left">Onde obter instruções</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copie os modelos de política de grupo do MBAM de <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> como obter os modelos de política de grupo do MDOP (. admx) </a> e instale-os em um computador que seja capaz de executar o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM).</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copiando os modelos de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Defina as configurações de política de grupo que você deseja usar na sua empresa.</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editando as configurações de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>



## Descrições das configurações da política de grupo do MBAM


O nó do GPO **MBAM (gerenciamento do BitLocker) do MDOP** contém quatro configurações de política global e quatro nós filho de GPO: **Gerenciamento de cliente**, **unidade fixa**, **unidade do sistema operacional**e **unidade removível**. As seções a seguir descrevem e sugerem as configurações das configurações da política de grupo do MBAM.

**Importante**  
Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente. O MBAM define automaticamente as configurações neste nó para você quando você define as configurações no nó **MDOP MBAM (gerenciamento de BitLocker)** .



### Definições globais de política de grupo

Esta seção descreve as definições de política de grupo global do MBAM no seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes** &gt; **do Windows MDOP MBAM (gerenciamento de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política de grupo sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Escolher método de criptografia de unidade e nível de codificação</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Configure essa política para usar um método de criptografia específico e um nível de codificação.</p>
<p>Quando essa política não está configurada, o BitLocker usa o método de criptografia padrão: AES 128 bits com difusor.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Um problema com o relatório de conformidade do computador BitLocker faz com que ele exiba &quot; desconhecido &quot; para o nível de codificação, mesmo se você estiver usando o valor padrão. Para solucionar esse problema, verifique se você habilitou essa configuração e defina um valor para a codificação de codificação.</p>
</div>
<div>

</div>
<ul>
<li><p>AES 128-bit com difusor – somente para Windows 7</p></li>
<li><p>AES 128 para Windows 8, Windows 8,1 e Windows 10</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Impedir substituição de memória na reinicialização</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para melhorar o desempenho de reinicialização sem substituir os segredos do BitLocker na memória na reinicialização.</p>
<p>Quando essa política não está configurada, os segredos do BitLocker são removidos da memória quando o computador é reiniciado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Validar regra de uso de certificado de cartão inteligente</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para usar a proteção do BitLocker baseada em certificados de cartão inteligente.</p>
<p>Quando essa política não está configurada, o identificador de objeto padrão 1.3.6.1.4.1.311.67.1.1 é usado para especificar um certificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fornecer os identificadores exclusivos para a sua organização</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para usar um agente de recuperação de dados baseado em certificado ou o leitor BitLocker To Go.</p>
<p>Quando essa política não está configurada, o <strong> campo de identificação </strong> não é usado.</p>
<p>Se a sua empresa exigir medidas de segurança mais altas, você poderá configurar o <strong> campo de identificação </strong> para garantir que todos os dispositivos USB tenham esse campo definido e que eles estejam alinhados com essa configuração de política de grupo.</p></td>
</tr>
</tbody>
</table>



### Definições de política de grupo do gerenciamento de cliente

Esta seção descreve as definições da política de gerenciamento de cliente para o MBAM no nó do GPO a seguir: políticas de **configuração do computador** &gt; **Policies** &gt; **modelos administrativos** do &gt; **Windows** &gt; MBAM o gerenciamento de cliente do **MDOP (gerenciamento do BitLocker)** &gt; **Gerenciamento de cliente**.

Você pode definir as mesmas configurações de política de grupo para as topologias de integração do System Center Configuration Manager autônomas e do System Center, com uma exceção: Desabilite a configuração de **ponto de extremidade do serviço de relatório de status do MBAM Services &gt; MBAM** se você estiver usando a topologia de integração do Configuration Manager, conforme indicado na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política de grupo sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar os serviços do MBAM</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<ul>
<li><p><strong>MBAM recuperação e ponto de extremidade do serviço de hardware </strong> . Use esta configuração para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM. Insira um local de ponto de extremidade semelhante ao seguinte exemplo: <strong> http:://MBAM de </strong><em> &lt; Administração e monitoração do nome do servidor &gt; </em><strong> : </strong><em> &lt; a porta que o serviço Web está associado ao &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selecione as informações de recuperação do BitLocker a serem armazenadas </strong> . Essa configuração de política permite configurar o serviço de recuperação de chave para fazer backup de informações de recuperação do BitLocker. Ele também permite que você configure um serviço de relatório de status para coletar relatórios. A política fornece um método administrativo de recuperação de dados criptografados pelo BitLocker para evitar a perda de dados devido à falta de informações importantes. O relatório de status e a atividade de recuperação de chave são enviados automaticamente e silenciosamente para o local do servidor de relatórios configurado.</p>
<p>Se você não definir essa configuração de política ou se desabilitá-la, as informações de recuperação de chave não serão salvas, e o relatório de status e a atividade de recuperação de chave não serão relatados para o servidor. Quando essa configuração é definida como <strong> senha de recuperação e pacote </strong> de chaves, a senha de recuperação e o pacote de chaves são atualizados automaticamente e silenciosamente no local do servidor de recuperação de chave configurado.</p></li>
<li><p><strong>Digite a frequência do status da verificação do cliente em minutos </strong> . Essa configuração de política gerencia com que frequência o cliente verifica as políticas de proteção do BitLocker e o status no computador cliente. Essa política também gerencia com que frequência o status de conformidade do cliente é salvo no servidor. O cliente verifica as políticas de proteção BitLocker e o status no computador cliente e também faz backup da chave de recuperação do cliente na frequência configurada.</p>
<p>Defina essa frequência com base no requisito definido por sua empresa com a frequência para verificar o status de conformidade do computador e com que frequência fazer backup da chave de recuperação do cliente.</p></li>
<li><p><strong>Ponto de extremidade do serviço de relatório de status do MBAM:</strong></p>
<p><strong>Para o MBAM em uma topologia autônoma </strong> : você deve definir essa configuração para habilitar o gerenciamento de criptografia do cliente do MBAM do cliente.</p>
<p>Insira um local de ponto de extremidade semelhante ao exemplo a seguir:</p>
<p><strong>http (s):// </strong><em> &lt; MBAM gerenciamento e monitoração do nome do servidor &gt; </em><strong> : </strong><em> &lt; a porta à qual o serviço Web está associado &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc</strong></p>
<p><strong>Para MBAM na topologia de integração do Configuration Manager </strong> : Desabilite essa configuração.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar a política de isenção de usuário</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar um endereço de site, endereço de email ou número de telefone que instrui um usuário a solicitar uma isenção da criptografia do BitLocker.</p>
<p>Se você habilitar essa configuração de política e fornecer um endereço de site, endereço de email ou número de telefone, os usuários verão uma caixa de diálogo com instruções sobre como solicitar uma isenção da proteção do BitLocker. Para obter mais informações sobre como habilitar a isenção de criptografia BitLocker para os usuários, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> como gerenciar as isenções de criptografia do BitLocker do usuário </a> .</p>
<p>Se você desabilitar ou não definir essa configuração de política, as instruções de solicitação de isenção não serão exibidas aos usuários.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isenção de usuário é gerenciada por usuário, não por computador. Se vários usuários fizerem logon no mesmo computador e qualquer usuário não estiver isento, o computador está criptografado.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar o programa de aperfeiçoamento da experiência do usuário</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política permite que você configure como os usuários do MBAM podem participar do programa de aperfeiçoamento da experiência do usuário. Este programa coleta informações sobre o hardware do computador e como os usuários usam o MBAM sem interromper o trabalho. As informações ajudam a Microsoft a identificar quais recursos do MBAM para melhorar. A Microsoft não usa essas informações para identificar ou contatar usuários do MBAM.</p>
<p>Se você habilitar essa configuração de política, os usuários poderão participar do programa de aperfeiçoamento da experiência do usuário.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão participar do programa de aperfeiçoamento da experiência do usuário.</p>
<p>Se você não definir essa configuração de política, os usuários terão a opção de participar do programa de aperfeiçoamento da experiência do usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fornecer a URL para o link de política de segurança</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Use essa configuração de política para especificar uma URL que é exibida para os usuários finais como um link chamado &quot; política de segurança da empresa. &quot; O link aponta para a política de segurança interna da sua empresa e fornece aos usuários finais informações sobre os requisitos de criptografia. O link é exibido quando os usuários são solicitados pelo MBAM para criptografar uma unidade.</p>
<p>Se você habilitar essa configuração de política, poderá configurar a URL para o link de política de segurança.</p>
<p>Se você desabilitar ou não definir essa configuração de política, o link política de segurança não será exibido para os usuários.</p></td>
</tr>
</tbody>
</table>



### Definições de política de grupo de unidade fixa

Esta seção descreve as definições de política de unidade fixa para a administração e o monitoramento do Microsoft BitLocker no seguinte nó de GPO: modelos administrativos de política de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes** &gt; **do Windows MDOP MBAM (gerenciamento de BitLocker)** &gt; **unidade fixa**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política de grupo sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações de criptografia de unidade de dados fixas</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política permite que você gerencie se as unidades de dados fixas devem ser criptografadas.</p>
<p>Se o volume do sistema operacional for necessário para ser criptografado, clique em <strong> habilitar desbloqueio automático de unidade de dados fixos </strong> .</p>
<p>Ao habilitar essa política, você não deve desabilitar a <strong> política configurar o uso da senha para unidades de dados fixas </strong> , a menos que esteja habilitando ou exigindo o uso de desbloqueio automático para unidades de dados fixas.</p>
<p>Se você precisar usar o desbloqueio automático para unidades de dados fixas, será preciso configurar os volumes do sistema operacional a serem criptografados.</p>
<p>Se você habilitar essa configuração de política, os usuários deverão colocar todas as unidades de dados fixas em proteção BitLocker e as unidades de dados serão criptografadas.</p>
<p>Se você não definir essa configuração de política, os usuários não serão obrigados a colocar unidades de dados fixas em proteção BitLocker. Se você aplicar essa política após as unidades de dados fixas serem criptografadas, o agente do MBAM descriptografará as unidades de dados fixas criptografadas.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão colocar as unidades de dados fixas na proteção BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar o acesso de gravação a unidades fixas não protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política determina se a proteção de BitLocker é necessária para que as unidades de dados fixas sejam graváveis em um computador. Essa configuração de política é aplicada quando você ativa o BitLocker.</p>
<p>Quando a política não está configurada, todas as unidades de dados fixas no computador são montadas com permissões de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades fixas protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para que unidades fixas com o sistema de arquivos FAT possam ser desbloqueadas e exibidas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Quando a política está habilitada ou não está configurada, unidades fixas formatadas com o sistema de arquivos FAT podem ser desbloqueadas e seu conteúdo pode ser visualizado em computadores que executam o Windows Server 2008, Windows Vista, Windows XP com SP3 ou Windows XP com SP2. Esses sistemas operacionais têm permissão somente leitura para unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades fixas formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades fixas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Use esta política para especificar se uma senha é necessária para desbloquear unidades de dados fixos protegidas pelo BitLocker.</p>
<p>Se você habilitar essa configuração de política, os usuários poderão configurar uma senha que atenda aos requisitos que você definir. O BitLocker permite que os usuários desbloqueiem uma unidade com qualquer um dos protetores disponíveis na unidade.</p>
<p>Essas configurações são impostas quando você ativa o BitLocker, não quando você desprotege um volume.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão usar uma senha.</p>
<p>Quando a política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para maior segurança, habilite essa política e selecione <strong> exigir senha para unidade de dados fixo </strong> , clique em <strong> exigir complexidade de senha </strong> e defina o <strong> tamanho mínimo da senha </strong> que você deseja.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão usar uma senha.</p>
<p>Se você não definir essa configuração de política, as senhas serão aceitas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades fixas protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando a política não está configurada, o agente de recuperação de dados BitLocker é permitido e não é feito o backup das informações de recuperação para o AD DS. O MBAM não requer o backup de informações de recuperação para o AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações de aplicação de política de criptografia</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Use essa configuração de política para configurar o número de dias que as unidades de dados fixas podem permanecer incompatíveis até que sejam forçadas a cumprir com as políticas de MBAM. Os usuários não podem adiar a ação necessária ou solicitar uma isenção após o período de carência. O período de carência começa quando a unidade de dados fixa é determinada como não compatível. No entanto, a política de unidade de dados fixas não é imposta até que a unidade do sistema operacional seja compatível.</p>
<p>Se o período de cortesia expirar e a unidade de dados fixa ainda não for compatível, os usuários não terão a opção de adiar ou de solicitar uma isenção. Se o processo de criptografia exigir a entrada do usuário, será exibida uma caixa de diálogo informando que os usuários não podem fechar até fornecer as informações necessárias.</p>
<p>Digite <strong> 0 </strong> em <strong> Configurar o número de dias do período de cortesia não compatível para unidades fixas </strong> para forçar o processo de criptografia a começar imediatamente após o vencimento do período de cortesia da unidade do sistema operacional.</p>
<p>Se você desabilitar ou não definir essa configuração, os usuários não serão forçados a cumprir com as políticas do MBAM.</p>
<p>Se não for necessária a interação do usuário para adicionar um protetor, a criptografia começará em segundo plano após o vencimento do período de cortesia.</p></td>
</tr>
</tbody>
</table>



### Definições de política de grupo de unidade do sistema operacional

Esta seção descreve as definições de política de unidade do sistema operacional para administração e monitoramento do Microsoft BitLocker no nó do GPO a seguir: políticas de **configuração do computador** &gt; **Policies** &gt; **modelos** do &gt; **Windows** o &gt; **MDOP MBAM (gerenciamento de BitLocker)** &gt; **unidade do sistema operacional**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política de grupo sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações de criptografia de unidade do sistema operacional</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política permite que você gerencie se a unidade do sistema operacional deve ser criptografada.</p>
<p>Para maior segurança, considere desabilitar as seguintes configurações de política nas <strong> configurações de suspensão do gerenciamento de energia do sistema </strong> &gt; <strong> </strong> &gt; <strong> </strong> ao habilitá-las com o protetor TPM + PIN:</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (bateria)</p></li>
</ul>
<p>Se você estiver executando o Microsoft Windows 8 ou posterior e desejar usar o BitLocker em um computador sem um TPM, marque a <strong> caixa de seleção Permitir BitLocker sem um TPM compatível </strong> . Nesse modo, é necessária uma senha para a inicialização. Se você esquecer a senha, será necessário usar uma das opções de recuperação do BitLocker para acessar a unidade.</p>
<p>Em um computador com um TPM compatível, dois tipos de métodos de autenticação podem ser usados na inicialização para fornecer proteção adicional para dados criptografados. Quando o computador é iniciado, ele pode usar apenas o TPM para autenticação ou também pode exigir a entrada de um PIN (número de identificação pessoal).</p>
<p>Se você habilitar essa configuração de política, os usuários precisarão colocar a unidade do sistema operacional em proteção BitLocker e a unidade será criptografada.</p>
<p>Se você desabilitar essa política, os usuários não poderão colocar a unidade do sistema operacional em proteção BitLocker. Se você aplicar essa política depois que a unidade do sistema operacional for criptografada, a unidade será descriptografada.</p>
<p>Se você não configurar essa política, a unidade do sistema operacional não precisará ser colocada em proteção BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permitir PINs aprimorados para inicialização</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Use essa configuração de política para configurar se os pinos de inicialização avançados serão usados com o BitLocker. PINs de inicialização avançados permitem o uso de caracteres, incluindo letras maiúsculas e minúsculas, símbolos, números e espaços. Essa configuração de política é aplicada quando você ativa o BitLocker.</p>
<p>Se você habilitar essa configuração de política, todos os novos PINs de inicialização do BitLocker serão habilitados para a criação de PINs avançados pelo usuário final. No entanto, nem todos os computadores podem dar suporte a pinos avançados no ambiente de pré-inicialização. É altamente recomendável que os administradores avaliem se os sistemas são compatíveis com esse recurso antes de habilitar seu uso.</p>
<p>Marque a <strong> caixa de seleção exigir Pins somente ASCII </strong> para ajudar a melhorar o redimensionamento de pinos aprimorados com computadores que limitam o tipo ou o número de caracteres que podem ser inseridos no ambiente de pré-inicialização.</p>
<p>Se você desabilitar ou não definir essa configuração de política, os PINs avançados não serão usados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades do sistema operacional protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando essa política não está configurada, o agente de recuperação de dados é permitido e não é feito o backup das informações de recuperação no AD DS.</p>
<p>A operação MBAM não exige o backup de informações de recuperação para o AD DS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso de senhas para unidades do sistema operacional</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Use essa configuração de política para definir as restrições para senhas usadas para desbloquear unidades do sistema operacional protegidas pelo BitLocker. Se protetores não TPM forem permitidos em unidades do sistema operacional, você poderá provisionar uma senha, impor requisitos de complexidade na senha e configurar um comprimento mínimo para a senha. Para que a configuração de requisito de complexidade seja eficiente, você também deve habilitar a configuração de política de grupo a &quot; senha deve atender aos requisitos &quot; de complexidade localizados em configurações do computador configurações de segurança das &gt; políticas de &gt; &gt; conta política de &gt; senha.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Essas configurações são impostas quando você ativa o BitLocker, não quando você desprotege um volume. O BitLocker permite desbloquear uma unidade com qualquer um dos protetores disponíveis na unidade.</p>
</div>
<div>

</div>
<p>Se você habilitar essa configuração de política, os usuários poderão configurar uma senha que atenda aos requisitos que você definir. Para impor requisitos de complexidade na senha, clique em <strong> exigir complexidade de senha </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar o perfil de validação da plataforma TPM para configurações de firmware baseado em BIOS</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar como o computador&#39;s o hardware de segurança do TPM (Trusted Platform Module) protege a chave de criptografia do BitLocker. Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver sido ativado com a proteção TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Essa configuração de política de grupo se aplica somente a computadores com configurações de BIOS ou a computadores com firmware UEFI com um módulo de serviço de compatibilidade (CSM) habilitado. Os computadores que usam uma configuração nativa de firmware UEFI armazenam valores diferentes nos registros de configuração de plataforma (PCRs). Use a &quot; configuração de política de grupo configurar o perfil de validação da plataforma TPM para configurações de firmware nativa de UEFI &quot; para configurar o perfil de PCRs de TPM para computadores que usam firmware UEFI nativo.</p>
</div>
<div>

</div>
<p>Se você habilitar essa configuração de política antes de ativar o BitLocker, poderá configurar os componentes de inicialização validados pelo TPM antes de desbloquear o acesso à unidade do sistema operacional criptografada pelo BitLocker. Se qualquer um desses componentes mudar durante a proteção BitLocker estar em vigor, o TPM não libera a chave de criptografia para desbloquear a unidade e o computador, em vez disso, exibe o console de recuperação do BitLocker e requer que você forneça a senha de recuperação ou a chave de recuperação para desbloquear a unidade.</p>
<p>Se você desabilitar ou não definir essa configuração de política, o BitLocker usará o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o perfil de validação da plataforma TPM</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar como o computador&#39;s o hardware de segurança do TPM (Trusted Platform Module) protege a chave de criptografia do BitLocker. Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver sido ativado com a proteção TPM.</p>
<p>Se você habilitar essa configuração de política antes de ativar o BitLocker, poderá configurar os componentes de inicialização validados pelo TPM antes de desbloquear o acesso à unidade do sistema operacional criptografada pelo BitLocker. Se qualquer um desses componentes mudar durante a proteção BitLocker estar em vigor, o TPM não libera a chave de criptografia para desbloquear a unidade e o computador, em vez disso, exibe o console de recuperação do BitLocker e requer que você forneça a senha de recuperação ou a chave de recuperação para desbloquear a unidade.</p>
<p>Se você desabilitar ou não definir essa configuração de política, o BitLocker usará o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar o perfil de validação da plataforma TPM para configurações nativas de firmware UEFI</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar como o computador&#39;s o hardware de segurança do TPM (Trusted Platform Module) protege a chave de criptografia do BitLocker. Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver sido ativado com a proteção TPM.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Essa configuração de política de grupo se aplica somente a computadores com uma configuração nativa de firmware UEFI.</p>
</div>
<div>

</div>
<p>Se você habilitar essa configuração de política antes de ativar o BitLocker, poderá configurar os componentes de inicialização validados pelo TPM antes de desbloquear o acesso à unidade do sistema operacional criptografada pelo BitLocker. Se qualquer um desses componentes mudar durante a proteção BitLocker estar em vigor, o TPM não libera a chave de criptografia para desbloquear a unidade e o computador, em vez disso, exibe o console de recuperação do BitLocker e requer que você forneça a senha de recuperação ou a chave de recuperação para desbloquear a unidade.</p>
<p>Se você desabilitar ou não definir essa configuração de política, o BitLocker usará o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Redefinir os dados de validação da plataforma após a recuperação do BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Use essa configuração de política para controlar se os dados de validação de plataforma são atualizados quando o Windows é iniciado após a recuperação do BitLocker.</p>
<p>Se você habilitar essa configuração de política, os dados de validação da plataforma serão atualizados quando o Windows for iniciado após a recuperação do BitLocker. Se você desabilitar essa configuração de política, os dados de validação da plataforma não serão atualizados quando o Windows for iniciado após a recuperação do BitLocker. Se você não definir essa configuração de política, os dados de validação da plataforma serão atualizados quando o Windows for iniciado após a recuperação do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar perfil de validação de dados de configuração de inicialização avançada</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite que você escolha configurações de dados de configuração de inicialização específicas (BCD) para verificar durante a validação da plataforma.</p>
<p>Se você habilitar essa configuração de política, poderá adicionar mais configurações, remover as configurações padrão ou ambas. Se você desabilitar essa configuração de política, o computador será revertido para um perfil BCD semelhante ao perfil BCD padrão usado pelo Windows 7. Se você não definir essa configuração de política, o computador verificará as configurações padrão de BCD do Windows.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Quando o BitLocker usa a inicialização segura para a validação da integridade dos dados de configuração de inicialização e de plataforma (BCD), conforme definido pela &quot; política permitir inicialização segura para validação de integridade &quot; , a &quot; política usar perfil de validação de dados de configuração de inicialização avançada &quot; é ignorada.</p>
</div>
<div>

</div>
<p>A configuração que controla a depuração de inicialização (0x16000010) é sempre validada e não tem efeito se estiver incluída nos campos fornecidos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações de aplicação de política de criptografia</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Use essa configuração de política para configurar o número de dias pelos quais os usuários podem adiar a conformidade com as políticas do MBAM para a unidade do sistema operacional. O período de cortesia começa quando o sistema operacional é detectado pela primeira vez como não compatível. Depois que esse período de cortesia expirar, os usuários não poderão adiar a ação necessária ou solicitar uma isenção a ele.</p>
<p>Se o processo de criptografia exigir a entrada do usuário, será exibida uma caixa de diálogo informando que os usuários não podem fechar até fornecer as informações necessárias.</p>
<p>Se você desabilitar ou não definir essa configuração, os usuários não serão forçados a cumprir com as políticas do MBAM.</p>
<p>Se não for necessária a interação do usuário para adicionar um protetor, a criptografia começará em segundo plano após o vencimento do período de cortesia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar a URL e mensagem de recuperação antes da inicialização</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa configuração de política para configurar uma mensagem de recuperação personalizada ou para especificar uma URL que será exibida na tela pré-inicialização de recuperação do BitLocker quando a unidade do sistema operacional estiver bloqueada. Essa configuração só está disponível em computadores cliente que executam o Windows 10.</p>
<p>Quando essa política está habilitada, você pode selecionar uma destas opções para a mensagem de recuperação de pré-inicialização:</p>
<ul>
<li><p><strong>Usar mensagem de recuperação personalizada </strong> : Selecione esta opção para incluir uma mensagem personalizada na tela pré-inicialização de recuperação do BitLocker. Na <strong> caixa de opção mensagem de recuperação personalizada </strong> , digite a mensagem que você deseja exibir. Se você também quiser especificar uma URL de recuperação, inclua-a como parte da sua mensagem de recuperação personalizada.</p></li>
<li><p><strong>Usar a URL de recuperação personalizada </strong> : Selecione esta opção para substituir a URL padrão que é exibida na tela pré-inicializar do BitLocker Recovery. Na <strong> caixa de opção a URL de recuperação personalizada </strong> , digite a URL que você deseja exibir.</p></li>
<li><p><strong>Usar a mensagem e a URL de recuperação padrão </strong> : Selecione esta opção para exibir a mensagem e a URL de recuperação do BitLocker padrão na tela pré-inicialização de recuperação do BitLocker. Se você configurou anteriormente uma mensagem ou URL de recuperação personalizada e quer reverter para a mensagem padrão, você deve habilitar essa política e selecionar a <strong> opção usar mensagem de recuperação e URL padrão </strong> .</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Nem todos os caracteres e idiomas têm suporte na pré-inicialização. Recomendamos que você teste se os caracteres que você usa para a mensagem ou a URL personalizada aparecem corretamente na tela de recuperação do BitLocker de pré-inicialização.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### Definições de política de grupo de unidade removível

Esta seção descreve as definições de política de grupo de unidade removível para administração e monitoramento do Microsoft BitLocker no nó do GPO a seguir: políticas de **configuração do computador** &gt; **Policies** &gt; **modelos** &gt; do **Windows** o &gt; **MDOP MBAM (gerenciamento de BitLocker)** &gt; **unidade removível**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política de grupo sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlar o uso do BitLocker em unidades removíveis</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Esta política controla o uso do BitLocker em unidades de dados removíveis.</p>
<p>Clique em <strong> permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> para permitir que os usuários executem o assistente de configuração do BitLocker em uma unidade de dados removível.</p>
<p>Clique em <strong> permitir que os usuários suspendam e descriptografem o BitLocker em unidades de dados removíveis </strong> para permitir que os usuários removam a criptografia de unidade de disco BitLocker da unidade ou para suspender a criptografia enquanto a manutenção é realizada.</p>
<p>Quando essa política está habilitada e você clica em <strong> permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , o cliente MBAM salva as informações de recuperação sobre unidades removíveis no servidor de recuperação de chave do MBAM e permite que os usuários recuperem a unidade se a senha for perdida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar o acesso de gravação a unidades removíveis não protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir somente permissões de gravação para unidades protegidas pelo BitLocker.</p>
<p>Quando essa política está habilitada, todas as unidades de dados removíveis no computador exigem Criptografia antes que a permissão de gravação seja permitida.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades removíveis protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir que unidades fixas com o sistema de arquivos FAT sejam desbloqueadas e exibidas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Quando essa política não está configurada, as unidades removíveis formatadas com o sistema de arquivos FAT podem ser desbloqueadas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2, e o conteúdo pode ser exibido. Esses sistemas operacionais têm permissão somente leitura para unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades removíveis formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades de dados removíveis</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para configurar a proteção por senha em unidades de dados removíveis.</p>
<p>Quando essa política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para aumentar a segurança, você pode habilitar essa política e selecionar <strong> exigir senha para unidade de dados removível </strong> , clicar em <strong> exigir complexidade de senha </strong> e definir o <strong> comprimento mínimo de senha preferencial </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades removíveis protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando definido como <strong> não configurado </strong> , o agente de recuperação de dados é permitido e não é feito backup das informações de recuperação no AD DS.</p>
<p>A operação MBAM não exige o backup de informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>




## Tópicos relacionados


[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Pré-requisitos para implantação do MBAM 2.5](mbam-25-deployment-prerequisites.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






