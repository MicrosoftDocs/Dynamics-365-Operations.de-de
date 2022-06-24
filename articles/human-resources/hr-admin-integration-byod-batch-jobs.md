---
title: Optimieren Sie geplante BYOD-Batchaufträge
description: In diesem Artikel wird erläutert, wie Sie die Leistung optimieren, wenn Sie die BYOD-Funktion (Bring Your Own Database = eigene Datenbank nutzen) mit Microsoft Dynamics 365 Human Resources verwenden.
author: twheeloc
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4df60a82e016ec8f3ba6ba0d70c261824961d221
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848312"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Optimieren Sie geplante BYOD-Batchaufträge


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel wird erläutert, wie Sie die Leistung optimieren, wenn Sie die BYOD-Funktion (Bring Your Own Database = eigene Datenbank nutzen) verwenden. Weitere Informationen zu BYOD finden Sie unter [Eigene Datenbank nutzen (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Leistungsüberlegungen für den Datenexport

Nachdem Entitäten in der Zieldatenbank veröffentlicht wurden, können Sie die Exportfunktion im Arbeitsbereich **Datenverwaltung** verwenden, um Daten zu verschieben. Mit der Exportfunktion können Sie einen Datenverschiebungsauftrag definieren, der eine oder mehrere Entitäten enthält. Weitere Informationen über den Datenexport finden Sie unter [Übersicht über Datenimport- und -exportaufträge](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Sie können die Seite **Export** benutzen, um Daten in verschiedene Zieldatenformate zu exportieren, wie z. B. eine Datei mit durch Komma getrennten Werten (CSV). Diese Seite unterstützt auch SQL-Datenbanken als weiteres Ziel.

Sie können ein Datenprojekt mit mehreren Entitäten erstellen und mithilfe eines Batchauftrags die Ausführung des Datenprojekts planen. Wenn Sie die Option **In Batch exportieren** auswählen, können Sie den Datenexportauftrag so planen, dass er periodisch ausgeführt wird.

Um die allgemeine Zuverlässigkeit des BYOD-Exports zu gewährleisten, müssen Sie vorsichtig sein, wenn Sie einem Exportprojekt mehrere Entitäten hinzufügen. Berücksichtigen Sie beim Festlegen der Anzahl der Entitäten, die demselben Projekt hinzugefügt werden sollen, die folgenden Parameter:

- Die Komplexität der Entitäten
- Das erwartete Datenvolumen pro Entität
- Die Gesamtzeit, die erforderlich ist, um den Export auf Auftragsebene abzuschließen

Vermeiden Sie für eine optimale Leistung das Hinzufügen von Hunderten von Entitäten zu einem einzelnen Projekt. Wir empfehlen, dass Sie mehrere Aufträge erstellen, von denen jeder weniger Entitäten enthält.

## <a name="scheduling-byod-batch-jobs"></a>Planen von BYOD-Batchaufträgen

Um die Auswirkungen auf Benutzer von Microsoft Dynamics 365 Human Resources zu verringern, führen Sie BYOD-Batchaufträge nachts oder außerhalb der Geschäftszeiten aus. Überprüfen Sie unbedingt die Zeitzone für sich wiederholenden Batchaufträge. Einige Batch-Jobs verwenden möglicherweise Pacific Standard Time (PST).

Berücksichtigen Sie beim Konfigurieren der Planungshäufigkeit für BYOD-Batchaufträge die folgenden Faktoren, um Leistungsprobleme zu vermeiden:

- Die Zeit, die erforderlich ist, um jeden Batchauftrag abzuschließen
- Der Geschäftsbedarf für die Daten in BYOD

Legen Sie die Häufigkeit für jeden Batchauftrag auf einen Wert ein, der sicherstellt, dass der Auftrag lange vor seiner nächsten geplanten Laufzeit abgeschlossen werden kann. Vermeiden Sie es, mehrere Jobs gleichzeitig auszuführen, da dieser Ansatz die Leistung von Human Resources beeinträchtigen kann.

Verwenden Sie für die beste Leistung immer die Option **In Batch exportieren** auf der Seite **Export** zum Planen von BYOD-Batchaufträgen. Vermeiden Sie es, wiederkehrende Exporte zu planen unter **Verwalten \> Wiederkehrende Datenaufträge verwalten**.

## <a name="incremental-export"></a>Inkrementeller Export

Wenn Sie eine Entität für den Datenexport hinzufügen, können Sie entweder einen inkrementellen Push (Export) oder einen vollständigen Push ausführen. Ein vollständiger Push löscht alle vorhandenen Datensätze aus einer Entität in der BYOD-Datenbank. Anschließend werden die aktuellen Datensätze aus der Human Resources-Entität eingefügt.

Um einen inkrementellen Push durchzuführen, müssen Sie die Änderungsnachverfolgung für jede Entität auf der Seite **Entitäten** aktivieren. Weitere Informationen finden Sie unter [Änderungsnachverfolgung für Entitäten aktivieren](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Wenn Sie einen inkrementellen Push auswählen, ist der erste Push immer ein vollständiger Push. SQL verfolgt Änderungen von diesem ersten vollständigen Push nach. Wenn ein neuer Datensatz eingefügt oder ein Datensatz aktualisiert oder gelöscht wird, wird die Änderung in der Zielentität wiedergegeben.

## <a name="time-outs"></a>Timeouts

Hier sind die Standardtimeouts für BYOD-Exporte:

- Zehn Minuten für Kürzungsvorgänge
- Eine Stunde für Masseneinfügevorgänge

Bei großem Datenvolumen sind diese Timeout-Einstellungen möglicherweise nicht ausreichend. Um sie zu aktualisieren, gehen Sie zu **Datenverwaltung \>Framework-Parameter \> Eigene Datenbank nutzen**. Diese Timeouts sind unternehmensspezifisch und müssen für jedes Unternehmen separat festgelegt werden.

## <a name="known-limitations"></a>Bekannte Einschränkungen

Die BYOD-Funktion hat die folgenden Einschränkungen:

- Während der Synchronisierung sollten keine aktiven Sperren für Ihre Datenbank vorhanden sein. Aktive Sperren können zu langsamen Schreibvorgängen führen oder sogar dazu, dass Daten nicht in Ihre Azure SQL-Datenbank exportiert werden.
- Sie können keine zusammengesetzten Entitäten in Ihre eigene Datenbank exportieren. Derzeit werden zusammengesetzte Entitäten nicht unterstützt. Sie müssen einzelne Entitäten exportieren, aus denen die zusammengesetzte Entität besteht. Sie können jedoch beide Entitäten in dasselbe Datenprojekt exportieren.
- Entitäten ohne eindeutige Schlüssel können nicht mithilfe von inkrementellem Push exportiert werden. Diese Einschränkung kann auftreten, insbesondere wenn Sie versuchen, Datensätze von einigen vorgefertigten Entitäten schrittweise zu exportieren. Da diese Entitäten für den Import von Daten konzipiert wurden, verfügen sie nicht über einen eindeutigen Schlüssel.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="incremental-push-doesnt-work-correctly"></a>Inkrementeller Push funktioniert nicht richtig

**Problem:** Wenn für eine Entität ein vollständiger Push ausgeführt wird, wird in BYOD eine große Anzahl von Datensätzen angezeigt, wenn Sie eine **Auswählen**-Anweisung verwenden. Wenn Sie jedoch einen inkrementellen Push ausführen, werden in BYOD nur wenige Datensätze angezeigt. Es scheint, als hätte der inkrementelle Push alle Datensätze gelöscht und nur die geänderten Datensätze in BYOD hinzugefügt.

**Lösung:** Die SQL-Änderungsnachverfolgungstabellen befinden sich möglicherweise nicht im erwarteten Status. In Fällen dieses Typs empfehlen wir, die Änderungsnachverfolgung für die Entität zu deaktivieren und dann wieder zu aktivieren. Weitere Informationen finden Sie unter [Änderungsnachverfolgung für Entitäten aktivieren](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Staging-Tabellen werden nicht geleert

**Problem:** Bei der Verwendung von Staging für das Projekt werden die Staging-Tabellen nicht korrekt geleert. Die Daten in den Tabellen wachsen dann weiter an, was zu Leistungsproblemen führt.

**Lösung:** In den Staging-Tabellen wird eine Historie von sieben Tagen geführt. Historische Daten, die älter als sieben Tage sind, werden durch den Batchauftrag **Bereinigung des Import-Export-Stagings** automatisch aus den Staging-Tabellen gelöscht. Wenn dieser Auftrag stecken bleibt, werden die Tabellen nicht korrekt gelöscht. Wenn Sie diesen Batchauftrag neu starten, wird der Prozess zum automatischen Löschen der Staging-Tabellen fortgesetzt.

## <a name="see-also"></a>Siehe auch

[Datenverwaltung – Übersicht](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Eigene Datenbanken nutzen (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Einzelvorgänge für Datenimport und ‑export – Übersicht](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Aktivieren der Nachverfolgung von Änderungen an Entitäten](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
