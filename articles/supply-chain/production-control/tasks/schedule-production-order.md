---
title: Einen Produktionsauftrag planen
description: Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3fe8f6890c7d8ac8835503091642faa773f7f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428663"
---
# <a name="schedule-a-production-order"></a>Einen Produktionsauftrag planen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die dritte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.


## <a name="schedule-a-production-order"></a>Einen Produktionsauftrag planen
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
    * Wählen Sie einen Produktionsauftrag aus, der den Status "Vorkalkuliert" aufweist.  
2. Klicken Sie im Aktivitätsbereich auf "Zeitplan".
3. Klicken Sie auf Einzelvorgänge planen.
    * Die für die Planung eingerichteten Parameter werden auf dieser Seite angezeigt. Sie können die Parameter für bestimmte Benutzer oder alle Benutzer einrichten.  
4. Wählen Sie im Feld Planungsrichtung "Vorwärts ab Lieferdatum" aus.
5. Geben Sie ein Datum in das Feld "Planungsdatum" ein.
6. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenzte Kapazität".
7. Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenztes Material".
8. Klicken Sie auf "OK".

## <a name="view-the-scheduling-results"></a>Planungsergebnisse anzeigen
1. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
2. Klicken Sie auf "Alle Einzelvorgänge".
    * Auf dieser Seite werden die geplanten Einzelvorgänge angezeigt, die Sie gerade generiert haben.  
3. Erweitern oder reduzieren Sie den Abschnitt 'Planung'.
    * Im Planungs-Inforegister können Sie das geplante Datum und die Uhrzeit anzeigen.  
4. Klicken Sie auf Abfragen.
5. Klicken Sie"Kapazitätsauslastung"
    * Die Kapazitätsauslastungsseite stellt die Kapazitäten dar, die für die Feinterminierung reserviert sind, die Gesamtanzahl von Stunden, die zur Zeit für die Ressource reserviert werden und die Anzahl der Stunden ,die für die Feinterminierung der Ressource verfügbar sind.  
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]