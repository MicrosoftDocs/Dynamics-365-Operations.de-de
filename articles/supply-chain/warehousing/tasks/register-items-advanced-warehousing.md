---
title: Artikel für einen für erweitertes Warehousing aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren
description: Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterten Lagerungsvorgänge verwenden.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2550e32db8b0d769f62c13654aa1dc1d201388ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148327"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Artikel für einen für erweitertes Warehousing aktivierten Artikel mithilfe einer Wareneingangserfassung registrieren

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen an, wie Artikel mithilfe der Wareneingangserfassung erfasst werden, wenn Sie die erweiterten Lagerungsvorgänge verwenden. Dies wird in der Regel von einem Sachbearbeiter für Zugänge ausgeführt. 

Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Sie müssen Sie eine bestätigte Bestellung mit einer offenen Bestellposition haben, bevor Sie diesen Leitfaden starten. Der Artikel in der Position muss gelagert werden, und er darf keine Produktvarianten verwenden und keine Rückverfolgungsangaben haben. Der Artikel muss außerdem einer Lagerdimensionsgruppe zugeordnet werden, die für den Lagerortverwaltungsprozess aktiviert ist. Der Lagerort, der verwendet wird, muss für Lagerortverwaltungsprozesse aktiviert sein und der Lagerplatz, der für den Eingang verwendet wird, muss über Ladungsträger gesteuert werden. Wenn Sie USMF verwenden, können Sie Unternehmenskonto 1001, Lagerort 51 und Artikel M9200 verwenden, um die Bestellung zu erstellen. 

Notieren Sie die Nummer der Bestellung die Sie erstellen, und notieren Sie auch die Artikelnummer und den Standort für die Bestellposition.


## <a name="create-an-item-arrival-journal-header"></a>Erstellen einer Wareneingangserfassungs-Kopfzeile
1. Wechseln Sie zu "Wareneingang".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
    * Wenn Sie USMF verwenden, können Sie WHS eingeben. Wenn Sie andere Daten verwenden, muss die Erfassung, deren Namen Sie auswählen, die folgenden Eigenschaften haben: „Entnahmeort prüfen“ muss auf „Kein“ festgelegt werden, und „Quarantäneverwaltung“ muss auf „Nein“ festgelegt werden.  
4. Geben Sie im Feld "Zahl" einen Wert ein.
5. Geben Sie im Feld "Standort" einen Wert ein.
    * Wählen Sie den Standort auf, der für die Bestellposition verwendet wird. Dieses dient als Standardwert, der für alle Positionen der Erfassung gilt. Wenn Sie Lagerort 51 in USMF verwendeten, wählen Sie Standort 5. aus.  
6. Geben Sie im Feld "Lagerort" einen Wert ein.
    * Wählen Sie einen gültigen Lagerort für den Standort aus, die Sie ausgewählt haben. Dieses dient als Standardwert, der für alle Positionen der Erfassung gilt. Wenn Sie die Beispielswerte in USMF verwenden, wählen Sie 51 aus.  
7. Geben Sie im Feld Standort einen Wert ein.
    * Wählen Sie einen gültigen Lagerplatz im Lagerort aus, den Sie ausgewählt haben. Der Lagerplatz muss einem Lagerplatzprofil zugeordnet sein, der über Ladungsträger gesteuert wird. Dieses dient als Standardwert, der für alle Positionen der Erfassung gilt. Wenn Sie die Beispielswerte in USMF verwenden, wählen Sie Bulk 008 aus.  
8. Klicken Sie mit rechts auf den Dropdownpfeil im Feld "Ladungsträger" wählen Sie dann "Details anzeigen" aus.
9. Klicken Sie auf "Neu".
10. Geben Sie im Feld "Ladungsträger" einen Wert ein.
    * Notieren Sie den Wert.  
11. Klicken Sie auf "Speichern".
12. Schließen Sie die Seite.
13. Geben Sie im Feld "Ladungsträger" einen Wert ein.
    * Geben Sie den Wert des Ladungsträgers ein, den Sie soeben erstellt haben. Dieses dient als Standardwert, der für alle Positionen der Erfassung gilt.  
14. Klicken Sie auf "OK".

## <a name="add-a-line"></a>Hinzufügen einer Line
1. Klicken Sie auf "Position hinzufügen".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein.
    * Geben Sie die Artikelnummer ein, die Sie in der Bestellposition verwendet haben.  
3. Geben Sie im Feld "Menge" eine Zahl ein.
    * Geben Sie die Menge ein, die Sie erfassen möchten.  
    * Das Datumsfeld bestimmt das Datum, an dem die verfügbare Menge dieses Artikels im Bestand erfasst wird.  
    * Die Loskennung wird vom System ausgefüllt, wenn sie über die bereitgestellten Informationen eindeutig identifiziert werden kann. Andernfalls müssen Sie sie manuell hinzufügen. Dies ist ein Pflichtfeld, das diese Erfassung mit einer bestimmten Quelldokumentposition verknüpft.  

## <a name="complete-the-registration"></a>Abschließen der Erfassung
1. Klicken Sie auf "Überprüfen".
    * Dies überprüft, ob die Erfassung für die Buchung bereit ist. Wenn die Prüfung fehlschlägt, müssen Sie die Fehler korrigieren, bevor Sie die Erfassung buchen können.  
2. Klicken Sie auf "OK".
    * Nachdem Sie auf "OK" geklickt haben, überprüfen Sie die Mitteilung. Es sollte eine Nachricht geben, die darauf hinweist, dass die Erfassung Ok ist.  
3. Klicken Sie auf "Buchen".
4. Klicken Sie auf "OK".
    * Nachdem Sie auf "OK" geklickt haben, überprüfen Sie die Statusleiste. Es sollte eine Nachricht geben, die darauf hinweist, dass der Vorgang abgeschlossen wurde.  
5. Schließen Sie die Seite.

