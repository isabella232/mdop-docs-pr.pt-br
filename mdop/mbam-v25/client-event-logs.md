---
title: Logs de eventos do cliente
description: Logs de eventos do cliente
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799423"
---
# Logs de eventos do cliente

Os logs de eventos do cliente MBAM estão localizados em Visualizador de eventos – logs de aplicativos e serviços – Microsoft – Windows – MBAM-caminho operacional.
A tabela a seguir contém as identificações de eventos que podem ocorrer no cliente MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID do evento</th>
<th align="left">Canal</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensagem</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>um</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>As políticas de MBAM foram aplicadas com êxito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>Ocorreu um erro ao aplicar políticas de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3D</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>Os dados do status de criptografia foram enviados com êxito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Ocorreu um erro ao enviar dados de status de criptografia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>08</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>O volume do sistema está ausente. SystemVolume é necessário para criptografar a unidade do sistema operacional.</p></td>
</tr>
<tr class="even">
<td align="left"><p>222</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>O hardware TPM está ausente. É necessário que o TPM criptografe a unidade do sistema operacional com qualquer protetor TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>254</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>O computador está isento da criptografia. Status de hardware da máquina: isento</p></td>
</tr>
<tr class="even">
<td align="left"><p>11:00</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>O computador está isento da criptografia. Status de hardware da máquina: desconhecido</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>Falha na verificação de isenção de hardware.</p></td>
</tr>
<tr class="even">
<td align="left"><p>0,13</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>O usuário está isento de criptografia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>quatorze</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>O usuário solicitou uma isenção.</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Falha na verificação de isenção de usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>Useradiamento</p></td>
<td align="left"><p>O usuário adie o processo de criptografia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>16</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>Falha na inicialização do TPM. O usuário rejeitou as mudanças do BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>dezoito</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>Não é possível se conectar ao serviço de recuperação e hardware do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>pol</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Conectado com êxito ao serviço de recuperação e hardware do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cedido</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>A política MBAM está em conflito ou está corrompida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>21</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Conflito nas políticas de criptografia de volume do so detectado. Verifique as políticas de BitLocker e MBAM relacionadas aos protetores de unidade do sistema operacional.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>22</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Conflito detectados nas políticas de criptografia de volume da unidade de dados fixas. Verifique as políticas de BitLocker e MBAM relacionadas a protetores de unidade de FDD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>Ocorreu um erro durante a criptografia. Um protetor de agente de recuperação de dados (DRA) é necessário no modo FIPS para máquinas anteriores ao Windows 8,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>28</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>O TPM OwnerAuth foi reapresentado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>anos</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>A chave de recuperação do BitLocker do volume foi em caução.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>30</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>A chave de recuperação do BitLocker do volume foi atualizada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>31</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p>A data da política de aplicação, <em> &lt; Data &gt; </em> , foi definida para o volume</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p>A data da política de aplicação, <em> &lt; Data &gt; </em> , foi limpa para o volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>O bloqueio do TPM foi redefinido com êxito.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Falha ao redefinir o bloqueio do TPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>OwnerAuth de TPM recuperados com êxito dos serviços do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Falha ao recuperar o TPM OwnerAuth dos serviços do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Falha ao atualizar o caminho de pesquisa de DLL para o provedor WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>Agente interrompido-tempo limite esgotado ao aguardar a instância do provedor WMI MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>A unidade removível foi montada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>A unidade removível foi desmontada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>Falha na conexão com o serviço de recuperação e recuperação do MBAM impedia a aplicação bem-sucedida das políticas do MBAM ao volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>Estado do volume bloqueado impedia a aplicação bem-sucedida das políticas de MBAM ao volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Operacionais</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>Falha ao se conectar ao serviço de conformidade e status da MBAM impedia a transferência de dados de status de criptografia.</p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados
[Referência técnica do MBAM 2.5](technical-reference-for-mbam-25.md)

[Logs de eventos do servidor](server-event-logs.md)

 


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





