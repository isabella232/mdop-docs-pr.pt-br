---
title: Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator
description: Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797496"
---
# Trabalhando com os modelos personalizados do UE-V 2. x e do UE-V 2. x Generator


Para sincronizar as configurações do aplicativo entre computadores dos usuários, o Microsoft User Experience Virtualization (UE-V) 2,0, o 2,1 e o 2,1 SP1 usam *modelos de local de configurações*. Alguns modelos de local de configurações estão incluídos na virtualização da experiência do usuário. Você também pode criar, editar ou validar modelos de local de configurações personalizadas usando o UE-V Generator.

O gerador do UE-V monitora aplicativos da área de trabalho do Windows para descobrir e capturar os locais onde o aplicativo armazena suas configurações. O aplicativo que é monitorado deve ser um aplicativo da área de trabalho. O UE-V Generator não pode criar um modelo de local de configurações para os seguintes tipos de aplicativos:

-   Aplicativos virtualizados

-   Aplicativos oferecidos por meio dos serviços de terminal

-   Aplicativos Java

-   Aplicativos do Windows  

Este tópico

**Locais de configurações padrão e não padrão:** O gerador UE-V ajuda você a identificar onde os aplicativos pesquisam arquivos de configurações e configurações do registro que os aplicativos usam para armazenar as informações das configurações. O gerador só descobre as configurações em locais acessíveis a um usuário padrão. As configurações armazenadas em outros locais são excluídas. As configurações descobertas são agrupadas em duas categorias: **padrão** e **não padrão**. As configurações padrão são recomendadas para sincronização, e o UE-V pode capturar e aplicá-las rapidamente. As configurações não padrão podem sincronizar as configurações, mas, devido às regras usadas pelo UE-V, essas configurações podem não ser consistente ou sincronizar as configurações de forma confiável. Essas configurações podem depender de arquivos temporários, resultar em uma sincronização não confiável ou podem não ser úteis. Esses locais de configurações são apresentados no UE-V Generator. Você pode optar por incluí-las ou excluí-las caso a caso.

O UE-V Generator abre o aplicativo como parte do processo de descoberta. O gerador pode capturar as configurações nos seguintes locais:

-   **Configurações do registro** – locais do registro em **HKEY \ _CURRENT \ _USER**

-   **Arquivos de configurações do aplicativo** – arquivos armazenados em \ \ **usuários** \ \ \ [nome de usuário \] \ \ **AppData**em  \\  **roaming**

O gerador do UE-V exclui locais, que normalmente armazenam arquivos de software do aplicativo, mas não sincronizam bem entre computadores ou ambientes do usuário. O gerador do UE-V exclui estes locais. Locais excluídos são os seguintes:

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores

-   HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows

-   Todas as chaves do registro localizadas em HKEY \ _LOCAL \ _MACHINE Hive, que exige direitos de administrador e pode exigir que você defina um contrato de controle de conta de usuário (UAC)

-   Arquivos localizados em diretórios de arquivos de programas, que exigem direitos de administrador e podem exigir a definição de um contrato de UAC

-   Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow

-   Arquivos do sistema operacional do Windows localizados em% SystemRoot%, o que exige direitos de administrador e pode exigir que um contrato de UAC seja definido

Se as chaves do registro e os arquivos armazenados nesses locais forem necessários para sincronizar as configurações do aplicativo, você pode adicionar manualmente os locais excluídos ao modelo de local de configurações durante o processo de criação de modelos (exceto para entradas do registro na seção HKEY \ _LOCAL \ _MACHINE).

## <a href="" id="edit"></a>Editar modelos de local de configurações com o UE-V Generator


Use o UE-V Generator para editar modelos de local de configurações. Quando as configurações revisadas são adicionadas aos modelos usando o UE-V Generator, as informações de versão no modelo são atualizadas automaticamente para garantir que os modelos existentes implantados na empresa sejam atualizados corretamente.

