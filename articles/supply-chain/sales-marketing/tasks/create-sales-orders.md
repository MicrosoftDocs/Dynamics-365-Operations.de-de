---
title: Aufträge erstellen
description: Diese Prozedur zeigt Ihnen, wie ein Auftrag erstellt wird.
author: Henrikan
ms.date: 04/06/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462f47ab5d85665ed8132e5bfb6dd945c537c1ef
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551723"
---
# <a name="create-sales-orders"></a>Aufträge erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt Ihnen, wie ein Auftrag erstellt wird. Sie können diese Prozedur im Demodatunternehmen USMF verwenden. Aufträge werden normalerweise von einem Auftragsprozessor erstellt. 

## <a name="enter-sales-order-header-details"></a>Auftragskopfdetails eingeben
1. Wechseln Sie zu **Navigationsbereich > Module > Vertrieb und Marketing > Aufträge > Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Debitorenkonto** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
4. Suchen Sie in der Liste den Debitorendatensatz und wählen Sie ihn aus.
    - Wählen Sie für dieses Beispiel Kundennummer US-004 aus.  
5. Wählen Sie **OK**.

## <a name="enter-sales-order-line-details"></a>Auftragspositionsdetails eingeben
    
Die Produkte, die von Ihrer Organisation verkauft werden, sind möglicherweise in verschiedenen Varianten nach Dimensionen, wie Konfiguration, Farbe, Größe und Stil, erhältlich. Zudem können Produkte so eingerichtet werden, dass sie Lagerdimensionen, wie Standort, Lagerort und Palette sowie Rückverfolgungsangaben, wie Charge und Seriennummern, verwenden. Wenn diese Dimensionen zugeordnet werden, müssen Sie die Werte für diese Dimensionen in der Auftragsposition auswählen. Um die Effizienz bei der Auftragserfassung zu verbessern, sollten Sie die jeweiligen Dimensionsfelder dem Auftragsraster hinzufügen.
    
1. Unter dem Abschnitt **Auftragspositionen** wählen Sie die **Auftragspositionszeile** aus.
2. Wählen Sie **Dimensionen** aus.
    
    Wählen Sie für dieses Beispiel die Farbe, die Standort- und Lagerortdimensionen aus. Die hier ausgewählten Dimensionen werden im Auftragsraster angezeigt. Wenn Ihre Auswahlen weiter bestehen sollen, legen Sie die Option **Einstellungen speichern** auf „Ja“ fest.
    
3. Wählen Sie **OK**.
4. Wählen Sie im Feld **Artikelnummer** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
5. Wählen Sie in diesem Beispiel die Artikelnummer T0004 aus.
    - Wenn der Artikel Teil einer Verkaufskategorie ist, wird der Artikelname automatisch im Feld "Verkaufskategorie" angezeigt.  
    - Wenn Produktdimensionsfelder bereits einen Wert enthalten, liegt dies daran, dass der Wert aus dem Produktdatensatz kopiert wurde, in dem dieser als Standardproduktdimension definiert ist. Sie können den Standardwert jederzeit ändern.   
6. Wählen Sie im Feld **Farbe** die Dropdown-Schaltfläche aus, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Geben Sie im Feld **Menge** eine Zahl ein.
    - Wenn der Artikel in anderen Einheiten verkauft wird, als er eingekauft, hergestellt und gelagert wird, und eine Menge in der Verkaufseinheit für den Produktdatensatz festgelegt wird, wird dieser Wert dann im Feld **Einheit** angezeigt. Sie können den Wert jederzeit ändern.   
    - Wenn das Feld **Standort** bereits einen Wert enthält, wurde der Wert vom Auftragskopf oder den Auftragseinstellungen kopiert, die dem Produkt zugeordnet sind. Sie können den Wert jederzeit ändern. Wenn das Feld leer ist, wählen Sie einen Wert aus.   
    - Wenn das Feld **Einzelpreis** bereits einen Wert enthält, wurde der Wert von einer gültigen Handelsvereinbarung oder vom Produktdatensatz kopiert. (Der Einzelpreis kann auch von einem Kaufvertrag stammen, aber der Prozess zum Erstellen von Aufträgen aus Kaufverträgen unterscheidet sich von dem hier angezeigten.) Wenn das Feld leer ist, geben Sie einen Wert ein.   
    - Das Feld **Rabatt** enthält einen Rabattbetrag pro Produkteinheit. Um den gesamten Positionsrabattbetrag zu berechnen, wird der Rabattwert nach Positionsmenge multipliziert. Wenn das Feld **Rabatt** bereits einen Wert enthält, wurde der Wert von einer gültigen Handelsvereinbarung kopiert. Wenn das Feld leer ist und Sie dem Debitor einen Positionsrabatt gewähren wollen, geben Sie einen Wert ein.  
    - Das Feld **Rabatt in Prozent** enthält einen Prozentwert, um den der gesamte Positionsbruttobetrag verringert werden soll.  Wenn das Feld **Rabatt in Prozent** bereits einen Wert enthält, wurde er von einer gültigen Handelsvereinbarung kopiert. Wenn das Feld leer ist und Sie dem Debitor einen Positionsrabatt gewähren wollen, geben Sie einen Wert ein. 
    - Das Feld **Nettobetrag** enthält einen Wert, der auf Grundlage der Menge und dem Einzelpreis der Position berechnet wird, um Rabatte angepasst.  Sie können den berechneten Wert mit einem anderen überschreiben.  

## <a name="review-the-order-totals"></a>Die Auftragssummen prüfen
1. Wählen Sie im **Aktivitätsbereich** die Option **Auftrag** aus.
2. Wählen Sie **Summen** aus.
    
    Die Seite **Summen** zeigt Details zum gesamten Auftrag an. Dazu zählt der Zwischensummenbetrag, der eine Summe aller Positionsnettobeträge ist, angepasst um spätere Positionsrabatte, den Gesamtrechnungsbetrag, der ein um spätere Rabatte auf Auftragsebene angepasster Zwischensummenbetrag ist, Belastungen und Mehrwertsteuer, die Debitorenkreditlimitsituation, usw. Der Rechnungsbetrag ist der Betrag, der auf dem Rechnungsdokument des Debitors angezeigt wird.  
    
3. Wählen Sie **OK** aus.

## <a name="sales-order-creation-performance-enhancement"></a>Verbesserte Leistung bei der Erstellung von Aufträgen
Die neue Funktion, die mit Version 10.0.26 der Anwendung eingeführt wird, reduziert die zusätzliche Datensatzerstellung für die Tabellen **SourceDocumentHeader** und **SourceDocumentLine**. Da diese Datensätze nicht erstellt werden, werden die Leistung verbessert und die Speichergröße reduziert. Diese zugrunde liegenden Quelldokumentframework-Tabellen werden derzeit nicht für Aufträge im Produkt verwendet, und es ist auch nicht geplant, sie zu verwenden. Die Aktivierung dieser Funktion wird als sichere Änderung für eine verbesserte Leistung angesehen. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
