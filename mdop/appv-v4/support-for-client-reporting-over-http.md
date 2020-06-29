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
# <span data-ttu-id="a29db-103">Suporte para relatórios de clientes via HTTP</span><span class="sxs-lookup"><span data-stu-id="a29db-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="a29db-104">A versão 4,6 do cliente App-V agora oferece suporte ao uso de comunicação HTTP ao enviar dados de relatório do cliente para o servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="a29db-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="a29db-105">Esse recurso dá suporte a cenários em que um cliente implementou um servidor de publicação HTTP (S) personalizado que está configurado para coletar e processar dados do cliente.</span><span class="sxs-lookup"><span data-stu-id="a29db-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="a29db-106">Para obter mais informações sobre servidores de publicação HTTP, consulte</span><span class="sxs-lookup"><span data-stu-id="a29db-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="a29db-107">Relatório de cliente via HTTP</span><span class="sxs-lookup"><span data-stu-id="a29db-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="a29db-108">O cliente começa a coletar dados quando recebe um atributo "Reporting =" TRUE "" no XML de resposta de atualização de publicação do Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="a29db-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="a29db-109">Quando esse atributo é recebido, o cliente envia todos os dados acumulados para o servidor de publicação que enviou a atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="a29db-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="a29db-110">Os detalhes desse processo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="a29db-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="a29db-111">O cliente envia uma solicitação HTTP GET para o servidor de publicação para uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="a29db-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="a29db-112">O cabeçalho dessa mensagem contém um cabeçalho personalizado "AppV-op: Refresh" que o servidor de publicação HTTP (S) personalizado usa para identificar o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29db-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="a29db-113">Em seguida, o servidor de publicação envia o XML de resposta de atualização de publicação que contém um valor "Reporting =" TRUE "".</span><span class="sxs-lookup"><span data-stu-id="a29db-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="a29db-114">Em seguida, o cliente envia uma solicitação HTTP POST para o servidor de publicação, juntamente com os dados de relatório que foram coletados desde a atualização anterior.</span><span class="sxs-lookup"><span data-stu-id="a29db-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="a29db-115">O cabeçalho dessa mensagem contém um cabeçalho personalizado "AppV-op: Report" que o servidor de publicação HTTP (S) personalizado usa para identificar o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a29db-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="a29db-116">O esquema a seguir fornece detalhes específicos do pacote e os dados de aplicativo que são enviados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a29db-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

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

 

 





