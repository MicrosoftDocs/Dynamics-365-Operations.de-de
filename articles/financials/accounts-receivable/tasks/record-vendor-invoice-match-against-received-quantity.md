--- 
title: Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen
description: "Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a64413ac1840ef535252bd2d9752d52b26ccade1
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. 

Stellen Sie auf der Seite "Kreditorenparameter" sicher, dass die Option "Rechnungsabgleichüberprüfung aktivieren" ausgewählt ist, dass das Feld "Rechnung mit Abweichungen buchen" auf "Genehmigung anfordern" fesgelegt ist und das Feld "Positionsabgleichsrichtlinie" auf "Dreiseitiger Abgleich" festgelegt ist.

Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie zu "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Geben Sie im Feld "Kreditorenkonto" einen Wert ein.
5. Klicken Sie auf "OK".
6. Klicken Sie auf "Position hinzufügen".
7. Geben Sie im Feld "Artikelnummer" einen Wert ein.
8. Klicken Sie im Aktivitätsbereich auf "Einkauf".
9. Klicken Sie auf "Bestätigen".

## <a name="post-a-product-receipt"></a>Einen Produktzugang buchen
1. Klicken Sie im Aktivitätsbereich auf "Empfangen".
2. Klicken Sie auf "Produktzugang".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld "Produktzugang" einen Wert ein.
5. Klicken Sie auf "OK".

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Eine Kreditorenrechnung erfassen und einem Produktzugang zuordnen
1. Klicken Sie im Aktivitätsbereich auf "Rechnung".
2. Klicken Sie auf "Rechnung".
3. Geben Sie im Feld "Zahl" einen Wert ein.
4. Klicken Sie auf "Standard" aus: "Bestellte Menge" um das Ablagedialogfeld zu öffnen.
5. Wählen Sie im Feld "Standardmenge für Positionen" eine Option aus.
6. Klicken Sie auf "OK".
7. Klicken Sie auf "Ja".
8. Klicken Sie auf "Produktzugänge abgleichen".
9. Klicken Sie auf "OK".
10. Klicken Sie im Aktivitätsbereich auf "Überprüfen".
11. Klicken Sie auf "Detailabgleich".