**Observação**  Se você editar um modelo do UE-V 1,0 usando o gerador UE-V 2, o modelo será convertido automaticamente em um modelo do UE-V 2. Os agentes do UE-V 1,0 não podem mais usar o modelo editado.

 

**Para editar um modelo de local de configurações de UE-V com o UE-V Generator**

1.  Clique em **Iniciar**, em **todos os programas**, em **virtualização de experiência do usuário da Microsoft**e, em seguida, clique em **Microsoft User Experience Virtualization Generator**.

2.  Clique em **Editar um modelo de local de configurações**.

3.  Na lista de modelos usados recentemente, selecione o modelo a ser editado. Ou, se preferir, clique em **procurar** para procurar o arquivo de modelo de configurações. Clique em **Avançar** para continuar.

4.  Examine as **Propriedades**, locais **do registro** e locais de **arquivos** do modelo de configurações. Edite-o conforme necessário.

    -   Na guia **Propriedades** , você pode exibir e editar as seguintes propriedades:

        -   **Nome do aplicativo**: o nome do aplicativo que está escrito na descrição das propriedades do arquivo de programa.

        -   **Nome do programa**: o nome do programa tirado das propriedades do arquivo de programa. Esse nome geralmente tem a extensão de nome de arquivo. exe.

        -   **Versão do produto**: o número da versão do produto do arquivo. exe do aplicativo. Essa propriedade, juntamente com a **versão do arquivo**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do produto.

        -   **Versão do arquivo**: o número da versão do arquivo. exe do aplicativo. Essa propriedade, juntamente com a **versão do produto**, ajuda a determinar quais aplicativos são direcionados pelo modelo de local de configurações. Essa propriedade aceita um número de versão principal. Se essa propriedade estiver vazia, o modelo de local de configurações aplica-se a todas as versões do programa.

        -   **Nome do autor do modelo** (opcional): o nome do autor do modelo de configurações.

        -   **Email do autor do modelo** (opcional): o endereço de email do autor do modelo de local de configurações.

    -   A guia **registro** lista a **chave** e o **escopo** dos locais do registro que estão incluídos no modelo de local de configurações. Você pode editar os locais do registro usando o menu suspenso **tarefas** . No menu tarefas, você pode adicionar novas chaves, editar o nome ou o escopo das chaves existentes, excluir chaves e procurar o registro no qual as chaves estão localizadas. Ao definir o escopo do registro, você pode usar o escopo **todas as configurações** para incluir todas as configurações do registro na chave especificada. Use **todas as configurações** e **subchaves** para incluir todas as configurações do registro na chave especificada, nas subchaves e nas configurações da subchave.

    -   A guia **arquivos** lista o caminho do arquivo e a máscara de arquivo dos locais de arquivos que estão incluídos no modelo de local de configurações. Você pode editar os locais dos arquivos usando o menu suspenso **tarefas** . No menu **tarefas** para locais de arquivos, você pode adicionar novos arquivos ou locais de pastas, editar o escopo de arquivos ou pastas existentes, excluir arquivos ou pastas e abrir o local selecionado no Windows Explorer. Para incluir todos os arquivos na pasta especificada, deixe a máscara de arquivo vazia.

5.  Clique em **salvar** para salvar as alterações no modelo de local de configurações.

6.  Clique em **fechar** para fechar o assistente de modelo de configurações. Saia do aplicativo do gerador do UE-V.

    Depois de editar o modelo de local de configurações para um aplicativo, você deve testar o modelo. Implante o modelo de local de configurações revisado em um ambiente de laboratório antes de colocá-lo em produção na empresa.

**Como editar manualmente um modelo de local de configurações**

1.  Crie uma cópia local do arquivo template. XML do modelo de local de configurações. Os modelos de local das configurações do UE-V são arquivos. XML que identificam os locais onde os valores das configurações da loja de aplicativos.

    **Observação**  Um modelo de local de configurações é exclusivo devido à **ID**do modelo. Se você copiar o modelo e renomear o arquivo. xml, o registro de modelo falhará porque o UE-V lê a marca de **ID** do modelo no arquivo. xml para determinar o nome, não o nome do arquivo. xml. O UE-V também lê o número da **versão** para saber se algo mudou. Se o número da versão for superior, o UE-V atualiza o modelo.

     

