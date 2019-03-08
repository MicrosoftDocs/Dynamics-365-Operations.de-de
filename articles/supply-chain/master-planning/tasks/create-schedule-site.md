---
title: Einen Zeitplan für einen Standort erstellen
description: Diese Prozedur zeigt, wie Produktionsaufträge geplant werden sollen, die noch nicht für einen Standort gestartet wurden.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54bb2532534d5567239dad4fab7fd74fa50d2826
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "330056"
---
# <a name="create-a-schedule-for-a-site"></a>Einen Zeitplan für einen Standort erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Produktionsaufträge geplant werden sollen, die noch nicht für einen Standort gestartet wurden.  Das Demodatenunternehmen USMF wird verwendet, um diese Prozedur abzuschließen.


## <a name="identify-production-orders-that-are-not-started"></a>Identifizieren Sie Produktionsaufträge, die noch nicht gestartet wurden.
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise zum Feld "Standort" mit einem Wert von "1".
    * 1 stellt einen Standort in USMF dar. Wenn Sie nicht USMF verwenden, wählen Sie eine Standort von Ihrem eigenen Unternehmen aus.  
3. Öffnen Sie den Spaltenfilter "Status".
4. Wenden Sie einen Filter für das Feld "Status" an, mit einem Wert "Eingeplant", mithilfe des Filteroperators "ist genau".

## <a name="create-a-schedule"></a>Erstellen Sie einen Zeitplan
1. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
2. Klicken Sie im Aktivitätsbereich auf "Zeitplan".
3. Klicken Sie auf "Einzelvorgänge planen".
4. Wählen Sie im Feld Planungsrichtung "Rückwärts ab Lieferdatum" aus.
5. Wählen Sie "Nein" im Feld "Begrenzte Kapazität" aus.
6. Wählen Sie "Nein" im Feld "Begrenztes Material" aus.
7. Klicken Sie auf "OK".
    * Dies kann einige Zeit in Anspruch nehmen.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Zeigen Sie das Ergebnis geplanter Produktionsaufträge an.
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * Sie können jede beliebige Zeile markieren.  
2. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
3. Klicken Sie auf "Alle Einzelvorgänge".
    * Auf dieser Seite können Sie die Liste der Einzelvorgänge anzeigen. Auf der Registerkarte "Planung" können Sie das Start- und Enddatum für einen Einzelvorgang anzeigen.  
4. Klicken Sie auf "Material".
    * Auf dieser Seite können Sie die vorkalkulierte Materialentnahme für die Arbeitsgänge im Produktionsauftrag und den aktuellen verfügbaren Bestand anzeigen.  

