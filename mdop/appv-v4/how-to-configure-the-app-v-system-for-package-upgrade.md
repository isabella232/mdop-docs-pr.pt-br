---
title: Como configurar o sistema App-V para upgrade de pacote
description: Como configurar o sistema App-V para upgrade de pacote
author: dansimp
ms.assetid: de133898-f887-46c1-9bc9-fbb03feac66a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5056f923c61aff39d9bd6e1d26f071177f7c12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797207"
---
# Como configurar o sistema App-V para upgrade de pacote


Ao implantar uma nova versão de um pacote de aplicativo existente que foi atualizado no sequenciador App-V, você pode implantá-lo para que os clientes App-V transmitam automaticamente a nova versão para o cache local. Dependendo da solução de transmissão de fluxo que você usa, há procedimentos diferentes para configurar a atualização do pacote. As seções a seguir descrevem os cenários mais comuns de publicação e streaming e incluem os procedimentos necessários para configurar a atualização de pacote para cada cenário.

## Usar um servidor de gerenciamento para publicação e streaming


Nesse cenário, um único servidor de gerenciamento App-V é usado para a publicação e streaming de pacotes e aplicativos, e o protocolo RTSP (S) é necessário. Quando o pacote original é importado para o servidor de gerenciamento do App-V, o administrador copia a pasta do pacote que contém os arquivos criados pelo sequenciador para a pasta de conteúdo, por exemplo, para \\\\server\\CONTENT\\packagename. O administrador também edita a entrada HREF no arquivo OSD para apontar para o arquivo SFT na pasta Package e, em seguida, importa o pacote para o servidor.

Quando um usuário é autenticado pelo servidor de gerenciamento, o servidor publica os aplicativos do usuário enviando o arquivo applist.xml ao cliente. Em seguida, o cliente recupera os arquivos e ícones OSD para os aplicativos do servidor de gerenciamento. Quando o usuário clica duas vezes no ícone do aplicativo, o conteúdo do aplicativo é transmitido para o cache do cliente a partir do caminho especificado no arquivo OSD, e o aplicativo é iniciado.

### Para atualizar o pacote

Para adicionar uma nova versão de um aplicativo que foi atualizado no sequenciador App-V, o administrador deve copiar o novo arquivo SFT e quaisquer outros arquivos modificados para a mesma pasta que a versão original do aplicativo. O administrador usará **Adicionar versão** no console de gerenciamento do servidor para adicionar a nova versão do pacote.

Quando o usuário inicia o aplicativo pela próxima vez, o servidor transmite a nova versão para o cliente automaticamente. Esse método específico de atualização de um pacote era anteriormente conhecido como atualização ativa.

## Usar um servidor de gerenciamento para publicação e um servidor de streaming para streaming


Nesse cenário, o servidor de gerenciamento App-V é usado para publicar os pacotes, e o servidor de streaming é usado para pacotes e aplicativos de streaming. O protocolo RTSP (S) é necessário. Quando o pacote original é importado para o servidor de gerenciamento, o administrador copia a pasta do pacote que contém os arquivos criados pelo sequenciador para a pasta de conteúdo, por exemplo, para \\\\server\\CONTENT\\packagename. O administrador edita a entrada HREF no arquivo OSD para apontar para o arquivo SFT no servidor de fluxo e, em seguida, importa o pacote para o servidor de gerenciamento.

Para configurar o servidor de streaming, o administrador copia a pasta do pacote do servidor de gerenciamento para a pasta de conteúdo no servidor de streaming. Essa pasta deve ter o mesmo nome e o caminho relativo na pasta de conteúdo do servidor de streaming, como no servidor de gerenciamento, por exemplo, \\\\streamingserver\\CONTENT\\packagename.

Se a configuração de ASR (raiz da fonte de aplicativos) do cliente estiver configurada para apontar para o servidor de streaming, o cliente usará essa configuração em vez do nome do servidor na entrada HREF no arquivo OSD. Os campos ISR e OSR no cliente podem ser configurados opcionalmente para apontar para o servidor de gerenciamento ou o servidor de transmissão, dependendo da arquitetura específica do sistema que é usada.

Quando um usuário é autenticado pelo servidor de gerenciamento, o servidor publica os aplicativos do usuário enviando o arquivo applist.xml ao cliente. O cliente recupera os arquivos OSD e os ícones dos aplicativos do servidor de streaming ou do servidor de gerenciamento, dependendo das configurações nos campos OSR e ISR.

