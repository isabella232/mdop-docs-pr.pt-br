---
title: Criando uma imagem do Virtual PC para o MED-V
description: Criando uma imagem do Virtual PC para o MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799317"
---
# Criando uma imagem do Virtual PC para o MED-V


Para criar uma imagem do Virtual PC (VPC) para MED-V, você deve executar o seguinte:

1.  [Crie uma imagem do VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Instale o pacote do espaço de trabalho do MED-V. msi na imagem do VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).

3.  [Execute a ferramenta de pré-requisitos da máquina virtual MED-V na imagem do VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).

4.  [Configurar manualmente os pré-requisitos da máquina virtual na imagem do VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).

5.  [Configurar o Sysprep para imagens do MED-V](#bkmk-howtoconfiguresysprepformedvimages) (opcional).

6.  [Desative o Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Criando uma imagem do Virtual PC usando o Microsoft Virtual PC


Para criar uma imagem do Virtual PC usando o Microsoft Virtual PC, consulte a documentação do Virtual PC.

Para obter mais informações, consulte:

-   [Ajuda do PC virtual do Windows](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [Criar uma máquina virtual e instalar um sistema operacional convidado](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>Como instalar o pacote do espaço de trabalho do MED-V. msi


Após a criação da imagem do Virtual PC, instale o pacote do espaço de trabalho do MED-V. msi na imagem.

**Para instalar a imagem do espaço de trabalho do MED-V**

1.  Inicie a máquina virtual e copie o pacote do espaço de trabalho do MED-V. msi dentro.

    O pacote do espaço de trabalho do MED-V. msi é chamado *MED-V\_workspace\_x.msi*, em que *x* é o número da versão.

    Por exemplo, *MED-V\_workspace\_1.0.65.msi*.

2.  Clique duas vezes no pacote do espaço de trabalho do MED-V. msi e siga as instruções do assistente de instalação.

    **Observação**  
    Quando uma nova versão do MED-V for lançada e uma imagem do Virtual PC existente for atualizada, desinstale o pacote do pacote de trabalho do MED-V existente. msi, reinicialize o computador e instale o novo pacote do espaço de trabalho do MED-V. msi.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>Como executar a ferramenta de pré-requisitos da máquina virtual


A ferramenta de pré-requisitos da máquina virtual (VM) é um assistente que automatiza vários dos pré-requisitos.

**Observação**  
Embora muitos parâmetros sejam configuráveis no assistente, as propriedades necessárias para o funcionamento adequado do MED-V não são configuráveis.



**Para executar a ferramenta de pré-requisitos da máquina virtual**

1.  Após a instalação do pacote do espaço de trabalho do MED-V. msi, no menu **Iniciar** do Windows, selecione **todos os programas da &gt; &gt; ferramenta de pré-requisitos da VM do MED-v VM**.

    **Observação**  
    O usuário que está executando a ferramenta pré-requisitos de máquina virtual deve ter direitos de administrador local e deve ser o único usuário conectado.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. Clique em **Avançar**.

3. Na página **configurações do Windows** , a partir das seguintes propriedades configuráveis, selecione as que deseja configurar:

   -   **Limpar informações do histórico pessoal dos usuários**

   -   **Limpar diretório temporário de perfis locais**

   -   **Desabilite os sons nos seguintes eventos do Windows: Iniciar, fazer logon, fazer logoff**

   **Observação**  
   Não habilite a proteção de página do Windows em uma política de grupo.



4. Clique em **Avançar**.

5. Na página **configurações do Internet Explorer** , nas seguintes propriedades configuráveis, selecione as que deseja configurar:

   -   **Não use recursos de preenchimento automático**

   -   **Desabilitar a reutilização de janelas para iniciar atalhos**

   -   **Limpar histórico de navegação**

   -   **Habilitar a navegação com guias no Internet Explorer 7**

6. Clique em **Avançar**.

7. Na página **Serviços do Windows** , nas seguintes propriedades configuráveis, selecione as opções a serem configuradas:

   -   **Serviço da central de segurança**

   -   **Serviço Agendador de tarefas**

   -   **Serviço de atualizações automáticas**

   -   **Serviço de restauração do sistema**

   -   **Serviço de indexação**

   -   **Configuração zero sem fio**

   -   **Compatibilidade com troca rápida de usuário**

8. Clique em **Avançar**.

9. Na página de **logon automático do Windows** , faça o seguinte:

   1.  Marque a caixa de seleção **habilitar logon automático do Windows** .

   2.  Atribua um **nome de usuário** e **senha**.

10. Clique em **aplicar**e, na caixa de confirmação que aparece, clique em **Sim**.

11. Na página **Resumo** , clique em **concluir** para fechar o assistente

**Observação**  
Verifique se as políticas de grupo não substituem as configurações obrigatórias definidas na ferramenta pré-requisitos.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>Como configurar os pré-requisitos de instalação manual da máquina virtual do MED-V


Várias das configurações não podem ser configuradas por meio da ferramenta de pré-requisitos de máquina virtual e devem ser realizadas manualmente.

-   Configurações da máquina virtual

    É recomendável definir as seguintes configurações de máquina virtual no console do Microsoft Virtual PC:

    -   Desative as unidades de disquete.

    -   Desabilitar desfazer-discos (** &gt; desfazer configurações-discos**).

    -   Verifique se a imagem tem apenas uma CPU virtual.

    -   Elimine as interações entre a máquina virtual e o usuário, onde eles não estão relacionados a aplicativos publicados (como mensagens que exigem entrada do usuário).

-   Configurações de imagem

    Defina as seguintes configurações manuais dentro da imagem:

    1.  Na janela **Propriedades de opções de energia** , desabilite hibernação e suspensão.

    2.  Aplicar as atualizações mais recentes do Windows.

    3.  Na caixa de diálogo **inicialização e recuperação do Windows** , na seção **falha do sistema** , desmarque a caixa de seleção **reinicialização automática** .

    4.  Verifique se a imagem usa uma chave de licença VLK.

-   Instalando o VPC Additions

    No menu **ação** , selecione **instalar ou atualizar adições de máquina virtual**.

-   Configurando a impressão

    Você pode configurar a impressão a partir do espaço de trabalho do MED-V de uma das seguintes maneiras:

    -   Adicionar uma impressora à máquina virtual.

    -   Permitir a impressão com impressoras configuradas no computador host.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>Como configurar o Sysprep para imagens do MED-V


Em um espaço de trabalho do MED-V, o Sysprep pode ser configurado para atribuir um identificador de segurança exclusivo (SID), especialmente quando vários espaços de trabalho do MED-V são executados em um único computador. Não é recomendável usar o Sysprep para ingressar em um domínio; em vez disso, use a ação de script do domínio de ingresso no MED-V conforme descrito em [como configurar ações de script](how-to-set-up-script-actions.md).

**Observação**  
Sysprep é o utilitário de preparação do sistema da Microsoft para o sistema operacional Windows.



**Para configurar o Sysprep em um espaço de trabalho do MED-V**

1.  Crie um diretório na raiz da unidade do sistema chamada *Sysprep*.

2.  No CD de instalação do Windows, extraia *deploy.cab* para a raiz da unidade do sistema ou baixe a atualização mais recente das ferramentas de implantação do site da Microsoft.

    -   Para o Windows 2000, consulte [atualização de ferramentas de implantação para windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).

    -   Para Windows XP, consulte [atualização de ferramentas de implantação para Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).

3.  Executar o **Gerenciador de instalação** (setupmgr.exe).

4.  Siga o assistente do Gerenciador de instalação.

Após a configuração do Sysprep e da criação do espaço de trabalho do MED-V, o Sysprep deve ser executado.

**Para executar o Sysprep**

1.  Na pasta Sysprep localizada na raiz da unidade do sistema, execute a ferramenta de preparação do sistema (Sysprep.exe).

2.  Na caixa de mensagem de aviso que aparecerá, clique em **OK**.

3.  Na caixa de diálogo **Propriedades do Sysprep** , marque as caixas de seleção **não redefinir período de cortesia para ativação** e **usar a mini-instalação** .

4.  Clique em **lacrar novamente**.

5.  Se você não estiver satisfeito com as informações listadas na caixa de mensagem de confirmação que aparece, clique em **Cancelar** e altere as opções.

6.  Clique em **OK** para concluir o processo de preparação do sistema.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Desativando o Microsoft Virtual PC


Após a instalação e a configuração de todos os componentes, feche o Microsoft Virtual PC **e selecione Desativar**.

## Tópicos relacionados


Criando uma imagem do MED-V [como configurar ações de script](how-to-set-up-script-actions.md)









