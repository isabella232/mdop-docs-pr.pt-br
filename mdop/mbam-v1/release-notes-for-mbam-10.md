---
title: Notas de Versão do MBAM 1.0
description: Notas de Versão do MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799790"
---
# Notas de Versão do MBAM 1.0


**Para procurar um problema específico nestas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM).

Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações MBAM documentação, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Sobre a documentação do produto


Para obter informações sobre a documentação do MBAM, consulte a home page do MBAM no Microsoft TechNet.

Para obter uma cópia disponível para download da documentação do MBAM, consulte <https://go.microsoft.com/fwlink/p/?LinkId=225356> o centro de download da Microsoft.

## Fornecer comentários


Estamos interessados em seus comentários sobre o MBAM. Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .

**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar alterações futuras na nossa documentação e nas versões do produto.

 

Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conhecidos com o MBAM 1,0


Esta seção contém notas de versão sobre os problemas conhecidos com a instalação e a instalação do MBAM.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>Se você selecionar a opção "usar um certificado para criptografar a comunicação de rede" durante a instalação, as conexões de banco de dados existentes e os aplicativos dependentes podem parar de funcionar

Você pode configurar o MBAM para **comunicação de rede criptografada** depois de instalar os recursos de banco de dados de recuperação e de banco de dados de status de conformidade. Se você optar por configurar o MBAM para comunicação de rede criptografada, o programa de instalação do MBAM configura a instância do mecanismo de banco de dados do SQL Server para usar SSL (Secure Sockets Layer) para comunicação entre o banco de dados aplicável e os recursos do servidor de relatório de conformidade e auditoria.

-   Se a instância do mecanismo de banco de dados do SQL Server ainda não estiver configurada para usar SSL, a instalação do MBAM a configurará para fazê-lo. Isso pode evitar que aplicativos que tentam usar bancos de dados não MBAM na instância do mecanismo de banco de dados do SQL Server se comuniquem com seus bancos de dados.

-   Se a instância do mecanismo de banco de dados do SQL Server já estiver configurada para usar SSL, ela será configurada para usar o certificado selecionado pelo usuário durante a instalação. Se esse certificado for diferente do que já estava em uso, ele pode impedir que aplicativos que usam bancos de dados do SQL Server na instância do mecanismo de banco de dados do SQL Server sejam executados.

**Solução alternativa:** Nenhuma

### A instalação do MBAM falha durante a instalação quando você usa uma conta de administrador local

A instalação do MBAM falha quando você usa uma conta de administrador local. O arquivo de log contém as seguintes informações:

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**Solução alternativa:** Use uma conta de domínio com credenciais administrativas no computador servidor ao instalar o MBAM.

### A instalação do MBAM reconfigura a instância do mecanismo de banco de dados do SQL Server para não usar SSL se você selecionar "não criptografar comunicação de rede"

Ao instalar o banco de dados de recuperação e de hardware ou o status de conformidade, você pode usar a instalação para configurar o MBAM selecionando **comunicação de rede criptografada**. Se você decidir não criptografar a comunicação de rede, o MBAM setup reconfigurará a instância do mecanismo de banco de dados do SQL Server para que ele não use SSL.

-   Se a instância do mecanismo de banco de dados do SQL Server já estiver configurada para usar SSL, a instalação do MBAM desabilitará a SSL na instância do mecanismo de banco de dados do SQL Server. Isso altera a segurança de comunicação entre os aplicativos que usam bancos de dados que não estão relacionados a bancos de dados do MBAM na instância do mecanismo de banco de dados do SQL Server.

**Solução alternativa:** Nenhuma

### Pré-requisito ausente para o recurso de servidor Web de ferramentas e scripts de gerenciamento de serviços de informações da Internet (IIS)

A configuração do MBAM depende do recurso de servidor Web de scripts e ferramentas de gerenciamento do IIS, mas não é um pré-requisito imposto. A instalação do servidor permite que você instale o MBAM quando esse recurso estiver ausente. No entanto, isso fará com que o serviço de backup MBAM o gravador VSS inicie e, em seguida, parar porque não consegue localizar a instrumentação de gerenciamento do Windows (WMI) e o provedor de serviços de informações da Internet (IIS). Não há nenhuma mensagem de erro para essa condição, exceto que ocorra no log de eventos. A instalação do MBAM sem scripts e ferramentas de gerenciamento do IIS faz com que as operações de backup não sejam executadas para MBAM.

