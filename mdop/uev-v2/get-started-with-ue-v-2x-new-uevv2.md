---
title: Introdução ao UE-V 2.x
description: Introdução ao UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799242"
---
# Introdução ao UE-V 2.x


Siga as etapas deste guia para implantar rapidamente o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1 em um pequeno ambiente de teste. Isso ajuda você a determinar se a UE-V é a solução certa para gerenciar as configurações de usuário em vários dispositivos na sua empresa.

**Observação**  As informações nesta seção são repetidas com mais detalhes em todo o restante da documentação. Portanto, se você já sabe que o UE-V 2 é a solução certa e não precisa avaliá-lo, você pode começar a [preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).

 

A instalação padrão do UE-V sincroniza as configurações padrão do Microsoft Windows e do Office e muitas configurações de aplicativo do Windows. Certifique-se de que seu ambiente de teste inclui dois ou mais computadores de usuário que compartilham acesso à rede e você vai avaliar o UE-V em apenas um período curto.

-   [Etapa 1: confirmar pré-requisitos](#step1): Certifique-se de que seu ambiente seja capaz de executar o UE-V, incluindo detalhes sobre as configurações com suporte.

-   [Etapa 2: implantar o local de armazenamento de configurações para UE-V 2](#step2): todas as implantações do UE-v exigem um local para pacotes de configurações que contêm os valores de configuração sincronizados.

-   [Etapa 3: implantar o agente do UE-V 2](#step3): para sincronizar as configurações usando o UE-v, os dispositivos devem ter o UE-v Agent instalado e em execução.

-   [Etapa 4: testar a implantação de avaliação do UE-V 2](#step4): execute alguns testes em dois computadores com o UE-v Agent instalado e veja como funciona o UE-v.

Isso é tudo! Depois de seguir as etapas, você poderá avaliar como o UE-V pode funcionar na sua empresa.

**Avaliação posterior:** Você também pode executar etapas adicionais para configurar alguns aplicativos de terceiros e de linha de negócios para sincronizar suas configurações usando o UE-V, conforme detalhado em [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a href="" id="step1"></a>Etapa 1: confirmar pré-requisitos


Antes de prosseguir, verifique se o seu ambiente inclui estes requisitos para executar o UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operacional</strong></th>
<th align="left"><strong>Edição</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitetura do sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Ultimate, Enterprise ou Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4 ou superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou servidor Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4 ou superior</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise ou pro</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2 ou Windows Server 2012</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, pre-1607 verison</p></td>
<td align="left"><p>Enterprise ou pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
</tbody>
</table>

**Observação:** A partir do Windows 10, versão 1607, o UE-V está incluído no [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e não faz mais parte do Microsoft Desktop Optimization Pack

Também...

-   **Licença do MDOP:** Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP). Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte como obter o MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenciais administrativas** para qualquer computador no qual você irá instalar

## <a href="" id="step2"></a>Etapa 2: implantar o local de armazenamento de configurações para UE-V 2


Você precisará implantar um local de armazenamento de configurações, um compartilhamento de rede padrão onde as configurações do usuário são armazenadas em um arquivo de pacote de configurações. Ao criar o compartilhamento de armazenamento de configurações, você deve limitar o acesso aos usuários que precisam dele. [Implantar um local de armazenamento de configurações](https://technet.microsoft.com/library/dn458891.aspx#ssl) fornece informações mais detalhadas.

**Criar um compartilhamento de rede**

1.  Crie um novo grupo de segurança e adicione usuários do UE-V a ele.

2.  Crie uma nova pasta no computador centralizado que armazena os pacotes de configurações do UE-V e conceda aos usuários do UE-V acesso às permissões de grupo para a pasta. O administrador que dá suporte a UE-V deve ter permissões para esta pasta compartilhada.

3.  Atribua permissão a usuários do UE-V para criar um diretório quando eles se conectam. Conceda permissão total a todas as subpastas desse diretório, mas bloqueie o acesso a qualquer coisa acima.

    1.  Defina as seguintes permissões de bloco de mensagens de servidor (SMB) de nível de compartilhamento para a pasta de local de armazenamento de configurações.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Conta de usuário</strong></th>
        <th align="left"><strong>Permissões recomendadas</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Todos</p></td>
        <td align="left"><p>Nenhuma permissão</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
        <td align="left"><p>Controle total</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  Defina as seguintes permissões do sistema de arquivos NTFS para a pasta de local de armazenamento de configurações.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Conta de usuário</strong></th>
        <th align="left"><strong>Permissões recomendadas</strong></th>
        <th align="left"><strong>Pasta</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Criador/proprietário</p></td>
        <td align="left"><p>Controle total</p></td>
        <td align="left"><p>Somente subpastas e arquivos</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
        <td align="left"><p>Listar pasta/ler dados, criar pastas/acrescentar dados</p></td>
        <td align="left"><p>Somente esta pasta</p></td>
        </tr>
        </tbody>
        </table>

         

**Observação de segurança:**

Se você criar o compartilhamento de armazenamento configurações em um computador que esteja executando um sistema operacional Windows Server, configure o UE-V para verificar se o grupo Administradores local ou o usuário atual é o proprietário da pasta em que os pacotes de configurações estão armazenados. Para habilitar essa segurança adicional, especifique essa configuração no editor do registro do Windows Server:

1.  Adicione uma chave do registro **reg \ _DWORD** chamada **"RepositoryOwnerCheckEnabled"** ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Defina o valor da chave do registro como *1*.

## <a href="" id="step3"></a>Etapa 3: implantar o agente do UE-V 2


O UE-V Agent sincroniza o aplicativo e as configurações do Windows entre os computadores e os dispositivos dos usuários. Para fins de avaliação, instale o agente em pelo menos dois computadores em seu ambiente de teste que pertençam ao mesmo usuário.

Execute o arquivo AgentSetup.exe a partir da linha de comando para instalar o UE-V Agent. Ele é instalado em sistemas operacionais de 32 bits e 64 bits.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

Você deve especificar o parâmetro de linha de comando SettingsStoragePath como o compartilhamento de rede da etapa 2. [Implantar um agente do UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fornece informações mais detalhadas.

## <a href="" id="step4"></a>Etapa 4: testar a implantação de avaliação do UE-V 2


Agora você pode executar alguns testes em sua implantação de avaliação do UE-V para ver como o UE-V funciona.

****

1.  No primeiro computador (computador A), faça uma ou mais destas alterações:

    1.  Abra a área de trabalho do Windows e mova a barra de tarefas para um local diferente na janela.

    2.  Alterar as fontes padrão.

    3.  Abra a calculadora e defina como **científico**.

    4.  Altere o comportamento de qualquer aplicativo do Windows, conforme detalhado no [Gerenciamento de modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

    5.  Desabilitar a sincronização e os perfis móveis das configurações de conta da Microsoft.

2.  Faça logoff do computador A. as configurações são salvas em um pacote de configurações do UE-V quando os usuários travam, fazem logoff, saem de um aplicativo ou quando o provedor de sincronização é executado (a cada 30 minutos por padrão).

3.  Faça logon no segundo computador (computador B) como o mesmo usuário do computador A.

4.  Abra a área de trabalho do Windows e verifique se o local da barra de tarefas corresponde ao do computador A. Verifique se as fontes padrão correspondem e se a calculadora está definida como **científica**. Verifique também a alteração feita em qualquer aplicativo do Windows.

Você pode alterar as configurações do computador B de volta para o computador original. Em seguida, faça logon no computador B e conecte-se ao computador A para verificar as alterações.

## Outros recursos para este produto


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solução de problemas do UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





