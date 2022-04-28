---
title: Datenbereinigung der Verkaufshistorie planen
description: In diesem Thema wird beschrieben, wie Sie zur Verbesserung der Systemleistung beitragen können, indem Sie die regelmäßige Bereinigung der Verkaufsaktualisierungshistorie so planen, dass sie in regelmäßigen Abständen ausgeführt wird.
author: myvakalo
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6c6c1e08d45f2a7d1e1267010b286111bad01a6c
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570365"
---
# <a name="schedule-sales-history-data-cleanup"></a>Datenbereinigung der Verkaufshistorie planen

[!include [banner](../includes/banner.md)]

Im Rahmen des Standardbetriebs generiert und speichert Microsoft Dynamics 365 Supply Chain Management laufend Aktualisierungsdaten der Verkaufshistorie. Im Laufe der Zeit kann sich in Ihrem System eine große Menge veralteter Verkaufshistoriendaten ansammeln. Diese gesammelten Daten können zu Leistungs- und Funktionsproblemen führen, wenn Belege gebucht werden, die sich auf Aufträge beziehen. (Zu diesen Dokumenten gehören Auftragsbestätigungen, Lieferscheine, Kommissionierlisten und Rechnungen). Daher sollten Sie die periodische Aufgabe *Bereinigung der Verkaufsaktualisierungshistorie* einrichten und so planen, dass sie in regelmäßigen Abständen ausgeführt wird. Diese Aufgabe entfernt alle Aktualisierungsdaten der Verkaufshistorie, die nicht mehr benötigt werden.

