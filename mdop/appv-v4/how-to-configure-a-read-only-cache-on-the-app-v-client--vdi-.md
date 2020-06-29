---
title: Como configurar um cache somente leitura no cliente do App-V (VDI)
description: Como configurar um cache somente leitura no cliente do App-V (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797226"
---
# Como configurar um cache somente leitura no cliente do App-V (VDI)


No Microsoft Application Virtualization (App-V) 4,6, o cliente dá suporte ao uso de um cache somente leitura compartilhado. O cache somente leitura compartilhado permite que o cliente use o espaço em disco de forma eficiente em um sistema da Virtual Desktop Infrastructure (VDI), em que os usuários executam aplicativos em máquinas virtuais (VM) hospedadas em um ambiente de servidor de data center e compartilham armazenamento de rede em uma rede de área de armazenamento (SAN). Os procedimentos a seguir fornecem uma visão geral do processo necessário para implementar o cliente App-V em qualquer uma das arquiteturas de VDI primárias, conhecida como "VM em pool" ou "VM estática". Presume-se que você esteja familiarizado com o planejamento, a implantação e a operação do sistema App-V e seus componentes e também a operação e o gerenciamento do servidor VDI. Para obter mais informações sobre o App-V, consulte [virtualização de aplicativo](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)

**Observação**  Os detalhes descritos nesses procedimentos destinam-se apenas a exemplos. Você pode usar métodos diferentes para concluir o processo geral.

 

## Implantando o cliente App-V em um cenário VDI


Você pode implantar o cliente App-V em um cenário VDI usando um cache somente leitura compartilhado que foi preenchido com todos os aplicativos necessários para todos os usuários. Em seguida, você configura a imagem da VM mestre do VDI para que todos os clientes do App-V usem o mesmo arquivo de cache. Os usuários recebem acesso a aplicativos específicos usando o processo de publicação do App-V. Já que o cache já está pré-carregado com todos os aplicativos, nenhum streaming ocorre quando um usuário inicia um aplicativo. No entanto, os pacotes usados para pré-popular o cache devem ser colocados em um servidor App-V que suporte a transmissão de protocolo RTSP (Real Time Streaming Protocol) e que conceda permissões de acesso aos clientes App-V. Se você publicar os aplicativos usando um servidor de gerenciamento App-V, poderá usá-lo para fornecer essa função de streaming.

O processo de implantação consiste em quatro tarefas principais:

-   Criar e preencher o arquivo de cache compartilhado mestre

-   Copiando o arquivo de cache compartilhado para o armazenamento do servidor VDI

-   Configurando o software cliente App-V na imagem mestra do VDI

-   Gerenciando o ciclo de implantação de atualização para o arquivo de cache compartilhado após a implantação inicial

Essas tarefas exigem um planejamento cuidadoso. Recomendamos que você prepare e documente um processo unificado e reproduzível para sua organização acompanhar. Isso é especialmente importante para a preparação e implantação iniciais do arquivo de cache principal compartilhado e para o gerenciamento contínuo de atualizações de aplicativos, cada uma delas requer uma atualização do cache compartilhado mestre. Use os procedimentos a seguir para concluir essas tarefas principais.

**Observação**  Embora você possa publicar os aplicativos usando vários métodos diferentes, os procedimentos a seguir se baseiam no uso de um servidor de gerenciamento App-V para publicação.

 

**Para configurar o cache somente leitura para implantação inicial em uma VDI de VM em pool ou em um cenário de VDI de VM estática**

1. Configure e configure um servidor de gerenciamento App-V em uma VM no servidor VDI para fornecer suporte à autenticação e publicação de usuários.

2. Preencha a pasta de conteúdo deste servidor de gerenciamento com todos os pacotes de aplicativos necessários para todos os usuários.

3. Configure um computador temporário que tenha o cliente App-V instalado. Faça logon no computador de teste com uma conta que tenha acesso a todos os aplicativos para que o conjunto completo de aplicativos sejam publicados no computador e, em seguida, transmita os aplicativos para o cache, para que eles sejam totalmente carregados.

   **Importante**  
   O computador de preparação deve usar o mesmo tipo de sistema operacional e arquitetura do sistema que os usados pelas VMs nas quais o cliente App-V será executado.

     

4. Reinicie o computador de preparação no modo de segurança para garantir que os drivers não sejam iniciados, o que bloquearia o arquivo de cache.

   **Observação**  
   Você também pode parar e desabilitar o serviço Application Virtualization e reiniciar o computador. Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.

     

5. Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada. Defina as permissões de acesso de pasta como somente leitura para o grupo todos e para controle total para administradores que gerenciarão as atualizações de arquivo de cache. O local do arquivo de cache pode ser obtido a partir da chave do registro AppFS\\FileName.

   **Importante**  
   Você deve colocar o arquivo FSD em um local com a capacidade de resposta e a confiabilidade equivalente ao desempenho de armazenamento conectado localmente, por exemplo, uma SAN.

     

6. Instale o cliente da área de trabalho do App-V na imagem da VM principal do VDI e, em seguida, configure-o para usar o cache somente leitura adicionando os seguintes valores de chave do registro para a chave AppFS no cliente. A chave AppFS está localizada em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Chave</th>
   <th align="left">Tipo</th>
   <th align="left">Valor</th>
   <th align="left">Finalidade</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>caminho para FSD</p></td>
   <td align="left"><p>Especifica o caminho para o arquivo de cache compartilhado, por exemplo, \VDIServername\Sharefolder\SFTFS. FSD (obrigatório).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>um</p></td>
   <td align="left"><p>Configura o cliente para operar no modo somente leitura. Isso garante que o cliente não tentará transmitir atualizações para o cache do pacote. (Obrigatório)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>caminho para o arquivo log de erros (. ETL)</p></td>
   <td align="left"><p>Entrada usada para especificar o caminho para o log de erros. Usar. Use um caminho local como C:\Logs\Sftfs.etl.</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configurar o cliente de imagem principal da VM para usar o servidor de publicação e usar a atualização de publicação durante o logon. À medida que os usuários fazem logon no sistema VDI e sua VM é criada a partir da imagem mestra da VM, um ciclo de atualização de publicação ocorre e publica todos os aplicativos para os quais sua conta está autorizada. Esses aplicativos são executados do cache compartilhado.

**Para configurar o cliente para a atualização do pacote em um cenário de VM em pool**

1.  Conclua a atualização e o teste do pacote de aplicativo.

2.  Atualize o pacote no App-V Server. Em seguida, publique e transmita a nova versão dos aplicativos para o cliente no computador temporário para que eles sejam totalmente carregados no cache.

3.  Reinicie o computador de teste no modo de segurança para garantir que os drivers não sejam iniciados.

    **Observação**  Você também pode parar e desabilitar o serviço Application Virtualization no Services. msc e reiniciar o computador. Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.

     

4.  Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada. Você pode usar um nome de arquivo diferente, por exemplo, SFTFS \ _V2. FSD, para distinguir a nova versão.

5.  Para configurar o cliente da área de trabalho do App-V na imagem da VM principal do VDI para usar o arquivo de cache compartilhado atualizado, altere o valor do nome de arquivo da chave do registro AppFS para apontar para o local do arquivo atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Quando os usuários fazem logoff e, em seguida, fazem logon novamente, uma nova VM é criada para ele usando a imagem mestra atualizada. Todas as configurações do usuário serão mantidas e aplicadas à nova VM. Em seguida, eles têm acesso aos aplicativos atualizados.

**Para configurar o cliente para a atualização do pacote em um cenário de VM estática**

1.  Conclua a atualização e o teste do pacote de aplicativo.

2.  Atualize o pacote no App-V Server. Em seguida, publique e transmita a nova versão dos aplicativos para o cliente no computador temporário para que os aplicativos sejam totalmente carregados no cache.

3.  Reinicie o computador de preparação no modo de segurança para garantir que os drivers não sejam iniciados.

    **Observação**  Você também pode parar e desabilitar o serviço Application Virtualization no Services. msc e reiniciar o computador. Depois que o arquivo for copiado, lembre-se de habilitar e iniciar o serviço novamente.

     

4.  Copie o arquivo de cache Sftfs. FSD para a SAN do servidor VDI, onde todas as VMs podem acessá-lo, por exemplo, em uma pasta compartilhada. Você pode usar um nome de arquivo diferente, por exemplo, SFTFS \ _V2. FSD, para distinguir a nova versão.

5.  Para configurar o cliente da área de trabalho do App-V na imagem da VM principal do VDI para usar o arquivo de cache compartilhado atualizado, altere o valor do nome de arquivo da chave do registro AppFS para apontar para o local do arquivo atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Isso garante que novos usuários obtenham a nova versão.

6.  Crie um script que edite o valor de nome de arquivo da chave AppFS para defini-lo como o local do cache atualizado, por exemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Configure esse script para ser executado quando o usuário fizer logoff ou logon para que ele seja executado antes do início dos drivers do cliente App-V, por exemplo, usando as configurações de política de grupo. Quando os usuários fazem logoff e se reconectam novamente, a VM existente é atualizada e ele usará a cópia atualizada do cache. Em seguida, eles têm acesso aos aplicativos atualizados.

## Como usar links simbólicos ao atualizar o cache


Em vez de modificar o valor do nome de arquivo da chave AppFS sempre que um novo arquivo de cache for implantado contendo pacotes novos ou atualizados, você pode usar um link simbólico nos seguintes sistemas operacionais: Windows Vista, Windows 7 e Windows Server 2008. Para obter mais informações sobre links simbólicos, consulte [links simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . Em contraste, o Windows XP não oferece suporte ao uso de links simbólicos, e você deve usar pontos de junção em vez disso. Para obter mais informações sobre junções, consulte o [artigo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) na base de dados de conhecimento Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) e também a junção de ferramenta [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .

**Para configurar um link simbólico para fazer referência ao cache**

1.  Durante o estágio de implantação inicial, abra uma janela do prompt de comando como administrador local no sistema operacional do host do servidor VDI.

2.  Crie um link simbólico usando o comando MKLINK e, em seguida, configure-o para apontar para o arquivo Sftfs. FSD.

    **     mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd**

3.  Na imagem da VM do VDI Master, abra uma janela do prompt de comando usando a opção **Executar como administrador** e conceder permissões de link remoto para que a VM possa acessar o link simbólico no sistema operacional do host VDI. Por padrão, as permissões de link remoto são desativadas.

    **fsutil Behavior Set SymlinkEvaluation R2R: 1**

    **Observação**  No servidor de armazenamento, as permissões de link adequadas devem estar habilitadas. Dependendo da localização do link e do arquivo Sftfs. FSD, as permissões são **L2L: 1** ou **l2r: 1** ou **R2L: 1** ou **R2R: 1**.

     

4.  Quando você configura o cliente da área de trabalho do App-V na imagem da VM principal do VDI, defina o valor do nome de arquivo do AppFS da chave igual ao caminho UNC do arquivo FSD que está usando o link simbólico; por exemplo, defina-o como \\\\VDIHostserver\\Symlinkname. Quando o cliente App-V acessa o cache pela primeira vez, o link simbólico passa para o identificador do cliente a para o arquivo de cache. O cliente continua a usar essa manipulação enquanto o cliente estiver em execução. O valor do link simbólico pode ser atualizado com segurança, mesmo se os clientes existentes tiverem o antigo cache compartilhado aberto.

5.  Quando você deve atualizar um pacote ou adicionar um novo pacote ao cache, siga as etapas de 1 a 5 do procedimento de atualização para a VM estática ou o cenário da máquina virtual em pool. Em seguida, exclua o link simbólico e crie-o novamente para apontar para a nova versão do arquivo de cache compartilhado. Quando a VM é reiniciada, o cliente recebe um identificador para a cópia atualizada do cache porque a VM usa o caminho que contém o link simbólico atualizado. Em seguida, os usuários têm acesso aos aplicativos novos e atualizados.

## Tópicos relacionados


[Como instalar o Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

[Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





