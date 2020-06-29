---
title: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft
description: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797344"
---
# Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o gerenciamento avançado de política de grupo (AGPM) 4,0 SP1 da Microsoft. Estas notas da versão contêm informações que são necessárias para instalar com êxito o AGPM 4,0 SP1 e contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outra documentação do AGPM, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo incluído neste produto.

## Problemas conhecidos do AGPM 4,0 SP1


Esta seção contém notas de versão do AGPM 4,0 SP1.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>A ferramenta "Desinstalar" do painel de controle pode não funcionar quando você tenta alterar as configurações do servidor do AGPM

A ferramenta no painel de controle que permite desinstalar ou alterar um programa pode não funcionar quando você tenta alterar as configurações do servidor de AGPM.

SOLUÇÃO alternativa: antes de tentar alterar as configurações do servidor do AGPM usando o painel de controle, faça uma cópia da pasta de arquivo de AGPM. Em seguida, você pode usar Setup.exe para reinstalar o servidor do AGPM e escolher os parâmetros de configuração desejados.

### Os relatórios não exibem os links que foram adicionados a um objeto de política de grupo

As configurações do AGPM e os relatórios de diferença não exibem os links que foram adicionados a um objeto de política de grupo (GPO).

SOLUÇÃO alternativa: para exibir os links nos relatórios, selecione o GPO no console de gerenciamento de política de grupo (GPMC) e clique na guia **configurações** no painel à direita.

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>Os relatórios não exibem todas as configurações de "Propriedades de opções de opção"

As configurações do AGPM e os relatórios de diferença não exibem todas as configurações selecionadas na janela Propriedades de opções de escolha no editor de objeto de política de grupo.

SOLUÇÃO alternativa: Use o GPMC para exibir as configurações de opções de opções de escolha selecionadas nos relatórios.

### Os relatórios não mostram as guias mostrar e ocultar em determinados navegadores

As guias mostrar e ocultar, mostradas no lado direito das configurações do AGPM e relatórios de diferença, não são exibidas quando você vê os relatórios no Google Chrome ou no Mozilla Firefox.

SOLUÇÃO alternativa: visualize os relatórios usando o Internet Explorer.

### As configurações do AGPM e os relatórios de diferença podem mostrar conteúdo diferente dos relatórios do GPMC

As configurações do AGPM e os relatórios de diferença podem não mostrar o mesmo conteúdo que os relatórios no GPMC (console de gerenciamento de política de grupo).

SOLUÇÃO alternativa: Use o GPMC para ver os relatórios do AGPM.

### O serviço do AGPM não iniciará se o controlador de domínio não estiver online

Quando o serviço do AGPM estiver instalado em um controlador de domínio no Windows 8, o serviço não iniciará se o controlador de domínio não estiver online.

SOLUÇÃO alternativa: Inicie manualmente o serviço do AGPM após o controlador de domínio estar online.

### A atualização do servidor do AGPM para o AGPM 4,0 SP1 é bloqueada quando você atualiza a partir da versão do AGPM 4,0 mais o hotfix

Se você tentar atualizar o servidor do AGPM para o AGPM 4,0. SP1 depois de instalar o AGPM 4,0 e, em seguida, instalar o hotfix do AGPM (consulte o artigo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)da base de dados de conhecimento), a atualização falha e não pode ser concluída.

SOLUÇÃO alternativa: desinstale o servidor do AGPM 4,0 e instale o AGPM 4,0 SP1.

### Relatórios não exibem links de unidade organizacional

Se você vincular um GPO não controlado a uma unidade organizacional e controlar esse GPO usando o AGPM, as configurações do AGPM e os relatórios de diferença não exibirão os links de unidade organizacional.

SOLUÇÃO alternativa: na guia **controlado** do nó **alterar configurações** , clique com o botão direito do mouse no GPO e clique em **configurações** e, em seguida, clique em **links de GPO** para ver os links organizacionais. Você também pode usar o GPMC para ver os links para um GPO na guia **escopo** .

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

[Novidades do AGPM 4.0 SP1](whats-new-in-agpm-40-sp1.md)

 

 





