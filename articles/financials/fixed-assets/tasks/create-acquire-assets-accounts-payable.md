--- 
title: Anlagen von Kreditoren erstellen und erwerben
description: "Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: de-de
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Anlagen von Kreditoren erstellen und erwerben

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess. Dabei werden der "Buchhalter" und die "Sachbearbeiter Kreditorenkonten" und das Demo-Unternehmen USMF verwendet.


## <a name="set-fixed-assets-parameters"></a>Anlagenparametern festlegen
1. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter".
2. Erweitern oder reduzieren Sie den Abschnitt "Bestellung".
3. Aktivieren Sie das Kontrollkästchen "Anlagenanschaffung aus Einkauf zulassen".
4. Aktivieren Sie das Kontrollkästchen "Anlage bei Buchung von Produktzugang oder Rechnung erstellen".

## <a name="create-a-new-vendor-invoice"></a>Eine neue Kreditorenrechnung erstellen
1. Wechseln Sie zu "Kreditoren" > "Arbeitsbereiche" > "Kreditorenrechnungseintrag".
2. Klicken Sie auf "Neue Kreditorenrechnung".
3. Klicken Sie im Feld "Rechnungskonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Geben Sie im Feld "Zahl" einen Wert ein.
6. Geben Sie im Feld "Buchungsdatum" ein Datum ein.
7. Klicken Sie auf "Position hinzufügen".
8. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Entweder nicht gelagerte Artikel oder Beschaffungskategorien können für Anlagenanschaffung verwendet werden.  
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Geben Sie im Feld "Menge" eine Zahl ein.
    * Eine Rechnungsposition erstellt nur eine Anlage, unabhängig von Menge.  Der Rechnungsmengen-Feldwert wird zur Anlagenmenge übertragen.  
11. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
12. Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".
13. Klicken Sie auf die Registerkarte "Anlagen".
14. Aktivieren Sie das Kontrollkästchen "Neue Anlage erstellen".
15. Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
16. Wählen Sie in der Liste die Anlagengruppe aus, die beim Erstellen der neuen Anlage zu verwenden ist.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie auf "Buchen".
    * Die Anlage wird erstellt und abgerufen, wann die Rechnung gebucht wird.  


