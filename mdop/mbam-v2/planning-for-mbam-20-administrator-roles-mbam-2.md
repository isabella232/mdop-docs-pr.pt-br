---
title: Planejamento para Funções de Administrador do MBAM 2.0
description: Planejamento para Funções de Administrador do MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799563"
---
# Planejamento para Funções de Administrador do MBAM 2.0


Este tópico lista e descreve as funções de administrador disponíveis que estão disponíveis no Microsoft BitLocker Administration and Monitoring (MBAM), bem como os locais do servidor em que os grupos locais são criados.

## Funções de administrador do MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Administradores do sistema do MBAM**  
Os administradores nesta função têm acesso a todos os recursos de administração e monitoramento do Microsoft BitLocker. O grupo local para esta função é instalado no servidor de administração e monitoramento.

<a href="" id="---------------mbam-helpdesk-users"></a> **Usuários da assistência técnica MBAM**  
Os administradores nesta função têm acesso aos recursos de suporte técnico do MBAM. O grupo local para esta função é instalado no servidor de administração e monitoramento.

<a href="" id="---------------mbam-report-users"></a> **Usuários do relatório MBAM**  
Os administradores nesta função têm acesso aos relatórios de conformidade e auditoria do MBAM. O grupo local para esta função é instalado no servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **Usuários avançados da assistência técnica MBAM**  
Os administradores nesta função têm acesso melhorado aos recursos de suporte técnico do MBAM. O grupo local para esta função é instalado no servidor de administração e monitoramento. Se um usuário for membro de usuários da assistência técnica do MBAM e MBAM usuários avançados da assistência técnica, as MBAM permissões de usuários avançados da assistência técnica substituirão as permissões de usuário MBAM da assistência técnica.

**Importante**  Para exibir relatórios, um usuário administrativo deve ser membro do grupo de segurança **usuários de relatório do MBAM** no servidor de administração e monitoramento, banco de dados de conformidade e auditoria e no servidor que hospeda o recurso de conformidade e relatórios de auditoria. Como prática recomendada, crie um grupo de segurança nos serviços de domínio Active Directory com direitos no grupo de segurança **usuários de relatório do MBAM** local no servidor de administração e monitoramento e no servidor que hospeda os relatórios de conformidade e auditoria.

 

## Tópicos relacionados


[Como preparar seu ambiente para o MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





