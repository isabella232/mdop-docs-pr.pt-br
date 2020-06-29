---
title: Planejar Requisitos de Política de Grupo do MBAM 2.0
description: Planejar Requisitos de Política de Grupo do MBAM 2.0
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796097"
---
# Planejar Requisitos de Política de Grupo do MBAM 2.0


Para gerenciar computadores cliente do Microsoft BitLocker Administration and Monitoring (MBAM), você precisa considerar os tipos de protetores de BitLocker que você deseja dar suporte em sua organização e, em seguida, configurar as configurações de política de grupo correspondentes que você deseja aplicar. Este tópico descreve as configurações de política de grupo que estão disponíveis para serem usadas quando você estiver usando a administração e o monitoramento do Microsoft BitLocker para gerenciar a criptografia de unidade de disco BitLocker na empresa.

O MBAM dá suporte aos seguintes tipos de protetores de BitLocker para unidades do sistema operacional: TPM (Trusted Platform Module), TPM + PIN, TPM + chave USB e TPM + PIN + chave USB, senha, senha numérica e agente de recuperação de dados. O protetor de senha tem suporte apenas para dispositivos Windows to go e para dispositivos Windows 8 que não têm um TPM. O MBAM dá suporte para a chave TPM + USB e os protetores de chave TPM + pino + USB somente quando o volume do sistema operacional é criptografado antes da instalação do MBAM.

O MBAM dá suporte aos seguintes tipos de protetores de BitLocker para unidades de dados fixas: senha, desbloqueio automático, senha numérica e agente de recuperação de dados.

O protetor de senha numérica é aplicado automaticamente como parte da criptografia de volume e não precisa ser configurado.

**Importante**  
As configurações padrão do objeto de política de grupo (GPO) de criptografia de unidade de disco BitLocker do Windows não são usadas pelo MBAM e podem causar comportamentos conflitantes se estiverem habilitados. Para habilitar o MBAM para gerenciar o BitLocker, você deve definir as configurações de política de grupo do MBAM somente após a instalação do modelo de política de grupo MBAM.



PINs de inicialização avançados podem conter caracteres, como letras maiúsculas e minúsculas e números. Ao contrário do BitLocker, o MBAM não dá suporte ao uso de símbolos e espaços para PINs avançados.

Instale o modelo de política de grupo do MBAM em um computador que é capaz de executar o console de gerenciamento de política de grupo (GPMC) ou a tecnologia avançada do MDOP do gerenciamento de política de grupo (AGPM). Para editar as configurações de GPO que habilitam a funcionalidade do MBAM, você deve primeiro instalar o modelo de política de grupo do MBAM, abrir o GPMC ou o AGPM para editar o GPO aplicável e, em seguida, navegar para o seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** \\ **Policies** \\ **Administrative Templates** \\ **componentes do Windows**o \\ **MDOP MBAM (gerenciamento de BitLocker).**

O nó do GPO MBAM (gerenciamento do BitLocker) do MDOP contém quatro configurações de política global e quatro nós de configurações de GPO filho: gerenciamento de cliente, unidade fixa, unidade do sistema operacional e unidade removível. As seções a seguir fornecem definições de política e configurações de política sugeridas para ajudá-lo a planejar os requisitos de configuração de política de GPO MBAM.

**Observação**  
Para obter mais informações sobre como configurar as configurações de GPO mínimas recomendadas para permitir que o MBAM gerencie a criptografia do BitLocker, consulte [como editar configurações de GPO do MBAM 2,0](how-to-edit-mbam-20-gpo-settings-mbam-2.md).



## Definições de política global


Esta seção descreve as definições de política global do MBAM encontradas no seguinte nó de GPO: modelos administrativos de política de **configuração de computador** \\ **Policies** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**.

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


