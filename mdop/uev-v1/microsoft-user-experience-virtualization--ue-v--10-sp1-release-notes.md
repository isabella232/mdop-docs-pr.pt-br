---
title: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft
description: Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796011"
---
# Notas de versão da Virtualização de Experiência do Usuário (UE-V) 1.0 SP1 da Microsoft


Para pesquisar as notas de versão do Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, pressione Ctrl + F.

Você deve ler essas notas de versão cuidadosamente antes de instalar o UE-V. As notas de versão contêm informações necessárias para instalar com êxito a virtualização da experiência do usuário e contêm informações adicionais que não estão disponíveis na documentação do produto. Se houver diferenças entre essas notas de versão e outra documentação da UE-V, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Problemas conhecidos do UE-V


Esta seção contém notas de versão para o User Experience Virtualization 1,0 SP1.

### As configurações do registro falham na sincronização entre aplicativos nativos e App-V no mesmo computador

Quando um computador tem um aplicativo que está disponível por meio do aplicativo virtualização do aplicativo (App-V) e um aplicativo de instalação original instalado com um Windows Installer (. msi File), as configurações baseadas no registro não são sincronizadas entre as tecnologias.

SOLUÇÃO alternativa: para solucionar esse problema, execute o aplicativo selecionando uma das duas tecnologias, mas não ambas.

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a>A configuração do Windows 8 falha na sincronização quando o compartilhamento de rede está fora do domínio do usuário

Quando o Windows® 8 tenta a sincronização das configurações do sistema operacional, o synchrnization falha com a seguinte mensagem de erro: **Boost:: FileSystem:: Exists:: nome de usuário ou senha incorreto**. Esse erro pode indicar que o compartilhamento de rede está fora do domínio do usuário. Para verificar eventos de log operacional, abra o **Visualizador de eventos** e navegue até **aplicativos e serviços logs**  /  **Microsoft**  /  **User Experience Virtualization**  /  **Logging**  /  **Operational**. Os compartilhamentos de rede usados para as configurações de UE-V armazenam locais de armazenamento devem residir no mesmo domínio do Active Directory que o usuário.

SOLUÇÃO alternativa: Use compartilhamentos de rede do mesmo domínio do Active Directory que o usuário. .

### Roaming de assinatura de email do Outlook 2010

O UE-V fará roaming dos arquivos de assinatura do Outlook 2010 entre dispositivos. No entanto, as opções de assinatura padrão para novas mensagens e respostas/encaminhamentos não são móveis. Essas duas configurações são armazenadas no perfil do Outlook, do qual a UE-V não faz roaming.

SOLUÇÃO alternativa: nenhum.

### As configurações de sincronização não são sincronizadas no intervalo esperado durante a execução no modo de link lento

Em condições normais, as configurações locais de armazenamento devem estar disponíveis em uma conexão de rede de link rápido. No modo de link lento, a sincronização ocorrerá periodicamente periodicamente. Por padrão, o cronograma de sincronização do modo de link lento é definido para cada 360 minutos.

SOLUÇÃO alternativa: para alterar a frequência da sincronização em segundo plano para computadores no modo de vínculo lento, você pode configurar a política de sincronização em segundo plano para **arquivos offline**.

### Os caracteres especiais não são sincronizados

Certos caracteres, como símbolos de moeda, não são sincronizados entre computadores com o Windows 7 e o Windows 8 que executam o UE-V Agent.

SOLUÇÃO alternativa: nenhum.

### O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Microsoft Office

Recomendamos que você instale a versão de 32 bits do Microsoft Office para sistemas operacionais de 32 bits e 64 bits. Para escolher a versão do Microsoft Office que você precisa, clique aqui ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ). O UE-V é compatível com as configurações de roaming entre versões de arquitetura idênticas do Office. Por exemplo, as configurações do Office de 32 bits serão transferidas entre todas as instâncias do Office de 32 bits. O UE-V não é compatível com as configurações de roaming entre as versões de 32 bits e 64 bits do Office.

SOLUÇÃO alternativa: nenhum

### <a href="" id="msi-s-are-not-localized"></a>Os MSI não estão localizados

