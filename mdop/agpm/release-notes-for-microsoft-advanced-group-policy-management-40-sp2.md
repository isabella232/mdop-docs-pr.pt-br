---
title: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2
description: Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797715"
---
# Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o serviço de gerenciamento de política de grupo (AGPM) Pack2 (SP2) 4.0 da Microsoft. Estas notas da versão contêm informações que são necessárias para instalar com êxito o AGPM 4.0 SP2 e contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outra documentação do AGPM, considere as alterações mais recentes autorizadas. Estas notas de versão substituem o conteúdo incluído neste produto.

## Problemas conhecidos do AGPM 4.0 SP2


Esta seção descreve os problemas conhecidos do AGPM 4,0 SP2.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>A ferramenta "Desinstalar" do painel de controle pode não funcionar quando você tenta alterar as configurações do servidor do AGPM

A ferramenta no painel de controle que você usa para desinstalar ou alterar um programa pode não funcionar quando você tenta alterar as configurações do servidor de AGPM.

**Solução alternativa:** Antes de tentar alterar as configurações do servidor de AGPM usando o painel de controle, faça uma cópia da pasta de arquivo de AGPM. Em seguida, você pode usar Setup.exe para reinstalar o servidor do AGPM e escolher os parâmetros de configuração desejados.

### Os relatórios não exibem os links que foram adicionados a um objeto de política de grupo

As configurações do AGPM e os relatórios de diferença não exibem os links que foram adicionados a um objeto de política de grupo (GPO).

**Solução alternativa:** Para exibir os links nos relatórios, selecione o GPO no console de gerenciamento de política de grupo (GPMC) e, em seguida, clique na guia **configurações** no painel direito.

### Relatórios não exibe todas as opções configurações de propriedades de opção

As configurações do AGPM e os relatórios de diferença não exibem todas as configurações selecionadas na janela **Propriedades de opções de escolha** no editor de objeto de política de grupo.

**Solução alternativa:** Use o GPMC para exibir as configurações de **Opções de opções de escolha** selecionadas nos relatórios.

### Os relatórios podem não exibir as guias mostrar e ocultar em determinados navegadores

As guias **Mostrar** e **ocultar** , no lado direito das configurações do AGPM e relatórios de diferença, podem não aparecer quando você vê os relatórios no Google Chrome ou no Mozilla Firefox.

**Solução alternativa:** Exiba os relatórios usando o navegador Internet Explorer.

### As configurações do AGPM e os relatórios de diferença podem mostrar conteúdo diferente dos relatórios do GPMC

As configurações do AGPM e os relatórios de diferença podem não mostrar o mesmo conteúdo que os relatórios no GPMC.

**Solução alternativa:** Use o GPMC para ver os relatórios do AGPM.

### O serviço do AGPM não iniciará se o controlador de domínio estiver offline

Quando o serviço do AGPM estiver instalado em um controlador de domínio nos sistemas operacionais Windows® 8 ou sistemas operacionais posteriores, o serviço não iniciará se o controlador de domínio estiver offline.

**Solução alternativa:** Inicie manualmente o serviço do AGPM após o controlador de domínio estar online.

### A atualização do servidor do AGPM para o AGPM 4.0 SP2 é bloqueada quando você atualiza da versão do AGPM 4.0 mais Hotfix1

Se você tentar atualizar o servidor do AGPM para o AGPM 4,0. SP2 depois de instalar o AGPM 4,0 Server e instalar o hotfix do AGPM chamado AGPM 4,0 relata diferenças incorretas no relatório HTML (consulte o artigo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)da base de dados de conhecimento), a atualização falha e não pode ser concluída.

**Solução alternativa:** Desinstale o servidor do AGPM 4,0 e instale o AGPM 4,0 SP2.

### Relatórios não exibem links de unidade organizacional

Se você vincular um GPO não controlado a uma unidade organizacional e controlar esse GPO usando o AGPM, as configurações do AGPM e os relatórios de diferença não exibirão os links de unidade organizacional.

**Solução alternativa:** Na guia **controlado** do nó **alterar configurações** , clique com o botão direito do mouse no GPO, clique em **configurações**e, em seguida, clique em **links de GPO** para ver os links organizacionais. Você também pode usar o GPMC para ver os links para um GPO na guia **escopo** .

### O AGPM exibirá um erro se você clicar no botão retornar na caixa de diálogo Alterar, reparar ou remover cliente do AGPM

Se você navegar até **programas e recursos** no painel de controle e, em seguida, selecionar **gerenciamento avançado de política de grupo da Microsoft – cliente**, o AGPM exibirá um erro se você clicar em **Modificar** e, em seguida, clicar no botão **retornar** na caixa de diálogo **alterar, reparar ou remover cliente do AGPM** .

**Solução alternativa:** Clique em **Cancelar** para limpar o erro e inicie o processo novamente. Não clique no botão **retornar** depois de clicar em **Modificar** .

### O comentário não aparecerá na janela do histórico quando o aprovador implantar um GPO e inserir um comentário

Se um usuário com a função de editor enviar uma solicitação para implantar um GPO e o usuário que tiver a função de aprovador implantar o GPO e inserir um comentário, o comentário não aparecerá na janela do **histórico** .

**Solução alternativa:** Nenhuma.

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

[Novidades do AGPM 4.0 SP2](whats-new-in-agpm-40-sp2.md)

 

 