Quando o usuário clica duas vezes no ícone do aplicativo, o cliente usa o caminho para o arquivo de conteúdo do pacote (SFT) contido no elemento HREF do arquivo OSD. Se a ASR for usada, o cliente substituirá o nome do servidor (e a porta e o protocolo, se usado) no elemento HREF pelo caminho para o servidor de streaming especificado na ASR. Em seguida, o aplicativo é transmitido do servidor de streaming para o cache do cliente e é iniciado.

### Para atualizar o pacote

Para adicionar uma nova versão de um aplicativo que foi atualizado na sequência do App-V, o administrador deve copiar a nova versão do arquivo SFT e quaisquer outros arquivos modificados para a mesma pasta que a versão original do aplicativo no servidor de fluxo.

Para fins de consistência, recomendamos também copiar novos arquivos para a pasta no servidor de gerenciamento. Em particular, se você usar os campos OSR ou ISR do cliente, copie o arquivo OSD atualizado e os ícones para o servidor especificado nos campos OSR e ISR.

Depois que o servidor de streaming detectar a nova versão, da próxima vez que o usuário iniciar o aplicativo, o servidor transmitirá a nova versão para o cliente automaticamente.

## Usar um servidor de gerenciamento para publicação e um servidor IIS para streaming


Nesse cenário, o servidor de gerenciamento App-V é usado para publicar os pacotes, e o servidor IIS é usado para pacotes e aplicativos de streaming. Quando o pacote original é importado para o servidor de gerenciamento, o administrador copia a pasta do pacote que contém os arquivos criados pelo sequenciador para a pasta de conteúdo, por exemplo, para \\\\server\\CONTENT\\packagename. O administrador edita a entrada HREF no arquivo OSD para que ele aponte para o arquivo SFT no servidor IIS e, em seguida, importe o pacote para o servidor de gerenciamento.

Para configurar o servidor IIS para streaming, o administrador copia a pasta do pacote do servidor de gerenciamento para a pasta de conteúdo no servidor IIS. Essa pasta deve ter o mesmo nome e o caminho relativo na pasta de conteúdo da Web do servidor IIS, como no servidor de gerenciamento; por exemplo, a URL no servidor IIS pode ser acessada usando http://IISserver/CONTENT/packagename ou https://IISserver/CONTENT/packagename .

Se a configuração de ASR (raiz da fonte de aplicativos) do cliente estiver configurada para apontar para o servidor IIS, o cliente usará a ASR em vez do nome do servidor na entrada HREF no arquivo OSD. Opcionalmente, você pode configurar os campos ISR e OSR no cliente para apontar para o servidor de gerenciamento ou o servidor IIS, dependendo da arquitetura específica do sistema que você usa.

Quando o servidor de gerenciamento autentica o usuário, o servidor publica os aplicativos do usuário enviando o arquivo applist.xml ao cliente. O cliente recupera os arquivos OSD e os ícones dos aplicativos do servidor IIS ou do servidor de gerenciamento, dependendo das configurações nos campos ISR e OSR.

Quando o usuário clica duas vezes no ícone do aplicativo, o cliente usa o caminho para o arquivo de conteúdo do pacote (SFT) contido no elemento HREF do arquivo OSD. Se a ASR for usada, o cliente substituirá o nome do servidor (e a porta e o protocolo, se usado) no elemento HREF pelo caminho para o servidor IIS especificado na ASR. Em seguida, o aplicativo é transmitido do servidor IIS para o cache do cliente usando o protocolo HTTP (S) e é iniciado.

### Para atualizar o pacote

O procedimento para atualizar o pacote é o seguinte:

-   Copie a nova versão do arquivo OSD para a pasta da versão original na pasta de conteúdo do servidor de gerenciamento, por exemplo, \\\\server\\CONTENT\\packagename, e substitua o arquivo OSD existente. Para consistência, copie outros arquivos modificados também. Se os campos OSR ou ISR do cliente forem usados, copie também o arquivo OSD atualizado e os ícones para o servidor especificado nos campos OSR e ISR.

-   Copie a nova versão do arquivo SFT para a pasta do pacote na pasta de conteúdo da Web no servidor IIS; por exemplo, a URL no servidor IIS pode ser acessada usando http://IISserver/CONTENT/packagename ou https://IISserver/CONTENT/packagename .

Na próxima atualização de publicação, o cliente é atualizado com a nova versão do arquivo OSD. Agora, esse arquivo aponta para a nova versão do arquivo SFT; Portanto, quando o usuário clica duas vezes em um ícone de aplicativo, a nova versão é iniciada.

## Usar um servidor de gerenciamento para publicação e um compartilhamento de arquivos para streaming