O UE-V 1,0 SP1 inclui um programa de instalação localizado para o UE-V Agent e o UE-V Generator. Esses arquivos MSI ainda estão disponíveis, mas a interface do usuário é minimizada e o MSI é exibido somente em inglês. Apesar de o arquivo estar em inglês, o programa de instalação instala todos os idiomas com suporte durante a instalação.

SOLUÇÃO alternativa: nenhum

### Outras pastas do compartilhamento com o local de armazenamento de configuração não estão disponíveis no modo de conexão lenta

Os compartilhamentos de repositório de configurações não devem estar localizados em um compartilhamento de rede que é usado para outras pastas que sempre devem estar disponíveis. Quando o compartilhamento de rede que hospeda a configuração local de armazenamento entrar em modo de conexão lenta, a única pasta disponível será a pasta de local de armazenamento de configurações. Outras pastas no compartilhamento não estão disponíveis no modo de conexão lenta.

Solução alternativa: nenhum

### Favicons associados ao Internet Explorer 9 favoritos não fazem roaming

Os favicons associados ao Internet Explorer 9 favoritos não são movidos pela virtualização da experiência do usuário e não aparecem quando os favoritos aparecem em um novo computador.

SOLUÇÃO alternativa: o favicons será exibido com seus favoritos associados quando o indicador for usado e armazenado no navegador do Internet Explorer 9.

### Caminhos de configurações de arquivo são armazenados no registro

Algumas configurações do aplicativo armazenam os caminhos dos arquivos de configuração e configurações como valores no registro. Os arquivos referenciados como caminhos no registro devem ser sincronizados quando as configurações estiverem em roaming entre computadores.

SOLUÇÃO alternativa: Use o redirecionamento de pastas ou outra tecnologia para garantir que todos os arquivos referenciados como caminhos de configurações de arquivo estejam presentes e colocados no mesmo local em todos os computadores em que as configurações sejam de roaming.

### Caminhos de armazenamento de configurações longos podem causar um erro

Mantenha as configurações dos caminhos de armazenamento o mais breve possível. Caminhos longos podem impedir a resolução ou a sincronização. O UE-V usa o caminho de armazenamento de configurações como parte do caminho calculado para armazenar as configurações. Esse caminho é calculado da seguinte maneira: caminho de armazenamento de configurações + "settingspackages" + dir dir (ID do modelo) + nome do pacote (ID do modelo). Se esse caminho calculado exceder 260 caracteres, o armazenamento do pacote falhará e gerará a seguinte mensagem de erro no log de eventos operacional do UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Para verificar os eventos de log operacional, abra o Visualizador de eventos e navegue até aplicativos e logs de serviços/Microsoft/User Experience Virtualization/Logging/Operational.

SOLUÇÃO alternativa: nenhum.

### O UE-V Agent atrasa após logoff ou logon

Se ocorrer um logon ou logout antes que os arquivos offline determinem que um link lento está em vigor, o logout ou o logon podem ser adiados. O recurso arquivos offline pode levar até três minutos para detectar o estado atual da rede. Se o logon ou o desligamento ocorrer antes de os arquivos offline determinarem que o computador está conectado a um link lento, o pacote de configurações do UE-V será enviado ao servidor em vez do cache local.

SOLUÇÃO alternativa: nenhum.

### As configurações estão em conflito ao tentar fazer roaming das configurações do sistema operacional no Windows 8

No Windows 8 se a sincronização da conta da Microsoft estiver habilitada juntamente com o UE-V para configurações do sistema operacional, as configurações aplicadas podem ser inconsistentes.

SOLUÇÃO alternativa: siga um destes procedimentos:

-   Desabilitar a sincronização de conta da Microsoft se você estiver usando o UE-V para fazer roaming das configurações do sistema operacional

-   Desabilitar o UE-V para configurações do sistema operacional

### Algumas configurações do sistema operacional são apenas roaming entre as versões do sistema operacional

As configurações do sistema operacional para o narrador e caracteres monetários específicos para a localidade só serão transferidas para versões de sistema operacional do Windows. Por exemplo, os caracteres de moeda só serão movidos do Windows 7 para o Windows 7.

SOLUÇÃO alternativa: nenhum

 

 





