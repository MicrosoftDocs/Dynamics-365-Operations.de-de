--- 
title: Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben
description: "Diese Aufgabenanleitung zeigt Ihnen an, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7cf810f1d8eabb9989fdd858585afcdf2e9574b
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung zeigt Ihnen an, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.


## <a name="create-and-post-and-invoice"></a>Erstellen und buchen und fakturieren
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsregister".
2. Klicken Sie auf "Neu".
3. Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf "Positionen", um das Register zu öffnen und Ausgabenpositionen einzugeben.
6. Wählen Sie einen Kreditor aus. Geben Sie beispielsweise US-104 ein oder wählen Sie es aus.
7. Geben Sie im Feld "Rechnung" einen Wert ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Geben Sie im Feld "Kredit" eine Zahl ein.
10. Klicken Sie im Feld "Genehmigt von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Heben Sie eine genehmigende Person hervor und klicken Sie auf "Auswählen", um die genehmigende Person auszuwählen.
12. Klicken Sie auf "Buchen".
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.

## <a name="approve-an-invoice"></a>Genehmigen einer Rechnung
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsgenehmigung".
2. Klicken Sie auf "Neu".
3. Wählen Sie den Namen der Rechnungsgenehmigungserfassung aus, den Sie benutzen möchten.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf Positionen, um eine Seite anzuzeigen, auf der Sie die Rechnungen auswählen können, die Sie genehmigen möchten.
6. Wählen Sie "Belege suchen" aus, um alle Rechnungen anzuzeigen, die zur Genehmigung bereit sind.
7. Markieren Sie die Rechnung, die Sie erstellt haben.
8. Klicken Sie auf Auswählen.
    * Die Belege, die Sie oben ausgewählt haben, werden auf diese Liste verschoben, nachdem Sie sie auswählen.  
9. Klicken Sie auf "OK".
10. Klicken Sie im auf das Kontonummernfeld, um ein Ausgabenkonto der Rechnung hinzuzufügen.
11. Geben Sie eine Kontonummer ein und bewegen Sie die Tabulatortaste vom Feld weg. Geben Sie beispielsweise "600120" ein.
12. Klicken Sie auf "Buchen".
13. Klicken Sie auf "Beleg", um die Einträge anzuzeigen, die gebucht wurden.
    * Das Konto "Rechnung mit ausstehender Genehmigung" wird zurückgesetzt und durch das tatsächliche Ausgabenkonto ersetzt.  


