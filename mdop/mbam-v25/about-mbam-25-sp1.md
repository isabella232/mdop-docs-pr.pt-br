---
title: Sobre o MBAM 2.5 SP1
description: Sobre o MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799341"
---
# Sobre o MBAM 2.5 SP1


O MBAM 2,5 SP1 fornece uma interface administrativa simplificada para a criptografia de unidade de disco BitLocker. O BitLocker oferece proteção aprimorada contra roubo de dados ou exposição de dados para computadores perdidos ou roubados. O BitLocker criptografa todos os dados armazenados no sistema operacional Windows e nas unidades de dados configuradas.

## Visão geral do MBAM


O MBAM 2,5 SP1 tem os seguintes recursos:

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

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>O que há de novo no MBAM 2,5 SP1


Esta seção descreve os novos recursos do MBAM 2,5 SP1.

### Idiomas recém-instalados para o cliente MBAM 2,5 SP1

Os seguintes idiomas adicionais agora são compatíveis com o MBAM 2,5 SP1 somente para o cliente MBAM, incluindo o portal de autoatendimento:

Tcheco (República Tcheca) CS-CZ

Dinamarquês (Dinamarca) da-DK

Holandês (Holanda) nl-NL

Finlandês (Finlândia) fi-FI

Grego (Grécia) El-GA

Húngaro (Hungria) hu-HU

Norueguês, Bokmål (Noruega) NB-não

Polonês (Polônia) pl-PL

Português (Portugal) pt-PT

Eslovaco (Eslováquia) SK-SK

Esloveno (Eslovênia) SL-SI

Sueco (Suécia) VA-SE

Turco (Turquia) TR-TR

Para obter uma lista de todos os idiomas compatíveis com o cliente e o servidor no MBAM 2,5 e o MBAM 2,5 SP1, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

### Suporte para Windows 10

O MBAM 2,5 SP1 adiciona suporte para o Windows 10 e o Windows Server 2016, além do mesmo software com suporte em versões anteriores do MBAM.

O Windows 10 tem suporte no MBAM 2,5 e no MBAM 2,5 SP1.

### Suporte para Microsoft SQL Server 2014 SP1

O MBAM 2,5 SP1 adiciona suporte para o Microsoft SQL Server 2014 SP1, além do mesmo software com suporte em versões anteriores do MBAM.

### O MBAM não é mais fornecido com um MSI separado

A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM. No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.

### MBAM pode caução OwnerAuth senhas sem possuir o TPM

Anteriormente, se MBAM não possuía o TPM, o OwnerAuth TPM não pôde ser recontado para o banco de dados do MBAM. Para configurar o MBAM para possuir o TPM e armazenar as senhas, você precisava desabilitar o provisionamento automático do TPM e limpar o TPM no computador cliente.

No Windows 8 e versões posteriores, o MBAM 2,5 SP1 agora pode caução nas senhas do OwnerAuth sem ter o TPM. Durante a inicialização do serviço, as consultas MBAM para ver se o TPM já tem proprietário e, em caso afirmativo, ele solicita as senhas do sistema operacional. As senhas são então em caução para o banco de dados do MBAM. Além disso, a política de grupo deve ser definida para impedir que o OwnerAuth seja excluído localmente.

No Windows 7, MBAM deve possuir o TPM para fazer automaticamente a caução do TPM OwnerAuth informações no banco de dados do MBAM. Se o MBAM não tiver o backup do TPM e do Active Directory (AD) do TPM configurado por meio da política de grupo, você deverá usar os **cmdlets de importação de dados do Active Directory do MBAM (AD)** para copiar os OWNERAUTH do TPM do AD para o banco de dados do MBAM. Estes são cinco novos cmdlets do PowerShell que preenchem bancos de dados do MBAM com as informações de recuperação de volume e de proprietário do TPM armazenadas no Active Directory.

