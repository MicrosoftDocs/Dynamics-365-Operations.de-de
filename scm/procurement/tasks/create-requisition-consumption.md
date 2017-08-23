--- 
title: "Anforderung für Verbrauch erstellen"
description: Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb4cd47104e2df1c973e5e508c1da02617b9a1d
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-for-consumption"></a>Anforderung für Verbrauch erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Sie einen Kreditbrief importieren. Sie zeigen die unterschiedliche Arten, um nach Produkte im Beschaffungskatalog zu suchen und zu erfahren, öie ein Produkt hinzufügt, das nicht im Katalog ist. Überprüfen Sie zunächst, müssen Sie eine Einkaufsrichtlinieneinstellung mit der Verbrauch mit der Standardtyp der Anforderung offen. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Die Prozedur kann in einem Benutzerprofil nur ausgeführt werden, das als Arbeitskraft eingerichtet ist.  Diese Aufgaben werden normalerweise von einem Lagerortmitarbeiter ausgeführt. Der Mitarbeiter setzen Sicherheitsrolle ermöglicht Ihnen, die Aufgaben besitzen ein, oder, wenn Sie USMF verwenden, können Sie als Alicia anmelden.


## <a name="create-a-new-requisition"></a>Neue Reiseanforderung erstellen
1. Wechseln Sie zu "Beschaffung" >"Bestellanforderungen" > "Von mir vorbereitete Bestellanforderungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld Name einen Namen für die Anforderung ein.
4. Geben Sie im Feld "Angefordertes Datum" ein Datum ein.
    * Hier werden das angeforderte Datum, der Abschlussstichtag und die Geschäftsbegründung für die Bestellanforderungsposition angezeigt. Sie können auch auf Positionsebene geändert werden. Das angeforderte Datum ist das angeforderte Lieferdatum.  
5. Geben Sie ein Datum in das Feld "Datum" ein.
    * Der Abschlussstichtag wird zum Erfassen des Buchhaltungseintrags im Hauptbuch und zum Überprüfen der verfügbaren Budgetmittel verwendet.  
6. Klicken Sie auf "OK".
7. Klicken Sie im Feld Grund auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die ausgewählte geschäftliche Begründung wird standardmäßig für Bestellanforderungspositionen angezeigt, kann aber auf Positionsebene geändert werden.    
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Wählen Sie den Grund aus.
10. Wählen Sie im Detailgebiet geben Sie eine beschreibendere Begründung für die Anforderung ein

## <a name="add-a-line-to-the-requisition"></a>Fügt dem Arbeitszeitnachweis eine neue Zeile hinzu.
1. Klicken Sie auf "Position hinzufügen".
    * Es gibt zwei Möglichkeiten zum Hinzufügen von Positionen der Bestellanforderung. Wenn Sie die Produktnummer bereits kennen oder Sie wissen, dass Sie ein Produkt anfordern, das nicht im Produktkatalog ist, können Sie die Position direkt mit "Position hinzufügen" hinzufügen. Die andere Methode ist zu verwenden "Produkte hinzufügen" wo das Suchen und Filtern verwenden können, um Artikel im Produktkatalog zu suchen.    
2. Klicken Sie auf der Zeile, die Sie soeben erstellt haben.
    * Die anfordernde Person ist die Arbeitskraft, die die Anforderung angefordert hat.   
    * Standardmäßig ist die Person, die die Anforderung vorbereitet, die Arbeitskraft, die sie angefordert hat. Sie müssen die Erlaubnis werden, eine Bestellanforderungsposition im Auftrag einer anderen Arbeitskraft vorbereitet. Wenn Sie solche Berechtigungen dann haben, zeigen andere Arbeitskräfte in dieser Suche.  
3. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Die Artikel, die verfügbar sind, damit Sie auswählen, werden durch die Kategoriezugriffsrichtlinie und den Beschaffungskatalog für die kaufende juristische Person beschränkt.   
4. Geben Sie im Feld "Menge" eine Zahl ein.

