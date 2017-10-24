--- 
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Eine Kreditorenrechnung in der Rechnungserfassung erfassen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind. Beispiele dieses Typs der Rechnung umfassen Ausgaben für Verbrauchsmaterial oder Dienstleistungen.  Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Kreditoren" > "Arbeitsbereiche" > "Kreditorenrechnungseintrag".
2. Klicken Sie auf "Neue Rechnungserfassung".
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Name" den Erfassungsname ein oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf "Positionen".
    * Geben Sie im Feld "Datum" das Buchungsdatum ein, das das Hauptbuch aktualisiert.  
7. Geben Sie im Feld "Konto" das "Kreditorenkonto" an.
8. Geben Sie im Feld "Rechnung" die Rechnungsnummer ein.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Geben Sie im Feld "Kredit" eine Zahl ein.
11. Geben Sie im Feld "Gegenkonto" den Kontoname ein oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Mehrwertsteuergruppe bezieht sich standardmäßig auf das Kreditorenkonto.  
    * Die Artikelmehrwertsteuer-Gruppe bezieht sich standardmäßig auf das Hauptkonto, das im Feld "Gegenkonto" angegeben ist.  
    * Das "Fälligkeitsdatum" wird anhand der "Zahlungsbedingungen" berechnet.  
    * Der "Skonto" wird standardmäßig aus dem Kreditorenkonto ermittelt.  
12. Klicken Sie auf "Buchen".
13. Schließen Sie die Seite.