**Solução alternativa:** Verifique se o recurso do servidor Web de ferramentas e scripts de gerenciamento do IIS está instalado antes de iniciar a configuração do MBAM.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>MBAM a instalação parar de responder durante a fase "Instalando recursos selecionados" quando a configuração estiver configurada para usar um certificado

MBAM a instalação parar de responder durante a fase de instalação dos **recursos selecionados** da instalação. Isso ocorre durante a instalação do banco de dados de recuperação e do banco de dados de hardware ou de status de conformidade após a seleção da opção **usar um certificado para criptografar a comunicação de rede** . Além disso, a configuração do MBAM para de responder se a instância do mecanismo de banco de dados do SQL Server não puder acessar o certificado especificado durante a instalação.

**Solução alternativa:** Atualize as permissões no certificado, para que o serviço do Windows para a instância aplicável do mecanismo de banco de dados do SQL Server possa acessar o certificado. Você também pode alterar a conta na qual a instância do mecanismo de banco de dados do SQL Server é executada, para o mecanismo de banco de dados usar o certificado. Para determinar as permissões do certificado, digite o seguinte comando no prompt de comando: **certutil-v-armazenar minha**

### A instalação do MBAM pausará ao instalar o SQL Server Reporting Services

Durante a instalação do MBAM, quando você seleciona uma instância do SQL Server Reporting Services (SSRS) e a instância do SSRS não está disponível ou está configurada incorretamente, a configuração do MBAM pode pausar por até um minuto enquanto tenta se comunicar com a instância do SSRS.

**Solução alternativa:** Aguarde pelo menos um minuto para que a instalação do MBAM retome enquanto o programa de instalação tenta entrar em contato com a instância do SSRS.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>O servidor de administração e monitoramento não é executado após a instalação

Após a instalação do MBAM instalar com êxito o recurso de servidor de administração e monitoramento, o MBAM exibe mensagens de erro quando você tenta acessar o site do administrador do MBAM. Esse problema ocorre por um dos seguintes motivos:

-   Um ou mais pré-requisitos no servidor de administração e monitoramento foram removidos após a instalação do MBAM.

-   Um ou mais pré-requisitos foram instalados no servidor e mais tarde foram removidos antes de executar a configuração do MBAM.

**Solução alternativa:** Examine a documentação do MBAM e confirme se todos os pré-requisitos do MBAM estão instalados.

### Clicar em links de documentação durante a instalação resulta em um erro de aplicativo após a conclusão da instalação

Quando você clica em um link de documentação durante a instalação e, em seguida, fecha o programa de instalação clicando em **Cancelar** ou em **concluir** após a conclusão da instalação, uma mensagem de erro do aplicativo é exibida... O problema é causado por um erro de violação de acesso no Agendador de tarefas do Windows.

**Solução alternativa:** Nenhuma. Você pode ignorar esse erro.

### Falha na configuração do MBAM não remove novos bancos de dados

Se a configuração do MBAM falhar, a instalação pode não remover os bancos de dados recém-criados. Isso pode causar falhas durante instalações subsequentes.

**Solução alternativa:** Escolha um nome diferente para a instância do banco de dados durante a instalação subsequente.

### A instalação do MBAM não reconhece certificados de cluster de balanceamento de carga de rede válidos

Durante a instalação do MBAM Administration and Monitoring Server, com a opção de criptografia de rede selecionada, o certificado do cluster não é reconhecido como um certificado válido. Ele é reconhecido como válido quando o certificado para comunicação com o banco de dados é instalado, mas é rejeitado para comunicação pelo cluster de balanceamento de carga.

**Solução alternativa:** Confirme se a lista de certificados revogados (CRL) associada ao certificado está acessível ou use um certificado que não exija validação usando a CRL.

## Informações de direitos autorais da versão


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft. Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.



## Tópicos relacionados


[Sobre o MBAM 1.0](about-mbam-10.md)

 

 





