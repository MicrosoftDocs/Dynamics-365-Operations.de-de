---
title: Kanalübersicht
description: Dieses Thema bietet einen Überblick über Kanäle in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412525"
---
# <a name="channels-overview"></a>Kanalübersicht


[!include [banner](includes/banner.md)]

Dieses Thema bietet einen Überblick über Kanäle in Microsoft Dynamics 365 Commerce. Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie die einzelnen Kanäle einrichten.

## <a name="types-of-channels"></a>Kanaltypen

Dynamics 365 Commerceunterstützt drei verschiedene Kanaltypen: Einzelhandel, Callcenter und Onlinekanäle.

### <a name="retail-channels"></a>Einzelhandelskanäle

Retail Channel repräsentieren herkömmliche physische Shops. Jeder Shop kann seine eigenen POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten. 

### <a name="call-center-channels"></a>Callcenterkanäle

Callcenterkanäle stehen für die Callcenter-Bestellung und Kundenverwaltung.

### <a name="online-channels"></a>Onlinekanäle

Onlinekanäle repräsentieren Online-E-Commerce-Schaufenster. Sobald ein Onlinekanal erstellt wurde, muss eine Site mit dem Microsoft Dynamics 365 Commerce Site Builder-Tool oder einer anderen E-Commerce-Lösung eines Drittanbieters erstellt werden.

## <a name="channel-setup-basics"></a>Grundlagen der Kanaleinrichtung

Die Kanaleinrichtung wird im Commerce-Tool durchgeführt. Jeder Kanal kann über eigene Zahlungsmethoden, Preisgruppen, Produkthierarchien, Sortimente und Produktgruppen verfügen. Nachdem Sie einen Kanal erstellt haben, weisen Sie die Produkte zu, die Sie führen und verkaufen möchten. Jeder Kanaltyp verfügt über eine Reihe von Funktionen, die möglicherweise konfiguriert werden müssen. Ein Retail Channel benötigt beispielsweise zugewiesene Mitarbeiter, Register und Kunden. Sobald ein neuer Kanal erstellt wurde, muss er einer Organisationshierarchie zugewiesen werden.

## <a name="channel-setup-prerequisites"></a>Voraussetzungen der Kanaleinrichtung

Bevor Sie einen Kanal einrichten können, müssen Sie einige erforderliche Aufgaben basierend auf dem Kanaltyp ausführen. Weitere Informationen finden Sie unter [Voraussetzungen für die Kanaleinrichtung ](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Einen Kanal einrichten

Verwenden Sie nach Abschluss der erforderlichen Aufgaben die folgenden Links, um weitere Anweisungen zur Einrichtung zu erhalten.

- [Einen Retail Channel einrichten](channel-setup-retail.md)
- [Einen Callcenterkanal einrichten](channel-setup-callcenter.md)
- [Einen Onlinekanal einrichten](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)
    
[Einen Onlinekanal einrichten](channel-setup-online.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)

[Organisationshierarchien einrichten](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]