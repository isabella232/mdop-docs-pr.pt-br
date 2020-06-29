---
title: Pré-requisitos para clientes do MBAM 2.5
description: Pré-requisitos para clientes do MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799978"
---
# Pré-requisitos para clientes do MBAM 2.5


Antes de instalar o software cliente MBAM nos computadores dos usuários finais, verifique se o seu ambiente e os computadores cliente atendem aos pré-requisitos a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O domínio da empresa deve conter pelo menos um controlador de domínio do Windows Server 2008 (ou posterior).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>O computador cliente deve estar conectado à intranet da empresa.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Para computadores cliente do Windows 7 somente: cada cliente deve ter a funcionalidade do Trusted Platform Module (TPM) (TPM 1,2 ou posterior).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Para o Windows 8,1, Windows 10 RTM ou Windows 10 versão 1511 computadores cliente somente: se você quiser que o MBAM possa armazenar e gerenciar as chaves de recuperação do TPM, o provisionamento automático do TPM deve estar desativado e MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM.</p>
<p>Somente no MBAM 2,5 SP1, você não precisa mais desativar o provisionamento automático do TPM, mas deve certificar-se de que os objetos de política de grupo TPM estejam definidos para não fazer a caução do OwnerAuth do TPM para o Active Directory.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Considerações sobre segurança do MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM.</p>
<p>No MBAM 2,5 SP1, você deve ativar o provisionamento automático.</p>
</p></td>
<td align="left"><p>Consulte <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> </a> a senha de proprietário do TPM para obter mais detalhes.
</p></td>
</tr>
<tr class="even">
<td align="left"><p>O chip TPM deve estar ativado no BIOS e ser redefinido do sistema operacional.</p></td>
<td align="left"><p>Consulte a documentação do BIOS para obter mais informações.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>O disco rígido do computador deve ter pelo menos duas partições e deve ser formatado com o sistema de arquivos NTFS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>O disco rígido do computador deve ter um BIOS compatível com TPM e compatível com dispositivos USB durante a inicialização do computador.</p></td>
<td align="left"><div class="alert">
<strong>Observação</strong><br/><p>Verifique se o teclado, o vídeo ou o mouse estão diretamente conectados e não são gerenciados por meio de um botão de teclado, vídeo ou mouse (KVM). Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Se você usar um proxy, ele deve estar visível no contexto do sistema. O MBAM é executado no contexto do sistema, não no contexto do usuário.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Importante**  
Se o BitLocker tiver sido usado sem o MBAM, MBAM poderá ser instalado e utilizar as informações existentes do TPM.




## Tópicos relacionados


[Configurações com suporte no MBAM 2.5](mbam-25-supported-configurations.md)

[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