Nesse cenário, o servidor de gerenciamento App-V é usado para publicar os pacotes, e o servidor de arquivos é usado para pacotes e aplicativos de streaming. Quando o pacote original é importado para o servidor de gerenciamento, o administrador copia a pasta do pacote que contém os arquivos criados pelo sequenciador para a pasta de conteúdo, por exemplo, para \\\\server\\CONTENT\\packagename. O administrador edita a entrada HREF no arquivo OSD para que ele aponte para o arquivo SFT no servidor de arquivos e importe o pacote para o servidor de gerenciamento.

Para configurar o servidor de arquivos para streaming, o administrador copia a pasta do pacote do servidor de gerenciamento para a pasta de conteúdo no servidor de arquivos. Essa pasta deve ter o mesmo nome e o caminho relativo na pasta de conteúdo do servidor de arquivos, como no servidor de gerenciamento, por exemplo, \\\\fileserver\\CONTENT\\packagename.

Se a configuração de ASR (raiz da fonte de aplicativos) do cliente estiver configurada para apontar para o servidor de arquivos usando um caminho UNC, por exemplo, \\\\fileserver\\content, o cliente usará essa configuração em vez do nome do servidor na entrada HREF no arquivo OSD. Opcionalmente, o administrador pode configurar os campos ISR e OSR no cliente para apontar para o servidor de gerenciamento ou o servidor de arquivos, dependendo da arquitetura específica do sistema que está sendo usada.

Quando o servidor de gerenciamento autentica o usuário, o servidor publica os aplicativos do usuário enviando o arquivo applist.xml ao cliente. O cliente recupera os arquivos OSD e os ícones dos aplicativos do servidor de arquivos ou do servidor de gerenciamento, dependendo das configurações nos campos ISR e OSR.

Quando o usuário clica duas vezes no ícone do aplicativo, o cliente usa o caminho para o arquivo de conteúdo do pacote (SFT) contido no elemento HREF do arquivo OSD. Se a ASR for usada, o cliente substituirá o nome do servidor (e a porta e o protocolo, se usado) no elemento HREF pelo caminho para o servidor de arquivos especificado na ASR. Em seguida, o aplicativo é transmitido do servidor de arquivos para o cache do cliente e é iniciado.

### Para atualizar o pacote

O procedimento para atualizar o pacote é o seguinte:

-   Copie a nova versão do arquivo OSD para a pasta da versão original na pasta de conteúdo do servidor de gerenciamento, por exemplo, \\\\server\\CONTENT\\packagename, substituindo o arquivo OSD existente. Qualquer outro arquivo modificado também deve ser copiado para fins de consistência. Se os campos OSR ou ISR do cliente forem usados, copie também o arquivo OSD atualizado e os ícones para o servidor especificado nos campos OSR e ISR.

-   Copie a nova versão do arquivo SFT para a pasta do pacote na pasta CONTENT do servidor de arquivos, por exemplo, \\\\fileserver\\CONTENT\\packagename. Copie o arquivo SFT do v2 para a pasta sob o compartilhamento de conteúdo no servidor de arquivos, por exemplo, \\\\fileserver\\CONTENT\\packagename\\V1.

Na próxima atualização da publicação, o cliente será atualizado com a nova versão do arquivo OSD. Agora, esse arquivo aponta para uma nova versão do arquivo SFT, portanto, quando o usuário clica duas vezes no ícone do aplicativo, a nova versão é iniciada.

## Atualizando o pacote usando o modo de streaming do MSI


Ao gerar um arquivo MSI (Windows Installer) durante o sequenciamento de um pacote, o sequenciador cria um. Arquivo MSI que contém todas as informações de publicação necessárias. O administrador deve copiar o. MSI para o cliente e o arquivo. Arquivo SFT que contém o conteúdo do pacote para um compartilhamento de rede acessível pelo computador cliente.

Para publicar o aplicativo no cliente, execute o seguinte comando no computador cliente:

   **Msiexec.exe/i \\\\PathToMsi\\packagename.msi MODE = STREAMING OVERRIDEURL = \\\\\\\\server\\share\\package.SFT**

O. MSI publica os aplicativos para o cliente e, em seguida, transmite os arquivos. Arquivo SFT para o cache do cliente.

### Para atualizar o pacote

Para adicionar uma nova versão, um administrador deve implantar uma nova. MSI para o cliente e um novo arquivo. Arquivo SFT para o compartilhamento de rede. O administrador deve então executar o mesmo comando usado para implantar o pacote, mas use o novo. MSI e o novo arquivo. Arquivo SFT, por exemplo:

   **Msiexec.exe/i \\\\PathToMsi\\packagename\_2.msi MODE = STREAMING OVERRIDEURL = \\\\\\\\server\\share\\package\_2.SFT**

 

 