Para obter mais informações, consulte [MBAM 2,5 considerações de segurança](mbam-25-security-considerations.md#bkmk-tpm).

### O MBAM pode desbloquear automaticamente o TPM após um bloqueio

Em computadores que executam o TPM 1,2, agora você pode configurar o MBAM para desbloquear automaticamente o TPM em caso de bloqueio. Se o recurso de redefinição automática do bloqueio do TPM estiver habilitado, o MBAM pode detectar que um usuário está bloqueado e obter a senha do OwnerAuth do banco de dados do MBAM para desbloquear automaticamente o TPM para o usuário.

Esse recurso deve ser habilitado no lado do servidor e na política de grupo no lado do cliente. Para obter mais informações, consulte [MBAM 2,5 considerações de segurança](mbam-25-security-considerations.md#bkmk-autounlock).

### Suporte para protetores de senha numérica do BitLocker compatíveis com FIPS

No MBAM 2.5, foi adicionada para as chaves de recuperação do BitLocker compatíveis com o padrão FIPS (Federal Information Processing Standard) em dispositivos que executam o sistema operacional Windows 8,1. No entanto, o Windows não implementou as chaves de recuperação compatíveis com FIPS no Windows 7. Portanto, os dispositivos Windows 7 e Windows 8 ainda exigem um protetor de agente de recuperação de dados (DRA) para recuperação.

A equipe do Windows tem chaves de recuperação compatíveis com FIPS com um hotfix e o MBAM 2,5 SP1 também adicionou suporte para elas.

**Observação**  Os computadores cliente que executam o sistema operacional Windows8 ainda exigem um protetor de DRA, pois o hotfix não era reportado para esse sistema operacional. Consulte [pacote de hotfix 2 para administração e monitoramento do bitlocker 2,5](https://support.microsoft.com/kb/3015477) para baixar e instalar o hotfix do BitLocker para computadores com o Windows 7 e o Windows 8. Para obter informações sobre DRA, consulte [usando agentes de recuperação de dados com o BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

 

Para habilitar a conformidade com FIPS em sua organização, você deve configurar as configurações de política de grupo do padrão FIPS (padrão de processamento de informações federais). Para obter instruções de configuração, consulte [configurações de política de grupo BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

### Personalizar mensagem de recuperação antes da inicialização e URL com a nova configuração de política de grupo

Uma nova configuração de política de grupo, **Configurar a URL e a mensagem de recuperação antes da inicialização**, permite que você configure uma mensagem de recuperação personalizada ou ESPECIFIQUE uma URL que, em seguida, será exibida na tela pré-inicialização de recuperação do BitLocker quando a unidade do sistema operacional estiver bloqueada. Essa configuração só está disponível em computadores cliente que executam o Windows 10.

Se você habilitar essa configuração de política, poderá selecionar uma destas opções para a mensagem de recuperação antes da inicialização:

-   **Usar mensagem de recuperação personalizada**: Selecione esta opção para incluir uma mensagem personalizada na tela pré-inicialização de recuperação do BitLocker.

-   **Usar a URL de recuperação personalizada**: Selecione esta opção para substituir a URL padrão que é exibida na tela pré-inicializar do BitLocker Recovery.

-   **Usar a mensagem e a URL de recuperação padrão**: Selecione esta opção para exibir a mensagem e a URL de recuperação do BitLocker padrão na tela pré-inicialização de recuperação do BitLocker. Se você configurou anteriormente uma mensagem ou URL de recuperação personalizada e quer reverter para a mensagem padrão, você deve habilitar essa política e selecionar essa opção.

A nova configuração de política de grupo está localizada no seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MDOP MBAM (gerenciamento de BitLocker)** &gt; **unidade de sistema operacional**. Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### MBAM adicionou suporte para criptografia de espaço usado

No MBAM 2,5 SP1, se você habilitar a criptografia de espaço usado via política de grupo do BitLocker, o cliente MBAM honrará-a.

Essa configuração de política de grupo é chamada **impor tipo de criptografia de unidade em unidades do sistema operacional** e está localizada no nó do GPO a seguir: modelos administrativos de **configuração de computador** &gt; **Administrative Templates** &gt; **componentes do Windows componentes** do &gt; **BitLocker Drive Encryption** &gt; **sistema operacional**da criptografia de unidade de disco rígido Se você habilitar essa política e selecionar o tipo de criptografia como **apenas criptografia de espaço usado**, o MBAM honrará a política e o BitLocker somente criptografará o espaço em disco usado no volume.

Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### Suporte do cliente MBAM para discos rígidos criptografados

O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667. Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada. Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .

### A configuração de delegação não é mais necessária ao registrar SPNs

A necessidade de configurar a delegação restrita para SPNs que você se registra para a conta do pool de aplicativos não é mais necessária no MBAM 2,5 SP1. No entanto, ainda é um requisito para o MBAM 2,5.

### Habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows

No MBAM 2,5 SP1, você pode usar um script do PowerShell para configurar a criptografia de unidade de disco BitLocker e as chaves de recuperação de caução para o servidor MBAM.

Para obter mais informações, consulte [como habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

### O portal de autoatendimento pode ser personalizado usando o PowerShell ou o assistente para personalização do SSP

A partir do MBAM 2,5 SP1, o portal de autoatendimento pode ser configurado usando o assistente para personalização e usando o PowerShell. Veja [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

### O navegador da Web não é mais intencionalmente executado como administrador

Um problema no MBAM 2,5 causou links de ajuda na ferramenta de configuração do servidor para fazer com que as janelas do navegador sejam abertas com direitos de administrador. Este problema foi corrigido no MBAM 2,5 SP1.

### Não precisa mais fazer o download dos arquivos JavaScript para configurar o portal de autoatendimento quando a CDN estiver inacessível

No MBAM 2,5 e anterior, os arquivos jQuery usados para a configuração do portal de autoatendimento precisavam ser baixados da CDN antecipadamente se os clientes que acessarem o portal de autoatendimento não tivessem acesso à Internet. No MBAM 2,5 SP1, todos os arquivos JavaScript são incluídos no produto, portanto o download é desnecessário.

### Os relatórios podem ser abertos no construtor de Relatórios 3,0

No MBAM 2,5 SP1, os relatórios foram atualizados para o esquema mais recente de linguagem de definição de relatório, permitindo que os usuários abram e personalizem os relatórios no construtor de Relatórios 3,0 e salve-os imediatamente sem danificar o arquivo de relatório.

### Novos cmdlets do PowerShell

Os novos cmdlets do PowerShell para MBAM 2,5 SP1 permitem que você configure e gerencie diferentes recursos do MBAM, incluindo bancos de dados, relatórios e aplicativos Web. Cada recurso tem um cmdlet do PowerShell correspondente que você pode usar para habilitar ou desabilitar recursos ou para obter informações sobre o recurso.

Os seguintes cmdlets foram implementados para o MBAM 2,5 SP1:

-   Write-MbamTpmInformation

-   Write-MbamRecoveryInformation

-   Leitura-ADTpmInformation

-   Leitura-ADRecoveryInformation

-   Write-MbamComputerUser

Os parâmetros a seguir foram implementados nos cmdlets Enable-MbamWebApplication e Test-MbamWebApplication para MBAM 2,5 SP1:

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Para obter informações sobre os cmdlets, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md) e [ajuda do cmdlet de administração e monitoramento do Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).

### O MBAM Agent detecta o modo de apresentação

O agente MBAM pode detectar quando o computador está no modo de apresentação e evitar invocar a interface do usuário do MBAM nesse momento.

### O serviço de agente MBAM agora está configurado para usar o início atrasado

Após a instalação, o serviço definirá o serviço do MBAM Agent para usar o início atrasado, reduzindo a quantidade de tempo necessária para iniciar o Windows.

### Volumes de dados fixos bloqueados agora se reportam como em conformidade

A lógica de cálculo de conformidade dos volumes de "dados fixos bloqueados" foi alterada para relatar os volumes como "compatível", mas com um estado de protetor e estado de criptografia de "desconhecido" e com um detalhe de status de conformidade de "volume está bloqueado". Anteriormente, os volumes bloqueados eram relatados como "não conforme", um estado de protetor de "criptografado", um estado de criptografia de "desconhecido" e um detalhe de status de conformidade de "um erro desconhecido".


## Como obter tecnologias do MDOP


O MBAM é parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do programa Microsoft Software Assurance. Para obter mais informações sobre o programa Microsoft Software Assurance e como adquirir o MDOP, consulte [como faço para obter o MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## Notas de versão do MBAM 2,5 SP1


Para obter mais informações e últimas notícias que não estão incluídas nesta documentação, confira [notas de versão do MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Tópicos relacionados


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Introdução ao MBAM 2.5](getting-started-with-mbam-25.md)

 

 





