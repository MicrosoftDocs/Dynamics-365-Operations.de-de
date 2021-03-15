---
title: Rechnungen und Schlüsseldaten im Kreditorsystem überwachen
description: In diesem Thema wird gezeigt, wie Rechnungen und Schlüsseldaten in Kreditorenkonten geprüft werden.
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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e173d2efe0d5acb1be60c9ba315c21563c2bf105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994764"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Rechnungen und Schlüsseldaten im Kreditorsystem überwachen

[!include [banner](../../includes/banner.md)]

Wenn Sie von einem Kreditor eine Rechnung für die Waren oder Dienstleistungen einer Bestellung erhalten, muss gemäß den Unternehmensrichtlinien möglicherweise zunächst der Eingang der Waren bzw. die Erbringung der Dienstleistungen stattfinden, bevor die Bezahlung der Rechnung genehmigt wird. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. 

Stellen Sie auf der Seite **Kreditorenparameter** sicher, dass die Option „Rechnungsabgleichüberprüfung aktivieren“ ausgewählt ist, dass das Feld **Rechnung mit Abweichungen buchen** auf **Genehmigung anfordern** festgelegt ist und das Feld **Positionsabgleichsrichtlinie** auf **Dreiseitiger Abgleich** festgelegt ist.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]