---
title: Gerenciamento de configurações do espaço de trabalho da MED-V usando o empacotador de espaço de trabalho da MED-V
description: Gerenciamento de configurações do espaço de trabalho da MED-V usando o empacotador de espaço de trabalho da MED-V
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799809"
---
# Gerenciamento de configurações do espaço de trabalho da MED-V usando o empacotador de espaço de trabalho da MED-V


Você pode usar o pacote do espaço de trabalho do MED-V para gerenciar determinadas configurações no espaço de trabalho do MED-V.

**Para gerenciar as configurações em um espaço de trabalho do MED-V**

1. Para abrir o **pacote do espaço de trabalho do MED-V**, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-v**.

2. No painel principal do **pacote de espaço de trabalho do MED-V** , clique em **gerenciar configurações**.

3. Na janela **gerenciar configurações** , você pode definir as seguintes configurações do espaço de trabalho do MED-V.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Iniciar o espaço de trabalho do MED-V</strong></p></td>
   <td align="left"><p>Escolha se deseja iniciar o espaço de trabalho do MED-V no logon do usuário, ao ser usado pela primeira vez ou para permitir que o usuário final decida quando o espaço de trabalho do MED-V é iniciado.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>O espaço de trabalho do MED-V é iniciado de duas maneiras: quando o usuário final faz logon ou quando executa pela primeira vez uma ação que requer MED-V, como abrir um aplicativo publicado ou inserir uma URL que exija redirecionamento.</p>
   <p>Você pode definir essa configuração para o usuário final ou permitir que o usuário final controle como o MED-V é iniciado.</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Se você especificar que o usuário final decide, o comportamento padrão que ele perceberá é que o espaço de trabalho do MED-V é iniciado quando eles fazem logon. Eles podem alterar o padrão clicando com o botão direito do mouse no ícone do MED-V na área de notificação e selecionando <strong> as configurações do usuário do MED-v </strong> . Se você definir essa configuração para o usuário final, ela não poderá alterar a forma como o MED-V é iniciado.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Rede</strong></p></td>
   <td align="left"><p>Selecione <strong> compartilhado </strong> ou <strong> ponte </strong> para a configuração de rede. O padrão é <strong> compartilhado </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Compartilhado </strong> - o espaço de trabalho do MED-V usa a NAT (conversão de endereços de rede) para compartilhar o host&#39;s de IP para o tráfego de saída.</p>
   <p><strong>Em ponte </strong> - , o espaço de trabalho do MED-V tem seu próprio endereço de rede, normalmente obtido por meio de DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Credenciais da loja</strong></p></td>
   <td align="left"><p>Escolha se deseja armazenar as credenciais do usuário final.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>O comportamento padrão é que o armazenamento de credenciais está desabilitado para que o usuário final deva ser autenticado toda vez que fizer logon.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Embora o armazenamento em cache das credenciais do usuário final forneça a melhor experiência do usuário, você deve estar ciente dos riscos envolvidos.</p>
   <p>A credencial do domínio do usuário final é armazenada em um formato reversível no Gerenciador de credenciais do Windows. Um invasor pode escrever um programa que recupere a senha e, assim, obter acesso às credenciais do usuário. Você só pode diminuir esse risco desabilitando o armazenamento de credenciais do usuário final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. Clique em **salvar como...** para salvar as configurações de configuração atualizadas na pasta especificada. O MED-V cria um arquivo de registro que contém as configurações atualizadas. Implantar o arquivo de registro atualizado usando a política de grupo. Para obter mais informações sobre como usar a política de grupo, consulte [instalação do software de política de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   O MED-V também cria um script do Windows PowerShell na pasta especificada que você pode usar para recriar o arquivo de registro atualizado.

## Tópicos relacionados


[Gerenciamento de configurações do espaço de trabalho da MED-V](managing-med-v-workspace-configuration-settings.md)

[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)









