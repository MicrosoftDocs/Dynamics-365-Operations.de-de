---
title: Sachkontoausgleiche
description: In diesem Thema wird erläutert, wie die Sachkontoausgleichseite verwendet wird, um Sachkontobuchungen und Stornierungs-Ausgleiche auszugleichen.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443487"
---
# <a name="ledger-settlements"></a>Sachkontoausgleiche

[!include [banner](../includes/banner.md)]

Mit dem Sachkontoausgleich können Sie Haben- und Solltransaktionen im Hauptbuch abgleichen und Sie als ausgeglichen markieren. Auf diese Weise können Sie sicherstellen, dass zugehörige Buchungen gelöscht wurden. Sie können einen Ausgleich auch stornieren, wenn er versehentlich vorgenommen wurden.

## <a name="enable-advanced-ledger-settlements"></a>Erweiterter Sachkontoausgleich aktivieren

Die erweiterte Sachkontoausgleichseite enthält zusätzliche Funktionalität zum Filtern und Auswählen von Buchungen. Um die erweiterte Sachkontoausgleichseite zu aktivieren, gehen Sie folgendermaßen vor.

1. Wechseln Sie zu **Hauptbuch**\>**Hauptbucheinstellungen**\>**Allgemeine Hauptbuchparameter**. 
2. Auf der Registerkarte **Sachkontoausgleiche** legen Sie die Option **Erweiterter Sachkontoausgleich** auf **Ja** fest und aktivieren Sie die erweiterte Sachkontoausgleichfunktion. Die erweiterte Seite **Sachkontoausgleiche** wird verwendet, wenn Sie **Sachkontoausgleiche** unter **Periodische Aufgaben** ausgewählt haben. 
3. Sie müssen die Liste von Konten zur Verwendung für Sachkontoausgleiche für jeden Kontenplan eingeben. Diese Liste wird verwendet, um die Liste der Buchungen zu filtern, die auf der Seite **Sachkontoausgleiche** angezeigt wird. In der **Kontenplan**-Liste wählen Sie einen Kontenplan aus, und wählen Sie dann **Neu**, um neue Konten der Liste hinzuzufügen.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Hierüber können Sie Buchungen ausgleichen, indem Sie die erweiterte Sachkontoausgleichseite verwenden

Um Sachkontobuchungen auszugleichen, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Hauptbuch** \> **Periodische Aufgaben** \> **Sachkontoausgleiche**.
2. Setzen Sie die Filter oben auf der Seite fest:

    - Wählen Sie einen Datumsbereich aus oder wählen Sie **Datumsintervallcode** aus, um den Datumsbereich automatisch auszufüllen.
    - Ändern Sie die Buchungsebene nach Wunsch.
    - Wenn das Sachkonto und Dimensionen separat angezeigt werden sollen, wählen Sie einen Finanzdimensionssatz aus.

3. Wählen Sie **Buchungen anzeigen**, um alle Buchungen anzuzeigen, die mit den Filtern und den  Kontenlisten übereinstimmen, die Sie festgelegt haben, als Sie die Kontenplanliste im vorherigen Abschnitt eingerichtet haben. Wenn Sie Filter- oder Dimensionseinstellungen ändern, müssen Sie **Buchungen anzeigen** wieder aktivieren.
4. Wählen Sie eine oder mehrere Positionen aus, die Sie für die Einrichtung auswählen. Der Wert des Felds **Ausgewählter Betrag** am oberen Seitenrand wird um die Zeilen erweitert oder verringert, die Sie ausgewählt haben.
5. Nachdem Sie alle Transaktionen ausgewählt haben, wählen Sie **Ausgewählte markieren** aus. Ein Häkchen wird in der Spalte **Markiert** für jede Buchung gesetzt, die Sie ausgewählt haben. Zusätzlich wird der Wert des Felds **Ausgewählter Betrag** am oberen Seitenrand um die Zeilen erweitert oder verringert, die Sie ausgewählt haben.
6. Wenn der **Markierter Betrag**-Wert **0** (Null) ist, wählen Sie **Markierte Transaktionen begleichen** aus. Der Status der markierten Transaktionen wird auf **Ausgeglichen** geändert.

## <a name="make-transactions-easier-to-find"></a>Suchen Sie Transkaktionen einfacher

Die Seite **Sachkontoausgleiche** enthält Funktionen, die es einfacher machen, die Transaktionen zu sehen, die Sie für den Ausgleich benötigen.

- Die Schaltfläche **Ausgewählte abwählen** deaktiviert das Feld **Markiert** für alle Positionen, die ausgewählt sind.
- Mit dem Filter **Markiert** können Sie Transaktionen auf der Grundlage filtern, ob das Feld für **Markiert** aktiviert oder deaktiviert ist.
- Mit dem **Status** Filter können Sie Buchungen auf Grundlage filtern, ob Status **Ausgeglichen** oder **Nicht ausgeglichen** ist.
- Mit der Schaltfläche **Sortieren nach absolutem Betrag** können Sie die Beträge nach absolutem Wert sortieren, sodass Sie Soll- und Habenbeträge gruppieren können, die den gleichen Betrag haben.

## <a name="reverse-a-settlement"></a>Ausgleich stornieren

Sie können einen Ausgleich stornieren, die versehentlich vorgenommen wurde.

1. Führen Sie die Schritte 1 bis 3 unter "Transaktionen ausgleichen" durch, indem Sie die Seite  "Sachkontoausgleichseite " verwenden, um die Buchungen zu veranschaulichen, die Sie suchen.
2. Wählen Sie im Feld **Status** die Option **ausgeglichen** aus.
3. Wählen Sie eine oder mehrere Positionen aus, die Sie für die Stornierung auswählen. Der Wert des Felds **Ausgewählter Betrag** am oberen Seitenrand wird um die Zeilen erweitert oder verringert, die Sie ausgewählt haben.
4. Nachdem Sie alle Transaktionen ausgewählt haben, wählen Sie **Ausgewählte markieren** aus. Ein Häkchen wird in der Spalte **Markiert** für jede Buchung gesetzt, die Sie ausgewählt haben. Zusätzlich wird der Wert des Felds **Ausgewählter Betrag** am oberen Seitenrand um die Zeilen erweitert oder verringert, die Sie ausgewählt haben.
5. Wenn der **Markierter Betrag**-Wert **0** (Null) ist, wählen Sie **Markierte Transaktionen stornieren** aus. Der Status der markierten Transaktionen wird auf **Nicht Ausgeglichen** geändert.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Aktualisiert die Liste mit Konten, die in der Liste der Transaktionen einbezogen werden

Wählen Sie **Sachkontoausgleichverrechnungskonten**, um ein Dialogfeld zu öffnen, in dem Sie die Konten bearbeiten können, die in der Liste der Transaktionen einbezogen werden. Wählen Sie **Neu** aus, um neue Konten der Liste hinzuzufügen. Diese Liste wird verwendet, um die Liste der Buchungen zu filtern, die auf der Seite **Sachkontoausgleiche** angezeigt wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]