Wenn Sie die generische Aufgabe *Bereinigung der Verkaufsaktualisierungshistorie* verwenden, empfehlen wir, dass Sie die Funktion *Verbesserungen an der Leistung der Verkaufshistorienbereinigung* aktivieren, wodurch die Aufgabe effektiver ausgeführt wird. (Sie können die Aufgabe aber auch ausführen, ohne diese Funktion zu aktivieren.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Funktionen zur Bereinigung der Verkaufshistorie aktivieren

Zum Einrichten und Verwenden der periodischen Aufgabe *Bereinigung der Verkaufsaktualisierungshistorie* zusammen mit allen Features, die in diesem Thema beschrieben werden, müssen Sie die Funktionen *Verbesserungen an der Leistung der Verkaufshistorienbereinigung* und *Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen* in der Funktionsverwaltung aktivieren, wie in den folgenden Unterabschnitten beschrieben.

### <a name="sales-history-cleanup-performance-improvements"></a>Verbesserungen an der Leistung der Verkaufshistorienbereinigung

Der regelmäßige Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** kann lange dauern, wenn er in Umgebungen mit einem hohen Volumen an Verkaufsaktualisierungen nur selten ausgeführt wird. In diesen Situationen kann die Funktion *Verbesserungen an der Leistung der Verkaufshistorienbereinigung* dazu beitragen, die Laufzeit zu verkürzen und die Zuverlässigkeit zu verbessern.

Die Funktion verbessert den vorhandenen Bereinigungsauftrag auf folgende Weise:

- Sie teilt die Bereinigung in Stapel auf (Sie können die Stapelgröße durch Anpassungen ändern).
- Es läuft maximal 2 Stunden (Sie können die Dauer durch Anpassungen ändern).
- Wenn möglich werden Datenbankfunktionen genutzt, um Sperrkonflikte zu minimieren und das Verbinden von Transaktionstabellen während der Bereinigung zu vermeiden.

Nachdem Sie die Funktion aktiviert haben, wird der Batchauftrag **Aktualisierungshistorie für Verkauf bereinigen** (**Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigung \> Aktualisierungshistorie für Verkauf bereinigen**) wie zuvor ausgeführt, jedoch mit besserer Leistung und für maximal 2 Stunden. Dies bedeutet, dass er möglicherweise mehrmals ausgeführt werden muss, um alle Daten für einen bestimmten Aufbewahrungszeitraum zu bereinigen.

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Vertrieb und Marketing*
- **Funktionsname:** *Verbesserungen an der Leistung der Verkaufshistorienbereinigung*

### <a name="clean-up-sales-update-history-based-on-age"></a>Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen

Mit der Funktion *Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen* können Sie das maximale Alter von Datensätzen festlegen, die aufbewahrt werden sollen, wenn die periodische Aufgabe *Bereinigung der Verkaufsaktualisierungshistorie* ausgeführt wird. Ältere Datensätze werden gelöscht. Dies ist nützlich, wenn Sie die regelmäßige Ausführung der Aufgabe festlegen, da das Alter immer relativ zum Ausführungsdatum der Aufgabe berechnet wird. Ohne diese Funktion können Sie nur ein bestimmtes Datum für die ältesten Aufzeichnungen festlegen, die aufbewahrt werden sollen.

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Vertrieb und Marketing*
- **Funktionsname:** *Aktualisierungsverlauf für Verkauf basierend auf Alter bereinigen*

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Regelmäßige Aufgabe zur Bereinigung der Verkaufshistorie einrichten und planen

Um die regelmäßige Aufgabe *Bereinigung der Verkaufshistorie* einzurichten und zu planen, führen Sie die folgenden Schritte aus.

1. Analysieren Sie Ihre geschäftlichen Anforderungen, um zu bestimmen, wie viele Tage Sie historische Auftragsbuchungsdaten aufbewahren müssen. Wir empfehlen normalerweise, die Bereinigungsaufgabe alle drei Monate und maximal alle sechs Monate auszuführen.
1. Gehen Sie zu **Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigung \> Bereinigung der Verkaufsaktualisierungshistorie**.
1. Legen Sie im Dialogfeld **Bereinigung der Verkaufsaktualisierungshistorie** auf dem Inforegister **Parameter** die folgenden Felder fest:

    - **Bereinigen** – Wählen Sie einen der folgenden Werte aus, um die Art der zu bereinigenden Datensätze anzugeben:

        - **Ausgeführt** – Nur vollständig bearbeitete Sätze löschen. Da Sie diese Datensätze wahrscheinlich nicht weiter verwenden werden, ist diese Option die sicherste.
        - **Ausgeführt und fehlerhaft** – Sowohl vollständig verarbeitete Datensätze als auch Datensätze löschen, bei denen ein Fehler aufgetreten ist. Diese Option wird am häufigsten verwendet. Möglicherweise möchten Sie fehlerhafte Datensätze überprüfen und sogar korrigieren, anstatt sie automatisch bereinigen zu lassen. Viele Unternehmen entscheiden sich jedoch dafür, diese Aufzeichnungen nach etwa einem Monat ebenfalls zu bereinigen, da sie zu diesem Zeitpunkt wahrscheinlich nicht mehr relevant sind.
        - **Alle** – Ausgeführte, fehlerhafte und wartende Datensätze löschen. Wartende Datensätze sind gültig, wurden aber noch nicht vollständig verarbeitet. In den meisten Fällen möchten Sie wahrscheinlich nicht, dass sie automatisch gelöscht werden. In einigen Situationen können Sie sich jedoch dafür entscheiden, dass sie nach Ablauf einer bestimmten Zeit automatisch gelöscht werden.

    - **Datensätze nach Alter aufbewahren** – Geben Sie an, ob Sie Datensätze basierend auf ihrem Alter am Ausführungstag der Aufgabe bereinigen oder Datensätze löschen möchten, die vor einem festgelegten Datum erstellt wurden. Wenn Sie die Bereinigung als wiederkehrende Aufgabe planen, sollten Sie diese Option auf *Ja* einstellen, da das Alter immer relativ zum Ausführungsdatum der Aufgabe berechnet wird.

        - Setzen Sie diese Option auf *Ja*, um das Feld **Max. Alter** zu aktivieren. Sie verwenden dieses Feld, um das maximale Alter der Datensätze anzugeben, die bei jeder Ausführung der Aufgabe aufbewahrt werden sollen. Das Feld **Erstellt bis** wird ignoriert.
        - Setzen Sie diese Option auf *Nein*, um das Feld **Erstellt bis** zu aktivieren. Sie verwenden dieses Feld, um das älteste Erstellungsdatum der Datensätze anzugeben, die bei der Ausführung der Aufgabe aufbewahrt werden sollen. Das Feld **Max. Alter** wird ignoriert.

    - **Erstellt bis** – Diese Einstellung gilt nur, wenn die Option **Datensätze nach Alter aufbewahren** auf *Nein* festgelegt ist. Geben Sie das älteste Erstellungsdatum der Datensätze an, die bei der Ausführung der Aufgabe aufbewahrt werden sollen. Datensätze, die vor diesem Datum erstellt wurden, werden gelöscht.
    - **Max. Alter** – Diese Einstellung gilt nur, wenn die Option **Datensätze nach Alter aufbewahren** auf *Ja* festgelegt ist. Geben Sie (in Tagen) das maximale Alter der Datensätze anzugeben, die bei jeder Ausführung der Aufgabe aufbewahrt werden sollen. Ältere Datensätze werden gelöscht.

1. Im Inforegister **Im Hintergrund ausführen** geben Sie an, wie, wann und wie oft die Aufgabe ausgeführt werden soll. Verwenden Sie diese Einstellungen, um den Zeitplan zu implementieren, den Sie in Schritt 1 festgelegt haben. Die Felder funktionieren genauso wie bei anderen Arten von [Stapelverarbeitungsaufträgen](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und das Dialogfeld zu schließen.
