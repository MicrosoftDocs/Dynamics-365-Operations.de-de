--- 
title: "Bestand an einem Lagerort zählen"
description: "Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerinventurerfassung, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>Bestand an einem Lagerort zählen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch die einzelnen Schritte der Erstellung und des Buchens einer Lagerinventurerfassung, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen. Die Prozedur ist auf die Funktion "Grundlegendes Warehousing", die sich im Inventurverwaltungsmodul befindet, anwendbar. Jedoch nicht auf die Warehousing-Funktion, die im Lagerortverwaltungsmodul verfügbar ist. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie eigene Daten verwenden, sollten Sie sicherstellen, dass Sie Produkte und Lagerplatzeinstellung eingerichtet haben und dass Sie eine Lagererfassung für Inventurerfassungen erstellt haben. Die Lagerinventur wird in der Regel von einem Lagerortmitarbeiter ausgeführt.


## <a name="create-an-inventory-counting-journal"></a>Lagerinventurerfassung erstellen
1. Wechseln Sie zu "Lagerverwaltung" Wechseln Sie zu "Lagerverwaltung" > "Erfassungseinträge" > "Artikelinventur" > "Artikel"
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf die Lagerinventurerfassung, die Sie verwenden möchten.
    * Einige andere Felder werden basierend auf den Einstellungen der Lagerinventurerfassung ausgefüllt, die Sie auswählen.  
5. Klicken Sie im Feld "Arbeitskraft" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Wählen Sie in der Liste die Arbeitskraft aus, die Sie verwenden möchten.
7. Klicken Sie auf Auswählen.
8. Klicken Sie auf "OK".

## <a name="create-journal-lines"></a>Erfassungspositionen erstellen
1. Klicken Sie auf "Neu".
2. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie "A0001" ein.  
4. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Standort "2" ein.  
6. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Lagerort "24" ein.  
8. Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wenn Sie das Demodatenunternehmen USMF verwenden, geben Sie den Lagerplatz "BULK-001" ein.  
10. Geben Sie im Feld "Gezählt" eine Zahl ein.
    * Wenn Sie eine Anzahl eingeben, die von der Zahl im Feld "Am Lager" angezeigt wird, wird das Mengenfeld aktualisiert, um die Abweichung anzuzeigen.  
11. Klicken Sie auf "Speichern".

## <a name="post-the-inventory-counting-journal"></a>Lagerinventurerfassung buchen
1. Klicken Sie auf "Buchen".
    * Wenn Sie eine Lagerinventurerfassung buchen und der gezählte Betrag unterscheidet sich vom Betrag, der im Feld "Am Lager" gemeldet ist, wird ein Lagerzugang oder Abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.  
2. Klicken Sie auf "OK".

## <a name="view-inventory-transactions"></a>Lagerbuchungen anzeigen
1. Klicken Sie auf Lager.
2. Klicken Sie auf "Transaktionen".
    * Hier können Sie alle zugehörigen Transaktionen finden, die erstellt werden, wenn Sie die Lagerinventurerfassung buchen.   