Esta seção descreve as definições da política de gerenciamento de cliente para administração e monitoramento do Microsoft BitLocker encontradas no nó GPO a seguir: políticas de **configuração do computador** \\ **Policies** \\ **modelos administrativos**do \\ **Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)** \\ **Gerenciamento de cliente**.

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
<li><p><strong>MBAM recuperação e ponto de extremidade do serviço de hardware </strong> . Use esta configuração para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM. Insira um local de ponto de extremidade semelhante ao seguinte exemplo: <strong> http:// </strong><em> &lt; MBAM administração e monitoração &gt; </em><strong> do nome do servidor: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</p></li>
<li><p><strong>Selecione as informações de recuperação do BitLocker a serem armazenadas </strong> . Essa configuração de política permite configurar o serviço de recuperação de chave para fazer backup de informações de recuperação do BitLocker. Ele também permite configurar o serviço de relatório de status para coletar relatórios de conformidade e auditoria. A política fornece um método administrativo de recuperação de dados criptografados pelo BitLocker para evitar a perda de dados devido à falta de informações importantes. O relatório de status e a atividade de recuperação de chave serão enviados automaticamente e silenciosamente para o local do servidor de relatório configurado.</p>
<p>Se você não configurar ou se desabilitar essa configuração de política, as informações de recuperação de chave não serão salvas, e o relatório de status e a atividade de recuperação de chave não serão relatados ao servidor. Quando essa configuração estiver definida como <strong> senha de recuperação e pacote </strong> de chaves, a senha de recuperação e o pacote de chaves serão automaticamente e, em seguida, o backup será silenciosa para o local do servidor de recuperação de chave configurado.</p></li>
<li><p><strong>Digite a frequência do status da verificação do cliente em minutos </strong> . Essa configuração de política gerencia com que frequência o cliente verifica as políticas de proteção do BitLocker e o status no computador cliente. Essa política também gerencia com que frequência o status de conformidade do cliente é salvo no servidor. O cliente verifica as políticas de proteção BitLocker e o status no computador cliente e também faz backup da chave de recuperação do cliente na frequência configurada.</p>
<p>Defina essa frequência com base no requisito definido por sua empresa com a frequência para verificar o status de conformidade do computador e com que frequência fazer backup da chave de recuperação do cliente.</p></li>
<li><p><strong>Ponto de extremidade do serviço de relatório de status do MBAM </strong> . Você deve definir essa configuração para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM. Insira um local de ponto de extremidade semelhante ao seguinte exemplo: <strong> http:// </strong><em> &lt; MBAM administração e monitoração &gt; </em><strong> do nome do servidor: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.svc </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar a política de isenção de usuário</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar um endereço de site, endereço de email ou número de telefone que instruirá o usuário a solicitar uma isenção da criptografia do BitLocker.</p>
<p>Se você habilitar essa configuração de política e fornecer um endereço de site, endereço de email ou número de telefone, os usuários verão uma caixa de diálogo que fornece instruções sobre como solicitar uma isenção da proteção do BitLocker. Para obter mais informações sobre como habilitar a isenção de criptografia BitLocker para os usuários, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> como gerenciar as isenções de criptografia do BitLocker do usuário </a> .</p>
<p>Se você desabilitar ou não definir essa configuração de política, as instruções de solicitação de isenção não serão apresentadas aos usuários.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Isenção de usuário é gerenciada por usuário, não por computador. Se vários usuários fizerem logon no mesmo computador e qualquer usuário não estiver isento, o computador será criptografado.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurar o programa de aperfeiçoamento da experiência do usuário</p></td>
<td align="left"><p>Essa configuração de política permite que você configure como os usuários do MBAM podem participar do programa de aperfeiçoamento da experiência do usuário. Este programa coleta informações sobre o hardware do computador e como os usuários usam o MBAM sem interromper o trabalho. As informações ajudam a Microsoft a identificar quais recursos do MBAM para melhorar. A Microsoft não usará essas informações para identificar ou contatar usuários do MBAM.</p>
<p>Se você habilitar essa configuração de política, os usuários poderão participar do programa de aperfeiçoamento da experiência do usuário.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão participar do programa de aperfeiçoamento da experiência do usuário.</p>
<p>Se você não definir essa configuração de política, os usuários terão a opção de participar do programa de aperfeiçoamento da experiência do usuário.</p></td>
</tr>
</tbody>
</table>



## Definições de política de unidade fixa


