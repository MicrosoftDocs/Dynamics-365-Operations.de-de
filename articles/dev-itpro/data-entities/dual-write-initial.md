---
title: Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations und Common Data Service
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797297"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations und Common Data Service

Bevor Sie die Datenintegration verwenden, müssen Sie die anfänglichen Daten erstellen, die für Debitoren, Kreditoren und Kontakte erforderlich sind. Wenn Sie beispielsweise ein neues Element **Kreditorengruppe** erstellen und seine **Zahlungsbedingungen** als **Net30** festlegen möchten, müssen Sie vor dem Erstellen der **Kreditorengruppe** sicherstellen, dass **Net30** sowohl in Finance and Operations als auch in Common Data Service vorhanden ist. (Bald wird eine Funktion für eine Dualschreibplattform namens **Initial Sync** veröffentlicht. Diese führt eine einmalige Datensynchronisierung zwischen Finance and Operations und Common Data Service im Rahmen der dualen Schreibeinrichtung durch.)

Tipps: Wir veröffentlichen eine Dualschreibzuordnung für alle Referenzdaten einschließlich **Zahlungsbedingungen**. Wenn Sie die anfänglichen Daten bereits in einem System haben, kann ein kleiner Updatevorgang in einem Datensatz einen Dualschreibvorgang in diesem Datensatz auslösen. 

Sie müssen die folgende Prioritätsreihenfolge beachten und sicherstellen, dass die anfänglichen Daten sowohl in Finance and Operations als auch in Common Data Service verfügbar sind.   

## <a name="vendor"></a>Lieferant

Die Ausführungsreihenfolge für Kreditor ist:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Debitor (Organisation)

Die Ausführungsreihenfolge für Debitor ist:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontakt (Person)

Die Ausführungsreihenfolge für Kontakt ist:

```
Customer
Vendor               
```
