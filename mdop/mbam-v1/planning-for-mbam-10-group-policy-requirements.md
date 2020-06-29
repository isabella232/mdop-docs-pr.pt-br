---
title: Planejar Requisitos de Política de Grupo do MBAM 1.0
description: Planejar Requisitos de Política de Grupo do MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795999"
---
# Planejar Requisitos de Política de Grupo do MBAM 1.0


O gerenciamento de clientes de administração e monitoramento do Microsoft BitLocker (MBAM) exige a aplicação de configurações personalizadas de política de grupo. Este tópico descreve as opções de política disponíveis para objeto de política de grupo (GPO) quando você usa o MBAM para gerenciar a criptografia de unidade de disco BitLocker na empresa.

**Importante**  
O MBAM não usa as configurações padrão de GPO para criptografia de unidade de disco BitLocker do Windows. Se as configurações padrão estiverem habilitadas, elas poderão causar um comportamento conflitante. Para permitir que o MBAM gerencie o BitLocker, você deve definir as configurações de política de GPO após a instalação do modelo de política de grupo do MBAM.



Depois de instalar o modelo de política de grupo do MBAM, você pode exibir e modificar as configurações de política de GPO de MBAM personalizadas disponíveis para permitir que o MBAM gerencie a criptografia do BitLocker corporativo. O modelo de política de grupo MBAM deve ser instalado em um computador que seja capaz de executar o console de gerenciamento de política de grupo (GPMC) ou a tecnologia avançada do MDOP do gerenciamento de política de grupo (AGPM). Em seguida, para editar o GPO aplicável, abra o GPMC ou o AGPM e navegue até o nó do GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**.

O nó do GPO MBAM (gerenciamento do BitLocker) do MDOP contém quatro configurações de política global e quatro nós de configuração de GPO filho, respectivamente. As quatro configurações de política global de GPO são: gerenciamento de cliente, unidade fixa, unidade do sistema operacional e unidade removível. As seções a seguir fornecem definições de política e configurações de política sugeridas para ajudá-lo a planejar os requisitos de configuração de política de GPO MBAM.

**Observação**  
Para obter mais informações sobre como definir as configurações mínimas de GPO sugeridas para permitir que o MBAM gerencie a criptografia do BitLocker, consulte [como editar configurações de GPO MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).



## Definições de política global


Esta seção descreve as definições de política global do MBAM, que podem ser encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configuração de política sugerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Escolher método de criptografia de unidade e nível de codificação</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para usar um método de criptografia específico e um nível de codificação.</p>
<p>Quando essa política não está configurada, o BitLocker usa o método de criptografia padrão do AES 128-bit com difusor ou o método de criptografia especificado pelo script de instalação.</p></td>
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
<p>Quando essa política não está configurada, um identificador de objeto padrão 1.3.6.1.4.1.311.67.1.1 é usado para especificar um certificado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fornecer os identificadores exclusivos para a sua organização</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para usar um agente de recuperação de dados baseado em certificado ou o leitor BitLocker To Go.</p>
<p>Quando essa política não está configurada, o <strong> campo de identificação </strong> não é usado.</p>
<p>Se a sua empresa exigir medidas de segurança superiores, talvez você queira configurar <strong> o </strong> campo de identificação para garantir que todos os dispositivos USB tenham esse campo definido e que eles estejam alinhados com essa configuração de política de grupo.</p></td>
</tr>
</tbody>
</table>



## Definições da política de gerenciamento de cliente


