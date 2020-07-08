---
title: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
description: Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797716"
---
# Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 da Microsoft


Outubro de 2009

## Sobre o gerenciamento avançado de política de grupo 4,0 da Microsoft


O gerenciamento avançado de política de grupo (AGPM) da Microsoft 4,0 estende os recursos do console de gerenciamento de política de grupo (GPMC). O AGPM oferece controle de alterações abrangente e gerenciamento aprimorado dos objetos de política de grupo (GPOs).

Os documentos a seguir podem ajudá-lo a começar a usar o AGPM 4,0.

-   Para obter uma visão geral dos recursos do AGPM, consulte [visão geral do gerenciamento avançado de política de grupo da Microsoft](https://go.microsoft.com/fwlink/?LinkID=162671) ( https://go.microsoft.com/fwlink/?LinkID=162671) .

-   Para obter informações sobre como o AGPM 4,0 é diferente do AGPM 3,0, consulte [novidades do agpm 4,0](https://go.microsoft.com/fwlink/?LinkId=160058) ( https://go.microsoft.com/fwlink/?LinkId=160058) .

-   Para obter orientação sobre como determinar se o AGPM 4,0, o AGPM 3,0 ou o AGPM 2,5 é apropriado para o seu ambiente, consulte [escolhendo qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=145981) ( https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Para obter orientação básica sobre como instalar o AGPM e um cenário de exemplo para usar o AGPM, consulte o guia passo a [passo para o gerenciamento avançado de política de grupo 4,0](https://go.microsoft.com/fwlink/?LinkID=153505) ( https://go.microsoft.com/fwlink/?LinkID=153505) . Este guia foi projetado principalmente para ajudar avaliadores e usuários iniciantes.

-   Para obter informações sobre como atualizar de uma versão anterior do AGPM ou uma orientação detalhada sobre como planejar a implantação do AGPM em sua organização, consulte o [Guia de planejamento para o gerenciamento avançado de política de grupo da Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkID=156883) ( https://go.microsoft.com/fwlink/?LinkID=156883) .

-   Para obter informações sobre como usar o AGPM para executar tarefas específicas, consulte a ajuda do gerenciamento avançado de política de grupo 4,0, que também está disponível no TechNet como o [Guia de operações para o AGPM 4,0](https://go.microsoft.com/fwlink/?LinkId=159872) ( https://go.microsoft.com/fwlink/?LinkId=159872) .

## Mais informações


Para obter mais informações sobre o AGPM, consulte o seguinte:

-   [Biblioteca do TechNet de gerenciamento de política de grupo avançado](https://go.microsoft.com/fwlink/?LinkID=146846) (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [TechCenter do Microsoft Desktop Optimization Pack](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [TechCenter de política de grupo](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## Fornecendo comentários


Você pode postar comentários ou perguntas sobre o AGPM para o [Fórum de política de grupo](https://go.microsoft.com/fwlink/?LinkId=145532) ( https://go.microsoft.com/fwlink/?LinkId=145532) .

## Problemas conhecidos com o AGPM 4,0


### O comando importar da produção não importa configurações para um GPO com check-out

Se você editar um GPO no ambiente de produção, deverá importar o GPO da produção para atualizar o GPO no arquivo morto offline. O comando **importar da produção** tem o objetivo de permitir que você execute um backup final da produção antes de terminar a edição para que você possa reverter para o backup de produção, se for necessário.

Se o GPO estiver com check-out quando você executar o comando **importar da produção** , as alterações de produção não serão incorporadas à versão verificada do GPO. No entanto, a versão importada do GPO é adicionada ao histórico do GPO, embora essa versão não esteja disponível para edição. Quando o GPO tiver sido verificado, essa versão substituirá a versão importada no arquivo, mas ambos estarão disponíveis no histórico do GPO.

**Solução alternativa:** Verifique se o GPO está marcado antes de importá-lo da produção. Se o GPO não tiver sido verificado antes de ser importado, você poderá usar o comando **Undo check out** para descartar suas alterações e reverter para a versão do GPO importada da produção.

### Os GPOs com check-out não podem ser editados por vários minutos em um ambiente que usa uma topologia de vários sites do Active Directory

O AGPM usa um modelo cliente/servidor. O servidor do AGPM e o cliente do AGPM determinam seu próprio controlador de domínio mais próximo para operações de política de grupo. Ao fazer o check-out de um GPO usando um cliente do AGPM, na verdade, ele é o servidor do AGPM que verifica o GPO do arquivo offline para uma pasta temporária na pasta SYSVOL.

Se o servidor do AGPM e o cliente do AGPM estiverem em sites diferentes, o GPO com check-out temporário poderá não estar presente no controlador de domínio do site local por vários minutos ou até 30 minutos devido à latência de replicação do SYSVOL. Nessa situação, você não pode editar o GPO com check-out usando o GPMC em um cliente do AGPM até que a duplicação de SYSVOL do GPO com check-out ocorra.

**Solução alternativa:** Como prática recomendada, você deve posicionar os clientes do AGPM no mesmo site que o servidor do AGPM ao qual se conectam para que você não precise aguardar que a replicação do SYSVOL ocorra antes de editar um GPO com check-out.

### O AGPM não poderá ler o limite de backup se a sua conta não tiver permissões para o arquivo morto

Em um cliente do AGPM, se você fizer logon usando uma conta que não tenha sido delegada para o arquivo do AGPM, inicie o console de gerenciamento de política de grupo (GPMC) e clique em **alterar controle**, você receberá o erro a seguir.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**Solução alternativa:** Entre em contato com um administrador do AGPM (controle total) e solicite que ele delegue o acesso ao AGPM para a sua conta. Se você for um administrador do AGPM, faça logon usando uma conta para a qual a função de administrador do AGPM seja atribuída para que você possa delegar o acesso à conta adicional. Para obter mais informações, consulte "delegar o acesso no nível do domínio ao arquivo morto" na ajuda do AGPM.

## Informações de direitos autorais da versão


As informações contidas neste documento, incluindo URL e outras referências de site da Web na Internet, estão sujeitas a alterações sem aviso prévio e são fornecidas apenas para fins informativos. Todo o risco do uso ou dos resultados do uso deste documento permanece com o usuário, e a Microsoft Corporation não oferece nenhuma garantia, seja expressa ou implícita. Os exemplos de empresas, organizações, produtos, pessoas e eventos descritos aqui são fictícios. Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional ou deve ser inferida. Obedecer a todas as leis de direitos autorais aplicáveis é responsável pelo usuário. Sem limitar os direitos sob direitos autorais, nenhuma parte deste documento pode ser reproduzida, armazenada ou introduzida em um sistema de recuperação, ou transmitida de qualquer forma ou por qualquer meio (eletrônico, mecânico, fotocópia, gravação ou de outra forma) ou para qualquer propósito, sem a permissão expressa por escrito da Microsoft Corporation.

A Microsoft pode ter patentes, aplicativos de patente, marcas comerciais, direitos autorais ou outros direitos de propriedade intelectual que abranjam o assunto deste documento. Exceto conforme expressamente fornecido em qualquer contrato de licença escrito da Microsoft, o fornecimento deste documento não lhe concede nenhuma licença para essas patentes, marcas comerciais, direitos autorais ou outra propriedade intelectual.



Microsoft, MS-DOS, Windows, WindowsServer e Windows Vista são marcas registradas ou marcas comerciais da MicrosoftCorporation nos Estados Unidos e/ou em outros países.

Os nomes das empresas e produtos reais mencionados aqui podem ser marcas comerciais de seus respectivos proprietários.

 

 





