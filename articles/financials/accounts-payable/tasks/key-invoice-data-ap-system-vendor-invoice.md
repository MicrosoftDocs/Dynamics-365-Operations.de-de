--- 
title: Rechnungsdaten mit einer Kreditorenrechnung in Kreditorenkonten eingeben
description: "Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich)."
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Rechnungsdaten mit einer Kreditorenrechnung in Kreditorenkonten eingeben

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabenleitfaden unterstützt Sie beim Erstellen einer Kreditorenrechnung anhand einer Bestellung und beim Anzeigen der Ergebnisse des Abgleichs von Bestellung, Zugang und Rechnung (dreiseitiger Abgleich).


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie einen Kreditor, um ihn auszuwählen. Führen Sie beispielsweise einen Bildlauf nach unten zu US-104 durch.
5. Wählen Sie Kreditor US-104 aus.
6. Klicken Sie auf "OK".
7. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Wählen Sie einen Lagerartikel aus. Wählen Sie beispielsweise die Artikelnummer 1000 aus.
9. Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".
10. Klicken Sie auf die Registerkarte "Einstellungen".
    * Sie können die Abgleichsrichtlinie außer Kraft setzen, um keinen Abgleich, einen zweiseitigen Abgleich oder einen dreiseitigen Abgleich zu verwenden.  
11. Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".
12. Klicken Sie im Aktivitätsbereich auf "Einkauf".
13. Klicken Sie auf "Bestätigen".

## <a name="receive-the-products"></a>Die Produkte empfangen
1. Klicken Sie im Aktivitätsbereich auf "Empfangen".
2. Klicken Sie auf "Produktzugang".
3. Geben Sie im Feld "Produktzugang" die Produktzugangsnummer ein. Geben Sie beispielsweise "PR123" ein.
4. Klicken Sie auf "OK", um den Produktzugang zu buchen.
5. Schließen Sie die Seite.

## <a name="create-a-vendor-invoice"></a>Eine Kreditorenrechnung erstellen
1. Wechseln Sie zu Kreditoren > Bestellungen > Bestellungen wurden empfangen, jedoch nicht fakturiert.
2. Wählen Sie die Bestellung aus, die Sie erstellt haben.
3. Klicken Sie im Aktivitätsbereich auf "Rechnung".
4. Klicken Sie auf "Rechnung".
5. Geben Sie im Feld "Nummer" die Rechnungsnummer ein.
6. Geben Sie im Feld "Rechnungsbeschreibung" einen Wert ein.
7. Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.
8. Geben Sie im Feld "Einzelpreis" die Zahl 1200 ein.
9. Klicken Sie auf "Position hinzufügen".
10. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Suchen Sie in der Liste die Installationsgebühr-Artikelnummer. Beispielsweise S0001
12. Wählen Sie die Installationsgebühr-Artikelnummer aus.
    * Beachten Sie, dass kein Abgleich ausgeführt wurde, seit Sie die Änderungen vorgenommen haben.  
13. Klicken Sie auf "Status des Abgleichs aktualisieren".
14. Klicken Sie im Aktivitätsbereich auf "Überprüfen".
15. Klicken Sie auf "Detailabgleich".
    * Die neue Position mit Diensten muss nicht abgeglichen werden, damit bleibt der Status "Nicht ausgeführt".  
16. Wählen Sie den Produktzugang für den Lagerartikel aus, den Sie empfangen haben.
    * Die Position mit dem Produktzugang wurde abgeglichen, allerdings stimmen Menge oder Preis nicht überein, daher wird ein Fehler ausgegeben.  
17. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
    * Jetzt, da der Preis je Einheit übereinstimmt, wird der Status zu "Bestanden" aktualisiert. Wenn Ihre Richtlinie Abweichungen zulässt oder wenn der Abgleich nur eine Warnung ist, können Sie die Rechnung dennoch buchen.  
18. Schließen Sie die Seite.
19. Klicken Sie auf "Buchen".
20. Schließt das Formular.
    * Beachten Sie, dass die Bestellung nicht mehr als "Empfangen", sondern als "Nicht fakturiert" aufgeführt ist.  


