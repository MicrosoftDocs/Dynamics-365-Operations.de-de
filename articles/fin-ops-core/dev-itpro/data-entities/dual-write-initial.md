---
title: Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations-Apps und Common Data Service
description: In diesem Thema wird die Synchronisierungsreihenfolge angegeben, die Sie beim Erstellen der anfänglichen Daten befolgen müssen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769636"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations-Apps und Common Data Service

[!include [banner](../includes/banner.md)]

Bevor Sie die Datenintegration verwenden, müssen Sie die anfänglichen Daten erstellen, die für Debitoren, Kreditoren und Kontakte erforderlich sind. Angenommen, Sie möchten einen neuen **Kreditorengruppe**-Artikel erstellen und seinen **Zahlungsbedingungen**-Wert auf **Net30** festlegen. In diesem Fall müssen Sie, bevor Sie versuchen, den **Kreditorengruppe**-Artikel zu erstellen, überprüfen, ob **Net30** in der Anwendung und Common Data Service vorhanden ist. (Bald wird eine Funktion für eine Dualschreibplattform namens Initial Sync von Microsoft veröffentlicht. Diese führt eine einmalige Datensynchronisierung zwischen der Anwendung und Common Data Service im Rahmen der dualen Schreibeinrichtung durch.)

> [!TIP]
> Microsoft veröffentlicht eine Dualschreibzuordnung für alle Referenzdaten einschließlich **Zahlungsbedingungen**. Wenn Sie die anfänglichen Daten bereits in einem System haben, kann ein kleiner Updatevorgang in einem Datensatz einen Dualschreibvorgang in diesem Datensatz auslösen.

Sie müssen die folgende Prioritätsreihenfolge beachten und sicherstellen, dass die anfänglichen Daten sowohl in der Anwendung als auch in Common Data Service verfügbar sind.

## <a name="vendor"></a>Lieferant

Hier die Reihenfolge der Ausführung für die **Kreditor**-Entität:

1. Kreditorengruppe

    1. Zahlungsbedingungen

        1. Zahlungstag und -positionen
        2. Zahlungszeitplan

2. Kreditorzahlungsmethode

## <a name="customer-organization"></a>Debitor (Organisation)

Hier die Reihenfolge der Ausführung für die **Debitor**-Entität:

1. Debitorengruppe

    1. Zahlungsbedingungen

        1. Zahlungstag und -positionen
        2. Zahlung 

2. Zahlungsmethode für Debitoren

## <a name="contact-person"></a>Kontakt (Person)

Hier die Reihenfolge der Ausführung für die **Kontakt**-Entität:

1. Debitor
2. Lieferant
