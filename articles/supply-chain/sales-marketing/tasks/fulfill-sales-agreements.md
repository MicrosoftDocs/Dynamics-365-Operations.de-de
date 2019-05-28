---
title: Kaufverträge erfüllen
description: Dieses Verfahren zeigt Ihnen, wie einen Kaufvertrag über die Zuordnung von Aufträgen erfüllt wird.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f03f05b85b8d242db1c85d0e84667949e241f1f7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563947"
---
# <a name="fulfill-sales-agreements"></a>Kaufverträge erfüllen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen, wie einen Kaufvertrag über die Zuordnung von Aufträgen erfüllt wird. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Bevor Sie mit diesem Leitfaden starten, vergewissern Sie sich, einen gültigen Kaufvertrag vom Typ "Produktwertszusage " vorhanden ist. Alternativ können Sie den Leitfaden "Kaufvertrag erstellen" ausführen.  




## <a name="release-a-sales-order-from-the-agreement"></a>Genehmigen einer Bestellung über den Kaufvertrags
1. Wechseln Sie zu "Vertrieb und Marketing" > "Kaufverträge" > "Kaufverträge".
2. Öffnen Sie in der Liste den Kaufvertrag, für den Sie die Bestellung genehmigen möchten.
3. Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".
4. Klicken Sie auf "Kaufvertrag genehmigen".
    * Da der Text oben auf der Seite "Freigabeauftrag erstellen" zeigt die Details, die für die Auftragspositionen benötigt werden. Diese weiche abhängig von, ob der Vertrag mengen- oder wertbasiert ist ab.  
    * Der Vertrag in diesem Leitfaden hat den Typ "Produktwertszusage". Daher ist der Abschnitt "Positionen" dieser Seite leer. Wenn die Zusage auf der Menge basiert, werden die Positionsinformationen aus dem Vertrag kopiert.  
5. Klicken Sie auf "Erstellen".
    * Die Nachricht informiert Sie darüber, dass eine Bestellung erstellt wurde. Da der Auftrag keine Positionen enthält, müssen Sie Auftragspositionsdetails hinzufügen, um den Freigabeprozess abzuschließen.   
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.
8. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
9. Wählen Sie in der Liste den Auftrag, der als Ergebnis der Auftragsgenehmigung in der vorherigen Aufgabe erstellt wurde.
10. Klicken Sie auf "Position hinzufügen".
11. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
12. Wählen Sie im Feld "Artikelnummer" den Artikel aus, der auf dem zugeordneten Kaufvertrag angegeben wird.
13. Geben Sie im Feld "Menge" eine Zahl ein.
    * Stellen Sie sicher, dass Sie eine Menge eingeben, die den Nettobetrag unter den Wert des zugeordneten Kaufvertrags bringt lässt.  
    * Beachten Sie, dass, da der Auftrag mit dem Vertrag verknüpft ist, der verhandelte Rabattprozentsatz auf die Auftragsposition angewendet wird.  
14. Klicken Sie auf "Position aktualisieren".
15. Klicken Sie auf "Zugeordnet".
    * Die Seite "Zugeordneter Vertrag" zeigt die Kennung und die Vertragsbedingungen an, über die die Position freigegeben wird.  
16. Schließen Sie die Seite.
17. Klicken Sie im Aktivitätsbereich auf "Allgemein".
18. Klicken Sie auf "Zugeordneter Kaufvertrag".
19. Erweitern Sie den Abschnitt "Positionsdetails".
20. Klicken Sie auf die Registerkarte "Erfüllung".
    * Die Erfüllungsregisterkarte zeit eine Zusammenfassung aller Auftragspositionen, ihren Erfüllungsstatus sowie der Betrag oder die Menge die noch nicht freigegeben wurde an, die dieser Zusage zugeordnet sind.   
21. Schließen Sie die Seite.
22. Schließen Sie die Seite.
23. Schließen Sie die Seite.

## <a name="apply-sales-agreement-in-the-order-process"></a>Anwenden des Kaufvertrags im Bestellungsprozess
1. Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie in der Liste den Debitor aus, der im Kaufvertrag angegeben wird.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Erweitern Sie den Abschnitt "Allgemein".
7. Klicken Sie im Feld "Kaufvertragskennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Klicken Sie auf "Ja".
10. Klicken Sie auf "OK".
11. Markieren Sie in der Liste die ausgewählte Zeile.
12. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Wählen Sie im Feld "Artikelnummer" den Artikel aus, der auf dem zugeordneten Kaufvertrag angegeben wird.
14. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
15. Klicken Sie auf Speichern.
16. Klicken Sie im Aktivitätsbereich auf "Entnehmen und verpacken".
17. Klicken Sie auf "Lieferschein buchen".
18. Erweitern Sie den Abschnitt "Parameter".
19. Wählen Sie "Ja" im Feld "Buchung" aus.
20. Klicken Sie auf "OK".
21. Klicken Sie auf "OK".
22. Klicken Sie im Aktivitätsbereich auf "Allgemein".
23. Klicken Sie auf "Zugeordneter Kaufvertrag".
24. Klicken Sie auf die Registerkarte "Erfüllung".