## <a name="add-more-products-to-the-requisition"></a>Produkte zu einer Bestellanforderung hinzufügen
1. Klicken Sie auf Produkte hinzufügen.
    * Dies ist die Option, in der Sie für Produkte im Produktkatalog suchen können.    
2. Wählen Sie im Suchenbeschaffungskategorieknotengebiet geben Sie den ersten Teils des Namens nach der Kategorie, der Sie feststellen, und klicken Sie dann auf die EINGABETASTE.
    * Geben Sie beispielsweise comput ein.  
3. Verwenden Sie die InvokeDefaultButton-Verknüpfung.
4. Verwenden Sie den Filter, um die Liste der Produkte in der ausgewählten Kategorie zu filtern.
5. Wählen Sie hier die Produkte aus, die Sie der Bestellanforderung hinzufügen möchten.
6. Zu Positionen hinzufügen
7. Geben Sie im Feld "Menge" eine Zahl ein.
8. Wählen Sie im Suchenbeschaffungskategorieknotengebiet geben Sie den ersten Teils des Namens nach der Kategorie, der Sie feststellen, und klicken Sie dann auf die EINGABETASTE.
    * Beispielsweise Typ hoch (Textmarker).  
9. Verwenden Sie die InvokeDefaultButton-Verknüpfung.
10. Klicken fügt nicht aufgeführtes Produkt Positionen hinzu, um ein Produkt hinzuzufügen, die nicht im Beschaffungskatalog aufgeführt ist.
11. Geben Sie im Feld "Produktname" einen Wert ein.
12. Geben Sie im Feld "Einheiten" einen Wert ein.
13. Klicken Sie auf "OK".
14. Geben Sie im Feld Artikelbeschreibung eine Beschreibung des Produkts ein.
15. Geben Sie im Feld "Menge" eine Zahl ein.
16. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
    * Wenn Sie wissen, kann der der Preis für einen bestimmten Kreditor (diesen, Sie im Feld Kreditorenkonto auswählen), dann dieser Preis eingegeben werden   
17. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Kreditoren, die in diesem Feld verfügbar sind, hängt von den Einkaufsrichtlinien und vom Status ab, den der Kreditor für die aktuelle Beschaffungskategorie hat. Als Alternative zu einen Kreditor hier auswählen, können Sie auf die Vorschlagungskreditorenschaltfläche klicken.    
18. Wählen Sie in der Liste die Arbeitskraft aus, die Sie verwenden möchten.
19. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Dies ist eine Referenznummer für das Produkt, das vom Kreditor bekannt ist. Beispielsweise kann diese die Artikelnummer des Produkts im eigenen Katalog des Kreditors sein.  
20. Klicken Sie auf "OK".

## <a name="distribute-amounts"></a>Beträge verteilen
1. Klicken Sie auf "Finanzdaten".
2. Verteilungsbeträge anzeigen
    * Dieser Prozess zeigt Ihnen an, wie die Kosten für die erste Position zwischen 2 Konten verteilt. Dies kann auch später nachholen, wenn die Anforderung im geprüft.  
3. Klicken Sie zum Erstellen einer neuen Verteilungsposition auf Teilen.
4. Wählen Sie im Feld Sachkonto wählen Sie die erste Kostenstelle, die von den Kosten teilnehmen soll.
5. Löschen Sie die ausgewählte Verteilungsposition.
6. Geben Sie im Feld "Konto für Sachkontobuchungen" die andere Kostenstelle an.
7. Gleichmäßig verteilen
8. Schließen Sie die Seite.

## <a name="view-line-details"></a>Artikel-Details anzeigen
1. Schalten Sie die Erweiterung des Abschnitts "Positionsdetails" ein/aus.

## <a name="submit-the-requisition"></a>Materialanforderung übermitteln
1. Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.
2. Klicken Sie auf Absenden.
3. Schließen Sie die Seite.
4. Im Kommentarfeld geben Sie einen Hinweis für den Genehmiger der Anforderung ein.
5. Klicken Sie auf Absenden.
6. Schließen Sie die Seite.
7. Aktualisieren Sie die Seite.

