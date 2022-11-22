---
title: Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen
description: Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778688"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen

[!include [banner](../../includes/banner.md)]

Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. 

Stellen Sie auf der Seite **Kreditorenparameter** sicher, dass die Option **Rechnungsabgleichüberprüfung aktivieren** ausgewählt ist, dass das Feld **Rechnung mit Abweichungen buchen** auf **Genehmigung anfordern** festgelegt ist und das Feld **Positionsabgleichsrichtlinie** auf **Dreiseitiger Abgleich** festgelegt ist.

Für diese Prozedur wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie zu **Alle Bestellungen**.
2. Klicken Sie auf **Neu**.
3. Klicken Sie im Feld **Kreditorenkonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Geben Sie im Feld **Lieferantenkonto** einen Wert ein.
5. Klicken Sie auf **OK**.
6. Klicken Sie auf **Position hinzufügen**.
7. Geben Sie im Feld **Artikelnummer** einen Wert ein.
8. Klicken Sie im Aktionsbereich auf **Einkauf**.
9. Klicken Sie auf **Bestätigen**.

## <a name="post-a-product-receipt"></a>Einen Produktzugang buchen
1. Klicken Sie im Aktionsbereich auf **Empfangen**.
2. Klicken Sie auf **Produktzugang**.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld **Produktzugang** einen Wert ein.
5. Klicken Sie auf **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Eine Kreditorenrechnung erfassen und einem Produktzugang zuordnen
1. Klicken Sie im Aktivitätsbereich auf **Rechnung**.
2. Klicken Sie auf **Rechnung**.
3. Geben Sie im Feld **Zahl** einen Wert ein.
4. Klicken Sie auf **Standard aus: Bestellte Menge** um das Ablagedialogfeld zu öffnen.
5. Wählen Sie im Feld **Standardmenge für Positionen** eine Option aus.
6. Klicken Sie auf **OK**.
7. Klicken Sie auf **Ja**.
8. Klicken Sie auf **Produktzugänge abgleichen**.
9. Klicken Sie auf **OK**.
10. Klicken Sie im Aktionsbereich auf **Überprüfen**.
11. Klicken Sie auf **Detailabgleich**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
