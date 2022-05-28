---
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716640"
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
