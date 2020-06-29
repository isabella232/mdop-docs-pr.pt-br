---
title: Notas de versão do MBAM 2.5 SP1
description: Notas de versão do MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799582"
---
# Notas de versão do MBAM 2.5 SP1


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM e podem conter informações que não estão disponíveis na documentação do produto. Se estas notas de versão forem diferentes das outras documentações do MBAM 2,5 SP1, considere as últimas alterações a serem autoritativas. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> Problemas conhecidos do MBAM 2,5 SP1


Esta seção contém notas de versão do MBAM 2,5 SP1.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>Os cmdlets Read-AD * do PowerShell não fornecem comentários se o usuário não tem direitos suficientes

Se um usuário tentar usar os cmdlets Read-AD \ * do PowerShell para o servidor do MBAM não tiver direitos de usuário para ler as informações de recuperação do Active Directory ou ler as informações do TPM, os cmdlets não fornecerão ao usuário qualquer erro ou aviso.

**Solução alternativa:** Use os cmdlets Read-AD * do PowerShell se você tiver os direitos de usuário necessários.

### Os cmdlets de migração do MBAM Active Directory (AD) não recuperam informações de recuperação de volume

MBAM cmdlets de migração do Active Directory (AD) falham ao recuperar informações de recuperação de volume para computadores em unidades organizacionais (UOs) se o caractere de barra (/) for parte do nome da UO. Recebimentos de anúncio repetidos falharão com um erro de encerramento de pipeline quando esse erro for encontrado.

**Detalhes técnicos:** Você verá esse erro ao executar o comando:

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

Além disso, o rastreamento de pilha de exceção `Error[0].Exception.StackTrace` terá a seguinte aparência:

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**Solução alternativa:** Execute uma destas tarefas para resolver essa situação:

-   Renomeie a UO para remover o caractere de barra e, em seguida, execute o script.

-   Para excluir qualquer UO problemática do processo de backup, localize uma lista de UOs cujos nomes não contenham o caractere de barra. Execute o script nessas UOs, uma OU por vez.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> O MBAM não criptografa um volume e informa um erro se você definir um protetor TPM + PIN em um dispositivo tablet

Se os usuários finais tentarem definir um protetor TPM + PIN em um dispositivo tablet, o MBAM não criptografará, e ele reportará um erro. Esse problema ocorre porque os dispositivos Tablet não têm um teclado de ambiente de pré-inicialização.

**Solução alternativa:** Habilite o **uso da autenticação do BitLocker exigindo a entrada do teclado de pré-inicialização na configuração da política de grupo do tablets** . Essa configuração é uma configuração de política de grupo do BitLocker e não está disponível nos modelos de política de grupo do MBAM.

### O nome UPN do usuário é necessário para todas as contas de serviço

Um nome UPN deve ser definido para todas as contas de serviço no MBAM. Se você não conseguir criar um UPN para uma conta, uma mensagem de erro aparecerá durante o processo de configuração para indicar que o usuário ou grupo não foi encontrado no Active Directory.

**Solução alternativa:** Adicione o UPN à conta de serviço.

### O portal de autoatendimento e o site de administração e monitoramento não abrem após a atualização do IIS para o .NET Framework 4,5

Quando você atualiza os serviços de informações da Internet (IIS) para o Microsoft .NET Framework 4,5, o portal de autoatendimento e o site de administração e monitoramento não abrem.

**Solução alternativa:** Veja a mensagem de erro do artigo [depois de instalar o .NET Framework 4,0: "não foi possível carregar o tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).

### Site de administração e monitoramento exibe uma mensagem de erro "não é possível encontrar o relatório" quando os relatórios não estão configurados

Se você configurar o site de administração e monitoramento e, em seguida, tentar exibir um relatório sem configurar o recurso relatórios primeiro, uma mensagem de erro indicará que o relatório não foi encontrado.

**Solução alternativa:** Configure o recurso relatórios antes de configurar os aplicativos Web.

### Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS

Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL do recurso de relatórios será definida como HTTP em vez de HTTPS quando você configurar o servidor MBAM. Se, em seguida, você abrir o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem de erro será exibida: "somente conteúdo seguro é exibido".

**Solução alternativa:** Para mostrar o relatório, clique em **mostrar todo o conteúdo**. Para corrigir esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**. Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.

### Clicar em "retornar" no relatório de Resumo de conformidade do BitLocker pode gerar um erro

Se você fizer buscas detalhadas em um relatório de Resumo de conformidade do BitLocker e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.

**Solução alternativa:** Nenhuma.

### O nível de codificação é exibido incorretamente no relatório de conformidade do computador BitLocker

Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação de codificação** , o relatório de conformidade do computador BitLocker na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits. O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.

**Solução alternativa:** Defina sempre um nível de codificação específico no objeto **escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação.

### A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração

Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.

**Solução alternativa:** Nenhuma. Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.

### A configuração de segurança reforçada pode fazer com que os relatórios exibam uma mensagem de erro incorretamente

Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de erro "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM. Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.

**Solução alternativa:** Se a mensagem de erro "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada. Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.

### Suporte para algoritmo de criptografia do XTS-AES para o BitLocker
Suporte adicionado ao BitLocker para o algoritmo de criptografia XTS-AES no Windows 10, versão 1511. Com o HF02, o MBAM adicionou suporte ao cliente para esta opção BitLocker e no HF04, o suporte do lado do servidor foi adicionado. No entanto, há uma limitação conhecida:

* Os clientes devem usar o mesmo nível de criptografia para o sistema operacional e volumes de dados na mesma máquina.
Se forem usados diferentes níveis de criptografia, o MBAM informará a máquina como **não compatível**.

### O portal de autoatendimento adiciona automaticamente "-" na entrada de ID da chave
A partir de HF02, o portal de autoatendimento do MBAM adiciona automaticamente o "-" na entrada de ID da chave.  
**Observação:** O servidor deve ser reconfigurado para que o JavaScript entre em vigor.

### Os relatórios do MBAM 2,5 SP1 não funcionam e são renderizados corretamente
A página relatórios não é renderizada corretamente quando o SSRS está hospedado na edição do SQL Server 2016. 
Por exemplo – navegar para o helpdesk – clicar em relatórios – (a parte realçada tem "x" nele) abordando isso ainda mais com o Fiddler – ela se parecerá quando clicarmos nos relatórios – ele chama a página SSRS com o formato de renderização HTML 4,0.

**Solução alternativa:** Olhando para o código mestre site. e observou que o modo X-UA foi ditado como IE8. À medida que o IE8 está ultrapassando o fim da vida útil, o cliente está usando o IE11. Atualize a configuração para o código abaixo. Isso permite que o site utilize tecnologias de renderização IE11

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

A configuração original é: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


Esse é o motivo pelo qual o problema não era visto com outros navegadores, como o Chrome, o Firefox, etc.



## Tópicos relacionados


[Sobre o MBAM 2.5](about-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