2.  Abra o arquivo de modelo de local de configurações com um editor de XML.

3.  Edite o arquivo de modelo de local de configurações. Todas as alterações devem estar de acordo com o arquivo de esquema do UE-V definido em [SettingsLocationTempate. xsd](https://technet.microsoft.com/library/dn763947.aspx). Por padrão, uma cópia do arquivo. xsd está localizada no \\ProgramData\\Microsoft\\UEV\\Templates.

4.  Aumente o número da **versão** para o modelo de local de configurações.

5.  Salve o arquivo de modelo de local de configurações e, em seguida, feche o editor de XML.

6.  Valide o arquivo de modelo de local de configurações modificadas usando o UE-V Generator.

7.  Você deve registrar o modelo de local de configurações do UE-V editado antes de poder sincronizar as configurações entre computadores cliente. Para registrar um modelo, abra o Windows PowerShell e execute o seguinte cmdlet: `update-uevtemplate [templatefilename]` . Em seguida, você pode copiar o arquivo para o catálogo de armazenamento de configurações. O UE-V Agent nos computadores dos usuários deve, em seguida, ser atualizado conforme programado na tarefa agendada.

## <a href="" id="validate"></a>Validar modelos de local de configurações com o UE-V Generator


É possível criar ou editar modelos de local de configurações em um editor de XML sem usar o UE-V Generator. Se fizer isso, você pode usar o UE-V Generator para validar que o XML novo ou revisado corresponde ao esquema definido para o modelo.

**Para validar um modelo de local de configurações de UE-V com o UE-V Generator**

1.  Clique em **Iniciar**, aponte para **todos os programas**, clique em **virtualização da experiência do usuário da Microsoft**e clique em **Microsoft User Experience Virtualization Generator**.

2.  Clique em **validar um modelo de local de configurações**.

3.  Na lista de modelos usados recentemente, selecione o modelo a ser editado. Você também pode **navegar** até o arquivo de modelo de configurações. Clique em **Avançar** para continuar.

4.  Clique em **validar** para continuar.

5.  Clique em **fechar** para fechar o assistente de modelo de configurações. Saia do aplicativo do gerador do UE-V.

    Depois de validar o modelo de local de configurações para um aplicativo, você deve testar o modelo. Implante o modelo em um ambiente de laboratório antes de colocá-lo em um ambiente de produção na empresa.

## <a href="" id="share"></a>Compartilhar modelos de local de configurações com a Galeria de modelos


A Galeria de modelos do Microsoft User Experience Virtualization (UE-V) 2,0 permite que os administradores compartilhem os modelos de local das configurações do UE-V. Na Galeria, você pode carregar os modelos de local de configurações para que outros usuários possam usá-los e baixar modelos criados por outros usuários. A Galeria de modelos UE-V está localizada no Microsoft TechNet [aqui](https://go.microsoft.com/fwlink/p/?LinkId=246589).

Antes de compartilhar um modelo de local de configurações na Galeria de modelos do UE-V, verifique se ele não contém nenhuma informação pessoal ou da empresa. Você pode usar qualquer visualizador de XML para abrir e exibir o conteúdo de um arquivo de modelo de local de configurações. Os seguintes valores de modelo devem ser analisados antes de compartilhar um modelo com qualquer pessoa de fora da sua empresa.

-   Nome do autor do modelo – especifique um nome geral, não identificado para o nome do autor do modelo ou exclua esses dados do modelo.

-   Email do autor do modelo – especifique um email geral e não identificado do autor do autor do modelo ou exclua esses dados do modelo.

Antes de implantar qualquer modelo de local de configurações que você baixou da Galeria UE-V, primeiro você deve testar o modelo para garantir que as configurações do aplicativo sincronizem as configurações corretamente em um ambiente de teste.






## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