Esta seção descreve as definições da política de gerenciamento de cliente para MBAM, encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **Gerenciamento de cliente**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configurações de política sugeridas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar os serviços do MBAM</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<ul>
<li><p><strong>MBAM recuperação e ponto de extremidade do serviço de hardware </strong> . Esta é a primeira configuração de política que você deve configurar para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM. Para essa configuração, insira o local do ponto de extremidade semelhante ao exemplo a seguir: <strong> http:// </strong><em> &lt; MBAM administração e monitoramento nome &gt; </em><strong> do servidor de monitoramento: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selecione as informações de recuperação do BitLocker a serem armazenadas </strong> . Essa configuração de política permite configurar o serviço de recuperação de chave para fazer backup das informações de recuperação do BitLocker. Ele também permite configurar o serviço de relatório de status para coletar relatórios de conformidade e auditoria. A política fornece um método administrativo de recuperação de dados criptografados pelo BitLocker para ajudar a evitar a perda de dados devido à falta de informações importantes. O relatório de status e a atividade de recuperação de chave serão enviados automaticamente e silenciosamente para o local do servidor de relatório configurado.</p>
<p>Se você não configurar ou se desabilitar essa configuração de política, as informações de recuperação de chave não serão salvas, e o relatório de status e a atividade de recuperação de chave não serão relatados ao servidor. Quando essa configuração estiver definida como <strong> senha de recuperação e pacote </strong> de chaves, a senha de recuperação e o pacote de chaves serão automaticamente e, em seguida, o backup será silenciosa para o local do servidor de recuperação de chave configurado.</p></li>
<li><p><strong>Digite a frequência de verificação do status do cliente em minutos </strong> . Essa configuração de política gerencia com que frequência o cliente verifica as políticas de proteção BitLocker e o status no computador cliente. Essa política também gerencia com que frequência o status de conformidade do cliente é salvo no servidor. O cliente verifica as políticas de proteção BitLocker e o status no computador cliente e também faz backup da chave de recuperação do cliente na frequência configurada.</p>
<p>Defina essa frequência com base na necessidade estabelecida pela sua empresa com a frequência para verificar o status de conformidade do computador e com que frequência fazer backup da chave de recuperação do cliente.</p></li>
<li><p><strong>Ponto de extremidade do serviço de relatório de status do MBAM </strong> . Esta é a segunda configuração de política que você deve configurar para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM. Para essa configuração, insira o local do ponto de extremidade usando o seguinte exemplo: <strong> http:// </strong><em> &lt; MBAM administração e monitoramento nome &gt; </em><strong> do servidor de monitoramento: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService. svc </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permitir verificação de compatibilidade de hardware</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política permite que você gerencie a verificação de compatibilidade de hardware antes de habilitar a proteção BitLocker em unidades de computadores cliente do MBAM.</p>
<p>Você deve habilitar essa opção de política se a sua empresa tiver hardware de computador ou computadores mais antigos que não dão suporte ao Trusted Platform Module (TPM). Se qualquer um desses critérios for verdadeiro, habilite a verificação de compatibilidade de hardware para garantir que o MBAM seja aplicado somente a modelos de computador que dão suporte ao BitLocker. Se todos os computadores de sua organização oferecerem suporte ao BitLocker, você não precisará implantar a compatibilidade de hardware e poderá definir essa política como <strong> não configurada </strong> .</p>
<p>Se você habilitar essa configuração de política, o modelo do computador será validado em relação à lista de compatibilidade de hardware uma vez a cada 24 horas, antes que a política habilite a proteção BitLocker em uma unidade de computador.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Antes de habilitar essa configuração de política, verifique se você configurou a <strong> configuração de ponto de extremidade do serviço de hardware e recuperação do MBAM </strong> nas <strong> Opções de política configurar serviços MBAM </strong> .</p>
</div>
<div>

