---
title: Como configurar a segurança do servidor de streaming após a instalação
description: Como configurar a segurança do servidor de streaming após a instalação
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797218"
---
# Como configurar a segurança do servidor de streaming após a instalação


Configure o servidor de streaming App-V para segurança aprimorada por meio do registro. Assim como no servidor de gerenciamento do App-V, um certificado deve ser provisionado corretamente com o identificador EKU correto para autenticação do servidor antes de concluir o seguinte procedimento de pós-instalação.

**Para configurar a pós-instalação do servidor de transmissão de segurança do Stream**

1.  Crie um MMC, adicione o snap-in **certificados** e selecione **repositório de certificados do computador local**.

2.  Abra os certificados **pessoais** do computador e abra o certificado provisionado para App-V.

3.  Na guia **detalhes** , role a tela para baixo até a impressão digital e copie o hash no painel detalhes.

4.  Abra o editor do registro e navegue até `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .

5.  Edite o `X509CertHash` valor, Cole o hash de impressão digital no campo valor e remova todos os espaços. Clique em **OK** para aceitar a edição.

6.  No editor do registro, navegue até `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .

7.  Crie um novo valor **DWORD** chamado "322" e insira o valor decimal como 322 ou o valor hexadecimal como 142.

8.  Reinicie o serviço de streaming.

## Tópicos relacionados


[Como configurar a segurança do servidor de gerenciamento após a instalação](how-to-configure-management-server-security-post-installation.md)

[Solução de problemas de permissão de certificado](troubleshooting-certificate-permission-issues.md)

 

 





