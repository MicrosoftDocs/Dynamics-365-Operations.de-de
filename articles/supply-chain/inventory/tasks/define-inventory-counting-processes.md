---
title: Lagerinventurprozesse definieren
description: In diesem Thema wird die Konfiguration von grundlegenden Lagerinventurprozessen erklärt, indem eine Inventurgruppe und eine Inventurerfassung erstellt wird.
author: MarkusFogelberg
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 535fa6cfcf1f966b02ee7b391bb41dcbc2c2ac1fc85bcd09e3811fc027621cc4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755394"
---
# <a name="define-inventory-counting-processes"></a>Lagerinventurprozesse definieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird die Konfiguration von grundlegenden Lagerinventurprozessen erklärt, indem eine Inventurgruppe und eine Inventurerfassung erstellt wird. Sie zeigt Ihnen auch, wie Inventurrichtlinien auf Lagerort- und Artikelebene aktiviert werden. Diese Aufgaben werden normalerweise von einem Vorgesetzten am Lagerort ausgeführt. Es ist eine Voraussetzung, einige vorhandene freigegebene Produkte und Lagerorte zu haben. Wenn Sie ein Demodatunternehmen verwenden, können Sie diese Prozedur im USMF-Unternehmen mit jedem gelagerten Artikel ausführen.


## <a name="create-a-counting-group"></a>Eine Inventurgruppe erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Inventurgruppen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Inventurgruppe** der neuen Zeile einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Inventurcode** eine Option aus.

    - **Manuell** – Schließt immer dann Positionen ein, wenn Sie den Einzelvorgang ausführen. Sie bestimmen das Inventurintervall für die Inventurgruppe also selbst.  
    - **Periode** – Umfasst Positionen für die Periode in der Inventurerfassung, wenn das Periodenintervall überschritten wird.  
    - **Null auf Lager** – Erreicht der verfügbare Lagerbestand 0, werden Positionen in der Inventurerfassung erzeugt, wenn Sie den Einzelvorgang ausführen. Wenn der verfügbare Lagerbestand nach einer Inventur Null erreicht, werden bis zum Start der nächsten Inventur keine Positionen generiert.  
    - **Minimum** – Fügt Positionen in die Inventurerfassung ein, wenn der verfügbare Lagerbestand gleich dem Minimum oder kleiner als das angegebene Minimum ist.  
    - Optional: Wenn Sie im Feld **Inventurcode** den Wert **Periode** angegeben haben, müssen Sie im Feld **Inventurperiode** das Intervall für die Periode eingeben. Die Einheit für Intervalle ist Tage.  
    - Wenn Sie den Einzelvorgang zum Erstellen neuer Positionen in der Inventurerfassung ausführen, werden neue Positionen in dem Intervall erstellt, das in diesem Feld angegeben ist, unabhängig davon, wie oft Sie denselben Einzelvorgang ausführen. Wenn beispielsweise die **Inventurperiode** auf 7 festgelegt wird und Erfassungspositionen zuletzt für eine Anzahl am 1. Januar generiert wurden, wenn ein anderer Einzelvorgang am 5. Januar gestartet wird, sind noch keine sieben Tage verstrichen und daher werden keine Positionen in der Erfassung für dieses Periodenintervall generiert. Wenn Sie den Einzelvorgang erneut am 8. Januar beginnen, werden für die Periode in der Inventurerfassung Positionen erstellt, da 7 Tage vergangen sind.  

6. Wählen Sie **Speichern**.

## <a name="create-a-counting-journal-name"></a>Einen Inventurerfassungsname erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Journale > Lager**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Erfassungstyp** die Option **Inventur** aus. Optional: Sie können eine andere Belegnummernkennung auswählen, wenn Sie einen bestimmten Nummernkreis für die Belegkennung haben möchten, wenn Sie Inventurerfassungen erstellen. Belegnummern werden auf der Seite **Nummernkreise** erstellt.  
6. Wählen Sie im Feld **Detailebene** eine Option aus.  

    - Das ist die Detailstufe, die angewendet wird, wenn die Erfassung gebucht wird.  
    - Optional: Sie können den Wert im Feld "Reservierung" ändern. Dies ist die Methode, die verwendet wird, um Artikel während der Inventur zu reservieren.   
    - **Manuell** – Die Artikel werden manuell im Formular „Reservierung“ reserviert.  
    - **Automatisch** – Die Auftragsmenge wird aus dem verfügbaren Lagerbestand für den Artikel reserviert.   
    - **Simultanplanungszeitraum** – Die Reservierung ist Teil des Produktprogrammplans der Transaktion.  

7. Wählen Sie **Speichern**.

## <a name="set-standard-counting-journal-name"></a>Standardmäßigen Inventurerfassungsnamen festlegen
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Parameter für Lager- und Lagerortverwaltung**.
2. Wählen Sie die Registerkarte **Erfassungen** aus.
3. Wählen Sie im Dropdownmenü des Feldes **Inventur** die Erfassung aus, die Sie zuvor erstellt haben. Diese Erfassung wird dann der Standarderfassungsname für Lagererfassungen vom Typ **Inventur** sein.  
4. Wählen Sie die Registerkarte **Allgemein** aus. Optional: Wählen Sie diese Option aus, um einen Artikel während des Inventurprozesses zu sperren, um Aktualisierungen für Lieferscheine, Kommissionierlisten oder Kommissionierlistenregistrierungen zu verhindern.  

## <a name="set-the-counting-policy-for-an-item"></a>Die Inventurrichtlinie für einen Artikel festlegen
1. Wechseln Sie im Navigationsbereich zu **Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
2. Wählen Sie in der Liste den Link für die Artikelnummer des Produkts aus, für das Sie Inventurrichtlinien festlegen möchten. Sie müssen einen Artikel auswählen, bei dem der Bestand nachverfolgt wird. Ein nicht auf Lager befindliches Produkt kann nicht gezählt werden. Wenn Sie USMF-Demodaten verwenden, können Sie Artikel A0001 auswählen.  
3. Wählen Sie **Bearbeiten** aus.
4. Schalten Sie die Erweiterung des Abschnitts **Lagerbestand verwalten** ein/aus.
5. Wählen Sie im Dropdownmenü des Feldes **Inventurgruppe** die Inventurgruppe aus, die Sie zuvor erstellt haben. Dieses Produkt wird jetzt einbezogen, wenn Lagerinventurerfassungspositionen mithilfe dieser Inventurgruppe erstellt werden.  
6. Wählen Sie **Speichern**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Die Inventurrichtlinie für einen Artikel an einem bestimmten Lagerort festlegen
1. Wählen Sie im Aktivitätsbereich **Lagerbestand verwalten** aus.
2. Wählen Sie **Lagerortartikel** aus.
3. Wählen Sie **Neu** aus.
4. Wählen Sie im Dropdownmenü des Feldes **Lagerort** den Lagerort aus, für den Sie bestimmte Inventurrichtlinien einrichten möchten.
5. Wählen Sie im Dropdownmenü des Feldes **Inventurgruppe** eine Inventurgruppe aus. Sie können eine bestimmte Inventurgruppe auswählen, die auf den Artikel am bestimmten Lagerort angewendet werden soll, den Sie ausgewählt haben. Wenn eine Inventur in diesem Lagerort ausgeführt wird, überschreibt diese Inventurrichtlinie die allgemeine Inventurrichtlinie für den Artikel.  
6. Wählen Sie **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]