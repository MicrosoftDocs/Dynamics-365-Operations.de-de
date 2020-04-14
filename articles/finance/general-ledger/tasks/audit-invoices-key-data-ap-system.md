---
title: Rechnungen und Schlüsseldaten im Kreditor-System überwachen
description: Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139942"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a>Rechnungen und Schlüsseldaten im Kreditor-System überwachen

[!include [banner](../../includes/banner.md)]

Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. 

Stellen Sie auf der Seite "Kreditorenparameter" sicher, dass die Option "Rechnungsabgleichüberprüfung aktivieren" ausgewählt ist, dass das Feld "Rechnung mit Abweichungen buchen" auf "Genehmigung anfordern" fesgelegt ist und das Feld "Positionsabgleichsrichtlinie" auf "Dreiseitiger Abgleich" festgelegt ist.

Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie zu **Alle Bestellungen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Lieferantenkonto** einen Wert ein.
4. Klicken Sie auf **OK**.
5. Klicken Sie auf **Position hinzufügen**.
6. Geben Sie im Feld **Artikelnummer** einen Wert ein.
7. Klicken Sie im Aktionsbereich auf **Einkauf**.
8. Klicken Sie auf **Bestätigen**.

## <a name="post-a-product-receipt"></a>Einen Produktzugang buchen
1. Klicken Sie im Aktionsbereich auf **Empfangen**.
2. Klicken Sie auf **Produktzugang**.
3. Geben Sie im Feld **Produktzugang** einen Wert ein.
4. Klicken Sie auf **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Eine Kreditorenrechnung erfassen und einem Produktzugang zuordnen
1. Klicken Sie im Aktionsbereich auf **Rechnung > Rechnung**.
2. Geben Sie im Feld **Zahl** einen Wert ein.
3. Klicken Sie auf **Standard aus: Bestellte Menge** um das Ablagedialogfeld zu öffnen.
4. Wählen Sie im Feld **Standardmenge für Positionen** eine Option aus.
5. Klicken Sie auf **OK**.
6. Klicken Sie auf **Ja**.
7. Klicken Sie auf **Produktzugänge abgleichen**.
8. Klicken Sie auf **OK**.
9. Klicken Sie im Aktionsbereich auf **Überprüfen**.
10. Klicken Sie auf **Detailabgleich**.