</div>
<p>Se você desabilitar ou não definir essa configuração de política, o modelo do computador não será validado em relação à lista de compatibilidade de hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar a política de isenção de usuário</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar um endereço de site, endereço de email ou número de telefone que instruirá o usuário a solicitar uma isenção da criptografia do BitLocker.</p>
<p>Se você habilitar essa configuração de política e fornecer um endereço de site, endereço de email ou número de telefone, os usuários verão uma caixa de diálogo com instruções sobre como solicitar uma isenção da proteção do BitLocker. Para obter mais informações sobre como habilitar as isenções de criptografia BitLocker para usuários, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> como gerenciar isenções de criptografia de usuário do usuário </a> .</p>
<p>Se você desabilitar ou não definir essa configuração de política, as instruções sobre como solicitar uma solicitação de isenção não serão apresentadas aos usuários.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isenção de usuário é gerenciada por usuário, não por computador. Se vários usuários fizerem logon no mesmo computador e um usuário não estiver isento, o computador será criptografado.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Definições de política de unidade fixa


Esta seção descreve as definições de política de unidade fixa para MBAM, que podem ser encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade fixa**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configuração de política sugerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações de criptografia de unidade de dados fixas</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada </strong> e marque a <strong> caixa de seleção Habilitar desbloqueio automático de unidade de dados fixa </strong> se o volume do sistema operacional precisar ser criptografado.</p>
<p>Essa configuração de política permite que você gerencie se deseja ou não criptografar as unidades fixas.</p>
<p>Quando você habilita essa política, não desabilite a <strong> política configurar o uso da senha para unidades de dados fixas </strong> .</p>
<p>Se a <strong> caixa de seleção Habilitar desbloqueio automático de unidade de dados fixa </strong> estiver marcada, o volume do sistema operacional deve ser criptografado.</p>
<p>Se você habilitar essa configuração de política, os usuários deverão colocar todas as unidades fixas em proteção BitLocker, que criptografará as unidades.</p>
<p>Se você não configurar essa política ou se desabilitar essa política, os usuários não deverão colocar unidades fixas sob proteção BitLocker.</p>
<p>Se você desabilitar essa política, o agente de MBAM descriptografará todas as unidades fixas criptografadas.</p>
<p>Se a criptografia do volume do sistema operacional não for necessária, desmarque a <strong> caixa de seleção Habilitar unidade de dados fixa de desbloqueio automático </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar permissão de "gravação" para unidades fixas que não estão protegidas por BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política determina se a proteção do BitLocker é necessária para unidades fixas em um computador para que elas sejam graváveis. Essa configuração de política é aplicada quando você ativa o BitLocker.</p>
<p>Quando a política não está configurada, todas as unidades fixas no computador são montadas com permissões de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades fixas protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para desbloquear e visualizar as unidades fixas que estão formatadas com o sistema de arquivos FAT (File Allocation Table) em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Esses sistemas operacionais têm permissões somente leitura para unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades fixas formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades fixas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para configurar a proteção por senha em unidades fixas.</p>
<p>Quando a política não está configurada, as senhas são compatíveis com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para maior segurança, habilite essa política e selecione <strong> exigir senha para unidade de dados fixo </strong> , selecione <strong> exigir complexidade de senha </strong> e defina o <strong> comprimento mínimo da senha </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades fixas protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando essa política não está configurada, o agente de recuperação de dados BitLocker é permitido e não é feito o backup das informações de recuperação para o AD DS. O MBAM não exige o backup das informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>



## Definições de política de unidade do sistema operacional


