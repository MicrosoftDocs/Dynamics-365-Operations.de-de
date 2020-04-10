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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140374"
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
12. Klicken Sie auf **Buchen**.
13. Schließen Sie die Seite.

