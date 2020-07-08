---
title: Compactação do disco rígido virtual da MED-V
description: Compactação do disco rígido virtual da MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799240"
---
# Compactação do disco rígido virtual da MED-V


Embora seja opcional, você pode compactar o disco rígido virtual (VHD) para recuperar espaço em disco vazio e reduzir o tamanho do VHD antes de configurar a imagem do PC virtual do Windows.

**Importante**  Antes de prosseguir, crie uma cópia de backup da sua imagem do Windows XP.

 

**Preparando o disco rígido virtual**

1.  Abra a imagem do Windows XP.

    Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**, clique em **PC virtual do Windows**e, em seguida, clique duas vezes em sua imagem do Windows XP.

2.  Limpe o cache de DLL.

    1.  Em um prompt de comando na máquina virtual, digite **sfc/cachesize = 1**.

    2.  Reinicie a máquina virtual.

    3.  Em um prompt de comando na máquina virtual, digite **Sfc/purgecache**.

3.  Exclua arquivos desnecessários, como desinstaladores, arquivos temporários, arquivos de log, arquivos de página, pastas compartilhadas e assim por diante.

4.  Desative a restauração do sistema. Você também pode especificar essa etapa no seu arquivo Sysprep. inf.

    1.  No **painel de controle**, clique duas vezes em **sistema**e selecione a guia **restauração do sistema** .

    2.  Selecione **Desativar restauração do sistema**e, em seguida, clique em **OK**.

5.  Definir tamanhos máximos de log de eventos e limpar todos os eventos.

    1.  Abra o Visualizador de eventos.

        Clique em **Iniciar**, clique em **painel de controle**, clique duas vezes em **Ferramentas administrativas**e clique duas vezes em **Visualizador de eventos**.

    2.  Clique com o botão direito do mouse em **aplicativo**e clique em **Propriedades**.

    3.  Na área **tamanho do log** , defina o **tamanho máximo do log** como 512KB e, em seguida, selecione **substituir eventos conforme necessário**.

    4.  Clique em **Limpar registro**. Na caixa de diálogo **Visualizador de eventos** exibida, clique em **não**.

    5.  Na janela **Propriedades** , clique em **OK**.

    6.  Repita as etapas a a e para os logs de **segurança** e do **sistema** .

6.  Execute a ferramenta de limpeza de disco.

    Clique em **Iniciar**, **em todos os programas**, em **acessórios**, em **Ferramentas do sistema**e, em seguida, clique em limpeza de **disco**.

7.  Configure o arquivo de página conforme necessário para seus aplicativos.

    1.  No **painel de controle**, clique duas vezes em **sistema**e selecione a guia **avançado** .

    2.  Na área **desempenho** , clique em **configurações**.

    3.  Na área **memória virtual** , clique em **alterar**.

    4.  Defina as configurações do arquivo de página.

8.  Desligue a imagem do Windows XP.

**Desfragmentando e compactando o disco rígido virtual**

1.  No **painel de controle** do computador host executando o Windows 7, clique em **Ferramentas administrativas**, clique duas vezes em **Gerenciamento do computador**e clique em gerenciamento de **disco**.

2.  Usando o console de gerenciamento de disco, anexe (Monte) o disco rígido virtual e Desfragmente o disco.

3.  Usando uma ferramenta de extração ISO, extraia o precompacto. ISO localizado na pasta \\Program Files\\Windows virtual PC\\Integration Components.

4.  Use o programa precompact.exe para compactar o disco rígido virtual do Windows XP.

5.  Usando o console de gerenciamento de disco, desconecte o disco rígido virtual.

**Compactar o disco rígido virtual**

1.  Abra o Windows Virtual PC.

    Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.

2.  Clique com o botão direito do mouse na imagem do Windows XP e selecione **configurações**.

3.  Clique em **disco rígido** para aquele que corresponde à sua imagem do Windows XP e clique em **Modificar**.

4.  Clique em **compactar disco rígido virtual**.

5.  Clique em **compactar** e, em seguida, clique em **OK**.

Crie uma cópia de backup do seu disco rígido virtual compactado.

## Tópicos relacionados


[Como configurar uma imagem do Windows Virtual PC para a MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Referência técnica da MED-V](technical-reference-for-med-v.md)

 

 