Esta seção descreve as definições de política de unidade do sistema operacional para MBAM, encontradas no seguinte nó de GPO: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade do sistema operacional**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configuração de política sugerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações de criptografia de unidade do sistema operacional</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política determina se a unidade do sistema operacional será criptografada.</p>
<p>Configure esta política para fazer o seguinte:</p>
<ul>
<li><p>Impor a proteção BitLocker para a unidade do sistema operacional.</p></li>
<li><p>Configurar o uso do PIN para usar um PIN do Trusted Platform Module (TPM) para proteção do sistema operacional.</p></li>
<li><p>Configure PINs de inicialização avançados para permitir caracteres como letras maiúsculas e minúsculas e números. O MBAM não dá suporte ao uso de símbolos e espaços para PINs avançados, mesmo que o BitLocker dê suporte a símbolos e espaços.</p></li>
</ul>
<p>Se você habilitar essa configuração de política, os usuários deverão proteger a unidade do sistema operacional usando o BitLocker.</p>
<p>Se você não configurar ou se desabilitar a configuração, os usuários não serão obrigados a proteger a unidade do sistema operacional usando o BitLocker.</p>
<p>Se você desabilitar essa política, o agente de MBAM descriptografará o volume do sistema operacional, se estiver criptografado.</p>
<p>Quando habilitada, essa configuração de política requer que os usuários protejam o sistema operacional usando a proteção do BitLocker, e a unidade é criptografada. Com base em seus requisitos de criptografia, você pode selecionar o método de proteção para a unidade do sistema operacional.</p>
<p>Para obter requisitos de segurança mais altos, use TPM + PIN, permitir pinos aprimorados e definir o comprimento mínimo do PIN como oito caracteres.</p>
<p>Quando essa política é habilitada com o protetor TPM + PIN, você pode considerar a desabilitação das seguintes políticas em <strong> configurações de suspensão do gerenciamento de energia do sistema </strong>  /  <strong> </strong>  /  <strong> </strong> :</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (bateria)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o perfil de validação da plataforma TPM</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar como o hardware de segurança TPM em um computador protege a chave de criptografia do BitLocker. Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver habilitado a proteção TPM.</p>
<p>Quando essa política não está configurada, o TPM usa o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como recuperar unidades do sistema operacional protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando essa política não está configurada, o agente de recuperação de dados é permitido, e não é feito o backup das informações de recuperação para o AD DS.</p>
<p>A operação MBAM não exige o backup das informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>



## Definições de política de unidade removível


Esta seção descreve as definições de política de unidade removível para MBAM, encontradas no seguinte nó de GPO: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade removível**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da política</th>
<th align="left">Visão geral e configuração de política sugerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Controlar o uso do BitLocker em unidades removíveis</p></td>
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Esta política controla o uso do BitLocker em unidades de dados removíveis.</p>
<p>Habilite a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , para permitir que os usuários executem o assistente de configuração do BitLocker em uma unidade de dados removível.</p>
<p>Habilite a <strong> opção permitir que os usuários suspendem e descriptografem o BitLocker em unidades de dados removíveis </strong> para permitir que os usuários removam a criptografia de unidade de disco BitLocker da unidade ou para suspender a criptografia enquanto a manutenção é realizada.</p>
<p>Quando essa política está habilitada e a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , o cliente MBAM salva as informações de recuperação sobre unidades removíveis no servidor de recuperação de chave do MBAM e permite que os usuários recuperem a unidade se a senha for perdida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar permissões de "gravação" para unidades removíveis que não estão protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir permissões somente gravação para unidades protegidas pelo BitLocker.</p>
<p>Quando essa política está habilitada, todas as unidades de dados removíveis no computador exigem criptografia para que as permissões de gravação sejam permitidas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades removíveis protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para desbloquear e exibir as unidades fixas formatadas com o sistema de arquivos (FAT) em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Esses sistemas operacionais têm permissões somente leitura para unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades removíveis formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades de dados removíveis</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para configurar a proteção por senha em unidades de dados removíveis.</p>
<p>Quando essa política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para aumentar a segurança, você pode habilitar essa política e selecionar <strong> exigir senha para unidade de dados removível </strong> , selecionar <strong> exigir complexidade de senha </strong> e, em seguida, definir o <strong> comprimento mínimo de senha preferencial </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades removíveis protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Você pode configurar esta política para habilitar o agente de recuperação de dados BitLocker ou salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando a política é definida como <strong> não configurada </strong> , o agente de recuperação de dados é permitido e não é feito o backup das informações de recuperação no AD DS.</p>
<p>A operação MBAM não exige o backup das informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Preparando seu ambiente para o MBAM 1.0](preparing-your-environment-for-mbam-10.md)









