---
title: Notas de versão do DaRT 10
description: Notas de versão do DaRT 10
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799175"
---
# Notas de versão do DaRT 10


**Para pesquisar essas notas de versão, pressione CTRL + F.**

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

Estas notas da versão contêm informações necessárias para instalar com êxito o diagnóstico e o conjunto de ferramentas de recuperação 10. As notas de versão também contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outra documentação do DaRT, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## Problemas conhecidos com o DaRT 10


### O Disk Commander não consegue reparar um registro de inicialização mestre corrompido em uma partição física no Windows 10

No Windows 10, o "restaurar o registro mestre de inicialização (MBR) ou o cabeçalho da tabela de partição GUID (GPT)" no Disk Commander não pode reparar um registro de inicialização mestre corrompido em uma partição física e, portanto, não pode inicializar o computador cliente.

**Solução alternativa:** Inicie **o reparo de inicialização**, clique em **solucionar problemas**, clique em **Opções avançadas**e clique em **Iniciar reparo**.

### Várias instâncias de apagamento de disco que destinam-se à mesma unidade fazem todas as instâncias, exceto a última para denunciar uma falha

Se você iniciar várias instâncias do apagamento de disco e, em seguida, tentar apagar a mesma unidade usando duas instâncias de apagamento de disco separadas, todas as instâncias, exceto a última, relatarão uma falha na limpeza da unidade.

**Solução alternativa:** Nenhuma.

### O apagamento de disco pode não limpar todos os dados em unidades de estado sólido com memória flash

Se você usar apagamento de disco para limpar dados em uma unidade de estado sólido (SSD) com memória flash, todos os dados podem não ser apagados. Esse problema ocorre porque o firmware de SSD controla a localização física de gravações durante a execução do apagamento de disco.

**Solução alternativa:** Nenhuma.

### A restauração do sistema falha quando você executa o assistente do locksmith ou o editor do registro

Se você executar o assistente do locksmith, editor do registro e possivelmente outras ferramentas, a restauração do sistema falhará.

**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie a restauração do sistema.

### A verificação do verificador de arquivos do sistema (SFC) falha ao executar após iniciar e fechar o assistente do locksmith ou o gerenciamento do computador

Se você iniciar e fechar o assistente do locksmith ou ferramentas no gerenciamento do computador, o verificador de arquivos do sistema falhará para executar.

**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie o verificador de arquivos do sistema.

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> O instalador do DaRT não falha quando o kit de avaliação e implantação do Windows não está instalado

Se você instalar o DaRT 10 usando a linha de comando para executar o Windows Installer (. msi) e o kit de avaliação e implantação do Windows (WindowsADK) não tiver sido instalado, a instalação do DaRT não será bem-sucedida. Atualmente, o instalador do DaRT 10 instala todos os componentes, exceto a imagem de recuperação do DaRT.

**Solução alternativa:** Nenhuma.

## Tópicos relacionados


[Sobre o DaRT 10](about-dart-10.md)

 

 