Esta seção descreve as definições de política de unidade fixa para administração e monitoramento do Microsoft BitLocker encontradas no nó do GPO a seguir: políticas de **configuração do computador** \\ **Policies** \\ **modelos administrativos**do \\ **Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)** \\ **unidade fixa**.

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
<td align="left"><p>Configuração sugerida: <strong> habilitada</strong></p>
<p>Essa configuração de política permite que você gerencie se as unidades fixas devem ser criptografadas.</p>
<p>Se o volume do sistema operacional for necessário para ser criptografado, marque a <strong> opção Habilitar unidade de dados fixa de desbloqueio automático </strong> .</p>
<p>Ao habilitar essa política, você não deve desabilitar a <strong> política configurar o uso da senha para unidades de dados fixas </strong> , a menos que o uso de desbloqueio automático para unidades de dados fixos seja permitido ou obrigatório.</p>
<p>Se você precisar do uso de desbloqueio automático para unidades de dados fixas, será preciso configurar os volumes do sistema operacional a serem criptografados.</p>
<p>Se você habilitar essa configuração de política, os usuários deverão colocar todas as unidades fixas em proteção BitLocker, e as unidades serão criptografadas.</p>
<p>Se você não definir essa configuração de política, os usuários não deverão colocar unidades fixas sob proteção BitLocker. Se você aplicar essa política após as unidades de dados fixas serem criptografadas, o agente do MBAM descriptografará as unidades corrigidas criptografadas.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão colocar as unidades de dados fixas na proteção BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar o acesso de gravação a unidades fixas não protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política determina se a proteção de BitLocker é necessária para unidades fixas a serem graváveis em um computador. Essa configuração de política é aplicada quando você ativa o BitLocker.</p>
<p>Quando a política não está configurada, todas as unidades de dados fixas no computador são montadas com acesso de leitura e gravação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades fixas protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir que unidades fixas com o sistema de arquivos FAT sejam desbloqueadas e exibidas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Quando a política está habilitada ou não está configurada, unidades fixas formatadas com o sistema de arquivos FAT podem ser desbloqueadas e seu conteúdo pode ser visualizado em computadores que executam o Windows Server 2008, Windows Vista, Windows XP com SP3 ou Windows XP com SP2. Esses sistemas operacionais têm acesso somente leitura às unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades fixas formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades fixas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Use esta política para especificar se uma senha é necessária para desbloquear unidades de dados fixos protegidas pelo BitLocker.</p>
<p>Se você habilitar essa configuração de política, os usuários poderão configurar uma senha que atenda aos requisitos que você definir. O BitLocker permitirá que os usuários desbloqueiem uma unidade com qualquer um dos protetores disponíveis na unidade.</p>
<p>Essas configurações são forçadas ao ativar o BitLocker, e não ao desbloquear um volume.</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão usar uma senha.</p>
<p>Quando a política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para maior segurança, habilite essa política e selecione <strong> exigir senha para unidade de dados fixo </strong> , selecione <strong> exigir complexidade de senha </strong> e defina o <strong> comprimento mínimo da senha </strong> .</p>
<p>Se você desabilitar essa configuração de política, os usuários não poderão usar uma senha.</p>
<p>Se você não definir essa configuração de política, as senhas serão aceitas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades fixas protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando a política não está configurada, o agente de recuperação de dados BitLocker é permitido e não é feito o backup das informações de recuperação para o AD DS. O MBAM não requer o backup de informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>



## Definições de política de unidade do sistema operacional


