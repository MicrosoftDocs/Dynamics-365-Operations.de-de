---
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18d8b74bd8783c23e548a3185414d1461bc1d869
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971827"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Eine Kreditorenrechnung in der Rechnungserfassung erfassen

[!include [banner](../../includes/banner.md)]

Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind. Beispiele dieses Typs der Rechnung umfassen Ausgaben für Verbrauchsmaterial oder Dienstleistungen.  Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Arbeitsbereiche > Kreditorenrechnungseintrag**.
2. Klicken Sie im **Aktivitätsbereich** auf **Neue Rechnungserfassung**.
3. Klicken Sie auf **Neu**.
4. Geben Sie im Feld **Name** den Erfassungsnamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Geben Sie im Feld **Beschreibung** einen Wert ein.
6. Klicken Sie im **Aktivitätsbereich** auf **Positionen**. Geben Sie im Feld **Datum** das Buchungsdatum ein, das das Hauptbuch aktualisiert.  
7. Geben Sie im Feld **Konto** das **Kreditorenkonto** an.
8. Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.
9. Geben Sie im Feld **Beschreibung** einen Wert ein.
10. Geben Sie im Feld **Kredit** eine Zahl ein.
11. Geben Sie im Feld **Gegenkonto** den Kontonamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die **Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Kreditorenkonto.  
    * Die **Artikel-Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Hauptkonto, das im Feld **Gegenkonto** angegeben ist.  
    * Das **Fälligkeitsdatum** wird anhand der Zahlungsbedingungen berechnet.  
    * Der **Skonto** wird standardmäßig aus dem Kreditorenkonto ermittelt.
12. Wenn Sie den Workflow für die Kreditorenrechnungserfassung aktiviert haben, klicken Sie auf **Workflow > Senden**.
    * Wenn Ihre Übermittlung genehmigt wurde, wird das Datum auf den ersten Tag des nächsten offenen Zeitraums vorverlegt, wenn das Datum der Transaktionsbuchung in einen Zeitraum fällt, der für die Buchung im Hauptbuch gesperrt oder geschlossen ist.
12. Klicken Sie auf **Buchen**.
13. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]