--- 
title: Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben
description: Diese Aufgabenanleitung zeigt Ihnen, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung zeigt Ihnen, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.  Nehmen Sie anschließend den Rechnungspool, um die Rechnung mit einer Bestellung abzugleichen und die Ausgaben auf der Kreditorenrechnungsseite abzuschließen.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Bestellungen".
2. Klicken Sie auf "Neu", um eine neue Bestellung zu erstellen.
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie in der Liste einen Händler aus. Beispielsweise Händler 1001.
5. Klicken Sie auf "OK".
6. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie die Services-Artikelnummer in der Liste. Wählen Sie z. B. S0001 aus.
8. Klicken Sie auf die Artikelnummer und wählen Sie diese aus.
    * Der Nettobetrag ist 75,00.  Der ist der Betrag, den wir auf der Rechnung erwarten.  
9. Klicken Sie im Aktivitätsbereich auf "Einkauf".
10. Klicken Sie auf "Bestätigen".

## <a name="create-and-post-and-invoice"></a>Erstellen und buchen und fakturieren
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsregister".
2. Klicken Sie auf "Neu".
3. Öffnen Sie die Suche, um den Namen des Rechnungsregisters auswählen, das Sie verwenden möchten.
4. Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.
5. Klicken Sie auf "Positionen", um das Register zu öffnen und Ausgabenpositionen einzugeben.
6. Wählen Sie in der Suche einen Händler aus. Beispielsweise klicken Sie auf Händler 1001.
7. Geben Sie im Feld "Rechnung" die Rechnungsnummer ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Geben Sie im Feld "Kredit" eine Zahl ein.
10. Klicken Sie im Feld "Bestellung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Wählen Sie die Bestellung aus, die Sie zuvor erstellt haben.
12. Klicken Sie im Feld "Genehmigt von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Heben Sie eine genehmigende Person hervor und klicken Sie auf "Auswählen", um die genehmigende Person auszuwählen.
14. Klicken Sie auf "Buchen".
15. Schließt das Formular.
16. Schließt das Formular.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Öffnen einer Rechnung aus dem Pool und Abgleichen mit einer Bestellung, um den Rechnungsprozess abzuschließen
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungspool".
2. Klicken Sie auf "Bestellung", um eine Kreditorenrechnung aus der Rechnung im Pool zu erstellen.
3. Wählen Sie die Rechnung aus, die Sie prüfen möchten.
4. Klicken Sie auf "Abgleichstatus", um den Abgleich abzuschließen.
5. Klicken Sie im Aktivitätsbereich auf "Optionen".
6. Klicken Sie auf "Ansicht ändern".
7. Klicken Sie auf "Rasteransicht".
8. Klicken Sie auf "Buchen".
9. Schließt das Formular.
10. Wechseln Sie zu "Kreditoren" > "Kreditoren" > "Kreditoren".
11. Wählen Sie den Händler aus, der auf der Bestellung war. Wählen Sie z. B. Händler 1001 aus.
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Klicken Sie im Aktivitätsbereich auf "Händler".
14. Klicken Sie auf "Transaktionen".
15. Wählen Sie die Rechnung aus, die Sie erstellt haben.
    * Die Rechnungsbuchabgrenzung wurde storniert und auf das entsprechende Ausgabenkonto gebucht.  


