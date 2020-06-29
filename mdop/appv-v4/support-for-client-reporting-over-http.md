---
title: Suporte para relatórios de clientes via HTTP
description: Suporte para relatórios de clientes via HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796695"
---
# Suporte para relatórios de clientes via HTTP


A versão 4,6 do cliente App-V agora oferece suporte ao uso de comunicação HTTP ao enviar dados de relatório do cliente para o servidor de publicação. Esse recurso dá suporte a cenários em que um cliente implementou um servidor de publicação HTTP (S) personalizado que está configurado para coletar e processar dados do cliente.

Para obter mais informações sobre servidores de publicação HTTP, consulte <https://go.microsoft.com/fwlink/?LinkId=157426>

## Relatório de cliente via HTTP


O cliente começa a coletar dados quando recebe um atributo "Reporting =" TRUE "" no XML de resposta de atualização de publicação do Publishing Server. Quando esse atributo é recebido, o cliente envia todos os dados acumulados para o servidor de publicação que enviou a atualização de publicação. Os detalhes desse processo são os seguintes:

-   O cliente envia uma solicitação HTTP GET para o servidor de publicação para uma atualização de publicação. O cabeçalho dessa mensagem contém um cabeçalho personalizado "AppV-op: Refresh" que o servidor de publicação HTTP (S) personalizado usa para identificar o tipo de mensagem.

-   Em seguida, o servidor de publicação envia o XML de resposta de atualização de publicação que contém um valor "Reporting =" TRUE "".

-   Em seguida, o cliente envia uma solicitação HTTP POST para o servidor de publicação, juntamente com os dados de relatório que foram coletados desde a atualização anterior. O cabeçalho dessa mensagem contém um cabeçalho personalizado "AppV-op: Report" que o servidor de publicação HTTP (S) personalizado usa para identificar o tipo de mensagem.

O esquema a seguir fornece detalhes específicos do pacote e os dados de aplicativo que são enviados para o servidor.

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





