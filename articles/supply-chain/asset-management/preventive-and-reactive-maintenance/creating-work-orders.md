---
title: Erstellen von Arbeitsaufträgen
description: In diesem Artikel wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba01a90f805300a27e4550e1371fb55d5e3a7536
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335044"
---
# <a name="creating-work-orders"></a>Erstellen von Arbeitsaufträgen

[!include [banner](../../includes/banner.md)]

Nachdem Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für diese zu erstellen. Sie können diesen Schritt mithilfe eines der Wartungszeitpläne ausführen. Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben, wie in der folgenden Tabelle beschrieben.

| Referenztyp | Beschreibung |
|---|---|
| Wartungspläne | Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen *Zeit* oder *Zähler*. |
| Wartungsdurchgänge | Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern. |
| Wartungsanfrage | Eine manuell erstellte Anforderung zur Wartung oder Reparatur einer Anlage. Diese Anforderung kann in einen Arbeitsauftrag konvertiert werden. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Erstellen von Arbeitsaufträgen basierend auf Ihrem Wartungsplan

Führen Sie die folgenden Schritte aus, um Arbeitsaufträge zu erstellen, die auf Ihrem Wartungsplan basieren.

1. Öffnen Sie eine der folgenden Seiten, je nachdem, wie Sie Zeitplanelemente für Ihre Arbeitsaufträge auswählen möchten:

    - Alle Wartungszeitpläne (**Anlagenerwaltung \> Verwaltungszeitplan \> Alle Wartungszeitpläne**)
    - Offene Wartungszeitplanpositionen (**Anlagenerwaltung \> Verwaltungszeitplan \> Offene Wartungszeitplanpositionen**)
    - Offene Wartungszeitplanpools (**Anlagenerwaltung \> Verwaltungszeitplan \> Offene Wartungszeitplanpools**)

1. Aktivieren Sie im Raster das Kontrollkästchen für jeden geplanten Wartungsauftrag, für den Sie einen Arbeitsauftrag erstellen möchten. Wählen Sie im Aktionsbereich **Arbeitsauftrag**.

    Das Dialogfeld **Arbeitsaufträge erstellen** wird angezeigt. Die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen wird im Feld **Wartungsprognosestunden** angezeigt.

    ![Das Dialogfeld „Arbeitsaufträge erstellen“.](media/18-preventive-maintenance.png)

1. Im Abschnitt **Parameter** geben Sie die Anzahl der Arbeitsaufträge an, die erstellt werden sollen. Folgende Optionen stehen zur Auswahl:

    - **Ein Arbeitsauftrag pro Position** – Erstellen Sie einen Arbeitsauftrag pro Wartungszeitplanposition.
    - **Ein Arbeitsauftrag pro** – Erstellen Sie Arbeitsaufträge, die gemäß den Einstellungen der anderen Optionen gruppiert sind, die verfügbar werden, wenn Sie diese Option auswählen.

1. In dem Feld **Arbeitsauftragstyp** wählen Sie den Arbeitsauftragstyp aus, der für alle von Ihnen erstellten Arbeitsaufträge verwendet werden soll.
1. Wählen Sie **OK** aus, um die Arbeitsaufträge gemäß Ihren Einstellungen zu erstellen.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Gruppieren Sie Arbeitsauftragspositionen, die automatisch erstellt werden, während ein Wartungszeitplan ausgeführt wird.

Mit dieser Funktion können Sie Regeln für die Gruppierung von Arbeitsauftragspositionen unter einem einzelnen Arbeitsauftrag definieren, wenn das System so eingerichtet ist, dass Arbeitsaufträge basierend auf einem Wartungszeitplan automatisch generiert werden. Bisher konnten automatisch generierte Arbeitsaufträge nur eine Position enthalten. Sie können Arbeitsaufträge jetzt jedoch beispielsweise nach Anlage, Anlagentyp oder funktionalem Standort gruppieren. (Manuell erstellte Arbeitsaufträge können bereits auf diese Weise gruppiert werden, wie im vorherigen Abschnitt dieses Artikels beschrieben.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Aktivieren der Gruppierung für automatisch generierte Arbeitsaufträge

Bevor Sie diese Funktion nutzen können, muss sie für Ihr System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Anlagenverwaltung*
- **Funktionsname:** *Regeln zum Gruppieren von Arbeitsaufträgen während der Ausführung eines Wartungsplans anwenden*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Einrichten der Gruppierung für automatisch generierte Arbeitsaufträge

Um die Gruppierung für automatisch generierte Arbeitsaufträge einzurichten, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Anlagenverwaltung \> Einrichtung \> Vorbeugende Wartung \> Wartungszeitpläne**.
1. Führen Sie für jeden Plan, in dem Sie gruppierte Arbeitsaufträge generieren möchten, die folgenden Schritte aus:

    1. Wählen Sie im Listenbereich den Plan aus.
    1. Auf dem Inforegister **Positionen** stellen Sie sicher, dass das Kontrollkästchen **Automatisch einrichten** in jeder Position aktiviert ist.

1. Wechseln Sie zu **Anlagenverwaltung \> Periodisch \> Vorbeugende Wartung \> Wartungspläne terminieren**.
1. In dem Dialogfeld **Wartungspläne terminieren** im Abschnitt **Periode** geben Sie den Zeithorizont für den Plan an (wie weit Sie nach vorne schauen müssen, wenn Sie geplante Wartungszeitpläne finden, für die Arbeit generiert werden soll).
1. Stellen Sie Option **Arbeitsauftrag automatisch aus Zeitplan erstellen** auf *Ja*.
1. Wählen Sie im Abschnitt **Arbeitsauftrag** eine der folgenden Optionen aus:

    - **Ein Arbeitsauftrag pro Position** – Erstellen Sie einen Arbeitsauftrag pro Wartungszeitplanposition. (Diese Option bietet die gleiche Funktionalität, die verfügbar ist, wenn die Funktion *Regeln zum Gruppieren von Arbeitsaufträgen während der Ausführung eines Wartungsplans anwenden* ausgeschaltet ist.)
    - **Ein Arbeitsauftrag pro** – Erstellen Sie Arbeitsaufträge, die gemäß den Einstellungen der anderen Optionen gruppiert sind, die verfügbar werden, wenn Sie diese Option auswählen.

1. Wenn Sie möchten, dass die Optionen angewendet werden, wenn Sie nur einige Ihrer Wartungspläne ausführen, klicken Sie auf das Inforegister **Einzuschließende Datensätze**, fügen Sie Filter nach Bedarf hinzu, genau wie bei anderen Stapelverarbeitungsaufträgen in Microsoft Dynamics 365 Supply Chain Management.
1. Richten Sie auf dem Inforegister **Im Hintergrund ausführen** Stapel- und Planungsoptionen nach Bedarf ein, genau wie bei anderen Stapelverarbeitungsaufträgen in Supply Chain Management.
1. Wählen **OK**, um die ausgewählten Wartungszeitpläne auszuführen und/oder zu planen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]