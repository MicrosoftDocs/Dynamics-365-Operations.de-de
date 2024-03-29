---
title: Reihenfolge der Produktions-Einzelvorgänge für Prozessfertigung
description: Bei dieser Prozedur werden Farbenprodukte als Beispiel verwendet, um anzuzeigen, wie Bestellvorschläge gemäß der Priorität von Farbe und Verpackungsgröße nacheinander geordnet werden.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e54cfa60fa9efd511aef8c074484b9b1a738e8cb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572744"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Reihenfolge der Produktions-Einzelvorgänge für Prozessfertigung

[!include [banner](../../includes/banner.md)]

Bei dieser Prozedur werden Farbenprodukte als Beispiel verwendet, um anzuzeigen, wie Bestellvorschläge gemäß der Priorität von Farbe und Verpackungsgröße nacheinander geordnet werden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USPI. Diese Prozedur ist für den Produktionsplaner vorgesehen.


## <a name="run-master-planning-for-uspi"></a>Führen Sie den Produktprogrammplan für USPI aus
1. Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Ausführen" > "Produktprogrammplan".
2. Klicken Sie im Feld "Produktprogrammplan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie "MasterPlan" aus.  
4. Klicken Sie auf "OK".
    * Dadurch wird der Produktprogrammplan gestartet, einschließlich des Sequenzprozesses. Dieser Prozess kann einige Minuten in Anspruch nehmen.  

## <a name="view-planned-orders-for-the-paint-products"></a>Zeigen Sie Bestellvorschläge für die Farbenprodukte an
1. Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Bestellvorschläge".
2. Erweitern Sie die Infobox "Artikeldetails".
3. Erweitern Sie die Infobox "Zeitplandetails".
4. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie "MasterPlan" aus.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P300" zu filtern.
    * Heben Sie die Sperrung auf, um einen Bildlauf nach rechts durchzuführen, um das Auftragsdatum und das Lieferdatum anzuzeigen. Beachten Sie, dass diese Artikel als Auftragsdatum "Heute" haben und die Lieferdaten für die Bestellvorschläge folgen nicht aufeinander nach Priorität von Farbe und Paketgröße, wie im Produktname angezeigt. Sie können auf eine Artikelnummer zeigen, um den Produktname und die Priorität anzuzeigen.  

## <a name="sequence-planned-orders-for-paint"></a>Ordnen Sie Bestellvorschläge für Farbe der Reihe nach ein
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Sequenzierte Bestellvorschläge".
3. Erweitern Sie die Infobox "Artikeldetails".
4. Erweitern Sie die Infobox "Zeitplandetails".
    * Hinweis: Hier sehen Sie, dass das Startdatum/die Startuhrzeit für die Bestellvorschläge gemäß Farbe und Paketgröße innerhalb einer Periode für den Zeitraum von 28 Tagen. Diese Perioden werden durch eine Nummer im Feld "Kampagne" definiert. Das Formular für sequenzierte Bestellvorschläge fungiert als Standardformular für Bestellvorschläge und der Produktionsplaner kann hier die Bestellvorschläge umwandeln.  
5. Markieren Sie alle Zeilen.
6. Klicken Sie auf "Annehmen".
    * Dadurch werden die Bestellvorschläge mit der ausgewählten Sequenzaktion, entweder "Verschieben" oder "Vorziehen", aktualisiert.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Überprüfen Sie die Reihenfolge der Bestellvorschläge
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Produktprogrammplan" > "Produktprogrammplan" > "Bestellvorschläge".
3. Erweitern Sie die Infobox "Artikeldetails".
4. Erweitern Sie die Infobox "Zeitplandetails".
5. Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie "MasterPlan" aus.  
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Verwenden Sie den Schnellfilter, um im Feld "Artikelnummer" nach dem Wert "P300" zu filtern.
    * Beachten Sie, dass die Aufträge nun entsprechend der Priorität von Farbe und Größe aufeinander folgen und die Bestellvorschläge beginnen mit dem frühesten Auftragsdatum und Lieferdatum. Überprüfen Sie die Spalte "Auftragsdatum" oder "Startdatum" in der Infobox "Planungsdetails".  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]