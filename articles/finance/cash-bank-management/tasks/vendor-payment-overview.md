---
title: Übersicht Kreditorenzahlung
description: Dieses Aufgabenhandbuch läuft Sie nach den verschiedenen Methoden durch, die verwendet werden, um die Kreditorenzahlungen, umfasst, wie ein Zahlungsvorschlag oder manuell erfolgt eine einmalige Zahlung zu erstellen verwendet.
author: kweekley
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4402be4be52f71bf346a1f85155aad4b9890b3bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827289"
---
# <a name="vendor-payment-overview"></a>Übersicht Kreditorenzahlung

[!include [banner](../../includes/banner.md)]

Dieses Aufgabenhandbuch läuft Sie nach den verschiedenen Methoden durch, die verwendet werden, um die Kreditorenzahlungen, umfasst, wie ein Zahlungsvorschlag oder manuell erfolgt eine einmalige Zahlung zu erstellen verwendet. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Kreditorenkonten > Zahlungen > Zahlungserfassung**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie die Zahlungserfassung aus, in der die Kreditorenzahlungen zu speichern sind. 
4. Wählen Sie die Erfassung aus, oder geben Sie sie manuell ein.
5. Klicken Sie auf **Positionen**.
6. Klicken im **Aktivitätsbereich** auf **Zahlungsvorschlag**.
7. Klicken Sie auf **Zahlungsvorschlag erstellen**. Der Zahlungsvorschlag ist eine Abfrage, die verwendet wird, um Rechnungen für die Zahlung auszuwählen. Sie können die Liste der Rechnungen bearbeiten, die gezahlt werden sollen, bevor Sie die Kreditorenzahlungen erstellen oder generieren.
8. Wählen Sie Rechnungen für die Zahlung nach Fälligkeitsdatum, Skonto oder beides aus. 
9. Geben Sie das Datum für das Vergleichen zum Fälligkeitsdatum oder zum Skonto ein. 
10. Optional: Geben Sie ein Zahlungsdatum ein, das für alle Zahlungen verwendet wird. Das Datum, das hier eingegeben wird, wird das Zahlungsdatum für alle erstellten Zahlungen, unabhängig vom Fälligkeitsdatum oder Skontodatum.  
11. Optional: Geben Sie ein Mindestzahlungsdatum ein, die als das Zahlungsdatum verwendet werden soll. Das Mindestzahlungsdatum ist das früheste Datum, das beim Erstellen von Zahlungen verwendet wird. Wenn beispielsweise eine Rechnung ein Fälligkeitsdatum nach dem Mindestzahlungsdatum hat, wird das Fälligkeitsdatum zum Zahlungsdatum anstelle des Mindestzahlungsdatums, damit die Rechnung am letzten möglichen Datum geleistet wird.
12. Geben Sie zusätzliche Abfrageneinschränkungen unter **Einzuschließende Datensätze** ein, die einbezogen werden sollen. Der Filter wird häufig verwendet, um die Rechnungen einzuschränken, die für die Zahlung nach Kreditorengruppe oder Zahlungsmethode ausgewählt werden. Sie können einen Filter hinzufügen, um in diesem Zahlungslauf nur Lohnrechnungen per Scheck zu zahlen.
13. Geben Sie zusätzliche Abfrageneinschränkung oder Zahlungsstandards ein. Folgende zusätzliche Parameter können verwendet werden, um die Zahlungswährung zu definieren oder zentralisierte Zahlungen für diesen Zahlungslauf zu aktivieren.  
14. Klicken Sie auf **OK**. Nachdem sie auf **OK** geklickt haben, werden die Ergebnisse der Abfrage angezeigt. Wenn Sie keine Vorschau der Liste der für die Zahlung ausgewählten Rechnungen anzeigen möchten, können Sie zur Inforegister **Parameter** zurückkehren und die Einstellung **Zahlungen ohne Rechnungsvorschau erstellen** in „Ja“ ändern.  
15. Wählen Sie die Schaltfläche **Zahlungsüberblick anzeigen** aus, um die Zahlungen anzeigen, die für den Kreditor der ausgewählten Rechnung erstellt werden.
16. Wählen Sie **Zahlungsübersicht ausblenden**, um die Zahlungen auszublenden. 
17. Klicken Sie auf **Zahlungen erstellen**. Bevor **Zahlungen erstellen** auswählen, können Sie im Raster mit der rechten Maustaste klicken und die Liste der Rechnungen in Excel exportieren. Die Schaltfläche **Zahlungen erstellen** erstellt die Kreditorenzahlungen in der Zahlungserfassung.  
18. Scannen Sie Ihre Zahlungen und vergewissern Sie sich, dass die Zahlungsmethode für alle Zahlungen definiert ist. Wenn Sie die Zahlungen generieren, wie Drucken eines Schecks oder Erstellen einer elektronischen Zahlung, muss die Zahlungsmethode definiert werden. Die Zahlungsmethode wird auch das Bankkonto definieren, mit dem die Zahlung getätigt wird.  
19. Klicken Sie auf **Neu**, um eine Einmalzahlung zu erstellen. Eine einmalige Zahlung kann in eine Zahlungserfassung vor Buchung jederzeit hinzugefügt werden. Dies erfolgt, indem Sie manuell auf die Schaltfläche **Neu** klicken und Zahlungsinformationen manuell hinzufügen, anstelle den **Zahlungsvorschlag** zu nutzen.  
20. Wählen Sie den Kreditor aus, für den die Zahlung erfolgt.
21. Wenn eine Rechnung vorhanden ist, die gezahlt werden soll, wählen Sie **Buchungen ausgleichen**, um die Rechnung für Zahlung auszuwählen. Wenn es sich um eine Vorauszahlung handelt, ist dieser Schritt optional. Sie können die Zahlung erstellen, ohne eine Rechnung auszuwählen. 
22. Markieren Sie alle Rechnungen, die bezahlt werden. Wenn Sie **Buchungen ausgleichen** verwenden, um die Rechnungen für Zahlung auszuwählen, wird der Zahlungsbetrag automatisch berechnet auf der Grundlage, welche Rechnungen Sie für die Zahlung markieren und welche Betrag Sie in den **auszugleichenden Betrag** eingeben.
23. Klicken Sie auf **OK**.
24. Wenn Sie eine Zahlung löschen möchten, markieren Sie die Zeile.
25. Klicken Sie auf **Löschen**. Eine Zahlung löschen, löscht nur die Zahlung. Alle Rechnungen, die für die Zahlung markiert werden, sind weiterhin verfügbar, durch eine andere Zahlung bezahlt zu werden.
26. Klicken Sie auf **Ja**.
27. Wählen Sie **Zahlung generieren**, um die Schecks zu drucken oder die elektronische Zahlungsdatei erstellen aus.
28. Dient zum Auswählen des Typs für die zu erstellende Zahlung. Die Zahlungserfassung kann Zahlungen sowohl für Schecks als auch für elektronischen Zahlungen enthalten, Sie können aber nur jeweils einen Zahlungstyp generieren.
29. Wählen Sie das Bankkonto aus, von dem die Zahlungen generieren.
30. Klicken Sie auf **OK**. Zahlungen werden nur für Zahlungen generiert, die der **Zahlungsmethode** und des **Bankkontos** entsprechen, die Sie ausgewählt haben.
31. Wenn Sie **Schecks** generieren, wählen Sie **Dokument**, um das korrekte Druckziel für die Schecks sicherzustellen.
32. Klicken Sie auf **OK**.
33. Klicken Sie zum Generieren der Zahlungen auf **OK**.
34. Klicken Sie auf **Buchen**, wenn alle Zahlungen genehmigt und generiert werden. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]