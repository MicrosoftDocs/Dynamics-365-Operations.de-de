---
title: Bestand an einem Lagerort zählen
description: In diesem Thema wird der Prozess der Erstellung und Buchung einer Lagerinventurerfassung beschrieben, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen.
author: MarkusFogelberg
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24b8bc2daff2d7df6279c76f4d9a0e83244c7988
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834048"
---
# <a name="count-inventory-in-a-warehouse"></a>Bestand an einem Lagerort zählen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird der Prozess der Erstellung und Buchung einer Lagerinventurerfassung beschrieben, um einen bestimmten Artikel in einem Lagerplatz am Lagerort zu zählen. Die Prozedur ist auf die Funktion Grundlegendes Warehousing ausgelegt, die sich im Inventurverwaltungsmodul befindet, jedoch nicht auf die Warehousing-Funktion, die im Lagerortverwaltungsmodul verfügbar ist. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden. Wenn Sie eigene Daten verwenden, sollten Sie sicherstellen, dass Sie die Produkte und Lagerplatzeinstellung eingerichtet haben und dass Sie eine Lagererfassung für Inventurerfassungen erstellt haben. Die Lagerinventur wird in der Regel von einem Lagerortmitarbeiter ausgeführt.


## <a name="create-an-inventory-counting-journal"></a>Lagerinventurerfassung erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Lagerverwaltung > Journaleinträge > Artikelinventur > Inventur**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Name** aus der Dropdownliste den Namen der Lagerinventurerfassung aus, die Sie verwenden möchten. Einige andere Felder werden basierend auf den Einstellungen der Lagerinventurerfassung ausgefüllt, die Sie auswählen.  
4. Klicken Sie im Feld **Arbeitskraft** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. **Wählen Sie** in der Liste die Arbeitskraft aus, die Sie verwenden möchten.
6. Wählen Sie **OK**.

## <a name="create-journal-lines"></a>Erfassungspositionen erstellen
1. Wählen Sie **Neu** aus.
2. Wählen Sie im Feld **Artikelnummer** den gewünschten Datensatz aus der Dropdown-Liste aus. Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie **A0001** aus.  
3. Wählen Sie im Feld **Standort** den gewünschten Datensatz aus der Dropdown-Liste aus. Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Standort **2** aus.
4. Wählen Sie im Feld **Lagerort** den gewünschten Datensatz aus der Dropdown-Liste aus. Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Lagerort **24** aus.  
5. Wählen Sie im Feld **Standort** den gewünschten Datensatz aus der Dropdown-Liste aus. Wenn Sie das Demodatenunternehmen USMF verwenden, wählen Sie den Standort **BULK-001** aus.  
6. Geben Sie im Feld "Gezählt" eine Zahl ein. Wenn Sie eine Anzahl eingeben, die von der Zahl im Feld **An Lager** abweicht, wird das Feld **Menge** aktualisiert, um die Abweichung anzuzeigen.  
7. Wählen Sie **Speichern**.

## <a name="post-the-inventory-counting-journal"></a>Lagerinventurerfassung buchen
1. Wählen Sie **Buchen** aus. Wenn Sie eine Lagerinventurerfassung buchen und die gezählte Menge sich von der Menge unterscheidet, die im Feld **An Lager** gemeldet ist, wird ein Lagerzugang oder -abgang gebucht, der Lagerbestand und der Lagerwert werden geändert, und Sachkontobuchungen werden generiert.
2. Wählen Sie **OK**.

## <a name="view-inventory-transactions"></a>Lagerbuchungen anzeigen
1. Wählen Sie **Bestand** aus.
2. Wählen Sie **Buchungen** aus. Hier können Sie alle zugehörigen Transaktionen finden, die erstellt werden, wenn Sie die Lagerinventurerfassung buchen.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]