Esta seção descreve as definições de política de unidade do sistema operacional para administração e monitoramento do Microsoft BitLocker encontradas no seguinte nó de GPO: modelos administrativos de política de **configuração do computador** \\ **Policies** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)** \\ **unidade do sistema operacional**.

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
<p>Essa configuração de política permite que você gerencie se a unidade do sistema operacional deve ser criptografada.</p>
<p>Para maior segurança, considere desabilitar as seguintes configurações de política nas <strong> configurações do sistema/gerenciamento de energia/repouso </strong> ao habilitá-las com o protetor TPM + PIN:</p>
<ul>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (conectado)</p></li>
<li><p>Permitir Estados de espera (S1-S3) quando em repouso (bateria)</p></li>
</ul>
<p>Se você estiver executando o Microsoft Windows 8 ou posterior e desejar usar o BitLocker em um computador sem um TPM, marque a <strong> caixa de seleção Permitir BitLocker sem um TPM compatível </strong> . Nesse modo, é necessária uma senha para a inicialização. Se você esquecer a senha, será necessário usar uma das opções de recuperação do BitLocker para acessar a unidade.</p>
<p>Em um computador com um TPM compatível, dois tipos de métodos de autenticação podem ser usados na inicialização para fornecer proteção adicional para dados criptografados. Quando o computador é iniciado, ele pode usar apenas o TPM para autenticação ou também pode exigir a entrada de um PIN (número de identificação pessoal).</p>
<p>Se você habilitar essa configuração de política, os usuários precisarão colocar a unidade do sistema operacional em proteção BitLocker, e a unidade será criptografada.</p>
<p>Se você desabilitar essa política, os usuários não poderão colocar a unidade do sistema operacional em proteção BitLocker. Se você aplicar essa política depois que a unidade do sistema operacional for criptografada, a unidade será descriptografada.</p>
<p>Se você não configurar essa política, a unidade do sistema operacional não precisará ser colocada em proteção BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o perfil de validação da plataforma TPM</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Essa configuração de política permite configurar como o hardware de segurança TPM em um computador protege a chave de criptografia do BitLocker. Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver sido ativado com a proteção TPM.</p>
<p>Quando essa configuração de política não é definida, o TPM usa o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolher como as unidades do sistema operacional protegidas pelo BitLocker podem ser recuperadas</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</p>
<p>Quando essa política não está configurada, o agente de recuperação de dados é permitido e não é feito o backup das informações de recuperação no AD DS.</p>
<p>A operação MBAM não exige o backup de informações de recuperação para o AD DS.</p></td>
</tr>
</tbody>
</table>



## Definições de política de unidade removível


Esta seção descreve as definições de política de unidade removível para administração e monitoramento do Microsoft BitLocker encontradas no nó GPO a seguir: políticas de **configuração do computador** \\ **Policies** \\ **modelos administrativos**do \\ **Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade removível**.

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
<p>Habilite a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> para permitir que os usuários executem o assistente de configuração do BitLocker em uma unidade de dados removível.</p>
<p>Habilite a <strong> opção permitir que os usuários suspendem e descriptografem o BitLocker em unidades de dados removíveis </strong> para permitir que os usuários removam a criptografia de unidade de disco BitLocker da unidade ou para suspender a criptografia enquanto a manutenção é realizada.</p>
<p>Quando essa política está habilitada e a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , o cliente MBAM salva as informações de recuperação sobre unidades removíveis no servidor de recuperação de chave do MBAM e permite que os usuários recuperem a unidade se a senha for perdida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Negar o acesso de gravação a unidades removíveis não protegidas pelo BitLocker</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir somente o acesso de gravação a unidades protegidas pelo BitLocker.</p>
<p>Quando essa política está habilitada, todas as unidades de dados removíveis no computador exigem Criptografia antes que o acesso de gravação seja permitido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir o acesso a unidades removíveis protegidas pelo BitLocker de versões anteriores do Windows</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para permitir que unidades fixas com o sistema de arquivos FAT sejam desbloqueadas e exibidas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p>
<p>Quando essa política não está configurada, as unidades de dados removíveis formatadas com o sistema de arquivos FAT podem ser desbloqueadas em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2, e seu conteúdo pode ser exibido. Esses sistemas operacionais têm acesso somente leitura às unidades protegidas pelo BitLocker.</p>
<p>Quando a política está desabilitada, as unidades removíveis formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o uso da senha para unidades de dados removíveis</p></td>
<td align="left"><p>Configuração sugerida: <strong> não configurada</strong></p>
<p>Habilite essa política para configurar a proteção por senha em unidades de dados removíveis.</p>
<p>Quando essa política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</p>
<p>Para aumentar a segurança, você pode habilitar essa política e verificar <strong> exigir senha para unidade de dados removível </strong> , selecionar <strong> exigir complexidade de senha </strong> e definir o <strong> comprimento mínimo de senha preferencial </strong> .</p></td>
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


[Pré-requisitos para implantação do MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)









